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
| BootStrap 4       | Eclipse STS 4.4+           |

## Steps and Approach

### Initialize Spring Starter project in Eclipse STS

Add necessary dependencies like below:
![spring-dependencies](https://user-images.githubusercontent.com/78957509/170806195-f2af2f73-a2fe-4bb4-8b53-914244503a16.PNG)

### Configure MYSQL database in application.properties
```
spring.datasource.url = jdbc:mysql://{your_mysql_url}/employee_mangement_system?useSSL=false
spring.datasource.username=root
spring.datasource.password={password}

spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL5InnoDBDialect
spring.jpa.hibernate.ddl-auto=update
```

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

##### 1) Create a new Rails app:
