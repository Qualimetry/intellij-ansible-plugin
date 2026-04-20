# Qualimetry Ansible Analyzer - IntelliJ Plugin

Static analysis of Ansible playbook and task files (`.yml`, `.yaml`) in IntelliJ IDEA, Rider, and other JetBrains IDEs, including headless analysis in JetBrains Qodana for CI/CD pipelines.

Powered by the same analysis engine as the [Qualimetry Ansible Analyzer for VS Code](https://github.com/Qualimetry/vscode-ansible-plugin) and the [Qualimetry Ansible Analyzer for SonarQube](https://github.com/Qualimetry/sonarqube-ansible-plugin).

## Features

- **75 rules** covering YAML syntax, naming, safety, and best practices.
- **Real-time diagnostics** as you edit Ansible files.
- **Configurable** — enable/disable individual rules and override severities via a per-rule settings panel.
- **SonarQube import** — import active rules from a SonarQube quality profile via Tools > Qualimetry Ansible > Import Rules from SonarQube.
- **Qodana support** — runs automatically in JetBrains Qodana for quality gates in CI/CD.

## Rule categories

| Category | Examples |
|----------|----------|
| YAML & Syntax | Valid YAML, schema compliance, key ordering, consistent indentation |
| Naming | Task names, variable names, role names, handler names |
| Security | No-log secrets, vault usage, HTTPS required, file permissions |
| Best Practices | Handler usage, tags required, FQCN, deprecated modules |
| Style | Line length, indentation, trailing whitespace, final newline |
| Complexity | Task count limits, play count, block size |
| Galaxy & Roles | Role structure, meta validation, galaxy metadata |

## Installation

### From JetBrains Marketplace

1. Open **Settings > Plugins > Marketplace**.
2. Search for **Qualimetry Ansible Analyzer**.
3. Click **Install** and restart.

### From source

```bash
cd <monorepo-root>
mvn clean install -pl ansible-analyzer

cd intellij-plugin
./gradlew buildPlugin
```

The plugin ZIP is produced in `build/distributions/`.

## Configuration

After installation, configure the analyzer under **Settings > Tools > Qualimetry Ansible Analyzer**:

- **Enable/disable** the analyzer globally.
- **Per-rule table** — enable/disable individual rules, set severity overrides, filter by name or key.
- **Reset to Defaults** — clear all overrides and return to the default profile.
- Per-rule overrides are stored in `qualimetry-ansible.xml`.

### Import from SonarQube

Use **Tools > Qualimetry Ansible > Import Rules from SonarQube** to fetch active rules from a SonarQube quality profile. Enter your server URL, an optional authentication token, and an optional profile name. The imported rules replace the current configuration. The server URL and profile name are remembered between sessions.

## Also available

The same analysis engine powers plugins for other platforms:

- **[VS Code extension](https://github.com/Qualimetry/vscode-ansible-plugin)** — catch issues as you type in VS Code.
- **[SonarQube plugin](https://github.com/Qualimetry/sonarqube-ansible-plugin)** — enforce quality gates in CI/CD pipelines.

Rule keys and severities align across all three tools so findings are directly comparable.

## Requirements

- IntelliJ IDEA 2024.3 or later (any JetBrains IDE based on the IntelliJ Platform).
- JDK 17+ runtime.

## License

Apache License 2.0. See [LICENSE](LICENSE) for details.
