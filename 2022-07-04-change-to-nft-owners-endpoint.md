# Changes to the NFT owners endpoint: `/nft/:address/owners` and `/nft/:address/:token_id/owners` from July 4, 2022

## Products affected
- [ ] SDK
- [X] API
- [ ] Admin UI
- [ ] Nodes
- [ ] Servers

## Is this a breaking change?
- [ ] yes
- [X] no

## Description of the change

The endpoints `/nft/:address/owners` and `/nft/:address/:token_id/owners` will no longer be ordered based on descending block number but rather based on descending activity timestamp to give a consistent return of data based on recent activity on the nfts.

## What exactly can break?

It is not a breaking change

## How to ensure my app won't break?

Nothing needs to be done as it is not a breaking change

## When will this change go live and be mandatory?

2022-07-04

## Link to Moralis Forum for disucssions


We have staff monitoring forum 24/7 - while we don't monitor github as much - so we need everyone to discuss in the forum