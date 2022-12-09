maimemo-cli
=================

The command line interface of maimemo (https://maimemo.com/).

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g maimemo-cli
$ maimemo COMMAND
running command...
$ maimemo (--version)
maimemo-cli/0.0.0 darwin-arm64 node-v16.15.1
$ maimemo --help [COMMAND]
USAGE
  $ maimemo COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`maimemo hello PERSON`](#maimemo-hello-person)
* [`maimemo hello world`](#maimemo-hello-world)
* [`maimemo help [COMMAND]`](#maimemo-help-command)
* [`maimemo plugins`](#maimemo-plugins)
* [`maimemo plugins:install PLUGIN...`](#maimemo-pluginsinstall-plugin)
* [`maimemo plugins:inspect PLUGIN...`](#maimemo-pluginsinspect-plugin)
* [`maimemo plugins:install PLUGIN...`](#maimemo-pluginsinstall-plugin-1)
* [`maimemo plugins:link PLUGIN`](#maimemo-pluginslink-plugin)
* [`maimemo plugins:uninstall PLUGIN...`](#maimemo-pluginsuninstall-plugin)
* [`maimemo plugins:uninstall PLUGIN...`](#maimemo-pluginsuninstall-plugin-1)
* [`maimemo plugins:uninstall PLUGIN...`](#maimemo-pluginsuninstall-plugin-2)
* [`maimemo plugins update`](#maimemo-plugins-update)

## `maimemo hello PERSON`

Say hello

```
USAGE
  $ maimemo hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/Oscaner/maimemo-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `maimemo hello world`

Say hello world

```
USAGE
  $ maimemo hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ maimemo hello world
  hello world! (./src/commands/hello/world.ts)
```

## `maimemo help [COMMAND]`

Display help for maimemo.

```
USAGE
  $ maimemo help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for maimemo.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.19/src/commands/help.ts)_

## `maimemo plugins`

List installed plugins.

```
USAGE
  $ maimemo plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ maimemo plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.7/src/commands/plugins/index.ts)_

## `maimemo plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ maimemo plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ maimemo plugins add

EXAMPLES
  $ maimemo plugins:install myplugin

  $ maimemo plugins:install https://github.com/someuser/someplugin

  $ maimemo plugins:install someuser/someplugin
```

## `maimemo plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ maimemo plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ maimemo plugins:inspect myplugin
```

## `maimemo plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ maimemo plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ maimemo plugins add

EXAMPLES
  $ maimemo plugins:install myplugin

  $ maimemo plugins:install https://github.com/someuser/someplugin

  $ maimemo plugins:install someuser/someplugin
```

## `maimemo plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ maimemo plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ maimemo plugins:link myplugin
```

## `maimemo plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ maimemo plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ maimemo plugins unlink
  $ maimemo plugins remove
```

## `maimemo plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ maimemo plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ maimemo plugins unlink
  $ maimemo plugins remove
```

## `maimemo plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ maimemo plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ maimemo plugins unlink
  $ maimemo plugins remove
```

## `maimemo plugins update`

Update installed plugins.

```
USAGE
  $ maimemo plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
