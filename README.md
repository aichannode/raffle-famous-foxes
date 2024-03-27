![React JS Apps](https://firebasestorage.googleapis.com/v0/b/athena-1127.appspot.com/o/images%2Fother%2F003.png?alt=media&token=cffb8742-171e-4c0c-afb7-4a7ce6ed7def "React JS Apps")

This is a [Next.js](https://nextjs.org/) project. 

Full process and video lectures on how to create the application can be found here: [NFT Marketplace in React, Typescript & Solidity - Full Guide
](https://academy.eincode.com/courses/nft-marketplace-in-react-js-next-typescript-full-guide)

# Rafffle.Famousfoxes: NFT Marketplace Website

![star this repo](https://img.shields.io/github/stars/react-native-webview/react-native-webview?style=flat-square)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![NPM Version](https://img.shields.io/npm/v/react-native-webview.svg?style=flat-square)](https://www.npmjs.com/package/react-native-webview)
![Npm Downloads](https://img.shields.io/npm/dm/react-native-webview.svg)

## Overview

The marketplace has dependencies on multiple technologies.

* [Website](https://rafffle.famousfoxes.com/) - Rafffle | Create your own rafffle
* [Pinata](https://app.pinata.cloud/) - store images, and NFT metadata
* [Ganache](https://trufflesuite.com/ganache/) - private Blockchain, to run applications locally

## Preview

Welcome to my project! Below are my favorite screenshots related to this project:

<img src="https://github.com/codecrafts1128/Rafffle_FamousFoxes_ReactJS/blob/master/public/screens/1.png" width="250" alt="Screen 1" hspace="5"> <img src="https://github.com/codecrafts1128/Rafffle_FamousFoxes_ReactJS/blob/master/public/screens/2.png" width="250" alt="Screen 5" hspace="5"> <img src="https://github.com/codecrafts1128/Rafffle_FamousFoxes_ReactJS/blob/master/public/screens/3.png" width="250" alt="Screen 4" hspace="5">

## Getting Started

1. run `npm install` to install dependencies

2. In the root folder of the application create a `.env.development` file with the following content:

```
NEXT_PUBLIC_NETWORK_ID=5777
NEXT_PUBLIC_TARGET_CHAIN_ID=1337
NEXT_PUBLIC_PINATA_DOMAIN=https://gateway.pinata.cloud

SECRET_COOKIE_PASSWORD={your custom at least 32 characters long password!}

PINATA_API_KEY={your api key from pinata}
PINATA_SECRET_API_KEY={your api secret key from pinata}
```
* (Your API pinata key has to allow `pinFileToIPFS` and `pinJSONToIPFS` rules)

3. Then migrate a contract to Ganache, contract can be found in the `contracts` folder. It's called `NftMarket.sol`

* To migrate the contract run `truffle migrate` in the terminal while Ganache network is set up and running.

* Do not forget to link `trufle-config.js` with Ganache, just go to `config` and click `Add Project`

* `keys.json` must be created if you want to deploy to Ropsten, if not, just remove import of `keys.json` from `trufle-config.js` and also comment out `ropsten` configuration

4. Now everything is set up and you can test out the app.

* Run `npm run dev` in the terminal. The app will run at `localhost:3000`

### Congratulations! :tada:

You've successfully run and modified your React Native App. :partying_face:

## License

Rafffle.Famousfoxes is licensed under [The MIT License](LICENSE) © Silas Jones 2021-
