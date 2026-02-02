# STM32 Embedded Project


## Overview

This repository contains the firmware for an STM32-based embedded system
developed using STM32Cube tools and libraries.

The project follows strict versioning, commit, and release rules to ensure:
- Traceability
- Reproducible builds
- Long-term maintainability

## Target Hardware

- MCU: STM32xxxx
- Board: Custom / Nucleo / Discovery
- Clock source: HSE / HSI (see board configuration)

## Toolchain

- STM32CubeMX
- STM32CubeIDE or ARM GCC
- OpenOCD / ST-Link
- Make or CMake

## Repository Structure

- Core/           Application core (main, interrupts)
- Drivers/        STM32 HAL / LL drivers
- Middlewares/    RTOS, stacks, external libraries
- Board/          Board-specific configuration
- Application/    Application-level code


## Versioning
Releases are tagged using semantic versioning:
    vMAJOR.MINOR.PATCH

Each tag corresponds to a flashable and reproducible firmware.

## Documentation

The following documents define the project rules and processes:
- COMMIT_CONVENTION.md
- CONTRIBUTING.md


## STM32Cube Policy

- The .ioc file is versioned
- Code regeneration must preserve user code sections
- Any CubeMX regeneration must be documented in the commit message

## Licensing

Internal company project – redistribution not allowed.
