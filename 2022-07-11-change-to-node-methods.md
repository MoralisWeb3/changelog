# Changes in available Node methods for FREE plan starting July 11, 2022

## Products affected
- [ ] SDK
- [ ] API
- [ ] Admin UI
- [X] Nodes

## Is this a breaking change?
- [X] yes
- [ ] no

## Description of the change
Moralis is not aiming to be a node provider. Moralis aims to provide nodes for dapp and smart contract developers however we've noticed that our nodes are also heavily used by users running big indexing jobs - these users are not interested in using the rest of the moralis stack and often sign up on several free plans which drains our resources that could be used to strengthen the Moralis full stack workflow.

Therefore we are changing our nodes to be mostly useful to users developing contracts which doesn't require historical data.

By doing this we hope to make our efforts laser focused on Moralis full stack experience, decrease abuse of multiple free accounts to get node access for indexing purposes and streamline our funnel so we only attract developers interested in Moralis full stack dev tools.

The following methods on our RPC nodes will only be available for the latest 15 minutes:
 - eth_getBlockByNumber
 - eth_getBlockByHash
 - eth_getTransactionByHash
 - eth_getTransactionReceipt
 - eth_getLogs

## What exactly can break?
If you are using our nodes for some kind of database building, or for other reasons are using our nodes to fetch information older than 15 minutes using any of the methods listed above you will not be able to do so.
For the time being you will still be able to use these methods for recent blocks.

## How to ensure my app won't break?
If you are using our nodes in the ways listed above, we  encourage you to use another chain provider.
You can find partner providers here: https://moralis.io/largenodes

We highly encourage you to also use our Web3API where you will be able to fetch the same information that we are now limiting from the nodes, still we provide an even better developer experience.

## When will this change go live ?
2022-07-11

## Link to Moralis Forum for discussions
https://forum.moralis.io/t/changes-to-speedy-nodes-methods-from-july-12-2022/16241

We have staff monitoring forum 24/7 - while we don't monitor Github as much - so we need everyone to discuss in the forum
