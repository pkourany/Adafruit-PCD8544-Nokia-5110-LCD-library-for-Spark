Adafruit-PCD8544-Nokia-5110-LCD-library-for-Spark
=================================================

Nokia 5110 LCD library adapted for Spark Core by Paul Kourany, April 2014

This code compiles on the Spark web IDE

TO use hardware SPI, connect the display as follows for the demo program to run:

Spark       Nokia 5110
A5 (MOSI)     DIN
A4 (MISO)      -
A3 (SCK)      CLK
A2 (SS)       CS
D3            RST
D2            D/C
GND           GND
3V3           VCC

D3(RST) and D2(D/C) may be any pin but changes must be made to object creation line:
  Adafruit_PCD8544 display = Adafruit_PCD8544(SS, D2, D3);

NOTES:
- Modified code for Spark Core compatibility
- Added hardware and (fast) software SPI to fastSPIwrite()
- Added new create object methods for HardwareSPI:

  Adafruit_PCD8544 display = Adafruit_PCD8544(CS, DC, RST);
    - Specify hardware SPI, chip select(CS pin), DC (data/command pin) and RST (reset pin)

  Adafruit_PCD8544 display = Adafruit_PCD8544(DC, RST);
    - Specify hardware SPI, NO chip select, DC (data/command pin) and RST (reset pin)

- Existing create methods will use (fast) software SPI code
- The existing slowSPIwrite() function which uses shiftOut() is not used anywhere in the library

