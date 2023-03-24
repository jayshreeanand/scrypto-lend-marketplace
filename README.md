# Scrypto Lend Marketplace on Betanet V2

This project is build using Scrypto and [Radix dApp Toolkit](https://github.com/radixdlt/radix-dapp-toolkit#readme). It is deployed on Radix Betanet V2 using Radix (Test) android wallet and Radix connector chrome extension

## Pre-requisites

1. Node >= 12.17.0
2. The Betanet wallet & Radix-connector browser extenstion installed. Instructions [here](https://docs-babylon.radixdlt.com/main/getting-started-developers/wallet-and-connector.html)
3. Scrypto v0.8.0. Instructions to install [here](https://docs-babylon.radixdlt.com/main/getting-started-developers/first-component/install-scrypto.html) and update [here](https://docs-babylon.radixdlt.com/main/getting-started-developers/first-component/updating-scrypto.html)

## Building the Scrypto code

1. Enter the scrypto directory in a terminal: `cd scrypto`
1. Build the code: `scrypto build`
1. Two important files (`scryptlend.abi` and `scryptlend.wasm`) will be generated in `scrypto/target/wasm32-unknown-unknown/release/`. You will need them for the next step.

## Deploy the package to Betanet

1. Go to the [Betanet Dashboard Website](https://betanet-dashboard.radixdlt.com/)
2. Connect the Wallet Via the Connect Button
3. Navigate to Deploy Package & choose an account and badge or have one created for you if you don't have one yet using the link below. (Which appears once you have selected an account)
4. Upload both `scryptlend.abi` and `scryptlend.wasm`
5. Click on "publish package"
6. The wallet should open up and ask you to approve the transaction
7. On the wallet click on "sign transaction"
8. The deployed package address should get displayed. **You will need it for the next step**.

## Interacting with our package

1. In a terminal go back to the root of this project (scrypto-lend-marketplace)
2. Install the npm dependencies: `npm install`
3. Start the local server with `npm start`
4. Open up your browser at the provided url if it doesn't open automatically.
5. Make sure you created an account on the wallet and added funds via the faucet by clicking on account name and then the three dots a button to get XRD from faucet should open.
6. Click on the connect button to fetch your wallet address. You should see your address appearing
7. Fill the package address you got in the previous section and "instantiate "
8. Your wallet will again open up. Click on "sign transaction". You should now see the instantiated component address and resource address on the page.
9. Fill in the loan details and submit proposal by clicking on "Submit proposal"
10. Your wallet will open up. Click on "sign transaction". The transaction receipt will get displayed on the page.
