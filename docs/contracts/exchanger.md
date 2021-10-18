---
title: Exchanger
---

Exchanger
========

This contract for indexing pair and getting a commission. This contract like a main database in blockchain. It contrains methods to get and create a pairs, save it and use. 

#### Variables
* bytes name - name of market
* uint128 commission - commission in percent
* uint128 highest_commission - the highest commission that could be possible
* TvmCell pair_code - code of nft pair
* TvmCell auction_code - code of auction
* (Address=>[PairState](/types)) pairs - index of pairs
* uint64 time_limit - the biggest time that could be set to pair
* address withdraw_address - its the address where will be sent a commission

#### Getters
* resolveNFTPair(uint128 price, uint64 time, address client, uint256 pubkey) return address addrData - help to get an address of fututre nftpair
* resolveNFTAuction(uint128 price, uint64 time, uint128 step, address client, uint256 pubkey) return address addrData - help to get an address of fututre nftauction



#### Methods
All methods call from [controller](/contracts/controller)
