# Changes for Ethereum Post-Merge on Testnets 

## Products affected
- [ ] SDK
- [x] API
- [ ] Admin UI
- [x] Nodes
- [x] Servers

## Is this a breaking change?
- [x] yes
- [ ] no

## Description of the change
The Ethereum core developers decided that the following testnets will be maintained in the future, including the merge:

- Sepolia Testnet (PoW), chain ID 11155111, https://sepolia.dev
- Goerli Testnet (PoA, rebranded to Prater testnet), chain ID 5, https://goerli.net

The following testnets will no longer receive protocol upgrades and shall no longer be considered:

- Kovan (PoA, chain ID 42)
- Ropsten (PoW, chain ID 3)
- Rinkeby (PoA, chain ID 4)
- The Ropsten Testnet (PoW, chain ID 3) will be receiving the merge upgrade for testing purposes but subsequently be deprecated in 2022.

## What exactly can break?
 The following testnets will be removed post-merge from Moralis Server, Moralis Nodes and from Moralis API:
### Kovan: 
- it has been declared dead multiple times.
- it will not be upgraded for the merge and subsequent protocol upgrades. 
- applications on Kovan should prepare to migrate to Goerli or Sepolia as soon as possible.
### Rinkeby: 
- Geth team plans to remove it after the merge
- it will not be upgraded for the merge and subsequent protocol upgrades. 
- applications on Rinkeby should prepare to migrate to Goerli or Sepolia as soon as possible.
- it should not be considered a public Ethereum testnet anymore
### Ropsten: 
- is run by whoever mines it, it has been dead, revived, and deprecated before.
- it will be upgraded for the merge but deprecated right after.
- it will most likely not receive post-merge upgrades and eventually also be removed from Geth in the future.
- applications on Ropsten should prepare to migrate to Goerli or Sepolia as soon as possible.

## How to ensure my app won't break?

### Migrate to Goerli (Recommended)

The best way to ensure no of your test environments break is to migrate to Goerli.
Nothing will change for Goerli and Moralis already offers Goerli support in Moralis Server, Moralis Nodes and Moralis API.

- Get some goerli Ethers (gEth), from faucets: [goerli faucet](https://goerlifaucet.com/) or [Goerli Authenticated Faucet](https://goerli-faucet.mudit.blog/)
- Migrate/Deploy your Smart Contract(s) to Goerli testnet. 

*IMPORTANT:* Goerli will be rebranded to Prater after the merge.


### Migrate to Sepolia

Moralis is working on adding Sepolia testnet to Moralis Nodes and Moralis API.

We expect this to be done at the merge date which should be around June 8th.

- Add Sepolia Tesnet to Metamask:
```
Network Name: Sepolia Testnet
RPC URL: https://nunki.htznr.fault.dev/rpc
ChainID: 11155111
Symbol: SEP
```
- Get some Sepolia Ethers (SEP), from [Sepolia faucet](https://faucet.sepolia.dev/)
- Migrate/Deploy your Smart Contract(s) to Sepolia testnet.



## When will this change go live and be mandatory?

We cant't set a exact date because we have to wait for the merge to happen, its rely on the TTD.

Proof-of-Work testnets can have volatile hash rates and the exact timing of The Merge is hard to predict accurately. Assuming no unexpected hash rate fluctuations, we expect The Merge to happen around June 8-9, 2022
