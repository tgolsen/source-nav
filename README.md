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
$ npm install -g source-nav
$ source-nav COMMAND
running command...
$ source-nav (--version)
source-nav/0.0.0 darwin-x64 node-v14.16.1
$ source-nav --help [COMMAND]
USAGE
  $ source-nav COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`source-nav help [COMMAND]`](#source-nav-help-command)
* [`source-nav plugins`](#source-nav-plugins)
* [`source-nav plugins:inspect PLUGIN...`](#source-nav-pluginsinspect-plugin)
* [`source-nav plugins:install PLUGIN...`](#source-nav-pluginsinstall-plugin)
* [`source-nav plugins:link PLUGIN`](#source-nav-pluginslink-plugin)
* [`source-nav plugins:uninstall PLUGIN...`](#source-nav-pluginsuninstall-plugin)
* [`source-nav plugins update`](#source-nav-plugins-update)

## `source-nav help [COMMAND]`

Display help for source-nav.

```
USAGE
  $ source-nav help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for source-nav.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `source-nav plugins`

List installed plugins.

```
USAGE
  $ source-nav plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ source-nav plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `source-nav plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ source-nav plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ source-nav plugins:inspect myplugin
```

## `source-nav plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ source-nav plugins:install PLUGIN...

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
  $ source-nav plugins add

EXAMPLES
  $ source-nav plugins:install myplugin 

  $ source-nav plugins:install https://github.com/someuser/someplugin

  $ source-nav plugins:install someuser/someplugin
```

## `source-nav plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ source-nav plugins:link PLUGIN

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
  $ source-nav plugins:link myplugin
```

## `source-nav plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ source-nav plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ source-nav plugins unlink
  $ source-nav plugins remove
```

## `source-nav plugins update`

Update installed plugins.

```
USAGE
  $ source-nav plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
