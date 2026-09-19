# KuroLanguage

A programming language with simple syntax, integrated tooling, and its own package ecosystem.

![Version](https://img.shields.io/badge/version-0.1.0-blue)
![Status](https://img.shields.io/badge/status-early%20development-orange)
![License](https://img.shields.io/badge/license-proprietary-lightgrey)
![Target platforms](https://img.shields.io/badge/target%20platforms-Linux%20%7C%20Windows%20%7C%20Android-informational)

> **Early development.** This README describes KuroLanguage 0.1.0. Language syntax and APIs may evolve before a stable release.

KuroLanguage is a programming language built around a simple, readable syntax. It is developed together with its own compiler/toolchain, a command-line interface (`kuro`), and a package ecosystem that supports public and private packages.

## Overview

KuroLanguage aims to provide a programming language whose syntax is simple and easy to understand, while still offering a compiler, a CLI, package management, testing, a build workflow, and its own package ecosystem.

It is not meant to be only a syntax experiment. The project is being shaped into a programming language ecosystem made up of:

- The KuroLanguage language
- Compiler/interpreter tooling
- The `kuro` command-line interface
- Package management
- A package format
- A public/private package workflow
- Multi-platform distribution

## Why KuroLanguage

KuroLanguage is guided by the following principles:

- **Simple syntax** — Keeping the syntax simple and easy to understand is a core goal. Statements end with a newline, and semicolons are not used.
- **Readable code** — Code should be easy to read and follow.
- **Beginner-friendly** — The language is designed to be approachable for people who are new to programming.
- **Integrated tooling** — The compiler/toolchain, CLI, package management, testing, and build workflow are part of KuroLanguage itself.
- **Own package ecosystem** — KuroLanguage defines its own project manifest, lockfile, and package formats.
- **Cross-platform direction** — The project is directed toward a consistent workflow across Linux, Windows, and Android.
- **Practical development workflow** — The `kuro` CLI covers everyday tasks such as setting up, running, building, checking, and testing a project, as well as packaging and publishing.

## Key Characteristics

- Source files use the `.kr` extension.
- A single CLI executable, `kuro`, for running, building, checking, testing, and package workflows.
- A project manifest (`set.kuro`) and a dependency lockfile (`set.lock`).
- Public packages (`.krl`) and private packages (`.krlp`).
- Private packages use authenticated encryption and password-based key derivation.
- Distribution targets Linux, Windows, and Android.

## Quick Example

Create a file named `main.kr`:

```
PrintLine("Hello, KuroLanguage!")
```

Run it with the KuroLanguage CLI:

```bash
kuro run main.kr
```

## Language Basics

The following characteristics of the language are currently documented.

- Source files use the `.kr` extension.
- Statements do not use semicolons. A newline ends a statement.
- Single-line comments start with `//`.
- Multi-line comments are written between `/*` and `*/`.
- Boolean literals are `true` and `false`.
- Logical operators are `&&`, `||`, and `!`.
- Numeric literals support decimal integers and floating-point values.

### Output

```
// Single-line comment
PrintLine("Hello")

/*
  Multi-line comment
*/
Console.PrintLine("Hello")
```

`PrintLine(...)` and `Console.PrintLine(...)` are both valid. `Print(...)` and `Console.Print(...)` are not available.

Language syntax and APIs may evolve before a stable release.

## Project Structure

Example of a KuroLanguage project:

```
my-project/
├── set.kuro
├── set.lock
└── src/
     └── main.kr
```

| File | Description |
| --- | --- |
| `main.kr` | Main source code of the project. |
| `set.kuro` | Project/package manifest. |
| `set.lock` | Dependency lockfile. |

## CLI

The KuroLanguage command-line interface is provided by the `kuro` executable.

| Command | Description |
| --- | --- |
| `kuro help` | Displays CLI help. |
| `kuro --version` | Displays the KuroLanguage version. |
| `kuro init` | Creates/prepares a KuroLanguage project. |
| `kuro run <file>` | Runs a source program. |
| `kuro build <file>` | Builds a program. |
| `kuro check` | Performs project/source checks. |
| `kuro test` | Runs tests. |
| `kuro search <package>` | Searches for a package. |
| `kuro install <package>` | Installs a dependency/package. |
| `kuro pack` | Creates a package artifact. |
| `kuro publish` | Publishes a package. |
| `kuro publish --private` | Publishes a private package. |

This table summarizes each command at a high level. Detailed command behavior is not covered in this README.

## Package Ecosystem

KuroLanguage has its own package ecosystem, covering the project manifest, the dependency lockfile, package formats, and a package workflow driven by the `kuro` CLI.

| Item | Description |
| --- | --- |
| `set.kuro` | Project/package manifest |
| `set.lock` | Dependency lockfile |
| `.krl` | Public package |
| `.krlp` | Private package |

A package's type is determined by the package artifact/domain, not by a `type` field in the manifest.

Packages are installed with `kuro install <package>`. The available package workflow is:

- **Search** — `kuro search <package>`
- **Install** — `kuro install <package>`
- **Pack** — `kuro pack`
- **Publish** — `kuro publish`
- **Private publish** — `kuro publish --private`

### Registry

KuroLanguage is designed to have a package registry. The registry client supports the concepts of package metadata, package versions, package download, public publishing, and private publishing. Registry availability details, including any registry address, are not listed in this README.

## Public and Private Packages

### Public packages

Public packages use the `.krl` format. They are intended for packages that can be used through the KuroLanguage package ecosystem.

### Private packages

Private packages use the `.krlp` format. They use authenticated encryption and password-based key derivation. The current implementation uses Argon2id and ChaCha20-Poly1305.

Protocol-level details of private packages are not documented in this README.

## Installation

KuroLanguage release packages are obtained through the official installation/download website:

<!-- NOTE: Replace the placeholder URL below with the final official installation domain before publishing this README. -->
[Official Installation Page](https://<OFFICIAL-INSTALL-DOMAIN>)

### Linux

KuroLanguage is distributed for Linux as a Debian package (`.deb`) named `kuro`, which provides the `kuro` binary. It is not currently distributed through an APT repository.

Download the package from the official installation page and install it with your system's standard Debian package tooling. Then verify the installation:

```bash
kuro --version
```

The expected output for this release is `kuro 0.1.0`.

### Windows

Windows distribution is planned through an MSI installer, `KuroLanguage-0.1.0.msi`, intended to install the KuroLanguage CLI.

Runtime installation on Windows has not yet been directly verified by the project owner, so Windows support should be considered unverified at this time.

### Android

The Android environment is under development. See [Android Environment](#android-environment).

## Platform Support

| Platform | Distribution | Status |
| --- | --- | --- |
| Linux | Debian package (`.deb`) | Release package available |
| Windows | MSI installer (`KuroLanguage-0.1.0.msi`) | Planned; runtime installation not yet directly verified by the project owner |
| Android | Native Android application / IDE (`.apk` / Android release build) | In development |

KuroLanguage is directed toward a consistent workflow across these platforms: one language, one CLI/toolchain, and one package ecosystem. This is a project direction; features are not claimed to be identical on every platform at this time.

## Android Environment

KuroLanguage for Android is being developed as a native Android application/IDE. It is not intended to be merely a Termux wrapper.

The planned environment includes:

```
KuroLanguage Android
├── code editor
├── project management
├── console
├── diagnostics
└── KuroLanguage engine
```

- **User interface:** Kotlin / Jetpack Compose
- **Language engine:** Rust, reused from the KuroLanguage core

Android builds and releases are planned to use GitHub Actions. The Android release build (`.apk`) is in development.

## Development Status

KuroLanguage is actively being developed. The current release is 0.1.0, and the project is in an early stage of development.

Current project direction includes:

- Language implementation
- Compiler/toolchain
- CLI
- Package management
- Package formats
- Package registry
- Cross-platform distribution
- Android development environment

Additional notes:

- The compiler has reached an internal milestone that the project owner considers complete. This does not mean the language or toolchain is finished; KuroLanguage as a whole remains under development.
- Parts of the toolchain are covered by automated tests. For the CLI, this includes command parsing/dispatch and rejection cases.
- Windows runtime installation has not yet been directly verified, and the Android environment is still in development (see [Platform Support](#platform-support)).
- APIs and language syntax may evolve before a stable release.

## Roadmap

This roadmap lists areas of development. It is not a commitment, and no release dates are attached.

- Language feature expansion
- Improved diagnostics
- Package ecosystem
- Registry
- Android IDE
- Cross-platform releases
- Developer tooling
- Documentation
- Ecosystem expansion

## Proprietary Software

KuroLanguage and its source code are proprietary software owned by YanKuro.

Distribution and usage are subject to the project's applicable license/terms.

## Links

<!-- NOTE: Replace the placeholder URL below with the final official installation domain before publishing this README. -->
- [Official Installation Page](https://<OFFICIAL-INSTALL-DOMAIN>)
