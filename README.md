# A hard fork from BitaCoin

## What are the most important Items in this fork?

* Decentralized Network
* RSA Wallet
* Mining Reward
* Transaction Fee
* Transaction Expiration
* Fix Double Spend Problem

## If you want to see a scenario check [this medium post](https://medium.com/@amirhossein2000/lets-run-a-coin-base-blockchain-that-is-written-by-golang-e9743d54a58) that has been written by me.

## Sample config file:

```json
{
  "Host": "127.0.0.1:8080",
  "InitialNodes": [
    "127.0.0.1:8081",
    "127.0.0.1:8082"
  ],
  "PubKeyPath": "./miner_wallet/public_key.txt"
}
```

Config Items | Explanations
------------ | -------------
Host | The address for serving web handlers
InitialNodes | Other nodes addresses
PubKeyPath | Public_key of miner wallet that gets the reward coins after mine a new block

## Commands:

### Generate key pair of a wallet:

```bash
./bitacoin wallet -dir <wallet directory path>
```

### Initialize the blockchain and create genesis block:

```bash
./bitacoin init -pub <genesis block owner public_key>
````

### Start web servers and miner worker:

```bash
./bitacoin start -config <config file>
````

### Download the blockchain data from other nodes:

```bash
./bitacoin download -config <config file>
````

## You should use the [bitacoin_client](https://github.com/Amirhossein2000/bitacoin_client "bitacoin_client") to get wallet balance and transfer coins.
