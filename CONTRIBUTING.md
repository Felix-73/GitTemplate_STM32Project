# Contributing Rules


## General Rules

- This project uses STM32Cube-generated code
- All contributors must follow the defined workflow
- Code reviews are mandatory

## Commit Rules

- Commits MUST follow COMMIT_CONVENTION.md
- One commit = one logical change
- Each commit must:
  - Compile
  - Link
  - Boot when applicable

## Workflow

1. Create a branch from 'develop'
2. Implement the change
3. Rebase on latest 'develop'
4. Open a merge request
5. Address review comments
6. Merge after approval

## Forbidden Actions

- Force push on 'main'
- Commit generated binaries
- Modify CubeMX files without justification

## CubeMX Policy

- The .ioc file is versioned
- Code regeneration must not overwrite user code
- Any CubeMX regeneration must be mentioned in commit message
