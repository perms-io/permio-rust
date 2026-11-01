# Releasing

Publishing is done by `.github/workflows/release.yml` on a `v*` tag that
matches the version in `Cargo.toml`:

1. Bump `version` in `Cargo.toml` and update `CHANGELOG.md`.
2. Tag and push: `git tag v0.1.1 && git push origin v0.1.1`.

The workflow needs a crates.io API token (scope `publish-new` /
`publish-update` for `permio`) in the repository secret
`CARGO_REGISTRY_TOKEN`.
