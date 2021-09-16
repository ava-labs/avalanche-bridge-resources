## Adding Your Token to the Avalanche Bridge

We are always evaluating new tokens to add support for on the Avalanche Bridge. In order to have a token be considered, please create a PR following the steps and requirements below. Creating a PR doesn't ensure that your token will be added, as there is a multifaceted internal review process for a token to be approved.

### General Requirements
1. The token contract must be verified on [Etherscan](https://etherscan.io/).
2. The token must have a token/ETH Chainlink price feed on the Ethereum Mainnet. See Chainlink price feed addresses [here](https://docs.chain.link/docs/ethereum-addresses/). 

### Adding Your Token
1. Submit a PR with the following information in the `token_list.json` file. Here is an example using Link:
    ```json
    "LINK": {
		"nativeNetwork": "ethereum",
		"nativeContractAddress": "0x514910771af9ca656af840dff83e8264ecf986ca",
		"denomination": 18,
		"chainlinkFeedAddress": "0xDC530D9457755926550b59e8ECcdaE7624181557",
		"logo": "https://raw.githubusercontent.com/ava-labs/avalanche-bridge-resources/main/tokens/LINK/logo.png",
		"coingeckoId": "chainlink"
	},
    ```
2. Include a png file for the token logo in the `Tokens/` directory.
3. The `chainlinkFeedAddress` field must refer to the token/ETH Chainlink price feed.
4. If your token has a Rinkeby feed, we strongly encourage you to add your token to the token_list.test.json configuration.
5. The template used for token deployments on the Avalanche C-Chain can be found in the `SmartContracts/` directory. If your project requires additional features, please contact the Ava Labs team.
6. It is important to note that the `nativeContractAddress` refers to the contract on Ethereum mainnnet. Once a token is added to the bridge, the Avalanche C-Chain address will be added to the `avalanche_contract_address.json` file.

### Avalanche C-Chain Contract Addresses
1. All tokens that are supported by the bridge have their Avalanche C-Chain contract address listed within the `avalanche_contract_address.json` file.
