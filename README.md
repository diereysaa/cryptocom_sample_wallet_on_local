# Crypto.com Sample Wallet on local machine

Update the system
```shell
sudo apt update
```

Install node.js
```shell
sudo apt install nodejs
sudo apt install libssl1.0-dev
sudo apt install nodejs-dev
sudo apt install node-gyp
sudo apt install npm
```
_(Note: you have to go step by spet on the above, because there are unmet dependencies that depend one on each other)_

Install Crypto.com Chain
You can follow my tutorial here: https://github.com/diereysaa/cryptocom_council_node_on_local/blob/master/README.md up to the part where it installs the chain. Also adding the chain listener as a service.

> :information_source: _Since you're probably running this as an "extra" of a council|full node, you already have the Crypto.com chain installed and running._

Cloning the wallet code
```shell
cd ~
git clone https://github.com/crypto-com/sample-chain-wallet.git ./crypto_wallet
```
_We will be using `crypto_wallet` for the wallet folder. You can use any folder you want, but be sure to **always use the same folder** from now on_

Now we need to install the whole package:
```shell
npm install
npm start
```

