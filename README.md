## Adding Your Token to the Avalanche Bridge


### General Requirements
1. Token should be present on Ethreum Mainnet and verifiable on the [etherscan explorer](https://etherscan.io/).
2. Token must have a valid Token/ETH Chainlink Price feed on the Ethereum Mainnet

## Adding Your Token
1. Submit a PR with the following information in the `token_list.json` file. Here is an example using Link:
    ```json
    "LINK": {
		"nativeNetwork": "ethereum",
		"nativeContractAddress": "0x514910771af9ca656af840dff83e8264ecf986ca",
		"denomination": 18,
		"chainlinkFeedAddress": "0xDC530D9457755926550b59e8ECcdaE7624181557",
		"logo": "https://raw.githubusercontent.com/ava-labs/bridge-tokens/main/avalanche-bridge-token-list/tokens/LINK/logo.png",
		"coingeckoId": "chainlink"
	},
    ```
2. Include a png file for the token image in the Tokens/ directory
3. The chainlinkFeedAddress field must refer to a Token/ETH Chainlink Price feed
4. If your token has a Rinkeby feed, we strongly encourage you to add your token to the token_list.test.json file
5. The template used for token deployments on the Avalanche C-Chain can be found in the SmartContracts/ directory.  If your project requires additional features, please contact the Ava Labs team
6. Important to note that the nativeContractAddress refers to the contract on Ethereum Mainnnet.  Once a token is added, the Avalanche C-Chain address will be added to the avalanche_contract_address.json file

## Avalanche C-Chain Contract Addresses
1. All tokens that are supported by the bridge have their Avalanche C-Chain contract address listed within the avalanche_contract_address.json file.
