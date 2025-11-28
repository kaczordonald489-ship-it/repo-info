# `rabbitmq:4.2.1-management-alpine`

## Docker Metadata

- Image ID: `sha256:013c1914c40bdbc64bc52eec8053357fad314a51349b9f5c04ff1d86df5e315c`
- Created: `2025-11-18T05:59:41.887250254Z`
- Virtual Size: ~ 200.75 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["docker-entrypoint.sh"]`
- Command: `["rabbitmq-server"]`
- Environment:
  - `PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `ERLANG_INSTALL_PATH_PREFIX=/opt/erlang`
  - `OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl`
  - `RABBITMQ_DATA_DIR=/var/lib/rabbitmq`
  - `RABBITMQ_VERSION=4.2.1`
  - `RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA`
  - `RABBITMQ_HOME=/opt/rabbitmq`
  - `HOME=/var/lib/rabbitmq`
  - `LANG=C.UTF-8`
  - `LANGUAGE=C.UTF-8`
  - `LC_ALL=C.UTF-8`

## `apk` (`.apk`-based packages)

### `apk` package: `alpine-baselayout`

```console
alpine-baselayout-3.7.0-r0 description:
Alpine base dir structure and init scripts

alpine-baselayout-3.7.0-r0 webpage:
https://git.alpinelinux.org/cgit/aports/tree/main/alpine-baselayout

alpine-baselayout-3.7.0-r0 installed size:
6441 B

alpine-baselayout-3.7.0-r0 license:
GPL-2.0-only

```

### `apk` package: `alpine-baselayout-data`

```console
alpine-baselayout-data-3.7.0-r0 description:
Alpine base dir structure and init scripts

alpine-baselayout-data-3.7.0-r0 webpage:
https://git.alpinelinux.org/cgit/aports/tree/main/alpine-baselayout

alpine-baselayout-data-3.7.0-r0 installed size:
18 KiB

alpine-baselayout-data-3.7.0-r0 license:
GPL-2.0-only

```

### `apk` package: `alpine-keys`

```console
alpine-keys-2.5-r0 description:
Public keys for Alpine Linux packages

alpine-keys-2.5-r0 webpage:
https://alpinelinux.org

alpine-keys-2.5-r0 installed size:
13 KiB

alpine-keys-2.5-r0 license:
MIT

```

### `apk` package: `alpine-release`

```console
alpine-release-3.22.2-r0 description:
Alpine release data

alpine-release-3.22.2-r0 webpage:
https://alpinelinux.org

alpine-release-3.22.2-r0 installed size:
343 B

alpine-release-3.22.2-r0 license:
MIT

```

### `apk` package: `apk-tools`

```console
apk-tools-2.14.9-r3 description:
Alpine Package Keeper - package manager for alpine

apk-tools-2.14.9-r3 webpage:
https://gitlab.alpinelinux.org/alpine/apk-tools

apk-tools-2.14.9-r3 installed size:
68 KiB

apk-tools-2.14.9-r3 license:
GPL-2.0-only

```

### `apk` package: `bash`

```console
bash-5.2.37-r0 description:
The GNU Bourne Again shell

bash-5.2.37-r0 webpage:
https://www.gnu.org/software/bash/bash.html

bash-5.2.37-r0 installed size:
1243 KiB

bash-5.2.37-r0 license:
GPL-3.0-or-later

```

### `apk` package: `busybox`

```console
busybox-1.37.0-r19 description:
Size optimized toolbox of many common UNIX utilities

busybox-1.37.0-r19 webpage:
https://busybox.net/

busybox-1.37.0-r19 installed size:
798 KiB

busybox-1.37.0-r19 license:
GPL-2.0-only

```

### `apk` package: `busybox-binsh`

```console
busybox-binsh-1.37.0-r19 description:
busybox ash /bin/sh

busybox-binsh-1.37.0-r19 webpage:
https://busybox.net/

busybox-binsh-1.37.0-r19 installed size:
1 B

busybox-binsh-1.37.0-r19 license:
GPL-2.0-only

```

### `apk` package: `ca-certificates-bundle`

```console
ca-certificates-bundle-20250911-r0 description:
Pre generated bundle of Mozilla certificates

ca-certificates-bundle-20250911-r0 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-bundle-20250911-r0 installed size:
214 KiB

ca-certificates-bundle-20250911-r0 license:
MPL-2.0 AND MIT

```

### `apk` package: `gdbm`

```console
gdbm-1.24-r0 description:
GNU dbm is a set of database routines that use extensible hashing

gdbm-1.24-r0 webpage:
https://www.gnu.org/software/gdbm/

gdbm-1.24-r0 installed size:
67 KiB

gdbm-1.24-r0 license:
GPL-3.0-or-later

```

### `apk` package: `libapk2`

```console
libapk2-2.14.9-r3 description:
Alpine Package Keeper - package manager for alpine

libapk2-2.14.9-r3 webpage:
https://gitlab.alpinelinux.org/alpine/apk-tools

libapk2-2.14.9-r3 installed size:
179 KiB

libapk2-2.14.9-r3 license:
GPL-2.0-only

```

### `apk` package: `libbz2`

```console
libbz2-1.0.8-r6 description:
Shared library for bz2

libbz2-1.0.8-r6 webpage:
https://sourceware.org/bzip2/

libbz2-1.0.8-r6 installed size:
72 KiB

libbz2-1.0.8-r6 license:
bzip2-1.0.6

```

### `apk` package: `libcrypto3`

```console
libcrypto3-3.5.4-r0 description:
Crypto library from openssl

libcrypto3-3.5.4-r0 webpage:
https://www.openssl.org/

libcrypto3-3.5.4-r0 installed size:
5091 KiB

libcrypto3-3.5.4-r0 license:
Apache-2.0

```

### `apk` package: `libexpat`

```console
libexpat-2.7.3-r0 description:
XML Parser library written in C (libraries)

libexpat-2.7.3-r0 webpage:
https://libexpat.github.io/

libexpat-2.7.3-r0 installed size:
133 KiB

libexpat-2.7.3-r0 license:
MIT

```

### `apk` package: `libffi`

```console
libffi-3.4.8-r0 description:
portable, high level programming interface to various calling conventions.

libffi-3.4.8-r0 webpage:
https://sourceware.org/libffi/

libffi-3.4.8-r0 installed size:
38 KiB

libffi-3.4.8-r0 license:
MIT

```

### `apk` package: `libgcc`

```console
libgcc-14.2.0-r6 description:
GNU C compiler runtime libraries

libgcc-14.2.0-r6 webpage:
https://gcc.gnu.org

libgcc-14.2.0-r6 installed size:
169 KiB

libgcc-14.2.0-r6 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libintl`

```console
libintl-0.24.1-r0 description:
GNU gettext runtime library

libintl-0.24.1-r0 webpage:
https://www.gnu.org/software/gettext/gettext.html

libintl-0.24.1-r0 installed size:
133 KiB

libintl-0.24.1-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `libncursesw`

```console
libncursesw-6.5_p20250503-r0 description:
Console display library (libncursesw)

libncursesw-6.5_p20250503-r0 webpage:
https://invisible-island.net/ncurses/

libncursesw-6.5_p20250503-r0 installed size:
334 KiB

libncursesw-6.5_p20250503-r0 license:
X11

```

### `apk` package: `libpanelw`

```console
libpanelw-6.5_p20250503-r0 description:
Console display library (libpanelw)

libpanelw-6.5_p20250503-r0 webpage:
https://invisible-island.net/ncurses/

libpanelw-6.5_p20250503-r0 installed size:
17 KiB

libpanelw-6.5_p20250503-r0 license:
X11

```

### `apk` package: `libproc2`

```console
libproc2-4.0.4-r3 description:
Library for monitoring system and processes

libproc2-4.0.4-r3 webpage:
https://gitlab.com/procps-ng/procps

libproc2-4.0.4-r3 installed size:
139 KiB

libproc2-4.0.4-r3 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libssl3`

```console
libssl3-3.5.4-r0 description:
SSL shared libraries

libssl3-3.5.4-r0 webpage:
https://www.openssl.org/

libssl3-3.5.4-r0 installed size:
823 KiB

libssl3-3.5.4-r0 license:
Apache-2.0

```

### `apk` package: `libstdc++`

```console
libstdc++-14.2.0-r6 description:
GNU C++ standard runtime library

libstdc++-14.2.0-r6 webpage:
https://gcc.gnu.org

libstdc++-14.2.0-r6 installed size:
2706 KiB

libstdc++-14.2.0-r6 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `mpdecimal`

```console
mpdecimal-4.0.1-r0 description:
complete implementation of the General Decimal Arithmetic Specification

mpdecimal-4.0.1-r0 webpage:
https://www.bytereef.org/mpdecimal/index.html

mpdecimal-4.0.1-r0 installed size:
187 KiB

mpdecimal-4.0.1-r0 license:
BSD-2-Clause

```

### `apk` package: `musl`

```console
musl-1.2.5-r10 description:
the musl c library (libc) implementation

musl-1.2.5-r10 webpage:
https://musl.libc.org/

musl-1.2.5-r10 installed size:
646 KiB

musl-1.2.5-r10 license:
MIT

```

### `apk` package: `musl-utils`

```console
musl-utils-1.2.5-r10 description:
the musl c library (libc) implementation

musl-utils-1.2.5-r10 webpage:
https://musl.libc.org/

musl-utils-1.2.5-r10 installed size:
54 KiB

musl-utils-1.2.5-r10 license:
MIT AND BSD-2-Clause AND GPL-2.0-or-later

```

### `apk` package: `ncurses-terminfo-base`

```console
ncurses-terminfo-base-6.5_p20250503-r0 description:
Descriptions of common terminals

ncurses-terminfo-base-6.5_p20250503-r0 webpage:
https://invisible-island.net/ncurses/

ncurses-terminfo-base-6.5_p20250503-r0 installed size:
98 KiB

ncurses-terminfo-base-6.5_p20250503-r0 license:
X11

```

### `apk` package: `procps-ng`

```console
procps-ng-4.0.4-r3 description:
Utilities for monitoring your system and processes on your system

procps-ng-4.0.4-r3 webpage:
https://gitlab.com/procps-ng/procps

procps-ng-4.0.4-r3 installed size:
521 KiB

procps-ng-4.0.4-r3 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `pyc`

```console
pyc-3.12.12-r0 description:
Meta package for pulling in all -pyc packages

pyc-3.12.12-r0 webpage:
https://www.python.org/

pyc-3.12.12-r0 installed size:
0 B

pyc-3.12.12-r0 license:
PSF-2.0

```

### `apk` package: `python3`

```console
python3-3.12.12-r0 description:
High-level scripting language

python3-3.12.12-r0 webpage:
https://www.python.org/

python3-3.12.12-r0 installed size:
22 MiB

python3-3.12.12-r0 license:
PSF-2.0

```

### `apk` package: `python3-pyc`

```console
python3-pyc-3.12.12-r0 description:
High-level scripting language (install .pyc cache files)

python3-pyc-3.12.12-r0 webpage:
https://www.python.org/

python3-pyc-3.12.12-r0 installed size:
0 B

python3-pyc-3.12.12-r0 license:
PSF-2.0

```

### `apk` package: `python3-pycache-pyc0`

```console
python3-pycache-pyc0-3.12.12-r0 description:
High-level scripting language (.pyc pycache files)

python3-pycache-pyc0-3.12.12-r0 webpage:
https://www.python.org/

python3-pycache-pyc0-3.12.12-r0 installed size:
10 MiB

python3-pycache-pyc0-3.12.12-r0 license:
PSF-2.0

```

### `apk` package: `readline`

```console
readline-8.2.13-r1 description:
GNU readline library

readline-8.2.13-r1 webpage:
https://tiswww.cwru.edu/php/chet/readline/rltop.html

readline-8.2.13-r1 installed size:
280 KiB

readline-8.2.13-r1 license:
GPL-3.0-or-later

```

### `apk` package: `scanelf`

```console
scanelf-1.3.8-r1 description:
Scan ELF binaries for stuff

scanelf-1.3.8-r1 webpage:
https://wiki.gentoo.org/wiki/Hardened/PaX_Utilities

scanelf-1.3.8-r1 installed size:
65 KiB

scanelf-1.3.8-r1 license:
GPL-2.0-only

```

### `apk` package: `skalibs-libs`

```console
skalibs-libs-2.14.4.0-r0 description:
Set of general-purpose C programming libraries for skarnet.org software. (libraries)

skalibs-libs-2.14.4.0-r0 webpage:
https://skarnet.org/software/skalibs/

skalibs-libs-2.14.4.0-r0 installed size:
191 KiB

skalibs-libs-2.14.4.0-r0 license:
ISC

```

### `apk` package: `sqlite-libs`

```console
sqlite-libs-3.49.2-r1 description:
C library that implements an SQL database engine (libraries)

sqlite-libs-3.49.2-r1 webpage:
https://www.sqlite.org/

sqlite-libs-3.49.2-r1 installed size:
1553 KiB

sqlite-libs-3.49.2-r1 license:
blessing

```

### `apk` package: `ssl_client`

```console
ssl_client-1.37.0-r19 description:
External ssl_client for busybox wget

ssl_client-1.37.0-r19 webpage:
https://busybox.net/

ssl_client-1.37.0-r19 installed size:
14 KiB

ssl_client-1.37.0-r19 license:
GPL-2.0-only

```

### `apk` package: `su-exec`

```console
su-exec-0.2-r3 description:
switch user and group id, setgroups and exec

su-exec-0.2-r3 webpage:
https://github.com/ncopa/su-exec

su-exec-0.2-r3 installed size:
13 KiB

su-exec-0.2-r3 license:
MIT

```

### `apk` package: `tzdata`

```console
tzdata-2025b-r0 description:
Timezone data

tzdata-2025b-r0 webpage:
https://www.iana.org/time-zones

tzdata-2025b-r0 installed size:
435 KiB

tzdata-2025b-r0 license:
Public-Domain

```

### `apk` package: `utmps-libs`

```console
utmps-libs-0.1.3.1-r0 description:
A secure utmp/wtmp implementation (libraries)

utmps-libs-0.1.3.1-r0 webpage:
https://skarnet.org/software/utmps/

utmps-libs-0.1.3.1-r0 installed size:
17 KiB

utmps-libs-0.1.3.1-r0 license:
ISC

```

### `apk` package: `xz-libs`

```console
xz-libs-5.8.1-r0 description:
Library and CLI tools for XZ and LZMA compressed files (libraries)

xz-libs-5.8.1-r0 webpage:
https://tukaani.org/xz/

xz-libs-5.8.1-r0 installed size:
225 KiB

xz-libs-5.8.1-r0 license:
GPL-2.0-or-later AND 0BSD AND Public-Domain AND LGPL-2.1-or-later

```

### `apk` package: `zlib`

```console
zlib-1.3.1-r2 description:
A compression/decompression Library

zlib-1.3.1-r2 webpage:
https://zlib.net/

zlib-1.3.1-r2 installed size:
101 KiB

zlib-1.3.1-r2 license:
Zlib

```
