# Open SSL 

### Show open ssl default directory

```
openssl version -d
```

### Generate Ethereum public and private key

```
openssl ecparam -name secp256k1 -genkey -noout | openssl ec -text -noout > key
```
