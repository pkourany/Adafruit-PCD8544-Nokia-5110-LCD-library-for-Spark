Adafruit-PCD8544-Nokia-5110-LCD-library-for-Spark
=================================================

Nokia 5110 LCD library adapted for Spark Core by Paul Kourany, April 2014

- Added hardware and (fast) software SPI to fastSPIwrite()
- Added new create object methods for HardwareSPI:

  Adafruit_PCD8544 display = Adafruit_PCD8544(CS, DC, RST);
    - Specify hardware SPI, chip select(CS pin), DC (data/command pin) and RST (reset pin)

  Adafruit_PCD8544 display = Adafruit_PCD8544(DC, RST);
    - Specify hardware SPI, NO chip select, DC (data/command pin) and RST (reset pin)

- Existing create methods will use (fast) software SPI code
