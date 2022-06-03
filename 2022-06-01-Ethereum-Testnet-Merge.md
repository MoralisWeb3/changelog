# Changes for Ethereum Post-Merge on Testnets 

## Products affected
- [ ] SDK
- [ ] API
- [ ] Admin UI
- [x] Nodes
- [ ] Servers

## Is this a breaking change?
- [x] yes
- [ ] no

## Description of the change
The Ethereum core developers decided that the following testnets will be maintained in the future, including the merge:

- Sepolia Testnet (PoW), chain ID 11155111, https://sepolia.dev
- Goerli Testnet (PoA), chain ID 5, https://goerli.net

The following testnets will no longer receive protocol upgrades and shall no longer be considered:

- Kovan (PoA, chain ID 42, retired with Parity Ethereum in 2019)
- Ropsten (PoW, chain ID 3, replaced by Sepolia in 2021)
- Rinkeby (PoA, chain ID 4, retired before the merge in 2022)
- The Ropsten Testnet (PoW, chain ID 3) will be receiving the merge upgrade for testing purposes but subsequently be deprecated in 2022.

## What exactly can break?
 The following testnets will be removed post-merge:
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
### Migrate to Sepolia
- Add Sepolia Tesnet to Metamask:
```
Network Name: Sepolia Testnet
RPC URL: https://nunki.htznr.fault.dev/rpc
ChainID: 11155111
Symbol: SEP
```
- Get some Sepolia Ethers (SEP), from [Sepolia faucet](https://faucet.sepolia.dev/)
- Migrate/Deploy your Smart Contract(s) to Sepolia testnet.

### Migrate to Goerli (Recommended)
- Get some goerli Ethers (gEth), from faucets: [goerli faucet](https://goerlifaucet.com/) or [Goerli Authenticated Faucet](https://goerli-faucet.mudit.blog/)
- Migrate/Deploy your Smart Contract(s) to Goerli testnet. 

## When will this change go live and be mandatory?

Around June 8, 2022.