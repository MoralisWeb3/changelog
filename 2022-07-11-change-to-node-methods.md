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
Here at Moralis, our main mission is to build a full-stack web3 flow.

We aim to provide you with the tools and resources you need so that you can take everything you know and develop amazing Web3 projects hassle-free.

"Speedy Nodes" have been a small part of our infrastructure service since we launched. However, as part of our improvement process, we will be retiring these nodes from our services.

Due to major growth, the majority of our users have now transitioned to our full-stack services, and our decision to discontinue speedy nodes will allow us to focus on our core technology.

🚨These changes will take place on Monday the 11th of July for free plans and 1st of September for pro users. 🚨

If you would like to switch to our Web3API, it offers many of the functionalities for which you may currently be using speedy nodes. Changing not only saves requests but also ensures your dapp is cross-chain by default. 


# **Web3API to the rescue**

Our Web3API offers many of the functionalities that you currently may be using the RPC nodes for. Not only do you save a lot of requests, but it makes your app cross chain by default as switching to another chain is just a matter of changing a parameter for each endpoint.

Below you will find some examples of endpoints that you can use, if you were previously relying on RPC nodes for retrieving information about blocks and transactions



* To call a smart contract function, you can use our [runContractFunction endpoint \
](https://deep-index.moralis.io/api-docs/#/native/runContractFunction)
* If you were using the nodes to build your own database, you can use the [getBlock endpoint](https://deep-index.moralis.io/api-docs/#/native/getBlock) that allows you to get a full block along with all the transactions and respective logs in one single request. This saves you from first getting the block by block number from the RPC node and then getting the receipts for each transaction with the getTransactionReceipts method: So instead of needing to do thousands of requests, now you only need to make one[ \
](https://deep-index.moralis.io/api-docs/#/native/getBlock)
* If you were using the RPC nodes to get information about a transaction made in your dApp, you can use the [getTransaction endpoint](https://deep-index.moralis.io/api-docs/#/native/getTransaction). It allows you to get a full transaction with all the logs by transaction hash

Click [here](https://admin.moralis.io/web3api) and [here](https://deep-index.moralis.io/api-docs) to see our other endpoints that will save you a lot of time.


# **Benefits of using the API**

By using the API you get faster and more reliable responses but most importantly you will get cross-chain compatibility even when Moralis adds non-EVM chains.

For nodes, you can also take a look at the services provided by some of our [partners.](https://moralis.io/largenodes)

We want to continue to be there for you to support your build — from the first line of code of your project through to the first dollars of funding — not just in terms of infrastructure, but also in terms of support, education and more.


## How to ensure my app won't break?
You can find partner providers here: https://moralis.io/largenodes

We highly encourage you to also use our Web3API where you will be able to fetch the same information that we are now limiting from the nodes, still we provide an even better developer experience.
https://docs.moralis.io/moralis-dapp/web3-api


## When will this change go live ?
2022-07-11


