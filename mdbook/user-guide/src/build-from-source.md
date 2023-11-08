# Building from source

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

## Dependencies

dt builds with Zig 0.11.x and 0.12.x (pre-release)

## Recommendations

If you are only ever going to develop with a single version of Zig, I recommend
simply installing it from upstream.

If you already develop with multiple versions of Zig, you probably already have
figured out how to manage versions. If not, I personally recommend either rtx or aqua.

If you're going to be installing a lot of Zig-built executables, check out crozbi.


# Build instructions

## 1. Build with Zig from upstream downloads

Zig can be obtained from: https://ziglang.org/download/

After installing Zig, you can build with:

```
git clone https://github.com/so-dang-cool/dt.git \
  && cd ./dt \
  && zig build
```

## 2. Build with Zig from rtx

The dt source tree contains an up-to-date `.tool-versions` file for rtx.

```
git clone https://github.com/so-dang-cool/dt.git \
  && cd ./dt \
  && rtx i \
  && zig build
```

## 3. Build with Zig from asdf

1. [Install asdf](https://asdf-vm.com/guide/getting-started.html)

```
git clone https://github.com/so-dang-cool/dt.git \
  && cd ./dt \
  && asdf install \
  && zig build
```

## 4. Build with Zig from aqua

1. [Install aqua](https://aquaproj.github.io/docs/install)

```
git clone https://github.com/so-dang-cool/dt.git \
  && cd ./dt \
  && aqua i \
  && zig build
```

## 5. Build as a Nix flake

1. [Install Nix][nix-install] or [upgrade Nix][nix-upgrade] to the latest release
2. [Enable Flakes][nix-flakes]

```
git clone https://github.com/so-dang-cool/dt.git \
  && cd ./dt \
  && nix build
```

[nix-install]: https://nixos.org/manual/nix/unstable/installation/installation
[nix-upgrade]: https://nixos.org/manual/nix/unstable/installation/upgrading
[nix-flakes]: https://nixos.wiki/wiki/Flakes


## 6. Build and install with crozbi

1. [Install crozbi](https://github.com/so-dang-cool/crozbi)

```
crozbi so-dang-cool/dt
```


# Cross-compiling

The project's `build.zig` is configured to compile for all dt's
known-supported platforms.

With the project cloned, Zig installed, and the source root as
your current working directory, run:

```
zig build cross
```

The targets to cross-compile can be edited in the project's `build.zig`.
