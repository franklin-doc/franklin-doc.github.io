---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - javascript
  - ruby

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
const Franklin = require('franklin');
const franklin = new Franklin(new HttpProvider('https://ropsten.infura.io'));
</pre>

# Deposits

# Checking balance

# Transfers

# Withdrawals
