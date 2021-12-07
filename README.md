# Convex System Shutdown Benchmarks

This repository benchmarks performance of various Ethereum development
frameworks by simulating a call to Convex's `systemShutdown` method. This method
uses about 16M gas and performs a number of token transfers

## Usage

1. Run `cp .env.example .env`, and in the resulting `.env` file enter a URL to an Ethereum archive node in the `ETH_RPC_URL` environment variable. ([Alchemy](https://www.alchemy.com/) provides free archive node data)

2. Run `yarn` to install dependencies for Ganache and Hardhat 

3. Install Foundry's forge and Dapptools using the installation instructions[here](https://github.com/gakonst/foundry/) and [here](https://github.com/dapphub/dapptools/) respectively

4. Run `dapp update` to install dependencies for Dapptools and Foundry

5. Run any command in the `Makefile` to benchmark that tool. For example, use `make benchmark-hardhat` to run the simulation against Hardhat. Alternatively, run `make benchmark-all` to run all tools

## Tips

Dapptools seems to fail when run on macOS, as explained in [this](https://github.com/dapphub/dapptools/issues/876), so you may need to skip that script on macOS
