# sysfs

[![Build Status](https://cloud.drone.io/api/badges/rolehippie/sysfs/status.svg)](https://cloud.drone.io/rolehippie/sysfs)

Ansible role to configure sysfs

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
