# pallet-template

[![Rust Check & Build](https://github.com/Akagi201/pallet-template/actions/workflows/ci.yml/badge.svg)](https://github.com/Akagi201/pallet-template/actions/workflows/ci.yml)

A template boilerplate code to start a pallet development

## Pallet 依赖库注意事项

* Substrate FRAME 支持任何可以编译为 Wasm 的 Rust 库。通常，这表示这些库需要启用 `no_std` feature.
* 只有当这个 pallet 启用 `std` feature 时，依赖库才能启用相应的 `std` feature.
* 添加库时需要添加 `default-features = false`，以确保 pallet 依赖的库不会启用 `std` feature.
* `dev-dependencies` 通常用在测试以及 benchmark 中，总是使用 `std` feature, 所以你不应该添加 `default-features = false`.

## Build && Test

```sh
# build
cargo build [--release]
# test
cargo test
```
