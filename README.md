# stm32f429_place_isr_code_in_ram

Description of how to place code and isr in sram with STM32CubeIDE.

Be careful to place Reset_Handelr of .text in Flash
  .text.Reset_Handler :
  {
    . = ALIGN(4);
    *(.text.Reset_Handler)
    . = ALIGN(4);
  } >FLASH

This source code is an example in which all of these source codes operate in SRAM and the LED toggles every update interrupt of Timer 1.
