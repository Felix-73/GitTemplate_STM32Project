Commit Convention
=================

Purpose
-------
This document defines the mandatory commit message format for all STM32 embedded projects.

Clear commit history is required for:
- Debugging
- Traceability
- Firmware certification
- Long-term maintenance

Commit Message Format
--------------------
Format:
    <type>(scope): short description

Rules:
- Use present tense
- Use imperative form
- Maximum 72 characters for the subject
- One logical change per commit
- Each commit MUST compile

Allowed Types
-------------
feat      : New feature
fix       : Bug fix
refactor  : Code change without functional impact
perf      : Performance or memory optimization
driver    : Peripheral drivers
hal       : HAL / LL / Cube updates
board     : Clock, pinout, linker, startup
build     : Build system changes
test      : Tests or validation tools
docs      : Documentation
chore     : Maintenance, formatting

Scopes (examples)
-----------------
uart, spi, i2c, adc, dma, rtos, power, clock, boot

Examples (Valid)
----------------
feat(uart): add DMA-based RX for USART2
fix(i2c): recover bus after NACK condition
perf(adc): reduce sampling latency
board(clock): switch PLL source to HSE
hal: update STM32CubeH7 to v1.11.0

Examples (Invalid)
------------------
fix
wip
test commit
update code

Forbidden Practices
------------------
- Mixing unrelated changes
- Committing broken builds
- Temporary or debug commits
