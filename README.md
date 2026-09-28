# repo-first-game-digitization

A lightweight skill for digitizing analog games from official rules while keeping repository-local rule and design canons as the working sources of truth.

## Purpose

The skill separates three responsibilities:

- official sources provide the source material;
- the rule canon provides a readable and complete description of the adopted game rules;
- the design canon records how those rules become digital behavior.

It also keeps source links traceable, records digitization-scope exclusions, routes unresolved conflicts and gaps to the user, and turns binding examples into implementation tests.

## Contents

- `SKILL.md` — skill definition

## Installation

Place the `repo-first-game-digitization` directory in the skill location used by your agent or skill loader.

The skill leaves document granularity, file organization, and test framework choices to the project.
