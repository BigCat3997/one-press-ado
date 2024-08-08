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

Azure Devops:
    - Project
        - one-press-ado[^1].
            - Service connection
                - infrastructure-vars-vault-service-connection.
                - project-dev-vars-vault-service-connection.
                - project-uat-vars-vault-service-connection.
        - weather-forecast[^2]. (the real project will be implement the core project).
            - Service connection
                - infrastructure-vars-vault-service-connection-weather-forecast[^3].
                - project-dev-vars-vault-service-connection-weather-forecast.
                - project-uat-vars-vault-service-connection-weather-forecast.

Azure Services:
    - Azure Key Vault
        - Infrastructure vault (contain all secrets involve infrastructure as k8s cred, docker cred, git cred,etc).
        - Project vaults (contain all secrets that involve a specific project by its environment, I prefer each vault for each env that you have).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

[^1]: The `one-press-ado` project is the core project that contains the business logic of the flow.
[^2]: The `weather-forecast` project is the real project will be implement the core project.
[^3]: When we share service connection whose name will have suffix is name of project was share.
