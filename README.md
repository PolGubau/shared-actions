# Reusable GitHub Actions Repository

Welcome to the **Shared GitHub Actions** repository! This project is designed to store and maintain reusable GitHub Actions, making it easier to standardize and streamline workflows across multiple repositories.

---

## Table of Contents

1. Overview
2. Repository Structure
3. Getting Started
4. Usage
5. Contributing
6. License

---

## Overview

This repository serves as a central hub for custom GitHub Actions that can be shared and reused across different projects. Each action is defined with:

- A clear purpose.
- Well-documented inputs and outputs.
- Versioning for backward compatibility.

By using shared actions, teams can:

- Reduce redundancy in workflow definitions.
- Centralize updates and maintenance.
- Promote consistency and best practices across projects.

---

## Repository Structure

```
📦shared-actions-main
 ┣ 📂.github
 ┃ ┗ 📂workflows
 ┃     ┗ 📜example.yml    # Example workflows
 ┣ 📂actions
 ┃ ┣ 📂action-one
 ┃ ┃ ┣ 📜action.yml       # Metadata for action-one
 ┃ ┣ 📂action-two
 ┃ ┃ ┣ 📜action.yml       # Metadata for action-two
 ┣ 📜README.md             # Project documentation
 ┗ 📜LICENSE               # Licensing information
```

- **`.github/workflows/`**: Contains example workflows demonstrating how to use the actions.
- **`actions/`**: Stores individual actions.

---

## Getting Started

### Prerequisites

To use the actions in this repository, ensure you:

- Have a GitHub account.
- Have access to a repository where you want to implement the actions.

### Cloning the Repository

Clone this repository locally to explore and modify the actions:

```
git clone https://github.com/PolGubau/shared-actions.git
```

---

## Usage

To use an action from this repository, include it in your workflow file. Below is an example:

### Example Workflow

```
name: Example Workflow

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Run Shared Action
        uses: PolGubau/shared-actions/actions/action-one@v1.0.0
        with:
          input-param: value
```

### Inputs and Outputs

Refer to the `README.md` file within each action's folder for detailed information about its inputs, outputs, and expected behavior.

---

## Contributing

Contributions are welcome! Follow these steps to get involved:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

Ensure your changes are accompanied by:

- Documentation updates.
- Relevant tests (if applicable).

### Development Standards

- Use clear and concise names for actions and workflows.
- Document all inputs, outputs, and examples.
- Follow semantic versioning for all actions.

---

## License

This repository is licensed under the MIT License. By using or contributing to this repository, you agree to the terms of this license.