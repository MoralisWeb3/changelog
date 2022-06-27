# Changes to the NFT search endpoint: `/nft/search` from July 1, 2022

## Products affected
- [ ] SDK
- [X] API
- [ ] Admin UI
- [ ] Nodes
- [ ] Servers

## Is this a breaking change?
- [X] yes
- [ ] no

## Description of the change

The `/nft/search` endpoint's ability to filter results using a list of addresses has been discontinued in favor of filtering results using a single token address.

## What exactly can break?

The `/nft/search` endpoint will return nft data that does not match the list of addresses supplied if you are sending queries to the endpoint with the `addresses` parameter to filter the results based on a list of token addresses.

## How to ensure my app won't break?

The `token_address` field, which accepts a single string value rather than a list of token addresses, is what we recommend using in order to ensure a seamless request.

## When will this change go live and be mandatory?

2022-07-01

## Link to Moralis Forum for disucssions

Create a thread in Moralis forum in this category (https://forum.moralis.io/c/changelog/20) and name the thread with the same TITLE as this MR and link it here

We have staff monitoring forum 24/7 - while we don't monitor github as much - so we need everyone to discuss in the forum