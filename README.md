# Flight Computer PCB (V1)

Custom PCB built around an STM32F446 microcontroller, designed as a foundational flight computer for future quadcopter flight-controller development. This project is part of a portfolio targeting embedded systems and aerospace/defense engineering roles.

## Status

Designed in Altium Designer — schematic and layout complete, board sent to fabrication, physical board received. Assembly and bring-up testing not yet started.

## V1 Scope

- **IMU:** ICM-42688-P (accelerometer + gyroscope) — SPI1
- **Barometer:** BMP581 (pressure / altitude) — I2C1
- **Magnetometer:** LIS2MDLTR (heading) — I2C1
- **Data logging:** microSD via SPI2 (Hirose DM3AT-SF-PEJM5 push-push socket)
- **Comms/power:** USB-C (USB4105-15-A-120), with USB D+/D- routed directly to the STM32's USB OTG FS peripheral

**Explicitly out of scope for V1:** GPS, battery monitoring, buzzer, status LED, motor control, ESC outputs, radio telemetry, autopilot/flight-stabilization logic.

## Hardware

| | |
|---|---|
| MCU | STM32F446RET6 (Cortex-M4 @ 180 MHz, FPU, LQFP64) |
| Power | LD39100PU33R LDO, fixed 3.3V / 1A |
| Bench power | USB-C 5V → LDO → 3.3V rail |
| Field power | Aircraft LiPo (2S–6S) → external 5V BEC → board |
| Clock | Abracon ABM3B 12.000 MHz HSE crystal, 18pF load, 20ppm |
| Board size | 49 × 51 mm |

## Roadmap

Planned to scale into a full flight controller capable of driving an ESC and controlling a quadcopter — GPS, battery monitoring, and motor control are targeted for a future revision.

## Tools

Designed in Altium Designer.

---

*Under active development.*
