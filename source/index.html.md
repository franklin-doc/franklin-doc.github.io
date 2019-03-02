---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - curl
  - javascript
  - java
  - swift

toc_footers:
  - Created by <a href='https://matter-labs.io'>Matter Labs</a>

search: true
---

# Introduction to Franklin

## What is Franklin Network?

Franklin Network is a rollup sidechain on Ethereum, secured by Zero Knowledge Proofs. Currenty, it is only deployed on Rinkeby testnet. You will find a detailed technical description of rollup sidechain technology [here](https://medium.com/matter-labs/introducing-matter-testnet-502fab5a6f17).

## What is a sidechain?

## What does it mean for practical applications?

# Setting up Franklin.js

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

- newKey(seed)
- sign
- verify

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

## Testnet config

`GET /api/v0.1/testnet_config`

Returns `200 OK` result of the form:

<pre class="center-column">
{
    contract_address: '0x6e3b4c6c6eA4292dFa5E67AC3E34738FFBa1bCFf',
}
</pre>

## Network status

`GET /api/v0.1/status`

Returns `200 OK` result the form:

<pre class="center-column">
{
    contract_address: '0x6e3b4c6c6eA4292dFa5E67AC3E34738FFBa1bCFf',
}
</pre>

## Submit tx

`POST /api/v0.1/submit_tx`

<pre class="center-column">
{ tx_hash, block_id, validator_sig }
</pre>

## Get account data

`GET /api/v0.1/account/:account_id`

<pre class="center-column">
{
    verified: { eth_block_height, balance, nonce, pub_key, [merkle_proof] },
    committed: { eth_block_height, balance, nonce, pub_key, [merkle_proof], [unverified_snark_proofs] },
    pending: { balance, nonce, [list_of_pending_transactions_with_confirmations] }
}
</pre>

## Get account transactions

`GET /api/v0.1/account/:account_id/transactions`

<pre class="center-column">
{
    verified: { eth_block_height, balance, nonce, pub_key, [merkle_proof] },
    committed: { eth_block_height, balance, nonce, pub_key, [merkle_proof], [unverified_snark_proofs] },
    pending: { balance, nonce, [list_of_pending_transactions_with_confirmations] }
}
</pre>