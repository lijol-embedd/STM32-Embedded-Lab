# STM32 GPIO and Peripheral Initialization

## Overview

This project demonstrates basic embedded firmware development using the STM32F103RB microcontroller and the STM32 Hardware Abstraction Layer (HAL).

The firmware configures the system clock, initializes GPIO and USART2 peripherals, and implements periodic LED toggling using HAL GPIO functions.

## Hardware and Software

- **Microcontroller:** STM32F103RB
- **Development Environment:** STM32CubeIDE
- **Configuration Tool:** STM32CubeMX
- **Programming Language:** Embedded C
- **Firmware Library:** STM32 HAL
- **System Clock:** 64 MHz

## Implemented Features

- System clock configuration using the internal High-Speed Internal (HSI) oscillator and PLL.
- GPIO output configuration using push-pull mode.
- Periodic LED toggling using `HAL_GPIO_TogglePin()`.
- Timing control using `HAL_Delay()`.
- Push-button GPIO configuration with external interrupt capability.
- USART2 initialization at 115200 baud, 8 data bits, no parity and 1 stop bit.

## Working Principle

After initializing the HAL library, the firmware configures the system clock and initializes the required peripherals.

The main application executes an infinite loop that toggles the LED state and introduces a 500 ms delay between successive transitions.

This produces a continuous blinking pattern with a 1-second complete ON/OFF cycle.

## Repository Structure

```text
STM32-Embedded-Lab/
├── Core/
│   ├── Inc/
│   ├── Src/
│   └── Startup/
├── Drivers/
│   ├── CMSIS/
│   └── STM32F1xx_HAL_Driver/
├── .project
├── .cproject
├── .mxproject
├── LedBlink.ioc
├── STM32F103RBTX_FLASH.ld
└── README.md
```

## Future Improvements

- UART-based serial communication and debugging.
- Interrupt-driven push-button control.
- Timer-based LED control without blocking delays.
- PWM generation and peripheral interfacing.

## Learning Outcomes

This project provides practical experience with STM32CubeIDE, STM32 HAL, GPIO configuration, clock initialization, interrupt configuration and basic embedded C programming.
