

# File CayenneTypes.hpp



[**FileList**](files.md) **>** [**src**](dir_68267d1309a1af8e8297ef4c3efbcdba.md) **>** [**CayenneTypes.hpp**](CayenneTypes_8hpp.md)

[Go to the source code of this file](CayenneTypes_8hpp_source.md)
















## Namespaces

| Type | Name |
| ---: | :--- |
| namespace | [**CayenneLPP**](namespaceCayenneLPP.md) <br> |


## Classes

| Type | Name |
| ---: | :--- |
| struct | [**AcceleroVal\_t**](structCayenneLPP_1_1AcceleroVal__t.md) <br> |
| struct | [**GPSCoord\_t**](structCayenneLPP_1_1GPSCoord__t.md) <br> |
| struct | [**GyroVal\_t**](structCayenneLPP_1_1GyroVal__t.md) <br> |
| struct | [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) <br> |


## Public Types

| Type | Name |
| ---: | :--- |
| union  | [**MeasurementData\_t**](#union-measurementdata_t)  <br> |















































## Macros

| Type | Name |
| ---: | :--- |
| define  | [**ANALOG\_VOLT\_MAX\_RANGE**](CayenneTypes_8hpp.md#define-analog_volt_max_range)  (UINT16\_MAX / 100)<br> |
| define  | [**BAROMETRIC\_PRESS\_MAX\_RANGE**](CayenneTypes_8hpp.md#define-barometric_press_max_range)  (UINT16\_MAX / 10)<br> |
| define  | [**CAYENNE\_MAX\_UNION\_SIZE**](CayenneTypes_8hpp.md#define-cayenne_max_union_size)  (sizeof(GPSCoord\_t))<br>_The max size of the union._  |
| define  | [**DIG\_GPIO\_MIN\_RANGE**](CayenneTypes_8hpp.md#define-dig_gpio_min_range)  (0)<br> |
| define  | [**LUM\_MAX\_RANGE**](CayenneTypes_8hpp.md#define-lum_max_range)  (UINT16\_MAX / 100)<br> |
| define  | [**MAX\_GPS\_ALT\_RANGE**](CayenneTypes_8hpp.md#define-max_gps_alt_range)  (UINT24\_MAX / 100)<br> |
| define  | [**MAX\_GPS\_LAT\_RANGE**](CayenneTypes_8hpp.md#define-max_gps_lat_range)  (UINT24\_MAX / 10000)<br> |
| define  | [**MAX\_GPS\_LONG\_RANGE**](CayenneTypes_8hpp.md#define-max_gps_long_range)  (UINT24\_MAX / 10000)<br> |
| define  | [**PRESENCE\_MIN\_RANGE**](CayenneTypes_8hpp.md#define-presence_min_range)  (0)<br> |
| define  | [**RH\_MAX\_RANGE**](CayenneTypes_8hpp.md#define-rh_max_range)  (UINT16\_MAX / 2)<br> |
| define  | [**TEMP\_MAX\_RANGE**](CayenneTypes_8hpp.md#define-temp_max_range)  (UINT16\_MAX / 10)<br> |
| define  | [**UINT24\_MAX**](CayenneTypes_8hpp.md#define-uint24_max)  ((((2 ^ 24) - 1)))<br>_The ranges for the checking inside the helper functions!_  |

## Public Types Documentation




### union MeasurementData\_t 

```C++

```



## Macro Definition Documentation





### define ANALOG\_VOLT\_MAX\_RANGE 

```C++
#define ANALOG_VOLT_MAX_RANGE (UINT16_MAX / 100)
```






### define BAROMETRIC\_PRESS\_MAX\_RANGE 

```C++
#define BAROMETRIC_PRESS_MAX_RANGE (UINT16_MAX / 10)
```






### define CAYENNE\_MAX\_UNION\_SIZE 

```C++
#define CAYENNE_MAX_UNION_SIZE (sizeof(GPSCoord_t))
```






### define DIG\_GPIO\_MIN\_RANGE 

```C++
#define DIG_GPIO_MIN_RANGE (0)
```






### define LUM\_MAX\_RANGE 

```C++
#define LUM_MAX_RANGE (UINT16_MAX / 100)
```






### define MAX\_GPS\_ALT\_RANGE 

```C++
#define MAX_GPS_ALT_RANGE (UINT24_MAX / 100)
```






### define MAX\_GPS\_LAT\_RANGE 

```C++
#define MAX_GPS_LAT_RANGE (UINT24_MAX / 10000)
```






### define MAX\_GPS\_LONG\_RANGE 

```C++
#define MAX_GPS_LONG_RANGE (UINT24_MAX / 10000)
```






### define PRESENCE\_MIN\_RANGE 

```C++
#define PRESENCE_MIN_RANGE (0)
```






### define RH\_MAX\_RANGE 

```C++
#define RH_MAX_RANGE (UINT16_MAX / 2)
```






### define TEMP\_MAX\_RANGE 

```C++
#define TEMP_MAX_RANGE (UINT16_MAX / 10)
```






### define UINT24\_MAX 

```C++
#define UINT24_MAX ((((2 ^ 24) - 1)))
```




------------------------------
The documentation for this class was generated from the following file `src/CayenneTypes.hpp`

