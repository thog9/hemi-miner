# Hemi Miner Testnet

> Hemi is a modular protocol for superior scaling, security, and interoperability, powered by Bitcoin and Ethereum.
 
#

* For non-Node participants, you can join  pilot program [here](https://points.absinthe.network/hemi/) : Use my code to Enter: `4ba337e5`
* You can run miner using web browser on windows here: https://pop-miner.hemi.xyz/

## Install Miner on Linux
**1. Download Binaries**
```bash
wget https://github.com/hemilabs/heminetwork/releases/download/v0.4.3/heminetwork_v0.4.3_linux_amd64.tar.gz
```

**2. Extract Binaries**
```bash
tar -xvf heminetwork_v0.4.3_linux_amd64.tar.gz && rm heminetwork_v0.4.3_linux_amd64.tar.gz && cd heminetwork_v0.4.3_linux_amd64
```

## Wallet
**1. Create tBTC wallet**
```bash
./keygen -secp256k1 -json -net="testnet" > ~/popm-address.json
```

**2. Get tBTC address**
```bash
cat $HOME/popm-address.json
```
* Save the output
* `pubkey_hash` is your tBTC address

**3. Fund your wallet**
* Get tBTC faucet in [Discord](https://discord.gg/hemixyz) for your bitcoin wallet
* Check your txhash in explorer until it get CONFIRMED

## Start Miner

**1. Replace your private key with `PRIVATE_KEY`**
```bash
echo 'export POPM_BTC_PRIVKEY=PRIVATE_KEY' >> ~/.bashrc
echo 'export POPM_STATIC_FEE=50' >> ~/.bashrc
echo 'export POPM_BFG_URL=wss://testnet.rpc.hemi.network/v1/ws/public' >> ~/.bashrc
source ~/.bashrc
```

**2. Start your node**
```bash
./popmd
```


