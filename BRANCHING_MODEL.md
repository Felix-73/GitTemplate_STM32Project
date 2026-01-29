Branching Model
===============

Branch Overview
---------------
Branch         Purpose
------         -------
main           Stable, production-ready firmware
develop        Integration branch
feature/*      New developments
fix/*          Bug fixes
release/*      Release preparation

Rules
-----
- Direct commits on 'main' are forbidden
- All changes must go through 'develop'
- 'main' is always flashable
- Each release is tagged

Branch Naming
-------------
Feature: feature/<short-description>
Fix    : fix/<issue-id>-<short-description>
Release: release/vX.Y.Z

Merge Strategy
--------------
- feature/* -> develop: rebase
- develop -> main: merge commit
- No fast-forward merges on main

Deleting Branches
-----------------
Feature and fix branches must be deleted after merge.
