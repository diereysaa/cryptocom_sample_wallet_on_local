# Crypto.com Sample Wallet on local machine
This document describes the steps on how to setup a chain wallet on a local machine.

Basically two main things are required: running the client-rpc and running the node app
Also, a full Crypto.com chain implementation is needed:

#### Pre-requisites
Install Crypto.com Chain
You can follow my tutorial here: https://github.com/diereysaa/cryptocom_council_node_on_local/blob/master/README.md up to the part where it installs the chain. Also adding the chain listener as a service.

> :information_source: _Since you're probably running this as an "extra" of a council|full node, you already have the Crypto.com chain installed and running._

---

## Compiling the wallet

#### Update the system
```shell
sudo apt update
```

#### Install node.js
```shell
sudo apt install nodejs
sudo apt install libssl1.0-dev
sudo apt install nodejs-dev
sudo apt install node-gyp
sudo apt install npm
```
_(Note: you have to go step by spet on the above, because there are unmet dependencies that depend one on each other)_


#### Cloning the wallet code
```shell
cd ~
git clone https://github.com/crypto-com/sample-chain-wallet.git ./crypto_wallet
```
_We will be using `crypto_wallet` for the wallet folder. You can use any folder you want, but be sure to **always use the same folder** from now on_

> :warning: If you're using a specific server on your network, and want to connect from another machine in your network, edit the **package.json** and change the "start" line, from
> ```
>    "start": "ng serve",
> ```
> to
> ```
>    "start": "ng serve --host 0.0.0.0   --port 4200 --disable-host-check",
> ```

#### Now we need to install the whole package:
```shell
npm install
```

---

## Running the ClientRPC
If you have followed my other guide to setup a full/council node (https://github.com/diereysaa/cryptocom_council_node_on_local/blob/master/README.md) you will have `client-rpc` on the **crypto_node** folder.

#### Copy the executable to the new path
```shell
cd ~
cp crypto_node/client-rpc crypto_wallet/client-rpc
```


npm start
```
_Note: This will launch the server to show the wallet, so it's a good idea to only have this running while you're operating with the wallet._

If you're using an external server, now you can go to any browser and try the server IP on the port 4200:

**http://<SERVER_IP>:4200**


