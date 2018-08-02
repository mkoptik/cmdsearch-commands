# Commands for Ethereum geth client

### Get synchronization status

```
geth attach
> eth.syncing
```

`geth attach` opens JavaScript console. When synchronization is not in progress, command `eth.syncing` returns false. When synchronization is in progress, json is returned with property *currentBlock* and *highestBlock*

### List ethereum accounts in local geth node

```
geth account list
```
