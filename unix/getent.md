# getent

The getent command displays entries from databases supported by the Name Service Switch libraries, which are configured in /etc/nsswitch.conf. If one or more key arguments are provided, then only the entries that match the supplied keys will be displayed. Otherwise, if no key is provided, all entries will be displayed (unless the database does not support enumeration).

### resolve IP address of a host

```
getent hosts <host-name> | awk '{ print $1 }'
```
