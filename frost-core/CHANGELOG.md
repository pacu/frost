# Changelog

Entries are listed in reverse chronological order.

## Unreleased

## 0.6.0

## Released

## 0.5.0

* expose SigningShare, VerifyingShare, NonceCommitment and SignatureResponse in ciphersuite libraries
* most structs now have a private field which mean that they can no longer be
  instantiated directly. `new()` methods have been added to them.
* change `SigningPackage::new()` to take `&[u8]P  instead of `Vec<u8>`
* add `serde` support under `serde` feature to allow encoding structs which
  need to be communicated between participants.
* expand docs to show the overall structure and contents

## 0.4.0

* add serialize and deserialize functions for VerifiableSecretSharingCommitment
* add value, serialize and deserialize functions for CoefficientCommitment

## 0.3.0

* add multiscalar support to speed up signing and aggregating
* change errors caused by protocol violations to contain the misbehaving party
* add frost::keys::split()
* rename reconstruct_secret() to reconstruct(), make it takes a slice instead
  of a Vector, make it return SigningKey, fix it to return Error instead of an
  error string
* rename keygen_with_dealer() to generate_with_dealer()
* change SigningKey::new() to take a reference instead of a value

## 0.2.0

* Implement Zeroize where needed or skip where not needed (fixes compiling error) (#301)
* Change keygen_with_dealer() to return a HashMap (#288)
* Re-export the frost-core traits and rand-core as part of top-level impls API (#297)

## 0.1.0

* Initial release.
