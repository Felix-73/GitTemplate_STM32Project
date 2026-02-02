# Commit Convention + Tag


## Purpose

This document defines the mandatory commit message format for all STM32 embedded projects.

Clear commit history is required for:
- Debugging
- Traceability
- Firmware certification
- Long-term maintenance

## Commit Message Format

### <span style="color:green">Type</span>(<span style="color:yellow">scope</span>): <span style="color:orange">short description</span>

Rules:
- Use present tense
- Use imperative form
- Maximum 72 characters for the subject
- One logical change per commit
- Each commit MUST compile



| <span style="color:green">Type</span>    | Description |
|----------|-------------|
| feat     | A new feature or functionality |
| fix      | A bug fix |
| refactor | Code changes that neither fix a bug nor add a feature |
| perf     | Performance improvements |
| docs     | Documentation changes |
| chore    | Routine tasks, maintenance, formatting, CI/CD updates |
| test     | Adding or updating tests |
| build    | Changes related to the build system or project configuration |




### Examples of valid commit

| <span style="color:green">Type</span>     | <span style="color:yellow">scope</span>    |  <span style="color:orange">short description</span>                          |
|----------|---------|---------------------------------------------------|
| feat     | uart    | Add UART driver support for STM32F4               |
| feat     | spi     | Implement SPI master mode                          |
| feat     | adc     | Add ADC continuous conversion                      |
| fix      | uart    | Correct framing error on reception                |
| fix      | spi     | Fix SPI data corruption issue                      |
| fix      | rtos    | Fix task scheduling priority bug                   |
| refactor | uart    | Simplify driver initialization                     |
| refactor | adc     | Clean up ADC read/write routines                   |
| refactor | rtos    | Restructure task management code                   |
| perf     | uart    | Optimize UART transmission speed                   |
| perf     | spi     | Improve SPI read throughput                         |
| perf     | rtos    | Reduce RTOS context switch overhead                 |
| docs     | uart    | Update UART driver usage documentation             |
| docs     | rtos    | Update FreeRTOS task creation examples             |
| docs     | power   | Document low-power modes                             |
| chore    | project   | Update STM32CubeMX project settings                   |
| chore    | build     | Update linker script for memory layout                |
| chore    | ci        | Update build scripts for CI/CD                         |
| test     | uart      | Add unit tests for UART driver                         |
| test     | adc       | Add automated ADC conversion tests                     |
| test     | rtos      | Add RTOS task scheduler tests                          |
| build    | stm32f4   | Update CMake build flags for STM32F4                  |
| build    | stm32f7   | Add target for STM32F7 board                           |
| build    | build     | Fix compilation warnings for GCC ARM                   |


### Command example

``` git commit -m "feat(uart): add UART driver support for STM32F4"```

# TAG
In this project, we use **Git tags** to track firmware versions. Tags mark a **specific commit** that corresponds to a released firmware build. This allows you to easily reference, checkout, or build a particular version.

Tags should follow semantic versioning: vMAJOR.MINOR.PATCH (e.g., v1.2.0).

Keep README.md and changelog separate from versioning. Don’t update the version in the README for every release.

### Command example

``` git tag -a v1.2.0 -m "Release firmware version 1.2.0"```


# Forbidden Actions

- Write the version in the commit
- Write a date in the commit
- Using vague or meaningless commit messages
- Reusing or moving existing version tags.
- Deleting or altering commits that are already pushed to a remote shared branch
