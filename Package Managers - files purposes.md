## $${\color{red}Package \ Managers \ - \ files \ purposes}$$

Common **file names, ecosystems, and their purpose**.

---

### JavaScript / Node Ecosystem

| File                | Package Manager   | Purpose                                             |
| ------------------- | ----------------- | --------------------------------------------------- |
| `package.json`      | npm / yarn / pnpm | Project metadata, dependencies, scripts, version    |
| `package-lock.json` | npm               | Locks dependency versions for reproducible installs |
| `yarn.lock`         | yarn              | Deterministic dependency tree lock file             |
| `pnpm-lock.yaml`    | pnpm              | Lock file for pnpm dependency resolution            |
| `.npmrc`            | npm               | npm configuration (registry, auth, cache)           |
| `.yarnrc.yml`       | yarn              | Yarn configuration file                             |
| `node_modules/`     | npm / yarn / pnpm | Installed dependencies directory                    |

---

### PHP

| File            | Package Manager | Purpose                                |
| --------------- | --------------- | -------------------------------------- |
| `composer.json` | Composer        | PHP dependencies, autoloading, scripts |
| `composer.lock` | Composer        | Locks exact dependency versions        |
| `vendor/`       | Composer        | Installed packages directory           |

---

### Python

| File               | Package Manager      | Purpose                               |
| ------------------ | -------------------- | ------------------------------------- |
| `requirements.txt` | pip                  | List of project dependencies          |
| `Pipfile`          | pipenv               | Dependency and environment definition |
| `Pipfile.lock`     | pipenv               | Locked dependency versions            |
| `pyproject.toml`   | poetry / pip / build | Modern Python build configuration     |
| `poetry.lock`      | poetry               | Locked dependencies for Poetry        |
| `setup.py`         | setuptools           | Python package build script           |
| `setup.cfg`        | setuptools           | Declarative package configuration     |
| `.venv/`           | pip / poetry         | Virtual environment directory         |

---

### Ruby

| File           | Package Manager | Purpose                     |
| -------------- | --------------- | --------------------------- |
| `Gemfile`      | Bundler         | Ruby gem dependencies       |
| `Gemfile.lock` | Bundler         | Locked gem versions         |
| `.bundle/`     | Bundler         | Local bundler configuration |

---

### Java / JVM

| File              | Package Manager | Purpose                            |
| ----------------- | --------------- | ---------------------------------- |
| `pom.xml`         | Maven           | Dependencies, build configuration  |
| `build.gradle`    | Gradle          | Gradle build and dependency config |
| `settings.gradle` | Gradle          | Multi-project configuration        |
| `gradle.lockfile` | Gradle          | Dependency version lock            |

---

### Rust

| File         | Package Manager | Purpose                           |
| ------------ | --------------- | --------------------------------- |
| `Cargo.toml` | Cargo           | Project metadata and dependencies |
| `Cargo.lock` | Cargo           | Locked dependency versions        |
| `target/`    | Cargo           | Build output directory            |

---

### Go

| File     | Package Manager | Purpose                          |
| -------- | --------------- | -------------------------------- |
| `go.mod` | Go Modules      | Module dependencies and versions |
| `go.sum` | Go Modules      | Dependency checksums             |

---

### .NET

| File                 | Package Manager | Purpose                                |
| -------------------- | --------------- | -------------------------------------- |
| `.csproj`            | NuGet           | Project configuration and dependencies |
| `packages.config`    | NuGet (legacy)  | List of dependencies                   |
| `nuget.config`       | NuGet           | NuGet configuration                    |
| `packages.lock.json` | NuGet           | Locked dependency versions             |

---

### Swift / iOS

| File               | Package Manager | Purpose                    |
| ------------------ | --------------- | -------------------------- |
| `Package.swift`    | SwiftPM         | Package definition         |
| `Package.resolved` | SwiftPM         | Locked dependency versions |
| `Podfile`          | CocoaPods       | iOS dependencies           |
| `Podfile.lock`     | CocoaPods       | Locked pod versions        |

---

### C / C++

| File            | Package Manager | Purpose                        |
| --------------- | --------------- | ------------------------------ |
| `conanfile.txt` | Conan           | Dependency definition          |
| `conanfile.py`  | Conan           | Programmatic dependency config |
| `vcpkg.json`    | vcpkg           | Package manifest               |

---

### Lock Files (Important Rule)

**Lock files ensure reproducible builds.**

Common examples:

```
package-lock.json
yarn.lock
pnpm-lock.yaml
composer.lock
poetry.lock
Gemfile.lock
Cargo.lock
Podfile.lock
```

General rule:

* **Commit lock files** for applications
* **Optional for libraries**

---

### Quick Concept Summary

| Concept          | Meaning                                                 |
| ---------------- | ------------------------------------------------------- |
| Manifest file    | Declares dependencies (`package.json`, `composer.json`) |
| Lock file        | Freezes exact versions (`package-lock.json`)            |
| Vendor directory | Installed packages (`node_modules`, `vendor`)           |
| Config file      | Package manager settings (`.npmrc`, `nuget.config`)     |

---

✅ **Typical workflow**

```
1 declare dependencies → manifest file
2 install dependencies → package manager
3 versions locked → lock file
4 packages installed → vendor directory
```
