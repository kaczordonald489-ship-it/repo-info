# `friendica:2024.12-fpm-alpine`

## Docker Metadata

- Image ID: `sha256:628eb132a839ede8fff99c00733b15a1281bcac1d0adb23b2ea35b72c254522e`
- Created: `2025-11-20T20:46:35.124518248Z`
- Virtual Size: ~ 270.05 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/entrypoint.sh"]`
- Command: `["php-fpm"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c`
  - `PHP_INI_DIR=/usr/local/etc/php`
  - `PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64`
  - `PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64`
  - `PHP_LDFLAGS=-Wl,-O1 -pie`
  - `GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA`
  - `PHP_VERSION=8.3.28`
  - `PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz`
  - `PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc`
  - `PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326`
  - `GOSU_VERSION=1.17`
  - `PHP_MEMORY_LIMIT=512M`
  - `PHP_UPLOAD_LIMIT=512M`
  - `FRIENDICA_SYSLOG_FLAGS=39`
  - `FRIENDICA_VERSION=2024.12`
  - `FRIENDICA_ADDONS=2024.12`
  - `FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e`
  - `FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5`

## `apk` (`.apk`-based packages)

### `apk` package: `acl-libs`

```console
acl-libs-2.3.2-r1 description:
Access control list utilities (libraries)

acl-libs-2.3.2-r1 webpage:
https://savannah.nongnu.org/projects/acl

acl-libs-2.3.2-r1 installed size:
33 KiB

acl-libs-2.3.2-r1 license:
LGPL-2.1-or-later AND GPL-2.0-or-later

```

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

### `apk` package: `argon2-libs`

```console
argon2-libs-20190702-r5 description:
The password hash Argon2, winner of PHC (libraries)

argon2-libs-20190702-r5 webpage:
https://github.com/P-H-C/phc-winner-argon2

argon2-libs-20190702-r5 installed size:
37 KiB

argon2-libs-20190702-r5 license:
Apache-2.0 OR CC0-1.0

```

### `apk` package: `brotli-libs`

```console
brotli-libs-1.1.0-r2 description:
Generic lossless compressor (libraries)

brotli-libs-1.1.0-r2 webpage:
https://github.com/google/brotli

brotli-libs-1.1.0-r2 installed size:
913 KiB

brotli-libs-1.1.0-r2 license:
MIT

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

### `apk` package: `c-ares`

```console
c-ares-1.34.5-r0 description:
Asynchronous DNS/names resolver library

c-ares-1.34.5-r0 webpage:
https://c-ares.org/

c-ares-1.34.5-r0 installed size:
233 KiB

c-ares-1.34.5-r0 license:
MIT

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

### `apk` package: `curl`

```console
curl-8.14.1-r2 description:
URL retrival utility and library

curl-8.14.1-r2 webpage:
https://curl.se/

curl-8.14.1-r2 installed size:
260 KiB

curl-8.14.1-r2 license:
curl

```

### `apk` package: `fftw-double-libs`

```console
fftw-double-libs-3.3.10-r6 description:
Discrete Fourier transform (DFT) library

fftw-double-libs-3.3.10-r6 webpage:
http://www.fftw.org/

fftw-double-libs-3.3.10-r6 installed size:
2031 KiB

fftw-double-libs-3.3.10-r6 license:
GPL-2.0-or-later

```

### `apk` package: `fontconfig`

```console
fontconfig-2.15.0-r3 description:
Library for configuring and customizing font access

fontconfig-2.15.0-r3 webpage:
https://www.freedesktop.org/wiki/Software/fontconfig

fontconfig-2.15.0-r3 installed size:
515 KiB

fontconfig-2.15.0-r3 license:
MIT

```

### `apk` package: `freetype`

```console
freetype-2.13.3-r0 description:
TrueType font rendering library

freetype-2.13.3-r0 webpage:
https://www.freetype.org/

freetype-2.13.3-r0 installed size:
646 KiB

freetype-2.13.3-r0 license:
FTL OR GPL-2.0-or-later

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

### `apk` package: `gmp`

```console
gmp-6.3.0-r3 description:
free library for arbitrary precision arithmetic

gmp-6.3.0-r3 webpage:
https://gmplib.org/

gmp-6.3.0-r3 installed size:
417 KiB

gmp-6.3.0-r3 license:
LGPL-3.0-or-later OR GPL-2.0-or-later

```

### `apk` package: `gnu-libiconv-libs`

```console
gnu-libiconv-libs-1.17-r2 description:
GNU charset conversion library for libc which doesn't implement it (libraries)

gnu-libiconv-libs-1.17-r2 webpage:
https://www.gnu.org/software/libiconv

gnu-libiconv-libs-1.17-r2 installed size:
1047 KiB

gnu-libiconv-libs-1.17-r2 license:
LGPL-2.1-or-later

```

### `apk` package: `icu-data-en`

```console
icu-data-en-76.1-r1 description:
Stripped down ICU data with only en_US/GB locale and no legacy charset converters

icu-data-en-76.1-r1 webpage:
https://icu.unicode.org/

icu-data-en-76.1-r1 installed size:
2938 KiB

icu-data-en-76.1-r1 license:
ICU

```

### `apk` package: `icu-libs`

```console
icu-libs-76.1-r1 description:
International Components for Unicode library (libraries)

icu-libs-76.1-r1 webpage:
https://icu.unicode.org/

icu-libs-76.1-r1 installed size:
4659 KiB

icu-libs-76.1-r1 license:
ICU

```

### `apk` package: `imagemagick`

```console
imagemagick-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats

imagemagick-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-7.1.2.8-r0 installed size:
3662 KiB

imagemagick-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `imagemagick-jpeg`

```console
imagemagick-jpeg-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (JPEG support modules)

imagemagick-jpeg-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-jpeg-7.1.2.8-r0 installed size:
54 KiB

imagemagick-jpeg-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `imagemagick-libs`

```console
imagemagick-libs-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (libraries)

imagemagick-libs-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-libs-7.1.2.8-r0 installed size:
4265 KiB

imagemagick-libs-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `imagemagick-webp`

```console
imagemagick-webp-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (WebP support modules)

imagemagick-webp-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-webp-7.1.2.8-r0 installed size:
30 KiB

imagemagick-webp-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `keyutils-libs`

```console
keyutils-libs-1.6.3-r4 description:
Key utilities library

keyutils-libs-1.6.3-r4 webpage:
https://people.redhat.com/~dhowells/keyutils/

keyutils-libs-1.6.3-r4 installed size:
17 KiB

keyutils-libs-1.6.3-r4 license:
GPL-2.0-or-later AND LGPL-2.0-or-later

```

### `apk` package: `krb5-conf`

```console
krb5-conf-1.0-r2 description:
Shared krb5.conf for both MIT krb5 and heimdal

krb5-conf-1.0-r2 webpage:
https://web.mit.edu/kerberos/www/

krb5-conf-1.0-r2 installed size:
450 B

krb5-conf-1.0-r2 license:
MIT

```

### `apk` package: `krb5-libs`

```console
krb5-libs-1.21.3-r0 description:
The shared libraries used by Kerberos 5

krb5-libs-1.21.3-r0 webpage:
https://web.mit.edu/kerberos/www/

krb5-libs-1.21.3-r0 installed size:
1751 KiB

krb5-libs-1.21.3-r0 license:
MIT

```

### `apk` package: `lcms2`

```console
lcms2-2.16-r0 description:
Color Management Engine

lcms2-2.16-r0 webpage:
https://www.littlecms.com

lcms2-2.16-r0 installed size:
328 KiB

lcms2-2.16-r0 license:
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

### `apk` package: `libbsd`

```console
libbsd-0.12.2-r0 description:
commonly-used BSD functions not implemented by all libcs

libbsd-0.12.2-r0 webpage:
https://libbsd.freedesktop.org/

libbsd-0.12.2-r0 installed size:
62 KiB

libbsd-0.12.2-r0 license:
BSD-3-Clause

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

### `apk` package: `libcom_err`

```console
libcom_err-1.47.2-r2 description:
Common error description library

libcom_err-1.47.2-r2 webpage:
https://e2fsprogs.sourceforge.net/

libcom_err-1.47.2-r2 installed size:
17 KiB

libcom_err-1.47.2-r2 license:
GPL-2.0-or-later AND LGPL-2.0-or-later AND BSD-3-Clause AND MIT

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

### `apk` package: `libcurl`

```console
libcurl-8.14.1-r2 description:
The multiprotocol file transfer library

libcurl-8.14.1-r2 webpage:
https://curl.se/

libcurl-8.14.1-r2 installed size:
669 KiB

libcurl-8.14.1-r2 license:
curl

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

### `apk` package: `libgcrypt`

```console
libgcrypt-1.10.3-r1 description:
General purpose crypto library based on the code used in GnuPG

libgcrypt-1.10.3-r1 webpage:
https://www.gnupg.org/

libgcrypt-1.10.3-r1 installed size:
1157 KiB

libgcrypt-1.10.3-r1 license:
LGPL-2.1-or-later AND GPL-2.0-or-later

```

### `apk` package: `libgomp`

```console
libgomp-14.2.0-r6 description:
GCC shared-memory parallel programming API library

libgomp-14.2.0-r6 webpage:
https://gcc.gnu.org

libgomp-14.2.0-r6 installed size:
322 KiB

libgomp-14.2.0-r6 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libgpg-error`

```console
libgpg-error-1.55-r0 description:
Support library for libgcrypt

libgpg-error-1.55-r0 webpage:
https://www.gnupg.org/

libgpg-error-1.55-r0 installed size:
168 KiB

libgpg-error-1.55-r0 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libgsasl`

```console
libgsasl-2.2.2-r0 description:
An implementation of the Simple Authentication and Security Layer framework

libgsasl-2.2.2-r0 webpage:
https://www.gnu.org/software/gsasl/

libgsasl-2.2.2-r0 installed size:
123 KiB

libgsasl-2.2.2-r0 license:
LGPL-2.0-or-later

```

### `apk` package: `libidn`

```console
libidn-1.42-r0 description:
Encode/Decode library for internationalized domain names

libidn-1.42-r0 webpage:
https://www.gnu.org/software/libidn

libidn-1.42-r0 installed size:
253 KiB

libidn-1.42-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `libidn2`

```console
libidn2-2.3.7-r0 description:
Encode/Decode library for internationalized domain names

libidn2-2.3.7-r0 webpage:
https://www.gnu.org/software/libidn#libidn2

libidn2-2.3.7-r0 installed size:
193 KiB

libidn2-2.3.7-r0 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

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

### `apk` package: `libjpeg-turbo`

```console
libjpeg-turbo-3.1.0-r0 description:
Accelerated baseline JPEG compression and decompression library

libjpeg-turbo-3.1.0-r0 webpage:
https://libjpeg-turbo.org/

libjpeg-turbo-3.1.0-r0 installed size:
629 KiB

libjpeg-turbo-3.1.0-r0 license:
BSD-3-Clause AND IJG AND Zlib

```

### `apk` package: `libldap`

```console
libldap-2.6.8-r0 description:
OpenLDAP libraries

libldap-2.6.8-r0 webpage:
https://www.openldap.org/

libldap-2.6.8-r0 installed size:
365 KiB

libldap-2.6.8-r0 license:
OLDAP-2.8

```

### `apk` package: `libltdl`

```console
libltdl-2.5.4-r1 description:
Runtime libraries for GNU Libtool Dynamic Module Loader

libltdl-2.5.4-r1 webpage:
https://www.gnu.org/software/libtool

libltdl-2.5.4-r1 installed size:
37 KiB

libltdl-2.5.4-r1 license:
LGPL-2.0-or-later AND GPL-2.0-or-later

```

### `apk` package: `libmd`

```console
libmd-1.1.0-r0 description:
Message Digest functions from BSD systems

libmd-1.1.0-r0 webpage:
https://www.hadrons.org/software/libmd/

libmd-1.1.0-r0 installed size:
49 KiB

libmd-1.1.0-r0 license:
BSD-3-Clause AND BSD-2-Clause AND ISC AND Beerware AND Public Domain

```

### `apk` package: `libmemcached-libs`

```console
libmemcached-libs-1.1.4-r1 description:
Client library and command line tools for memcached server (resurrected) (libraries)

libmemcached-libs-1.1.4-r1 webpage:
https://github.com/awesomized/libmemcached

libmemcached-libs-1.1.4-r1 installed size:
239 KiB

libmemcached-libs-1.1.4-r1 license:
BSD-3-Clause

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

### `apk` package: `libpng`

```console
libpng-1.6.47-r0 description:
Portable Network Graphics library

libpng-1.6.47-r0 webpage:
http://www.libpng.org

libpng-1.6.47-r0 installed size:
181 KiB

libpng-1.6.47-r0 license:
Libpng

```

### `apk` package: `libpsl`

```console
libpsl-0.21.5-r3 description:
C library for the Publix Suffix List

libpsl-0.21.5-r3 webpage:
https://rockdaboot.github.io/libpsl

libpsl-0.21.5-r3 installed size:
73 KiB

libpsl-0.21.5-r3 license:
MIT

```

### `apk` package: `libsasl`

```console
libsasl-2.1.28-r8 description:
Cyrus Simple Authentication and Security Layer (SASL) library

libsasl-2.1.28-r8 webpage:
https://www.cyrusimap.org/sasl/

libsasl-2.1.28-r8 installed size:
163 KiB

libsasl-2.1.28-r8 license:
BSD-3-Clause-Attribution AND BSD-4-Clause

```

### `apk` package: `libsharpyuv`

```console
libsharpyuv-1.5.0-r0 description:
Libraries for working with WebP images (libsharpyuv library)

libsharpyuv-1.5.0-r0 webpage:
https://developers.google.com/speed/webp

libsharpyuv-1.5.0-r0 installed size:
25 KiB

libsharpyuv-1.5.0-r0 license:
BSD-3-Clause

```

### `apk` package: `libsodium`

```console
libsodium-1.0.20-r0 description:
P(ortable|ackageable) NaCl-based crypto library

libsodium-1.0.20-r0 webpage:
https://github.com/jedisct1/libsodium

libsodium-1.0.20-r0 installed size:
339 KiB

libsodium-1.0.20-r0 license:
ISC

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

### `apk` package: `libunistring`

```console
libunistring-1.3-r0 description:
Library for manipulating Unicode strings and C strings

libunistring-1.3-r0 webpage:
https://www.gnu.org/software/libunistring/

libunistring-1.3-r0 installed size:
1857 KiB

libunistring-1.3-r0 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

```

### `apk` package: `libverto`

```console
libverto-0.3.2-r2 description:
Main loop abstraction library

libverto-0.3.2-r2 webpage:
https://github.com/latchset/libverto

libverto-0.3.2-r2 installed size:
21 KiB

libverto-0.3.2-r2 license:
MIT

```

### `apk` package: `libwebp`

```console
libwebp-1.5.0-r0 description:
Libraries for working with WebP images

libwebp-1.5.0-r0 webpage:
https://developers.google.com/speed/webp

libwebp-1.5.0-r0 installed size:
485 KiB

libwebp-1.5.0-r0 license:
BSD-3-Clause

```

### `apk` package: `libwebpdemux`

```console
libwebpdemux-1.5.0-r0 description:
Libraries for working with WebP images (libwebpdemux library)

libwebpdemux-1.5.0-r0 webpage:
https://developers.google.com/speed/webp

libwebpdemux-1.5.0-r0 installed size:
17 KiB

libwebpdemux-1.5.0-r0 license:
BSD-3-Clause

```

### `apk` package: `libwebpmux`

```console
libwebpmux-1.5.0-r0 description:
Libraries for working with WebP images (libwebpmux library)

libwebpmux-1.5.0-r0 webpage:
https://developers.google.com/speed/webp

libwebpmux-1.5.0-r0 installed size:
45 KiB

libwebpmux-1.5.0-r0 license:
BSD-3-Clause

```

### `apk` package: `libx11`

```console
libx11-1.8.11-r0 description:
X11 client-side library

libx11-1.8.11-r0 webpage:
https://xorg.freedesktop.org/

libx11-1.8.11-r0 installed size:
2275 KiB

libx11-1.8.11-r0 license:
X11

```

### `apk` package: `libxau`

```console
libxau-1.0.12-r0 description:
X11 authorisation library

libxau-1.0.12-r0 webpage:
https://xorg.freedesktop.org/

libxau-1.0.12-r0 installed size:
13 KiB

libxau-1.0.12-r0 license:
MIT

```

### `apk` package: `libxcb`

```console
libxcb-1.17.0-r0 description:
X11 client-side library

libxcb-1.17.0-r0 webpage:
https://xcb.freedesktop.org/

libxcb-1.17.0-r0 installed size:
966 KiB

libxcb-1.17.0-r0 license:
MIT

```

### `apk` package: `libxdmcp`

```console
libxdmcp-1.1.5-r1 description:
X11 Display Manager Control Protocol library

libxdmcp-1.1.5-r1 webpage:
https://xorg.freedesktop.org/

libxdmcp-1.1.5-r1 installed size:
25 KiB

libxdmcp-1.1.5-r1 license:
MIT

```

### `apk` package: `libxext`

```console
libxext-1.3.6-r2 description:
X11 miscellaneous extensions library

libxext-1.3.6-r2 webpage:
https://xorg.freedesktop.org/

libxext-1.3.6-r2 installed size:
66 KiB

libxext-1.3.6-r2 license:
MIT

```

### `apk` package: `libxml2`

```console
libxml2-2.13.9-r0 description:
XML parsing library, version 2

libxml2-2.13.9-r0 webpage:
https://gitlab.gnome.org/GNOME/libxml2

libxml2-2.13.9-r0 installed size:
1050 KiB

libxml2-2.13.9-r0 license:
MIT

```

### `apk` package: `libxxhash`

```console
libxxhash-0.8.3-r0 description:
Extremely fast non-cryptographic hash algorithm (libraries)

libxxhash-0.8.3-r0 webpage:
https://cyan4973.github.io/xxHash/

libxxhash-0.8.3-r0 installed size:
69 KiB

libxxhash-0.8.3-r0 license:
BSD-2-Clause

```

### `apk` package: `libzip`

```console
libzip-1.11.4-r0 description:
C library for manipulating zip archives

libzip-1.11.4-r0 webpage:
https://libzip.org/

libzip-1.11.4-r0 installed size:
102 KiB

libzip-1.11.4-r0 license:
BSD-3-Clause

```

### `apk` package: `linux-pam`

```console
linux-pam-1.7.0-r4 description:
Linux PAM (Pluggable Authentication Modules for Linux)

linux-pam-1.7.0-r4 webpage:
https://www.kernel.org/pub/linux/libs/pam

linux-pam-1.7.0-r4 installed size:
821 KiB

linux-pam-1.7.0-r4 license:
BSD-3-Clause

```

### `apk` package: `lz4-libs`

```console
lz4-libs-1.10.0-r0 description:
LZ4 is lossless compression algorithm with fast decoder @ multiple GB/s per core. (libraries)

lz4-libs-1.10.0-r0 webpage:
https://github.com/lz4/lz4

lz4-libs-1.10.0-r0 installed size:
145 KiB

lz4-libs-1.10.0-r0 license:
BSD-2-Clause AND GPL-2.0-or-later

```

### `apk` package: `msmtp`

```console
msmtp-1.8.28-r0 description:
SMTP client with a sendmail compatible interface

msmtp-1.8.28-r0 webpage:
https://marlam.de/msmtp/

msmtp-1.8.28-r0 installed size:
137 KiB

msmtp-1.8.28-r0 license:
GPL-3.0-or-later

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

### `apk` package: `nghttp2-libs`

```console
nghttp2-libs-1.65.0-r0 description:
HTTP/2 C client, server and proxy (libraries)

nghttp2-libs-1.65.0-r0 webpage:
https://nghttp2.org

nghttp2-libs-1.65.0-r0 installed size:
129 KiB

nghttp2-libs-1.65.0-r0 license:
MIT

```

### `apk` package: `oniguruma`

```console
oniguruma-6.9.10-r0 description:
a regular expressions library

oniguruma-6.9.10-r0 webpage:
https://github.com/kkos/oniguruma

oniguruma-6.9.10-r0 installed size:
551 KiB

oniguruma-6.9.10-r0 license:
BSD-2-Clause

```

### `apk` package: `openssl`

```console
openssl-3.5.4-r0 description:
Toolkit for Transport Layer Security (TLS)

openssl-3.5.4-r0 webpage:
https://www.openssl.org/

openssl-3.5.4-r0 installed size:
801 KiB

openssl-3.5.4-r0 license:
Apache-2.0

```

### `apk` package: `popt`

```console
popt-1.19-r4 description:
commandline option parser

popt-1.19-r4 webpage:
https://github.com/rpm-software-management/popt

popt-1.19-r4 installed size:
42 KiB

popt-1.19-r4 license:
MIT

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

### `apk` package: `rsync`

```console
rsync-3.4.1-r1 description:
A file transfer program to keep remote files in sync

rsync-3.4.1-r1 webpage:
https://rsync.samba.org/

rsync-3.4.1-r1 installed size:
375 KiB

rsync-3.4.1-r1 license:
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

### `apk` package: `shadow`

```console
shadow-4.17.3-r0 description:
PAM-using login and passwd utilities (usermod, useradd, ...)

shadow-4.17.3-r0 webpage:
https://github.com/shadow-maint/shadow

shadow-4.17.3-r0 installed size:
1302 KiB

shadow-4.17.3-r0 license:
BSD-3-Clause

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

### `apk` package: `tar`

```console
tar-1.35-r3 description:
Utility used to store, backup, and transport files

tar-1.35-r3 webpage:
https://www.gnu.org/software/tar/

tar-1.35-r3 installed size:
403 KiB

tar-1.35-r3 license:
GPL-3.0-or-later

```

### `apk` package: `tini`

```console
tini-0.19.0-r3 description:
A tiny but valid init for containers

tini-0.19.0-r3 webpage:
https://github.com/krallin/tini

tini-0.19.0-r3 installed size:
27 KiB

tini-0.19.0-r3 license:
MIT

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

### `apk` package: `xz`

```console
xz-5.8.1-r0 description:
Library and CLI tools for XZ and LZMA compressed files

xz-5.8.1-r0 webpage:
https://tukaani.org/xz/

xz-5.8.1-r0 installed size:
162 KiB

xz-5.8.1-r0 license:
GPL-2.0-or-later AND 0BSD AND Public-Domain AND LGPL-2.1-or-later

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

### `apk` package: `zstd-libs`

```console
zstd-libs-1.5.7-r0 description:
Zstandard - Fast real-time compression algorithm (libraries)

zstd-libs-1.5.7-r0 webpage:
https://facebook.github.io/zstd/

zstd-libs-1.5.7-r0 installed size:
701 KiB

zstd-libs-1.5.7-r0 license:
BSD-3-Clause OR GPL-2.0-or-later

```
