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

### Change user name and email for repository

```
git config user.email "<email-address>" && git config user.name "<name-of-user>"
```

This will apply change only for single repository. To apply this change globally, add --global modifier
