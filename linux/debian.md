# Debian and debian based distro specific command
## Identify which package a binary installed from
So let say you have want to know which package install a certain package, you can use dpkg -S /usr/bin/binary. 

Here is an example for a binary called /usr/bin/pyvenv-3.4
```

$ dpkg -S /usr/bin/pyvenv-3.4
python3.4: /usr/bin/pyvenv-3.4

```

From here you can see that this is installed from python3.4 package