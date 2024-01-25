# Basic scripts

### Open file using TextEdit.app
```
set Target_Filepath to POSIX file "/Users/username/path/file.txt"
tell application "TextEdit" to open Target_Filepath
tell application "TextEdit" to activate
```
### Open specific folder using Finder.app
```
do shell script "open /Users/username/path"
```
### Open Google Chrome in incognito mode
```
do shell script "open -a 'Google Chrome' --args --incognito "
tell application "Google Chrome" to activate
```
### Open Trash 
```
do shell script "open ~/.Trash"
```
### Open some application
```
do shell script "open -a 'Visual Studio Code'"
```


# Enable traffic dump (wireshark, tcpdump, etc.)

### CHOWN bpf to user
```
cd /dev
ls -lh | grep bpf
chown username:admin bpf*
```

### Check settings

```
ls -lh | grep bpf
```

### Revert to default settings

```
chown root:wheel bpf*
```
