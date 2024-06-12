# htmlproc

[![crates.io](https://img.shields.io/crates/v/htmlproc?label=latest)](https://crates.io/crates/htmlproc)
[![Documentation](https://docs.rs/htmlproc/badge.svg?version=latest)](https://docs.rs/htmlproc/latest)
[![Dependency Status](https://deps.rs/crate/htmlproc/latest/status.svg)](https://deps.rs/crate/htmlproc/latest)
[![License](https://img.shields.io/github/license/nabbisen/htmlproc-rs)](https://github.com/nabbisen/htmlproc-rs/blob/main/LICENSE)

HTML processors as utils written in Rust.
Each function is offered as a single `feature`, so the dependencies are kept small.

## Install in Rust project

```sh
# intall crate
cargo add htmlproc

# intall crate with specific features
cargo add htmlproc --features omit_enclosures

# uninstall
# cargo remove htmlproc
```

## Functions (Features)

### omit_enclosures

Remove specific tag enclosures from HTML text.

#### Usage

```rust
use htmlproc::omit_enclosures::manipulate;

let result: String = manipulate("<div>...<span>---</span>...</div>", &["span"]);
```
