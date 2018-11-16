# General unix commands

### Print full path of current directory

```
pwd
```

The pwd command is a command line utility for printing the current working directory. It will print the full system path of the current working directory to standard output.

### Find files by name and sort results by name

```
find <location> -name "<file-name>" -print | sort
```

### Get graphic card name

```
lspci | grep VGA
```

Before running this command, update list of PCI IDs via sudo update-pciids

### Get external IP address

```
curl ipinfo.io/ip
```

### Delete all directories by name

```
find -type d -name <directory-name> -exec rm -rf {} \;
```

### Get free (available) and used memory

```
free -m
```

### Search text in files recursively, ignoring case

```
grep -iR '<text-to-search>'
```

### Add or update symlink

```
sudo ln -sfn <target-path> <path-to-symlink>
```

### Install .deb package

```
sudo dpkg -i <path-to-package>.deb && sudo apt-get install -f
```

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
### List listening ports with program name / PID

```
netstat -tulpn
```


### Unzip file to destination

```
unzip -d <destination-directory> <zip-file>
```

### Append directory to PATH variable

```
export PATH=$PATH:<directory-to-append>
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

### Set permissions to file or directory

```
chmod u=rwx,g=rx,o=r <file-or-directory>
```

u - user, g - group, o - others, r - read, w - write, x - execute

### List repositories used by apt

```
grep ^ /etc/apt/sources.list /etc/apt/sources.list.d/*
```

### Add current user to a group

```
sudo adduser $USER <group-name>
```

### Change owner of all files in directory

```
chown <user>:<group> <directory>/*
```

### Get text length

```
expr length "<text>"
```

### Remove symlink

```
unlink <link>
```

### Replace all text occurences in a file

```
sed -i -e 's/<search>/<replace>/g' <file>
```

### Replace all text occurences in a file with a environment variable

```
sed -i -e 's/<search>/'"$<ENV_VARIABLE_NAME>"'/g' <file>
```
