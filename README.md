KuroLanguage

<p align="center">
  <strong>A modern programming language designed for simplicity.</strong>
</p><p align="center">
  Learn, build, and distribute applications with KuroLanguage.
</p><p align="center">""Status" (https://img.shields.io/badge/status-in%20development-yellow)"
""Platform" (https://img.shields.io/badge/platform-Linux%20%7C%20Windows%20%7C%20Android-blue)"

</p>---

Overview

KuroLanguage is a programming language and development ecosystem designed to make programming easier to learn and easier to build with.

KuroLanguage provides its own language tooling, command-line interface, package ecosystem, project system, and cross-platform development experience.

The project is designed to provide a consistent experience across desktop and mobile platforms.

---

Highlights

- Simple and beginner-friendly syntax
- ".kr" source files
- No semicolons
- Built-in interpreter
- Native compilation
- Integrated command-line tools
- Package management
- Dependency management
- Public and private packages
- ".krl" package format
- ".krlp" private package format
- Linux support
- Windows support
- Android development environment

---

Hello, KuroLanguage

A minimal KuroLanguage program:

PrintLine("Hello, KuroLanguage!")

KuroLanguage uses newlines as statement boundaries, so semicolons are not required.

Functions

Functions are declared using "Func" and called using "OpenFunc".

Func hello()
    PrintLine("Hello from KuroLanguage!")

OpenFunc hello()

---

Language

KuroLanguage is designed around a clean and readable syntax.

Source Files

KuroLanguage programs use the:

.kr

file extension.

Comments

Single-line:

// This is a comment

Multi-line:

/*
   This is a
   multi-line comment
*/

Boolean Values

true
false

Logical Operators

&&
||
!

Output

Standard output:

PrintLine("Hello")

Namespaced output:

Console.PrintLine("Hello")

---

Kuro CLI

KuroLanguage includes the "kuro" command-line tool.

kuro help

Available commands:

Command| Description
"kuro init"| Create a new project
"kuro run <file>"| Run a KuroLanguage program
"kuro build <file>"| Build a KuroLanguage program
"kuro check"| Check a project
"kuro test"| Run project tests
"kuro search <package>"| Search for packages
"kuro install <package>"| Install a package
"kuro pack"| Create a package
"kuro publish"| Publish a package

Check the installed version:

kuro --version

---

Installation

KuroLanguage provides official installation packages for supported platforms.

Linux

The recommended installation method is through the official KuroLanguage installer website:

https://kurolanguage/install.my.id

From the website:

1. Select Linux.
2. Download the appropriate ".deb" package.
3. Open a terminal in the download directory.
4. Install the package:

sudo apt install ./kuro_0.1.0_amd64.deb

5. Verify the installation:

kuro --version

This method does not require adding a third-party APT repository.

«The package name and version may change with future releases.»

---

Windows

Download the official Windows installer from:

https://kurolanguage/install.my.id

Select Windows and download the ".msi" installer.

After installation, open PowerShell or Command Prompt:

kuro --version

---

Android

A native Android application is currently in development.

The Android application is designed to provide a complete KuroLanguage development environment directly on Android, including:

- Code editor
- Project management
- Run
- Build
- Console output
- Diagnostics
- KuroLanguage development tools

Android releases will be distributed through the official KuroLanguage installation page.

---

Package Ecosystem

KuroLanguage includes its own package ecosystem.

Package Formats

Extension| Purpose
".krl"| Public KuroLanguage package
".krlp"| Private KuroLanguage package
"set.kuro"| Project/package manifest
"set.lock"| Dependency lockfile

Install a package:

kuro install <package>

Create a package:

kuro pack

Publish a package:

kuro publish

Publish a private package:

kuro publish --private

---

Public Packages

Public KuroLanguage packages use the ".krl" format.

Public packages are intended for packages that can be distributed as readable KuroLanguage projects.

---

Private Packages

Private packages use the ".krlp" format.

Private packages are designed for projects where the package contents should not be distributed as directly readable source.

Private package protection uses authenticated encryption and password-based key derivation.

---

Cross-Platform

KuroLanguage is being developed for multiple platforms.

Platform| Status
Linux| Available
Windows| Release preparation
Android| In development

The goal is to provide a consistent KuroLanguage experience across supported platforms.

---

Android Development Environment

The upcoming Android application is designed as a native development environment rather than a terminal wrapper.

The planned experience includes:

┌─────────────────────────────┐
│       KuroLanguage          │
├─────────────────────────────┤
│ Project                     │
│                             │
│  main.kr                    │
│                             │
│  PrintLine("Hello")         │
│                             │
├─────────────────────────────┤
│ Run    Build    Check       │
├─────────────────────────────┤
│ Console                     │
│ > Hello                     │
└─────────────────────────────┘

Android builds and releases are planned to use automated CI/CD.

---

Project Status

KuroLanguage is actively under development.

Current development focuses on:

- Language stability
- Compiler and runtime improvements
- CLI improvements
- Package ecosystem
- Registry infrastructure
- Release packaging
- Windows distribution
- Android development environment

Features and interfaces may change before the first stable release.

---

Roadmap

Language

- [x] Lexer
- [x] Parser
- [x] Semantic analysis
- [x] Interpreter foundation
- [x] Compiler foundation
- [ ] Stable language specification
- [ ] Expanded standard library

Tooling

- [x] Kuro CLI
- [x] Project initialization
- [x] Package management foundation
- [x] Package packing
- [x] Public package format
- [x] Private package format
- [ ] Registry improvements
- [ ] Documentation tooling

Platforms

- [x] Linux package
- [x] Windows executable
- [ ] Windows release validation
- [ ] Android native application
- [ ] Automated Android releases

---

Downloads

Official downloads will be available through:

https://kurolanguage/install.my.id

The installation page will provide the appropriate package for each supported platform.

---

Contributing

KuroLanguage is a proprietary project.

The project does not distribute its internal implementation publicly.

For questions, bug reports, feature requests, or other inquiries, use the official project channels.

---

License

KuroLanguage is proprietary software.

Usage and distribution are subject to the project's official license and terms.

---

<p align="center">
  <strong>KuroLanguage</strong>
</p><p align="center">
  Build with KuroLanguage.
</p>
