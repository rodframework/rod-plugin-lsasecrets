# rod-plugin-lsasecrets

lsasecrets -- LSA secrets: survey the policy's secret store and read its values in place -- the inventory enumerated out of the registry's SECURITY subtree, the values asked back through the LSA's policy API (the system performs its own decryption), nothing landing on disk -- collect.lsasecrets's execution half packed as the artifact an implant load...

A Rod capability module (entry kind: plugin) in the
[Rod](https://github.com/rodframework/Rod) ecosystem. The manifest
(`rod-module.toml`) is the contract; the package installs from the
[rod-registry](https://github.com/rodframework/rod-registry) index:

    rod mod install lsasecrets

## Building the artifact

The execution half compiles from the Rust module crates in the Rod
platform tree; `build.sh` drops it at the path the manifest's
`[[plugin.artifacts]]` row names, then `rod mod publish` packs it.
Point `ROD_RUST_TREE` at a Rod checkout's `src/implant/rust` (or an
unpacked `rod-src.tar.gz`):

    ROD_RUST_TREE=/path/to/src/implant/rust ./build.sh

## License

Apache-2.0, as declared in the manifest.
