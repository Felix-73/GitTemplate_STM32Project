# Contributing Rules


## General Rules

- This project uses STM32Cube-generated code
- All contributors must follow the defined workflow

## Commit Rules

- Commits MUST follow COMMIT_CONVENTION.md
- One commit = one logical change
- Each commit must:
  - Compile
  - Link
  - Boot when applicable

## Workflow

1. Create a branch 'develop'
2. Implement the change
3. Open a merge request
4. Address review comments
5. Merge after approval on the master branch

## Forbidden Actions

- Force push on 'main'
- Commit generated binaries
- Modify CubeMX files without justification

## CubeMX Policy

- The .ioc file is versioned
- Code regeneration must not overwrite user code
- Any CubeMX regeneration must be mentioned in commit message
