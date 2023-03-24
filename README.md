# libffi for RACE

This repo provides scripts to custom-build the
[libffi library](https://github.com/libffi/libffi) for RACE.

## License

The libffi library is licensed under the MIT license.

Additionally the build scripts in this repo are licensed under Apache 2.0.

## Dependencies

libffi has no dependencies on any custom-built libraries.

## How To Build

The [ext-builder](https://github.com/tst-race/ext-builder) image is used to
build libffi.

```
git clone https://github.com/tst-race/ext-builder.git
git clone https://github.com/tst-race/ext-libffi.git
./ext-builder/build.py \
    --target linux-x86_64 \
    ./ext-libffi
```

## Platforms

libffi is built for the following platforms:

* `android-x86_64`
* `android-arm64-v8a`

It is also used on Linux but can be installed via `apt`.

## How It Is Used

libffi is a dependency for the custom-built Android Python packages.
