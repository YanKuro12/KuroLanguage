KuroLanguage

«A simple, readable programming language with integrated tooling and its own package ecosystem.»

"Version" (https://img.shields.io/badge/version-0.1.0-blue)
"Status" (https://img.shields.io/badge/status-early%20development-orange)
"License" (https://img.shields.io/badge/license-proprietary-lightgrey)
"Platforms" (https://img.shields.io/badge/platforms-Linux%20%7C%20Windows%20%7C%20Android-informational)

KuroLanguage is a proprietary programming language designed around simple syntax, readable source code, integrated development tooling, and an independent package ecosystem.

The project includes the KuroLanguage language, its compiler and runtime tooling, the "kuro" command-line interface, package management, package formats, and cross-platform distribution.

«Development status: KuroLanguage 0.1.0 is an early-development release. Language syntax, APIs, tooling, and package ecosystem behavior may evolve before a stable release.»

---

Overview

KuroLanguage is being developed as a complete programming language ecosystem rather than only a language syntax implementation.

The ecosystem is built around several core components:

- KuroLanguage — the programming language itself
- KuroLanguage toolchain — compilation, execution, checking, and testing
- "kuro" CLI — the primary command-line interface
- Package management — dependency installation and package workflows
- Package formats — public and private package artifacts
- Project management — project manifests and dependency lockfiles
- Cross-platform distribution — Linux, Windows, and Android
- Android development environment — a native Android environment currently under development

The goal is to provide a consistent development experience while keeping the language and its tooling straightforward to use.

---

Why KuroLanguage?

KuroLanguage is guided by a few core principles.

Simple

KuroLanguage avoids unnecessary syntax where possible. Statements do not require semicolons, and source code is designed to remain easy to read.

Readable

The language is designed so that source code can be understood without excessive syntactic noise.

Beginner-friendly

KuroLanguage is intended to be approachable for people learning programming while still providing the tooling required to build real projects.

Integrated

Language execution, building, checking, testing, and package workflows are exposed through the "kuro" CLI.

Independent ecosystem

KuroLanguage defines its own project manifest, lockfile, package formats, and package workflow rather than relying on another programming language's package system.

Cross-platform

The project is being developed toward a common workflow across Linux, Windows, and Android.

---

Language

KuroLanguage source files use the ".kr" extension.

Some currently documented language characteristics include:

- Statements end at a newline.
- Semicolons are not required.
- Single-line comments use "//".
- Multi-line comments use "/* ... */".
- Boolean literals are "true" and "false".
- Logical operators include "&&", "||", and "!".
- Decimal integer literals are supported.
- Floating-point literals are supported.

Output

The currently defined output APIs include:

PrintLine("Hello, KuroLanguage!")

The namespace form is also supported:

Console.PrintLine("Hello, KuroLanguage!")

The following APIs are not part of the current interface:

Print(...)
Console.Print(...)

Language syntax and APIs may continue to change while KuroLanguage is in development.

---

Quick Start

A minimal KuroLanguage source file can look like:

PrintLine("Hello, KuroLanguage!")

If the file is located at "src/main.kr", it can be executed with:

kuro run src/main.kr

The exact project workflow may expand as the language and CLI continue to develop.

---

Project Structure

A KuroLanguage project uses a dedicated "src" directory for source code.

my-project/
├── set.kuro
├── set.lock
└── src/
    └── main.kr

Path| Purpose
"set.kuro"| Project and package manifest
"set.lock"| Dependency lockfile
"src/"| Project source directory
"src/main.kr"| Main source file / project entry source

Keeping source code under "src/" separates project metadata from the actual KuroLanguage source tree.

---

"kuro" CLI

The KuroLanguage command-line interface is provided through the "kuro" executable.

Available commands

Command| Purpose
"kuro help"| Display CLI help
"kuro --version"| Display the installed KuroLanguage version
"kuro init"| Initialize a KuroLanguage project
"kuro run <file>"| Run a KuroLanguage source file
"kuro build <file>"| Build a KuroLanguage program
"kuro check"| Check the project/source
"kuro test"| Run project tests
"kuro search <package>"| Search for a package
"kuro install <package>"| Install a package/dependency
"kuro pack"| Create a package artifact
"kuro publish"| Publish a package
"kuro publish --private"| Publish a private package

The CLI is intended to be the primary interface for common KuroLanguage development workflows.

---

Package Ecosystem

KuroLanguage has its own package model.

Projects and packages use two important project-level files:

set.kuro
set.lock

Manifest

"set.kuro" describes project/package metadata and dependency configuration.

Example:

nama = "KuroTest"
version = "1.0.0"

Additional manifest capabilities are part of the KuroLanguage package system.

Lockfile

"set.lock" records resolved dependency information so that dependency state can be reproduced consistently.

Package formats

Extension| Type
".krl"| Public package
".krlp"| Private package

Package type is determined by the package artifact/domain rather than a "type" field in the project manifest.

---

Package Workflow

Package operations are integrated into the "kuro" CLI.

Search

kuro search <package>

Search for available packages.

Install

kuro install <package>

Install a package or project dependency.

Pack

kuro pack

Create a package artifact from the project.

Publish

kuro publish

Publish a public package.

Private publishing is available through:

kuro publish --private

---

Public Packages

Public packages use the ".krl" package format.

They are intended for packages distributed through the KuroLanguage package ecosystem.

Public packages are designed to provide a straightforward way to distribute reusable KuroLanguage projects and libraries.

---

Private Packages

Private packages use the ".krlp" format.

Private package protection uses password-based key derivation and authenticated encryption.

The current cryptographic implementation uses:

- Argon2id for password-based key derivation
- ChaCha20-Poly1305 for authenticated encryption

Cryptographic protocol details are intentionally not documented in the main README.

«Private package encryption is a security mechanism, not a guarantee that package contents are impossible to reverse-engineer.»

---

Package Registry

KuroLanguage includes registry tooling for package discovery, version information, package downloads, and publishing workflows.

Registry infrastructure is still part of the broader KuroLanguage ecosystem and may evolve during development.

Registry addresses and deployment-specific details are intentionally omitted from this README.

---

Installation

KuroLanguage distributions are provided through the official installation/download page.

Official installation page:
"<OFFICIAL-INSTALL-DOMAIN>"

Replace the placeholder above with the final official installation domain before publishing the README.

---

Linux

Linux distribution uses the Debian package format:

.deb

The package provides the "kuro" executable.

After installation, verify the CLI with:

kuro --version

For KuroLanguage 0.1.0, the expected version output is:

kuro 0.1.0

KuroLanguage is currently distributed as a Debian package rather than through an APT repository.

---

Windows

Windows distribution uses an MSI installer:

KuroLanguage-0.1.0.msi

The installer is intended to install the KuroLanguage CLI on Windows.

The Windows installer has been prepared, but final runtime installation and behavior have not yet been directly verified by the project owner.

---

Android

KuroLanguage for Android is being developed as a native Android application, rather than as a terminal wrapper around Termux.

The planned environment includes:

KuroLanguage Android
├── Editor
├── Project Manager
├── Console
├── Diagnostics
└── KuroLanguage Engine

The application is planned around:

- Kotlin
- Jetpack Compose
- Rust-based KuroLanguage engine

The Android application is still under development.

Android release builds are planned to use automated CI/CD through GitHub Actions.

---

Platform Support

Platform| Distribution| Current status
Linux| ".deb"| Available
Windows| ".msi"| Release preparation / runtime verification pending
Android| Native Android application| In development

The long-term direction is a consistent KuroLanguage ecosystem across supported platforms.

This does not imply that every feature is currently available or identical on every platform.

---

Development Status

KuroLanguage is currently in active development.

Version "0.1.0" represents an early stage of the project rather than a stable language specification.

Current development areas include:

- Language implementation
- Compiler and runtime tooling
- CLI development
- Project management
- Package management
- Package formats
- Package registry infrastructure
- Cross-platform distribution
- Android development environment
- Documentation

The compiler/toolchain has progressed through major implementation milestones, while the overall language and ecosystem continue to evolve.

Automated testing is also used throughout the development of the KuroLanguage tooling.

---

Roadmap

The roadmap represents development direction rather than guaranteed release commitments.

Language

- Expand language capabilities
- Improve language diagnostics
- Continue refining syntax and APIs
- Stabilize the language specification

Tooling

- Improve CLI workflows
- Improve diagnostics
- Expand testing capabilities
- Improve developer tooling
- Expand documentation

Package Ecosystem

- Continue registry development
- Improve package discovery
- Improve package distribution
- Expand public/private package workflows

Platforms

- Continue Windows support and verification
- Develop the native Android environment
- Improve cross-platform consistency

No specific release dates are attached to these roadmap items.

---

Design Direction

KuroLanguage is being developed around a simple idea:

«The language, tooling, and package ecosystem should work together as one development environment.»

Instead of treating the compiler, CLI, package manager, project files, and package distribution as unrelated tools, KuroLanguage is designed to provide them as parts of the same ecosystem.

This approach is intended to make the path from creating a project to running, testing, building, packaging, and distributing it straightforward.

---

Versioning

The current release is:

KuroLanguage 0.1.0

Because the project is still in early development, users should expect changes to:

- language syntax
- language APIs
- CLI behavior
- package behavior
- package formats
- platform support

Stable compatibility guarantees will be defined as the project approaches a stable release.

---

Proprietary Software

KuroLanguage and its source code are proprietary software owned by YanKuro.

The source code is not distributed as an open-source project.

Use and distribution of KuroLanguage are subject to the applicable license and terms provided with the software.

---

Links

- Official Installation: "<OFFICIAL-INSTALL-DOMAIN>"
- Documentation: "<DOCUMENTATION-URL>"
- Project Website: "<PROJECT-WEBSITE>"

Replace placeholders with official URLs before publishing.

---

Project Status

KuroLanguage 0.1.0 — Early Development

The project is actively evolving toward a complete programming language ecosystem with its own language, tooling, package system, and multi-platform development environment