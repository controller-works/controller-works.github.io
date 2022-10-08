---
permalink: /cornedc/
---
# Corne DC
Low profile Corne (CRKBD) variant with sandwich PCB design and support for Kailh chocolate v1 and v2 switches and MX spacing. Features PCB art back plate.
The Corne DC is electrically identical to the Corne keyboard, except the layout has been completely redone.
When building firmware you must uncomment
```mk
/* #define EE_HANDS  */
```
for proper functioning. This is because the board does not use a pull-up resister to set the main versus secondary side of the keyboard.