Coding Rules
============

General
-------
- Language: C / C++
- MISRA-inspired practices
- No dynamic memory unless approved

STM32 Specific
--------------
- Prefer LL for performance-critical paths
- HAL allowed for configuration and init
- ISRs must be minimal

Formatting
----------
- 4 spaces indentation
- No tabs
- Clear and explicit naming

Forbidden
---------
- Blocking delays in interrupts
- Magic numbers
- Dead code
