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
keytool -import -alias <certficate-alias> -file <path-to-certificate> -keystore <path-to-trust-store>.jks
```

### Change alias in key store / trust store

```
keytool -changealias -keystore <path-to-key-store>.jks -alias <existing-alias> -destalias <new-alias>
```
