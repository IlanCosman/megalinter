<!-- markdownlint-disable MD003 MD020 MD033 MD041 -->
<!-- @generated by .automation/build.py, please do not update manually -->
<!-- Instead, update descriptor file at https://github.com/megalinter/megalinter/tree/main/megalinter/descriptors/powershell.yml -->
# POWERSHELL

## Linters

| Linter                                 | Configuration key                      |
|----------------------------------------|----------------------------------------|
| [powershell](powershell_powershell.md) | [POWERSHELL](powershell_powershell.md) |

## Linted files

- File extensions:
  - `.ps1`
  - `.psm1`
  - `.psd1`
  - `.ps1xml`
  - `.pssc`
  - `.psrc`
  - `.cdxml`

## Configuration in MegaLinter

| Variable                        | Description                   | Default value |
|---------------------------------|-------------------------------|---------------|
| POWERSHELL_FILTER_REGEX_INCLUDE | Custom regex including filter |               |
| POWERSHELL_FILTER_REGEX_EXCLUDE | Custom regex excluding filter |               |


## Behind the scenes

### Installation

- Dockerfile commands :
```dockerfile
ARG PWSH_VERSION='latest'
ARG PWSH_DIRECTORY='/opt/microsoft/powershell'
RUN mkdir -p ${PWSH_DIRECTORY} \
    && curl --retry 5 --retry-delay 5 -s https://api.github.com/repos/powershell/powershell/releases/${PWSH_VERSION} \
        | grep browser_download_url \
        | grep linux-alpine-x64 \
        | cut -d '"' -f 4 \
        | xargs -n 1 wget -O - \
        | tar -xzC ${PWSH_DIRECTORY} \
    && ln -sf ${PWSH_DIRECTORY}/pwsh /usr/bin/pwsh

```

