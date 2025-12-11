# OpenCode Agent System

A comprehensive framework for managing specialized AI agents that handle coding,
documentation, testing, and workflow coordination across any codebase and
programming language.

**Note:** This project incorporates files from
[https://github.com/darrenhinde/OpenAgents](https://github.com/darrenhinde/OpenAgents)
with modifications to suit my workflow.

## Thanks

Thanks to [darrenhinde/OpenAgents](https://github.com/darrenhinde/OpenAgents) for the original work.

## Features

- **Universal Agent (OpenAgent)**: Handles questions, tasks, and workflow
  coordination across any domain
- **Development Agent (OpenCoder)**: Specialized for modular and functional code
  implementation with strict quality gates
- **Specialized Subagents**: Code review, testing, documentation, build
  validation, and task management
- **Context-Aware Execution**: Loads project-specific standards and patterns
  before any implementation
- **Security-First Design**: Restricted permissions and approval gates for
  sensitive operations
- **Multi-Language Support**: Works with TypeScript, Python, Go, Rust, and other
  languages

## Installation

This is a configuration-based system. Clone the repository and set up your
environment:

```bash
git clone <repository-url>
cd opencode
```

## Quick Start

### Using OpenAgent (Universal Tasks)

OpenAgent handles general questions and coordination:

```bash
# Ask questions about codebases
"What does this function do?"

# Execute tasks with approval gates
"Create a new feature branch"
"Run tests and build"
```

### Using OpenCoder (Development Tasks)

OpenCoder specializes in code implementation:

```bash
# Implement features with context loading
"Add user authentication"
"Refactor this component"
"Fix the bug in line 42"
```

## Project Structure

```
.opencode/
├── agent/           # AI agents for specific tasks
│   ├── subagents/   # Specialized subagents
│   │   ├── code/    # Code-related agents
│   │   ├── core/    # Core functionality agents
│   │   └── utils/   # Utility agents
│   └── *.md         # Primary agents (openagent.md, opencoder.md)
├── command/         # Slash commands for operations
├── context/         # Knowledge base and standards
│   ├── core/
│   │   ├── standards/  # Code, docs, tests standards
│   │   ├── system/     # System guides
│   │   └── workflows/  # Review, delegation workflows
│   └── project/        # Project-specific context
└── plugin/          # Extensions and integrations
```

## Usage

```bash
grep -rl "/home/flagmate/.config/opencode/" . | xargs sed -i 's#/home/flagmate/.config/opencode/#{CURRENT_DIR}#g'
```
### Agent Commands

- `/analyze` - Analyze codebase patterns and structure
- `/implement` - Implement features with OpenCoder
- `/review` - Code review with specialized agents
- `/test` - Generate and run tests
- `/docs` - Generate documentation
- `/optimize` - Performance optimization
- `/validate-repo` - Repository validation

### Context Loading

Agents automatically load relevant context files before execution:

- **Code tasks**: Loads coding standards and patterns
- **Documentation**: Loads documentation standards
- **Testing**: Loads testing frameworks and patterns
- **Reviews**: Loads review workflows and checklists

## Core Agents

### OpenAgent

- **Purpose**: Universal agent for any domain
- **Capabilities**: Questions, tasks, workflow coordination
- **Tools**: read, write, edit, grep, bash, task delegation

### OpenCoder

- **Purpose**: Development specialist with quality gates
- **Capabilities**: Code implementation, refactoring, debugging
- **Focus**: Modular, functional, type-safe implementations

## Contributing

1. Follow the established patterns in `context/core/standards/`
2. Load appropriate context files before implementation
3. Request approval for any changes
4. Update documentation when adding new agents or commands

## License

[Specify license type]
