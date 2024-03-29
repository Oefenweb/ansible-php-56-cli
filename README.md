## php-56-cli, DEPRECATED ([see](https://github.com/Oefenweb/ansible-php-cli-ondrej))

[![CI](https://github.com/Oefenweb/ansible-php-56-cli/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-php-56-cli/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-php--56--cli-blue.svg)](https://galaxy.ansible.com/Oefenweb/php_56_cli)

Set up PHP 5.6 Cli in Ubuntu systems.

#### Requirements

None

#### Variables

* `php_56_cli_install`: [default: `[]`]: (Additional) Packages to install

* `php_56_cli_update_alternatives`: [default: `true`]: Whether or not to run `update-alternatives`

* `php_56_cli_precision`: [default: `14`]: The number of significant digits displayed in floating point numbers
* `php_56_cli_serialize_precision`: [default: `17`]: When floats & doubles are serialized store serialize_precision significant digits after the floating point
* `php_56_cli_disable_functions`: [default: `[]`]: This directive allows you to disable certain functions for security reasons
* `php_56_cli_max_execution_time`: [default: `0`]: Maximum execution time of each script, in seconds
* `php_56_cli_memory_limit`: [default: `-1`]: Maximum amount of memory a script may consume
* `php_56_cli_error_reporting`: [default: `E_ALL & ~E_DEPRECATED & ~E_STRICT`]: This directive informs PHP of which errors, warnings and notices you would like it to take action for
* `php_56_cli_openssl_cafile`: [optional]: The location of a Certificate Authority (CA) file on the local filesystem
* `php_56_cli_openssl_capath`: [optional]: The location of a Certificate Authority (CA) directory on the local filesystem

* `php_56_cli_mods_present`: [default: `{json: {}, xml: {}, readline: {}, mysql: {}, memcache: {}, memcached: {}, mstring: {}, mcrypt: {}, gd: {}, curl: {}}`]: Modules to enable
* `php_56_cli_mods_present.key`: [required]: The identifier of the module (e.g. `curl`)
* `php_56_cli_mods_present.key.dependencies`: [optional: default: `[]`]: Packages needed by the module (e.g. `php5.6-curl`)

* `php_56_cli_mods_absent`: [default: `{opcache: {}}`]: Modules to disable
* `php_56_cli_mods_absent.key`: [required]: The identifier of the module (e.g. `opcache`)

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - oefenweb.php-56-cli
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-php-56-cli/issues)!
