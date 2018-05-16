## `bootstrap.sh`

This is a modified upstream script used to generate aarch64 cross-build tools.

We need to do this because Alpine Linux does not provide cross-build tools in
its repository. When cross-compiling, we can use Alpine Linux aarch64
repository to generate aarch64 sysroot. Therefore we do not bootstrap a
complete sysroot environment.

First checkout Alpine Linux `aports` repository, `3.7-stable` branch.

Then you can run the script as follows.

``
$ cd /home/builder/src/aports-sdk/scripts

$ APORTS=/home/builder/src/upstream-alpine/aports ./bootstrap.sh aarch64 2>&1 | tee log
``
