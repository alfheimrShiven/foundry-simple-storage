# Welcome to my first smart contract Foundry project 

This has been deployed on Sepolia TestNet:

Contract Address: ```0xf3267284701C45Bc62Dc121649Ab348Ec144fc7b```

Block explorer: ```https://sepolia.etherscan.io/```

This contract was deployed through the ```DeploySimpleStorage.s.sol``` script.

## Add the following env. variables to your .env file:
```
SEPOLIA_PRIVATE_KEY=${YOUR_SEPOLIA_PRIVATE_KEY}
SEPOLIA_RPC_URL=${YOUR_SEPOLIA_RPC_URL}
```

## Deploy cmd:
```
source .env

forge script script/DeploySimpleStorage.s.sol --rpc-url $SEPOLIA_RPC_URL --private
-key $SEPOLIA_PRIVATE_KEY
```

## Interact with the SimpleStorage.sol smart contract:
1. Store a number:

```
cast send {contractAddress} "store(uint256)" 123 --rpc-url $SEPOLIA_RPC_URL --private-key $SEPOLIA_PRIVATE_KEY
```

2. Retrieve the stored number:
```
cast call {contractAddress} " retrieve()" --rpc-url $SEPOLIA_RPC_URL --private-key $SEPOLIA_PRIVATE_KEY

cast --to-base {returnedHash} dec
```