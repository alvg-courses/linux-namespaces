Simple example functions for understanding different aspects of Linux namespaces.
Each folder illustrates different namespace isolation methods.

1. UTS namespace
2. User ID namespace
3. Mount and PID namespace
4. Network Namespace

Primary commands corresponding to namespace usage are clone with set of flags, and
unshare and setns. Feel free to look these up on the internet. Especially the man pages.

Understanding each aspect of namespace will require one to check which commands to run and
figure out outputs in each scenario, expectedly. Use all sorts of commands inside these (child) shells.

We use $ symbol to denote parent shell and % for child (or the sandboxed) shell.

## Minimal Alpine Linux installation.

Create rootfs in respective folders i.e. mount and network before running the respective executables.
```
$ wget http://dl-cdn.alpinelinux.org/alpine/v3.10/releases/x86_64/alpine-minirootfs-3.10.1-x86_64.tar.gz
$ mkdir rootfs
$ tar -xzf alpine-minirootfs-3.10.1-x86_64.tar.gz -C rootfs
```

Credits: u/iffyio.
