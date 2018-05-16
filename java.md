# java commands

### Print system properties

```
java -XshowSettings:properties -version
```

### List certificates in trust store

```
keytool -list -v -keystore <path-to-trust-store>.jks
```

### Put certificate into trust store

```
keytool -import -alias stan -file <path-to-certificate> -keystore <path-to-trust-store>.jks
```
