# Android Debug Bridge

### Input text from shell

```
adb shell input text '<text-to-input>'
```

Useful for entering long text

### Make screenshot and save it to file on host

```
adb exec-out screencap -p > <output-file>.png
```

### Get log with logcat by process name

```
adb logcat --pid=$(adb shell pidof -s <process_name>)
```
