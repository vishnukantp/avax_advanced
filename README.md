# Guide to Creating and Deploying an Avalanche Subnet

This guide outlines the steps to create an Avalanche Subnet and deploy Solidity code using Remix and MetaMask.

## Requirements

- MetaMask extension installed in your browser
- Avalanche-CLI installed on your machine
- Access to Remix IDE (https://remix.ethereum.org/)
- Basic knowledge of Solidity and smart contract development

## Installing Avalanche-CLI

To install Avalanche-CLI, execute the following command in your terminal:

```bash
curl -sSfL https://raw.githubusercontent.com/ava-labs/avalanche-cli/main/scripts/install.sh | sh -s
```

## Steps to Create an Avalanche Subnet

1. **Initiate the Subnet Creation Wizard:**

   Select a name for your Subnet (e.g., `VKR`) and run:

   ```bash
   avalanche subnet create mySubnet
   ```

   Follow the prompts to set up your Subnet.

2. **Deploy the Subnet Locally:**

   To deploy your Subnet locally, use:

   ```bash
   avalanche subnet deploy VKR
   ```

   Choose "Local Network" when asked.

3. **Connect to Your Subnet:**

   Use the following details to connect:

   - **RPC URL:**  http://127.0.0.1:9650/ext/bc/2idntNmJFhF34mpjcLhkYBws6qnWbdk2WLxYJaNBTi1dZiAHD2/rpc
   - **Funded address:** 0x8db97C7cEcE249c2b98bDC0226Cc4C2A57BF52FC with 1000000 (10^18)
   - **Network name:** VKR
   - **Chain ID:** 125
   - **Currency Symbol:** VS

   Note: Add `--http-host=0.0.0.0` to the config to allow API calls from other machines.

## Deploying Solidity Code on Remix with MetaMask

1. **Open Remix IDE:**

   Go to [Remix IDE](https://remix.ethereum.org/).

2. **Connect to Avalanche Subnet:**

   In the "Deploy & Run Transactions" tab, select "Injected Web3" as the environment. Connect MetaMask to your Avalanche Subnet by choosing the correct account.

3. **Compile and Deploy Solidity Code:**

   Paste your Solidity code (e.g., ERC20 and Vault contracts) into Remix. Compile and deploy the contracts to the Avalanche Subnet using MetaMask.

4. **Interact with Deployed Contracts:**

   After deployment, interact with your contracts using the provided RPC URL and addresses.

Congratulations! You've successfully created an Avalanche Subnet, deployed Solidity code, and interacted with the contracts using Remix and MetaMask.
