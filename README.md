The Rust Programming Language 2018 Book
=======================================

These are my notes and experiments related to The Rust Programming Language
book, 2018 edition, published by No Starch Press and authored by Steve Klabnik
and Carol Nichols.

## Installation

The recommended way to install Rust packages is to use rustup, but I'm not fond
of `curl | sh` style installations as nothing verifies the downloaded script.
Since I use Debian, an easy way to install all the normal developer tools is to
`apt install rust-all`.

### Crates

To limit crates specifically to those available via the Debian apt repos, add
this snippet to your project's `.cargo/config` file:

```
[source]
[source.debian-packages]
directory = "/usr/share/cargo/registry"
[source.crates-io]
replace-with = "debian-packages"
```

Then install the needed crates via `apt install librust-CRATE-dev` (replacing
"CRATE" with the crate you need's name).

To see which crates are available in your Debian distribution, search with apt
`apt search librust-.*-dev`.  Many are available.

### Documentation

Install the rust documentation which matches the version of Rust which comes
with your Debian distribution with `apt install rust-doc`.  All the
documentation will be located at `/usr/share/doc/rust-doc/html/` in an easy to
browse format:
[file:///usr/share/doc/rust-doc/html/index.html](file:///usr/share/doc/rust-doc/html/index.html)

Documentation is also available online, but finding the exact version which
matches your local install is a bit trickier:
[https://www.rust-lang.org/learn](https://www.rust-lang.org/learn)
