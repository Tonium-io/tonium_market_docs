---
title: Marketplace
---

Market
========

This page about how contract market work.

## Contracts

Exist some kind of types contracts to exchange

* Exchanger
* Controller
* TrueNFT
* Pair
    * NftAuction
    * NftPair

```mermaid
sequenceDiagram;
    Controller0 ->> TrueNFT: Mint token with metadata
    Controller0 ->> Exchanger: Please, create a pair for me
    Exchanger ->> Pair: Create a pair for user
    Controller0 ->> TrueNFT: Please, send a token to pair
    TrueNFT ->> Exchanger: Send a token
    Controller0 ->> Pair: Let's start a selling
    Pair ->> Exchanger: We have a new pair. Please, index me
    Controller1 ->> Exchanger: What's pair do you have?
    Exchanger ->> Controller1: [list of pairs]
    Controller1 ->> Pair: I want to buy your tokens
    Pair ->> Controller1: Sure, here your tokens
    Pair ->> Exchanger: We finished, here is your commission
    Pair ->> Controller0: We sold your tokens. Here is your money
    Pair ->> Pair: selfdestruct
```
This diagram show how they work with each other to sell token

## How to read it
### What is a variables?
Its getter methods without any param in input and with one output.
### What is a getter?
Its getter methods with params and some output or without parms and some outputs.