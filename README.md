## php-56-cli 

[![Build Status](https://travis-ci.org/Oefenweb/ansible-php-56-cli.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-php-56-cli) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-php--56--cli-blue.svg)](https://galaxy.ansible.com/list#/roles/4437)

Set up PHP 5.6 Cli in Ubuntu systems.

#### Requirements

None

#### Variables

##### php

* `php_56_cli_install`: [default: `[]`]: (Additional) Packages to install

###### general

* `php_56_cli_expose`: [default: `false`]: Whether PHP may expose the fact that it is installed on the server
* `php_56_cli_max_input_vars`: [default: `1000`]: How many GET/POST/COOKIE input variables may be accepted
* `php_56_cli_precision`: [default: `14`]: The number of significant digits displayed in floating point numbers
* `php_56_cli_realpath_cache_size`: [default: `16k`]: Determines the size of the `realpath` cache to be used by PHP
* `php_56_cli_realpath_cache_ttl`: [default: `120`]: Duration of time, in seconds for which to cache `realpath` information for a given file or directory
* `php_56_cli_serialize_precision`: [default: `17`]: When floats & doubles are serialized store serialize_precision significant digits after the floating point
* `php_56_cli_max_execution_time`: [default: `30`]: Maximum execution time of each script, in seconds
* `php_56_cli_memory_limit`: [default: `128M`]: Maximum amount of memory a script may consume
* `php_56_cli_error_reporting`: [default: `E_ALL & ~E_DEPRECATED & ~E_STRICT`]: This directive informs PHP of which errors, warnings and notices you would like it to take action for
* `php_56_cli_post_max_size`: [default: `8M`]: Maximum size of `POST` data that PHP will accept
* `php_56_cli_upload_max_filesize`: [default: `2M`]: Maximum allowed size for uploaded files
* `php_56_cli_save_handler`: [default: `files`]: Handler used to store/retrieve data
* `php_56_cli_session_save_path`: [default: `/var/lib/php5/sessions`]: Argument passed to `save_handler`. In the case of files, this is the path where data files are stored

###### mods

* `php_56_cli_mods_present`: [default: `{opcache: {}, json: {}, mysql: {}, memcache: {}, memcached: {}, mcrypt: {}, gd: {}, curl: {}}`]: Modules to enable
* `php_56_cli_mods_present.key`: [required]: The identifier of the module (e.g. `curl`)
* `php_56_cli_mods_present.key.dependencies`: [optional: default: `[]`]: Packages needed by the module (e.g. `php5-curl`)

* `php_56_cli_mods_absent`: [default: `{}`]: Modules to disable
* `php_56_cli_mods_absent.key`: [required]: The identifier of the module (e.g. `curl`)

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - php-56-cli
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-php-56-cli/issues)!
