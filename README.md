# one-press-ado

## Overview

This project is designed to provide the way to implement one-press project in Azure DevOps platform.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Modules](#modules)
- [License](#license)

## Installation

## Usage

This is the way describe detail how to set up this flow in Azure DevOps.

[Usage](docs/usage.md)

## Modules

This is all modules as technique stacks was required by the flow.

- Azure Devops
  - Project
    - one-press-ado (the core project contains the business logic of the flow).
      - Service connection
            - Service connection of infrastructure vault.
            - Service connections of project vaults.
    - weather-forecast (the real project will be implement the core project).
      - Service connection
            - Service connection of infrastructure vault (was shared by the one-press-ado project).
            - Service connections of project vaults (was shared by the one-press-ado project).
- Azure Services
  - Azure Key Vault
    - Infrastructure vault (contain all secrets involve infrastructure as k8s cred, docker cred, git cred,etc).
    - Project vaults (contain all secrets that involve a specific project by its environment, I prefer each vault for each env that you have).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
