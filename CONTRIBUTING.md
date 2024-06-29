# Contributing to FinMan

Thank you for considering contributing to FinMan! We welcome contributions from the community to make this project better. Please take a moment to review this document to understand how to contribute to this project.

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Getting Started](#getting-started)
3. [How to Contribute](#how-to-contribute)
   - [Reporting Bugs](#reporting-bugs)
   - [Suggesting Features](#suggesting-features)
   - [Contributing Code](#contributing-code)
   - [Writing Documentation](#writing-documentation)
4. [Development Guidelines](#development-guidelines)
   - [Branching Model](#branching-model)
   - [Commit Messages](#commit-messages)
   - [Code Style](#code-style)
5. [License](#license)

## Code of Conduct

This project and everyone participating in it is governed by the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [email@example.com](mailto:email@example.com).

## Getting Started

1. Fork the repository on GitHub.
2. Clone your forked repository to your local machine:

   ```bash
   git clone https://github.com/your-username/finman.git
   ```

3. Create a new branch for your work:

   ```bash
   git checkout -b feature/your-feature-name
   ```

## How to Contribute

### Reporting Bugs

If you find a bug in the project, please report it by creating a new issue on the [GitHub Issues](https://github.com/your-username/finman/issues) page. Include as much detail as possible to help us understand and reproduce the issue.

### Suggesting Features

We welcome feature suggestions! To propose a new feature, please open an issue on the [GitHub Issues](https://github.com/your-username/finman/issues) page and describe the feature in detail.

### Contributing Code

1. Ensure you have followed the [Getting Started](#getting-started) steps.
2. Ensure your code follows the [Code Style](#code-style) guidelines.
3. Add or update tests as appropriate.
4. Ensure all tests pass.
5. Submit a pull request to the `develop` branch with a clear description of your changes.

### Writing Documentation

Documentation improvements are welcome! If you want to contribute to the documentation:

1. Follow the [Getting Started](#getting-started) steps.
2. Update the relevant Markdown files in the `docs` directory.
3. Submit a pull request to the `develop` branch with a clear description of your changes.

## Development Guidelines

### Branching Model

We follow the [Gitflow](https://nvie.com/posts/a-successful-git-branching-model/) branching model:

- `main`: Contains production-ready code.
- `develop`: Contains the latest development changes.
- `feature/*`: Branches for new features.
- `bugfix/*`: Branches for bug fixes.
- `hotfix/*`: Branches for hotfixes.

### Commit Messages

Use clear and descriptive commit messages. Follow these guidelines:

- Use the present tense ("Add feature" not "Added feature").
- Use the imperative mood ("Move button left..." not "Moves button left...").
- Limit the first line to 72 characters or less.
- Reference issues and pull requests liberally.

### Code Style

- Follow the Go [Effective Go](https://golang.org/doc/effective_go.html) guidelines.
- Use `gofmt` to format your code.
- Ensure your code passes `golint` and `go vet` checks.

## License

By contributing to FinMan, you agree that your contributions will be licensed under the [MIT License](LICENSE).

---

Feel free to modify the email address and repository URLs to fit your project's details.