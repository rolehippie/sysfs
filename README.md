# sysfs

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/sysfs) [![Build Status](https://img.shields.io/drone/build/rolehippie/sysfs/master?logo=drone)](https://cloud.drone.io/rolehippie/sysfs) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/sysfs)](https://github.com/rolehippie/sysfs/blob/master/LICENSE) 

Ansible role to configure sysfs settings. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [sysfs_defaults](#sysfs_defaults)
  * [sysfs_extra](#sysfs_extra)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

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

## Dependencies

* None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
