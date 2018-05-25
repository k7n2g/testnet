![TESTNET In Operation](https://user-images.githubusercontent.com/317/40411678-465103e0-5e9b-11e8-8ac0-84538920aabe.png)

**Testnet Name:** LWMA-2  
**Current Status:** running  
**Lead Developer:** [GH:ZedPea](https://github.com/ZedPea) / [Discord:@Zpalmtree#9096](http://discord.turtlecoin.lol)

**Algorithms**  
Hash: CryptoNight Lite Variant 1  
Difficulty: LWMA-2  

**Block Explorer:** https://testnet-lwma-2.turtlecoin.ws/blocks/  
**Pool**: https://testnet-lwma-2.turtlecoin.ws/  

**Purpose**    
Testing the effects of the LWMA-2 difficulty algorithm (https://github.com/zawy12/difficulty-algorithms/issues/3)
Other slight changes include raising the minimum mixin limits, and lowering the dust threshold to zero.

You can running anything you want on this testnet, if you run into issues ping us in [\#dev-general chat](http://discord.turtlecoin.lol)  

**Quickstart**

Linux *(deps already taken care of cause you already run mainnet)*
```
git clone --depth 1 -b lwma-2 https://github.com/turtlecoin/testnet.git trtl-testnet-lwma-2_src
mkdir -p trtl-testnet-lwma-2_run/data
mkdir trtl-testnet-lwma-2_src/build
cd trtl-testnet-lwma-2_src/build
cmake -DCMAKE_BUILD_TYPE=Release -DDO_TESTS=OFF ..
# specify -j core count here for fast build
make 
cd src
cp TurtleCoind simplewallet walletd miner ../../../trtl-testnet-lwma-2_run/
cd ../../../trtl-testnet-lwma-2_run/
cat <<EOT > trtl-testnet-lwma-2
rpc-bind-ip=127.0.0.1
data-dir=$(pwd)/data
log-file=$(pwd)/trtl-testnet-lwma-2.log
EOT
./TurtleCoind --config-file=trtl-testnet-lwma-2
```

**Disclaimer**  
Testnets are for testing, they are disconnected from the main TurtleCoin Network.  
As such coins on mainnet can't be sent to testnet and testnet coins can't be sent to mainnet.
