Release Process
===============

Purpose
-------
Defines the official firmware release procedure.

Versioning
----------
Semantic Versioning:
    vMAJOR.MINOR.PATCH
- MAJOR: breaking change
- MINOR: new feature
- PATCH: bug fix

Release Steps
-------------
1. Create release branch:
       git checkout -b release/vX.Y.Z
2. Update version identifiers
3. Run full build
4. Run validation tests
5. Generate binaries:
       - ELF
       - BIN / HEX
       - MAP
6. Merge into 'main'
7. Create Git tag:
       git tag -a vX.Y.Z -m "Release vX.Y.Z"

Release Checklist
-----------------
- Firmware builds without warnings
- Memory usage checked
- Startup tested
- Power modes tested
- Regression tests passed

Artifacts
---------
Release artifacts must be archived:
- Firmware binaries
- Map file
- Release notes
