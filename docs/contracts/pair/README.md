---
title: Pair
---

Pair
========
This is an interface for changing ton to nft/ft

#### Variables
* address seller
* uint256 seller_pubkey
* address exchanger
* address[] wallets - list of selling tnft tokens
* PairState status
* address receiver - who will get a tnft tokens
* uint64 finish_time
* uint128 commission
* uint128 price

#### Methods
* addNewToken(address token_addr) - then you transfer tnft token to pair address you need to send a new address of data tnft there
* approveSell() - start selling tokens
* pre_finish() - force send token to owner. Can call only owner of this pair
* finish() - call then time is over
* sell(address client) - call from controller method [buyNFT](/contracts/controller#methods-4)



* [NFTPair](/contracts/pair/NFTPair.md)
* [NFTAuction](/contracts/pair/NFTAuction.md)