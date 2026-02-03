# `debian:sid`

## Docker Metadata

- Image ID: `sha256:d52c63bfd4d9e476098ea36997cf204fefff98a5d9b2bfa2eefd145ae8ab279d`
- Created: `2026-01-12T00:00:00Z`
- Virtual Size: ~ 118.47 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

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
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA256:1f42130ccb5442fe2db2aee1dcc03c51a31512dd2519a38e8fc9270c5abbc807
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA256:e27b6e194c0a7554595d76f96acdceb800631bdc46c36457b73bc7e4a0c5f2ee
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.3.2-2/ (for browsing the source)
- https://sources.debian.net/src/acl/2.3.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.3.2-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-3.dsc' attr_2.5.2-3.dsc 2576 SHA256:c2ae3e15db059029030ddf4fdac179d8f90d423f2310a6ef8c745ba28ac18b0a
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-3.debian.tar.xz' attr_2.5.2-3.debian.tar.xz 32260 SHA256:153f98c87575277ea021e24dae36293b7738699174438a2060b47e8312b771e3
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.5.2-3/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.5.2-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.5.2-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.1.2-1.dsc' audit_4.1.2-1.dsc 2546 SHA256:5443f3ff043dd30cba1549f93940928d04c90cdc7598741a19f722d4109a7f4b
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.1.2.orig.tar.gz' audit_4.1.2.orig.tar.gz 656095 SHA256:5c638bbeef9adb6c5715d3a60f0f5adb93e9b81633608af13d23c61f5e5db04d
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.1.2-1.debian.tar.xz' audit_4.1.2-1.debian.tar.xz 19712 SHA256:1cb30c0bc4bed825cbac829cec4b840b9d0726dedaf25f57cbc3af9bc7d7bcc2
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:4.1.2-1/ (for browsing the source)
- https://sources.debian.net/src/audit/1:4.1.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:4.1.2-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_14.dsc' base-files_14.dsc 1207 SHA256:5cdce966268b529d7897b088f28d022093f390970eb63541f5e3753ca521c23b
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_14.tar.xz' base-files_14.tar.xz 68388 SHA256:dbb9ebd9278b0507d82c29dff894caf9dfc2b46d35e33a4a1505c96c6c6e54d8
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/14/ (for browsing the source)
- https://sources.debian.net/src/base-files/14/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/14/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.6.8`

Binary Packages:

- `base-passwd=3.6.8`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.8
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.8.dsc' base-passwd_3.6.8.dsc 2044 SHA256:e76e572d2653f2b8eda64c662f5b4310a978ef1fdd039410ace5f6355c3af7d6
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.8.tar.xz' base-passwd_3.6.8.tar.xz 61840 SHA256:fab3d0e6e8b641e116bda9bd5f7a7ed24482384c1513f6a369b506327fbc8dde
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.8/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.8/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.3-1.dsc' bash_5.3-1.dsc 2141 SHA256:48fc3b83911ae279877f37efa489d67e91ce2b62ea7ffd81a9770fbec1949021
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.3.orig.tar.xz' bash_5.3.orig.tar.xz 5571836 SHA256:a70de6bb41f5e192534a5a1836b1d7fad9a8d4818a6e1506d70f38441552c17a
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.3-1.debian.tar.xz' bash_5.3-1.debian.tar.xz 88912 SHA256:e011bc46fc8d3c3a0cf2a349bf7c7da9b2d5237384b3c92297ae8e8181e2b612
```

Other potentially useful URLs:

- https://sources.debian.net/src/bash/5.3-1/ (for browsing the source)
- https://sources.debian.net/src/bash/5.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bash/5.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA256:cd3bfd77254a6b5ef1be144bdc90a0dd374bc8206afd98ba4abf828741b79820
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA256:648ed0dac9a041ba6951e0cca521628aa39947cefee78139f7b934a5dc502095
```

Other potentially useful URLs:

- https://sources.debian.net/src/bzip2/1.0.8-6/ (for browsing the source)
- https://sources.debian.net/src/bzip2/1.0.8-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bzip2/1.0.8-6/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.282.dsc' cdebconf_0.282.dsc 2694 SHA256:eddf49a846ed6e9f4f20cb14975cca7107580c061bc748f2b51dc9d0b7f4ddf7
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.282.tar.xz' cdebconf_0.282.tar.xz 286192 SHA256:7451627f8274a8db0a1d24c3c589ba163036ca79fdb96ed86ddd0157a4369618
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.282/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.282/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.282/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.7-3.dsc' coreutils_9.7-3.dsc 2122 SHA256:c3a207e3aaad165765c7a6fab89045f5fd20035fea6830b9f9ebbb92ebfbff89
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.7.orig.tar.xz' coreutils_9.7.orig.tar.xz 6158960 SHA256:e8bb26ad0293f9b5a1fc43fb42ba970e312c66ce92c1b0b16713d7500db251bf
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.7.orig.tar.xz.asc' coreutils_9.7.orig.tar.xz.asc 833 SHA256:5070e9428bd372a7fa1f66b395b81092bb40c98f9f56a2e2bc55c47fd387e901
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.7-3.debian.tar.xz' coreutils_9.7-3.debian.tar.xz 26820 SHA256:483f77876a080577f63da1d004cc1cf17d16df65d6925aefdd3294c6101eccfb
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/9.7-3/ (for browsing the source)
- https://sources.debian.net/src/coreutils/9.7-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/9.7-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-12.dsc' dash_0.5.12-12.dsc 1460 SHA256:589efc4d87a4ae4745c273bdb33198d7c4f28a71736a8ece81d3677cf9c6e5ce
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-12.debian.tar.xz' dash_0.5.12-12.debian.tar.xz 47300 SHA256:a278acb5d9a1f5d9a086d36a547287cbf3105b8f33c0e62d86d264decf5ba1ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.12-12/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.12-12/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.12-12/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-11.dsc' db5.3_5.3.28+dfsg2-11.dsc 2032 SHA256:0550eb464a02703e35d86fbc4a7ac0736ab30b2a0ebe0818c490f7106d1d4230
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-11.debian.tar.xz' db5.3_5.3.28+dfsg2-11.debian.tar.xz 36580 SHA256:701601b7398c1ff8714594287db6c042b2cbc2e15bc98e85afd77c4324d3e3aa
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-11/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debconf=1.5.91`

Binary Packages:

- `debconf=1.5.91`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.91
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.91.dsc' debconf_1.5.91.dsc 2035 SHA256:1aa3ceaef24ef533cfffe7f9ca750c6325dbaea86a7abca77cb4439ceae930d8
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.91.tar.xz' debconf_1.5.91.tar.xz 609964 SHA256:18f3f43924ccc870be483d7c5f1a9be59e51ae1da403059d654666b5a175bf15
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.91/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.91/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.91/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debian-archive-keyring=2025.1`

Binary Packages:

- `debian-archive-keyring=2025.1`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2025.1
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.dsc' debian-archive-keyring_2025.1.dsc 1267 SHA256:09604bd8d4562a1e942e5d1a19a6b82447cbdeb2e7c7f0df7c32a2503647ea47
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.tar.xz' debian-archive-keyring_2025.1.tar.xz 138248 SHA256:2d019c3fa19c42da4d37571e473c296286dad0214cb3bd5cafd99f04a8bf5471
```

Other potentially useful URLs:

- https://sources.debian.net/src/debian-archive-keyring/2025.1/ (for browsing the source)
- https://sources.debian.net/src/debian-archive-keyring/2025.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debian-archive-keyring/2025.1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.23.2.dsc' debianutils_5.23.2.dsc 1908 SHA256:471b65deec232bb033f3e3e06d5bf64dac0ced474c6fd61d41538f3f3de876f8
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.23.2.tar.xz' debianutils_5.23.2.tar.xz 82376 SHA256:79e524b7526dba2ec5c409d0ee52ebec135815cf5b2907375d444122e0594b69
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/5.23.2/ (for browsing the source)
- https://sources.debian.net/src/debianutils/5.23.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/5.23.2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12-1.dsc' diffutils_3.12-1.dsc 1875 SHA256:eb99be6cc60e71249bd119dfb66ada6a8c0fdd2e1bb8b1325f4801b813ad820c
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz' diffutils_3.12.orig.tar.xz 1938800 SHA256:7c8b7f9fc8609141fdea9cece85249d308624391ff61dedaf528fcb337727dfd
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz.asc' diffutils_3.12.orig.tar.xz.asc 833 SHA256:ad05b321b2f23441275af68072123a5907b05ad989335a9f1f6e3781cb0846a6
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12-1.debian.tar.xz' diffutils_3.12-1.debian.tar.xz 14752 SHA256:ffacb3eb9ad1a8cc90768e13e1d09da1b71cfab3cb99b1e0bd1f0ba26f89dd46
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.12-1/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.23.3`

Binary Packages:

- `dpkg=1.23.3`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.23.3
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.23.3.dsc' dpkg_1.23.3.dsc 3474 SHA256:fc8ea0d894361716bf6ff6e42e6da8f7d60d3798a6d14640fade86ba7774f396
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.23.3.tar.xz' dpkg_1.23.3.tar.xz 5803688 SHA256:57f759b573dfe25602be8f4f0df24d5264367bbd6489741dd767c30dde65ae36
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.23.3/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.23.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.23.3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA256:fa6b67056d9e5b4d8edbfc8ab95ac15ac769b140284426973f6a1ef07a4594ec
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA256:1387e0b67ff247d2abde998f90dfbf70c1491391a59ddfecb8ae698789f0a4f5
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA256:7f53670eea6bd114e014571221eb652855c1129a3ed99f2a9257c2a313cc216f
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA256:7d19668508523a6fcfb7731f5646305a8b1a00a3105ee3f0a5f167adf93a8a46
```

Other potentially useful URLs:

- https://sources.debian.net/src/findutils/4.10.0-3/ (for browsing the source)
- https://sources.debian.net/src/findutils/4.10.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/findutils/4.10.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-15=15.2.0-12`

Binary Packages:

- `gcc-15-base:amd64=15.2.0-12`
- `libgcc-s1:amd64=15.2.0-12`
- `libstdc++6:amd64=15.2.0-12`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-15=15.2.0-12
'http://deb.debian.org/debian/pool/main/g/gcc-15/gcc-15_15.2.0-12.dsc' gcc-15_15.2.0-12.dsc 52289 SHA256:bdcdce7ace72bb100038fc7f80e6e54e639d6c8d82eef7aef53bb7a1b88093fd
'http://deb.debian.org/debian/pool/main/g/gcc-15/gcc-15_15.2.0.orig.tar.gz' gcc-15_15.2.0.orig.tar.gz 100989491 SHA256:3121d3e2821fe21088deb77f11ee786d80969a1c55255386a43ecca1e06b47c0
'http://deb.debian.org/debian/pool/main/g/gcc-15/gcc-15_15.2.0-12.debian.tar.xz' gcc-15_15.2.0-12.debian.tar.xz 2842772 SHA256:47a304bf28549884096c071efb44418ce4507264e3d3f4bee82560bddddc9fdc
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-15/15.2.0-12/ (for browsing the source)
- https://sources.debian.net/src/gcc-15/15.2.0-12/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-15/15.2.0-12/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.42-7`

Binary Packages:

- `libc-bin=2.42-7`
- `libc-gconv-modules-extra:amd64=2.42-7`
- `libc6:amd64=2.42-7`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-gconv-modules-extra/copyright`, `/usr/share/doc/libc6/copyright`)

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
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.42-7.dsc' glibc_2.42-7.dsc 8582 SHA256:e7be4e87e63ea86547b8f8d897c70e7b5a1d8aed9e7d44910cde324528f1a41d
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.42.orig.tar.xz' glibc_2.42.orig.tar.xz 21052916 SHA256:69c1e915c8edd75981cbfc6b7654e8fc4e52a48d06b9f706f463492749a9b6fb
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.42-7.debian.tar.xz' glibc_2.42-7.debian.tar.xz 414240 SHA256:7dd4737238647f4abf649890e30eedf8b8c8a0bc59ef7f956098e7580426d5d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.42-7/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.42-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.42-7/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5.dsc' gmp_6.3.0+dfsg-5.dsc 2230 SHA256:609cad99ebddece1d7028a9c3f0a728c68e5a5fbb15b879a2ea6107ea5b16168
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5.debian.tar.xz' gmp_6.3.0+dfsg-5.debian.tar.xz 20424 SHA256:9a41837b2e2678506c24c2791d3f551fdb61bb01cc5e79aaaf45c68a8f26089a
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-5/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.3.0+dfsg-5/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12-1.dsc' grep_3.12-1.dsc 1647 SHA256:ce35486482abc0591a00be0848c90a3f40ce14b62e501da637296d23bc4c29f4
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12.orig.tar.xz' grep_3.12.orig.tar.xz 1918448 SHA256:2649b27c0e90e632eadcd757be06c6e9a4f48d941de51e7c0f83ff76408a07b9
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12.orig.tar.xz.asc' grep_3.12.orig.tar.xz.asc 833 SHA256:62d4867d7cfff57a364b745866d798958a90286551fdf45d08df515fa8c79c25
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12-1.debian.tar.xz' grep_3.12-1.debian.tar.xz 24160 SHA256:5baef65e599c41285a0393c1c6845c03c9b29f14765447911a1871a50321fd42
```

Other potentially useful URLs:

- https://sources.debian.net/src/grep/3.12-1/ (for browsing the source)
- https://sources.debian.net/src/grep/3.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/grep/3.12-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13-1.dsc' gzip_1.13-1.dsc 1884 SHA256:4942638dbb63dc5690e0a95ed70ee9f11e93565c43941c2485da3e561ec72028
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA256:7454eb6935db17c6655576c2e1b0fabefd38b4d0936e0f87f48cd062ce91a057
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz.asc' gzip_1.13.orig.tar.xz.asc 833 SHA256:aa752d6460fff2e0064857f1c6057d2dc49a28a45ad28c6b29c525851d6771f1
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13-1.debian.tar.xz' gzip_1.13-1.debian.tar.xz 19028 SHA256:29319b3f91d8e03d940d4d7c0f2a5fe5ec4f2ba4a0e621c9ef2682f2d0240dd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/gzip/1.13-1/ (for browsing the source)
- https://sources.debian.net/src/gzip/1.13-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gzip/1.13-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hostname=3.25`

Binary Packages:

- `hostname=3.25`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.25.dsc' hostname_3.25.dsc 1519 SHA256:80aadf116c3423044be69a4cef8ba2766f412bd4d46a500aacb61f303c19c4ef
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.25.tar.xz' hostname_3.25.tar.xz 12804 SHA256:5bb5d1be011158090157c9e7587ae5606c262a5020ecdc5caac6686b9910592e
```

Other potentially useful URLs:

- https://sources.debian.net/src/hostname/3.25/ (for browsing the source)
- https://sources.debian.net/src/hostname/3.25/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hostname/3.25/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.69.dsc' init-system-helpers_1.69.dsc 2234 SHA256:99b681c969728fba085226b1d1fd25cc37c9fe16f9eb5118e679d845b50ae7ee
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.69.tar.xz' init-system-helpers_1.69.tar.xz 45648 SHA256:e246ee7f39b110803e5307fdb25ec2fb5fe0c62dbd9274011803fef50af08100
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.69/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.69/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.69/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA256:01eb1d0c896096f9038213f5f00376ecfd1c0d1def21b7042f28ae070e4837e3
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA256:36c878a32c1f190ca2cb474de5c6139990a6c029906493d3566770b1ebd569bf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libbsd/0.12.2-2/ (for browsing the source)
- https://sources.debian.net/src/libbsd/0.12.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libbsd/0.12.2-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.dsc' libcap-ng_0.8.5-4.dsc 1710 SHA256:a5745b7d68a11068ae5beddcc7fbc94cd87dd81cb2d7495e7d48610603be3526
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.debian.tar.xz' libcap-ng_0.8.5-4.debian.tar.xz 7816 SHA256:f5d4e7f38bdbca87de77317ce95f973883081370ef257019b484e29e3368a20d
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.8.5-4/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.8.5-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.8.5-4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75-10.dsc' libcap2_2.75-10.dsc 2703 SHA256:b7a692cecf4d1975991073b77e7a5e45106d62f428f010284fc44f323f1acce7
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA256:de4e7e064c9ba451d5234dd46e897d7c71c96a9ebf9a0c445bc04f4742d83632
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA256:c71b593e7c3160fd7f406641074d93462bbc4906c9243937a0e232f42d5c54d2
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75-10.debian.tar.xz' libcap2_2.75-10.debian.tar.xz 22964 SHA256:b1eb36e050fa1d03e83df78f35ef8538f05cd3ad96a7362cb4113b2541a390ce
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap2/1:2.75-10/ (for browsing the source)
- https://sources.debian.net/src/libcap2/1:2.75-10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap2/1:2.75-10/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmd/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/libmd/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmd/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libseccomp=2.6.0-2`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2+b1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.dsc' libseccomp_2.6.0-2.dsc 2622 SHA256:d05f94536558d34fa339326c6f958a3357b51efac8234470b5d97b69472db765
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA256:83b6085232d1588c379dc9b9cae47bb37407cf262e6e74993c61ba72d2a784dc
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA256:52e338fa958128293cbd25d2be189e34da41c4f4abbb1b641cf58f373c001f94
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.debian.tar.xz' libseccomp_2.6.0-2.debian.tar.xz 20800 SHA256:ed705ec85719403e77d004c99c0b06b795f090c66fcae265c4bcf37ffea9cc27
```

Other potentially useful URLs:

- https://sources.debian.net/src/libseccomp/2.6.0-2/ (for browsing the source)
- https://sources.debian.net/src/libseccomp/2.6.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libseccomp/2.6.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=3.9-4`

Binary Packages:

- `libselinux1:amd64=3.9-4+b1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.9-4
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.9-4.dsc' libselinux_3.9-4.dsc 2905 SHA256:b16d1fc5b82dbc3a17a6f2891425ac521ea0da22937ea8ae5cef91bd9beadf7d
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz' libselinux_3.9.orig.tar.gz 205334 SHA256:e7ee2c01dba64a0c35c9d7c9c0e06209d8186b325b0638a0d83f915cc3c101e8
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz.asc' libselinux_3.9.orig.tar.gz.asc 833 SHA256:3529c5a905fdfa9e0a8e926ce0333f508213cccd9f6e35ca1011e37412042ca5
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.9-4.debian.tar.xz' libselinux_3.9-4.debian.tar.xz 38096 SHA256:662b33b6d14a591910391f013fb62ee0ef9e8bad055d6d632a23a3c3b8450dd7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/3.9-4/ (for browsing the source)
- https://sources.debian.net/src/libselinux/3.9-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/3.9-4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.9-1.dsc' libsemanage_3.9-1.dsc 2965 SHA256:68069c6d39a80c09d3179d4ed69ba1bf9dc41fd4b635f548570836827b478752
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.9.orig.tar.gz' libsemanage_3.9.orig.tar.gz 185278 SHA256:ec05850aef48bfb8e02135a7f4f3f7edba3670f63d5e67f2708d4bd80b9a4634
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.9.orig.tar.gz.asc' libsemanage_3.9.orig.tar.gz.asc 833 SHA256:af7644b29d7ae1f69f89444900b2e2b0eb0b4e71f10a2667c7820d10d55fa53f
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.9-1.debian.tar.xz' libsemanage_3.9-1.debian.tar.xz 38028 SHA256:7982b2652b5a3b73b8dd6ec2cf901d02b1f78fc620861db437aea26f5a1b9654
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.9-1/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.9-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.9-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.9-2.dsc' libsepol_3.9-2.dsc 2326 SHA256:fca98e9732bd9385e689f1b3bec87517a938217d5e3bf735cd88b9ee5c971850
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz' libsepol_3.9.orig.tar.gz 515726 SHA256:ba630b59e50c5fbf9e9dd45eb3734f373cf78d689d8c10c537114c9bd769fa2e
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz.asc' libsepol_3.9.orig.tar.gz.asc 833 SHA256:2059e9c2e195f8d4102f9868295b0a2c16e91082b236d510499dc27620b812fd
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.9-2.debian.tar.xz' libsepol_3.9-2.debian.tar.xz 21416 SHA256:f4f7f317fccf7dac9c72f1448a335edcf10ea7894f3492c475e76d404fcfb268
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsepol/3.9-2/ (for browsing the source)
- https://sources.debian.net/src/libsepol/3.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsepol/3.9-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcrypt=1:4.5.1-1`

Binary Packages:

- `libcrypt1:amd64=1:4.5.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.5.1-1
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.dsc' libxcrypt_4.5.1-1.dsc 2434 SHA256:c9051653fc74d9209e8a3f8b496c359cfecdf7992b0a73f69c090973bae90e4b
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1.orig.tar.xz' libxcrypt_4.5.1.orig.tar.xz 433264 SHA256:bddf278d44e2ecdbf1439a52ddc0bb292921dd9f3013030a2a8461c32a45533f
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.debian.tar.xz' libxcrypt_4.5.1-1.debian.tar.xz 8684 SHA256:b6096f6498adf5a94d727c9065ed33b784190e8c2cd3eda5f073e435708293ae
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcrypt/1:4.5.1-1/ (for browsing the source)
- https://sources.debian.net/src/libxcrypt/1:4.5.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcrypt/1:4.5.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libzstd=1.5.7+dfsg-3`

Binary Packages:

- `libzstd1:amd64=1.5.7+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-3
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.dsc' libzstd_1.5.7+dfsg-3.dsc 2490 SHA256:e32b7bb90ac7b312238add6abb77023cec6f59385b1c9a78b41b69ea2ef5001a
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA256:0c092ef267edce57ba7f3f2645c861f72eaf5e76273c6c3632869423464b90a5
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.debian.tar.xz' libzstd_1.5.7+dfsg-3.debian.tar.xz 23164 SHA256:ada18b02a46878f2f0a845fd003179ab9591f7f96f0b984db06a024ab46ae81f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libzstd/1.5.7+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/libzstd/1.5.7+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libzstd/1.5.7+dfsg-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-6.dsc' lz4_1.10.0-6.dsc 1941 SHA256:990687371c2426db24e74922a4e19cb7666e321031409ca33bc1dda858ee503e
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA256:537512904744b35e232912055ccf8ec66d768639ff3abe5788d90d792ec5f48b
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-6.debian.tar.xz' lz4_1.10.0-6.debian.tar.xz 9236 SHA256:edd2f342f469dbb24452fca50a65e323be12047aeeaad4d188faae57a38d57a0
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/1.10.0-6/ (for browsing the source)
- https://sources.debian.net/src/lz4/1.10.0-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/1.10.0-6/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131-2.dsc' mawk_1.3.4.20250131-2.dsc 2969 SHA256:e0b020dbf75a7aa312b6938034c3e6c971b5d22dad1dccc43e42da918611650c
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz' mawk_1.3.4.20250131.orig.tar.gz 433213 SHA256:51bcb82d577b141d896d9d9c3077d7aaa209490132e9f2b9573ba8511b3835be
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz.asc' mawk_1.3.4.20250131.orig.tar.gz.asc 729 SHA256:bc83f127727edb42a91d516770c8d0d3cdb5f6e541aa3cb5213b79dae494db95
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131-2.debian.tar.xz' mawk_1.3.4.20250131-2.debian.tar.xz 16120 SHA256:aa9eb515b394eec97cdf28e0c3e52ec4519d63c42701bbc747613cf044d9271c
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.4.20250131-2/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.4.20250131-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.4.20250131-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.6+20251231-1`

Binary Packages:

- `libtinfo6:amd64=6.6+20251231-1`
- `ncurses-base=6.6+20251231-1`
- `ncurses-bin=6.6+20251231-1`

Licenses: (parsed from: `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.6+20251231-1
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.dsc' ncurses_6.6+20251231-1.dsc 4163 SHA256:1c7b340d53b1fc75df31bc219e6395c7d6474348b2ec968098c1a0cc7cecfe0e
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz' ncurses_6.6+20251231.orig.tar.gz 3789898 SHA256:e280541f4f601b8586bec305976c873fd641607f9bc4254bf661034dcccac4e9
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz.asc' ncurses_6.6+20251231.orig.tar.gz.asc 729 SHA256:ccb61134c7ffd365aa1f7f3afc3dadaadbda3a46aee463b289c9d0dddb2e9bd3
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.debian.tar.xz' ncurses_6.6+20251231-1.debian.tar.xz 50852 SHA256:fd4a1fd7113e034175310bda8f4589854a0f66fe70482a6bd553de73d773303c
```

Other potentially useful URLs:

- https://sources.debian.net/src/ncurses/6.6+20251231-1/ (for browsing the source)
- https://sources.debian.net/src/ncurses/6.6+20251231-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ncurses/6.6+20251231-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2-1.dsc' nettle_3.10.2-1.dsc 2297 SHA256:e2f713973191da5d021759173f2176c21abb5f9420df45cd93a8ff058d62493f
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz' nettle_3.10.2.orig.tar.gz 2644644 SHA256:fe9ff51cb1f2abb5e65a6b8c10a92da0ab5ab6eaf26e7fc2b675c45f1fb519b5
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz.asc' nettle_3.10.2.orig.tar.gz.asc 573 SHA256:3496de6ba5685733aaab2e4e611ea5860fdd76964c56c995f5a0b4c2ec5084ae
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2-1.debian.tar.xz' nettle_3.10.2-1.debian.tar.xz 25052 SHA256:6f5be658d8bfbc5ffd3c75bd15b8a40fd51c5dd4ae10519d7835be135944f0a7
```

Other potentially useful URLs:

- https://sources.debian.net/src/nettle/3.10.2-1/ (for browsing the source)
- https://sources.debian.net/src/nettle/3.10.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nettle/3.10.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=3.5.4-1`

Binary Packages:

- `libssl3t64:amd64=3.5.4-1`
- `openssl-provider-legacy=3.5.4-1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.5.4-1
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.5.4-1.dsc' openssl_3.5.4-1.dsc 2637 SHA256:35e7e427f8ba3660b77ef5408433b748f7e9070eade4ba0e9452b13bd078ca23
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.5.4.orig.tar.gz' openssl_3.5.4.orig.tar.gz 53190367 SHA256:967311f84955316969bdb1d8d4b983718ef42338639c621ec4c34fddef355e99
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.5.4.orig.tar.gz.asc' openssl_3.5.4.orig.tar.gz.asc 833 SHA256:cfcabcfc6e43237392e0ab42e2326fceb71037036c2adaa7ecc7e251778e38f4
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.5.4-1.debian.tar.xz' openssl_3.5.4-1.debian.tar.xz 48888 SHA256:17fc0e9b7df7bb5a5d33755c1efdc18b74a93affc47f5d9b62c4c8b17337be81
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/3.5.4-1/ (for browsing the source)
- https://sources.debian.net/src/openssl/3.5.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/3.5.4-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-5.dsc' pam_1.7.0-5.dsc 2210 SHA256:5c127aa18c7cb52ec9ee91fa2099453b3a851bcc0088e79045384a2a508b341c
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA256:57dcd7a6b966ecd5bbd95e1d11173734691e16b68692fa59661cdae9b13b1697
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA256:7a8ea18ec7d9dd1f8cbf9055c32128cbca8241aa63e9fea44d56ce6f0e15e441
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-5.debian.tar.xz' pam_1.7.0-5.debian.tar.xz 145640 SHA256:d776d7cb6fc8b08273f96b7f843299356ef13c6756e30468c594ab28faf1701c
```

Other potentially useful URLs:

- https://sources.debian.net/src/pam/1.7.0-5/ (for browsing the source)
- https://sources.debian.net/src/pam/1.7.0-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pam/1.7.0-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pcre2=10.46-1`

Binary Packages:

- `libpcre2-8-0:amd64=10.46-1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.46-1
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.46-1.dsc' pcre2_10.46-1.dsc 2337 SHA256:f07e05cd55dd8189d1a7eec2c3ed2d963f51a84ab5494567a112b42f8d525661
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.46.orig.tar.gz' pcre2_10.46.orig.tar.gz 2718545 SHA256:8d28d7f2c3b970c3a4bf3776bcbb5adfc923183ce74bc8df1ebaad8c1985bd07
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.46-1.diff.gz' pcre2_10.46-1.diff.gz 8748 SHA256:307f2b889eb62e71fba064fb6ec65a367f1a88ceb667c4d7109c8d3fe1859e88
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre2/10.46-1/ (for browsing the source)
- https://sources.debian.net/src/pcre2/10.46-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre2/10.46-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `perl=5.40.1-7`

Binary Packages:

- `perl-base=5.40.1-7`

Licenses: (parsed from: `/usr/share/doc/perl-base/copyright`)

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
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1-7.dsc' perl_5.40.1-7.dsc 2372 SHA256:b74d67b039d7bb2c2c63b0928fae9269f4c025ef6d09254af196827388ff885a
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA256:4ea023d08101443f6ed9dc3bdd9bb5f5e08087678dc9e443d195df22da36209a
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA256:dfa20c2eef2b4af133525610bbb65dd13777ecf998c9c5b1ccf0d308e732ee3f
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1-7.debian.tar.xz' perl_5.40.1-7.debian.tar.xz 172940 SHA256:d9a0b6e8466e0b2061e6fe7605e1f316a86a8e2a95fb3ed7f9e91e698ff002cc
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.40.1-7/ (for browsing the source)
- https://sources.debian.net/src/perl/5.40.1-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.40.1-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rust-sequoia-sqv=1.3.0-5`

Binary Packages:

- `sqv=1.3.0-5`

Licenses: (parsed from: `/usr/share/doc/sqv/copyright`)

- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sqv=1.3.0-5
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-5.dsc' rust-sequoia-sqv_1.3.0-5.dsc 2630 SHA256:dd766214353afb35bc610df910323263abd79da52e9ed7d003858e4db3c590ac
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0.orig.tar.gz' rust-sequoia-sqv_1.3.0.orig.tar.gz 140759 SHA256:8924571d26720b245292ad3c450e4061fcb24890461874790549747bffa35e60
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-5.debian.tar.xz' rust-sequoia-sqv_1.3.0-5.debian.tar.xz 3944 SHA256:ddff90296cb649bd9408e801f9f8cca28a36e63c7e2bab8db8c8716043152b3d
```

Other potentially useful URLs:

- https://sources.debian.net/src/rust-sequoia-sqv/1.3.0-5/ (for browsing the source)
- https://sources.debian.net/src/rust-sequoia-sqv/1.3.0-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rust-sequoia-sqv/1.3.0-5/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA256:17f10deac1b327cb2a623352cdc33444ac9c109359a0caa46b3980b0e415f671
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA256:549fa5cec6eb4fde8cc74ca263b8bf42f947ede677e39d2afeedf661da1d4e52
```

Other potentially useful URLs:

- https://sources.debian.net/src/sed/4.9-2/ (for browsing the source)
- https://sources.debian.net/src/sed/4.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sed/4.9-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `shadow=1:4.19.0-4`

Binary Packages:

- `login.defs=1:4.19.0-4`
- `passwd=1:4.19.0-4`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/shadow/1:4.19.0-4/


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
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_259-1.dsc' systemd_259-1.dsc 8690 SHA256:6c7fa02ae6215a7240b8087269e77abc3d422ba7934490b88de3aeba227653ee
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_259.orig.tar.gz' systemd_259.orig.tar.gz 17250241 SHA256:a84123692d1add7f9c48fd11cdf5f901393008c2d2ade667c18f25a20bf1290d
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_259-1.debian.tar.xz' systemd_259-1.debian.tar.xz 185568 SHA256:a7d59268e759334bdc6d32fb32f8ad0ca91d31471399a2f1c8d0aa19dcab6e97
```

Other potentially useful URLs:

- https://sources.debian.net/src/systemd/259-1/ (for browsing the source)
- https://sources.debian.net/src/systemd/259-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/systemd/259-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.15-6.dsc' sysvinit_3.15-6.dsc 2382 SHA256:07f2bb807af3823e2b1fc7f202b4ad6b4701cfb51f7e5fe586a13473e68c03a8
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.15.orig.tar.gz' sysvinit_3.15.orig.tar.gz 516469 SHA256:0979dd582056130a45bf70738260fb7f3da5cca989509b1e37ad5ad1d4cbe0bf
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.15-6.debian.tar.xz' sysvinit_3.15-6.debian.tar.xz 122884 SHA256:c5114a70a202cd5570c03c9834ae222aac343e9aac8428e0e910210870efacac
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.15-6/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.15-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.15-6/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.dsc' tar_1.35+dfsg-3.1.dsc 2017 SHA256:5bb58d4966d94c99a9f1b182676089ecc05058d62fdb927f5c07539d9cda4077
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.debian.tar.xz' tar_1.35+dfsg-3.1.debian.tar.xz 21540 SHA256:0d0278034b82ed84dce04a461879b6e1871e4cb416a0ff04d3d35ff05fc30a53
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.35+dfsg-3.1/ (for browsing the source)
- https://sources.debian.net/src/tar/1.35+dfsg-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.35+dfsg-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tzdata=2025c-3`

Binary Packages:

- `tzdata=2025c-3`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025c-3
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025c-3.dsc' tzdata_2025c-3.dsc 2434 SHA256:1ca8b94238670a1e91b3148f1ed9510863d291f91e7b08daf764fed779773467
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025c.orig.tar.gz' tzdata_2025c.orig.tar.gz 469363 SHA256:4aa79e4effee53fc4029ffe5f6ebe97937282ebcdf386d5d2da91ce84142f957
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025c.orig.tar.gz.asc' tzdata_2025c.orig.tar.gz.asc 833 SHA256:6d72ec402e89cd426d5e22b28cf6f51bde6fe8e0f6ce2bd1a0129a3108735747
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025c-3.debian.tar.xz' tzdata_2025c-3.debian.tar.xz 127680 SHA256:80e66a654e967167ced72e3461581b8e3379a3a21c347d4184efc789267ef14c
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2025c-3/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2025c-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2025c-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `util-linux=2.41.3-3`

Binary Packages:

- `bsdutils=1:2.41.3-3`
- `libblkid1:amd64=2.41.3-3`
- `libmount1:amd64=2.41.3-3`
- `libsmartcols1:amd64=2.41.3-3`
- `libuuid1:amd64=2.41.3-3`
- `login=1:4.16.0-2+really2.41.3-3`
- `mount=2.41.3-3`
- `util-linux=2.41.3-3`

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

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.41.3-3
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.41.3-3.dsc' util-linux_2.41.3-3.dsc 5332 SHA256:3f12e1fd7eafe52e8c4765aa1b1b4850f3b0153f7a8a5646210f1cfacc4415d2
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.41.3.orig.tar.xz' util-linux_2.41.3.orig.tar.xz 9467224 SHA256:3330d873f0fceb5560b89a7dc14e4f3288bbd880e96903ed9b50ec2b5799e58b
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.41.3-3.debian.tar.xz' util-linux_2.41.3-3.debian.tar.xz 108832 SHA256:b952a76225e9c52782dae94ad21e104452cff1f7b9bcc8dad9dbae6fb9f42c57
```

Other potentially useful URLs:

- https://sources.debian.net/src/util-linux/2.41.3-3/ (for browsing the source)
- https://sources.debian.net/src/util-linux/2.41.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/util-linux/2.41.3-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA256:9d1f7aaace7871fbdb8775d756c6eaca84e6ad5d8e9c6ac465b7e0adc06ff90c
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA256:aae608dfe8213dfd05d909a57718ef82f30722c392344583d3f39050c7f29a80
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA256:13824bfb2b2367225dfe3090d0ae050614f1c470a47db7232a2e9d4b2b14ad31
```

Other potentially useful URLs:

- https://sources.debian.net/src/xxhash/0.8.3-2/ (for browsing the source)
- https://sources.debian.net/src/xxhash/0.8.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xxhash/0.8.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xz-utils=5.8.2-1`

Binary Packages:

- `liblzma5:amd64=5.8.2-1`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

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
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.8.2-1.dsc' xz-utils_5.8.2-1.dsc 2530 SHA256:87f0db65eab5054173057b9bf90b650175cd5fbce6a7917502320a7106bc5fc6
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.8.2.orig.tar.xz' xz-utils_5.8.2.orig.tar.xz 1511132 SHA256:890966ec3f5d5cc151077879e157c0593500a522f413ac50ba26d22a9a145214
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.8.2.orig.tar.xz.asc' xz-utils_5.8.2.orig.tar.xz.asc 877 SHA256:d04e180b3cdf93af5b723d7f52286ecd2b7ffd59cc34f891aab1a30644fb4063
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.8.2-1.debian.tar.xz' xz-utils_5.8.2-1.debian.tar.xz 24800 SHA256:60f998c2f27eded515f379cb6d73eb4a6846bd60f00eae18065210e1c5823978
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.8.2-1/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.8.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.8.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1+b2`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.dsc' zlib_1.3.dfsg+really1.3.1-1.dsc 2637 SHA256:ede2791e29c1d3b422f9208bdd7edf040c20445ea1e7453a72037576e64fa197
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA256:60dd315c07f616887caa029408308a018ace66e3d142726a97db164b3b8f69fb
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1.debian.tar.xz 16576 SHA256:9ed525955ce9fb0c1b39be8ff98f73450dbfc6305a9a27e6149c8972d38a0a9e
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.3.dfsg+really1.3.1-1/ (for access to the source package after it no longer exists in the archive)
