# Contributing to bfra-me/renovate-config

Welcome! This repository contains [Renovate](https://renovatebot.com/) configuration presets used by [bfra.me](https://bfra.me) projects. Contributions are welcome and appreciated.

## Table of Contents

- [Getting Started](#getting-started)
- [Contributing Workflow](#contributing-workflow)
- [Code Standards](#code-standards)
- [Release Process](#release-process)

## Getting Started

### Prerequisites

- **Node.js**: Version specified in `.node-version` file
- **Git**: For version control and conventional commits

### Repository Structure

- **`default.json5`**: Primary Renovate preset with common configuration
- **`automerge.json5`**: Preset for enabling automerge
- **`group/`**: Presets for grouping dependency updates
- **`maintenance/`**: Presets for maintenance-related updates
- **`vendors/`**: Vendor-specific Renovate presets
- **`.github/workflows/`**: CI/CD workflows

## Contributing Workflow

### 1. Issue Creation

Before starting work:

- Check existing issues and discussions
- Create an issue describing the proposed changes
- For significant changes, discuss the approach in the issue

### 2. Branch Strategy

```bash
# Create a feature branch from main
git checkout main
git pull origin main
git checkout -b feat/your-feature-name

# Or for fixes
git checkout -b fix/issue-description
```

### 3. Development Process

1. **Make changes** to the relevant preset files
2. **Format files** using Prettier: `npx prettier --write .`
3. **Commit using conventional commits**:
   ```bash
   git commit -m "feat: add new preset for grouping monorepo updates"
   git commit -m "fix: correct automerge configuration"
   git commit -m "docs: update README usage example"
   ```

### 4. Pull Request Process

1. **Push your branch** and create a pull request
2. **Ensure all checks pass** (Prettier formatting, CI)
3. **Address review feedback** promptly

## Code Standards

### Preset File Format

All preset files use [JSON5](https://json5.org/) format (`.json5`) with 2-space indentation. Files are formatted with [Prettier](https://prettier.io/).

```json5
{
  $schema: 'https://docs.renovatebot.com/renovate-schema.json',
  extends: ['config:recommended'],
  // Your preset configuration
}
```

### Formatting

Run Prettier before committing:

```bash
npx prettier --write .
```

The CI workflow checks formatting with Prettier. PRs with formatting issues will fail the lint check.

### Commit Message Convention

This repository uses [Conventional Commits](https://www.conventionalcommits.org/) for automated semantic versioning:

- `feat:` — New preset or significant new functionality
- `fix:` — Bug fix in an existing preset
- `docs:` — Documentation updates
- `chore:` — Maintenance tasks, dependency updates
- `ci:` — CI/CD workflow changes

## Release Process

Releases are automated using [semantic-release](https://semantic-release.gitbook.io/) based on conventional commit messages:

- `fix:` commits → patch release (e.g., `5.1.1`)
- `feat:` commits → minor release (e.g., `5.2.0`)
- `BREAKING CHANGE:` footer → major release (e.g., `6.0.0`)

Releases are triggered automatically on merge to `main`.

## Getting Help

- **GitHub Issues**: For bugs, feature requests, and questions
- **Renovate Documentation**: https://docs.renovatebot.com/
- **Renovate Config Presets**: https://docs.renovatebot.com/config-presets/

## License

By contributing to this repository, you agree that your contributions will be licensed under the [MIT License](LICENSE.md).
