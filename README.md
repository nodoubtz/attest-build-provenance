# Attest Build Provenance

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

An Action for generating build provenance attestations for workflow artifacts. This repository is a fork of [actions/attest-build-provenance](https://github.com/actions/attest-build-provenance), aimed at simplifying and securing the process of attesting builds.

## Features

- **Provenance Generation**: Automatically generates attestations for workflow artifacts.
- **Secure Builds**: Ensures the integrity and authenticity of build artifacts.
- **Customizable**: Easily integrates into existing workflows.

## Getting Started

### Prerequisites

- A GitHub account and access to a repository where you want to set up the action.
- Basic knowledge of GitHub Actions and workflows.

### Installation

1. Add the action to your GitHub repository as part of your workflow.
2. Example usage:

   ```yaml
   name: Build and Attest
   on:
     push:
       branches:
         - main
   jobs:
     build-and-attest:
       runs-on: ubuntu-latest
       steps:
         - name: Checkout code
           uses: actions/checkout@v3

         - name: Build
           run: |
             echo "Building project..."
             # Add your build commands here

         - name: Generate Provenance
           uses: nodoubtz/attest-build-provenance@main
           with:
             # Add any required inputs here
   ```

3. Customize as needed for your project.

## Documentation

For detailed documentation, see the [original repository](https://github.com/actions/attest-build-provenance).

## Contributing

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with clear documentation of your changes.

## License

This repository is licensed under the [MIT License](LICENSE).

## Acknowledgments

This repository is a fork of the [attest-build-provenance](https://github.com/actions/attest-build-provenance) project by the GitHub Actions team.
