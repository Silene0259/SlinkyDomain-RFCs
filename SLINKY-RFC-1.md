# SLINKY-RFC-1

Slinky defines a method of assigning domain names to public-key cryptography in a decentralized, minimilastic matter using a **block lattice**. This system is useful when accessing certain information or creating dynamic rules for domain names.

## Basic Format

`Schnorr Signature (Digital Signature) ==> Slinky Domain Spaces (SDS) ==> YAML List of Rules`

## Accessing Content

The format is as follows:

`slinky::/<sds-id>/<content>/` where `sds-id` is in base32 and of length 8 bytes and where `content` can be .

Slinky Domains use **proof-of-work** to generate the schnorr signature for a new Slinky Domain Space (SDS).

## Block Lattice

A Block Lattice is defined as a blockchain-like object where each account has its own blockchain starting with the **Genesis Chain**. As a subset of the genesis chain, exists `SlinkyGenesisSubset`, a standardized method of including data.

The block lattice is defined as in **pivot-context**. In other words, you can select any base pivot to get a new address space.

### Lattice-Interactions

Lattice-Interactions are transactions sent via specially marked data points. These are public addresses that can be designed for various purposes.

### Outline of Pivot (for future extensions)

TODO: For now, use a plain-pivot.

A Pivot Contains the following

1. The `PivotPointAddress` (PPA) which is a schnorr signature encoded in base32. This is included in the `pivot-block`
2. The `PivotPointGenesisRules` (PPG) which is code used to define rules for SlinkyDomainSpaces

## Schnorr Signature

Schnorr Signatures are used throughout slinky.

`Encoding:` BASE32 (CROCKFORD)

`Public Key Length:` 52 characters

`Secret Key Length:` 103 characters
