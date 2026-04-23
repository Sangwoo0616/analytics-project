# AGENTS.md

## Purpose

This project is maintained with a strong bias toward long-term maintainability.
Every change should improve or preserve clarity, testability, and ease of future modification.

## Core Rule

For any feature addition, always write or update tests first.
Only then implement the feature so the new tests pass.

Required workflow for feature work:

1. Understand the requested behavior and define expected outcomes.
2. Add or update automated tests that describe that behavior first.
3. Run the tests and confirm the new test fails for the expected reason.
4. Implement the minimum code required to make the tests pass.
5. Run the relevant test suite again and confirm it passes.
6. Refactor only if tests remain green and readability improves.

## Maintainability Standards

- Prefer small, focused modules and functions with clear responsibilities.
- Avoid duplicated logic. Extract shared behavior when it meaningfully improves clarity.
- Use descriptive names for files, functions, variables, and tests.
- Keep side effects localized and explicit.
- Favor simple designs over clever or tightly coupled implementations.
- Add concise comments only when intent is not obvious from the code itself.
- Preserve backward compatibility unless the task explicitly allows breaking changes.

## Testing Expectations

- New features must include automated tests.
- Bug fixes should include a regression test whenever practical.
- Tests should describe observable behavior, not implementation details.
- Keep tests readable and deterministic.
- Prefer fast unit tests by default. Add integration tests when behavior crosses boundaries.
- Do not merge feature work with failing tests.

## Change Discipline

- Make the smallest safe change that satisfies the requirement.
- Separate refactors from feature behavior when possible.
- Do not silently rewrite unrelated code.
- If existing structure makes safe changes difficult, improve the design in small steps backed by tests.

## Definition of Done

A task is only complete when all of the following are true:

- Tests for the requested behavior were written first for feature work.
- The implementation satisfies the requirement.
- Relevant automated tests pass.
- The changed code is understandable and maintainable by another engineer.
