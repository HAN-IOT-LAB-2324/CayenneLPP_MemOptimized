

# File CayenneTypes.hpp

[**File List**](files.md) **>** [**src**](dir_68267d1309a1af8e8297ef4c3efbcdba.md) **>** [**CayenneTypes.hpp**](CayenneTypes_8hpp.md)

[Go to the documentation of this file](CayenneTypes_8hpp.md)

```C++

/*
 *  Copyright 2024 (C) CayenneLPP library
 *
 *  Licensed under the GPL License, Version 3.0 (the "License");
 *  you may not use this file except in compliance with the License.
 *  You may obtain a copy of the License at
 *
 *  https://fsf.org/
 *
 *  Unless required by applicable law or agreed to in writing, software
 *  distributed under the License is distributed on an "AS IS" BASIS,
 *  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 *  See the License for the specific language governing permissions and
 *  limitations under the License.
 *
 * Authors: Adrian Sanchez del C. <asanchezdelc>
 *          Jarno           <JarnoW999>
 *          Majid           <majidsabbagh>
 *          Victor Hogeweij <Hoog-V>
 */
#ifndef CayenneTypes_HPP
#define CayenneTypes_HPP
namespace CayenneLPP
{
#define CAYENNE_MAX_UNION_SIZE (sizeof(GPSCoord_t))

#define UINT24_MAX ((((2 ^ 24) - 1)))
#define TEMP_MAX_RANGE (UINT16_MAX / 10)
#define LUM_MAX_RANGE (UINT16_MAX / 100)
#define PRESENCE_MIN_RANGE (0)
#define DIG_GPIO_MIN_RANGE (0)
#define RH_MAX_RANGE (UINT16_MAX / 2)
#define ANALOG_VOLT_MAX_RANGE (UINT16_MAX / 100)
#define BAROMETRIC_PRESS_MAX_RANGE (UINT16_MAX / 10)
#define MAX_GPS_LAT_RANGE (UINT24_MAX / 10000)
#define MAX_GPS_LONG_RANGE (UINT24_MAX / 10000)
#define MAX_GPS_ALT_RANGE (UINT24_MAX / 100)
    typedef uint8_t RawByteVal_t;

    typedef uint8_t RawBitVal_t;

    // Represents a 16-bit word, commonly used for medium-range integer values.
    typedef uint16_t Word16Val_t;

    /***
     * Represents a 32-bit word, used for larger integer values or raw data.
     */
    typedef uint32_t Word32Val_t;

    /***
     * Represents a 32-bit floating-point number, used for precise numerical values.
     */
    typedef float Float32Val_t;

    /***
     * Represents a digital GPIO (General Purpose Input/Output) value, for digital pin states.
     */
    typedef uint8_t DigitalGPIOVal_t;

    /***
     * Represents a presence detection value, typically indicating detection (1) or absence (0).
     */
    typedef uint8_t PresenceVal_t;

    /***
     * Represents a luminosity value, used for light intensity measurements.
     */
    typedef uint16_t LuminosityVal_t;

    /***
     * Represents an analog GPIO value, for analog pin readings.
     */
    typedef uint16_t AnalogGPIOVal_t;

    /***
     * Represents a temperature measurement, typically in a scaled format for precision.
     */
    typedef uint16_t TemperatureVal_t;

    /***
     * Represents relative humidity as a percentage, in a scaled format for precision.
     */
    typedef uint16_t RelativeHumidity_t;

    /***
     * Represents barometric pressure, typically in a scaled format to represent hPa values.
     */
    typedef uint16_t BarometricPressure_t;

#pragma pack(push, 1)
    typedef struct
    {
        uint16_t x;
        uint16_t y;
        uint16_t z;
    } GyroVal_t;
#pragma pack(pop)

    /***
     * Represents 3-axis acceleration values, for motion or orientation detection.
     */
#pragma pack(push, 1)
    typedef struct
    {
        uint16_t x;
        uint16_t y;
        uint16_t z;
    } AcceleroVal_t;
#pragma pack(pop)

    /***
     * Represents GPS coordinates (latitude, longitude) and altitude, with compact bit field packing.
     */
#pragma pack(push, 1)
    typedef struct
    {
        uint32_t latitude : 24;  /* Latitude, scaled to store fractional degrees */
        uint32_t longitude : 24; /* Longitude, scaled to store fractional degrees */
        uint32_t altitude : 24;  /* Altitude, scaled to store values with precision */
    } GPSCoord_t;
#pragma pack(pop)

    /***
     * Represents a union of all possible measurement values, allowing for diverse data types.
     */
    typedef union
    {
        RawBitVal_t RawBit;
        RawByteVal_t RawByte;
        DigitalGPIOVal_t DigitalGPIO;
        PresenceVal_t Presence;
        Word16Val_t Word16;
        LuminosityVal_t Luminosity;
        AnalogGPIOVal_t AnalogGPIO;
        TemperatureVal_t Temperature;
        RelativeHumidity_t RelativeHumidity;
        BarometricPressure_t BarometricPressure;
        Word32Val_t Word32;
        Float32Val_t Float32;
        GPSCoord_t GPS;
        AcceleroVal_t Acceleration;
        GyroVal_t Gyro;
        uint8_t RawBytes[CAYENNE_MAX_UNION_SIZE];
    } MeasurementData_t;

    // Defines the measurement types, corresponding to specific data representations.
    typedef enum
    {
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
        MEASUREMENT_TYPE_GPS = 136,
    } CayenneMeasurementType_t;

    // Represents a general-purpose measurement structure, including type and value.
    typedef struct
    {
        CayenneMeasurementType_t type;
        MeasurementData_t val;
    } Measurement_t;

    static inline Measurement_t ResetMeasurement()
    {
        MeasurementData_t Data = {.RawByte = 0};
        return {MEASUREMENT_TYPE_INVALID, Data};
    }

    static inline Measurement_t SetDigitalOutput(const uint8_t digital_output_val)
    {
        MeasurementData_t Data = {.DigitalGPIO = (digital_output_val > DIG_GPIO_MIN_RANGE)};
        return {MEASUREMENT_TYPE_DIGITAL_OUTPUT, Data};
    }

    static inline Measurement_t SetDigitalInput(const uint8_t digital_input_val)
    {
        MeasurementData_t Data = {.DigitalGPIO = (digital_input_val > DIG_GPIO_MIN_RANGE)};
        return {MEASUREMENT_TYPE_DIGITAL_INPUT, Data};
    }

    static inline Measurement_t SetPresence(const uint8_t presence_val)
    {
        MeasurementData_t Data = {.Presence = (presence_val > PRESENCE_MIN_RANGE)};
        return {MEASUREMENT_TYPE_PRESENCE, Data};
    }

    static inline Measurement_t SetLuminosity(const float luminosity_val)
    {
        const float val = (luminosity_val <= LUM_MAX_RANGE) ? luminosity_val : LUM_MAX_RANGE;
        MeasurementData_t Data = {.Luminosity = uint16_t(val * 100)};
        return {MEASUREMENT_TYPE_LUMINOSITY, Data};
    }

    static inline Measurement_t SetAnalogOutput(const float analog_output_val)
    {
        const float val = (analog_output_val <= ANALOG_VOLT_MAX_RANGE) ? analog_output_val : ANALOG_VOLT_MAX_RANGE;
        MeasurementData_t Data = {.AnalogGPIO = uint16_t((val * 100))};
        return {MEASUREMENT_TYPE_ANALOG_OUTPUT, Data};
    }

    static inline Measurement_t SetAnalogInput(const float analog_input_val)
    {
        const float val = (analog_input_val <= ANALOG_VOLT_MAX_RANGE) ? analog_input_val : ANALOG_VOLT_MAX_RANGE;
        MeasurementData_t Data = {.AnalogGPIO = uint16_t((val * 100))};
        return {MEASUREMENT_TYPE_ANALOG_INPUT, Data};
    }

    static inline Measurement_t SetTemperature(const float temperature_val)
    {
        const float val = (temperature_val <= TEMP_MAX_RANGE) ? temperature_val : TEMP_MAX_RANGE;
        MeasurementData_t Data = {.Temperature = uint16_t(val * 10)};
        return {MEASUREMENT_TYPE_TEMPERATURE, Data};
    }

    static inline Measurement_t SetRelativeHumidity(const float humidity_val)
    {
        const float val = (humidity_val <= RH_MAX_RANGE) ? humidity_val : RH_MAX_RANGE;
        MeasurementData_t Data = {.RelativeHumidity = uint16_t(val * 2)};
        return {MEASUREMENT_TYPE_RELATIVE_HUMIDITY, Data};
    }

    static inline Measurement_t SetBarometricPressure(const float barometric_pressure_val)
    {
        const float val = (barometric_pressure_val <= BAROMETRIC_PRESS_MAX_RANGE) ? barometric_pressure_val : BAROMETRIC_PRESS_MAX_RANGE;
        MeasurementData_t Data = {.BarometricPressure = uint16_t(val * 10)};
        return {MEASUREMENT_TYPE_BAROMETRIC_PRESSURE, Data};
    }

    static inline Measurement_t SetAcceleration(const float x, const float y, const float z)
    {
        const AcceleroVal_t accelero_val = {.x = uint16_t(x * 1000), .y = uint16_t(y * 1000), .z = uint16_t(z * 1000)};
        const MeasurementData_t Data = {.Acceleration = accelero_val};
        return {MEASUREMENT_TYPE_ACCELERATION, Data};
    }

    static inline Measurement_t SetGyro(const float x, const float y, const float z)
    {
        const GyroVal_t gyro_val = {.x = uint16_t(x * 100), .y = uint16_t(y * 100), .z = uint16_t(z * 100)};
        const MeasurementData_t Data = {.Gyro = gyro_val};
        return {MEASUREMENT_TYPE_GYRO, Data};
    }

    static inline Measurement_t SetGPS(const float latitude, const float longitude, const float altitude)
    {
        const float lat_val = latitude <= MAX_GPS_LAT_RANGE ? latitude : MAX_GPS_LAT_RANGE;
        const float long_val = longitude <= MAX_GPS_LONG_RANGE ? longitude : MAX_GPS_LONG_RANGE;
        const float alt_val = altitude <= MAX_GPS_ALT_RANGE ? altitude : MAX_GPS_ALT_RANGE;
        const GPSCoord_t gps_val = {.latitude = uint32_t(alt_val * 10000), .longitude = uint32_t(long_val * 10000), .altitude = uint32_t(alt_val * 100)};
        const MeasurementData_t Data = {.GPS = gps_val};
        return {MEASUREMENT_TYPE_GPS, Data};
    }

    static inline void SetRawBit(const uint8_t raw_bit_val, Measurement_t *prevMeasurement)
    {
        const uint8_t prevMeasurementWasBit = (prevMeasurement->type >= MEASUREMENT_TYPE_RAWBIT_1 && prevMeasurement->type < MEASUREMENT_TYPE_RAWBIT_8);
        uint8_t bitpos = prevMeasurementWasBit ? ((prevMeasurement->type - MEASUREMENT_TYPE_RAWBIT_1) + 1) : 0;
        if (prevMeasurementWasBit)
        {
            prevMeasurement->val.RawBit |= (raw_bit_val << bitpos);
            bitpos++;
            prevMeasurement->type = static_cast<CayenneMeasurementType_t>((MEASUREMENT_TYPE_RAWBIT_1 + bitpos) - 1);
        }
        else
        {
            prevMeasurement->val.RawBit = (raw_bit_val << bitpos);
            prevMeasurement->type = MEASUREMENT_TYPE_RAWBIT_1;
        }
    }

    static inline Measurement_t SetRawByte(const uint8_t raw_byte_val)
    {
        const RawByteVal_t raw_byte = raw_byte_val;
        const MeasurementData_t Data = {.RawByte = raw_byte};
        return {MEASUREMENT_TYPE_RAWBYTE, Data};
    }

    static inline Measurement_t SetWord16(const uint16_t word16_val)
    {
        const Word16Val_t word16 = word16_val;
        const MeasurementData_t Data = {.Word16 = word16};
        return {MEASUREMENT_TYPE_RAWWORD16, Data};
    }

    static inline Measurement_t SetWord32(const uint32_t word32_val)
    {
        const Word32Val_t word32 = word32_val;
        const MeasurementData_t Data = {.Word32 = word32};
        return {MEASUREMENT_TYPE_RAWWORD32, Data};
    }

    static inline Measurement_t SetFloat32(const float float32_val)
    {
        const Float32Val_t float32 = float32_val;
        const MeasurementData_t Data = {.Float32 = float32};
        return {MEASUREMENT_TYPE_RAWFLOAT32, Data};
    }
}
#endif

```

