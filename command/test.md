---
description: Run the complete testing pipeline
---

# Testing Pipeline

This command executes the full testing workflow for the project, regardless of
the technology stack. It automates type checking, linting, test execution, user
prompts, and reporting.

## Usage

The exact commands depend on the ecosystem you're working in. Examples:

- **JavaScript/TypeScript**: `pnpm`, `npm`, `yarn`, `bun`
- **Python**: `pytest`, `ruff`, `mypy`
- **Go**: `go test`, `golangci-lint`
- **Rust**: `cargo test`, `cargo clippy`, `cargo check`
- **Java**: `mvn test`, `gradle test`
- **PHP**: `phpunit`, `phpstan`, `pint`
- **Others**: use the appropriate type checker, linter, and test runner.

Typical workflow steps:

1. Run the type checker
2. Run the linter
3. Run the test suite
4. Report any failures
5. Ask the user if they want to fix the errors on their own
6. If they choose to fix, pause the pipeline
7. Re-run the pipeline until all checks pass
8. Report success

## What This Command Does

1. **Type Check**\
   Executes the project’s type-checking command.

2. **Lint**\
   Runs static analysis and code-style validation.

3. **Run Tests**\
   Executes the test suite for the project.

4. **Report Failures**\
   Shows errors from type checking, linting, and tests.

5. **Prompt the User**\
   Asks:\
   _"Do you want to fix these errors before continuing?"_
   - **Yes** → pipeline pauses
   - **No** → pipeline exits or gives guidance

6. **Loop Until Clean**\
   Continues running until all checks pass.

7. **Success Message**\
   Reports successful completion of the full pipeline.

