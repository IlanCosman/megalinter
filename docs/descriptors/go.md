<!-- markdownlint-disable MD003 MD020 MD033 MD041 -->
<!-- @generated by .automation/build.py, please do not update manually -->
<!-- Instead, update descriptor file at https://github.com/megalinter/megalinter/tree/main/megalinter/descriptors/go.yml -->
# GO

## Linters

| Linter                               | Configuration key         |
|--------------------------------------|---------------------------|
| [golangci-lint](go_golangci_lint.md) | [GO](go_golangci_lint.md) |
| [revive](go_revive.md)               | [GO](go_revive.md)        |

## Linted files

- File extensions:
  - `.go`

## Configuration in MegaLinter

| Variable                | Description                   | Default value |
|-------------------------|-------------------------------|---------------|
| GO_FILTER_REGEX_INCLUDE | Custom regex including filter |               |
| GO_FILTER_REGEX_EXCLUDE | Custom regex excluding filter |               |


## Behind the scenes

### Installation

- APK packages (Linux):
  - [go](https://pkgs.alpinelinux.org/packages?branch=edge&name=go)
