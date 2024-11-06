# Arduino Nano Example

This sketch was written for a Nano.

This sketch implements:
* two servos, each with three positions
   Positions can be set to angles 0-180
   
* The i/o channels, each of which can be an input or an output,
   If an output it may be solid, pulse or flashing. 

It demonstrates: 
* CDI
* memstruct of EEPROM reflecting the CDI structure
* setting flags to refect whether eveentids are used as consumers, producers, or both, see: **const EIDTab eidtab[NUM_EVENT] PROGMEM**
* Initialization routine to initialize the EEPROM, see: **userInitAll()**
* Eventid processing to set a servo's position, see: **pceCallback(unsigned int index)**
* Sampling of inputs and producing events.

This is my test version for demonstration use only by John Holmes
  - Pin 3 is used for interrupt
  - Pin 10 CS SS (Slave Select) (used to select the slave device, also known as CS or Chip Select)
  - Pin 11 SI MOSI (Master Out Slave In)
  - Pin 12 SO MISO (Master In Slave Out)
  - Pin 13 SCK (Serial Clock)

  - Pins 4,5,6,7,A0,A1,A2,A3 are used for input or output
  - Pins A4 & A5 are the servo pins