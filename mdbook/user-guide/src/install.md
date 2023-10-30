# Installation


## Install from a package manager

[![Packaging status](https://repology.org/badge/vertical-allrepos/dt-script.svg)](https://repology.org/project/dt-script/versions)

Where possible, prefer to install dt from a package manager.

If you want to assist with packaging, please get in touch [on discord](https://discord.gg/yNfc8J48aM).


## Install with rtx or asdf

Install the plugin (once)

```shell
rtx plugin add https://github.com/so-dang-cool/asdf-dt.git
# or
asdf plugin add https://github.com/so-dang-cool/asdf-dt.git
```

Use dt (rtx)

```shell
rtx use dt@latest
dt --version
```

Install and use dt (asdf)

```shell
asdf install dt latest
asdf global dt latest
dt --version
```

## Install with aqua

dt is supported by [aqua](https://aquaproj.github.io).

In your `aqua.yml` simply add:

```
packages:
- name: so-dang-cool/dt@v1.3.1
```

Where the version is [the latest release](https://github.com/so-dang-cool/dt/releases).


## Download binaries

Standalone, statically-compiled binaries of dt are available for many operating
systems and computing architectures.

For now, it's recommended to place these somewhere local like `~/.local/bin/dt`
if you normally put this on your PATH.

Binaries can be downloaded from the GitHub repository's releases page:

* [https://github.com/so-dang-cool/dt/releases](https://github.com/so-dang-cool/dt/releases)

The binares are produced in the context of github CI/CD workflows, and not
produced on random laptops. They are "deployed" as attachments to releases
automatically.


### Getting updates

If you aren't installing from a package manager you won't get updates. The
project intends for installations from package managers to be the primary
method of vending dt, and no independent update tool or script is planned.

If you already have an account at GitHub, it's recommended to subscribe only to
release notifications for the GitHub project.

1. Navigate to the project at [https://github.com/so-dang-cool/dt](https://github.com/so-dang-cool/dt)
2. Find and click the "Watch" button
3. Choose "Custom" and then check only the "Releases" checkbox

It's not critical to follow every update, but the notifications can be useful
as an occasional reminder until your package manager is supported.

