# Bash command
## setting environment for a command once
There is time we don't want to export environment variable, but only use it once. What you do is set the variable once 
```
VARIABLE=A command
```

This is actually useful when debugging vagrant, but I am lazy at setting variable. Vagrant set logging in `VAGRANT_LOG=log_level`
```
VAGRANT_LOG=debug vagrant up
```