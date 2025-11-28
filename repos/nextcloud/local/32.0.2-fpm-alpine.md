# `nextcloud:32.0.2-fpm-alpine`

## Docker Metadata

- Image ID: `sha256:d6b27a628a9a42240e905609d2432549d5ce467fb4e6320b10ee7e64082826c1`
- Created: `2025-11-21T01:00:41.78067486Z`
- Virtual Size: ~ 1.03 Gb  
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
  - `PHP_MEMORY_LIMIT=512M`
  - `PHP_UPLOAD_LIMIT=512M`
  - `PHP_OPCACHE_MEMORY_CONSUMPTION=128`
  - `NEXTCLOUD_VERSION=32.0.2`

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

### `apk` package: `aom-libs`

```console
aom-libs-3.12.1-r0 description:
Alliance for Open Media (AOM) AV1 codec SDK (libraries)

aom-libs-3.12.1-r0 webpage:
https://aomedia.org/

aom-libs-3.12.1-r0 installed size:
7450 KiB

aom-libs-3.12.1-r0 license:
BSD-2-Clause AND custom

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

### `apk` package: `avahi-libs`

```console
avahi-libs-0.8-r21 description:
Libraries for avahi run-time use

avahi-libs-0.8-r21 webpage:
https://www.avahi.org/

avahi-libs-0.8-r21 installed size:
104 KiB

avahi-libs-0.8-r21 license:
LGPL-2.1-or-later

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

### `apk` package: `cairo`

```console
cairo-1.18.4-r0 description:
A vector graphics library

cairo-1.18.4-r0 webpage:
https://cairographics.org/

cairo-1.18.4-r0 installed size:
1056 KiB

cairo-1.18.4-r0 license:
LGPL-2.1-or-later OR MPL-1.1

```

### `apk` package: `cups-libs`

```console
cups-libs-2.4.11-r0 description:
CUPS libraries

cups-libs-2.4.11-r0 webpage:
https://github.com/OpenPrinting/cups/

cups-libs-2.4.11-r0 installed size:
559 KiB

cups-libs-2.4.11-r0 license:
Apache-2.0

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

### `apk` package: `dbus-libs`

```console
dbus-libs-1.16.2-r1 description:
D-BUS access libraries

dbus-libs-1.16.2-r1 webpage:
https://www.freedesktop.org/Software/dbus

dbus-libs-1.16.2-r1 installed size:
289 KiB

dbus-libs-1.16.2-r1 license:
AFL-2.1 OR GPL-2.0-or-later

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

### `apk` package: `fribidi`

```console
fribidi-1.0.16-r1 description:
Free Implementation of the Unicode Bidirectional Algorithm

fribidi-1.0.16-r1 webpage:
https://github.com/fribidi/fribidi

fribidi-1.0.16-r1 installed size:
136 KiB

fribidi-1.0.16-r1 license:
LGPL-2.1-or-later

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

### `apk` package: `gdk-pixbuf`

```console
gdk-pixbuf-2.42.12-r1 description:
GTK+ image loading library

gdk-pixbuf-2.42.12-r1 webpage:
https://wiki.gnome.org/Projects/GdkPixbuf

gdk-pixbuf-2.42.12-r1 installed size:
435 KiB

gdk-pixbuf-2.42.12-r1 license:
LGPL-2.1-or-later

```

### `apk` package: `ghostscript`

```console
ghostscript-10.05.1-r0 description:
Interpreter for the PostScript language and for PDF

ghostscript-10.05.1-r0 webpage:
https://ghostscript.com/

ghostscript-10.05.1-r0 installed size:
61 MiB

ghostscript-10.05.1-r0 license:
AGPL-3.0-or-later

```

### `apk` package: `glib`

```console
glib-2.84.4-r0 description:
Common C routines used by Gtk+ and other libs

glib-2.84.4-r0 webpage:
https://developer.gnome.org/glib/

glib-2.84.4-r0 installed size:
5249 KiB

glib-2.84.4-r0 license:
LGPL-2.1-or-later

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

### `apk` package: `gnutls`

```console
gnutls-3.8.8-r0 description:
TLS protocol implementation

gnutls-3.8.8-r0 webpage:
https://www.gnutls.org/

gnutls-3.8.8-r0 installed size:
1865 KiB

gnutls-3.8.8-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `graphite2`

```console
graphite2-1.3.14-r6 description:
reimplementation of the SIL Graphite text processing engine

graphite2-1.3.14-r6 webpage:
https://graphite.sil.org/

graphite2-1.3.14-r6 installed size:
121 KiB

graphite2-1.3.14-r6 license:
LGPL-2.1-or-later OR MPL-1.1

```

### `apk` package: `harfbuzz`

```console
harfbuzz-11.2.1-r0 description:
Text shaping library

harfbuzz-11.2.1-r0 webpage:
https://harfbuzz.github.io/

harfbuzz-11.2.1-r0 installed size:
1311 KiB

harfbuzz-11.2.1-r0 license:
MIT

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

### `apk` package: `imagemagick-heic`

```console
imagemagick-heic-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (HEIC support modules)

imagemagick-heic-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-heic-7.1.2.8-r0 installed size:
30 KiB

imagemagick-heic-7.1.2.8-r0 license:
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

### `apk` package: `imagemagick-pango`

```console
imagemagick-pango-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (pango support modules)

imagemagick-pango-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-pango-7.1.2.8-r0 installed size:
22 KiB

imagemagick-pango-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `imagemagick-pdf`

```console
imagemagick-pdf-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (PDF support modules)

imagemagick-pdf-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-pdf-7.1.2.8-r0 installed size:
121 KiB

imagemagick-pdf-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `imagemagick-raw`

```console
imagemagick-raw-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (RAW support modules)

imagemagick-raw-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-raw-7.1.2.8-r0 installed size:
22 KiB

imagemagick-raw-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `imagemagick-svg`

```console
imagemagick-svg-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (SVG support modules)

imagemagick-svg-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-svg-7.1.2.8-r0 installed size:
75 KiB

imagemagick-svg-7.1.2.8-r0 license:
ImageMagick

```

### `apk` package: `imagemagick-tiff`

```console
imagemagick-tiff-7.1.2.8-r0 description:
Collection of tools and libraries for many image formats (TIFF support modules)

imagemagick-tiff-7.1.2.8-r0 webpage:
https://imagemagick.org/

imagemagick-tiff-7.1.2.8-r0 installed size:
115 KiB

imagemagick-tiff-7.1.2.8-r0 license:
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

### `apk` package: `jbig2dec`

```console
jbig2dec-0.20-r0 description:
JBIG2 image compression format decoder

jbig2dec-0.20-r0 webpage:
https://jbig2dec.com/

jbig2dec-0.20-r0 installed size:
127 KiB

jbig2dec-0.20-r0 license:
AGPL-3.0-or-later

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

### `apk` package: `libblkid`

```console
libblkid-2.41-r9 description:
Block device identification library from util-linux

libblkid-2.41-r9 webpage:
https://git.kernel.org/cgit/utils/util-linux/util-linux.git

libblkid-2.41-r9 installed size:
190 KiB

libblkid-2.41-r9 license:
LGPL-2.1-or-later

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

### `apk` package: `libdav1d`

```console
libdav1d-1.5.1-r0 description:
small and fast AV1 Decoder (libraries)

libdav1d-1.5.1-r0 webpage:
https://code.videolan.org/videolan/dav1d

libdav1d-1.5.1-r0 installed size:
1697 KiB

libdav1d-1.5.1-r0 license:
BSD-2-Clause

```

### `apk` package: `libde265`

```console
libde265-1.0.15-r1 description:
Open h.265 video codec implementation

libde265-1.0.15-r1 webpage:
https://github.com/strukturag/libde265

libde265-1.0.15-r1 installed size:
454 KiB

libde265-1.0.15-r1 license:
LGPL-3.0-or-later

```

### `apk` package: `libeconf`

```console
libeconf-0.6.3-r0 description:
Enhanced Config File Parser

libeconf-0.6.3-r0 webpage:
https://github.com/openSUSE/libeconf

libeconf-0.6.3-r0 installed size:
72 KiB

libeconf-0.6.3-r0 license:
MIT

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

### `apk` package: `libheif`

```console
libheif-1.19.8-r0 description:
ISO/IEC 23008-12:2017 HEIF file format decoder and encoder

libheif-1.19.8-r0 webpage:
https://www.libde265.org/

libheif-1.19.8-r0 installed size:
986 KiB

libheif-1.19.8-r0 license:
LGPL-3.0-or-later

```

### `apk` package: `libice`

```console
libice-1.1.2-r0 description:
X11 Inter-Client Exchange library

libice-1.1.2-r0 webpage:
https://xorg.freedesktop.org/

libice-1.1.2-r0 installed size:
86 KiB

libice-1.1.2-r0 license:
X11

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

### `apk` package: `libmount`

```console
libmount-2.41-r9 description:
Block device identification library from util-linux

libmount-2.41-r9 webpage:
https://git.kernel.org/cgit/utils/util-linux/util-linux.git

libmount-2.41-r9 installed size:
266 KiB

libmount-2.41-r9 license:
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

### `apk` package: `libpq`

```console
libpq-17.7-r0 description:
PostgreSQL client library

libpq-17.7-r0 webpage:
https://www.postgresql.org/

libpq-17.7-r0 installed size:
322 KiB

libpq-17.7-r0 license:
PostgreSQL

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

### `apk` package: `libraw`

```console
libraw-0.21.4-r0 description:
Library for reading RAW files obtained from digital photo cameras

libraw-0.21.4-r0 webpage:
https://www.libraw.org/

libraw-0.21.4-r0 installed size:
2454 KiB

libraw-0.21.4-r0 license:
CDDL-1.0 OR LGPL-2.1-only

```

### `apk` package: `librsvg`

```console
librsvg-2.60.0-r0 description:
SAX-based renderer for SVG files into a GdkPixbuf

librsvg-2.60.0-r0 webpage:
https://wiki.gnome.org/Projects/LibRsvg

librsvg-2.60.0-r0 installed size:
4029 KiB

librsvg-2.60.0-r0 license:
LGPL-2.1-or-later

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

### `apk` package: `libsm`

```console
libsm-1.2.5-r0 description:
X11 Session Management library

libsm-1.2.5-r0 webpage:
https://xorg.freedesktop.org/

libsm-1.2.5-r0 installed size:
33 KiB

libsm-1.2.5-r0 license:
MIT

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

### `apk` package: `libtasn1`

```console
libtasn1-4.20.0-r0 description:
The ASN.1 library used in GNUTLS

libtasn1-4.20.0-r0 webpage:
https://www.gnu.org/software/gnutls/

libtasn1-4.20.0-r0 installed size:
65 KiB

libtasn1-4.20.0-r0 license:
LGPL-2.1-or-later

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

### `apk` package: `libuuid`

```console
libuuid-2.41-r9 description:
DCE compatible Universally Unique Identifier library

libuuid-2.41-r9 webpage:
https://git.kernel.org/cgit/utils/util-linux/util-linux.git

libuuid-2.41-r9 installed size:
29 KiB

libuuid-2.41-r9 license:
BSD-3-Clause

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

### `apk` package: `libxft`

```console
libxft-2.3.8-r3 description:
FreeType-based font drawing library for X

libxft-2.3.8-r3 webpage:
https://xorg.freedesktop.org/

libxft-2.3.8-r3 installed size:
81 KiB

libxft-2.3.8-r3 license:
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

### `apk` package: `libxrender`

```console
libxrender-0.9.12-r0 description:
X Rendering Extension client library

libxrender-0.9.12-r0 webpage:
https://xorg.freedesktop.org/

libxrender-0.9.12-r0 installed size:
41 KiB

libxrender-0.9.12-r0 license:
MIT

```

### `apk` package: `libxt`

```console
libxt-1.3.1-r0 description:
X11 toolkit intrinsics library

libxt-1.3.1-r0 webpage:
https://xorg.freedesktop.org/

libxt-1.3.1-r0 installed size:
347 KiB

libxt-1.3.1-r0 license:
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

### `apk` package: `nettle`

```console
nettle-3.10.1-r0 description:
Low-level cryptographic library

nettle-3.10.1-r0 webpage:
https://www.lysator.liu.se/~nisse/nettle/

nettle-3.10.1-r0 installed size:
587 KiB

nettle-3.10.1-r0 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

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

### `apk` package: `numactl`

```console
numactl-2.0.18-r0 description:
Simple NUMA policy support

numactl-2.0.18-r0 webpage:
https://github.com/numactl/numactl

numactl-2.0.18-r0 installed size:
46 KiB

numactl-2.0.18-r0 license:
LGPL-2.1-only

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

### `apk` package: `openjpeg`

```console
openjpeg-2.5.3-r0 description:
Open-source implementation of JPEG2000 image codec

openjpeg-2.5.3-r0 webpage:
https://www.openjpeg.org/

openjpeg-2.5.3-r0 installed size:
305 KiB

openjpeg-2.5.3-r0 license:
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

### `apk` package: `p11-kit`

```console
p11-kit-0.25.5-r2 description:
Library for loading and sharing PKCS#11 modules

p11-kit-0.25.5-r2 webpage:
https://p11-glue.freedesktop.org/

p11-kit-0.25.5-r2 installed size:
1362 KiB

p11-kit-0.25.5-r2 license:
BSD-3-Clause

```

### `apk` package: `pango`

```console
pango-1.56.3-r0 description:
library for layout and rendering of text

pango-1.56.3-r0 webpage:
https://www.pango.org/

pango-1.56.3-r0 installed size:
616 KiB

pango-1.56.3-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `pcre2`

```console
pcre2-10.46-r0 description:
Perl-compatible regular expression library

pcre2-10.46-r0 webpage:
https://pcre.org/

pcre2-10.46-r0 installed size:
767 KiB

pcre2-10.46-r0 license:
BSD-3-Clause

```

### `apk` package: `pixman`

```console
pixman-0.46.4-r0 description:
Low-level pixel manipulation library

pixman-0.46.4-r0 webpage:
https://gitlab.freedesktop.org/pixman

pixman-0.46.4-r0 installed size:
557 KiB

pixman-0.46.4-r0 license:
MIT

```

### `apk` package: `pkgconf`

```console
pkgconf-2.4.3-r0 description:
development framework configuration tools

pkgconf-2.4.3-r0 webpage:
https://gitea.treehouse.systems/ariadne/pkgconf

pkgconf-2.4.3-r0 installed size:
137 KiB

pkgconf-2.4.3-r0 license:
ISC

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

### `apk` package: `shared-mime-info`

```console
shared-mime-info-2.4-r6 description:
Freedesktop.org Shared MIME Info

shared-mime-info-2.4-r6 webpage:
https://www.freedesktop.org/Software/shared-mime-info

shared-mime-info-2.4-r6 installed size:
2493 KiB

shared-mime-info-2.4-r6 license:
GPL-2.0-or-later

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

### `apk` package: `tiff`

```console
tiff-4.7.1-r0 description:
Provides support for the Tag Image File Format or TIFF

tiff-4.7.1-r0 webpage:
https://gitlab.com/libtiff/libtiff

tiff-4.7.1-r0 installed size:
453 KiB

tiff-4.7.1-r0 license:
libtiff

```

### `apk` package: `x265-libs`

```console
x265-libs-3.6-r0 description:
Open Source H265/HEVC video encoder (libraries)

x265-libs-3.6-r0 webpage:
https://www.videolan.org/developers/x265.html

x265-libs-3.6-r0 installed size:
18 MiB

x265-libs-3.6-r0 license:
GPL-2.0-or-later

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
