# upgrade
Simple Ansible role to upgrade hosts, based on [debian_upgrade.yml](https://gist.github.com/maethor/380676f6b1cec8cc7439) by Guillaume Subiron (maethor).
`apt`, `gem` and `npm` packages will be upgraded, if the respective package manager is installed.

## Role Variables
| Option                            | Type    | Default | Description                                                                                         | Required |
|:----------------------------------|:--------|:--------|:----------------------------------------------------------------------------------------------------|:--------:|
| `upgrade_restart_services`        | boolean | `True`  | Automatically restart services, when needed (e.g. linked libaries are updated)                      |     N    |
| `upgrade_restart_services_ignore` | list    | `[]`    | List of services that shall not be restarted. `dbus` is always appended.                            |     N    |
| `upgrade_do_autoremove`           | boolean | `True`  | Automatically remove no longer needed packages (e.g. old kernels)                                   |     N    |
| `upgrade_do_autoclean`            | boolean | `True`  | If enabled, cleans the local repository of retrieved package files that can no longer be downloaded |     N    |
| `upgrade_gem`                     | boolean | `True`  | Skip gem upgrade routines when disabled                                                             |     N    |
| `upgrade_npm`                     | boolean | `True`  | Skip npm (node) upgrade routines when disabled                                                      |     N    |

You cannot list systemd in the list of ignored services, the `systemctl daemon-reexec` will always be executed when a library dependency of systemd changes.

## License
This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).


## Author Information
- [Markus Mroch (Mr. Pi)](https://github.com/Mr-Pi) _markus.mroch@stuvus.uni-stuttgart.de_
