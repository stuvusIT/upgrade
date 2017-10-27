# upgrade

Simple Ansible role to upgrade hosts, based on [debian_upgrade.yml](https://gist.github.com/maethor/380676f6b1cec8cc7439) by Guillaume Subiron (maethor)

## Role Variables

| Option                            | Type    | Default | Description                                                                      | Required |
|:----------------------------------|:--------|:--------|:---------------------------------------------------------------------------------|:--------:|
| `upgrade_restart_services`        | boolean | `true`  | Automatically restart services, when needed(for ex. linked libaries are updated) |    N     |
| `upgrade_restart_services_ignore` | list    | `[]`    | List of services that shall not be restarted. `dbus` is always appended.         |    N     |

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).


## Author Information

- [Markus Mroch (Mr. Pi)](https://github.com/Mr-Pi) _markus.mroch@stuvus.uni-stuttgart.de_
