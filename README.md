# Practica-ESP32-con-DHT11
Este repositorio muestra como podemos programar una ESP32 con el sensor DHT11.

## Introducción
### Descripción
La ```Esp32``` la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (```DTH11```) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado WOKWI.

## Material Necesario
Para realizar esta practica necesitas lo siguiente

- [WOKWI](https://wokwi.com/)
- Tarjeta ESP 32
- Sensor DHT11
## Instrucciones
### Requisitos previos
Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://wokwi.com/).

### Instrucciones de preparación de entorno
1. Abrir la terminal de programación y colocar la siguente programación:

```
#include "DHTesp.h"
#include <LiquidCrystal_I2C.h>

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}
```

2. Instalar la libreria de DHT sensor library for ESPx como se muestra en la siguente imagen.
![](https://github.com/DaybeatAV/Practica-ESP32-con-DHT11/blob/main/Librer%C3%ADa%20DHT.png)

3.Hacer la conexion de DHT11 con la ESP32 como se muestra en la siguente imagen.
![](https://github.com/DaybeatAV/Practica-ESP32-con-DHT11/blob/main/Pr%C3%A1ctica%201%20Conexiones.png)

### Instrucciónes de operación
1.Iniciar simulador.

2.Visualizar los datos en el monitor serial.

3.Colocar la temperatura y humedad dando doble click al sensor DHT11

## Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.
![](https://github.com/DaybeatAV/Practica-ESP32-con-DHT11/blob/main/Pr%C3%A1ctica%201%20Funcionando.png)

### Evidencias
![](https://github.com/DaybeatAV/Practica-ESP32-con-DHT11/blob/main/Pr%C3%A1ctica%201%20Evidencias.mp4)

# Créditos

Desarrollado por **JOSE DAVID AYALA VILLALBA**

-[GITHUB]()
