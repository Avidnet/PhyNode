# PhyNode
## Introduction
Avidnet physical nodes send data with [CBOR](http://cbor.io/) format over LoRaWAN network.
To reduce message length the physical team at Avidnet decides to use numbers instead of the sensor's names.
Following structure introduces these numbers:

```c
typedef enum {
    SensorType_Temperature = 1,
    SensorType_Humidity,
    SensorType_Pressure,
    SensorType_SoilTemperature,
    SensorType_SoilMoisture,
    SensorType_Luminosity,
    SensorType_Radiation,
    SensorType_Pluviometer,
    SensorType_WindVane,
    SensorType_Anemometer,
    SensorType_PowerOfHydrogen,
    SensorType_Nitrate,
    SensorType_UltraViolet,

    SensorType_SoilWater = 0xF0,
    SensorType_Battery,
    SensorType_NodeTemperature,

    SensorType_Longitude = 0xF3,
    SensorType_Latitude,
    SensorType_Altitude,

    SensorType_AccelerometerX = 0xF6,
    SensorType_AccelerometerY,
    SensorType_AccelerometerZ,
    SensorType_GyroscopeX = 0xF9,
    SensorType_GyroscopeY,
    SensorType_GyroscopeZ,
    SensorType_MagnetometerX = 0xFC,
    SensorType_MagnetometerY,
    SensorType_MagnetometerZ,

    SensorType_RXDebug = 0xFF,
} SensorType;
```
