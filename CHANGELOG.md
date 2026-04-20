# Changelog

All notable changes to the Qualimetry Ansible Analyzer for IntelliJ are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.2.9] - 2026-04-21

### Fixed

- Republish to clear a JetBrains Marketplace verifier failure ("plugin archive file cannot be extracted") observed against 3.2.8. No analyzer or plugin behaviour changes; the build pipeline now starts from a clean Gradle state in CI and no longer carries stale build caches into the GitHub snapshot consumed by the publish job.
## [3.2.7] - 2026-03-04

### Added

- Initial release of the Ansible Analyzer plugin for IntelliJ IDEA, Rider, and other JetBrains IDEs.
- **70+ analysis rules** covering syntax, style, security, best practices, and complexity.
- **Default quality profile** with curated rules active out of the box.
- Real-time diagnostics as you edit Ansible playbook and task files.
- Per-rule settings panel with enable/disable, severity override, and search filter under Settings > Tools.
- **Import from SonarQube** — fetch active rules from a SonarQube quality profile via Tools > Qualimetry Ansible > Import Rules from SonarQube.
- Per-rule inspection options for Qodana profile configuration.
- Compatible with JetBrains Qodana for headless CI/CD analysis.
- Same analysis engine as the Qualimetry Ansible Analyzer for VS Code and SonarQube.

## [3.2.6] - 2026-03-03

### Added

- Initial release of the Ansible Analyzer plugin for IntelliJ IDEA, Rider, and other JetBrains IDEs.
- **70+ analysis rules** covering syntax, style, security, best practices, and complexity.
- **Default quality profile** with curated rules active out of the box.
- Real-time diagnostics as you edit Ansible playbook and task files.
- Per-rule settings panel with enable/disable, severity override, and search filter under Settings > Tools.
- **Import from SonarQube** — fetch active rules from a SonarQube quality profile via Tools > Qualimetry Ansible > Import Rules from SonarQube.
- Per-rule inspection options for Qodana profile configuration.
- Compatible with JetBrains Qodana for headless CI/CD analysis.
- Same analysis engine as the Qualimetry Ansible Analyzer for VS Code and SonarQube.
