

# Namespace CayenneLPP



[**Namespace List**](namespaces.md) **>** [**CayenneLPP**](namespaceCayenneLPP.md)




















## Classes

| Type | Name |
| ---: | :--- |
| struct | [**AcceleroVal\_t**](structCayenneLPP_1_1AcceleroVal__t.md) <br> |
| class | [**CayenneLPP**](classCayenneLPP_1_1CayenneLPP.md) &lt;static\_size&gt;<br> |
| struct | [**GPSCoord\_t**](structCayenneLPP_1_1GPSCoord__t.md) <br> |
| struct | [**GyroVal\_t**](structCayenneLPP_1_1GyroVal__t.md) <br> |
| struct | [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) <br> |


## Public Types

| Type | Name |
| ---: | :--- |
| typedef uint16\_t | [**AnalogGPIOVal\_t**](#typedef-analoggpioval_t)  <br> |
| typedef uint16\_t | [**BarometricPressure\_t**](#typedef-barometricpressure_t)  <br> |
| union  | [**MeasurementData\_t**](#union-measurementdata_t)  <br> |
| enum  | [**CayenneMeasurementType\_t**](#enum-cayennemeasurementtype_t)  <br> |
| typedef uint8\_t | [**DigitalGPIOVal\_t**](#typedef-digitalgpioval_t)  <br> |
| typedef float | [**Float32Val\_t**](#typedef-float32val_t)  <br> |
| typedef uint16\_t | [**LuminosityVal\_t**](#typedef-luminosityval_t)  <br> |
| typedef uint8\_t | [**PresenceVal\_t**](#typedef-presenceval_t)  <br> |
| typedef uint8\_t | [**RawBitVal\_t**](#typedef-rawbitval_t)  <br> |
| typedef uint8\_t | [**RawByteVal\_t**](#typedef-rawbyteval_t)  <br> |
| typedef uint16\_t | [**RelativeHumidity\_t**](#typedef-relativehumidity_t)  <br> |
| typedef uint16\_t | [**TemperatureVal\_t**](#typedef-temperatureval_t)  <br> |
| typedef uint16\_t | [**Word16Val\_t**](#typedef-word16val_t)  <br> |
| typedef uint32\_t | [**Word32Val\_t**](#typedef-word32val_t)  <br> |






















## Public Static Functions

| Type | Name |
| ---: | :--- |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**ResetMeasurement**](#function-resetmeasurement) () <br>_Clears currently used Measurement struct with invalid data._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetAcceleration**](#function-setacceleration) (const float x, const float y, const float z) <br>_Sets the acceleration values for the x, y, and z axes._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetAnalogInput**](#function-setanaloginput) (const float analog\_input\_val) <br>_Sets the analog input value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetAnalogOutput**](#function-setanalogoutput) (const float analog\_output\_val) <br>_Sets the analog output value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetBarometricPressure**](#function-setbarometricpressure) (const float barometric\_pressure\_val) <br>_Sets the barometric pressure value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetDigitalInput**](#function-setdigitalinput) (const uint8\_t digital\_input\_val) <br>_Sets the digital input value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetDigitalOutput**](#function-setdigitaloutput) (const uint8\_t digital\_output\_val) <br>_Sets the digital output value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetFloat32**](#function-setfloat32) (const float float32\_val) <br>_Sets a 32-bit floating-point value in a measurement._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetGPS**](#function-setgps) (const float latitude, const float longitude, const float altitude) <br>_Sets the GPS coordinates and altitude._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetGyro**](#function-setgyro) (const float x, const float y, const float z) <br>_Sets the gyroscopic values for the x, y, and z axes._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetLuminosity**](#function-setluminosity) (const float luminosity\_val) <br>_Sets the luminosity value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetPresence**](#function-setpresence) (const uint8\_t presence\_val) <br>_Sets the presence value._  |
|  void | [**SetRawBit**](#function-setrawbit) (const uint8\_t raw\_bit\_val, [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) \* prevMeasurement) <br>_Sets a raw bit value in a measurement._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetRawByte**](#function-setrawbyte) (const uint8\_t raw\_byte\_val) <br>_Sets a raw byte value in a measurement._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetRelativeHumidity**](#function-setrelativehumidity) (const float humidity\_val) <br>_Sets the relative humidity value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetTemperature**](#function-settemperature) (const float temperature\_val) <br>_Sets the temperature value._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetWord16**](#function-setword16) (const uint16\_t word16\_val) <br>_Sets a 16-bit word value in a measurement._  |
|  [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) | [**SetWord32**](#function-setword32) (const uint32\_t word32\_val) <br>_Sets a 32-bit word value in a measurement._  |


























## Public Types Documentation




### typedef AnalogGPIOVal\_t 

```C++
typedef uint16_t CayenneLPP::AnalogGPIOVal_t;
```






### typedef BarometricPressure\_t 

```C++
typedef uint16_t CayenneLPP::BarometricPressure_t;
```






### union MeasurementData\_t 

```C++

```






### enum CayenneMeasurementType\_t 

```C++
enum CayenneLPP::CayenneMeasurementType_t {
    MEASUREMENT_TYPE_INVALID = 255,
    MEASUREMENT_TYPE_DIGITAL_OUTPUT = 1,
    MEASUREMENT_TYPE_DIGITAL_INPUT = 0,
    MEASUREMENT_TYPE_RAWBIT_1 = 116,
    MEASUREMENT_TYPE_RAWBIT_2 = 117,
    MEASUREMENT_TYPE_RAWBIT_3 = 118,
    MEASUREMENT_TYPE_RAWBIT_4 = 119,
    MEASUREMENT_TYPE_RAWBIT_5 = 120,
    MEASUREMENT_TYPE_RAWBIT_6 = 121,
    MEASUREMENT_TYPE_RAWBIT_7 = 122,
    MEASUREMENT_TYPE_RAWBIT_8 = 123,
    MEASUREMENT_TYPE_RAWBYTE = 5,
    MEASUREMENT_TYPE_RAWWORD16 = 6,
    MEASUREMENT_TYPE_RAWWORD32 = 7,
    MEASUREMENT_TYPE_RAWFLOAT32 = 8,
    MEASUREMENT_TYPE_PRESENCE = 102,
    MEASUREMENT_TYPE_LUMINOSITY = 101,
    MEASUREMENT_TYPE_ANALOG_OUTPUT = 3,
    MEASUREMENT_TYPE_ANALOG_INPUT = 2,
    MEASUREMENT_TYPE_TEMPERATURE = 103,
    MEASUREMENT_TYPE_RELATIVE_HUMIDITY = 104,
    MEASUREMENT_TYPE_BAROMETRIC_PRESSURE = 115,
    MEASUREMENT_TYPE_ACCELERATION = 113,
    MEASUREMENT_TYPE_GYRO = 134,
    MEASUREMENT_TYPE_GPS = 136
};
```






### typedef DigitalGPIOVal\_t 

```C++
typedef uint8_t CayenneLPP::DigitalGPIOVal_t;
```






### typedef Float32Val\_t 

```C++
typedef float CayenneLPP::Float32Val_t;
```






### typedef LuminosityVal\_t 

```C++
typedef uint16_t CayenneLPP::LuminosityVal_t;
```






### typedef PresenceVal\_t 

```C++
typedef uint8_t CayenneLPP::PresenceVal_t;
```






### typedef RawBitVal\_t 


```C++
typedef uint8_t CayenneLPP::RawBitVal_t;
```



Represents a single bit value, often used in bit manipulation or status indication. 


        



### typedef RawByteVal\_t 


```C++
typedef uint8_t CayenneLPP::RawByteVal_t;
```



Represents a raw byte value, typically used for byte-oriented data operations. 


        



### typedef RelativeHumidity\_t 

```C++
typedef uint16_t CayenneLPP::RelativeHumidity_t;
```






### typedef TemperatureVal\_t 

```C++
typedef uint16_t CayenneLPP::TemperatureVal_t;
```






### typedef Word16Val\_t 

```C++
typedef uint16_t CayenneLPP::Word16Val_t;
```






### typedef Word32Val\_t 

```C++
typedef uint32_t CayenneLPP::Word32Val_t;
```



## Public Static Functions Documentation




### function ResetMeasurement 

_Clears currently used Measurement struct with invalid data._ 
```C++
static inline Measurement_t CayenneLPP::ResetMeasurement () 
```





**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with invalid data 





        



### function SetAcceleration 

_Sets the acceleration values for the x, y, and z axes._ 
```C++
static inline Measurement_t CayenneLPP::SetAcceleration (
    const float x,
    const float y,
    const float z
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with scaled acceleration values and sets the measurement type to MEASUREMENT\_TYPE\_ACCELERATION. The acceleration values are scaled by a factor of 1000 to convert them from floats to uint16\_t, providing milli-g precision in their digital representation. It is used for capturing or simulating acceleration in various axes, typically in motion or orientation detection applications.




**Parameters:**


* `x` The acceleration value along the x-axis. 
* `y` The acceleration value along the y-axis. 
* `z` The acceleration value along the z-axis. These values are scaled by 1000 for precise milli-g representation. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled acceleration values and the type set to MEASUREMENT\_TYPE\_ACCELERATION. 





        



### function SetAnalogInput 

_Sets the analog input value._ 
```C++
static inline Measurement_t CayenneLPP::SetAnalogInput (
    const float analog_input_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a scaled analog input value and sets the measurement type to MEASUREMENT\_TYPE\_ANALOG\_INPUT. The analog input value is scaled by a factor of 100 to convert it from a float to a uint16\_t for digital representation. It is used for capturing or simulating analog sensor readings.




**Parameters:**


* `analog_input_val` The analog input value to set, as a floating-point number. This value is scaled by 100 to facilitate digital representation without losing precision. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled analog input value and the type set to MEASUREMENT\_TYPE\_ANALOG\_INPUT. 





        



### function SetAnalogOutput 

_Sets the analog output value._ 
```C++
static inline Measurement_t CayenneLPP::SetAnalogOutput (
    const float analog_output_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a scaled analog output value and sets the measurement type to MEASUREMENT\_TYPE\_ANALOG\_OUTPUT. The analog output value is scaled by a factor of 100 to convert it from a float to a uint16\_t for digital representation. It is designed for controlling analog output devices or interfaces.




**Parameters:**


* `analog_output_val` The analog output value to set, as a floating-point number. This value is scaled by 100 to facilitate digital representation without losing precision. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled analog output value and the type set to MEASUREMENT\_TYPE\_ANALOG\_OUTPUT. 





        



### function SetBarometricPressure 

_Sets the barometric pressure value._ 
```C++
static inline Measurement_t CayenneLPP::SetBarometricPressure (
    const float barometric_pressure_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a scaled barometric pressure value and sets the measurement type to MEASUREMENT\_TYPE\_BAROMETRIC\_PRESSURE. The pressure value is scaled by a factor of 10 to convert it from a float to a uint16\_t, providing a precision of 0.1 hPa (hectopascals) in its digital representation. It is used for atmospheric pressure monitoring in weather stations or environmental monitoring systems.




**Parameters:**


* `barometric_pressure_val` The barometric pressure value to set, as a floating-point number. This value is scaled by 10 to provide a precision of 0.1 hPa. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled barometric pressure value and the type set to MEASUREMENT\_TYPE\_BAROMETRIC\_PRESSURE. 





        



### function SetDigitalInput 

_Sets the digital input value._ 
```C++
static inline Measurement_t CayenneLPP::SetDigitalInput (
    const uint8_t digital_input_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with the given digital input value and sets the measurement type to MEASUREMENT\_TYPE\_DIGITAL\_INPUT. It is primarily used for capturing or simulating the state of digital input pins in hardware abstraction layers.




**Parameters:**


* `digital_input_val` The digital input value to set. This value is typically used to represent the state of a digital input, such as reading a pin as high (1) or low (0). 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the digital input value and the type set to MEASUREMENT\_TYPE\_DIGITAL\_INPUT. 





        



### function SetDigitalOutput 

_Sets the digital output value._ 
```C++
static inline Measurement_t CayenneLPP::SetDigitalOutput (
    const uint8_t digital_output_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with the given digital output value and sets the measurement type to MEASUREMENT\_TYPE\_DIGITAL\_OUTPUT. It is designed to be used for configuring or controlling digital output pins in hardware abstraction layers.




**Parameters:**


* `digital_output_val` The digital output value to set. This value is typically used to control a digital output, such as setting a pin high (1) or low (0). 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the digital output value and the type set to MEASUREMENT\_TYPE\_DIGITAL\_OUTPUT. 





        



### function SetFloat32 

_Sets a 32-bit floating-point value in a measurement._ 
```C++
static inline Measurement_t CayenneLPP::SetFloat32 (
    const float float32_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a 32-bit floating-point value and sets the measurement type to MEASUREMENT\_TYPE\_RAWFLOAT32. It is particularly used for handling floating-point data in scenarios where precise numerical values are essential, such as in scientific measurements or complex data processing tasks.




**Parameters:**


* `float32_val` The 32-bit floating-point value to set. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the 32-bit floating-point value and the type set to MEASUREMENT\_TYPE\_RAWFLOAT32. 





        



### function SetGPS 

_Sets the GPS coordinates and altitude._ 
```C++
static inline Measurement_t CayenneLPP::SetGPS (
    const float latitude,
    const float longitude,
    const float altitude
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with scaled GPS coordinate and altitude values and sets the measurement type to MEASUREMENT\_TYPE\_GPS. The latitude and longitude values are scaled by a factor of 10000, and the altitude by 100, converting them from floats to uint32\_t for precise geographic positioning. It is used for tracking and navigation applications.




**Parameters:**


* `latitude` The latitude value in degrees. 
* `longitude` The longitude value in degrees. 
* `altitude` The altitude value in meters. The latitude and longitude are scaled by 10000, and altitude by 100, for precise representation. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled GPS values and the type set to MEASUREMENT\_TYPE\_GPS. 





        



### function SetGyro 

_Sets the gyroscopic values for the x, y, and z axes._ 
```C++
static inline Measurement_t CayenneLPP::SetGyro (
    const float x,
    const float y,
    const float z
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with scaled gyroscopic values and sets the measurement type to MEASUREMENT\_TYPE\_GYRO. The gyro values are scaled by a factor of 100 to convert them from floats to uint16\_t, aiming to maintain precision for angular velocity measurements. It is typically used in orientation and rotation detection systems.




**Parameters:**


* `x` The gyro value along the x-axis. 
* `y` The gyro value along the y-axis. 
* `z` The gyro value along the z-axis. These values are scaled by 100 for digital representation. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled gyro values and the type set to MEASUREMENT\_TYPE\_GYRO. 





        



### function SetLuminosity 

_Sets the luminosity value._ 
```C++
static inline Measurement_t CayenneLPP::SetLuminosity (
    const float luminosity_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with the given luminosity value and sets the measurement type to MEASUREMENT\_TYPE\_LUMINOSITY. It is primarily used for monitoring or simulating light intensity levels in various applications, ranging from environmental sensing to smart lighting control.




**Parameters:**


* `luminosity_val` The luminosity value to set. This value typically represents the intensity of light measured, using a specific unit such as lux. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the luminosity value and the type set to MEASUREMENT\_TYPE\_LUMINOSITY. 





        



### function SetPresence 

_Sets the presence value._ 
```C++
static inline Measurement_t CayenneLPP::SetPresence (
    const uint8_t presence_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with the given presence value and sets the measurement type to MEASUREMENT\_TYPE\_PRESENCE. It is designed to be used for representing the presence or absence of an object or entity, typically detected through sensors.




**Parameters:**


* `presence_val` The presence value to set. This value is typically used to indicate the detection of presence (1) or absence (0) of an entity. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the presence value and the type set to MEASUREMENT\_TYPE\_PRESENCE. 





        



### function SetRawBit 

_Sets a raw bit value in a measurement._ 
```C++
static inline void CayenneLPP::SetRawBit (
    const uint8_t raw_bit_val,
    Measurement_t * prevMeasurement
) 
```



This function updates the provided measurement with a new bit value, setting or appending it based on the previous measurement's type. It is used to incrementally build up a raw bit measurement from individual bits.




**Parameters:**


* `raw_bit_val` The raw bit value to set or append. Only the least significant bit is used. 
* `prevMeasurement` Reference to the previous measurement which will be updated with the new bit value. 



**Returns:**

void 





        



### function SetRawByte 

_Sets a raw byte value in a measurement._ 
```C++
static inline Measurement_t CayenneLPP::SetRawByte (
    const uint8_t raw_byte_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a raw byte value and sets the measurement type to MEASUREMENT\_TYPE\_RAWBYTE. It is used for handling raw byte data in various data communication or storage scenarios.




**Parameters:**


* `raw_byte_val` The raw byte value to set. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the raw byte value and the type set to MEASUREMENT\_TYPE\_RAWBYTE. 





        



### function SetRelativeHumidity 

_Sets the relative humidity value._ 
```C++
static inline Measurement_t CayenneLPP::SetRelativeHumidity (
    const float humidity_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a scaled relative humidity value and sets the measurement type to MEASUREMENT\_TYPE\_RELATIVE\_HUMIDITY. The humidity value is scaled by a factor of 2 to convert it from a float to a uint16\_t, aiming to maintain precision while accommodating the data type. It is used for humidity monitoring in environmental control systems.




**Parameters:**


* `humidity_val` The relative humidity value to set, as a floating-point number. This value is scaled by 2 to adjust for the digital representation. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled relative humidity value and the type set to MEASUREMENT\_TYPE\_RELATIVE\_HUMIDITY. 





        



### function SetTemperature 

_Sets the temperature value._ 
```C++
static inline Measurement_t CayenneLPP::SetTemperature (
    const float temperature_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a scaled temperature value and sets the measurement type to MEASUREMENT\_TYPE\_TEMPERATURE. The temperature value is scaled by a factor of 10 to convert it from a float to a uint16\_t, allowing for a fraction of a degree precision in digital representation. It is used for temperature monitoring applications.




**Parameters:**


* `temperature_val` The temperature value to set, as a floating-point number. This value is scaled by 10 to provide a precision of 0.1 degrees in its digital form. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the scaled temperature value and the type set to MEASUREMENT\_TYPE\_TEMPERATURE. 





        



### function SetWord16 

_Sets a 16-bit word value in a measurement._ 
```C++
static inline Measurement_t CayenneLPP::SetWord16 (
    const uint16_t word16_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a 16-bit word value and sets the measurement type to MEASUREMENT\_TYPE\_RAWWORD16. It is used for handling 16-bit data in various scenarios, such as digital communication or sensor data encoding.




**Parameters:**


* `word16_val` The 16-bit word value to set. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the 16-bit word value and the type set to MEASUREMENT\_TYPE\_RAWWORD16. 





        



### function SetWord32 

_Sets a 32-bit word value in a measurement._ 
```C++
static inline Measurement_t CayenneLPP::SetWord32 (
    const uint32_t word32_val
) 
```



This function initializes a [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure with a 32-bit word value and sets the measurement type to MEASUREMENT\_TYPE\_RAWWORD32. It is used for handling 32-bit data in various applications, including data communication and sensor data processing.




**Parameters:**


* `word32_val` The 32-bit word value to set. 



**Returns:**

[**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) A [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) structure initialized with the 32-bit word value and the type set to MEASUREMENT\_TYPE\_RAWWORD32. 





        

------------------------------
The documentation for this class was generated from the following file `src/CayenneLPP.hpp`

