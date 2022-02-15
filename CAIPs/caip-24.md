---
caip: 24
title: Asset Reference for the Cosmos Asset Namespace
author: Theobold Frazier
discussions-to: https://github.com/shapeshift/CAIPs/issues/1
status: Draft
type: Standard
created: 2020-02-14
updated: 2020-02-14
requires: 19
---

## Simple Summary

This document is about the details of the Cosmos network asset namespace and reference for CAIP-19.

## Abstract

In CAIP-19 a general asset identification scheme is defined. This is the
implementation of CAIP-19 for Cosmos chain native assets and ibc assets.

## Motivation

See CAIP-19.

## Specification

### Cosmos chain Native Asset Namespace

An asset namespace called "native" that references Cosmos network blockchain native assets, allowing for unique identification on Cosmos chains with multiple native assets.

### Cosmos chain ibc asset Asset Namespace

The asset namespace is called "ibc". It reference Cosmos network blockchain inter blockchain channel assets.

#### Asset Reference Definition

The Asset Reference format for cosmos chains is the the base denom of the asset in the current chain_id.

## Rationale

The asset namespace using slip44 for Cosmos chains is insufficient for chains with multiple native assets like osmosis-1. Using the "native" namespace allows multiple native assets to have unique CAIP19s.

## Backwards Compatibility

Not applicable.

## Test Cases

This is a list of manually composed examples

```
# Native Atom Asset ont the cosmoshub-4 chain
cosmos:cosmoshub-4/slip44:118

# Native Osmosis Asset on the osmosis-1 chain
cosmos:osmosis-1/slip44:118

# Native Ion Asset on the osmosis-1 chain
cosmos:osmosis-1/native:uion

# IBC Atom asset on the osmosis-1 chain
cosmos:osmosis-1/ibc:27394FB092D2ECCD56123C74F36E4C1F926001CEADA9CA97EA622B25F41E5EB2
```

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
