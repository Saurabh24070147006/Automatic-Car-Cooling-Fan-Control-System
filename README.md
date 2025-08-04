# 🚗 Automatic Car Engine Cooling Fan Control System

This project implements a real-time automatic engine cooling system using an **STM32 microcontroller** and an **LM35 temperature sensor**. The system activates or deactivates a cooling fan based on the measured engine temperature.

---

## 📦 Project Summary

- **Platform:** STM32F4 Series (e.g., STM32F401RE)
- **IDE:** STM32CubeIDE
- **Language:** Embedded C
- **Peripherals Used:**
  - ADC (for LM35 temperature sensor)
  - GPIO (for fan control)
  - UART (for serial communication)
- **Sensor:** LM35 (Analog Temperature Sensor)
- **Output Device:** GPIO controlled fan (or LED)
- **Optional:** LCD Display (16x2) via custom LCD library

---

## 📈 System Architecture

```text
   +-----------+       +--------------+       +-----------------+
   |  LM35     | ----> |   STM32 ADC  | ----> |   Decision Logic|
   +-----------+       +--------------+       +-----------------+
                                                |       |
                                          +-----+       +------+
                                          |                    |
                                      GPIO High           GPIO Low
                                        (Fan ON)           (Fan OFF)

