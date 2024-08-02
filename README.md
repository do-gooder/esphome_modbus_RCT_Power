# esphome_modbus_RCT_Power

This is a project for reading values from RCT Power inverters via MODBUS with RS485 based on an ESP32 with ESPHOME.


## Prepare the inverter

To be able to use the RS485 interface, you must log in as an ***installer*** via the Android app "[RCT Power App](https://play.google.com/store/apps/details?id=org.rctpower.heiphossil)" (not iOS!).

Then set the "RS485 Betriebsmodus" to "Modbus Master" under Gerät --> Einstellungen -> Schnittstelle --> RS485. The "RS485 Adresse" must be greater than 0 (e.g. 1). Do not forget to press "FLASH"!


## Wiring

Look in the manual for your inverter and search for RS485. The X102 connection on the communication board should be the correct one. It is also labelled RS485.

**ATTENTION, HIGH VOLTAGE --> Check what is required to ensure that the modules are disconnected from the inverter and that the battery and fuse are switched off if necessary. The inverter must not be energised!**

[Wiring guide](https://github.com/evcc-io/evcc/discussions/9292#discussioncomment-6702960)



## ToDo

- According to the documentation, it is also possible to write values. This still needs to be worked out
- Create documentation
- Implement "Bitmask value. Event fields."
- Create python script to enable modbus
- Wiring picture
- Find out if the modbus_controller's update_interval can be reduced


## External Links

[RS485 Communication with external devices v.1.2](https://downloads.vodnici.net/uploads/wpforo/attachments/536/6706-RCTPowerRS485Communication.pdf)
