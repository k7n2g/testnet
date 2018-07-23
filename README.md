![TESTNET In Operation](https://user-images.githubusercontent.com/317/40411678-465103e0-5e9b-11e8-8ac0-84538920aabe.png)

This repo is for setting up testnets. Dedicated testnets let us fully test various changes that the --testnet flag doesn't let us test.

Each branch of this repo is a testnet, on each branch the README.md should explain what it is about.  
This master/development branches will be kept in sync with upstream master turtlecoin/turtlecoin and testnets can be created from master or development:

```
git clone https://github.com/turtlecoin/testnet.git

# if tracking master
git checkout -b new-testnet

# if tracking development
git checkout development
git checkout -b new-testnet
```

Master branch tracks released code.  
Development branch tracks code in development/testing.

Note that there are missing parameters that need to be filled in, this is on purpose to avoid accidentally joining the testnet to mainnet.


## 3x Permanent Testnets

We've talked about this a few times in #dev_general on [Discord](http://chat.turtlecoin.lol). Things come up and there isn't really anyway to effectively verify & check things out before going live. Thus the idea was raised to launch 3x permanent testnets.

- TestnetMainClone
- TestnetDevClone
- TestnetDevZero

So these 3x testnets are being setup and deployed, can monitor this testnet repo for activity.

## Call for Testnet Seed Nodes

These testnets require seed nodes to be running and kept up to date. SoreGums has launched the required minimum of 3x nodes for each one. However if anything happens to the host/server these are all on, the testnets will stop working and possibly require being reset - start again. Running a seed node won't get you anything, it is purely for the lulz and for the benefit of the community.

Here is what makes a seed node a seed node

- listed in the config as a seed node
- node is available/connectable 24/7
 
This is what is required of a seed node operator

- ensure daemon is available/connectable 24/7 and respond swiftly when/if there are issues 
- update daemons as things are updated
- run a 1 thread solo miner 24/7
- expose the daemon's RPC API port either to the public _(not ideal)_ or only to SoreGums dedicated IP for the seed nodes stat page
- able to be in [Discord](http://chat.turtlecoin.lol) to be notified when things are updated
  * #dev_general is where testnet info is discussed

If you are able to assist by running a seed node please ping SoreGums#8071 in #dev_general on the TurtleCoin [Discord](http://chat.turtlecoin.lol). You can absolutely participate if you have never done anything like this before! TurtleCoin is also all about the Education of how Blockchain technology works. If you have capability to run something 24/7 for an extended period of time, jump in.

## Testnets Being Deployed

Check readme on each Testnet for additional information.

- [testnet-main-clone](https://github.com/turtlecoin/testnet/tree/testnet-main-clone)
  * from turtlecoin/turtlecoin master branch
  * blockchain is a clone of mainnet from block 650,000 _(target)_
  * Web Wallets will be tested here _(as testnet is down, so are the wallets)_
    - [Canti Web Wallet](https://canti.turtlecoin.ws/redeem.php?key=wVishaQguTRTL70Mem5rLOTasdTOblnY8JBjTRTLtk4mE3sLOTafTO2QNfhkwVnpDrgu6sFcTRTLhkbt8ZjLOTasdadTOqJRWzl7Yl) - [Discord](https://discord.gg/FBzS7J6)
    - [TurtleWallet.io](https://beta.turtlewallet.io/) - [Discord](https://discord.gg/Z4utZ7x)
- [testnet-dev-clone](https://github.com/turtlecoin/testnet/tree/testnet-main-clone)
  * from turtlecoin/turtlecoin development branch
  * blockchain is a clone of mainnet from block 650,000 _(target)_
- [testnet-dev-zero](https://github.com/turtlecoin/testnet/tree/testnet-dev-zero)
  * from turtlecoin/turtlecoin development branch
  * blockchain starts from zero

## Previous Testnets

- [lwma-2](https://github.com/turtlecoin/testnet/tree/lwma-2)
- [vico-7xT](https://github.com/turtlecoin/testnet/tree/vico-7xT)
- [main-clone](https://github.com/turtlecoin/testnet/tree/main-clone)
