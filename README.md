# SimpleEVSE-WiFi-adding-plug-temperature-sensor protection against burning marode mains jack at high currents (until 16A)  
This lowers the charging current (pulswide) mains plug temperature dependet by use of the A0 A/D pin of D1 Mini.
Hardware is easy, glue a NTC temperature sensor  SEMI833ET (sold from Reichelt Elektronik) inside mains plug.
Change the mains cable by one with additional 2 wires for the temperature sensor. 
Wire the sensor cables between GND and A0 analog A/D input of D1 Mini
Wire a 20 KOhms resistor between A0 and 3,3V reference voltage pin of D1 Mini 
Wire a low pas filter capacitor 1µF between GND and A0 
So a temperature dependet voltage between 1,1V @ approx. 80°C and 2V @approx. 50°C mains plug temperature can be read at A0 A/D pin.
My problem: I`m not able to programm the current limiting routines. The current limmiting have to be start @60°C growing limit until 5A @ 80°C
and more than 80°C down to Zero. Who can do this?
By adding this feature charging will be shure also at high adjustet currents at foreign marode mains jacks !  
