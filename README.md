oclif-hello-world
=================

oclif example Hello World CLI

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
$ npm install -g yucsv
$ yucsv COMMAND
running command...
$ yucsv (--version)
yucsv/0.0.0 darwin-arm64 node-v14.18.3
$ yucsv --help [COMMAND]
USAGE
  $ yucsv COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`yucsv hello PERSON`](#yucsv-hello-person)
* [`yucsv hello world`](#yucsv-hello-world)
* [`yucsv help [COMMAND]`](#yucsv-help-command)
* [`yucsv plugins`](#yucsv-plugins)
* [`yucsv plugins:inspect PLUGIN...`](#yucsv-pluginsinspect-plugin)
* [`yucsv plugins:install PLUGIN...`](#yucsv-pluginsinstall-plugin)
* [`yucsv plugins:link PLUGIN`](#yucsv-pluginslink-plugin)
* [`yucsv plugins:uninstall PLUGIN...`](#yucsv-pluginsuninstall-plugin)
* [`yucsv plugins update`](#yucsv-plugins-update)

## `yucsv hello PERSON`

Say hello

```
USAGE
  $ yucsv hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/yuc0rp/yucsv/blob/v0.0.0/dist/commands/hello/index.ts)_

## `yucsv hello world`

Say hello world

```
USAGE
  $ yucsv hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `yucsv help [COMMAND]`

Display help for yucsv.

```
USAGE
  $ yucsv help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for yucsv.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `yucsv plugins`

List installed plugins.

```
USAGE
  $ yucsv plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ yucsv plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `yucsv plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ yucsv plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ yucsv plugins:inspect myplugin
```

## `yucsv plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ yucsv plugins:install PLUGIN...

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
  $ yucsv plugins add

EXAMPLES
  $ yucsv plugins:install myplugin 

  $ yucsv plugins:install https://github.com/someuser/someplugin

  $ yucsv plugins:install someuser/someplugin
```

## `yucsv plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ yucsv plugins:link PLUGIN

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
  $ yucsv plugins:link myplugin
```

## `yucsv plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ yucsv plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ yucsv plugins unlink
  $ yucsv plugins remove
```

## `yucsv plugins update`

Update installed plugins.

```
USAGE
  $ yucsv plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
