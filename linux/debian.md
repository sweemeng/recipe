# Debian and debian based distro specific command
## Identify which package a binary installed from
So let say you have want to know which package install a certain package, you can use dpkg -S /usr/bin/binary. 

Here is an example for a binary called /usr/bin/pyvenv-3.4
```

$ dpkg -S /usr/bin/pyvenv-3.4
python3.4: /usr/bin/pyvenv-3.4

```

From here you can see that this is installed from python3.4 package

## Determine the installed version and source of installation of a package in debian
So say you want to know what is the version of app you installed in debian, and you want to know where it is installed form. You can use `apt-cache policy`. 

We use that because I used to work in an where we maintain our own debian repository, and have our own patch to an open source project. We want to see what is the priority of our own package to installed and whether the source is set correctly. 

Here I use the example firefox. As you can see, there is the source, and the priority of package that get installed. 
```
$  apt-cache policy firefox
firefox:
  Installed: 34.0+build2-0ubuntu0.14.04.1
  Candidate: 35.0+build3-0ubuntu0.14.04.2
  Version table:
     35.0+build3-0ubuntu0.14.04.2 0
        500 http://archive.ubuntu.com/ubuntu/ trusty-updates/main amd64 Packages
        500 http://archive.ubuntu.com/ubuntu/ trusty-security/main amd64 Packages
 *** 34.0+build2-0ubuntu0.14.04.1 0
        100 /var/lib/dpkg/status
     28.0+build2-0ubuntu2 0
        500 http://archive.ubuntu.com/ubuntu/ trusty/main amd64 Packages
```
