poet
=================

A new CLI generated with oclif


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/poet.svg)](https://npmjs.org/package/poet)
[![Downloads/week](https://img.shields.io/npm/dw/poet.svg)](https://npmjs.org/package/poet)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g poet
$ poet COMMAND
running command...
$ poet (--version)
poet/0.0.0 darwin-arm64 node-v22.10.0
$ poet --help [COMMAND]
USAGE
  $ poet COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`poet hello PERSON`](#poet-hello-person)
* [`poet hello world`](#poet-hello-world)
* [`poet help [COMMAND]`](#poet-help-command)
* [`poet plugins`](#poet-plugins)
* [`poet plugins add PLUGIN`](#poet-plugins-add-plugin)
* [`poet plugins:inspect PLUGIN...`](#poet-pluginsinspect-plugin)
* [`poet plugins install PLUGIN`](#poet-plugins-install-plugin)
* [`poet plugins link PATH`](#poet-plugins-link-path)
* [`poet plugins remove [PLUGIN]`](#poet-plugins-remove-plugin)
* [`poet plugins reset`](#poet-plugins-reset)
* [`poet plugins uninstall [PLUGIN]`](#poet-plugins-uninstall-plugin)
* [`poet plugins unlink [PLUGIN]`](#poet-plugins-unlink-plugin)
* [`poet plugins update`](#poet-plugins-update)

## `poet hello PERSON`

Say hello

```
USAGE
  $ poet hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ poet hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/poet/poet/blob/v0.0.0/src/commands/hello/index.ts)_

## `poet hello world`

Say hello world

```
USAGE
  $ poet hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ poet hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/poet/poet/blob/v0.0.0/src/commands/hello/world.ts)_

## `poet help [COMMAND]`

Display help for poet.

```
USAGE
  $ poet help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for poet.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.28/src/commands/help.ts)_

## `poet plugins`

List installed plugins.

```
USAGE
  $ poet plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ poet plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.37/src/commands/plugins/index.ts)_

## `poet plugins add PLUGIN`

Installs a plugin into poet.

```
USAGE
  $ poet plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into poet.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the POET_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the POET_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ poet plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ poet plugins add myplugin

  Install a plugin from a github url.

    $ poet plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ poet plugins add someuser/someplugin
```

## `poet plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ poet plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ poet plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.37/src/commands/plugins/inspect.ts)_

## `poet plugins install PLUGIN`

Installs a plugin into poet.

```
USAGE
  $ poet plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into poet.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the POET_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the POET_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ poet plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ poet plugins install myplugin

  Install a plugin from a github url.

    $ poet plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ poet plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.37/src/commands/plugins/install.ts)_

## `poet plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ poet plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ poet plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.37/src/commands/plugins/link.ts)_

## `poet plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ poet plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ poet plugins unlink
  $ poet plugins remove

EXAMPLES
  $ poet plugins remove myplugin
```

## `poet plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ poet plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.37/src/commands/plugins/reset.ts)_

## `poet plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ poet plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ poet plugins unlink
  $ poet plugins remove

EXAMPLES
  $ poet plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.37/src/commands/plugins/uninstall.ts)_

## `poet plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ poet plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ poet plugins unlink
  $ poet plugins remove

EXAMPLES
  $ poet plugins unlink myplugin
```

## `poet plugins update`

Update installed plugins.

```
USAGE
  $ poet plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.37/src/commands/plugins/update.ts)_
<!-- commandsstop -->
