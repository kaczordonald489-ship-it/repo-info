# `eclipse-mosquitto:2.0.22`

## Docker Metadata

- Image ID: `sha256:0745ced90756f8f0e75e16b872c7f4e281ea37e1dd93ba101880152bb31a98a6`
- Created: `2025-11-14T17:51:17.165825884Z`
- Virtual Size: ~ 10.37 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/docker-entrypoint.sh"]`
- Command: `["/usr/sbin/mosquitto","-c","/mosquitto/config/mosquitto.conf"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `VERSION=2.0.22`
  - `DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68`
  - `GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7`
  - `LWS_VERSION=4.2.1`
  - `LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51`
- Labels:
  - `description=Eclipse Mosquitto MQTT Broker`
  - `maintainer=Roger Light <roger@atchoo.org>`

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

### `apk` package: `ca-certificates`

```console
ca-certificates-20250911-r0 description:
Common CA certificates PEM files from Mozilla

ca-certificates-20250911-r0 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-20250911-r0 installed size:
248 KiB

ca-certificates-20250911-r0 license:
MPL-2.0 AND MIT

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

### `apk` package: `cjson`

```console
cjson-1.7.19-r0 description:
Lighweight JSON parser in C

cjson-1.7.19-r0 webpage:
https://github.com/DaveGamble/cJSON

cjson-1.7.19-r0 installed size:
29 KiB

cjson-1.7.19-r0 license:
MIT

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
