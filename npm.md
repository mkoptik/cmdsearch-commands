# Node package manager commands

### Update npm to latest version

```
npm update npm -g
```

Updates itself

### Install specific NodeJS version

```
sudo n <version>
```

version in format v8, v9, v10

### Login to private repository

```
npm login --registry=<registry-url> --scope=<dependencies-scope>
```

### Link two packages

```
package1$ npm link
package2$ npm link <name-of-package-1>
```
