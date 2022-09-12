# Deprecation of `token_address` on NFT search endpoint: `/nft/search` from Oct 15, 2022

## Products affected
- [] SDK
- [X] API
- [ ] Admin UI
- [ ] Nodes

## Is this a breaking change?
- [X] yes
- [ ] no

## Description of the change

### Deprecation of `token_address` in `/nft/search` endpoint

The `token_address` query parameter in `/nft/search` API endpoint will be deprecated.

Alternatively, you can still use `addresses` parameter to search for NFTs based on their contract address. You are allowed to passed in an array of addresses using this parameter.

## What exactly can break?

If your application relies on `token_address` to perform the contract address specific query, the logic will break. The changes will eventually returns a result of NFTs without filtering based on the contract address.

## How to ensure my app won't break?

In order to ensure that the response still return a result based on contract address, you will need to use the `addresses` parameter instead of `token_address`.

## When will this change go live and be mandatory?

2022-10-15

## Link to Moralis Forum for discussions

https://forum.moralis.io/t/deprecation-of-token-address-on-nft-search-endpoint-nft-search-from-oct-15-2022/19507

We have staff monitoring forum 24/7 - while we don't monitor github as much - so we need everyone to discuss in the forum
