

# File CayenneLPP.hpp

[**File List**](files.md) **>** [**src**](dir_68267d1309a1af8e8297ef4c3efbcdba.md) **>** [**CayenneLPP.hpp**](CayenneLPP_8hpp.md)

[Go to the documentation of this file](CayenneLPP_8hpp.md)

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
#ifndef _CAYENNE_LPP_H_
#define _CAYENNE_LPP_H_
#include <stddef.h>
#include <stdint.h>
#include <string.h>
#include "CayenneTypes.hpp"
namespace CayenneLPP
{

    template <size_t static_size>
    class CayenneLPP
    {
    public:
        CayenneLPP()
        {
            /* Set the max size of the encoder buffer */
            maxsize = static_size;
            /* Zero the buffer*/
            memset(buffer, 0x00, static_size);
            /* Set the buffer cursor to zero */
            reset();
        }

        ~CayenneLPP()
        {
        }

        void reset(void)
        {
            cursor = 0;
        }

        constexpr uint8_t getSize(void)
        {
            return cursor;
        }

        constexpr uint8_t *getBuffer(void)
        {
            return buffer;
        }

        const uint8_t setMeasurement(const uint8_t channel, const Measurement_t* measurement)
        {
            const size_t measurement_size = DetermineMeasurementSize(measurement->type);
            size_t new_cursor_pos = (cursor + measurement_size + 2);
            if (new_cursor_pos > maxsize)
            {
                return 0;
            }
            buffer[cursor++] = channel;
            buffer[cursor++] = measurement->type;
            memcpy((buffer + cursor), measurement->val.RawBytes, measurement_size);
            cursor = new_cursor_pos;
            return cursor;
        }

    private:
        const uint8_t DetermineMeasurementSize(const CayenneMeasurementType_t type)
        {
            switch (type)
            {
            case MEASUREMENT_TYPE_DIGITAL_OUTPUT:
            case MEASUREMENT_TYPE_DIGITAL_INPUT:
            case MEASUREMENT_TYPE_PRESENCE:
            case MEASUREMENT_TYPE_RAWBYTE:
            case MEASUREMENT_TYPE_RAWBIT_1:
            case MEASUREMENT_TYPE_RAWBIT_2:
            case MEASUREMENT_TYPE_RAWBIT_3:
            case MEASUREMENT_TYPE_RAWBIT_4:
            case MEASUREMENT_TYPE_RAWBIT_5:
            case MEASUREMENT_TYPE_RAWBIT_6:
            case MEASUREMENT_TYPE_RAWBIT_7:
            case MEASUREMENT_TYPE_RAWBIT_8:
            {
                return sizeof(DigitalGPIOVal_t);
            }
            case MEASUREMENT_TYPE_RAWWORD16:
            case MEASUREMENT_TYPE_LUMINOSITY:
            case MEASUREMENT_TYPE_ANALOG_OUTPUT:
            case MEASUREMENT_TYPE_ANALOG_INPUT:
            case MEASUREMENT_TYPE_TEMPERATURE:
            case MEASUREMENT_TYPE_RELATIVE_HUMIDITY:
            case MEASUREMENT_TYPE_BAROMETRIC_PRESSURE:
            {
                return sizeof(AnalogGPIOVal_t);
            }
            case MEASUREMENT_TYPE_RAWWORD32:
            case MEASUREMENT_TYPE_RAWFLOAT32:
            {
                return sizeof(Float32Val_t);
            }

            case MEASUREMENT_TYPE_GYRO:
            case MEASUREMENT_TYPE_ACCELERATION:
            {
                return sizeof(AcceleroVal_t);
            }

            case MEASUREMENT_TYPE_GPS:
            {
                return sizeof(GPSCoord_t);
            }
            default:
            {
                return sizeof(uint8_t);
            }
            }
        }
        uint8_t buffer[static_size];

        uint8_t maxsize;

        uint8_t cursor;
    };
    
}
#endif

```

