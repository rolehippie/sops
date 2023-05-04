# sops

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/sops)
[![General Workflow](https://github.com/rolehippie/sops/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/sops/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/sops/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/sops/actions/workflows/readme.yml)
[![Galaxy Workflow](https://github.com/rolehippie/sops/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/sops/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/sops)](https://github.com/rolehippie/sops/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.sops-blue)](https://galaxy.ansible.com/rolehippie/sops)

Ansible role to install sops secret encryption cli.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [sops_arch](#sops_arch)
  - [sops_download](#sops_download)
  - [sops_path](#sops_path)
  - [sops_version](#sops_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### sops_arch

Architecture for sops binary

#### Default value

```YAML
sops_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

### sops_download

URL to download sops binary from

#### Default value

```YAML
sops_download: https://github.com/mozilla/sops/releases/download/v{{ sops_version
  }}/sops-v{{ sops_version }}.linux.{{ sops_arch }}
```

### sops_path

Path to install the binaries

#### Default value

```YAML
sops_path: /usr/bin
```

### sops_version

Version of sops binary to install

#### Default value

```YAML
sops_version: 3.7.3
```

## Discovered Tags

**_sops_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
