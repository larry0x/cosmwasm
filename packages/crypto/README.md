# CosmWasm Crypto

[![cosmwasm-crypto on crates.io](https://img.shields.io/crates/v/cosmwasm-crypto.svg)](https://crates.io/crates/cosmwasm-crypto)

This crate implements cryptography-related functions, so that they can be
available for both, the [cosmwasm-vm](`https://crates.io/crates/cosmwasm-vm`)
and [cosmwasm-std](`https://crates.io/crates/cosmwasm-std`) crates.

## Implementations

- `secp256k1_verify()`: Digital signature verification using the ECDSA secp256k1
  scheme, for Cosmos signature / public key formats.
- `secp256r1_verify()`: Digital signature verification using the ECDSA secp256r1
  scheme, for Cosmos signature / public key formats.
- `ed25519_verify()`: Digital signature verification using the EdDSA ed25519
  scheme, for Tendermint signature / public key formats.
- `ed25519_batch_verify()`: Batch digital signature verification using the EdDSA
  ed25519 scheme, for Tendermint signature / public key formats.

## Benchmarking

```
cd packages/crypto
cargo bench --features std
```

## License

This package is part of the cosmwasm repository, licensed under the Apache
License 2.0 (see [NOTICE](https://github.com/CosmWasm/cosmwasm/blob/main/NOTICE)
and [LICENSE](https://github.com/CosmWasm/cosmwasm/blob/main/LICENSE)).
