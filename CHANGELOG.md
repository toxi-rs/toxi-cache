# Changelog — `toxi-cache`

Per-crate history extracted from the monolith changelog
([meshackbahati/toxi](https://github.com/meshackbahati/toxi/blob/main/CHANGELOG.md)),
which remains the full documentation hub.

## Unreleased

- **toxi-cache** (`3.1.2`): Redis backend shares one lazily established
  multiplexed connection instead of handshaking per operation.

## 3.1.5

- **toxi-cache** (`3.1.1`): `MemoryCache` replaces the per-operation
  full-scan expiry sweep under a write lock with lazy single-entry
  eviction and an amortized sweep every 1024 operations.
