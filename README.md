# rr232x-linux-src

## About

This is the open-source Linux driver for the HighPoint RocketRaid 232x controller.

The origin open-source driver can be downloaded from the [official Highpoint website](http://www.highpoint-tech.com/USA_new/rr2300_download.htm).

## Kernel 3.x patch

The origin driver runs only on Linux systems with Kernel 2.4 and 2.6.
To support newer Linux distributions with a 3.x kernel, the source code has been patched.

You can find the origin source in the `src/` directory, while the patched source is in the `patched/` directory.

Kudos to __camper2__ in the [Ubuntu Forums](http://ubuntuforums.org/showthread.php?t=1899544&page=2&p=12802693#post12802693), because he provided the patch.

## Build

Install required build packages and kernel headers:

```bash
apt-get -y install build-essential checkinstall linux-headers-$(uname -r)
```

Clone git repo:

```bash
cd /usr/src
git clone https://github.com/confirm-it-solutions/rr232x-linux-src.git
```

CD into patched directory and compile driver:

```bash
cd rr232x-linux-src/patched/product/rr232x/linux/
make install
```

Load kernel module:

```bash
modprobe rr232x
```
