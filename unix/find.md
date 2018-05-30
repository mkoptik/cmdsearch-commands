# find commands

### Find file by name

```
find <search-root-path> -name "<file-name-pattern>" -print
```

### Find files created today

```
find <path> -daystart -ctime 0 -print
```

- **-daystart** Measure times from the beginning of today rather than from 24 hours ago. This option only affects tests which appear later on the command line.
- **-ctime** File's status was last changed n*24 hours ago. See the comments for -atime to understand how rounding affects the interpretation of file status change times
- **-print** True; print the full file name on the standard output, followed by a newline. If you are piping the output of find into another program and there is the faintest possibility that the files which you are searching for might contain a newline, then you should seriously consider using the -print0 option instead of -print. See the UNUSUAL FILENAMES section for information about how unusual characters in filenames are handled.
