# GitHub Actions Repository

This repository contains a collection of reusable GitHub Actions designed to automate various tasks. These actions can be integrated into your workflows to streamline processes related to Python, Node.js, and version control.

## Available Actions

### 1. **Detect Direct Push to Main**
- **Description**: This action detects direct pushes to the `main` branch and checks whether the push is a pull request merge or a direct commit. It ensures that only pull request merges are allowed to `main`, preventing direct pushes.

### 2. **Validate Version and Changelog Updates**
- **Description**: This action ensures that the `VERSION` and `CHANGELOG.md` files are updated in pull requests. It checks if these files are modified when a pull request is opened or synchronized, enforcing best practices for versioning and changelog management.

### 3. **Python Actions**
These actions help with automating Python-related tasks such as linting, testing and dependency installation.

- **Linting**: Runs `flake8` on Python code to enforce coding standards.
- **Run Tests**: Executes unit tests using `pytest`.
- **Install Dependencies**: Installs project dependencies from the `requirements.txt` file.

### 4. **Node.js Actions**
These actions help automate tasks related to Node.js projects, including dependency installation, testing, and building the app.

- **Install Dependencies**: Installs project dependencies using `npm ci` for faster, deterministic installations in CI environments.
- **Run Tests**: Executes tests using `npm test`.
- **Build App**: Builds the app by installing dependencies and running the build command.

## Usage

To use any of these actions in your own workflows, reference them in your `.github/workflows` directory.

For example, to use the **Detect Direct Push to Main** action in your workflow:

```yaml
name: Detect Direct Push to Main

on:
  push:
    branches:
      - main

jobs:
  detect-direct-push:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Detect Direct Push
        uses: your-org/your-repo/actions/version-control/detect-direct-push@main