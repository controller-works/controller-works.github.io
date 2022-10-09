---
permalink: /corneob/
---
# Corne OB
Low profile Corne (CRKBD) variant with aluminum case and support for Kailh chocolate v1 switches and chocolate spacing. Features PCB art back plate. It has a highly integrated design with over voltage and over current protection on the USB and TRRS connectors. It also integrates the controller and OLED support circuitry on the main board (no modules).
The Corne OB's schematic is identical to the Corne keyboard, except the layout has been completely redone.
When building firmware you must uncomment
```mk
/* #define EE_HANDS  */
```
in your config.h for proper functioning. This is because the board does not use a pull-up resister to set the main versus secondary side of the keyboard.