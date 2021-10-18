---
title: Controller
---

Controller
========
This contract is using for connect person, exchanger, true nft

#### Variables
* uint256 client - pubkey of owner this controller

#### Methods
* buyNFT(address pair, price uint128) - Buy a pair (doesnt matter what kind of pair). Need to be an owner of this controller
* mintNFT(rootNFT address, bytes metadata(its a json metadata)) - Mint a new nft for this controller
* transferOwnership(address dataNFT, address addrTo) - Transfer a nft token #TODO
* sendValue(address dest, uint128 amount, bool bounce) - Send some tons
* createNFTPair(address exchanger, uint128 price, uint64 time) - Create new pair #TODO
* createNFTPair(address exchanger, uint128 price, uint64 time, uint128 step) - Create new auction pair #TODO
* setCode(TvmCell newcode) - upgrade to new code 