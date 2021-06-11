# Plutil

**plutil** is a cross-platform, drop-in replacement for Apple's plutil. The primary purpose is to allow developers to modify plist files on other systems; however, it could also be extended to allow custom encoding / decoding of plists.

This project is derived from Facebook's, now archived, [xcbuild](https://github.com/facebookarchive/xcbuild). Currently, the source is pretty raw and still carries many of the abstractions introduced for xcbuild. However, as time goes on, we expect to simplify the source to remove any, now-unnecessary, abstractions.

### Requirements

#### All platforms

- [CMake](http://www.cmake.org) and [Ninja](https://ninja-build.org/) (or [llbuild](https://github.com/apple/swift-llbuild)) are required to build xcbuild.

On macOS you can install those tools with [Homebrew](https://brew.sh/): `brew install cmake ninja`.

On Windows you can install those tools with [Chocolatey](https://chocolatey.org): `choco install cmake ninja`.

#### Linux

###### Ubuntu 18.04

`sudo apt install libpng-dev libpng16-16 libxml2-dev pkg-config ninja-build`

###### All others

- GCC 4.8 or later. `libpng16-dev`, `zlib1g-dev`, `libxml2-dev`, and `pkg-config` are also required.

#### FreeBSD

###### FreeBSD 12.1

`pkg install png-1.6.37 libxml2-2.9.9 pkgconf-1.6.3,1 ninja-1.9.0,2 gmake-4.2.1_3`

#### OpenBSD

###### OpenBSD 6.6

`pkg_add png-1.6.37 libxml-2.9.9 pkgconf-1.6.3 ninja-1.9.0 gmake-4.2.1p4`

#### macOS

- Xcode 7 or later.

#### Windows

- Visual Studio 2015 or later, on Windows. A `zlib` DLL is also required.

### Instructions

#### All platforms

```sh
git clone --depth=1 https://github.com/screenplaydev/plutil
git submodule update --init
```

#### Linux and macOS:

```sh
make install
```

or

```sh
DESTDIR=/tmp/test make install
```

## Licenses

Third-party licenses are listed in the `LICENSE` document.
