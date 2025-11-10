# sysfs

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/sysfs)
[![General Workflow](https://github.com/rolehippie/sysfs/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/sysfs/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/sysfs/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/sysfs/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/sysfs/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/sysfs/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/sysfs)](https://github.com/rolehippie/sysfs/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.sysfs-blue)](https://galaxy.ansible.com/rolehippie/sysfs)

Ansible role to configure sysfs settings.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of contents

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [sysfs_defaults](#sysfs_defaults)
  - [sysfs_extra](#sysfs_extra)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### sysfs_defaults

List of global sysfs settings

#### Default value

```YAML
sysfs_defaults: []
```

#### Example usage

```YAML
sysfs_defaults:
  - name: kernel/mm/transparent_hugepage/enabled
    value: never
  - name: kernel/mm/transparent_hugepage/defrag
    value: never
  - name: power/stat
    mode: 0660
    owner: root:power
```

### sysfs_extra

List of extra sysfs settings

#### Default value

```YAML
sysfs_extra: []
```

#### Example usage

```YAML
sysfs_extra:
  - name: kernel/mm/transparent_hugepage/enabled
    value: never
  - name: kernel/mm/transparent_hugepage/defrag
    value: never
  - name: power/stat
    mode: 0660
    owner: root:power
```

## Discovered Tags

**_sysfs_**

## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
