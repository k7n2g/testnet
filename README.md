![TESTNET In Operation](https://user-images.githubusercontent.com/317/40411678-465103e0-5e9b-11e8-8ac0-84538920aabe.png)

**Testnet Name:** Vico  
**Current Status:** running

**Algorithms**  
Hash: CryptoNight Lite Variant 1  
Difficulty: ???? 7xT  

**Seed Node Status**: https://testnet-vico-7xt.turtlecoin.ws/status/
**Block Explorer:** https://testnet-vico-7xt.turtlecoin.ws/blocks/
**Mining Pool**: https://testnet-vico-7xt.turtlecoin.ws/pool/

**Purpose**  
Right now it is the only live testnet.  
It has all of master's commits up to `eb5d0a`  

The two web wallets in dev are using it.

You can running anything you want on this testnet, if you run into issues ping us in [\#dev-general chat](http://discord.turtlecoin.lol)  

**Quickstart**

Linux *(deps already taken care of cause you already run mainnet)*
```
git clone --depth 1 -b vico-7xT https://github.com/turtlecoin/testnet.git trtl-testnet-vico-7xT_src
mkdir -p trtl-testnet-vico-7xT_run/data
mkdir trtl-testnet-vico-7xT_src/build
cd trtl-testnet-vico-7xT_src/build
cmake -DCMAKE_BUILD_TYPE=Release -DDO_TESTS=OFF ..
# specify -j core count here for fast build
make 
cd src
cp TurtleCoind simplewallet walletd miner ../../../trtl-testnet-vico-7xT_run/
cd ../../../trtl-testnet-vico-7xT_run/
cat <<EOT > trtl-testnet-vico-7xT
rpc-bind-ip=127.0.0.1
data-dir=$(pwd)/data
log-file=$(pwd)/trtl-testnet-vico-7xT.log
EOT
./TurtleCoind --config-file=trtl-testnet-vico-7xT
```

**Disclaimer**  
Testnets are for testing, they are disconnected from the main TurtleCoin Network.  
As such coins on mainnet can't be sent to testnet and testnet coins can't be sent to mainnet.  
