# libingenialink - Communications library for Ingenia servodrives


`libingenialink` is a portable, pure C implementation library for communicating
with Ingenia drives via the IngeniaLink protocol.

## What it can do

The library provides:

* Communications API for Ingenia drives using the IngeniaLink protocol
  (available on the USB/RS232/RS485 interfaces)
* Object oriented interface
* Supports single link and daisy-chain topologies
* Device listing and monitor
* Descriptive and detailed error messages

## Building libingenialink

The `libingenialink` library is built using [CMake](<https://cmake.org/>)
(version 3.0 or newer) on all platforms. It depends on `libsercomm`.

On most systems you can build the library using the following commands:

```sh
cmake -H. -Bbuild
cmake --build build
```

### Build options

The following build options are available:

- `WITH_GITINFO` (OFF): When enabled, the current Git commit hash will be
  included in version. This may be useful to trace installed development builds.
- `WITH_EXAMPLES` (OFF): When enabled, the library usage example applications
  will be built.
- `WITH_ERRDESC` (ON): When enabled, error details description can be obtained.
- `WITH_DOCS` (OFF): When enabled the API documentation can be built.

Furthermore, *standard* CMake build options can be used. You may find useful to
read this list of [useful CMake variables][cmakeuseful].

[cmakeuseful]: https://cmake.org/Wiki/CMake_Useful_Variables

## Coding standards

`libingenialink` is written in [ANSI C][ansic] (C99). Code is written following
the [Linux Kernel coding style][kernelstyle]. You can check for errors or
suggestions like this (uses `checkpatch.pl`):

```sh
cmake --build build --target style_check
```

[ansic]: http://en.wikipedia.org/wiki/ANSI_C
[kernelstyle]: https://www.kernel.org/doc/html/latest/process/coding-style.html