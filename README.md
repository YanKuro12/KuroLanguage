KuroLanguage

"Version" (https://img.shields.io/badge/version-0.1.0-blue)
"Status" (https://img.shields.io/badge/status-early%20development-orange)
"License" (https://img.shields.io/badge/license-proprietary-lightgrey)
"Platforms" (https://img.shields.io/badge/platforms-Linux%20%7C%20Windows%20%7C%20Android-informational)

«A simple, readable programming language with integrated tooling and its own package ecosystem.»

KuroLanguage is a proprietary programming language designed around simple syntax, readable source code, integrated development tooling, and an independent package ecosystem.

The project includes the KuroLanguage language, its compiler and runtime tooling, the "kuro" command-line interface, package management, package formats, and cross-platform distribution.

«Development status: KuroLanguage 0.1.0 is an early-development release. Language syntax, APIs, tooling, and package ecosystem behavior may evolve before a stable release.»

---

Overview

KuroLanguage is being developed as a complete programming language ecosystem rather than only a language syntax implementation.

The ecosystem includes:

- KuroLanguage programming language
- Compiler and runtime tooling
- "kuro" command-line interface
- Package management
- Project manifests and lockfiles
- Public and private package formats
- Package publishing and distribution
- Linux, Windows, and Android support

The goal is to provide a consistent development experience while keeping the language and its tooling straightforward to use.

---

Why KuroLanguage?

KuroLanguage is built around several principles.

Simple

KuroLanguage keeps syntax straightforward and avoids unnecessary syntax where possible. Statements do not require semicolons.

Readable

The language is designed to keep source code easy to read and understand.

Beginner-friendly

KuroLanguage is intended to be approachable for people who are learning programming while still providing a complete development workflow.

Integrated

Running, building, checking, testing, packaging, and publishing are handled through the "kuro" CLI.

Independent ecosystem

KuroLanguage has its own project manifest, lockfile, package formats, and package workflow.

Cross-platform

The project is being developed toward a consistent workflow across Linux, Windows, and Android.

---

Language

KuroLanguage source files use the ".kr" extension.

Current documented language characteristics include:

- Statements end at a newline.
- Semicolons are not required.
- Single-line comments use "//".
- Multi-line comments use "/* ... */".
- Boolean literals are "true" and "false".
- Logical operators include "&&", "||", and "!".
- Decimal integer literals are supported.
- Floating-point literals are supported.

Output

PrintLine("Hello, KuroLanguage!")

The namespace form is also supported:

Console.PrintLine("Hello, KuroLanguage!")

The following APIs are not available:

Print(...)
Console.Print(...)

Language syntax and APIs may evolve before a stable release.

---

Quick Start

A minimal KuroLanguage source file can look like this:

PrintLine("Hello, KuroLanguage!")

If the file is located at "src/main.kr", run it with:

kuro run src/main.kr

---

Project Structure

A KuroLanguage project uses a dedicated "src" directory for source code.

my-project/
├── set.kuro
├── set.lock
└── src/
    └── main.kr

Path| Description
"set.kuro"| Project and package manifest
"set.lock"| Dependency lockfile
"src/"| Project source directory
"src/main.kr"| Main source file

---

CLI

The KuroLanguage command-line interface is provided through the "kuro" executable.

Command| Description
"kuro help"| Display CLI help
"kuro --version"| Display the installed KuroLanguage version
"kuro init"| Initialize a KuroLanguage project
"kuro run <file>"| Run a KuroLanguage source file
"kuro build <file>"| Build a KuroLanguage program
"kuro check"| Check the project or source
"kuro test"| Run project tests
"kuro search <package>"| Search for a package
"kuro install <package>"| Install a package or dependency
"kuro pack"| Create a package artifact
"kuro publish"| Publish a package
"kuro publish --private"| Publish a private package

---

Package Ecosystem

KuroLanguage has its own package system.

Project files

set.kuro
set.lock

"set.kuro" contains project and package configuration.

"set.lock" contains resolved dependency information.

Package formats

Extension| Type
".krl"| Public package
".krlp"| Private package

Package type is determined by the package artifact and its domain rather than by a "type" field in the manifest.

---

Package Workflow

Search

kuro search <package>

Search for packages.

Install

kuro install <package>

Install a package or dependency.

Pack

kuro pack

Create a package artifact from the project.

Publish

kuro publish

Publish a public package.

For private packages:

kuro publish --private

---

Public Packages

Public packages use the ".krl" format.

They are intended for packages distributed through the KuroLanguage package ecosystem.

---

Private Packages

Private packages use the ".krlp" format.

Private packages use password-based key derivation and authenticated encryption.

The current implementation uses:

- Argon2id
- ChaCha20-Poly1305

Protocol-level security details are intentionally not documented in the main README.

---

Package Registry

KuroLanguage includes registry tooling for:

- Package discovery
- Package metadata
- Package versions
- Package downloads
- Public publishing
- Private publishing

Registry infrastructure is still part of the broader KuroLanguage ecosystem and may evolve during development.

---

Installation

KuroLanguage distributions are provided through the official installation page.

Official installation page:
"<OFFICIAL-INSTALL-DOMAIN>"

Replace the placeholder with the final official domain before publishing the README.

Linux

KuroLanguage is distributed as a Debian package:

.deb

The package provides the "kuro" executable.

After installation:

kuro --version

Expected output for version 0.1.0:

kuro 0.1.0

KuroLanguage is currently distributed as a Debian package rather than through an APT repository.

Windows

Windows distribution uses an MSI installer:

KuroLanguage-0.1.0.msi

The installer is intended to install the KuroLanguage CLI on Windows.

The MSI has been prepared, but final Windows runtime installation has not yet been directly verified by the project owner.

Android

The Android environment is currently under development.

See "Android Environment" (#android-environment).

---

Platform Support

Platform| Distribution| Status
Linux| Debian package (".deb")| Available
Windows| MSI installer (".msi")| Release preparation; runtime verification pending
Android| Native Android application| In development

The long-term goal is to provide a consistent KuroLanguage workflow across supported platforms.

This does not mean every feature is currently available on every platform.

---

Android Environment

KuroLanguage for Android is being developed as a native Android application rather than a Termux wrapper.

The planned environment includes:

KuroLanguage Android
├── Editor
├── Project Manager
├── Console
├── Diagnostics
└── KuroLanguage Engine

The Android application is being developed using:

- Kotlin
- Jetpack Compose
- Rust-based KuroLanguage engine

The Android release build is still in development.

Android builds and releases are planned to use GitHub Actions.

---

Development Status

KuroLanguage 0.1.0 is an early-development release.

Current development areas include:

- Language implementation
- Compiler and runtime tooling
- CLI
- Package management
- Package formats
- Package registry
- Cross-platform distribution
- Android development environment
- Documentation

The compiler has reached a major internal development milestone, while the overall KuroLanguage ecosystem remains under active development.

Automated testing is also used throughout the development of the KuroLanguage tooling.

---

Roadmap

The roadmap represents the current development direction and does not include guaranteed release dates.

Language

- Expand language capabilities
- Improve diagnostics
- Refine syntax and APIs
- Continue language specification work

Tooling

- Improve CLI workflows
- Expand testing capabilities
- Improve developer tooling
- Expand documentation

Package Ecosystem

- Continue registry development
- Improve package discovery
- Improve package distribution
- Expand public and private package workflows

Platforms

- Continue Windows verification
- Continue Android development
- Improve cross-platform consistency

---

Design Direction

KuroLanguage is being developed around one central idea:

«The language, tooling, and package ecosystem should work together as one development environment.»

The compiler, CLI, project system, package manager, package formats, and distribution workflow are designed as parts of the same ecosystem.

The intended workflow is straightforward:

Create
  |
  v
Develop
  |
  v
Check / Test
  |
  v
Build
  |
  v
Pack
  |
  v
Publish

---

Versioning

Current release:

KuroLanguage 0.1.0

Because the project is still in early development, users should expect changes to:

- Language syntax
- Language APIs
- CLI behavior
- Package behavior
- Package formats
- Platform support

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

Replace these placeholders with the official URLs before publishing.

---

Project Status

KuroLanguage 0.1.0 - Early Development

KuroLanguage is actively evolving toward a complete programming language ecosystem with its own language, development tooling, package system, and multi-platform environment.