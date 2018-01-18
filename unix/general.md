# General unix commands

### List all users and their id

```
cut -d: -f1,3 /etc/passwd
```

### Create group with specified group id

```
groupadd --gid <group-id> <group-name>
```


### Create user with specified user id, without home and assigned to group

```
useradd --uid <user-id> -M --gid <group-id> <user-name>
```