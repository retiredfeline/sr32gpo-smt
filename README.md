# Shift register 32 general purpose output board

![sr32gpo-front.jpg](sr32gpo-front.jpg)

These are the Kicad design files for the Shift register 32 bit general purpose output board described in my [Hackaday project page](https://hackaday.io/project/184239-3-line-to-32-line-output-expander).

## Versioning

SMT version February 2025

This version has been tested after assembly by PCBWay, who I thank for sponsoring a batch. You can find an uploaded project zip in the pcbway directory.

## Notes

The minimum lines required to use this board are: GND, SER (data), SRCLK (shift), RCLK (strobe). Vcc depends on the power arrangement. You should jumper the ~OESEL (output enable select) to ground if you don't wish to disable the display by signal, or vary the output with PWM, from a controller. The ~SRCLR input is only needed for resetting the output by the controller.

This board is designed with optional aspects you can choose to include or not:

- As mentioned some lines don't need to be driven in smaller configurations.

- Between 1 and 4 74HC595s can be installed for 8-32 outputs, in steps of 8. Naturally only the resistors for the used outputs need to be installed.

- The 74HC595 can source or sink 6 mA current.

- The 74HC595 can operate between 2V and 6V. This can be chosen to suit the controller, e.g. 3.3V or 5V, and the power supply section if installed.

- The power supply section is optional. You can choose to power this from the controller. Or you could power the controller with this.

- Copper pads for data and output are duplicated so you can attach more connectors or even solder wires. The input power is also brought out to duplicate pads for piggybacking to other circuits, e.g. an auxiliary board.

- Although the connectors are rendered as vertical pin headers, you can use other kinds of connectors like pin sockets, or even solder wires to the pads.

- You may wish to change the resistor to suit your application if you are getting the PCB assembled by editing the BoM. Currently it's set to 4.7k.

## Authors

* **Ken Yap**

## License

See the [LICENSE](LICENSE.md) file for license rights and limitations (MIT).
