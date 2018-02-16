# General unix commands

### Get linux distribution name and version

```
cat /etc/*-release
```

### Get time zone id

```
cat /etc/sysconfig/clock
```

### Get current date with local timezone

```
date
```

### Compress folder to tar.gz (TODO: !!!! File contains absolute paths)

```
tar -zcvf <archive-name>.tar.gz <directory-name-to-compress>
```

Create compressed file with directory contents where:
- z: Use gzip program
- c: Create archive
- v: Verbose output
- f: Output into given file

### Compress folder to tar.gz and exclude some folder or file

```
tar --exclude='<directory-or-file-to-exclude>' --exclude='<another>' -zcvf <archive-name>.tar.gz <directory-name-to-compress>
```

Parameters description in previous command example. Path to file to exclude can be relative or absolute.

### Extract/Uncompress tar.gz into specified folder

```
tar -zxvf <archive-file>.tar.gz -C <folder-where-to-extract>
```

Archive will be extracted into folder/<archive-file>. Parameters description in first command example. Plus:
- x: Extract archive
- C: Switch into directory

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

### Restart unix system

```
sudo shutdown -r now
```

### Show IP address

```
ip addr show
```
