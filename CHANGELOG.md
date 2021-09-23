# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

### Unreleased

## [0.4.13] "eth-patched"

### Changed
- Bump digest-sha3-patched-ruby-3 version for ruby 3 support

## [0.4.12]

### Changed
- Bump rake version because of security vulnerability

## [0.4.11]

### Added
- Support for recovering signatures with a V value below 27 (like from Ledger hardware wallets)

## [0.4.10]

### Changed
- Use updated sha3 dependency
- Improved OpenSSL support

### Changed
- Changed Eth::Configuration.default_chain_id back to .chain_id for dependent libraries.

## [0.4.9]

### Changed
- [escoffon](https://github.com/escoffon) added support for chain IDs larger than 120.

## [0.4.8]

### Added
- [@buhrmi](https://github.com/buhrmi) added Eth::Key#personal_sign.
- [@buhrmi](https://github.com/buhrmi) added Eth::Key#personal_recover.

## [0.4.7]

### Changed
- Updated MoneyTree dependency.

## [0.4.6]

### Added
- Support scrypt private key decryption

## [0.4.5]

### Changed
- Further improve Open SSL configurability

## [0.4.4]

### Changed
- Support old versions of SSL to help avoid preious breaking changes

## [0.4.3]

### Added
- Eth::Key::Encrypter class to handle encrypting keys.
- Eth::Key.encrypt as a nice wrapper around Encrypter class.
- Eth::Key::Decrypter class to handle encrypting keys.
- Eth::Key.decrypt as a nice wrapper around Decrypter class.

## [0.4.2]

### Added
- Address#valid? to validate EIP55 checksums.
- Address#checksummed to generate EIP55 checksums.
- Utils.valid_address? to easily validate EIP55 checksums.
- Utils.format_address to easily convert an address to EIP55 checksummed.

### Changed
- Dependencies no longer include Ethereum::Base. Eth now implements those helpers directly and includes ffi, digest-sha3, and rlp directly.


## [0.4.1]

### Changed
- Tx#hash includes the '0x' hex prefix.

## [0.4.0]

### Added
- Tx#data_bin returns the data field of a transaction in binary.
- Tx#data_hex returns the data field of a transaction as a hexadecimal string.
- Tx#id is an alias of Tx#hash

### Changed
- Tx#data is configurable to return either hex or binary: `config.tx_data_hex = true`.
- Tx#hex includes the '0x' hex prefix.
- Key#address getter is prepended by '0x'.
- Extract public key to address method into Utils.public_key_to_address.
- Tx#from returns an address instead of a public key.
- Chain ID is updated to the later version of the spec.
