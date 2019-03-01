---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript
  - java
  - swift

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

search: true
---

# Getting started with Franklin

## What is Franklin Network?

Franklin Network is a rollup sidechain on Ethereum, secured by Zero Knowledge Proofs. Currenty, it is only deployed on Rinkeby testnet. You will find a detailed technical description of rollup sidechain technology [here](https://medium.com/matter-labs/introducing-matter-testnet-502fab5a6f17).

## What is a sidechain?

## What does it mean for practical applications?

# Working with Franklin.js

Franklin.js is an easy-to-use, stateless js library for building applications on Franklin Network.

To get started with Franklin.js:

## 1. Install npm dependency

<pre class="center-column">
npm install --save franklin 
</pre>

## 2. Add it to your code

<pre class="center-column">
// any provider that follows the web3 provider specification:
const HttpProvider = require('ethjs-provider-http');
const Franklin = require('franklinjs');
const franklin = new Franklin(new HttpProvider('https://ropsten.infura.io'));
</pre>

# Deposits

```javascript
let from = accounts[0];
let amount = new BN(100);
let tx = franklin.deposit(from, amount);
```

```java
TBD
```

```swift
TBD
```

# Checking balance

```javascript
let accountId = franklin.addressToAccountId(accounts[0]);
let account = franklin.deposit(from, amount);
```

```java
TBD
```

```swift
TBD
```

> This will return account information of the following form:

```json
{
    verified: { eth_block_height, balance, nonce, pub_key, [merkle_proof] },
    committed: { eth_block_height, balance, nonce, pub_key, [merkle_proof], [unverified_snark_proofs] },
    pending: { balance, nonce, [list_of_pending_transactions_with_confirmations] }
}
```

# Transfers

# Withdrawals

# API reference

## Key management

### newKey(seed)

### sign

### verify

## Mainchain functions

- addressToAccountId
- createDepositTx
- createFullWithdrawTx

## Sidechain functions

- createTransferTx
- createPartialWithdrawTx
- signTx
- submitTx
- getAccount
- getNetworkStatus

## Instant confirmation claims

# Raw REST API

## /testnet_config

## /status

## /submit_tx

## /account/:id

