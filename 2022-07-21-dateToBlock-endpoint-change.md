# Endpoint `/dateToBlock` no longer supports `providerUrl` parameter from July 21st 2022

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

The `/dateToBlock` endpoint will no longer support the `providerUrl` parameter for use with local dev chains.
However, the `subdomain` parameter, specifying the subdomain of the moralis server to use will be made available.

## What exactly can break?

Any use of local dev chain relying on the `providerUrl` with the `/dateToBlock` endpoint will no longer return a result.

## How to ensure my app won't break?

In cases where a local dev chain is utilized, such chain must be setup through a moralis server and its address should be specified in the `subdomain` parameter.

## When will this change go live and be mandatory?

2022-07-21

## Link to Moralis Forum for discussions

https://forum.moralis.io/t/changes-to-datetoblock-endpoint/17237
