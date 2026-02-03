# `r-base:4.5.2`

## Docker Metadata

- Image ID: `sha256:c76afb0f2d1ac31e5267ca28c3351ec276f1be177a846113eebc70fbebf7e402`
- Created: `2026-01-13T01:56:57.869961855Z`
- Virtual Size: ~ 893.07 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["R"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LC_ALL=en_US.UTF-8`
  - `LANG=en_US.UTF-8`
  - `R_BASE_VERSION=4.5.2`
- Labels:
  - `org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>`
  - `org.opencontainers.image.licenses=GPL-2.0-or-later`
  - `org.opencontainers.image.source=https://github.com/rocker-org/rocker`
  - `org.opencontainers.image.vendor=Rocker Project`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2+b1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-2
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA256:1f42130ccb5442fe2db2aee1dcc03c51a31512dd2519a38e8fc9270c5abbc807
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA256:e27b6e194c0a7554595d76f96acdceb800631bdc46c36457b73bc7e4a0c5f2ee
```

### `dpkg` source package: `apt=3.1.13`

Binary Packages:

- `apt=3.1.13`
- `libapt-pkg7.0:amd64=3.1.13`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/3.1.13/


### `dpkg` source package: `attr=1:2.5.2-3`

Binary Packages:

- `libattr1:amd64=1:2.5.2-3`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-3
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-3.dsc' attr_2.5.2-3.dsc 2576 SHA256:c2ae3e15db059029030ddf4fdac179d8f90d423f2310a6ef8c745ba28ac18b0a
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-3.debian.tar.xz' attr_2.5.2-3.debian.tar.xz 32260 SHA256:153f98c87575277ea021e24dae36293b7738699174438a2060b47e8312b771e3
```

### `dpkg` source package: `audit=1:4.1.2-1`

Binary Packages:

- `libaudit-common=1:4.1.2-1`
- `libaudit1:amd64=1:4.1.2-1+b1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.1.2-1
'http://http.debian.net/debian/pool/main/a/audit/audit_4.1.2-1.dsc' audit_4.1.2-1.dsc 2546 SHA256:5443f3ff043dd30cba1549f93940928d04c90cdc7598741a19f722d4109a7f4b
'http://http.debian.net/debian/pool/main/a/audit/audit_4.1.2.orig.tar.gz' audit_4.1.2.orig.tar.gz 656095 SHA256:5c638bbeef9adb6c5715d3a60f0f5adb93e9b81633608af13d23c61f5e5db04d
'http://http.debian.net/debian/pool/main/a/audit/audit_4.1.2-1.debian.tar.xz' audit_4.1.2-1.debian.tar.xz 19712 SHA256:1cb30c0bc4bed825cbac829cec4b840b9d0726dedaf25f57cbc3af9bc7d7bcc2
```

### `dpkg` source package: `base-files=14`

Binary Packages:

- `base-files=14`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=14
'http://http.debian.net/debian/pool/main/b/base-files/base-files_14.dsc' base-files_14.dsc 1207 SHA256:5cdce966268b529d7897b088f28d022093f390970eb63541f5e3753ca521c23b
'http://http.debian.net/debian/pool/main/b/base-files/base-files_14.tar.xz' base-files_14.tar.xz 68388 SHA256:dbb9ebd9278b0507d82c29dff894caf9dfc2b46d35e33a4a1505c96c6c6e54d8
```

### `dpkg` source package: `base-passwd=3.6.8`

Binary Packages:

- `base-passwd=3.6.8`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.8
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.8.dsc' base-passwd_3.6.8.dsc 2044 SHA256:e76e572d2653f2b8eda64c662f5b4310a978ef1fdd039410ace5f6355c3af7d6
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.8.tar.xz' base-passwd_3.6.8.tar.xz 61840 SHA256:fab3d0e6e8b641e116bda9bd5f7a7ed24482384c1513f6a369b506327fbc8dde
```

### `dpkg` source package: `bash=5.3-1`

Binary Packages:

- `bash=5.3-1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `BSD-4-clause-UC`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `Latex2e`
- `MIT-like`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris bash=5.3-1
'http://http.debian.net/debian/pool/main/b/bash/bash_5.3-1.dsc' bash_5.3-1.dsc 2141 SHA256:48fc3b83911ae279877f37efa489d67e91ce2b62ea7ffd81a9770fbec1949021
'http://http.debian.net/debian/pool/main/b/bash/bash_5.3.orig.tar.xz' bash_5.3.orig.tar.xz 5571836 SHA256:a70de6bb41f5e192534a5a1836b1d7fad9a8d4818a6e1506d70f38441552c17a
'http://http.debian.net/debian/pool/main/b/bash/bash_5.3-1.debian.tar.xz' bash_5.3-1.debian.tar.xz 88912 SHA256:e011bc46fc8d3c3a0cf2a349bf7c7da9b2d5237384b3c92297ae8e8181e2b612
```

### `dpkg` source package: `binutils=2.45.50.20251209-1`

Binary Packages:

- `binutils=2.45.50.20251209-1`
- `binutils-common:amd64=2.45.50.20251209-1`
- `binutils-x86-64-linux-gnu=2.45.50.20251209-1`
- `libbinutils:amd64=2.45.50.20251209-1`
- `libctf-nobfd0:amd64=2.45.50.20251209-1`
- `libctf0:amd64=2.45.50.20251209-1`
- `libgprofng0:amd64=2.45.50.20251209-1`
- `libsframe2:amd64=2.45.50.20251209-1`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe2/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.45.50.20251209-1
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.45.50.20251209-1.dsc' binutils_2.45.50.20251209-1.dsc 11614 SHA256:276d49031cd8b5883757e14c930660061ea4f241c738cf281d06745e50bdde1a
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.45.50.20251209.orig.tar.xz' binutils_2.45.50.20251209.orig.tar.xz 24813448 SHA256:16a624f1ecc32d9bf809cf5b7b171a5b25fc5085f1fb961473fb426af7a3f7d7
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.45.50.20251209-1.debian.tar.xz' binutils_2.45.50.20251209-1.debian.tar.xz 123640 SHA256:a1e7306cfb8ba4d07faa688f2c420602b437316a71dcb4e98b0f68f784952e58
```

### `dpkg` source package: `boot=1.3-32-1`

Binary Packages:

- `r-cran-boot=1.3-32-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-boot/copyright`)

- `'unlimited distribution'`

Source:

```console
$ apt-get source -qq --print-uris boot=1.3-32-1
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-32-1.dsc' boot_1.3-32-1.dsc 1802 SHA256:be6caffe2a0a4745ce179149003d99bd31be74a7fade6b4d8aac2ca4f31a3b2d
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-32.orig.tar.gz' boot_1.3-32.orig.tar.gz 238282 SHA256:3a05aced6fea42a5c310c5c6ab7a2019f69f757f5e77c4961183977747136c97
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-32-1.debian.tar.xz' boot_1.3-32-1.debian.tar.xz 5448 SHA256:0e255004401b69c47e584a29ded445eeb2526d0fb06e000c3fc67666b186db07
```

### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2+b9`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA256:39b06802a852629132d549a7f7449dee7f435e801706714a4bc2ea2f15b28f36
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA256:10973f4b4199eafa1d5735ef661ddb2ec2f97319ee9fd1824d4aabe08cff5265
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA256:3d913a3740bcad9a294007575a6beb1846beadbd62b44fb2bf9fdaeddea3236f
```

### `dpkg` source package: `build-essential=12.12`

Binary Packages:

- `build-essential=12.12`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris build-essential=12.12
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.12.dsc' build-essential_12.12.dsc 2259 SHA256:c947434e212c70963a1767c492b2a098fa2389bf6ce1b0be2a8971dead43a255
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.12.tar.xz' build-essential_12.12.tar.xz 51772 SHA256:091efa279e3a3609c4b013cf123ff4d7ec105f7df7b759e09ea93047039c2110
```

### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `bzip2=1.0.8-6`
- `libbz2-1.0:amd64=1.0.8-6`
- `libbz2-dev:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA256:cd3bfd77254a6b5ef1be144bdc90a0dd374bc8206afd98ba4abf828741b79820
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA256:648ed0dac9a041ba6951e0cca521628aa39947cefee78139f7b934a5dc502095
```

### `dpkg` source package: `ca-certificates=20250419`

Binary Packages:

- `ca-certificates=20250419`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20250419
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20250419.dsc' ca-certificates_20250419.dsc 1766 SHA256:3fc919369a3b84e34a959faa8bdffb9bd2c5a7d4a948a4b07a09a5d43e257030
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20250419.tar.xz' ca-certificates_20250419.tar.xz 277504 SHA256:33b44ef78653ecd3f0f2f13e5bba6be466be2e7da72182f737912b81798ba5d2
```

### `dpkg` source package: `cairo=1.18.4-3`

Binary Packages:

- `libcairo2:amd64=1.18.4-3`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.4-3
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.4-3.dsc' cairo_1.18.4-3.dsc 2784 SHA256:5dfb99f2896a2f23810cde3e80e930bd917079b143e4e984feb44ba018590d2a
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.4.orig.tar.xz' cairo_1.18.4.orig.tar.xz 32578804 SHA256:445ed8208a6e4823de1226a74ca319d3600e83f6369f99b14265006599c32ccb
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.4-3.debian.tar.xz' cairo_1.18.4-3.debian.tar.xz 29988 SHA256:25cb656a9c4165f36950b01710683efce6b5b0e30b80d81d519d7c3d1a2f7b2a
```

### `dpkg` source package: `cdebconf=0.282`

Binary Packages:

- `libdebconfclient0:amd64=0.282+b2`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.282
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.282.dsc' cdebconf_0.282.dsc 2694 SHA256:eddf49a846ed6e9f4f20cb14975cca7107580c061bc748f2b51dc9d0b7f4ddf7
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.282.tar.xz' cdebconf_0.282.tar.xz 286192 SHA256:7451627f8274a8db0a1d24c3c589ba163036ca79fdb96ed86ddd0157a4369618
```

### `dpkg` source package: `cluster=2.1.8.1-1`

Binary Packages:

- `r-cran-cluster=2.1.8.1-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-cluster/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cluster=2.1.8.1-1
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8.1-1.dsc' cluster_2.1.8.1-1.dsc 1845 SHA256:c085f1ba08fb98239dd0f65f49262ae77d835056d8998e5179695aae65f85152
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8.1.orig.tar.gz' cluster_2.1.8.1.orig.tar.gz 372103 SHA256:4b95b78e09b17ddca72edc0bb180c753c004ed2f61c3eb12e0451ac77f441e57
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8.1-1.debian.tar.xz' cluster_2.1.8.1-1.debian.tar.xz 4392 SHA256:e4a98e91a7f14ae37690affc02c8f18553563c80d8dfbb886206b5b53f634b3c
```

### `dpkg` source package: `codetools=0.2-20-1`

Binary Packages:

- `r-cran-codetools=0.2-20-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-codetools/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris codetools=0.2-20-1
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-20-1.dsc' codetools_0.2-20-1.dsc 1859 SHA256:298e275af68522d839af2738a384e20c7d6f094d30483c06ba089025c70dd76e
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-20.orig.tar.gz' codetools_0.2-20.orig.tar.gz 38683 SHA256:3be6f375ec178723ddfd559d1e8e85bfeee04a5fbaf9f53f2f844e1669fea863
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-20-1.debian.tar.xz' codetools_0.2-20-1.debian.tar.xz 2916 SHA256:b244f4268d17492bde7834747e48f92657ad8adc5fc69aa12757d988744a4700
```

### `dpkg` source package: `coreutils=9.7-3`

Binary Packages:

- `coreutils=9.7-3`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris coreutils=9.7-3
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7-3.dsc' coreutils_9.7-3.dsc 2122 SHA256:c3a207e3aaad165765c7a6fab89045f5fd20035fea6830b9f9ebbb92ebfbff89
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7.orig.tar.xz' coreutils_9.7.orig.tar.xz 6158960 SHA256:e8bb26ad0293f9b5a1fc43fb42ba970e312c66ce92c1b0b16713d7500db251bf
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7.orig.tar.xz.asc' coreutils_9.7.orig.tar.xz.asc 833 SHA256:5070e9428bd372a7fa1f66b395b81092bb40c98f9f56a2e2bc55c47fd387e901
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7-3.debian.tar.xz' coreutils_9.7-3.debian.tar.xz 26820 SHA256:483f77876a080577f63da1d004cc1cf17d16df65d6925aefdd3294c6101eccfb
```

### `dpkg` source package: `curl=8.18.0-1`

Binary Packages:

- `libcurl4t64:amd64=8.18.0-1`

Licenses: (parsed from: `/usr/share/doc/libcurl4t64/copyright`)

- `BSD-4-Clause-UC`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `OLDAP-2.8`
- `X11`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/curl/8.18.0-1/


### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-10`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-10`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-10`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-2-clause`
- `BSD-2.2-clause`
- `BSD-3-Clause-Attribution`
- `BSD-3-clause`
- `BSD-3-clause-JANET`
- `BSD-3-clause-PADL`
- `BSD-4-clause-UC`
- `FSFULLR`
- `GPL-3`
- `GPL-3+`
- `IBM-as-is`
- `MIT-CMU`
- `MIT-Export`
- `MIT-OpenVision`
- `OpenLDAP`
- `RSA-MD`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-10
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-10.dsc' cyrus-sasl2_2.1.28+dfsg1-10.dsc 3319 SHA256:bf58deb4c9e97e81418a8cead3504040185867e9349c08697398aab1553f41d1
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-10.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-10.debian.tar.xz 102528 SHA256:8761d3e32dfbee1c8f88865f26691f7dcd4359c2e53b638087ac6218fa7827fe
```

### `dpkg` source package: `dash=0.5.12-12`

Binary Packages:

- `dash=0.5.12-12`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-12.dsc' dash_0.5.12-12.dsc 1460 SHA256:589efc4d87a4ae4745c273bdb33198d7c4f28a71736a8ece81d3677cf9c6e5ce
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-12.debian.tar.xz' dash_0.5.12-12.debian.tar.xz 47300 SHA256:a278acb5d9a1f5d9a086d36a547287cbf3105b8f33c0e62d86d264decf5ba1ad
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-11`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-11`

Licenses: (parsed from: `/usr/share/doc/libdb5.3t64/copyright`)

- `Artistic`
- `BSD-3-clause`
- `BSD-3-clause-fjord`
- `GPL`
- `GPL-3`
- `MIT-old`
- `Ms-PL`
- `Sleepycat`
- `TCL-like`
- `X11`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-11
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-11.dsc' db5.3_5.3.28+dfsg2-11.dsc 2032 SHA256:0550eb464a02703e35d86fbc4a7ac0736ab30b2a0ebe0818c490f7106d1d4230
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-11.debian.tar.xz' db5.3_5.3.28+dfsg2-11.debian.tar.xz 36580 SHA256:701601b7398c1ff8714594287db6c042b2cbc2e15bc98e85afd77c4324d3e3aa
```

### `dpkg` source package: `debconf=1.5.91`

Binary Packages:

- `debconf=1.5.91`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.91
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.91.dsc' debconf_1.5.91.dsc 2035 SHA256:1aa3ceaef24ef533cfffe7f9ca750c6325dbaea86a7abca77cb4439ceae930d8
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.91.tar.xz' debconf_1.5.91.tar.xz 609964 SHA256:18f3f43924ccc870be483d7c5f1a9be59e51ae1da403059d654666b5a175bf15
```

### `dpkg` source package: `debian-archive-keyring=2025.1`

Binary Packages:

- `debian-archive-keyring=2025.1`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2025.1
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.dsc' debian-archive-keyring_2025.1.dsc 1267 SHA256:09604bd8d4562a1e942e5d1a19a6b82447cbdeb2e7c7f0df7c32a2503647ea47
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.tar.xz' debian-archive-keyring_2025.1.tar.xz 138248 SHA256:2d019c3fa19c42da4d37571e473c296286dad0214cb3bd5cafd99f04a8bf5471
```

### `dpkg` source package: `debianutils=5.23.2`

Binary Packages:

- `debianutils=5.23.2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.23.2
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.23.2.dsc' debianutils_5.23.2.dsc 1908 SHA256:471b65deec232bb033f3e3e06d5bf64dac0ced474c6fd61d41538f3f3de876f8
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.23.2.tar.xz' debianutils_5.23.2.tar.xz 82376 SHA256:79e524b7526dba2ec5c409d0ee52ebec135815cf5b2907375d444122e0594b69
```

### `dpkg` source package: `diffutils=1:3.12-1`

Binary Packages:

- `diffutils=1:3.12-1`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with autoconf exception`
- `GPL-3+ with texinfo exception`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3.0+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.12-1
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.12-1.dsc' diffutils_3.12-1.dsc 1875 SHA256:eb99be6cc60e71249bd119dfb66ada6a8c0fdd2e1bb8b1325f4801b813ad820c
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz' diffutils_3.12.orig.tar.xz 1938800 SHA256:7c8b7f9fc8609141fdea9cece85249d308624391ff61dedaf528fcb337727dfd
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz.asc' diffutils_3.12.orig.tar.xz.asc 833 SHA256:ad05b321b2f23441275af68072123a5907b05ad989335a9f1f6e3781cb0846a6
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.12-1.debian.tar.xz' diffutils_3.12-1.debian.tar.xz 14752 SHA256:ffacb3eb9ad1a8cc90768e13e1d09da1b71cfab3cb99b1e0bd1f0ba26f89dd46
```

### `dpkg` source package: `dpkg=1.23.3`

Binary Packages:

- `dpkg=1.23.3`
- `dpkg-dev=1.23.3`
- `libdpkg-perl=1.23.3`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.23.3
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.23.3.dsc' dpkg_1.23.3.dsc 3474 SHA256:fc8ea0d894361716bf6ff6e42e6da8f7d60d3798a6d14640fade86ba7774f396
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.23.3.tar.xz' dpkg_1.23.3.tar.xz 5803688 SHA256:57f759b573dfe25602be8f4f0df24d5264367bbd6489741dd767c30dde65ae36
```

### `dpkg` source package: `e2fsprogs=1.47.2-3`

Binary Packages:

- `libcom-err2:amd64=1.47.2-3+b8`

Licenses: (parsed from: `/usr/share/doc/libcom-err2/copyright`)

- `0BSD`
- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause-Variant`
- `BSD-4-Clause-CMU`
- `Expat`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Texinfo exception`
- `ISC`
- `Kazlib`
- `LGPL-2`
- `Latex2e`
- `MIT-US-export`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-3
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3.dsc' e2fsprogs_1.47.2-3.dsc 3035 SHA256:860abb653ecbe01a11bb7e41c9e09a45e83847bffa585f7a3d3c0f9401c9d4bb
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA256:6dcd67ff9d8b13274ba3f088e4318be4f5b71412cd863524423fc49d39a6371f
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA256:2063f62a198dd3df21f789c990c2cf9b4a5de24ed55f0b78d86e97e98daffc9d
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3.debian.tar.xz' e2fsprogs_1.47.2-3.debian.tar.xz 103684 SHA256:5517aae5ce5196e49fa314492f0639ad7a1692c9521d703b6c81acff77a1564e
```

### `dpkg` source package: `ed=1.22.4-1`

Binary Packages:

- `ed=1.22.4-1`

Licenses: (parsed from: `/usr/share/doc/ed/copyright`)

- `BSD-2-Clause`
- `FCONF`
- `FDOC`
- `FLOG`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris ed=1.22.4-1
'http://http.debian.net/debian/pool/main/e/ed/ed_1.22.4-1.dsc' ed_1.22.4-1.dsc 1832 SHA256:c415c993a1a37ddd996a198440d77b7c1187951e80a42922d6016ec4b3284837
'http://http.debian.net/debian/pool/main/e/ed/ed_1.22.4.orig.tar.gz' ed_1.22.4.orig.tar.gz 96644 SHA256:9b9d7dd462c72563c84dc6043b48187692ca7b902e68a85319e84a4a7da289e0
'http://http.debian.net/debian/pool/main/e/ed/ed_1.22.4-1.debian.tar.xz' ed_1.22.4-1.debian.tar.xz 8744 SHA256:c690a6447594c9f08f04ec168c932d7d5c6420a5195959e1c3cdd8c41ed7c56d
```

### `dpkg` source package: `expat=2.7.3-1`

Binary Packages:

- `libexpat1:amd64=2.7.3-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/expat/2.7.3-1/


### `dpkg` source package: `findutils=4.10.0-3`

Binary Packages:

- `findutils=4.10.0-3`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL`
- `GPL with automake exception`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-data exception`
- `GPL-3+ with Bison-2.2 exception`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.10.0-3
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA256:fa6b67056d9e5b4d8edbfc8ab95ac15ac769b140284426973f6a1ef07a4594ec
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA256:1387e0b67ff247d2abde998f90dfbf70c1491391a59ddfecb8ae698789f0a4f5
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA256:7f53670eea6bd114e014571221eb652855c1129a3ed99f2a9257c2a313cc216f
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA256:7d19668508523a6fcfb7731f5646305a8b1a00a3105ee3f0a5f167adf93a8a46
```

### `dpkg` source package: `fontconfig=2.15.0-2.4`

Binary Packages:

- `fontconfig=2.15.0-2.4`
- `fontconfig-config=2.15.0-2.4`
- `libfontconfig1:amd64=2.15.0-2.4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/fontconfig/2.15.0-2.4/


### `dpkg` source package: `foreign=0.8.90-1`

Binary Packages:

- `r-cran-foreign=0.8.90-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-foreign/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris foreign=0.8.90-1
'http://deb.debian.org/debian/pool/main/f/foreign/foreign_0.8.90-1.dsc' foreign_0.8.90-1.dsc 1838 SHA256:0d566e1a8829fb9214d5904e64c63181a27b26acbd5f1aec362328afac3188bb
'http://deb.debian.org/debian/pool/main/f/foreign/foreign_0.8.90.orig.tar.gz' foreign_0.8.90.orig.tar.gz 365447 SHA256:1dc6798002a50b9014227a2d20c0c2450fe6feb991a4a0b3bee36c0ee779a196
'http://deb.debian.org/debian/pool/main/f/foreign/foreign_0.8.90-1.debian.tar.xz' foreign_0.8.90-1.debian.tar.xz 4424 SHA256:f203d8448d6fc3c970cd361b7ed3b87a8bc67be9891a53e6629827a08c54f215
```

Other potentially useful URLs:

- https://sources.debian.net/src/foreign/0.8.90-1/ (for browsing the source)
- https://sources.debian.net/src/foreign/0.8.90-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/foreign/0.8.90-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `freetype=2.14.1+dfsg-2`

Binary Packages:

- `libfreetype6:amd64=2.14.1+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `Expat`
- `FSFAP`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT-Modern-Variant`
- `MIT-SMC`
- `OpenGroup-MIT`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.14.1+dfsg-2
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.14.1%2bdfsg-2.dsc' freetype_2.14.1+dfsg-2.dsc 3732 SHA256:806c60dd48017b66791d6ef4eaede96243e1273167fc124b5bd9561e7ba84aca
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2demos.tar.xz' freetype_2.14.1+dfsg.orig-ft2demos.tar.xz 344228 SHA256:06aaf46e1cabca75856193e83f01f260a0d3dfc9954081db5b4ed1467b4385a0
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.14.1+dfsg.orig-ft2demos.tar.xz.asc 833 SHA256:3008f2db5a555bebd2986e21a29b623fd8240e0a89129a4e727065a32002839a
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2docs.tar.xz' freetype_2.14.1+dfsg.orig-ft2docs.tar.xz 2175972 SHA256:719142a897aef4e5b47689ba4394934285045f45f6aade07c65160e1813839f2
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.14.1+dfsg.orig-ft2docs.tar.xz.asc 833 SHA256:3a7e7dfad0c305387e6c187d913e80601fd28ee3f7a0e8d26b3526fa9c8f7f9b
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig.tar.xz' freetype_2.14.1+dfsg.orig.tar.xz 2247228 SHA256:a29379e6f0641587f85ece9ec3bb46240a38bd091d80a228ae75050b68ca999b
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.14.1%2bdfsg-2.debian.tar.xz' freetype_2.14.1+dfsg-2.debian.tar.xz 43904 SHA256:a7cf2aec15d0f361280e4ab14b50775d24c4869502e80a5506c69ce57b637aa6
```

### `dpkg` source package: `fribidi=1.0.16-5`

Binary Packages:

- `libfribidi0:amd64=1.0.16-5`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.16-5
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.16-5.dsc' fribidi_1.0.16-5.dsc 2014 SHA256:bc60303e25c24c017928a8e19766a0d10c7196ddeb419a646b0781d746cba918
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.16.orig.tar.xz' fribidi_1.0.16.orig.tar.xz 1098260 SHA256:1b1cde5b235d40479e91be2f0e88a309e3214c8ab470ec8a2744d82a5a9ea05c
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.16-5.debian.tar.xz' fribidi_1.0.16-5.debian.tar.xz 9052 SHA256:72209d3e970d4d10d2a2c691c9177d3bfeee59d75a45bacd6ec2f004513b0283
```

### `dpkg` source package: `gcc-15=15.2.0-12`

Binary Packages:

- `cpp-15=15.2.0-12`
- `cpp-15-x86-64-linux-gnu=15.2.0-12`
- `g++-15=15.2.0-12`
- `g++-15-x86-64-linux-gnu=15.2.0-12`
- `gcc-15=15.2.0-12`
- `gcc-15-base:amd64=15.2.0-12`
- `gcc-15-x86-64-linux-gnu=15.2.0-12`
- `gfortran-15=15.2.0-12`
- `gfortran-15-x86-64-linux-gnu=15.2.0-12`
- `libasan8:amd64=15.2.0-12`
- `libatomic1:amd64=15.2.0-12`
- `libcc1-0:amd64=15.2.0-12`
- `libgcc-15-dev:amd64=15.2.0-12`
- `libgcc-s1:amd64=15.2.0-12`
- `libgfortran-15-dev:amd64=15.2.0-12`
- `libgfortran5:amd64=15.2.0-12`
- `libgomp1:amd64=15.2.0-12`
- `libhwasan0:amd64=15.2.0-12`
- `libitm1:amd64=15.2.0-12`
- `liblsan0:amd64=15.2.0-12`
- `libquadmath0:amd64=15.2.0-12`
- `libstdc++-15-dev:amd64=15.2.0-12`
- `libstdc++6:amd64=15.2.0-12`
- `libtsan2:amd64=15.2.0-12`
- `libubsan1:amd64=15.2.0-12`

Licenses: (parsed from: `/usr/share/doc/cpp-15/copyright`, `/usr/share/doc/cpp-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-15/copyright`, `/usr/share/doc/g++-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-15/copyright`, `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/gcc-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran-15/copyright`, `/usr/share/doc/gfortran-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-15-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran-15-dev/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-15-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-15=15.2.0-12
'http://http.debian.net/debian/pool/main/g/gcc-15/gcc-15_15.2.0-12.dsc' gcc-15_15.2.0-12.dsc 52289 SHA256:bdcdce7ace72bb100038fc7f80e6e54e639d6c8d82eef7aef53bb7a1b88093fd
'http://http.debian.net/debian/pool/main/g/gcc-15/gcc-15_15.2.0.orig.tar.gz' gcc-15_15.2.0.orig.tar.gz 100989491 SHA256:3121d3e2821fe21088deb77f11ee786d80969a1c55255386a43ecca1e06b47c0
'http://http.debian.net/debian/pool/main/g/gcc-15/gcc-15_15.2.0-12.debian.tar.xz' gcc-15_15.2.0-12.debian.tar.xz 2842772 SHA256:47a304bf28549884096c071efb44418ce4507264e3d3f4bee82560bddddc9fdc
```

### `dpkg` source package: `gcc-defaults=1.229`

Binary Packages:

- `cpp=4:15.2.0-4`
- `cpp-x86-64-linux-gnu=4:15.2.0-4`
- `g++=4:15.2.0-4`
- `g++-x86-64-linux-gnu=4:15.2.0-4`
- `gcc=4:15.2.0-4`
- `gcc-x86-64-linux-gnu=4:15.2.0-4`
- `gfortran=4:15.2.0-4`
- `gfortran-x86-64-linux-gnu=4:15.2.0-4`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran/copyright`, `/usr/share/doc/gfortran-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.229
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.229.dsc' gcc-defaults_1.229.dsc 37836 SHA256:17bf3650515a1b279ad7c3274320cfd0356eefa6d7fbdc7e5cb8d58253cfba3f
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.229.tar.xz' gcc-defaults_1.229.tar.xz 55528 SHA256:8d13cad4125379ac070a4c6b63e76d0a4d70f1fa4367fe4c6b6fa1f1995e9955
```

### `dpkg` source package: `gdbm=1.26-1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.26-1`
- `libgdbm6t64:amd64=1.26-1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.26-1
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.26-1.dsc' gdbm_1.26-1.dsc 2234 SHA256:ba4b64d1275f986b40ca13e31ebef34e00e0c3227cfdc904fe4d84973af6a22b
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.26.orig.tar.gz' gdbm_1.26.orig.tar.gz 1226591 SHA256:6a24504a14de4a744103dcb936be976df6fbe88ccff26065e54c1c47946f4a5e
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.26-1.debian.tar.xz' gdbm_1.26-1.debian.tar.xz 16832 SHA256:3d358964671e794485be3b567751701061c5e46328ec303512ab26dfe246699d
```

### `dpkg` source package: `glib2.0=2.86.3-4`

Binary Packages:

- `libglib2.0-0t64:amd64=2.86.3-4`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0t64/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `Iconv-PD`
- `Janik-permissive`
- `Kuchling-PD`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `Mingw-PD`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`
- `cmph`
- `old-glib-tests`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.86.3-4
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.86.3-4.dsc' glib2.0_2.86.3-4.dsc 4685 SHA256:9765bae7f89aeb50946a50ede08d4d0dbe33fe7aee7ad2ae8e52e0c069bdb24c
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.86.3.orig-unicode-data.tar.xz' glib2.0_2.86.3.orig-unicode-data.tar.xz 660708 SHA256:c1742461e8c0e9673a3453a3127671169de9cb0138493e5c916f1b989530efcd
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.86.3.orig.tar.xz' glib2.0_2.86.3.orig.tar.xz 5674820 SHA256:b3211d8d34b9df5dca05787ef0ad5d7ca75dec998b970e1aab0001d229977c65
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.86.3-4.debian.tar.xz' glib2.0_2.86.3-4.debian.tar.xz 141400 SHA256:63a2cb8d427e6ef56ae86b42e66cbee52b251e827ffeb2476727a9e33ca7ac0c
```

### `dpkg` source package: `glibc=2.42-7`

Binary Packages:

- `libc-bin=2.42-7`
- `libc-dev-bin=2.42-7`
- `libc-gconv-modules-extra:amd64=2.42-7`
- `libc-l10n=2.42-7`
- `libc6:amd64=2.42-7`
- `libc6-dev:amd64=2.42-7`
- `locales=2.42-7`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-gconv-modules-extra/copyright`, `/usr/share/doc/libc-l10n/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`, `/usr/share/doc/locales/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSD-like-Spencer`
- `BSL-1.0`
- `CORE-MATH`
- `Carnegie`
- `DEC`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-link-exception`
- `GPL-3`
- `GPL-3+`
- `IBM`
- `ISC`
- `Inner-Net`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-2.1+-with-link-exception`
- `LGPL-3`
- `LGPL-3+`
- `MIT-like-Lord`
- `PCRE`
- `SunPro`
- `Unicode-DFS-2016`
- `Univ-Coimbra`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.42-7
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.42-7.dsc' glibc_2.42-7.dsc 8582 SHA256:e7be4e87e63ea86547b8f8d897c70e7b5a1d8aed9e7d44910cde324528f1a41d
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.42.orig.tar.xz' glibc_2.42.orig.tar.xz 21052916 SHA256:69c1e915c8edd75981cbfc6b7654e8fc4e52a48d06b9f706f463492749a9b6fb
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.42-7.debian.tar.xz' glibc_2.42-7.debian.tar.xz 414240 SHA256:7dd4737238647f4abf649890e30eedf8b8c8a0bc59ef7f956098e7580426d5d1
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-5`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-5`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-5
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5.dsc' gmp_6.3.0+dfsg-5.dsc 2230 SHA256:609cad99ebddece1d7028a9c3f0a728c68e5a5fbb15b879a2ea6107ea5b16168
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5.debian.tar.xz' gmp_6.3.0+dfsg-5.debian.tar.xz 20424 SHA256:9a41837b2e2678506c24c2791d3f551fdb61bb01cc5e79aaaf45c68a8f26089a
```

### `dpkg` source package: `gnutls28=3.8.11-3`

Binary Packages:

- `libgnutls30t64:amd64=3.8.11-3`

Licenses: (parsed from: `/usr/share/doc/libgnutls30t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `CC0 license`
- `Expat`
- `FSFAP`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `GPLv3+`
- `LGPL`
- `LGPL-3`
- `LGPLv2.1+`
- `LGPLv3+_or_GPLv2+`
- `MIT OR Unlicense`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.11-3
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.11-3.dsc' gnutls28_3.8.11-3.dsc 3249 SHA256:a6b7c28d4ce47cc81c1d869c06223f73ecd0f5d1416e5b4ca4537aa83ec6c5d0
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.11.orig.tar.xz' gnutls28_3.8.11.orig.tar.xz 6939944 SHA256:91bd23c4a86ebc6152e81303d20cf6ceaeb97bc8f84266d0faec6e29f17baa20
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.11.orig.tar.xz.asc' gnutls28_3.8.11.orig.tar.xz.asc 833 SHA256:6bcfeee1548a8d2afe8997a4015b3a55422cfdadc14524d14400cb3ad716a81a
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.11-3.debian.tar.xz' gnutls28_3.8.11-3.debian.tar.xz 173820 SHA256:4da2d1e5232cf5fa3192c00686afede92d0002d156bae45d33b877e114b0d782
```

### `dpkg` source package: `graphite2=1.3.14-11`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-11`

Licenses: (parsed from: `/usr/share/doc/libgraphite2-3/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1`
- `custom-sil-open-font-license`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris graphite2=1.3.14-11
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14-11.dsc' graphite2_1.3.14-11.dsc 2570 SHA256:871f8acc979bbc4b1b54a9e1780f67c520bb4f61babc19c4ecfe145afacf7cf9
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA256:7a3b342c5681921ce2e0c2496509d30b5b078399d5a7bd2358f95166d57d91df
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14-11.debian.tar.xz' graphite2_1.3.14-11.debian.tar.xz 15760 SHA256:6cb334d0b855139ba69084b2755c2453a9a51e53b1209766965206a6d32ab6b3
```

### `dpkg` source package: `grep=3.12-1`

Binary Packages:

- `grep=3.12-1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `FSFULLR and/or GPL and/or LGPL`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris grep=3.12-1
'http://http.debian.net/debian/pool/main/g/grep/grep_3.12-1.dsc' grep_3.12-1.dsc 1647 SHA256:ce35486482abc0591a00be0848c90a3f40ce14b62e501da637296d23bc4c29f4
'http://http.debian.net/debian/pool/main/g/grep/grep_3.12.orig.tar.xz' grep_3.12.orig.tar.xz 1918448 SHA256:2649b27c0e90e632eadcd757be06c6e9a4f48d941de51e7c0f83ff76408a07b9
'http://http.debian.net/debian/pool/main/g/grep/grep_3.12.orig.tar.xz.asc' grep_3.12.orig.tar.xz.asc 833 SHA256:62d4867d7cfff57a364b745866d798958a90286551fdf45d08df515fa8c79c25
'http://http.debian.net/debian/pool/main/g/grep/grep_3.12-1.debian.tar.xz' grep_3.12-1.debian.tar.xz 24160 SHA256:5baef65e599c41285a0393c1c6845c03c9b29f14765447911a1871a50321fd42
```

### `dpkg` source package: `gzip=1.13-1`

Binary Packages:

- `gzip=1.13-1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13-1.dsc' gzip_1.13-1.dsc 1884 SHA256:4942638dbb63dc5690e0a95ed70ee9f11e93565c43941c2485da3e561ec72028
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA256:7454eb6935db17c6655576c2e1b0fabefd38b4d0936e0f87f48cd062ce91a057
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz.asc' gzip_1.13.orig.tar.xz.asc 833 SHA256:aa752d6460fff2e0064857f1c6057d2dc49a28a45ad28c6b29c525851d6771f1
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13-1.debian.tar.xz' gzip_1.13-1.debian.tar.xz 19028 SHA256:29319b3f91d8e03d940d4d7c0f2a5fe5ec4f2ba4a0e621c9ef2682f2d0240dd2
```

### `dpkg` source package: `harfbuzz=12.3.0-4`

Binary Packages:

- `libharfbuzz0b:amd64=12.3.0-4`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz0b/copyright`)

- `Apache-2.0`
- `CC0-1.0`
- `GPL-2`
- `GPL-2+ with Font exception`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `MIT`
- `Monotype`
- `OFL-1.1`
- `UFL-1.0`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=12.3.0-4
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_12.3.0-4.dsc' harfbuzz_12.3.0-4.dsc 2573 SHA256:dddfa54aaead7b1ee5f1678178176178a754e2b1d585633c7bc6577e99313952
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_12.3.0.orig.tar.xz' harfbuzz_12.3.0.orig.tar.xz 18580220 SHA256:8660ebd3c27d9407fc8433b5d172bafba5f0317cb0bb4339f28e5370c93d42b7
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_12.3.0-4.debian.tar.xz' harfbuzz_12.3.0-4.debian.tar.xz 20012 SHA256:fd3efd130c213928dec5c2d25a659a2e5f663f71dd048fec396a31f264c8ddcb
```

Other potentially useful URLs:

- https://sources.debian.net/src/harfbuzz/12.3.0-4/ (for browsing the source)
- https://sources.debian.net/src/harfbuzz/12.3.0-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/harfbuzz/12.3.0-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hostname=3.25`

Binary Packages:

- `hostname=3.25`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.25.dsc' hostname_3.25.dsc 1519 SHA256:80aadf116c3423044be69a4cef8ba2766f412bd4d46a500aacb61f303c19c4ef
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.25.tar.xz' hostname_3.25.tar.xz 12804 SHA256:5bb5d1be011158090157c9e7587ae5606c262a5020ecdc5caac6686b9910592e
```

### `dpkg` source package: `icu=76.1-4`

Binary Packages:

- `icu-devtools=76.1-4`
- `libicu-dev:amd64=76.1-4`
- `libicu76:amd64=76.1-4`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu76/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=76.1-4
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1-4.dsc' icu_76.1-4.dsc 2236 SHA256:2587ef23962b42a074ceab2f0407058f8e3fca0e6edd5d7c0bc1df6c683724a6
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1.orig.tar.gz' icu_76.1.orig.tar.gz 27437767 SHA256:dfacb46bfe4747410472ce3e1144bf28a102feeaa4e3875bac9b4c6cf30f4f3e
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1.orig.tar.gz.asc' icu_76.1.orig.tar.gz.asc 228 SHA256:6ef6ef96376eb6550f2b450e08b84c29238f60a77b89273f1521e1b57db73472
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1-4.debian.tar.xz' icu_76.1-4.debian.tar.xz 65216 SHA256:5f9ff8b3a8e89a01b52c84bfebd35e7825ac561669d24e5a3d5f25d158e4f412
```

### `dpkg` source package: `init-system-helpers=1.69`

Binary Packages:

- `init-system-helpers=1.69`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.69
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.69.dsc' init-system-helpers_1.69.dsc 2234 SHA256:99b681c969728fba085226b1d1fd25cc37c9fe16f9eb5118e679d845b50ae7ee
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.69.tar.xz' init-system-helpers_1.69.tar.xz 45648 SHA256:e246ee7f39b110803e5307fdb25ec2fb5fe0c62dbd9274011803fef50af08100
```

### `dpkg` source package: `isl=0.27-1`

Binary Packages:

- `libisl23:amd64=0.27-1`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.27-1
'http://http.debian.net/debian/pool/main/i/isl/isl_0.27-1.dsc' isl_0.27-1.dsc 1829 SHA256:35ceb67dbb1b4098431b184e342143c2bd94c4a41ebfb3a983e3be31440b0453
'http://http.debian.net/debian/pool/main/i/isl/isl_0.27.orig.tar.xz' isl_0.27.orig.tar.xz 2056436 SHA256:6d8babb59e7b672e8cb7870e874f3f7b813b6e00e6af3f8b04f7579965643d5c
'http://http.debian.net/debian/pool/main/i/isl/isl_0.27-1.debian.tar.xz' isl_0.27-1.debian.tar.xz 24868 SHA256:1ac2e33075903489d4284ff4e86645405e68a282a80432ee4ee0c43397f59224
```

### `dpkg` source package: `jansson=2.14-2`

Binary Packages:

- `libjansson4:amd64=2.14-2+b4`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14-2.dsc' jansson_2.14-2.dsc 1980 SHA256:6296ddd9c0a022bd1b70074aefb171cfcdf5694a04ffd32b35fd66097621af87
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA256:c739578bf6b764aa0752db9a2fdadcfe921c78f1228c7ec0bb47fa804c55d17b
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14-2.debian.tar.xz' jansson_2.14-2.debian.tar.xz 5428 SHA256:e89fe4fd8221f6934ddb50f2e7f8404311928d0e23e49a5599f3d3d14ee8cb88
```

### `dpkg` source package: `jbigkit=2.1-6.1`

Binary Packages:

- `libjbig0:amd64=2.1-6.1+b2`

Licenses: (parsed from: `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.dsc' jbigkit_2.1-6.1.dsc 2089 SHA256:8dea586c47cb4b2436f77fd33ef4a702b9da936d74de8332a72a8ddbe8124e09
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA256:de7106b6bfaf495d6865c7dd7ac6ca1381bd12e0d81405ea81e7f2167263d932
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.debian.tar.xz' jbigkit_2.1-6.1.debian.tar.xz 9244 SHA256:c9ba99e84d18b1affdc97b26b625721ed06b41a92996d9b426b62c0dbe3868cd
```

### `dpkg` source package: `kernsmooth=2.23-26-1`

Binary Packages:

- `r-cran-kernsmooth=2.23-26-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris kernsmooth=2.23-26-1
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-26-1.dsc' kernsmooth_2.23-26-1.dsc 1891 SHA256:a9cc51d9ffeb82bd4989518d7448537dfeaa25b41e42347665dfdec5762dceb8
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-26.orig.tar.gz' kernsmooth_2.23-26.orig.tar.gz 27607 SHA256:b465bdac197f7faa787e625412ae03d1b7c2c134b1c924cfeb775faf9c4da73e
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-26-1.debian.tar.xz' kernsmooth_2.23-26-1.debian.tar.xz 3504 SHA256:d6ca5f4d034a59c6960042015350e6371d89ff8d9e68fe7758e47cc00561e71b
```

### `dpkg` source package: `keyutils=1.6.3-6`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-6`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-6
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-6.dsc' keyutils_1.6.3-6.dsc 2100 SHA256:e63869474c390d5d5bdee8492f7b2f4d6034ff10d8190da18593620c0f35fbf8
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-6.debian.tar.xz' keyutils_1.6.3-6.debian.tar.xz 16588 SHA256:6fc3c1217b8e92df9dff73e4919c45dff4ada5fd414ab57329af487f4476466a
```

### `dpkg` source package: `krb5=1.22.1-2`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.22.1-2`
- `libk5crypto3:amd64=1.22.1-2`
- `libkrb5-3:amd64=1.22.1-2`
- `libkrb5support0:amd64=1.22.1-2`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.22.1-2
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.22.1-2.dsc' krb5_1.22.1-2.dsc 3378 SHA256:2f6e27442ee93856cdb52cf87050b7c2447239c2ad4e30da8a6d8972ac862c2d
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz' krb5_1.22.1.orig.tar.gz 8747101 SHA256:1a8832b8cad923ebbf1394f67e2efcf41e3a49f460285a66e35adec8fa0053af
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz.asc' krb5_1.22.1.orig.tar.gz.asc 833 SHA256:598334b7b54f63a2280f72cc566bee6f9cbc5ef4dcd9ccabd3a0460641908a64
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.22.1-2.debian.tar.xz' krb5_1.22.1-2.debian.tar.xz 102864 SHA256:6256a11c4dec6ec9897fb6aee006a14cb13cfe89dc4e66cc9cfc3ed31294c59c
```

### `dpkg` source package: `lapack=3.12.1-7`

Binary Packages:

- `libblas-dev:amd64=3.12.1-7`
- `libblas3:amd64=3.12.1-7`
- `liblapack-dev:amd64=3.12.1-7`
- `liblapack3:amd64=3.12.1-7`

Licenses: (parsed from: `/usr/share/doc/libblas-dev/copyright`, `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack-dev/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.12.1-7
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.1-7.dsc' lapack_3.12.1-7.dsc 3389 SHA256:3358ae0356808709ce142ebfe4ed9b48c2c28700b652f7d1b508af3803c71d3d
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.1.orig.tar.gz' lapack_3.12.1.orig.tar.gz 8067087 SHA256:2ca6407a001a474d4d4d35f3a61550156050c48016d949f0da0529c0aa052422
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.1-7.debian.tar.xz' lapack_3.12.1-7.debian.tar.xz 28648 SHA256:2d5aaab5ea97fc394d7f14c5a354357475260c30b048fd3e1b5ef2767e3c68e2
```

### `dpkg` source package: `lattice=0.22-7-1`

Binary Packages:

- `r-cran-lattice=0.22-7-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-lattice/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris lattice=0.22-7-1
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-7-1.dsc' lattice_0.22-7-1.dsc 1838 SHA256:65cab033d638165efe6b8998d9d70603f5c8ec7b339bc9b2e6ef99a4c296432d
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-7.orig.tar.gz' lattice_0.22-7.orig.tar.gz 598622 SHA256:400fa62b95e90410d52a36cee2ddeb025dd49695e55fe3db709fe60886bff9f7
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-7-1.debian.tar.xz' lattice_0.22-7-1.debian.tar.xz 5400 SHA256:6992ffd8f0603cfafae3983913627cf40ef6a8c8cc4291580aa5eb1598d1db13
```

### `dpkg` source package: `lerc=4.0.0+ds-5`

Binary Packages:

- `liblerc4:amd64=4.0.0+ds-5`

Licenses: (parsed from: `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-5
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-5.dsc' lerc_4.0.0+ds-5.dsc 2673 SHA256:84de8dac3dd5f5edc005c5c02be58c1f549f9365ad4147c138c85e07d624cc12
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA256:acf855502fd3b950ee78f0b67bc9e9b39316b3526fbf6d8b8b1a9482fb756723
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-5.debian.tar.xz' lerc_4.0.0+ds-5.debian.tar.xz 8576 SHA256:28ab2b1c19c845cd493e804bb9c43b47f72d5852281ebf832ed68a7576afbf6d
```

### `dpkg` source package: `less=668-1`

Binary Packages:

- `less=668-1`

Licenses: (parsed from: `/usr/share/doc/less/copyright`)

- `GPL-3`
- `GPL-3+`
- `Less`
- `Less,`
- `Spencer-86`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris less=668-1
'http://http.debian.net/debian/pool/main/l/less/less_668-1.dsc' less_668-1.dsc 1889 SHA256:84c63a051999d30deab36131d98345d4277105dadfd5d7c63ffea6a631f498f1
'http://http.debian.net/debian/pool/main/l/less/less_668.orig.tar.gz' less_668.orig.tar.gz 649770 SHA256:2819f55564d86d542abbecafd82ff61e819a3eec967faa36cd3e68f1596a44b8
'http://http.debian.net/debian/pool/main/l/less/less_668.orig.tar.gz.asc' less_668.orig.tar.gz.asc 195 SHA256:5b24942fb8e4352fc22ddff6ccaa61eb978d590fb3eecd26591f5cca8965ab03
'http://http.debian.net/debian/pool/main/l/less/less_668-1.debian.tar.xz' less_668-1.debian.tar.xz 22332 SHA256:83e659f43c11ee8591685744cd71e6b99e8cb430224649ac98557068d881e4ce
```

### `dpkg` source package: `libbsd=0.12.2-2`

Binary Packages:

- `libbsd0:amd64=0.12.2-2`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Regents`
- `BSD-3-clause-author`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.12.2-2
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA256:01eb1d0c896096f9038213f5f00376ecfd1c0d1def21b7042f28ae070e4837e3
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA256:36c878a32c1f190ca2cb474de5c6139990a6c029906493d3566770b1ebd569bf
```

### `dpkg` source package: `libcap-ng=0.8.5-4`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4+b2`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.dsc' libcap-ng_0.8.5-4.dsc 1710 SHA256:a5745b7d68a11068ae5beddcc7fbc94cd87dd81cb2d7495e7d48610603be3526
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.debian.tar.xz' libcap-ng_0.8.5-4.debian.tar.xz 7816 SHA256:f5d4e7f38bdbca87de77317ce95f973883081370ef257019b484e29e3368a20d
```

### `dpkg` source package: `libcap2=1:2.75-10`

Binary Packages:

- `libcap2:amd64=1:2.75-10+b5`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.75-10
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75-10.dsc' libcap2_2.75-10.dsc 2703 SHA256:b7a692cecf4d1975991073b77e7a5e45106d62f428f010284fc44f323f1acce7
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA256:de4e7e064c9ba451d5234dd46e897d7c71c96a9ebf9a0c445bc04f4742d83632
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA256:c71b593e7c3160fd7f406641074d93462bbc4906c9243937a0e232f42d5c54d2
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75-10.debian.tar.xz' libcap2_2.75-10.debian.tar.xz 22964 SHA256:b1eb36e050fa1d03e83df78f35ef8538f05cd3ad96a7362cb4113b2541a390ce
```

### `dpkg` source package: `libdatrie=0.2.14-1`

Binary Packages:

- `libdatrie1:amd64=0.2.14-1`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.14-1
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.14-1.dsc' libdatrie_0.2.14-1.dsc 2236 SHA256:ae0434bcde3663feaea221c5ac6539baa19152ca02dc80d7280aef8fa839a38d
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.14.orig.tar.xz' libdatrie_0.2.14.orig.tar.xz 325696 SHA256:f04095010518635b51c2313efa4f290b7db828d6273e39b2b8858f859dfe81d5
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.14-1.debian.tar.xz' libdatrie_0.2.14-1.debian.tar.xz 9792 SHA256:9cde71692c59f4b440b0524ff309c564571b0b515b0ae63b0cfc1af6d730c9c1
```

### `dpkg` source package: `libdeflate=1.23-2`

Binary Packages:

- `libdeflate-dev:amd64=1.23-2`
- `libdeflate0:amd64=1.23-2`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.23-2
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23-2.dsc' libdeflate_1.23-2.dsc 1743 SHA256:fbec7154ffff5193ef71c196e1e7348a154b1ed35c2a9ce3ece5fcc947303d77
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA256:1ab18349b9fb0ce8a0ca4116bded725be7dcbfa709e19f6f983d99df1fb8b25f
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23-2.debian.tar.xz' libdeflate_1.23-2.debian.tar.xz 5624 SHA256:6d3101de26f30c25e4900fecc3b6da34543771d6014767af29850bc3ff3cbd09
```

### `dpkg` source package: `libffi=3.5.2-3`

Binary Packages:

- `libffi8:amd64=3.5.2-3`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

- `Expat`
- `GPL`
- `GPL-2+`
- `GPL-3+`
- `LGPL-2.1+`
- `MPL-1.1`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.5.2-3
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.5.2-3.dsc' libffi_3.5.2-3.dsc 1954 SHA256:ed67eb00402650aafdc76a7f491a64889fcf5b2da70c6bbb43ffab2e480cffc9
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.5.2.orig.tar.gz' libffi_3.5.2.orig.tar.gz 598870 SHA256:dd19253d3007f366319a51d248a40c9e5fcace4498cbea990b566291844e4e30
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.5.2-3.debian.tar.xz' libffi_3.5.2-3.debian.tar.xz 10928 SHA256:682fc1b23da5ece07584e30263c4dd178ebc819a8d8ec2ac5e5fd7c67c247d30
```

### `dpkg` source package: `libice=2:1.1.1-1`

Binary Packages:

- `libice6:amd64=2:1.1.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.1.1-1
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.1.1-1.dsc' libice_1.1.1-1.dsc 2021 SHA256:88722aa66d7f1807d1b0d3ae5bc62f8f06424dc5e970b1c73a0ea2fdf171f0b8
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.1.1.orig.tar.gz' libice_1.1.1.orig.tar.gz 489944 SHA256:04fbd34a11ba08b9df2e3cdb2055c2e3c1c51b3257f683d7fcf42dabcf8e1210
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.1.1-1.diff.gz' libice_1.1.1-1.diff.gz 7355 SHA256:8ce8ffaf775b0868e0633053fcd0755850938ddda9d977232e536a206c063d18
```

### `dpkg` source package: `libidn2=2.3.8-4`

Binary Packages:

- `libidn2-0:amd64=2.3.8-4`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.8-4
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8-4.dsc' libidn2_2.3.8-4.dsc 2811 SHA256:a48a66a00e742b5985db5215dc99d59f5bc257de32ef62f9c71374934cc2ce8d
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA256:bbad1678d35d28e2c62e6a2577083829461402d9e47b908791c55314a5cb5e04
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA256:8995cab7db361d9d6989eab26d9b521c74236960a5d78250121c8d369b013bd8
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8-4.debian.tar.xz' libidn2_2.3.8-4.debian.tar.xz 18116 SHA256:527b1675003a8be38cda322be1f3ba9352687f8d2ba438f0c82a06318848ff83
```

### `dpkg` source package: `libjpeg-turbo=1:2.1.5-4`

Binary Packages:

- `libjpeg-dev:amd64=1:2.1.5-4`
- `libjpeg62-turbo:amd64=1:2.1.5-4`
- `libjpeg62-turbo-dev:amd64=1:2.1.5-4`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg62-turbo/copyright`, `/usr/share/doc/libjpeg62-turbo-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=1:2.1.5-4
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4.dsc' libjpeg-turbo_2.1.5-4.dsc 2508 SHA256:26cbf22aa3b3e327df072513f14a5ddfb4a7b9a3d78c46a5dccfd711c13ac743
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA256:254f3642b04e309fee775123133c6464181addc150499561020312ec61c1bf7c
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4.debian.tar.xz' libjpeg-turbo_2.1.5-4.debian.tar.xz 108128 SHA256:739e7dc22904dccdc5ab105de57a6e4c1515c0e841e68226e6410ff4976e0e91
```

### `dpkg` source package: `libmd=1.1.0-2`

Binary Packages:

- `libmd0:amd64=1.1.0-2+b1`

Licenses: (parsed from: `/usr/share/doc/libmd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-3-clause`
- `BSD-3-clause-Aaron-D-Gifford`
- `Beerware`
- `ISC`
- `public-domain-md4`
- `public-domain-md5`
- `public-domain-sha1`

Source:

```console
$ apt-get source -qq --print-uris libmd=1.1.0-2
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
```

### `dpkg` source package: `libpaper=2.2.5-0.3`

Binary Packages:

- `libpaper-utils=2.2.5-0.3+b3`
- `libpaper2:amd64=2.2.5-0.3+b3`

Licenses: (parsed from: `/usr/share/doc/libpaper-utils/copyright`, `/usr/share/doc/libpaper2/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libpaper=2.2.5-0.3
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_2.2.5-0.3.dsc' libpaper_2.2.5-0.3.dsc 1863 SHA256:c81d68db130d6930282c46a4ce471c198193ca0e22d2659245f5bc82464931fe
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_2.2.5.orig.tar.xz' libpaper_2.2.5.orig.tar.xz 524008 SHA256:c41cd29f49bb8c2fbc14964a6307451dfd3cada15c1edcc82de878f937cca6a3
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_2.2.5-0.3.debian.tar.xz' libpaper_2.2.5-0.3.debian.tar.xz 25072 SHA256:f34d1a3b1125977ddd30d72aac9cd1105165f7368b58f51c5c55160442d4a31f
```

### `dpkg` source package: `libpng1.6=1.6.53-1`

Binary Packages:

- `libpng-dev:amd64=1.6.53-1`
- `libpng16-16t64:amd64=1.6.53-1`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16t64/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-like-with-advertising-clause`
- `GPL-2`
- `GPL-2+`
- `expat`
- `libpng`
- `libpng OR Apache-2.0 OR BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libpng1.6/1.6.53-1/


### `dpkg` source package: `libpsl=0.21.2-1.1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1+b1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.dsc' libpsl_0.21.2-1.1.dsc 2285 SHA256:b9b5496ca2bffb827cb0b2d997469908a2b7a7475c20a11c02f9dcd1ed2a0cc9
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA256:11e34380f2c81d6e72c710464aae3b680df4ddcc1007826c630fb03c7ca6aa54
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.debian.tar.xz' libpsl_0.21.2-1.1.debian.tar.xz 12120 SHA256:0eccab147b6dfbfb7f5ad40fb5bd9f888d72a0fe44e7d1801811c34a9acad1a7
```

### `dpkg` source package: `libseccomp=2.6.0-2`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2+b1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.dsc' libseccomp_2.6.0-2.dsc 2622 SHA256:d05f94536558d34fa339326c6f958a3357b51efac8234470b5d97b69472db765
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA256:83b6085232d1588c379dc9b9cae47bb37407cf262e6e74993c61ba72d2a784dc
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA256:52e338fa958128293cbd25d2be189e34da41c4f4abbb1b641cf58f373c001f94
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.debian.tar.xz' libseccomp_2.6.0-2.debian.tar.xz 20800 SHA256:ed705ec85719403e77d004c99c0b06b795f090c66fcae265c4bcf37ffea9cc27
```

### `dpkg` source package: `libselinux=3.9-4`

Binary Packages:

- `libselinux1:amd64=3.9-4+b1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.9-4
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.9-4.dsc' libselinux_3.9-4.dsc 2905 SHA256:b16d1fc5b82dbc3a17a6f2891425ac521ea0da22937ea8ae5cef91bd9beadf7d
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz' libselinux_3.9.orig.tar.gz 205334 SHA256:e7ee2c01dba64a0c35c9d7c9c0e06209d8186b325b0638a0d83f915cc3c101e8
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz.asc' libselinux_3.9.orig.tar.gz.asc 833 SHA256:3529c5a905fdfa9e0a8e926ce0333f508213cccd9f6e35ca1011e37412042ca5
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.9-4.debian.tar.xz' libselinux_3.9-4.debian.tar.xz 38096 SHA256:662b33b6d14a591910391f013fb62ee0ef9e8bad055d6d632a23a3c3b8450dd7
```

### `dpkg` source package: `libsemanage=3.9-1`

Binary Packages:

- `libsemanage-common=3.9-1`
- `libsemanage2:amd64=3.9-1+b1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.9-1
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.9-1.dsc' libsemanage_3.9-1.dsc 2965 SHA256:68069c6d39a80c09d3179d4ed69ba1bf9dc41fd4b635f548570836827b478752
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.9.orig.tar.gz' libsemanage_3.9.orig.tar.gz 185278 SHA256:ec05850aef48bfb8e02135a7f4f3f7edba3670f63d5e67f2708d4bd80b9a4634
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.9.orig.tar.gz.asc' libsemanage_3.9.orig.tar.gz.asc 833 SHA256:af7644b29d7ae1f69f89444900b2e2b0eb0b4e71f10a2667c7820d10d55fa53f
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.9-1.debian.tar.xz' libsemanage_3.9-1.debian.tar.xz 38028 SHA256:7982b2652b5a3b73b8dd6ec2cf901d02b1f78fc620861db437aea26f5a1b9654
```

### `dpkg` source package: `libsepol=3.9-2`

Binary Packages:

- `libsepol2:amd64=3.9-2`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.9-2
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.9-2.dsc' libsepol_3.9-2.dsc 2326 SHA256:fca98e9732bd9385e689f1b3bec87517a938217d5e3bf735cd88b9ee5c971850
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz' libsepol_3.9.orig.tar.gz 515726 SHA256:ba630b59e50c5fbf9e9dd45eb3734f373cf78d689d8c10c537114c9bd769fa2e
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz.asc' libsepol_3.9.orig.tar.gz.asc 833 SHA256:2059e9c2e195f8d4102f9868295b0a2c16e91082b236d510499dc27620b812fd
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.9-2.debian.tar.xz' libsepol_3.9-2.debian.tar.xz 21416 SHA256:f4f7f317fccf7dac9c72f1448a335edcf10ea7894f3492c475e76d404fcfb268
```

### `dpkg` source package: `libsm=2:1.2.6-1`

Binary Packages:

- `libsm6:amd64=2:1.2.6-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.6-1
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6-1.dsc' libsm_1.2.6-1.dsc 2302 SHA256:d0ab34a54b145ea728242638b878d05f84bcb71feabf075c5e9510cc608aab93
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz' libsm_1.2.6.orig.tar.gz 467497 SHA256:166b4b50d606cdd83f1ddc61b5b9162600034f848b3e32ccbb0e63536b7d6cdd
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz.asc' libsm_1.2.6.orig.tar.gz.asc 833 SHA256:b5e59abae8a79ae9901e73178dacf5af9d7c3b91704fd86de85d305fd7a17a7f
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6-1.diff.gz' libsm_1.2.6-1.diff.gz 13291 SHA256:7cc1d915c18fa6c34cc57c44ca844b62e99fba79b70c0941466d3747e15f2195
```

### `dpkg` source package: `libssh2=1.11.1-1`

Binary Packages:

- `libssh2-1t64:amd64=1.11.1-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-1
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1-1.dsc' libssh2_1.11.1-1.dsc 2319 SHA256:f97f7ac25300908b255a29c63055e78684e68c12c308edb016747da1de592377
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA256:d9ec76cbe34db98eec3539fe2c899d26b0c837cb3eb466a56b0f109cabf658f7
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA256:f5618c9356a1d5a8059d6cf64015d86547f06b2b8b1f542fbbaf381a736c8075
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1-1.debian.tar.xz' libssh2_1.11.1-1.debian.tar.xz 17136 SHA256:f3b9e55f706c89e9408478a1eecb0067b8e18902e0cab168f44194fcc53641cf
```

### `dpkg` source package: `libtasn1-6=4.20.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libtasn1-6/4.20.0-2/


### `dpkg` source package: `libtext-charwidth-perl=0.04-11`

Binary Packages:

- `libtext-charwidth-perl:amd64=0.04-11+b4`

Licenses: (parsed from: `/usr/share/doc/libtext-charwidth-perl/copyright`)

- `Artistic`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-charwidth-perl=0.04-11
'http://http.debian.net/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.dsc' libtext-charwidth-perl_0.04-11.dsc 2162 SHA256:8a4f6e7a44880f8b4dd8f3dc0c97a39c6fef979f99899de4962c9ccfe84a2577
'http://http.debian.net/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04.orig.tar.bz2' libtext-charwidth-perl_0.04.orig.tar.bz2 8327 SHA256:2990c13c3f4a5479d7dbc5a94b86c23798cf0dc7df54ffe54e065f072558b6ed
'http://http.debian.net/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.debian.tar.xz' libtext-charwidth-perl_0.04-11.debian.tar.xz 3016 SHA256:2590d0b6ee7b9cea5396debb96190077210874b4847e844f9eb0d8a4d87ba19c
```

### `dpkg` source package: `libtext-wrapi18n-perl=0.06-10`

Binary Packages:

- `libtext-wrapi18n-perl=0.06-10`

Licenses: (parsed from: `/usr/share/doc/libtext-wrapi18n-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-wrapi18n-perl=0.06-10
'http://http.debian.net/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.dsc' libtext-wrapi18n-perl_0.06-10.dsc 1829 SHA256:726c08c23af488c28b70600a5c1632468f1535cb50dcd5255cc153a4f8558ed9
'http://http.debian.net/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06.orig.tar.gz' libtext-wrapi18n-perl_0.06.orig.tar.gz 3797 SHA256:432c2a801efe9f12d631124c1163439eac4c99449ba13d80133c45ecacc627f5
'http://http.debian.net/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.debian.tar.xz' libtext-wrapi18n-perl_0.06-10.debian.tar.xz 3452 SHA256:751073476ee62cc3430ff0afcab74a4e02b432199d7612e1fd63105fc89ec378
```

### `dpkg` source package: `libthai=0.1.30-1`

Binary Packages:

- `libthai-data=0.1.30-1`
- `libthai0:amd64=0.1.30-1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.30-1
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.30-1.dsc' libthai_0.1.30-1.dsc 2301 SHA256:dd3e8be0d6afc47875cc554be7c0afe76448555e5d1bee1cb620219427699aa0
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.30.orig.tar.xz' libthai_0.1.30.orig.tar.xz 436044 SHA256:ddba8b53dfe584c3253766030218a88825488a51a7deef041d096e715af64bdd
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.30-1.debian.tar.xz' libthai_0.1.30-1.debian.tar.xz 12652 SHA256:820cc8bbaf8e032393c2ff8c8422264922c384ca6a2920f00516051e3f2d9f37
```

### `dpkg` source package: `libtirpc=1.3.6+ds-1`

Binary Packages:

- `libtirpc-common=1.3.6+ds-1`
- `libtirpc-dev:amd64=1.3.6+ds-1`
- `libtirpc3t64:amd64=1.3.6+ds-1`

Licenses: (parsed from: `/usr/share/doc/libtirpc-common/copyright`, `/usr/share/doc/libtirpc-dev/copyright`, `/usr/share/doc/libtirpc3t64/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-4-Clause`
- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PERMISSIVE`
- `__AUTO_PERMISSIVE__`

Source:

```console
$ apt-get source -qq --print-uris libtirpc=1.3.6+ds-1
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.6%2bds-1.dsc' libtirpc_1.3.6+ds-1.dsc 2154 SHA256:737f9f15b21f8ea4226a2aa8c18c956e69e6eb3546c4c8ec9f5194380e2cd4e6
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.6%2bds.orig.tar.gz' libtirpc_1.3.6+ds.orig.tar.gz 704513 SHA256:f9eeeb368d733e11f18ddb750a41bdf9089ba5f9476404da848c2cd295624f0d
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.6%2bds-1.debian.tar.xz' libtirpc_1.3.6+ds-1.debian.tar.xz 11924 SHA256:3aecc6669961a233b6adda8a1d2136777b68dcf64c61dd6986262199b2e5b95b
```

### `dpkg` source package: `libunistring=1.3-2`

Binary Packages:

- `libunistring5:amd64=1.3-2`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `BSD-3-clause`
- `FreeSoftware`
- `GFDL-1.2+`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode-DFS-2016`
- `X11`
- `bsd-3-clause`
- `gfdl-1.2+`
- `gfdl-1.3+`
- `isc`
- `public-domain`
- `unicode-dfs-2016`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.3-2
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3-2.dsc' libunistring_1.3-2.dsc 2215 SHA256:0c09938cace7fbbf36c73af8bc2243fd2f70d3fe336539e8d4c10d0e61742571
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA256:f245786c831d25150f3dfb4317cda1acc5e3f79a5da4ad073ddca58886569527
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA256:62201b5b7ce9c0b033c50cefa5d7769dff4b7cee8205572e0cf917653cae9e33
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3-2.debian.tar.xz' libunistring_1.3-2.debian.tar.xz 28480 SHA256:feaf9761d365430178ea46feefeb602b435c21acf5924918e2257238e0378fc9
```

### `dpkg` source package: `libwebp=1.5.0-0.1`

Binary Packages:

- `libsharpyuv0:amd64=1.5.0-0.1`
- `libwebp7:amd64=1.5.0-0.1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp7/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.5.0-0.1
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0-0.1.dsc' libwebp_1.5.0-0.1.dsc 2865 SHA256:2e7be6f202ebfaac738278bebc10b151768aef60857e63734018ced4d59b9c9a
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz' libwebp_1.5.0.orig.tar.gz 4267494 SHA256:7d6fab70cf844bf6769077bd5d7a74893f8ffd4dfb42861745750c63c2a5c92c
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz.asc' libwebp_1.5.0.orig.tar.gz.asc 833 SHA256:1383ff0b093f57d65f5a902e1bc51c550795ce4713b38712c60bb9151e15dcd6
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0-0.1.debian.tar.xz' libwebp_1.5.0-0.1.debian.tar.xz 11284 SHA256:0dc0e727dc5f5e04ddd41b482f964626e92658099981b57ddd156b530ae01826
```

### `dpkg` source package: `libx11=2:1.8.12-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.12-1`
- `libx11-data=2:1.8.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.12-1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12-1.dsc' libx11_1.8.12-1.dsc 2490 SHA256:745fb04a4b0f8942183f6ac84ebd9e2dae1416c37f90abeaacabb57dc11286f5
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz' libx11_1.8.12.orig.tar.gz 3215077 SHA256:220fbcf54b6e4d8dc40076ff4ab87954358019982490b33c7802190b62d89ce1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz.asc' libx11_1.8.12.orig.tar.gz.asc 833 SHA256:c3d177c8efcef9d3a1963956de0edc56ef2dd63d13dc39d3d7473dc9011fca65
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12-1.diff.gz' libx11_1.8.12-1.diff.gz 74466 SHA256:2231b0ec8ce2eb380256b67eb30c05d90b0e92d75dd583c24e0bf640b3078977
```

### `dpkg` source package: `libxau=1:1.0.11-1`

Binary Packages:

- `libxau6:amd64=1:1.0.11-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.11-1
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11-1.dsc' libxau_1.0.11-1.dsc 2213 SHA256:6058ab58b243ae2b175eee067b868f37b74cd4e8cc40b90607ce6d9ee99c50f9
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz' libxau_1.0.11.orig.tar.gz 404973 SHA256:3a321aaceb803577a4776a5efe78836eb095a9e44bbc7a465d29463e1a14f189
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz.asc' libxau_1.0.11.orig.tar.gz.asc 358 SHA256:72320a0c036cc2d36bebdd7d279c402620e2f3553f639581dfb23736803ce258
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11-1.diff.gz' libxau_1.0.11-1.diff.gz 22671 SHA256:0af3f94102f73c585c48a6b17f54c92e154f6b560a061871d437bd720edd5314
```

### `dpkg` source package: `libxcb=1.17.0-2`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2+b1`
- `libxcb-shm0:amd64=1.17.0-2+b1`
- `libxcb1:amd64=1.17.0-2+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.dsc' libxcb_1.17.0-2.dsc 5318 SHA256:b2728d156f79d2e757e7378cfcefca52bd570739d2efffa87e1aaeaf4f21de3a
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA256:2c69287424c9e2128cb47ffe92171e10417041ec2963bceafb65cb3fcf8f0b85
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.diff.gz' libxcb_1.17.0-2.diff.gz 28069 SHA256:c5b33b67a61d0d1c1b624bf88a8150f4be1ba9b46e855e38f03a8f73858af558
```

### `dpkg` source package: `libxcrypt=1:4.5.1-1`

Binary Packages:

- `libcrypt1:amd64=1:4.5.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.5.1-1
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.dsc' libxcrypt_4.5.1-1.dsc 2434 SHA256:c9051653fc74d9209e8a3f8b496c359cfecdf7992b0a73f69c090973bae90e4b
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1.orig.tar.xz' libxcrypt_4.5.1.orig.tar.xz 433264 SHA256:bddf278d44e2ecdbf1439a52ddc0bb292921dd9f3013030a2a8461c32a45533f
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.debian.tar.xz' libxcrypt_4.5.1-1.debian.tar.xz 8684 SHA256:b6096f6498adf5a94d727c9065ed33b784190e8c2cd3eda5f073e435708293ae
```

### `dpkg` source package: `libxdmcp=1:1.1.5-2`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.5-2`

Licenses: (parsed from: `/usr/share/doc/libxdmcp6/copyright`)

- `OpenGroup-MIT`

Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.5-2
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5-2.dsc' libxdmcp_1.1.5-2.dsc 2269 SHA256:c69bdf96d80bdaa2759bf32131e6ec60a5d3e397963f3b13370789dfe8704cdc
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz' libxdmcp_1.1.5.orig.tar.gz 442597 SHA256:31a7abc4f129dcf6f27ae912c3eedcb94d25ad2e8f317f69df6eda0bc4e4f2f3
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz.asc' libxdmcp_1.1.5.orig.tar.gz.asc 833 SHA256:0c7666da02d66ab785584cd16a6f9324f0d949555734e70b3b1385e525c7860b
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5-2.diff.gz' libxdmcp_1.1.5-2.diff.gz 10201 SHA256:c64245c976c5e54214c43936aa73a7186c417f549fb0d10ee396fe34d6115196
```

### `dpkg` source package: `libxext=2:1.3.4-1`

Binary Packages:

- `libxext6:amd64=2:1.3.4-1+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4-1.dsc' libxext_1.3.4-1.dsc 2118 SHA256:25024f57d955739c6b858822bf93ec3c71400b56fc0d666826f440e3661fd7c0
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA256:8ef0789f282826661ff40a8eef22430378516ac580167da35cc948be9041aac1
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4-1.diff.gz' libxext_1.3.4-1.diff.gz 12509 SHA256:b975870d6a7b791ffbe2d57efdf6e20c250c5e76d12e45b04c8655f593bb8337
```

### `dpkg` source package: `libxmu=2:1.1.3-4`

Binary Packages:

- `libxmuu1:amd64=2:1.1.3-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxmu=2:1.1.3-4
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-4.dsc' libxmu_1.1.3-4.dsc 2112 SHA256:3b7d461d87f3014f7df3f4f51470a2ddb8b77885aae9b8d5938a6623d93d813f
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3.orig.tar.gz' libxmu_1.1.3.orig.tar.gz 497343 SHA256:5bd9d4ed1ceaac9ea023d86bf1c1632cd3b172dce4a193a72a94e1d9df87a62e
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-4.diff.gz' libxmu_1.1.3-4.diff.gz 11594 SHA256:abcb5c9c31498e3a1a62bd799c902615e7a3485bd4faf98a95b1f0bf2ad53deb
```

### `dpkg` source package: `libxrender=1:0.9.12-1`

Binary Packages:

- `libxrender1:amd64=1:0.9.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.12-1
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12-1.dsc' libxrender_0.9.12-1.dsc 2258 SHA256:2980c127d296455f4e9bcaf5ba114284fa0735ce3ef5b613dbe99d854bc87ca3
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz' libxrender_0.9.12.orig.tar.gz 450034 SHA256:0fff64125819c02d1102b6236f3d7d861a07b5216d8eea336c3811d31494ecf7
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz.asc' libxrender_0.9.12.orig.tar.gz.asc 833 SHA256:0bbd310ac3974ef398cf4d8a4b362b0b4d60ceb43e6eba393c3cc740b03816fc
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12-1.diff.gz' libxrender_0.9.12-1.diff.gz 21464 SHA256:c0d3e91a3aa474772c242dcbb997504dff4c28e177d9b7fbb70c50ce7bf56fc5
```

### `dpkg` source package: `libxss=1:1.2.3-1`

Binary Packages:

- `libxss1:amd64=1:1.2.3-1+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxss=1:1.2.3-1
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3-1.dsc' libxss_1.2.3-1.dsc 2203 SHA256:783dbcd49a0934d994693af676ee98734dad070ab2434a6afe831c2de0ecca1d
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz' libxss_1.2.3.orig.tar.gz 385215 SHA256:4f74e7e412144591d8e0616db27f433cfc9f45aae6669c6c4bb03e6bf9be809a
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz.asc' libxss_1.2.3.orig.tar.gz.asc 705 SHA256:4e900524d56c8e7263365267efa91bb3671110c9eb28ccab58f70e2188f0b91b
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3-1.diff.gz' libxss_1.2.3-1.diff.gz 7145 SHA256:9d381b48f1377f27c506113e1f9b7d6ee286b856421f7f2b27017f01dccfef04
```

### `dpkg` source package: `libxt=1:1.2.1-1.3`

Binary Packages:

- `libxt6t64:amd64=1:1.2.1-1.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.3
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1-1.3.dsc' libxt_1.2.1-1.3.dsc 2359 SHA256:29cbda6ae719fdb74bfcc925b5b477c28e233062cd1e0c44195799c29693826b
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA256:6da1bfa9dd0ed87430a5ce95b129485086394df308998ebe34d98e378e3dfb33
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA256:da406cc94c25ca6773bb37c2055e2eb5665491f7ca6dfc9ea04f0f30ea3fd098
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1-1.3.diff.gz' libxt_1.2.1-1.3.diff.gz 46408 SHA256:1823454f1a0f59f222beea7e37843987181fdce9232b87c23165a18e93586516
```

### `dpkg` source package: `libzstd=1.5.7+dfsg-3`

Binary Packages:

- `libzstd-dev:amd64=1.5.7+dfsg-3`
- `libzstd1:amd64=1.5.7+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-3
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.dsc' libzstd_1.5.7+dfsg-3.dsc 2490 SHA256:e32b7bb90ac7b312238add6abb77023cec6f59385b1c9a78b41b69ea2ef5001a
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA256:0c092ef267edce57ba7f3f2645c861f72eaf5e76273c6c3632869423464b90a5
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.debian.tar.xz' libzstd_1.5.7+dfsg-3.debian.tar.xz 23164 SHA256:ada18b02a46878f2f0a845fd003179ab9591f7f96f0b984db06a024ab46ae81f
```

### `dpkg` source package: `linux=6.18.3-1`

Binary Packages:

- `linux-libc-dev=6.18.3-1`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+-or-X11`
- `LGPL-2.1`
- `Unicode-data`
- `Xen-interface`

Source:

```console
$ apt-get source -qq --print-uris linux=6.18.3-1
'http://http.debian.net/debian/pool/main/l/linux/linux_6.18.3-1.dsc' linux_6.18.3-1.dsc 188042 SHA256:bb8b2ea6c244793690a88c751ee5271ced9f37b910ef565bf5b7a184c705a45a
'http://http.debian.net/debian/pool/main/l/linux/linux_6.18.3.orig.tar.xz' linux_6.18.3.orig.tar.xz 157370668 SHA256:48b96f5ac168dc3e13d407a0aeb4ca236e0f7f362544ba772555a1aff6eaf669
'http://http.debian.net/debian/pool/main/l/linux/linux_6.18.3-1.debian.tar.xz' linux_6.18.3-1.debian.tar.xz 1448248 SHA256:ecf0fbd96248acf06c42f1310b8038c6d3c0bb998006f2c778e7ae6616434080
```

### `dpkg` source package: `littler=0.3.21-2`

Binary Packages:

- `littler=0.3.21-2`
- `r-cran-littler=0.3.21-2`

Licenses: (parsed from: `/usr/share/doc/littler/copyright`, `/usr/share/doc/r-cran-littler/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris littler=0.3.21-2
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.21-2.dsc' littler_0.3.21-2.dsc 1888 SHA256:b6ec506a7b7d2ae8cde91ebce2764311c5243f7fe792c3bfd2b1eb080dda91d0
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.21.orig.tar.gz' littler_0.3.21.orig.tar.gz 129864 SHA256:9e8be7aca97ef31ecc7af845954caddf52f9dad4d28ee1392dca829b75e64085
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.21-2.debian.tar.xz' littler_0.3.21-2.debian.tar.xz 5484 SHA256:5d0cde944c93edbd2064320942b1718d46562321dc77a2062a5cda5c0b9134b9
```

### `dpkg` source package: `lz4=1.10.0-6`

Binary Packages:

- `liblz4-1:amd64=1.10.0-6`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-6
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0-6.dsc' lz4_1.10.0-6.dsc 1941 SHA256:990687371c2426db24e74922a4e19cb7666e321031409ca33bc1dda858ee503e
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA256:537512904744b35e232912055ccf8ec66d768639ff3abe5788d90d792ec5f48b
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0-6.debian.tar.xz' lz4_1.10.0-6.debian.tar.xz 9236 SHA256:edd2f342f469dbb24452fca50a65e323be12047aeeaad4d188faae57a38d57a0
```

### `dpkg` source package: `make-dfsg=4.4.1-3`

Binary Packages:

- `make=4.4.1-3`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.4.1-3
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1-3.dsc' make-dfsg_4.4.1-3.dsc 1976 SHA256:731cf705bc0d727ddd3c34d717e176d8713efecea83902534502c888edb59c85
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA256:3b16b00ea1079af9f8096bbc71ff7cc00c249fc6a862003da3c42308a0adb0fe
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1-3.debian.tar.xz' make-dfsg_4.4.1-3.debian.tar.xz 44236 SHA256:315b591ae5ead58c9f904c532d939c7658073e38ff93f7c1694db83683796511
```

### `dpkg` source package: `mawk=1.3.4.20250131-2`

Binary Packages:

- `mawk=1.3.4.20250131-2`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20250131-2
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131-2.dsc' mawk_1.3.4.20250131-2.dsc 2969 SHA256:e0b020dbf75a7aa312b6938034c3e6c971b5d22dad1dccc43e42da918611650c
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz' mawk_1.3.4.20250131.orig.tar.gz 433213 SHA256:51bcb82d577b141d896d9d9c3077d7aaa209490132e9f2b9573ba8511b3835be
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz.asc' mawk_1.3.4.20250131.orig.tar.gz.asc 729 SHA256:bc83f127727edb42a91d516770c8d0d3cdb5f6e541aa3cb5213b79dae494db95
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131-2.debian.tar.xz' mawk_1.3.4.20250131-2.debian.tar.xz 16120 SHA256:aa9eb515b394eec97cdf28e0c3e52ec4519d63c42701bbc747613cf044d9271c
```

### `dpkg` source package: `mgcv=1.9-4-1`

Binary Packages:

- `r-cran-mgcv=1.9-4-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mgcv/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris mgcv=1.9-4-1
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-4-1.dsc' mgcv_1.9-4-1.dsc 1826 SHA256:b063ab3ac1c9e18d0873fe77c2979cf329cb682a8dc20d7d035fa2ec803ab46d
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-4.orig.tar.gz' mgcv_1.9-4.orig.tar.gz 1163324 SHA256:a98159698afb269e06a46cac1f945bf2b3427a2dd587c6f2efd67ede90089372
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-4-1.debian.tar.xz' mgcv_1.9-4-1.debian.tar.xz 5596 SHA256:eb8cd03c3fedb7631de6708774e14ca6937e223c63269ff5a506429b16d71422
```

### `dpkg` source package: `mpclib3=1.3.1-2`

Binary Packages:

- `libmpc3:amd64=1.3.1-2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-2
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1-2.dsc' mpclib3_1.3.1-2.dsc 1919 SHA256:829425b2e64d5e68541daafb80bc7f1b0a47dc1f3d5870f406aeddf5f11ef179
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA256:ab642492f5cf882b74aa0cb730cd410a81edcdbec895183ce930e706c1c759b8
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1-2.debian.tar.xz' mpclib3_1.3.1-2.debian.tar.xz 4628 SHA256:54e2beb85863fec85a30ca0a5d3f119111f8f1047be7549604377a74c18d6a9f
```

### `dpkg` source package: `mpfr4=4.2.2-2`

Binary Packages:

- `libmpfr6:amd64=4.2.2-2`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.2-2
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.2-2.dsc' mpfr4_4.2.2-2.dsc 2007 SHA256:dce07f556eb43b02367d42768a695b46530b93848fe04e858f29528d2703aaf4
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.2.orig.tar.xz' mpfr4_4.2.2.orig.tar.xz 1505596 SHA256:b67ba0383ef7e8a8563734e2e889ef5ec3c3b898a01d00fa0a6869ad81c6ce01
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.2-2.debian.tar.xz' mpfr4_4.2.2-2.debian.tar.xz 12616 SHA256:6607b4e9395c5af5bc32ad51bfcdf45ac2ff3406540d39df18676714df32aaaf
```

### `dpkg` source package: `ncurses=6.6+20251231-1`

Binary Packages:

- `libncurses-dev:amd64=6.6+20251231-1`
- `libncurses6:amd64=6.6+20251231-1`
- `libncursesw6:amd64=6.6+20251231-1`
- `libtinfo6:amd64=6.6+20251231-1`
- `ncurses-base=6.6+20251231-1`
- `ncurses-bin=6.6+20251231-1`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.6+20251231-1
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.dsc' ncurses_6.6+20251231-1.dsc 4163 SHA256:1c7b340d53b1fc75df31bc219e6395c7d6474348b2ec968098c1a0cc7cecfe0e
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz' ncurses_6.6+20251231.orig.tar.gz 3789898 SHA256:e280541f4f601b8586bec305976c873fd641607f9bc4254bf661034dcccac4e9
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz.asc' ncurses_6.6+20251231.orig.tar.gz.asc 729 SHA256:ccb61134c7ffd365aa1f7f3afc3dadaadbda3a46aee463b289c9d0dddb2e9bd3
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.debian.tar.xz' ncurses_6.6+20251231-1.debian.tar.xz 50852 SHA256:fd4a1fd7113e034175310bda8f4589854a0f66fe70482a6bd553de73d773303c
```

### `dpkg` source package: `nettle=3.10.2-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10.2-1`
- `libnettle8t64:amd64=3.10.2-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed6t64/copyright`, `/usr/share/doc/libnettle8t64/copyright`)

- `Expat`
- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.10.2-1
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.2-1.dsc' nettle_3.10.2-1.dsc 2297 SHA256:e2f713973191da5d021759173f2176c21abb5f9420df45cd93a8ff058d62493f
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz' nettle_3.10.2.orig.tar.gz 2644644 SHA256:fe9ff51cb1f2abb5e65a6b8c10a92da0ab5ab6eaf26e7fc2b675c45f1fb519b5
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz.asc' nettle_3.10.2.orig.tar.gz.asc 573 SHA256:3496de6ba5685733aaab2e4e611ea5860fdd76964c56c995f5a0b4c2ec5084ae
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.2-1.debian.tar.xz' nettle_3.10.2-1.debian.tar.xz 25052 SHA256:6f5be658d8bfbc5ffd3c75bd15b8a40fd51c5dd4ae10519d7835be135944f0a7
```

### `dpkg` source package: `nghttp2=1.64.0-1.1`

Binary Packages:

- `libnghttp2-14:amd64=1.64.0-1.1+b1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1.1
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.1.dsc' nghttp2_1.64.0-1.1.dsc 2514 SHA256:1d0393fc66b1db3e9e842a2a02bf41e7c25b020704ef601b7e5d3f5a0e74cc00
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA256:b452dc69a1fcbc9375389b8b154175d8b7b125cdd713fc426774c2b79a1ebd77
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.1.debian.tar.xz' nghttp2_1.64.0-1.1.debian.tar.xz 39356 SHA256:02b15d82ad6b62a149481fd2871bda26486457821e9a4fa28897f55e1294f379
```

### `dpkg` source package: `nghttp3=1.12.0-1`

Binary Packages:

- `libnghttp3-9:amd64=1.12.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp3-9/copyright`)

- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf generic exception`
- `GPL-2+ with Libtool Exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf generic exception`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris nghttp3=1.12.0-1
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.12.0-1.dsc' nghttp3_1.12.0-1.dsc 1614 SHA256:f440f49945e0b3a00ae14b0e5e89cb449d5e91bb30a11c2e6c29fe71239ebae1
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.12.0.orig.tar.xz' nghttp3_1.12.0.orig.tar.xz 407704 SHA256:6ca1e523b7edd75c02502f2bcf961125c25577e29405479016589c5da48fc43d
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.12.0.orig.tar.xz.asc' nghttp3_1.12.0.orig.tar.xz.asc 833 SHA256:58cc65ccbf825efa40c55214d0f89602db1ee872adc69bcfd498ad1c1000112b
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.12.0-1.debian.tar.xz' nghttp3_1.12.0-1.debian.tar.xz 8444 SHA256:ed0449af7b07687ec6c5992c5d7dc7b08ba16a5798982058144658221a58ba43
```

### `dpkg` source package: `ngtcp2=1.16.0-1`

Binary Packages:

- `libngtcp2-16:amd64=1.16.0-1`
- `libngtcp2-crypto-ossl0:amd64=1.16.0-1`

Licenses: (parsed from: `/usr/share/doc/libngtcp2-16/copyright`, `/usr/share/doc/libngtcp2-crypto-ossl0/copyright`)

- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf generic exception`
- `GPL-2+ with Libtool Exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf generic exception`
- `ISC`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris ngtcp2=1.16.0-1
'http://http.debian.net/debian/pool/main/n/ngtcp2/ngtcp2_1.16.0-1.dsc' ngtcp2_1.16.0-1.dsc 1996 SHA256:e07ed396c076e93d6a97880fea78e2ef601c20817c5c0cc0855d96ff75f34a7e
'http://http.debian.net/debian/pool/main/n/ngtcp2/ngtcp2_1.16.0.orig.tar.xz' ngtcp2_1.16.0.orig.tar.xz 674160 SHA256:367cbcecaca539f76453c49454d8e7b38ecb162acf89cd571535ac4acf82a2b4
'http://http.debian.net/debian/pool/main/n/ngtcp2/ngtcp2_1.16.0.orig.tar.xz.asc' ngtcp2_1.16.0.orig.tar.xz.asc 833 SHA256:8131ec9fcaa1012722f7317d9e96997ab3d08ca975e5dce1c09ca212e19c0b96
'http://http.debian.net/debian/pool/main/n/ngtcp2/ngtcp2_1.16.0-1.debian.tar.xz' ngtcp2_1.16.0-1.debian.tar.xz 10996 SHA256:7bc1cd8d9839f1377cf6769d8b7ae8de6544bd3790d30a72010918cf8b0cacb0
```

### `dpkg` source package: `nlme=3.1.168-1`

Binary Packages:

- `r-cran-nlme=3.1.168-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nlme/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris nlme=3.1.168-1
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.168-1.dsc' nlme_3.1.168-1.dsc 1840 SHA256:a3e233c4708c7d2a4ac1c4695d9ac6b5ee8fb7ab7380b0623044b9f7f9f01959
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.168.orig.tar.gz' nlme_3.1.168.orig.tar.gz 860576 SHA256:23b78468344cb6775dee5e0d9c8133032d64f08ebaba20776508a0443a897362
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.168-1.debian.tar.xz' nlme_3.1.168-1.debian.tar.xz 7376 SHA256:92c007f10be211cc87764096d2eb935e9e373dd4e3249726a51b7747415478b8
```

### `dpkg` source package: `openblas=0.3.30+ds-3`

Binary Packages:

- `libopenblas0-pthread:amd64=0.3.30+ds-3`

Licenses: (parsed from: `/usr/share/doc/libopenblas0-pthread/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-2-clause-texas`
- `BSD-3-clause`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openblas=0.3.30+ds-3
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.30%2bds-3.dsc' openblas_0.3.30+ds-3.dsc 4670 SHA256:90fe8597825336678fa037eed6214231dfea3fdcdada6e950dceb248a9016e9b
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.30%2bds.orig.tar.xz' openblas_0.3.30+ds.orig.tar.xz 2230516 SHA256:441ce70583c6d5d18a727b9b20110818f7794cf8209859969d95edc1c5eda30b
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.30%2bds-3.debian.tar.xz' openblas_0.3.30+ds-3.debian.tar.xz 25832 SHA256:9407f9cbfc618636fdb0b47ceae7fb4358a917bf350bc9250f014279293d71ef
```

### `dpkg` source package: `openldap=2.6.10+dfsg-1`

Binary Packages:

- `libldap2:amd64=2.6.10+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libldap2/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-California`
- `BSD-3-clause-variant`
- `BSD-4-clause-California`
- `Beerware`
- `Expat`
- `Expat-ISC`
- `Expat-UNM`
- `F5`
- `FSF-unlimited`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-2+ with Libtool exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Libtool exception`
- `JCG`
- `MIT-XC`
- `NeoSoft-permissive`
- `OpenLDAP-2.8`
- `UMich`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openldap=2.6.10+dfsg-1
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1.dsc' openldap_2.6.10+dfsg-1.dsc 3285 SHA256:05cdd431ef995904f094f4464ca78d5d3b2abdbe4eefacd72446ff8443a2ffac
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA256:e871102bda1e42155fd4d6be4825a297e1c593cb0907b84fc7dde888dc847877
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1.debian.tar.xz' openldap_2.6.10+dfsg-1.debian.tar.xz 170112 SHA256:2dc95ade5655d67c9043e45b5601734fdb7f668267682d087b595a80de24a500
```

### `dpkg` source package: `openssl=3.5.4-1`

Binary Packages:

- `libssl3t64:amd64=3.5.4-1`
- `openssl=3.5.4-1`
- `openssl-provider-legacy=3.5.4-1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.5.4-1
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.4-1.dsc' openssl_3.5.4-1.dsc 2637 SHA256:35e7e427f8ba3660b77ef5408433b748f7e9070eade4ba0e9452b13bd078ca23
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.4.orig.tar.gz' openssl_3.5.4.orig.tar.gz 53190367 SHA256:967311f84955316969bdb1d8d4b983718ef42338639c621ec4c34fddef355e99
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.4.orig.tar.gz.asc' openssl_3.5.4.orig.tar.gz.asc 833 SHA256:cfcabcfc6e43237392e0ab42e2326fceb71037036c2adaa7ecc7e251778e38f4
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.4-1.debian.tar.xz' openssl_3.5.4-1.debian.tar.xz 48888 SHA256:17fc0e9b7df7bb5a5d33755c1efdc18b74a93affc47f5d9b62c4c8b17337be81
```

### `dpkg` source package: `p11-kit=0.25.10-1`

Binary Packages:

- `libp11-kit0:amd64=0.25.10-1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `X11`
- `customFSFULLRWD`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.25.10-1
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.10-1.dsc' p11-kit_0.25.10-1.dsc 2548 SHA256:b190dc31128ae7f53c55adb2c4c6c8cba0acdbf67200709f44aa269211605484
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.10.orig.tar.xz' p11-kit_0.25.10.orig.tar.xz 1053532 SHA256:a62a137a966fb3a9bbfa670b4422161e369ddea216be51425e3be0ab2096e408
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.10.orig.tar.xz.asc' p11-kit_0.25.10.orig.tar.xz.asc 228 SHA256:d18f6b1956bb040455e83774410fcfd23952d0f83f8893bf297b7dc15de7c184
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.10-1.debian.tar.xz' p11-kit_0.25.10-1.debian.tar.xz 24308 SHA256:78846d266dcd6c75fa0bb9d7f6d116aaa472dfb86a017a0ab56c94fac64c917d
```

### `dpkg` source package: `pam=1.7.0-5`

Binary Packages:

- `libpam-modules:amd64=1.7.0-5`
- `libpam-modules-bin=1.7.0-5`
- `libpam-runtime=1.7.0-5`
- `libpam0g:amd64=1.7.0-5`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pam=1.7.0-5
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0-5.dsc' pam_1.7.0-5.dsc 2210 SHA256:5c127aa18c7cb52ec9ee91fa2099453b3a851bcc0088e79045384a2a508b341c
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA256:57dcd7a6b966ecd5bbd95e1d11173734691e16b68692fa59661cdae9b13b1697
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA256:7a8ea18ec7d9dd1f8cbf9055c32128cbca8241aa63e9fea44d56ce6f0e15e441
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0-5.debian.tar.xz' pam_1.7.0-5.debian.tar.xz 145640 SHA256:d776d7cb6fc8b08273f96b7f843299356ef13c6756e30468c594ab28faf1701c
```

### `dpkg` source package: `pango1.0=1.56.4-1`

Binary Packages:

- `libpango-1.0-0:amd64=1.56.4-1`
- `libpangocairo-1.0-0:amd64=1.56.4-1`
- `libpangoft2-1.0-0:amd64=1.56.4-1`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

- `Apache-2`
- `Apache-2.0`
- `Bitstream-Vera`
- `Chromium-BSD-style`
- `Example`
- `ICU`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OFL-1.1`
- `TCL`
- `Unicode`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pango1.0/1.56.4-1/


### `dpkg` source package: `patch=2.8-2`

Binary Packages:

- `patch=2.8-2`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris patch=2.8-2
'http://http.debian.net/debian/pool/main/p/patch/patch_2.8-2.dsc' patch_2.8-2.dsc 1689 SHA256:41fbd3f2c99f60dcbe02699ff01955a47711377b20987352b957bd55e02e2088
'http://http.debian.net/debian/pool/main/p/patch/patch_2.8.orig.tar.xz' patch_2.8.orig.tar.xz 907208 SHA256:f87cee69eec2b4fcbf60a396b030ad6aa3415f192aa5f7ee84cad5e11f7f5ae3
'http://http.debian.net/debian/pool/main/p/patch/patch_2.8-2.debian.tar.xz' patch_2.8-2.debian.tar.xz 9460 SHA256:9a740460988c910c5538e4d24df00d9961d19dee014c63e92f5d60e611fa60c4
```

### `dpkg` source package: `pcre2=10.46-1`

Binary Packages:

- `libpcre2-16-0:amd64=10.46-1`
- `libpcre2-32-0:amd64=10.46-1`
- `libpcre2-8-0:amd64=10.46-1`
- `libpcre2-dev:amd64=10.46-1`
- `libpcre2-posix3:amd64=10.46-1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.46-1
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.46-1.dsc' pcre2_10.46-1.dsc 2337 SHA256:f07e05cd55dd8189d1a7eec2c3ed2d963f51a84ab5494567a112b42f8d525661
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.46.orig.tar.gz' pcre2_10.46.orig.tar.gz 2718545 SHA256:8d28d7f2c3b970c3a4bf3776bcbb5adfc923183ce74bc8df1ebaad8c1985bd07
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.46-1.diff.gz' pcre2_10.46-1.diff.gz 8748 SHA256:307f2b889eb62e71fba064fb6ec65a367f1a88ceb667c4d7109c8d3fe1859e88
```

### `dpkg` source package: `perl=5.40.1-7`

Binary Packages:

- `libperl5.40:amd64=5.40.1-7`
- `perl=5.40.1-7`
- `perl-base=5.40.1-7`
- `perl-modules-5.40=5.40.1-7`

Licenses: (parsed from: `/usr/share/doc/libperl5.40/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.40/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `Artistic-dist`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `FSFAP`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.40.1-7
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1-7.dsc' perl_5.40.1-7.dsc 2372 SHA256:b74d67b039d7bb2c2c63b0928fae9269f4c025ef6d09254af196827388ff885a
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA256:4ea023d08101443f6ed9dc3bdd9bb5f5e08087678dc9e443d195df22da36209a
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA256:dfa20c2eef2b4af133525610bbb65dd13777ecf998c9c5b1ccf0d308e732ee3f
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1-7.debian.tar.xz' perl_5.40.1-7.debian.tar.xz 172940 SHA256:d9a0b6e8466e0b2061e6fe7605e1f316a86a8e2a95fb3ed7f9e91e698ff002cc
```

### `dpkg` source package: `pixman=0.46.4-1`

Binary Packages:

- `libpixman-1-0:amd64=0.46.4-1`

Licenses: (parsed from: `/usr/share/doc/libpixman-1-0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris pixman=0.46.4-1
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.46.4-1.dsc' pixman_0.46.4-1.dsc 2019 SHA256:cb83e2f57bff31103db1d6248cacf07862cf060fcbd651b03bdd4cafb61df62c
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.46.4.orig.tar.gz' pixman_0.46.4.orig.tar.gz 827198 SHA256:d09c44ebc3bd5bee7021c79f922fe8fb2fb57f7320f55e97ff9914d2346a591c
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.46.4-1.diff.gz' pixman_0.46.4-1.diff.gz 9639 SHA256:6e642aa9ca3c9e36d66ac3680a7b63daa73991f8e04429be45841109ddd996b4
```

### `dpkg` source package: `pkgconf=1.8.1-4`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-4`
- `pkgconf:amd64=1.8.1-4`
- `pkgconf-bin=1.8.1-4`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-4
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-4.dsc' pkgconf_1.8.1-4.dsc 2130 SHA256:782a764448d1ecf39f80c7a1747c28fcbde1800b615eee6a46639a17e58b62f9
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA256:644361ada2942be05655d4452eb018791647c31bba429b287f1f68deb2dc6840
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-4.debian.tar.xz' pkgconf_1.8.1-4.debian.tar.xz 17736 SHA256:e56c56a5f40eb0d57bebcb79983a755e16cf1e1595a6fec7f02b20bd58baa734
```

### `dpkg` source package: `procps=2:4.0.4-9`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-9`
- `procps=2:4.0.4-9`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-9
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-9.dsc' procps_4.0.4-9.dsc 2124 SHA256:0ea43605b8d5d7ac4306af0dcd2d01e237cbaba6603b0cf248dd7cfd4364ac7a
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-9.debian.tar.xz' procps_4.0.4-9.debian.tar.xz 45932 SHA256:4821ca009f83b05522bc97ddac82661898938323ef0808416bca7830ce19bd97
```

### `dpkg` source package: `r-base=4.5.2-1`

Binary Packages:

- `r-base=4.5.2-1`
- `r-base-core=4.5.2-1`
- `r-base-dev=4.5.2-1`
- `r-recommended=4.5.2-1`

Licenses: (parsed from: `/usr/share/doc/r-base/copyright`, `/usr/share/doc/r-base-core/copyright`, `/usr/share/doc/r-base-dev/copyright`, `/usr/share/doc/r-recommended/copyright`)

- `Artistic`
- `GPL-2`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-base=4.5.2-1
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.5.2-1.dsc' r-base_4.5.2-1.dsc 2907 SHA256:4acf22d4a6c68b3ffd513dbd4a7385231273538472bdabc1d466b1a18f025d39
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.5.2.orig.tar.gz' r-base_4.5.2.orig.tar.gz 40812825 SHA256:802020684a01365da50a540e61944aa4098729db83c73d9c3b981a4775c7b0dd
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.5.2-1.debian.tar.xz' r-base_4.5.2-1.debian.tar.xz 100956 SHA256:c822c729a72b0bfce18776f006efc9f7ebacbe94bfbaf2564ccc591d8a1ef698
```

### `dpkg` source package: `r-cran-class=7.3-23-1`

Binary Packages:

- `r-cran-class=7.3-23-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-class/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-class=7.3-23-1
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-23-1.dsc' r-cran-class_7.3-23-1.dsc 1873 SHA256:67260b6a959736c538cd4574488a7ebe6c56a8a561b4bdf12a854f5db05cb4ac
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-23.orig.tar.gz' r-cran-class_7.3-23.orig.tar.gz 22058 SHA256:4d1adb12eae045f15641516d795177dd1d3074c0a86ac633000507c4822891f1
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-23-1.debian.tar.xz' r-cran-class_7.3-23-1.debian.tar.xz 3316 SHA256:cffa8348b0495dad67767a1d6ee38762dd25cf5674c44635cf83ff928f39ff5a
```

### `dpkg` source package: `r-cran-docopt=0.7.2-1`

Binary Packages:

- `r-cran-docopt=0.7.2-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-docopt/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris r-cran-docopt=0.7.2-1
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.2-1.dsc' r-cran-docopt_0.7.2-1.dsc 2142 SHA256:2f8d1a7b44361100ef65dc6749d47df13b6c54333907bf95b9148bfad758bcdc
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.2.orig.tar.gz' r-cran-docopt_0.7.2.orig.tar.gz 29467 SHA256:783692117346074cc8860cc16f7e8b328b05fd040e5c206a869ee351e704e917
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.2-1.debian.tar.xz' r-cran-docopt_0.7.2-1.debian.tar.xz 2604 SHA256:5b80dcbfc23e42562446c16d8da55f1f8450da12cd5f6f365b71ae81bbd018be
```

### `dpkg` source package: `r-cran-mass=7.3-65-1`

Binary Packages:

- `r-cran-mass=7.3-65-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mass/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-mass=7.3-65-1
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-65-1.dsc' r-cran-mass_7.3-65-1.dsc 1851 SHA256:530e4881166d5a06103cd8bd8ea1378269390fd788a2092e948684759edef6e0
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-65.orig.tar.gz' r-cran-mass_7.3-65.orig.tar.gz 510322 SHA256:b07ef1e3c364ce56269b4a8a7759cc9f87c876554f91293437bb578cfe38172f
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-65-1.debian.tar.xz' r-cran-mass_7.3-65-1.debian.tar.xz 6656 SHA256:7afbb1ad2accbdd53ec74654d9b6bebbcd31a0e474fbaca4289b9928c85c275c
```

### `dpkg` source package: `r-cran-nnet=7.3-20-1`

Binary Packages:

- `r-cran-nnet=7.3-20-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nnet/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-nnet=7.3-20-1
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-20-1.dsc' r-cran-nnet_7.3-20-1.dsc 1848 SHA256:420c69ec7bb32356568e0f9cd4e72de5afdad2de8263fc185095ccb7cc1f5e9a
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-20.orig.tar.gz' r-cran-nnet_7.3-20.orig.tar.gz 31285 SHA256:8f33e17e0eb161cfbc1bfee4875baa23c66fcdba8215a64a63402b099db2b555
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-20-1.debian.tar.xz' r-cran-nnet_7.3-20-1.debian.tar.xz 3352 SHA256:128815fe8f2cec37a1e8826ceba2345014208e99a8b2f34fe6e11a6ba430f2aa
```

### `dpkg` source package: `r-cran-spatial=7.3-18-1`

Binary Packages:

- `r-cran-spatial=7.3-18-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-spatial/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-spatial=7.3-18-1
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-18-1.dsc' r-cran-spatial_7.3-18-1.dsc 1884 SHA256:8a1529c41d35fdb85098bb0ee4c677045a395ad0a9d6f6f4d12840efd5ee9e11
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-18.orig.tar.gz' r-cran-spatial_7.3-18.orig.tar.gz 46556 SHA256:cc46693d69745af8ec95b557e7a8ee4e1865df69dc0d25723629fd8e9ea43055
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-18-1.debian.tar.xz' r-cran-spatial_7.3-18-1.debian.tar.xz 3228 SHA256:62b62f43f100841ac79518bde24676d4dcfb4f9133b0643f6a8f3ac92a554bde
```

### `dpkg` source package: `readline=8.3-3`

Binary Packages:

- `libreadline-dev:amd64=8.3-3`
- `libreadline8t64:amd64=8.3-3`
- `readline-common=8.3-3`

Licenses: (parsed from: `/usr/share/doc/libreadline-dev/copyright`, `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.3-3
'http://http.debian.net/debian/pool/main/r/readline/readline_8.3-3.dsc' readline_8.3-3.dsc 2817 SHA256:eb1a1b3c36b5e3b127adf941dd2c861157b5861016ae2b63efc27f1b80742776
'http://http.debian.net/debian/pool/main/r/readline/readline_8.3.orig.tar.gz' readline_8.3.orig.tar.gz 3419642 SHA256:fe5383204467828cd495ee8d1d3c037a7eba1389c22bc6a041f627976f9061cc
'http://http.debian.net/debian/pool/main/r/readline/readline_8.3-3.debian.tar.xz' readline_8.3-3.debian.tar.xz 34188 SHA256:7c6bfc62ecdcc8d311534cfd01ef8c24117650a95aead8d2625c7f12f5793ad9
```

### `dpkg` source package: `rmatrix=1.7-4-1`

Binary Packages:

- `r-cran-matrix=1.7-4-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-matrix/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rmatrix=1.7-4-1
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-4-1.dsc' rmatrix_1.7-4-1.dsc 1860 SHA256:adcb2800928bbc526d22f27257b44a3a98aaa9bf3b37966037735c4499daaf1c
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-4.orig.tar.gz' rmatrix_1.7-4.orig.tar.gz 2485182 SHA256:7b131ecb6a21ff09a33691dac7bf8a7bc2eab9fd1dd09ef14856d74346eb4779
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-4-1.debian.tar.xz' rmatrix_1.7-4-1.debian.tar.xz 6100 SHA256:37dba8e241c16a9f8651596065425727d487e785eada99010041920eff17ef9f
```

### `dpkg` source package: `rpart=4.1.24-1`

Binary Packages:

- `r-cran-rpart=4.1.24-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-rpart/copyright`)

- `GPL-2`
- `GPL-2+ | license included below`

Source:

```console
$ apt-get source -qq --print-uris rpart=4.1.24-1
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.24-1.dsc' rpart_4.1.24-1.dsc 1843 SHA256:bc9677338746e43252b9e23974bb64365143d04db7b2cdd457ddb807e75b77a0
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.24.orig.tar.gz' rpart_4.1.24.orig.tar.gz 620065 SHA256:4ab169a764d9857d299313aae0e7764bcea9220576e537cf165d4f8117e72f29
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.24-1.debian.tar.xz' rpart_4.1.24-1.debian.tar.xz 4436 SHA256:471f830d8b7eb7ca5acde84993e2920a0ad771707f7549893cbb290195597565
```

### `dpkg` source package: `rpcsvc-proto=1.4.3-1`

Binary Packages:

- `rpcsvc-proto=1.4.3-1`

Licenses: (parsed from: `/usr/share/doc/rpcsvc-proto/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+-autoconf-exception`
- `GPL-3`
- `GPL-3+-autoconf-exception`
- `MIT`
- `permissive-autoconf-m4`
- `permissive-autoconf-m4-no-warranty`
- `permissive-configure`
- `permissive-fsf`
- `permissive-makefile-in`

Source:

```console
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.3-1
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.dsc' rpcsvc-proto_1.4.3-1.dsc 1999 SHA256:7d8e122bd18b02fe0de6d467a0ecdafff74035b3e1ed0da1c0c792d9c015682f
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA256:69315e94430f4e79c74d43422f4a36e6259e97e67e2677b2c7d7060436bd99b1
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.debian.tar.xz' rpcsvc-proto_1.4.3-1.debian.tar.xz 4228 SHA256:02034b9dadcf3af5424f72eb65c3842c8d7117b6b78e7a3c798316ceb60843d1
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-3`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-3`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-3
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-3.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-3.dsc 2295 SHA256:8a593a016f6c816dac66ba78a49915af645056acf424146c3488edd27c52075c
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-3.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-3.debian.tar.xz 8180 SHA256:8b1d25a5942e762d792ea1beacb0fda0f9761331fd46ce3874fe24c2360485e2
```

### `dpkg` source package: `rust-sequoia-sqv=1.3.0-5`

Binary Packages:

- `sqv=1.3.0-5`

Licenses: (parsed from: `/usr/share/doc/sqv/copyright`)

- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sqv=1.3.0-5
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-5.dsc' rust-sequoia-sqv_1.3.0-5.dsc 2630 SHA256:dd766214353afb35bc610df910323263abd79da52e9ed7d003858e4db3c590ac
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0.orig.tar.gz' rust-sequoia-sqv_1.3.0.orig.tar.gz 140759 SHA256:8924571d26720b245292ad3c450e4061fcb24890461874790549747bffa35e60
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-5.debian.tar.xz' rust-sequoia-sqv_1.3.0-5.debian.tar.xz 3944 SHA256:ddff90296cb649bd9408e801f9f8cca28a36e63c7e2bab8db8c8716043152b3d
```

### `dpkg` source package: `sed=4.9-2`

Binary Packages:

- `sed=4.9-2`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `BSD-4-clause-UC`
- `BSL-1`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `X11`
- `pcre`

Source:

```console
$ apt-get source -qq --print-uris sed=4.9-2
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA256:17f10deac1b327cb2a623352cdc33444ac9c109359a0caa46b3980b0e415f671
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA256:549fa5cec6eb4fde8cc74ca263b8bf42f947ede677e39d2afeedf661da1d4e52
```

### `dpkg` source package: `sensible-utils=0.0.26`

Binary Packages:

- `sensible-utils=0.0.26`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.26
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.26.dsc' sensible-utils_0.0.26.dsc 1706 SHA256:ca691944ce867871cdc216dd142d66315523773646740cd2801cab85da5bcec5
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.26.tar.xz' sensible-utils_0.0.26.tar.xz 76736 SHA256:46adb7a12d32a9323b29711bc6470628fcc0f94f1748fe5bae4729df50531f68
```

### `dpkg` source package: `shadow=1:4.18.0-2`

Binary Packages:

- `login.defs=1:4.18.0-2`
- `passwd=1:4.18.0-2`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.18.0-2
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.18.0-2.dsc' shadow_4.18.0-2.dsc 2844 SHA256:d556601b8e38c3d6635c3f977fbf4d461df4c7251e3f51bc878e74887b038eb0
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.18.0.orig.tar.xz' shadow_4.18.0.orig.tar.xz 2347912 SHA256:add4604d3bc410344433122a819ee4154b79dd8316a56298c60417e637c07608
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.18.0.orig.tar.xz.asc' shadow_4.18.0.orig.tar.xz.asc 488 SHA256:f16001bf1aedc1aff5d406ecfa4163a4aa4598550f5b9df6b2f3d535d53f535f
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.18.0-2.debian.tar.xz' shadow_4.18.0-2.debian.tar.xz 170120 SHA256:e0f538046d2b8d5252896fea4cf762763ad30e49ac5fd4f3c3e59967b7d8ca0d
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.18.0-2/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.18.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.18.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `survival=3.8-3-1`

Binary Packages:

- `r-cran-survival=3.8-3-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-survival/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris survival=3.8-3-1
'http://deb.debian.org/debian/pool/main/s/survival/survival_3.8-3-1.dsc' survival_3.8-3-1.dsc 1861 SHA256:69ed685e38174f9dca3fc3aaed3bcdc2195602c799f2dec0942d45099f16aa8e
'http://deb.debian.org/debian/pool/main/s/survival/survival_3.8-3.orig.tar.gz' survival_3.8-3.orig.tar.gz 9537074 SHA256:dcab05a57d37a561c7426f6213d49852dc4f462180dd28b5325ff4b6a5e59915
'http://deb.debian.org/debian/pool/main/s/survival/survival_3.8-3-1.debian.tar.xz' survival_3.8-3-1.debian.tar.xz 6384 SHA256:4b50bb4b568f0e66d697fbf1aeef0e9825231f274755e838a339eed051d00808
```

Other potentially useful URLs:

- https://sources.debian.net/src/survival/3.8-3-1/ (for browsing the source)
- https://sources.debian.net/src/survival/3.8-3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/survival/3.8-3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=259-1`

Binary Packages:

- `libsystemd0:amd64=259-1`
- `libudev1:amd64=259-1`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2 with Linux-syscall-note exception`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris systemd=259-1
'http://http.debian.net/debian/pool/main/s/systemd/systemd_259-1.dsc' systemd_259-1.dsc 8690 SHA256:6c7fa02ae6215a7240b8087269e77abc3d422ba7934490b88de3aeba227653ee
'http://http.debian.net/debian/pool/main/s/systemd/systemd_259.orig.tar.gz' systemd_259.orig.tar.gz 17250241 SHA256:a84123692d1add7f9c48fd11cdf5f901393008c2d2ade667c18f25a20bf1290d
'http://http.debian.net/debian/pool/main/s/systemd/systemd_259-1.debian.tar.xz' systemd_259-1.debian.tar.xz 185568 SHA256:a7d59268e759334bdc6d32fb32f8ad0ca91d31471399a2f1c8d0aa19dcab6e97
```

### `dpkg` source package: `sysvinit=3.15-6`

Binary Packages:

- `sysvinit-utils=3.15-6`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.15-6
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.15-6.dsc' sysvinit_3.15-6.dsc 2382 SHA256:07f2bb807af3823e2b1fc7f202b4ad6b4701cfb51f7e5fe586a13473e68c03a8
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.15.orig.tar.gz' sysvinit_3.15.orig.tar.gz 516469 SHA256:0979dd582056130a45bf70738260fb7f3da5cca989509b1e37ad5ad1d4cbe0bf
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.15-6.debian.tar.xz' sysvinit_3.15-6.debian.tar.xz 122884 SHA256:c5114a70a202cd5570c03c9834ae222aac343e9aac8428e0e910210870efacac
```

### `dpkg` source package: `tar=1.35+dfsg-3.1`

Binary Packages:

- `tar=1.35+dfsg-3.1`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris tar=1.35+dfsg-3.1
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.dsc' tar_1.35+dfsg-3.1.dsc 2017 SHA256:5bb58d4966d94c99a9f1b182676089ecc05058d62fdb927f5c07539d9cda4077
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.debian.tar.xz' tar_1.35+dfsg-3.1.debian.tar.xz 21540 SHA256:0d0278034b82ed84dce04a461879b6e1871e4cb416a0ff04d3d35ff05fc30a53
```

### `dpkg` source package: `tcl8.6=8.6.17+dfsg-1`

Binary Packages:

- `libtcl8.6:amd64=8.6.17+dfsg-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tcl8.6=8.6.17+dfsg-1
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.17%2bdfsg-1.dsc' tcl8.6_8.6.17+dfsg-1.dsc 2120 SHA256:9ec620fa937d098c501043162fa2c84cc6b36ad1b651b2f1790da28d51824969
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.17%2bdfsg.orig.tar.gz' tcl8.6_8.6.17+dfsg.orig.tar.gz 7043939 SHA256:a1748f61ae9de840b112bdefe8178118fbc35609d2b4f0a73f3b9e73da7f6530
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.17%2bdfsg-1.debian.tar.xz' tcl8.6_8.6.17+dfsg-1.debian.tar.xz 14484 SHA256:a687b1cbe1bc50790dbdae1c9c6a19552534655674051f86308be3b9bf803e85
```

### `dpkg` source package: `tex-gyre=20180621-7`

Binary Packages:

- `fonts-texgyre=20180621-7`

Licenses: (parsed from: `/usr/share/doc/fonts-texgyre/copyright`)

- `Apache-2.0`
- `DejaVu-License`
- `GPL-2`
- `GPL-2+`
- `GUST-Font-License`

Source:

```console
$ apt-get source -qq --print-uris tex-gyre=20180621-7
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621-7.dsc' tex-gyre_20180621-7.dsc 2245 SHA256:3285ee774b549fe3c52f33c550b9db3625d5242ea4dc095d77a7013a3e3a50b7
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621.orig.tar.gz' tex-gyre_20180621.orig.tar.gz 24033627 SHA256:fe6b0f8ca6890d4a369f36c3b45bc30470069701a2f59042178ad5933fc9cdb8
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621-7.debian.tar.xz' tex-gyre_20180621-7.debian.tar.xz 11832 SHA256:059f978365e54f87321d10fd98d2fe92cb59bff4205f05c536f7e0a0d9c79434
```

### `dpkg` source package: `tiff=4.7.1-1`

Binary Packages:

- `libtiff6:amd64=4.7.1-1`

Licenses: (parsed from: `/usr/share/doc/libtiff6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.7.1-1
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.7.1-1.dsc' tiff_4.7.1-1.dsc 2255 SHA256:073eada2a2c9ed50604fd77d2791975a03d534afc5a364005c21bf382edf821a
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.7.1.orig.tar.bz2' tiff_4.7.1.orig.tar.bz2 2200037 SHA256:7bbeb6ece519e302dc68bb820ae17b9cf071baf30f70a4a6b98e9f72e6d8c1eb
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.7.1-1.debian.tar.xz' tiff_4.7.1-1.debian.tar.xz 22284 SHA256:2154b9653694baeabf09420e881a40fafe0120deedd193d1d11a0017238c6233
```

### `dpkg` source package: `tk8.6=8.6.17-1`

Binary Packages:

- `libtk8.6:amd64=8.6.17-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tk8.6=8.6.17-1
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.17-1.dsc' tk8.6_8.6.17-1.dsc 2155 SHA256:fe1aa840f6229d60e8b3a7ee5f6097298d002da1042d29dc3b683c86ba0de189
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.17.orig.tar.gz' tk8.6_8.6.17.orig.tar.gz 4593109 SHA256:e4982df6f969c08bf9dd858a6891059b4a3f50dc6c87c10abadbbe2fc4838946
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.17-1.debian.tar.xz' tk8.6_8.6.17-1.debian.tar.xz 10820 SHA256:f0f2435c2c2cb1dd97993179aeaa606e63fe87a7972a75b42fb4f7cd9adaf778
```

### `dpkg` source package: `tzdata=2025c-3`

Binary Packages:

- `tzdata=2025c-3`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025c-3
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025c-3.dsc' tzdata_2025c-3.dsc 2434 SHA256:1ca8b94238670a1e91b3148f1ed9510863d291f91e7b08daf764fed779773467
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025c.orig.tar.gz' tzdata_2025c.orig.tar.gz 469363 SHA256:4aa79e4effee53fc4029ffe5f6ebe97937282ebcdf386d5d2da91ce84142f957
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025c.orig.tar.gz.asc' tzdata_2025c.orig.tar.gz.asc 833 SHA256:6d72ec402e89cd426d5e22b28cf6f51bde6fe8e0f6ce2bd1a0129a3108735747
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025c-3.debian.tar.xz' tzdata_2025c-3.debian.tar.xz 127680 SHA256:80e66a654e967167ced72e3461581b8e3379a3a21c347d4184efc789267ef14c
```

### `dpkg` source package: `ucf=3.0052`

Binary Packages:

- `ucf=3.0052`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0052
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0052.dsc' ucf_3.0052.dsc 1512 SHA256:9117f54533d23ad74371e91c3038e13b1aa0fabd51a382f47a5af81e9b5ee591
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0052.tar.xz' ucf_3.0052.tar.xz 71488 SHA256:94130b4840618a65543ca4c12f4de062081008f42f36d0abfbd75098ebe9a7eb
```

### `dpkg` source package: `unzip=6.0-29`

Binary Packages:

- `unzip=6.0-29`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-29
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-29.dsc' unzip_6.0-29.dsc 1464 SHA256:ecc73beeb9a18f354124b87f6713facb726ffd4b732ce7a6e144d073a1e777ae
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA256:036d96991646d0449ed0aa952e4fbe21b476ce994abc276e49d30e686708bd37
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-29.debian.tar.xz' unzip_6.0-29.debian.tar.xz 25876 SHA256:14043e5ea351c02b3bc8676e1e6d20d79b9a690b6d7520e8138ac629cc048417
```

### `dpkg` source package: `util-linux=2.41.3-2`

Binary Packages:

- `bsdutils=1:2.41.3-2`
- `libblkid1:amd64=2.41.3-2`
- `libmount1:amd64=2.41.3-2`
- `libsmartcols1:amd64=2.41.3-2`
- `libuuid1:amd64=2.41.3-2`
- `login=1:4.16.0-2+really2.41.3-2`
- `mount=2.41.3-2`
- `util-linux=2.41.3-2`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `BSLA`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/util-linux/2.41.3-2/


### `dpkg` source package: `vim=2:9.1.1882-1`

Binary Packages:

- `vim-common=2:9.1.1882-1`
- `vim-tiny=2:9.1.1882-1`

Licenses: (parsed from: `/usr/share/doc/vim-common/copyright`, `/usr/share/doc/vim-tiny/copyright`)

- `Apache`
- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-2-clause`
- `BSD-3-clause`
- `Compaq`
- `EDL-1`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `HPND-sell`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OPL-1+`
- `UC`
- `Unlicense`
- `Vim`
- `Vim-Regexp`
- `X11`
- `XPM`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/vim/2:9.1.1882-1/


### `dpkg` source package: `wget=1.25.0-2`

Binary Packages:

- `wget=1.25.0-2`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.25.0-2
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0-2.dsc' wget_1.25.0-2.dsc 2251 SHA256:32caf133042db927360a8c35357e4b2877eb83ff0ca144ceb64508947d894f55
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz' wget_1.25.0.orig.tar.gz 5263736 SHA256:766e48423e79359ea31e41db9e5c289675947a7fcf2efdcedb726ac9d0da3784
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz.asc' wget_1.25.0.orig.tar.gz.asc 854 SHA256:47f0989685931c3df6166061069659bc13a75b221a62041625007fa2dad7411b
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0-2.debian.tar.xz' wget_1.25.0-2.debian.tar.xz 27884 SHA256:45d4411e892d12af710ddff536d2daf430031387e336153f5f996cf536487b90
```

### `dpkg` source package: `xauth=1:1.1.2-1.1`

Binary Packages:

- `xauth=1:1.1.2-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xauth=1:1.1.2-1.1
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.1.dsc' xauth_1.1.2-1.1.dsc 1828 SHA256:042ec790bd830c17bf1fe195d292f4eed29f0e095db1fb4e5156008ddda2ddd1
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2.orig.tar.gz' xauth_1.1.2.orig.tar.gz 214621 SHA256:84d27a1023d8da524c134f424b312e53cb96e08871f96868aa20316bfcbbc054
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.1.diff.gz' xauth_1.1.2-1.1.diff.gz 18218 SHA256:763c20707faf0ba512294c83dcb2df4541e37eeb53eb596af608b0188de5243e
```

### `dpkg` source package: `xdg-utils=1.2.1-2`

Binary Packages:

- `xdg-utils=1.2.1-2`

Licenses: (parsed from: `/usr/share/doc/xdg-utils/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris xdg-utils=1.2.1-2
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.2.1-2.dsc' xdg-utils_1.2.1-2.dsc 2137 SHA256:954ff8314f513926f03677d3ec830b8195eaf7714ba8d80d54547871049d6280
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.2.1.orig.tar.gz' xdg-utils_1.2.1.orig.tar.gz 307637 SHA256:f6b648c064464c2636884c05746e80428110a576f8daacf46ef2e554dcfdae75
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.2.1-2.debian.tar.xz' xdg-utils_1.2.1-2.debian.tar.xz 13612 SHA256:f288e1abb87d0b8a510776d55c5085e8f30ed6459f3f4a07dd9332a8d1162a98
```

### `dpkg` source package: `xft=2.3.6-1`

Binary Packages:

- `libxft2:amd64=2.3.6-1+b4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xft=2.3.6-1
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.dsc' xft_2.3.6-1.dsc 2006 SHA256:252220495bd12fac30d8f1b1994916beaed9c5149138dcc62e230fee17339530
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6.orig.tar.gz' xft_2.3.6.orig.tar.gz 447498 SHA256:b7e59f69e0bbabe9438088775f7e5a7c16a572e58b11f9722519385d38192df5
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.diff.gz' xft_2.3.6-1.diff.gz 17995 SHA256:9d4c64fc52626134a3f753df88fceaba0cb460bd9b56544f0e42178deca77019
```

### `dpkg` source package: `xorg=1:7.7+26`

Binary Packages:

- `x11-common=1:7.7+26`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+26
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b26.dsc' xorg_7.7+26.dsc 1970 SHA256:435390a010511b741e5c9e9a130baa1fc68f1b5c016ca1d2bb267bf71a59d6c8
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b26.tar.xz' xorg_7.7+26.tar.xz 234356 SHA256:60b5827327f725d0a36965f7443f2c8c3488624b1cffa7127394c0cf0bcbd519
```

### `dpkg` source package: `xxhash=0.8.3-2`

Binary Packages:

- `libxxhash0:amd64=0.8.3-2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.3-2
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA256:9d1f7aaace7871fbdb8775d756c6eaca84e6ad5d8e9c6ac465b7e0adc06ff90c
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA256:aae608dfe8213dfd05d909a57718ef82f30722c392344583d3f39050c7f29a80
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA256:13824bfb2b2367225dfe3090d0ae050614f1c470a47db7232a2e9d4b2b14ad31
```

### `dpkg` source package: `xz-utils=5.8.2-1`

Binary Packages:

- `liblzma-dev:amd64=5.8.2-1`
- `liblzma5:amd64=5.8.2-1`
- `xz-utils=5.8.2-1`

Licenses: (parsed from: `/usr/share/doc/liblzma-dev/copyright`, `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

- `0BSD`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3.0-or-later-WITH-Autoconf-exception-macro`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `noderivs`
- `none`
- `permissive-nowarranty`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.8.2-1
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.2-1.dsc' xz-utils_5.8.2-1.dsc 2530 SHA256:87f0db65eab5054173057b9bf90b650175cd5fbce6a7917502320a7106bc5fc6
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.2.orig.tar.xz' xz-utils_5.8.2.orig.tar.xz 1511132 SHA256:890966ec3f5d5cc151077879e157c0593500a522f413ac50ba26d22a9a145214
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.2.orig.tar.xz.asc' xz-utils_5.8.2.orig.tar.xz.asc 877 SHA256:d04e180b3cdf93af5b723d7f52286ecd2b7ffd59cc34f891aab1a30644fb4063
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.2-1.debian.tar.xz' xz-utils_5.8.2-1.debian.tar.xz 24800 SHA256:60f998c2f27eded515f379cb6d73eb4a6846bd60f00eae18065210e1c5823978
```

### `dpkg` source package: `zip=3.0-15`

Binary Packages:

- `zip=3.0-15`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zip=3.0-15
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-15.dsc' zip_3.0-15.dsc 1439 SHA256:1cee3f25b904023d12c46e55628a79328ce21e47e32737358b3cd99233b5bc6d
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0.orig.tar.gz' zip_3.0.orig.tar.gz 1118845 SHA256:f0e8bb1f9b7eb0b01285495a2699df3a4b766784c1765a8f1aeedf63c0806369
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-15.debian.tar.xz' zip_3.0-15.debian.tar.xz 10692 SHA256:6dc1711c67640e8d1dee867ff53e84387ddb980c40885bd088ac98c330bffce9
```

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1+b2`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1+b2`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.dsc' zlib_1.3.dfsg+really1.3.1-1.dsc 2637 SHA256:ede2791e29c1d3b422f9208bdd7edf040c20445ea1e7453a72037576e64fa197
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA256:60dd315c07f616887caa029408308a018ace66e3d142726a97db164b3b8f69fb
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1.debian.tar.xz 16576 SHA256:9ed525955ce9fb0c1b39be8ff98f73450dbfc6305a9a27e6149c8972d38a0a9e
```
