# EmployeeManagementSystem-CRUD

This report will document the approach to create a full stack web application for the Employee Management System (EMS) using Spring Boot and Angular

## Architecture overview

![EMS-architecture drawio](https://user-images.githubusercontent.com/78957509/170805013-728932de-93e6-41ac-8ed4-bec02694cecb.png)

Angular app contains templates which render the single page web displaying to clients. The templates are associated with components which contain HTML templates that declares what renders on the page, a TypeScript class that defines behavior, and a CSS selector that defines how the component is used in a template. The services are responsible for communicating with Spring Boot Controller via HTTP. 

Spring Boot app contains the controller which routes to a desired function based on given URI path. Spring data JPA defines repository interfaces which simply performs CRUD operation, sorting, and pagination on MYSQL database 

[See the manual][manual] for setup and usage instructions

## Technology and versioning

| Front-end         | Back-end                   |
| ----------------- | -----------------          |
| Angular 10        | Spring Boot 2.7.0          |
| TypeScript        | Java SE 17                 |
| NodeJS 14.7       | Maven 3.2+                 |
| NPM 8.0+          | Embedded Tomcat            |
| VSCode 1.6+       | MySQL Database (Workbench) |
| BootStrap 4       |                            |

## Installation

### macOS

`gh` is available via [Homebrew][], [MacPorts][], [Conda][], [Spack][], and as a downloadable binary from the [releases page][].

#### Homebrew

| Install:          | Upgrade:          |
| ----------------- | ----------------- |
| `brew install gh` | `brew upgrade gh` |

#### MacPorts

| Install:               | Upgrade:                                       |
| ---------------------- | ---------------------------------------------- |
| `sudo port install gh` | `sudo port selfupdate && sudo port upgrade gh` |

#### Conda

| Install:                                 | Upgrade:                                |
|------------------------------------------|-----------------------------------------|
| `conda install gh --channel conda-forge` | `conda update gh --channel conda-forge` |

Additional Conda installation options available on the [gh-feedstock page](https://github.com/conda-forge/gh-feedstock#installing-gh).

#### Spack

| Install:           | Upgrade:                                 |
| ------------------ | ---------------------------------------- |
| `spack install gh` | `spack uninstall gh && spack install gh` |

### Linux & BSD

`gh` is available via [Homebrew](#homebrew), [Conda](#conda), [Spack](#spack), and as downloadable binaries from the [releases page][].

For instructions on specific distributions and package managers, see [Linux & BSD installation](./docs/install_linux.md).

### Windows

`gh` is available via [WinGet][], [scoop][], [Chocolatey][], [Conda](#conda), and as downloadable MSI.

#### WinGet

| Install:            | Upgrade:            |
| ------------------- | --------------------|
| `winget install --id GitHub.cli` | `winget upgrade --id GitHub.cli` |

#### scoop

| Install:           | Upgrade:           |
| ------------------ | ------------------ |
| `scoop install gh` | `scoop update gh`  |

#### Chocolatey

| Install:           | Upgrade:           |
| ------------------ | ------------------ |
| `choco install gh` | `choco upgrade gh` |

#### Signed MSI

MSI installers are available for download on the [releases page][].

### GitHub Actions

GitHub CLI comes pre-installed in all [GitHub-Hosted Runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners).

### Other platforms

Download packaged binaries from the [releases page][].

### Build from source

See here on how to [build GitHub CLI from source][build from source].

## Comparison with hub

For many years, [hub][] was the unofficial GitHub CLI tool. `gh` is a new project that helps us explore
what an official GitHub CLI tool can look like with a fundamentally different design. While both
tools bring GitHub to the terminal, `hub` behaves as a proxy to `git`, and `gh` is a standalone
tool. Check out our [more detailed explanation][gh-vs-hub] to learn more.

[manual]: https://cli.github.com/manual/
[Homebrew]: https://brew.sh
[MacPorts]: https://www.macports.org
[winget]: https://github.com/microsoft/winget-cli
[scoop]: https://scoop.sh
[Chocolatey]: https://chocolatey.org
[Conda]: https://docs.conda.io/en/latest/
[Spack]: https://spack.io
[releases page]: https://github.com/cli/cli/releases/latest
[hub]: https://github.com/github/hub
[contributing]: ./.github/CONTRIBUTING.md
[gh-vs-hub]: ./docs/gh-vs-hub.md
[build from source]: ./docs/source.md
