# Rafffle

[Rafffle](https://rafffle.famousfoxes.com/) — create and run raffles. Powered by [Famous Fox Federation](https://famousfoxes.com/).

This is a [Next.js](https://nextjs.org/) project for the NFT raffle marketplace.

## Overview

* **Website:** [rafffle.famousfoxes.com](https://rafffle.famousfoxes.com/)
* **[Pinata](https://app.pinata.cloud/)** — IPFS for images and NFT metadata
* **[Ganache](https://trufflesuite.com/ganache/)** — local blockchain for development

## Getting started

1. Install dependencies:

   ```bash
   npm install
   ```

2. In the project root, create `.env.development`:

   ```
   NEXT_PUBLIC_NETWORK_ID=5777
   NEXT_PUBLIC_TARGET_CHAIN_ID=1337
   NEXT_PUBLIC_PINATA_DOMAIN=https://gateway.pinata.cloud

   SECRET_COOKIE_PASSWORD={your custom at least 32 characters long password!}

   PINATA_API_KEY={your api key from pinata}
   PINATA_SECRET_API_KEY={your api secret key from pinata}
   ```

   Your Pinata API key must allow `pinFileToIPFS` and `pinJSONToIPFS`.

3. Deploy the Solidity contract locally. The contract is `contracts/NftMarket.sol`. With Ganache running, link `truffle-config.js` to your Ganache workspace, then:

   ```bash
   truffle migrate
   ```

   For Ropsten (or other networks), add `keys.json` as required by `truffle-config.js`, or adjust the config if you only use local development.

4. Run the app:

   ```bash
   npm run dev
   ```

   Open [http://localhost:3000](http://localhost:3000).
