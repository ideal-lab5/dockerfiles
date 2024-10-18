# ci-linux-arm64

Docker image based on our base CI image `<base-ci-linux-arm64:latest>`.

This is an adaptation of [Parity's `ci-linux` image](https://github.com/paritytech/scripts/tree/fa1ad07a88bc4c4ad2c3e0091e4e3d626fae4352/dockerfiles/ci-linux) for arm64.

Used to build and test Substrate-based projects.

## Dependencies and Tools

- `chromium-driver`

**Inherited from `<base-ci-linux-arm64:latest>`:**

- `libssl-dev`
- `clang`
- `lld`
- `libclang-dev`
- `make`
- `cmake`
- `git`
- `pkg-config`
- `curl`
- `time`
- `rhash`
- `ca-certificates`

**Rust versions:**

- stable (default)
- nightly

**Rust tools & toolchains:**

- `cargo-web`
- `cargo-hack`
- `cargo-nextest`
- `sccache`
- `wasm-pack`
- `wasm-bindgen`
- `cargo-deny`
- `cargo-spellcheck`: Required for the CI to do automated spell-checking.
- `cargo-hfuzz`
- `wasm32-unknown-unknown` toolchain
- `mdbook mdbook-mermaid mdbook-linkcheck mdbook-graphviz mdbook-last-changed`

[Click here](https://hub.docker.com/repository/docker/ideallabs/ci-linux-arm64) for the registry.

## Usage

```yaml
test-substrate:
    stage: test
        image: ideallabs/ci-linux-arm64:latest
        script:
            - cargo build ...
```
