# Contribution Guidelines

First off, thanks for taking the time to contribute! ❤️ We appreciate your efforts to improve this project and make it better for everyone.

## Table of Contents

- [How to Contribute](#how-to-contribute)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)
- [Commit Guidelines](#commit-guidelines)
- [Testing](#testing)
- [Development Environment](#development-environment)
- [Submitting Changes](#submitting-changes)
- [Code of Conduct](#code-of-conduct)

---

## How to Contribute

We encourage all kinds of contributions, from bug reports to feature requests and code improvements. Please follow the guidelines below to ensure a smooth process.

## Reporting Bugs

Before reporting a bug, please check the existing issues on [GitHub Issues](https://github.com/escalate/hugo-split-theme/issues?q=label%3Abug) to avoid duplicates. If your issue is not listed, you can report it via [GitHub Issues](https://github.com/escalate/hugo-split-theme/issues/new). A good bug report should include:

- Clear steps to reproduce the issue
- Expected vs. actual behavior
- Relevant logs or error messages
- Your environment details (OS, version, dependencies, etc.)

## Suggesting Enhancements

Before suggesting an enhancement, please check the existing issues on [GitHub Issues](https://github.com/escalate/hugo-split-theme/issues?q=label%3Aenhancement) to avoid duplicates. If your suggestion is not listed, enhancement suggestions should also be submitted through [GitHub Issues](https://github.com/escalate/hugo-split-theme/issues/new) and should include:

- A clear and descriptive title
- A detailed explanation of the suggested enhancement
- Any potential alternatives or references to similar implementations

## Commit Guidelines

All commit messages must follow the [Conventional Commits](https://www.conventionalcommits.org/) format. These messages are used to automatically generate release versions and release notes.

Format:

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

Example:

```
feat(auth): add OAuth2 support
```

Allowed types: `feat`, `fix`, `build`, `chore`, `ci`, `docs`, `style`, `refactor`, `perf`, `test`

## Testing

All tests must pass before submitting any changes. The test suite runs via [GitHub Actions](https://github.com/escalate/hugo-split-theme/actions), and contributions will not be merged unless all tests are successful.

- Test suite is located in the [.github/workflows/test.yml](.github/workflows/test.yml) file.
- Add suitable tests for any new functionality or changes.
- Run tests locally before pushing changes.

## Development Environment

To set up your local development environment:

1. Clone the repository.
2. Check the [README.md](README.md) for setup details.

## Submitting Changes

1. Fork the repository and create a new branch.
2. Stick to the commit guidelines.
3. Ensure all tests pass.
4. Submit a pull request (PR) with a clear description.
5. Your PR will be reviewed, and you may be asked to make adjustments before merging.

## Code of Conduct

Please follow our [Code of Conduct](CODE_OF_CONDUCT.md) to maintain a welcoming and respectful community.

Thank you for your contributions! 🚀
