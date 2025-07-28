# octra-testnet
a guide and walkthrough for octra testnet,


so far we are 2 phases gone which innvolves wallet generation and the CLI interactions like token sending, encryption and decryption of tokens

if you are yet to generate a wallet follow through here and claim faucet https://github.com/octra-labs/wallet-gen 


# Now fastforward to current testnet version
its a new CLI version, a script with alot of new interaction options available

<img width="742" height="526" alt="image" src="https://github.com/user-attachments/assets/0c094f53-418d-43ab-a4d5-04a1d36a424e" />

# guide

change to home directory
```
cd ~
```


install rust if you haven't yet 
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```

clone the new repo and build
```
git clone https://github.com/octra-labs/ocs01-test.git
cd ocs01-test
cargo build --release
```

copy contract interface 
```
cp EI/exec_interface.json ~/ocs01-test
```

now you need to copy your wallet.json file from where you have been interacting before to this new dir or you can simple create it

N:B...both your wallet.json file and exec_interface.json file needs to be on the same directory for this to work 

you can navuigate to where the wallet.json file is and copy to the new directory
```
cp wallet.json ~/ocs01-test
```
OR you can simply create it if you have your previous private key and aaddress 

```
nano wallet.json
```

copy the below content into the wallet.json 
```
{
  "priv": "your private key",
  "addr": "your octra wallet address",
  "rpc": "https://octra.network"
}
```
use ctrl X then Y, then enter to save 


start the CLI

```
./target/release/ocs01-test
```

Interact with all the listed options at least once and you are good to go
