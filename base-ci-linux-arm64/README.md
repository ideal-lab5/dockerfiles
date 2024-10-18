# base-ci-linux-arm64

Docker image based on [official Debian image](https://hub.docker.com/_/debian) debian:bullseye-slim.

This is an adaptation of [Parity's `base-ci-linux` image](https://github.com/paritytech/scripts/tree/fa1ad07a88bc4c4ad2c3e0091e4e3d626fae4352/dockerfiles/base-ci-linux) for arm64.

Used as base for `Substrate`-based CI images.

Our base CI image `<base-ci-linux-arm64:latest>`.

Used to build and test Substrate-based projects.

**Dependencies and Tools:**

- `libssl-dev`
- `clang-14`
- `lld-14`
- `libclang-14-dev`
- `make`
- `cmake`
- `git`
- `pkg-config`
- `curl`
- `time`
- `jq`
- `lsof`
- `rhash`
- `ca-certificates`

[Click here](https://hub.docker.com/repository/docker/ideallabs/base-ci-linux-arm64) for the registry.

**Rust tools & toolchains:**

- stable (default)
- `sccache`

## Usage

```Dockerfile
FROM docker.io/ideallabs/base-ci-linux-arm64:latest
```
