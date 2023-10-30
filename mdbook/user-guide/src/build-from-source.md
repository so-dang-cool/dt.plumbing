# Building from source

A prerequisite for all options is installing Zig.

[Install Zig 0.11.+](https://ziglang.org/download/)

## Getting updates

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


## Build from source (Vanilla)


Clone and build:

```
git clone https://github.com/so-dang-cool/dt.git
cd ./dt
zig build -Doptimize=ReleaseSmall
```

The resulting binary will be available in `./zig-out/bin/dt`.


## Build from source (Nix)

Prerequisites

1. [Install][install-nix] or [upgrade to][upgrade-nix] the latest Nix release

```
git clone https://github.com/so-dang-cool/dt.git
cd ./dt
nix build
```

[install-nix]: https://nixos.org/manual/nix/unstable/installation/installation
[upgrade-nix]: https://nixos.org/manual/nix/unstable/installation/upgrading


## Build from source (crozbi)

Prerequisites

1. Install the [crozbi](https://github.com/so-dang-cool/crozbi) Zig installer.

```
crozbi so-dang-cool/dt
```


## Cross-compiling

The project's `build.zig` is pre-configured to compile for all
known-supported platforms.

With the project cloned:

```
zig build cross
```

The targets to cross-compile can be edited in the project's `build.zig`.
