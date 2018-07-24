# Git example commands

### Change remote URL

```
git remote set-url origin <remote-url>
```

### Create patch from staged changes

```
git diff --cached > <patch-file>
```

--cached: Use stashed changes

### Apply stash on working directory

```
git apply <patch-file>
```
