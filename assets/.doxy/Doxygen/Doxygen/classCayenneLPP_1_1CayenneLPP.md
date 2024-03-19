

# Class CayenneLPP::CayenneLPP

**template &lt;size\_t static\_size&gt;**



[**ClassList**](annotated.md) **>** [**CayenneLPP**](namespaceCayenneLPP.md) **>** [**CayenneLPP**](classCayenneLPP_1_1CayenneLPP.md)










































## Public Functions

| Type | Name |
| ---: | :--- |
|   | [**CayenneLPP**](#function-cayennelpp) () <br> |
|  constexpr uint8\_t \* | [**getBuffer**](#function-getbuffer) (void) <br>_This gets a pointer to the statically allocated internal buffer._  |
|  constexpr uint8\_t | [**getSize**](#function-getsize) (void) <br>_This gets the amount of bytes currently stored in the buffer._  |
|  void | [**reset**](#function-reset) (void) <br>_Reset the cursor back to zero._  |
|  const uint8\_t | [**setMeasurement**](#function-setmeasurement) (const uint8\_t channel, const [**Measurement\_t**](structCayenneLPP_1_1Measurement__t.md) \* measurement) <br>_Store a new measurement in the encoder buffer._  |
|   | [**~CayenneLPP**](#function-cayennelpp) () <br>_Since this class is initialized statically, there is nothing to clean up._  |




























## Public Functions Documentation




### function CayenneLPP 

```C++
inline CayenneLPP::CayenneLPP::CayenneLPP () 
```






### function getBuffer 

_This gets a pointer to the statically allocated internal buffer._ 
```C++
inline constexpr uint8_t * CayenneLPP::CayenneLPP::getBuffer (
    void
) 
```





**Returns:**

Pointer to the buffer 





        



### function getSize 

_This gets the amount of bytes currently stored in the buffer._ 
```C++
inline constexpr uint8_t CayenneLPP::CayenneLPP::getSize (
    void
) 
```





**Returns:**

The amount of bytes stored 





        



### function reset 

```C++
inline void CayenneLPP::CayenneLPP::reset (
    void
) 
```






### function setMeasurement 

_Store a new measurement in the encoder buffer._ 
```C++
inline const uint8_t CayenneLPP::CayenneLPP::setMeasurement (
    const uint8_t channel,
    const Measurement_t * measurement
) 
```





**Returns:**

The cursor position in the internal buffer 





        



### function ~CayenneLPP 

```C++
inline CayenneLPP::CayenneLPP::~CayenneLPP () 
```




------------------------------
The documentation for this class was generated from the following file `src/CayenneLPP.hpp`

