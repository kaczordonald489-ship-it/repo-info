# `ros:jazzy-perception`

## Docker Metadata

- Image ID: `sha256:3973d7319306a198fd47dc52345b0077ae0976903622b204edca944271fda958`
- Created: `2026-01-16T02:18:48.015261422Z`
- Virtual Size: ~ 3.46 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/ros_entrypoint.sh"]`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LANG=C.UTF-8`
  - `LC_ALL=C.UTF-8`
  - `ROS_DISTRO=jazzy`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=24.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-1build1.1`

Binary Packages:

- `libacl1:amd64=2.3.2-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-1build1.1.dsc' acl_2.3.2-1build1.1.dsc 2616 SHA512:484c1b046c3d1fa9fc2837cb0612da89ea65fab4ed823ac41b0d7b3fc5deb12d1a30208e24ccc04ae9529a105ddd36d8ead48c22eb14df37f97b1d9e05dfb7bb
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA512:c2d061dbfd28c00cecbc1ae614d67f3138202bf4d39b383f2df4c6a8b10b830f33acec620fb211f268478737dde4037d338a5823af445253cb088c48a135099b
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA512:a425b385e3ce30e7146cf8b143ca269e3edd78af82a21dea76d10ea68215f9abcfb1ed8be24ce3b6dce24e6640df8d5d5f365a47399e37006a66c6a62a41fe41
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-1build1.1.debian.tar.xz' acl_2.3.2-1build1.1.debian.tar.xz 23472 SHA512:02e1eadeccb773f30f67c40aaf9cef3401cd771870c7aa82e94bcfbdf3f885879abec23a79ad8103e559dcd02b5ab7b92633890040d2b4db1f984a2a4c4aa232
```

### `dpkg` source package: `adduser=3.137ubuntu1`

Binary Packages:

- `adduser=3.137ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `adwaita-icon-theme=46.0-1`

Binary Packages:

- `adwaita-icon-theme=46.0-1`

Licenses: (parsed from: `/usr/share/doc/adwaita-icon-theme/copyright`)

- `CC-BY-3.0-US`
- `CC-BY-SA-2.0-IT`
- `CC-BY-SA-2.0-IT,`
- `CC-BY-SA-3.0`
- `CC-BY-SA-3.0-US`
- `CC-BY-SA-3.0-Unported`
- `CC-BY-SA-4.0`
- `GFDL-1.2`
- `GFDL-1.2+`
- `GPL`
- `GPL-2`
- `GPL-3`
- `GPL-3+`
- `GPL-unspecified`
- `LGPL-3`
- `LGPL-3,`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/adwaita-icon-theme/46.0-1/


### `dpkg` source package: `alsa-lib=1.2.11-1ubuntu0.1`

Binary Packages:

- `libasound2-data=1.2.11-1ubuntu0.1`
- `libasound2t64:amd64=1.2.11-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libasound2-data/copyright`, `/usr/share/doc/libasound2t64/copyright`)

- `LGPL-2.1`
- `LPGL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris alsa-lib=1.2.11-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.11-1ubuntu0.1.dsc' alsa-lib_1.2.11-1ubuntu0.1.dsc 3034 SHA512:9d3365367d31026c5270766f00ca42b5c0ed7763703fd2ee014b53ad331152915ea2a7583bbc3521f8e4afde9a8c3cd35a30ff7a4b0af9966bf4ae8dfb645fc2
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.11.orig.tar.bz2' alsa-lib_1.2.11.orig.tar.bz2 1107150 SHA512:7bf2c541dff5262c0302a1c716ca10cdb5105f4e0ad48f3341c3c7e975b0c3ea835a298a05974c3e216a85912c368d8025ba3cdda3ff04a7683133ce5b2a286d
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.11.orig.tar.bz2.asc' alsa-lib_1.2.11.orig.tar.bz2.asc 833 SHA512:22ebba05f37ffe8e38644907e9037379c826ff36940f0c5a96f1c7abd5c2a87109899c362e242d12f079251b8423b8234ae4b333feddad5e220351828e30c732
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.11-1ubuntu0.1.debian.tar.xz' alsa-lib_1.2.11-1ubuntu0.1.debian.tar.xz 33912 SHA512:a0ffe096b22003213378d62414301f750d9e1e75ac6ff55398ee776527fdefa199a1419bddaa85a7d85e1525c414fec3579ad86b9592356ada2cde514b00a69d
```

### `dpkg` source package: `ann=1.1.2+doc-9build1`

Binary Packages:

- `libann0=1.1.2+doc-9build1`

Licenses: (parsed from: `/usr/share/doc/libann0/copyright`)

- `GPL-3`
- `GPL-3.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `aom=3.8.2-2ubuntu0.1`

Binary Packages:

- `libaom-dev:amd64=3.8.2-2ubuntu0.1`
- `libaom3:amd64=3.8.2-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libaom-dev/copyright`, `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.8.2-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.8.2-2ubuntu0.1.dsc' aom_3.8.2-2ubuntu0.1.dsc 2395 SHA512:4a21de7415dbb23550b17ebebb98e443a20f3b811ee4e3d5da4995377fc308e6523f4f906aa77ad459e1aee8e8fad36348e45799277a98569fa367088455989f
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.8.2.orig.tar.gz' aom_3.8.2.orig.tar.gz 5466676 SHA512:fca573bab8653fb99773377444c8890325ba0ba4d2cde7cdcbd5aba3465859b297df3ba9343f5917a46284413743efb0730646ac720bb4abf8324875103ab2e7
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.8.2-2ubuntu0.1.debian.tar.xz' aom_3.8.2-2ubuntu0.1.debian.tar.xz 22776 SHA512:cf01fad7c9c05a65ccabc046e91305612c8b9311502f51a09cf07e99296ef3900c85fb5bd18e7ab6cc5b562efdb6ba18a4c18c922f4d6aa6364950e16fd6ad25
```

### `dpkg` source package: `apparmor=4.0.1really4.0.1-0ubuntu0.24.04.5`

Binary Packages:

- `libapparmor1:amd64=4.0.1really4.0.1-0ubuntu0.24.04.5`

Licenses: (parsed from: `/usr/share/doc/libapparmor1/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris apparmor=4.0.1really4.0.1-0ubuntu0.24.04.5
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_4.0.1really4.0.1-0ubuntu0.24.04.5.dsc' apparmor_4.0.1really4.0.1-0ubuntu0.24.04.5.dsc 3434 SHA512:5e59f2649b7dd5c1da7e2e73d6d79bff79ac09173383744834f761d06ce2780c79df260cfebb6be869735dd8dc10f020adb458308ae72d3df5aad195e64199e1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_4.0.1really4.0.1.orig.tar.gz' apparmor_4.0.1really4.0.1.orig.tar.gz 6984984 SHA512:5e569c3f6adc7b72cd61c65c54a5c3686647eb535bf11e0ceb888e8a093f317fa49df598131493af6ec807011459286516df0170788d02fc73e3a70f218a1923
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_4.0.1really4.0.1-0ubuntu0.24.04.5.debian.tar.xz' apparmor_4.0.1really4.0.1-0ubuntu0.24.04.5.debian.tar.xz 125184 SHA512:fc666a9f487ab9be16ee18977c58ceb04db8632bfce8c4ccd23b2e7a0e02f16e8943576bb59304dce6e807f79eeb25deb9922bf7d82b1d63e9784970e98aa964
```

### `dpkg` source package: `apt=2.8.3`

Binary Packages:

- `apt=2.8.3`
- `libapt-pkg6.0t64:amd64=2.8.3`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.8.3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.8.3.dsc' apt_2.8.3.dsc 2973 SHA512:02223363e56b43eb224e418f9ff470228777eaac1355c787b0e648e4eae0686d3aa38f28aaf95ad75007f2529b32d5fb535024dd2a634b3fad014c95de0f33a0
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.8.3.tar.xz' apt_2.8.3.tar.xz 2354680 SHA512:bb79bdeb9a0685efd3e9dd2e491001445ebdbccd889ab4c05c2eb0c048117f769bab86ce4a1889acd426222f2eae97fa43aa83a8227690ca061ce25787343c25
```

### `dpkg` source package: `argon2=0~20190702+dfsg-4build1`

Binary Packages:

- `libargon2-1:amd64=0~20190702+dfsg-4build1`

Licenses: (parsed from: `/usr/share/doc/libargon2-1/copyright`)

- `Apache-2.0`
- `CC0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `armadillo=1:12.6.7+dfsg-1build2`

Binary Packages:

- `libarmadillo-dev=1:12.6.7+dfsg-1build2`
- `libarmadillo12=1:12.6.7+dfsg-1build2`

Licenses: (parsed from: `/usr/share/doc/libarmadillo-dev/copyright`, `/usr/share/doc/libarmadillo12/copyright`)

- `Apache`
- `Apache-2.0`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `arpack=3.9.1-1.1build2`

Binary Packages:

- `libarpack2-dev:amd64=3.9.1-1.1build2`
- `libarpack2t64:amd64=3.9.1-1.1build2`

Licenses: (parsed from: `/usr/share/doc/libarpack2-dev/copyright`, `/usr/share/doc/libarpack2t64/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `at-spi2-core=2.52.0-1build1`

Binary Packages:

- `at-spi2-common=2.52.0-1build1`
- `libatk-bridge2.0-0t64:amd64=2.52.0-1build1`
- `libatk1.0-0t64:amd64=2.52.0-1build1`
- `libatspi2.0-0t64:amd64=2.52.0-1build1`

Licenses: (parsed from: `/usr/share/doc/at-spi2-common/copyright`, `/usr/share/doc/libatk-bridge2.0-0t64/copyright`, `/usr/share/doc/libatk1.0-0t64/copyright`, `/usr/share/doc/libatspi2.0-0t64/copyright`)

- `AFL-2.1`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `attr=1:2.5.2-1build1.1`

Binary Packages:

- `libattr1:amd64=1:2.5.2-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build1.1.dsc' attr_2.5.2-1build1.1.dsc 2588 SHA512:14b89e51d44ebe63fffb1b060ec9106b8a7724f6373b095bf1a31c7da73e835be5a97f7210d1a7709e4513acab3360f423d32ef1acb519124b31165ea6674bc8
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build1.1.debian.tar.xz' attr_2.5.2-1build1.1.debian.tar.xz 26032 SHA512:768a95c9ecf2d2ecd5081f28a1e9982f1222bb437a3e93af44c1ffb4b24fb61c8a43ef78fc7f2ffc80f47c020db005e361f4bf83425d83a43e3de8b82ea40c68
```

### `dpkg` source package: `audit=1:3.1.2-2.1build1.1`

Binary Packages:

- `libaudit-common=1:3.1.2-2.1build1.1`
- `libaudit1:amd64=1:3.1.2-2.1build1.1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.1.2-2.1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.1build1.1.dsc' audit_3.1.2-2.1build1.1.dsc 2848 SHA512:3e54e808c6130829a386f25a3a40a35ae1598955407ca5eb1c400cabe4226da47688c0970e35bba4d841c73f3c625cce08130982657d9c5debdf98d78b717fb6
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA512:a97003a294ed3671df01e2952688e7d5eef59a35f6891feb53e67c4c7eab9ae8c2d18de41a5b5b20e0ad7156fac93aec05f32f6bc5eea706b42b6f27f676446a
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.1build1.1.debian.tar.xz' audit_3.1.2-2.1build1.1.debian.tar.xz 18860 SHA512:0d536e42718911a3b237816d67a1cb05f0c4e591dcf6aa2e17a657711e27b523bb8f79e06c895a107f0fa0039bdc192cfffd16f7b0c17eced8102bd902ac16e7
```

### `dpkg` source package: `autoconf=2.71-3`

Binary Packages:

- `autoconf=2.71-3`

Licenses: (parsed from: `/usr/share/doc/autoconf/copyright`)

- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Texinfo exception`
- `MIT-X-Consortium`
- `no-modification`
- `other`
- `permissive`
- `permissive-long-disclaimer`
- `permissive-short-disclaimer`
- `permissive-without-disclaimer`
- `permissive-without-notices-or-disclaimer`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/autoconf/2.71-3/


### `dpkg` source package: `automake-1.16=1:1.16.5-1.3ubuntu1`

Binary Packages:

- `automake=1:1.16.5-1.3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/automake/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `autotools-dev=20220109.1`

Binary Packages:

- `autotools-dev=20220109.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/autotools-dev/20220109.1/


### `dpkg` source package: `avahi=0.8-13ubuntu6`

Binary Packages:

- `libavahi-client3:amd64=0.8-13ubuntu6`
- `libavahi-common-data:amd64=0.8-13ubuntu6`
- `libavahi-common3:amd64=0.8-13ubuntu6`

Licenses: (parsed from: `/usr/share/doc/libavahi-client3/copyright`, `/usr/share/doc/libavahi-common-data/copyright`, `/usr/share/doc/libavahi-common3/copyright`)

- `GPL`
- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-files=13ubuntu10.3`

Binary Packages:

- `base-files=13ubuntu10.3`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=13ubuntu10.3
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu10.3.dsc' base-files_13ubuntu10.3.dsc 1377 SHA512:616eacb8d3217d4c3e8a57f5f3561411933ffdf680a4161cdf96cc39494f093933667d59263e77db92725ccfbf22fbbc60f0b6c94fce853a3e15d5e046e8b3fb
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu10.3.tar.xz' base-files_13ubuntu10.3.tar.xz 94184 SHA512:9fe21ced2bbb578c164f7cd60e6068a7b66d5e62848b6e7b2ea5670fba48d692a0ab477210bbcc92e41ce16b4ae589784c7168979b5b2727a16c4d1df5f8b22b
```

### `dpkg` source package: `base-passwd=3.6.3build1`

Binary Packages:

- `base-passwd=3.6.3build1`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bash=5.2.21-2ubuntu4`

Binary Packages:

- `bash=5.2.21-2ubuntu4`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `binutils=2.42-4ubuntu2.8`

Binary Packages:

- `binutils=2.42-4ubuntu2.8`
- `binutils-common:amd64=2.42-4ubuntu2.8`
- `binutils-x86-64-linux-gnu=2.42-4ubuntu2.8`
- `libbinutils:amd64=2.42-4ubuntu2.8`
- `libctf-nobfd0:amd64=2.42-4ubuntu2.8`
- `libctf0:amd64=2.42-4ubuntu2.8`
- `libgprofng0:amd64=2.42-4ubuntu2.8`
- `libsframe1:amd64=2.42-4ubuntu2.8`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.42-4ubuntu2.8
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.8.dsc' binutils_2.42-4ubuntu2.8.dsc 10148 SHA512:be5a842fcc21200b65dac1f276a61edab9107ce3720e0f8742125d07e4244e4040718719a84ff6c5daeb0b1c2575a57b1c4f824dc996bd4dd8271c4613fb1adc
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42.orig.tar.xz' binutils_2.42.orig.tar.xz 27567160 SHA512:155f3ba14cd220102f4f29a4f1e5cfee3c48aa03b74603460d05afb73c70d6657a9d87eee6eb88bf13203fe6f31177a5c9addc04384e956e7da8069c8ecd20a6
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.8.debian.tar.xz' binutils_2.42-4ubuntu2.8.debian.tar.xz 189180 SHA512:3d7e00b2e49b6b50293fbf2933dfaa98f5ed9f290d807507bdc1f7e361248c45eefe48207c3f4e20340fcfa1d7e1d28bad2c148d36e30a573cb0ea6fac4fb0d5
```

### `dpkg` source package: `boost-defaults=1.83.0.1ubuntu2`

Binary Packages:

- `libboost-all-dev=1.83.0.1ubuntu2`
- `libboost-atomic-dev:amd64=1.83.0.1ubuntu2`
- `libboost-chrono-dev:amd64=1.83.0.1ubuntu2`
- `libboost-container-dev:amd64=1.83.0.1ubuntu2`
- `libboost-context-dev:amd64=1.83.0.1ubuntu2`
- `libboost-coroutine-dev:amd64=1.83.0.1ubuntu2`
- `libboost-date-time-dev:amd64=1.83.0.1ubuntu2`
- `libboost-dev:amd64=1.83.0.1ubuntu2`
- `libboost-exception-dev:amd64=1.83.0.1ubuntu2`
- `libboost-fiber-dev:amd64=1.83.0.1ubuntu2`
- `libboost-filesystem-dev:amd64=1.83.0.1ubuntu2`
- `libboost-graph-dev:amd64=1.83.0.1ubuntu2`
- `libboost-graph-parallel-dev=1.83.0.1ubuntu2`
- `libboost-iostreams-dev:amd64=1.83.0.1ubuntu2`
- `libboost-json-dev:amd64=1.83.0.1ubuntu2`
- `libboost-locale-dev:amd64=1.83.0.1ubuntu2`
- `libboost-log-dev=1.83.0.1ubuntu2`
- `libboost-math-dev:amd64=1.83.0.1ubuntu2`
- `libboost-mpi-dev=1.83.0.1ubuntu2`
- `libboost-mpi-python-dev=1.83.0.1ubuntu2`
- `libboost-nowide-dev=1.83.0.1ubuntu2`
- `libboost-numpy-dev=1.83.0.1ubuntu2`
- `libboost-program-options-dev:amd64=1.83.0.1ubuntu2`
- `libboost-python-dev=1.83.0.1ubuntu2`
- `libboost-random-dev:amd64=1.83.0.1ubuntu2`
- `libboost-regex-dev:amd64=1.83.0.1ubuntu2`
- `libboost-serialization-dev:amd64=1.83.0.1ubuntu2`
- `libboost-stacktrace-dev:amd64=1.83.0.1ubuntu2`
- `libboost-system-dev:amd64=1.83.0.1ubuntu2`
- `libboost-test-dev:amd64=1.83.0.1ubuntu2`
- `libboost-thread-dev:amd64=1.83.0.1ubuntu2`
- `libboost-timer-dev:amd64=1.83.0.1ubuntu2`
- `libboost-tools-dev=1.83.0.1ubuntu2`
- `libboost-type-erasure-dev:amd64=1.83.0.1ubuntu2`
- `libboost-url-dev:amd64=1.83.0.1ubuntu2`
- `libboost-wave-dev:amd64=1.83.0.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libboost-all-dev/copyright`, `/usr/share/doc/libboost-atomic-dev/copyright`, `/usr/share/doc/libboost-chrono-dev/copyright`, `/usr/share/doc/libboost-container-dev/copyright`, `/usr/share/doc/libboost-context-dev/copyright`, `/usr/share/doc/libboost-coroutine-dev/copyright`, `/usr/share/doc/libboost-date-time-dev/copyright`, `/usr/share/doc/libboost-dev/copyright`, `/usr/share/doc/libboost-exception-dev/copyright`, `/usr/share/doc/libboost-fiber-dev/copyright`, `/usr/share/doc/libboost-filesystem-dev/copyright`, `/usr/share/doc/libboost-graph-dev/copyright`, `/usr/share/doc/libboost-graph-parallel-dev/copyright`, `/usr/share/doc/libboost-iostreams-dev/copyright`, `/usr/share/doc/libboost-json-dev/copyright`, `/usr/share/doc/libboost-locale-dev/copyright`, `/usr/share/doc/libboost-log-dev/copyright`, `/usr/share/doc/libboost-math-dev/copyright`, `/usr/share/doc/libboost-mpi-dev/copyright`, `/usr/share/doc/libboost-mpi-python-dev/copyright`, `/usr/share/doc/libboost-nowide-dev/copyright`, `/usr/share/doc/libboost-numpy-dev/copyright`, `/usr/share/doc/libboost-program-options-dev/copyright`, `/usr/share/doc/libboost-python-dev/copyright`, `/usr/share/doc/libboost-random-dev/copyright`, `/usr/share/doc/libboost-regex-dev/copyright`, `/usr/share/doc/libboost-serialization-dev/copyright`, `/usr/share/doc/libboost-stacktrace-dev/copyright`, `/usr/share/doc/libboost-system-dev/copyright`, `/usr/share/doc/libboost-test-dev/copyright`, `/usr/share/doc/libboost-thread-dev/copyright`, `/usr/share/doc/libboost-timer-dev/copyright`, `/usr/share/doc/libboost-tools-dev/copyright`, `/usr/share/doc/libboost-type-erasure-dev/copyright`, `/usr/share/doc/libboost-url-dev/copyright`, `/usr/share/doc/libboost-wave-dev/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `boost1.83=1.83.0-2.1ubuntu3.1`

Binary Packages:

- `libboost-atomic1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-atomic1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-chrono1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-chrono1.83.0t64:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-container1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-container1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-context1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-context1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-coroutine1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-coroutine1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-date-time1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-date-time1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-exception1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-fiber1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-fiber1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-filesystem1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-filesystem1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-graph-parallel1.83-dev=1.83.0-2.1ubuntu3.1`
- `libboost-graph-parallel1.83.0=1.83.0-2.1ubuntu3.1`
- `libboost-graph1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-graph1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-iostreams1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-iostreams1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-json1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-json1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-locale1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-locale1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-log1.83-dev=1.83.0-2.1ubuntu3.1`
- `libboost-log1.83.0=1.83.0-2.1ubuntu3.1`
- `libboost-math1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-math1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-mpi-python1.83-dev=1.83.0-2.1ubuntu3.1`
- `libboost-mpi-python1.83.0=1.83.0-2.1ubuntu3.1`
- `libboost-mpi1.83-dev=1.83.0-2.1ubuntu3.1`
- `libboost-mpi1.83.0=1.83.0-2.1ubuntu3.1`
- `libboost-nowide1.83-dev=1.83.0-2.1ubuntu3.1`
- `libboost-nowide1.83.0=1.83.0-2.1ubuntu3.1`
- `libboost-numpy1.83-dev=1.83.0-2.1ubuntu3.1`
- `libboost-numpy1.83.0=1.83.0-2.1ubuntu3.1`
- `libboost-program-options1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-program-options1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-python1.83-dev=1.83.0-2.1ubuntu3.1`
- `libboost-python1.83.0=1.83.0-2.1ubuntu3.1`
- `libboost-random1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-random1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-regex1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-regex1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-serialization1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-serialization1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-stacktrace1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-stacktrace1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-system1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-system1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-test1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-test1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-thread1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-thread1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-timer1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-timer1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-type-erasure1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-type-erasure1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-url1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-url1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-wave1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost-wave1.83.0:amd64=1.83.0-2.1ubuntu3.1`
- `libboost1.83-dev:amd64=1.83.0-2.1ubuntu3.1`
- `libboost1.83-tools-dev=1.83.0-2.1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libboost-atomic1.83-dev/copyright`, `/usr/share/doc/libboost-atomic1.83.0/copyright`, `/usr/share/doc/libboost-chrono1.83-dev/copyright`, `/usr/share/doc/libboost-chrono1.83.0t64/copyright`, `/usr/share/doc/libboost-container1.83-dev/copyright`, `/usr/share/doc/libboost-container1.83.0/copyright`, `/usr/share/doc/libboost-context1.83-dev/copyright`, `/usr/share/doc/libboost-context1.83.0/copyright`, `/usr/share/doc/libboost-coroutine1.83-dev/copyright`, `/usr/share/doc/libboost-coroutine1.83.0/copyright`, `/usr/share/doc/libboost-date-time1.83-dev/copyright`, `/usr/share/doc/libboost-date-time1.83.0/copyright`, `/usr/share/doc/libboost-exception1.83-dev/copyright`, `/usr/share/doc/libboost-fiber1.83-dev/copyright`, `/usr/share/doc/libboost-fiber1.83.0/copyright`, `/usr/share/doc/libboost-filesystem1.83-dev/copyright`, `/usr/share/doc/libboost-filesystem1.83.0/copyright`, `/usr/share/doc/libboost-graph-parallel1.83-dev/copyright`, `/usr/share/doc/libboost-graph-parallel1.83.0/copyright`, `/usr/share/doc/libboost-graph1.83-dev/copyright`, `/usr/share/doc/libboost-graph1.83.0/copyright`, `/usr/share/doc/libboost-iostreams1.83-dev/copyright`, `/usr/share/doc/libboost-iostreams1.83.0/copyright`, `/usr/share/doc/libboost-json1.83-dev/copyright`, `/usr/share/doc/libboost-json1.83.0/copyright`, `/usr/share/doc/libboost-locale1.83-dev/copyright`, `/usr/share/doc/libboost-locale1.83.0/copyright`, `/usr/share/doc/libboost-log1.83-dev/copyright`, `/usr/share/doc/libboost-log1.83.0/copyright`, `/usr/share/doc/libboost-math1.83-dev/copyright`, `/usr/share/doc/libboost-math1.83.0/copyright`, `/usr/share/doc/libboost-mpi-python1.83-dev/copyright`, `/usr/share/doc/libboost-mpi-python1.83.0/copyright`, `/usr/share/doc/libboost-mpi1.83-dev/copyright`, `/usr/share/doc/libboost-mpi1.83.0/copyright`, `/usr/share/doc/libboost-nowide1.83-dev/copyright`, `/usr/share/doc/libboost-nowide1.83.0/copyright`, `/usr/share/doc/libboost-numpy1.83-dev/copyright`, `/usr/share/doc/libboost-numpy1.83.0/copyright`, `/usr/share/doc/libboost-program-options1.83-dev/copyright`, `/usr/share/doc/libboost-program-options1.83.0/copyright`, `/usr/share/doc/libboost-python1.83-dev/copyright`, `/usr/share/doc/libboost-python1.83.0/copyright`, `/usr/share/doc/libboost-random1.83-dev/copyright`, `/usr/share/doc/libboost-random1.83.0/copyright`, `/usr/share/doc/libboost-regex1.83-dev/copyright`, `/usr/share/doc/libboost-regex1.83.0/copyright`, `/usr/share/doc/libboost-serialization1.83-dev/copyright`, `/usr/share/doc/libboost-serialization1.83.0/copyright`, `/usr/share/doc/libboost-stacktrace1.83-dev/copyright`, `/usr/share/doc/libboost-stacktrace1.83.0/copyright`, `/usr/share/doc/libboost-system1.83-dev/copyright`, `/usr/share/doc/libboost-system1.83.0/copyright`, `/usr/share/doc/libboost-test1.83-dev/copyright`, `/usr/share/doc/libboost-test1.83.0/copyright`, `/usr/share/doc/libboost-thread1.83-dev/copyright`, `/usr/share/doc/libboost-thread1.83.0/copyright`, `/usr/share/doc/libboost-timer1.83-dev/copyright`, `/usr/share/doc/libboost-timer1.83.0/copyright`, `/usr/share/doc/libboost-type-erasure1.83-dev/copyright`, `/usr/share/doc/libboost-type-erasure1.83.0/copyright`, `/usr/share/doc/libboost-url1.83-dev/copyright`, `/usr/share/doc/libboost-url1.83.0/copyright`, `/usr/share/doc/libboost-wave1.83-dev/copyright`, `/usr/share/doc/libboost-wave1.83.0/copyright`, `/usr/share/doc/libboost1.83-dev/copyright`, `/usr/share/doc/libboost1.83-tools-dev/copyright`)

- `Apache-2.0`
- `BSD2`
- `BSD3_DEShaw`
- `BSD3_Google`
- `BSL-1.0`
- `Caramel`
- `CrystalClear`
- `HP`
- `Jam`
- `Kempf`
- `MIT`
- `NIST`
- `OldBoost1`
- `OldBoost2`
- `OldBoost3`
- `Python`
- `SGI`
- `Spencer`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris boost1.83=1.83.0-2.1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.83/boost1.83_1.83.0-2.1ubuntu3.1.dsc' boost1.83_1.83.0-2.1ubuntu3.1.dsc 10382 SHA512:086293d50b9118a7d5eeac5bb33717fa2e5d409ae68cbf8029394a17c1882b8cc7e51918ee7cea4ae9dd8b104fe1c1271a96b4874252eaab5ee5b26f516d201c
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.83/boost1.83_1.83.0.orig.tar.xz' boost1.83_1.83.0.orig.tar.xz 77376520 SHA512:de285fe516794a888196c0b1fafd5b62dbd3acf7c2214287c3a51a02d127981fa56f09c436e8d5868ceb1f5e9e9490c96fe635ed9aa84fd96c21b557a23558c8
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.83/boost1.83_1.83.0-2.1ubuntu3.1.debian.tar.xz' boost1.83_1.83.0-2.1ubuntu3.1.debian.tar.xz 379096 SHA512:1e201bbbaff88ecd751e3787701f6413e330963027111805a56059113edeba252004c8b9807dbe4c46d2aee6197425987c8dee736b788e23b98051dc08d559ad
```

### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2build2`
- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `build-essential=12.10ubuntu1`

Binary Packages:

- `build-essential=12.10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bullet=3.24+dfsg-2.1build1`

Binary Packages:

- `libbullet-dev:amd64=3.24+dfsg-2.1build1`
- `libbullet3.24t64:amd64=3.24+dfsg-2.1build1`

Licenses: (parsed from: `/usr/share/doc/libbullet-dev/copyright`, `/usr/share/doc/libbullet3.24t64/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSL-1.0`
- `Elsevier-CDROM-License`
- `Expat`
- `GNU-All-Permissive-License`
- `GPL-2`
- `GPL-2+`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bzip2=1.0.8-5.1build0.1`

Binary Packages:

- `bzip2=1.0.8-5.1build0.1`
- `libbz2-1.0:amd64=1.0.8-5.1build0.1`
- `libbz2-dev:amd64=1.0.8-5.1build0.1`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5.1build0.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.dsc' bzip2_1.0.8-5.1build0.1.dsc 2220 SHA512:1233c3065a9355482c826f35f7859450a868a6e98ef7793dcc1ae68d68360c840ed8bd21af872501d36803c10b9b2516556e8bb716f3d0ff5cdaa877a1ab95df
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.debian.tar.bz2' bzip2_1.0.8-5.1build0.1.debian.tar.bz2 26927 SHA512:ee39a01bcd6b31d70b3dfaa14bf7f943cb3711d073569cf9e35092062742077801ca287425c855a499114335748f2f791a7ff07eb502f2601a3d58f5041e7413
```

### `dpkg` source package: `c-blosc=1.21.5+ds-1build1`

Binary Packages:

- `libblosc-dev:amd64=1.21.5+ds-1build1`
- `libblosc1:amd64=1.21.5+ds-1build1`

Licenses: (parsed from: `/usr/share/doc/libblosc-dev/copyright`, `/usr/share/doc/libblosc1/copyright`)

- `BSD-3-clause`
- `Expat`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ca-certificates-java=20240118`

Binary Packages:

- `ca-certificates-java=20240118`

Licenses: (parsed from: `/usr/share/doc/ca-certificates-java/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ca-certificates-java/20240118/


### `dpkg` source package: `ca-certificates=20240203`

Binary Packages:

- `ca-certificates=20240203`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ca-certificates/20240203/


### `dpkg` source package: `cairo=1.18.0-3build1`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.0-3build1`
- `libcairo2:amd64=1.18.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `catch2=3.4.0-1build1`

Binary Packages:

- `catch2=3.4.0-1build1`

Licenses: (parsed from: `/usr/share/doc/catch2/copyright`)

- `BSD-3`
- `Boost-1.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cdebconf=0.271ubuntu3`

Binary Packages:

- `libdebconfclient0:amd64=0.271ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cfitsio=4.3.1-1.1build2`

Binary Packages:

- `libcfitsio-dev:amd64=4.3.1-1.1build2`
- `libcfitsio10t64:amd64=4.3.1-1.1build2`

Licenses: (parsed from: `/usr/share/doc/libcfitsio-dev/copyright`, `/usr/share/doc/libcfitsio10t64/copyright`)

- `GPL-2`
- `LGPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `charls=2.4.2-2build2`

Binary Packages:

- `libcharls2:amd64=2.4.2-2build2`

Licenses: (parsed from: `/usr/share/doc/libcharls2/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `chromaprint=1.5.1-5`

Binary Packages:

- `libchromaprint1:amd64=1.5.1-5`

Licenses: (parsed from: `/usr/share/doc/libchromaprint1/copyright`)

- `BSD-3-clause`
- `Expat`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/chromaprint/1.5.1-5/


### `dpkg` source package: `cjson=1.7.17-1`

Binary Packages:

- `libcjson1:amd64=1.7.17-1`

Licenses: (parsed from: `/usr/share/doc/libcjson1/copyright`)

- `Apache-2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/cjson/1.7.17-1/


### `dpkg` source package: `cmake=3.28.3-1build7`

Binary Packages:

- `cmake=3.28.3-1build7`
- `cmake-data=3.28.3-1build7`

Licenses: (parsed from: `/usr/share/doc/cmake/copyright`, `/usr/share/doc/cmake-data/copyright`)

- `Apache-2.0`
- `BSD-0-Clause`
- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `BSD-4-Clause`
- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+ with Bison exception`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `ISC`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `codec2=1.2.0-2build1`

Binary Packages:

- `libcodec2-1.2:amd64=1.2.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libcodec2-1.2/copyright`)

- `JMVBSD`
- `KISSFFTBSD`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `colord=1.4.7-1build2`

Binary Packages:

- `libcolord2:amd64=1.4.7-1build2`

Licenses: (parsed from: `/usr/share/doc/libcolord2/copyright`)

- `CC0-1.0`
- `GFDL-NIV`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1+`
- `NPES`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `console-bridge=1.0.1+dfsg2-3build1`

Binary Packages:

- `libconsole-bridge-dev:amd64=1.0.1+dfsg2-3build1`
- `libconsole-bridge1.0:amd64=1.0.1+dfsg2-3build1`

Licenses: (parsed from: `/usr/share/doc/libconsole-bridge-dev/copyright`, `/usr/share/doc/libconsole-bridge1.0/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `coreutils=9.4-3ubuntu6.1`

Binary Packages:

- `coreutils=9.4-3ubuntu6.1`

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
$ apt-get source -qq --print-uris coreutils=9.4-3ubuntu6.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3ubuntu6.1.dsc' coreutils_9.4-3ubuntu6.1.dsc 2030 SHA512:dc10ff1405ba4f50260e3d63b62162e4b9c7d4d258da785f956e008f63ed7dfbf2e10753643e688658957ce0d185b4b31e4c22e8e08007112f2102264926fc6f
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA512:7c55ee23b685a0462bbbd118b04d25278c902604a0dcf3bf4f8bf81faa0500dee5a7813cba6f586d676c98e520cafd420f16479619305e94ea6798d8437561f5
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3ubuntu6.1.debian.tar.xz' coreutils_9.4-3ubuntu6.1.debian.tar.xz 41308 SHA512:abbd5d534ad307d8244f5ae6112ebe050306459ec5de4231e5dd1266361157b307c821e8c1e2bbd41f7cf6c7ab796a592fb8d2ef1cb516ae90e8050fb84c1502
```

### `dpkg` source package: `cppcheck=2.13.0-2ubuntu3`

Binary Packages:

- `cppcheck=2.13.0-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/cppcheck/copyright`)

- `BSD-2`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ZLIB`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cryptsetup=2:2.7.0-1ubuntu4.2`

Binary Packages:

- `libcryptsetup12:amd64=2:2.7.0-1ubuntu4.2`

Licenses: (parsed from: `/usr/share/doc/libcryptsetup12/copyright`)

- `Apache-2.0`
- `CC0`
- `CC0-1.0`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with OpenSSL exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-2.1+ with OpenSSL exception`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris cryptsetup=2:2.7.0-1ubuntu4.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cryptsetup/cryptsetup_2.7.0-1ubuntu4.2.dsc' cryptsetup_2.7.0-1ubuntu4.2.dsc 3690 SHA512:847a0f4ede10e6ebf5a459f62dd7a91372c753fc154d3709c44292439c6ab75530ab99151cd09bbcf038ce17b58f3a1ad9452ea0054781ccca6e0df49593b625
'http://archive.ubuntu.com/ubuntu/pool/main/c/cryptsetup/cryptsetup_2.7.0.orig.tar.gz' cryptsetup_2.7.0.orig.tar.gz 11754085 SHA512:cc197e785bebac24618996852371e8158496d7cf84c1f9051723a0ead4966cd0c0063bdcacd7f0ef58d8252fa86156b847312f8aadf2c6292bbea9bc2fac7ecd
'http://archive.ubuntu.com/ubuntu/pool/main/c/cryptsetup/cryptsetup_2.7.0-1ubuntu4.2.debian.tar.xz' cryptsetup_2.7.0-1ubuntu4.2.debian.tar.xz 169908 SHA512:6fd19d7346d71949b38c298045535a93858f21bae55dfd084ea6f75e3d7bbc03f8ff1d44b015a3f70e71c559becb9edea1d17584203044b90c5ccb7b99908af6
```

### `dpkg` source package: `cups=2.4.7-1.2ubuntu7.9`

Binary Packages:

- `libcups2t64:amd64=2.4.7-1.2ubuntu7.9`

Licenses: (parsed from: `/usr/share/doc/libcups2t64/copyright`)

- `Apache-2.0`
- `Apache-2.0-with-GPL2-LGPL2-Exception`
- `BSD-2-Clause`
- `BSD-2-clause`
- `FSFUL`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris cups=2.4.7-1.2ubuntu7.9
'http://archive.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.7-1.2ubuntu7.9.dsc' cups_2.4.7-1.2ubuntu7.9.dsc 3188 SHA512:49aadaf466874815257b71ca96c1233c1c40397d7962620727dce95b452a8340f9ec3c44bed6855847090123dcbe932e7ee4fa3a9f617a9e047c940e7d99872d
'http://archive.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.7.orig.tar.gz' cups_2.4.7.orig.tar.gz 8134809 SHA512:914b574ff6d85de9f3471528b52d4a436c484c441f47651846e1bdfa00aec26774efd416ff466216d2bccf468f8a797b1e0d666b5c82abc87e77550ce8b00d39
'http://archive.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.7-1.2ubuntu7.9.debian.tar.xz' cups_2.4.7-1.2ubuntu7.9.debian.tar.xz 418144 SHA512:cbb3dbc2d630b20f6aef4deafa907b9737ee970df8724b7af2684574fcd01c62affd8df1c95857bc6c04577c8be9a67f692e8c6bcf3f2480df06cf205ce070e3
```

### `dpkg` source package: `curl=8.5.0-2ubuntu10.6`

Binary Packages:

- `curl=8.5.0-2ubuntu10.6`
- `libcurl3t64-gnutls:amd64=8.5.0-2ubuntu10.6`
- `libcurl4-openssl-dev:amd64=8.5.0-2ubuntu10.6`
- `libcurl4t64:amd64=8.5.0-2ubuntu10.6`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4-openssl-dev/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `OLDAP-2.8`
- `X11`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris curl=8.5.0-2ubuntu10.6
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.6.dsc' curl_8.5.0-2ubuntu10.6.dsc 3051 SHA512:befb2dcd69003718eef66ddd619e4756b087b14f25ff1cd3e84a39bc1011d64c68b4f9cf919fc5dc2a2998e1b46848cc00e2677f36af3e78638b7a730a28a84c
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0.orig.tar.gz' curl_8.5.0.orig.tar.gz 4372979 SHA512:1ff70e8fd5f233b373dea2a031d46698c03ed35f384c2eacbe9368f9daed65e91d7f45ade350c3ac3dd3d662c913b17cdc8702a0c23879b0c78fbd396fd0b926
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.6.debian.tar.xz' curl_8.5.0-2ubuntu10.6.debian.tar.xz 63144 SHA512:cbcd07b07b961c3e6c23fd1701b270a48d372c60f55d9af16684f3fc5d832d24e965c0240ba4a92a198db45d1609daa7eb556ee59bfdf81f196c997a682131c3
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-5ubuntu3.1`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-5ubuntu3.1`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-5ubuntu3.1`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-5ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-5ubuntu3.1.dsc' cyrus-sasl2_2.1.28+dfsg1-5ubuntu3.1.dsc 3501 SHA512:3a6f5d06ebf66b8f547eeae248414f9af7cc8a3f499d7d55d919e1c5b8a0851b624d28d48ea90a04d67261f350a890461156946909e83427e09237a8d90ed0bc
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-5ubuntu3.1.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-5ubuntu3.1.debian.tar.xz 98324 SHA512:7e2fb71cd5693f9504158125385657920df46efcd63e28b14d0553772e2f2d906cd0c25425762e75adadec4a18715eee12c945dc4d27ce2d8c118efcb65175a5
```

### `dpkg` source package: `dash=0.5.12-6ubuntu5`

Binary Packages:

- `dash=0.5.12-6ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dav1d=1.4.1-1build1`

Binary Packages:

- `libdav1d-dev:amd64=1.4.1-1build1`
- `libdav1d7:amd64=1.4.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libdav1d-dev/copyright`, `/usr/share/doc/libdav1d7/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `db5.3=5.3.28+dfsg2-7`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-7`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-7/


### `dpkg` source package: `dbus-python=1.3.2-5build3`

Binary Packages:

- `python3-dbus=1.3.2-5build3`

Licenses: (parsed from: `/usr/share/doc/python3-dbus/copyright`)

- `AFL-2.1`
- `AFL-2.1,`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dbus=1.14.10-4ubuntu4.1`

Binary Packages:

- `dbus=1.14.10-4ubuntu4.1`
- `dbus-bin=1.14.10-4ubuntu4.1`
- `dbus-daemon=1.14.10-4ubuntu4.1`
- `dbus-session-bus-common=1.14.10-4ubuntu4.1`
- `dbus-system-bus-common=1.14.10-4ubuntu4.1`
- `dbus-user-session=1.14.10-4ubuntu4.1`
- `libdbus-1-3:amd64=1.14.10-4ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/dbus/copyright`, `/usr/share/doc/dbus-bin/copyright`, `/usr/share/doc/dbus-daemon/copyright`, `/usr/share/doc/dbus-session-bus-common/copyright`, `/usr/share/doc/dbus-system-bus-common/copyright`, `/usr/share/doc/dbus-user-session/copyright`, `/usr/share/doc/libdbus-1-3/copyright`)

- `AFL-2.1`
- `AFL-2.1,`
- `BSD-3-clause`
- `BSD-3-clause-generic`
- `Expat`
- `FSF-unlimited-permission`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Tcl-BSDish`
- `autoconf-archive-permissive`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris dbus=1.14.10-4ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10-4ubuntu4.1.dsc' dbus_1.14.10-4ubuntu4.1.dsc 3746 SHA512:5ac50f3bfa7f83739b76897dddab068f756e54e3019a848fa8943f61fc9862c72e642f57c3c6a3392146ae817731779e3d8b1c91080ef79aaa906342b96003d3
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10.orig.tar.xz' dbus_1.14.10.orig.tar.xz 1372328 SHA512:775b708326059692937acb69d4ce1a89e69878501166655b5d1b1628ac31b50dd53d979d93c84e57f95e90b15e25aa33893e51a7421d3537e9c2f02b1b91bfae
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10.orig.tar.xz.asc' dbus_1.14.10.orig.tar.xz.asc 833 SHA512:2a646884150f31e50b1bf2238fe21377929ceb536691fb9ef06aee25737c1a5be5ca18d8bdd8a02fdf3b00681fd26509a3e6e62a49541ef5685d09499ba9d30b
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10-4ubuntu4.1.debian.tar.xz' dbus_1.14.10-4ubuntu4.1.debian.tar.xz 69668 SHA512:3b8a963e5143a0ca730aab7a90775c77958fd98dfe4e2d26f452115c8df748e5ca18cd501672e61b64ca7ae5af6b043f1119faa5928f9f47785a214fb2ae0455
```

### `dpkg` source package: `dconf=0.40.0-4ubuntu0.1`

Binary Packages:

- `dconf-gsettings-backend:amd64=0.40.0-4ubuntu0.1`
- `dconf-service=0.40.0-4ubuntu0.1`
- `libdconf1:amd64=0.40.0-4ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/dconf-gsettings-backend/copyright`, `/usr/share/doc/dconf-service/copyright`, `/usr/share/doc/libdconf1/copyright`)

- `GPL-3`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris dconf=0.40.0-4ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dconf/dconf_0.40.0-4ubuntu0.1.dsc' dconf_0.40.0-4ubuntu0.1.dsc 2810 SHA512:d207841b6d1e5a358d2c3f1e4039025ed7213c68ba4e92ead3f516084b467d6eb079ef38782d23947239f99327eca2e94fa1fb30689cdf385d613d0cbafb11df
'http://archive.ubuntu.com/ubuntu/pool/main/d/dconf/dconf_0.40.0.orig.tar.xz' dconf_0.40.0.orig.tar.xz 117764 SHA512:71396d71f24f47653181482b052fdfc63795c50c373de34e2fb93e16101745daa7e81192b79a102d5389911cea34138eedf3ac32bc80562018e8a7f31963559a
'http://archive.ubuntu.com/ubuntu/pool/main/d/dconf/dconf_0.40.0-4ubuntu0.1.debian.tar.xz' dconf_0.40.0-4ubuntu0.1.debian.tar.xz 12104 SHA512:1ceff3f18cf856bb47b40afc1b3c49efcf01e338c6aee75286e01b7eff12fe62ef519cd5e7d17b922105c9186e69dee2a6ef09c64007810ecea671c9c84805cd
```

### `dpkg` source package: `debconf=1.5.86ubuntu1`

Binary Packages:

- `debconf=1.5.86ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `debianutils=5.17build1`

Binary Packages:

- `debianutils=5.17build1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `diffutils=1:3.10-1build1`

Binary Packages:

- `diffutils=1:3.10-1build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `distlib=0.3.8-1`

Binary Packages:

- `python3-distlib=0.3.8-1`

Licenses: (parsed from: `/usr/share/doc/python3-distlib/copyright`)

- `BSD-3-clause`
- `Python`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/distlib/0.3.8-1/


### `dpkg` source package: `double-conversion=3.3.0-1build1`

Binary Packages:

- `libdouble-conversion-dev:amd64=3.3.0-1build1`
- `libdouble-conversion3:amd64=3.3.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libdouble-conversion-dev/copyright`, `/usr/share/doc/libdouble-conversion3/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dpkg=1.22.6ubuntu6.5`

Binary Packages:

- `dpkg=1.22.6ubuntu6.5`
- `dpkg-dev=1.22.6ubuntu6.5`
- `libdpkg-perl=1.22.6ubuntu6.5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.6ubuntu6.5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.dsc' dpkg_1.22.6ubuntu6.5.dsc 3156 SHA512:6c6f43612ac5f74937a2a83525ebb66a21af81e4678fd2b3bafbcb490e0e33be6a611b1475c205de378b64efdf7c615abd46b78c58b6c232145e7d2b75fe9d7b
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.tar.xz' dpkg_1.22.6ubuntu6.5.tar.xz 5547360 SHA512:a52c556b632205b84bf8e795f68f54fe7e78b251561d032be76ecde9c5e3d9a74c5358476956ab8c3b2fb0266a5f4a03f3d67ec7039e62dc56905ee8c52d2d5d
```

### `dpkg` source package: `e2fsprogs=1.47.0-2.4~exp1ubuntu4.1`

Binary Packages:

- `e2fsprogs=1.47.0-2.4~exp1ubuntu4.1`
- `libcom-err2:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `libext2fs2t64:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `libss2:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `logsave=1.47.0-2.4~exp1ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `GPL`
- `GPL-2`
- `GPL-2+ with Texinfo exception`
- `ISC`
- `Kazlib`
- `LGPL-2`
- `Latex2e`
- `MIT-US-export`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.0-2.4~exp1ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4%7eexp1ubuntu4.1.dsc' e2fsprogs_1.47.0-2.4~exp1ubuntu4.1.dsc 3294 SHA512:0b9616118928aee8c2893dd1d6444735fd2c1852975414fbfeccb8d94bd01c34b49111282d728f835d539a17b6642b1c20509b17367b0bafc1d417b2910621b0
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz' e2fsprogs_1.47.0.orig.tar.gz 9637717 SHA512:4f03a469d03cb0f0656bd17c64d944606fb25e68002e3e42c278f3775fee6bf776cc2061ae378b5df4f167a5c33444490111fdcbb140e0320445706f9d048dd0
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz.asc' e2fsprogs_1.47.0.orig.tar.gz.asc 488 SHA512:cd3652ec12f694f1c1f5bd4af4964bb32ad832ba8a06a48864d12a998dc514e9a950ebdb475707a3abb8360852a3469794f2327f097328c99233beef575df144
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4%7eexp1ubuntu4.1.debian.tar.xz' e2fsprogs_1.47.0-2.4~exp1ubuntu4.1.debian.tar.xz 90580 SHA512:c95606b9d20cdfeacedf1b7fb7185406562117a71afaae5e1c246f30a510ba46abe79e12221503e3809a8595caa967835f640990dd41921ca6ec5abbea20a371
```

### `dpkg` source package: `eigen3=3.4.0-4build0.1`

Binary Packages:

- `libeigen3-dev=3.4.0-4build0.1`

Licenses: (parsed from: `/usr/share/doc/libeigen3-dev/copyright`)

- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-2`

Source:

```console
$ apt-get source -qq --print-uris eigen3=3.4.0-4build0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.4.0-4build0.1.dsc' eigen3_3.4.0-4build0.1.dsc 2202 SHA512:14873701c5925f8a5fefc4c77cb0fee4ddf8361849f52275f979ab4b49309ae09650c66a53fe403f50ede03266184ae822cf86dad00732818815c5d58ca2a379
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.4.0.orig.tar.bz2' eigen3_3.4.0.orig.tar.bz2 2143091 SHA512:cc488eb111e0e248744d2bc4475b345b5fb82361dff226a5b73a33bd0388de8c219cff8cffcf8f476b672fc0e223f339e8c6a1cfb6293840a4a6abf232438a89
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.4.0-4build0.1.debian.tar.xz' eigen3_3.4.0-4build0.1.debian.tar.xz 20600 SHA512:8b4151d3258be1b14624cc9d3ac492833748626acad6d44a15de800a3d266c8ed285170a0d50df10836c41a746a211190976fe9a3ea15aa7118541e68a1297a8
```

### `dpkg` source package: `elfutils=0.190-1.1ubuntu0.1`

Binary Packages:

- `libdw1t64:amd64=0.190-1.1ubuntu0.1`
- `libelf1t64:amd64=0.190-1.1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libdw1t64/copyright`, `/usr/share/doc/libelf1t64/copyright`)

- `BSD-2-clause`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
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
$ apt-get source -qq --print-uris elfutils=0.190-1.1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190-1.1ubuntu0.1.dsc' elfutils_0.190-1.1ubuntu0.1.dsc 3410 SHA512:56440e43ecfac444cca2cbd6f2a33f2780cea395b5caa302587c4a1e602b3c4bb45dbcede76e7767b6f18f519458b52c6300ef83b80cdebc603418fe2a4a0889
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190.orig.tar.bz2' elfutils_0.190.orig.tar.bz2 9162766 SHA512:9c4f5328097e028286c42f29e39dc3d80914b656cdfbbe05b639e91bc787ae8ae64dd4d69a6e317ce30c01648ded10281b86a51e718295f4c589df1225a48102
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190-1.1ubuntu0.1.debian.tar.xz' elfutils_0.190-1.1ubuntu0.1.debian.tar.xz 46976 SHA512:f4bf523b754c8fd09c189483b3f084955b2b467e5e03338e2448ec0d4af478ea39a7d7bd4c2b7dfcfbe538a870ec452c51f840e6c33b0ffdec65837c2f6384cd
```

### `dpkg` source package: `empy=3.3.4-2`

Binary Packages:

- `python3-empy=3.3.4-2`

Licenses: (parsed from: `/usr/share/doc/python3-empy/copyright`)

- `GPL-2`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/empy/3.3.4-2/


### `dpkg` source package: `expat=2.6.1-2ubuntu0.3`

Binary Packages:

- `libexpat1:amd64=2.6.1-2ubuntu0.3`
- `libexpat1-dev:amd64=2.6.1-2ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.1-2ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.3.dsc' expat_2.6.1-2ubuntu0.3.dsc 1474 SHA512:2331ab71158152f87fffa9e05e04b6f79bbeee7842cd957e3237847684b3508fb193850ca47049f1ed3284cc54d553183d9886de595a5ada114da20bf0119c69
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1.orig.tar.gz' expat_2.6.1.orig.tar.gz 8414649 SHA512:cf6c64fc0ca55dd172ca8a6ca10d1fb2c915d0f941b0068f42cb90488022dea73e04119c49a1bd4ab9a5d425ddc132ae5f22260ff6d2e25204637a1169e7bd4f
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.3.debian.tar.xz' expat_2.6.1-2ubuntu0.3.debian.tar.xz 30100 SHA512:9b71cdafaacb1148f3e22cef6bde49f2701339a15c78ccf0df954c19bdba6b6f8ee778ab2227c8543f75bcc8b6e5f8e380e99d6d0c7ea4660526669e4d97df0e
```

### `dpkg` source package: `ffmpeg=7:6.1.1-3ubuntu5`

Binary Packages:

- `libavcodec-dev:amd64=7:6.1.1-3ubuntu5`
- `libavcodec60:amd64=7:6.1.1-3ubuntu5`
- `libavformat-dev:amd64=7:6.1.1-3ubuntu5`
- `libavformat60:amd64=7:6.1.1-3ubuntu5`
- `libavutil-dev:amd64=7:6.1.1-3ubuntu5`
- `libavutil58:amd64=7:6.1.1-3ubuntu5`
- `libswresample-dev:amd64=7:6.1.1-3ubuntu5`
- `libswresample4:amd64=7:6.1.1-3ubuntu5`
- `libswscale-dev:amd64=7:6.1.1-3ubuntu5`
- `libswscale7:amd64=7:6.1.1-3ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libavcodec-dev/copyright`, `/usr/share/doc/libavcodec60/copyright`, `/usr/share/doc/libavformat-dev/copyright`, `/usr/share/doc/libavformat60/copyright`, `/usr/share/doc/libavutil-dev/copyright`, `/usr/share/doc/libavutil58/copyright`, `/usr/share/doc/libswresample-dev/copyright`, `/usr/share/doc/libswresample4/copyright`, `/usr/share/doc/libswscale-dev/copyright`, `/usr/share/doc/libswscale7/copyright`)

- `BSD-1-clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSL`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `IJG`
- `ISC`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Sundry`
- `Zlib`
- `man-page`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `findutils=4.9.0-5build1`

Binary Packages:

- `findutils=4.9.0-5build1`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `BSD-3-clause`
- `BSD-3-clause and/or GPL-3+`
- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL with automake exception`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-data exception`
- `GPL-3+ with Bison-2.2 exception`
- `ISC`
- `ISC and/or LGPL-2.1+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `flake8-builtins=2.1.0-1`

Binary Packages:

- `python3-flake8-builtins=2.1.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-builtins/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-builtins/2.1.0-1/


### `dpkg` source package: `flake8-comprehensions=3.14.0-1`

Binary Packages:

- `python3-flake8-comprehensions=3.14.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-comprehensions/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-comprehensions/3.14.0-1/


### `dpkg` source package: `flake8-docstrings=1.6.0-2`

Binary Packages:

- `python3-flake8-docstrings=1.6.0-2`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-docstrings/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-docstrings/1.6.0-2/


### `dpkg` source package: `flake8-import-order=0.18.2-2`

Binary Packages:

- `python3-flake8-import-order=0.18.2-2`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-import-order/copyright`)

- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-import-order/0.18.2-2/


### `dpkg` source package: `flake8-quotes=3.4.0-1`

Binary Packages:

- `python3-flake8-quotes=3.4.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-quotes/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-quotes/3.4.0-1/


### `dpkg` source package: `flann=1.9.2+dfsg-2build1`

Binary Packages:

- `libflann-dev:amd64=1.9.2+dfsg-2build1`
- `libflann1.9:amd64=1.9.2+dfsg-2build1`

Licenses: (parsed from: `/usr/share/doc/libflann-dev/copyright`, `/usr/share/doc/libflann1.9/copyright`)

- `BSD-3-clause`
- `BSL-1`
- `Contract_DE-AC04-94AL85000`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fmtlib=9.1.0+ds1-2`

Binary Packages:

- `libfmt-dev:amd64=9.1.0+ds1-2`
- `libfmt9:amd64=9.1.0+ds1-2`

Licenses: (parsed from: `/usr/share/doc/libfmt-dev/copyright`, `/usr/share/doc/libfmt9/copyright`)

- `BSD-2-Clause`
- `CC0-1.0`
- `Expat`
- `Expat with embedded exception`
- `Python`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/fmtlib/9.1.0+ds1-2/


### `dpkg` source package: `fontconfig=2.15.0-1.1ubuntu2`

Binary Packages:

- `fontconfig=2.15.0-1.1ubuntu2`
- `fontconfig-config=2.15.0-1.1ubuntu2`
- `libfontconfig-dev:amd64=2.15.0-1.1ubuntu2`
- `libfontconfig1:amd64=2.15.0-1.1ubuntu2`
- `libfontconfig1-dev:amd64=2.15.0-1.1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fonts-dejavu=2.37-8`

Binary Packages:

- `fonts-dejavu-core=2.37-8`
- `fonts-dejavu-mono=2.37-8`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`, `/usr/share/doc/fonts-dejavu-mono/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/fonts-dejavu/2.37-8/


### `dpkg` source package: `freetype=2.13.2+dfsg-1build3`

Binary Packages:

- `libfreetype-dev:amd64=2.13.2+dfsg-1build3`
- `libfreetype6:amd64=2.13.2+dfsg-1build3`

Licenses: (parsed from: `/usr/share/doc/libfreetype-dev/copyright`, `/usr/share/doc/libfreetype6/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `freexl=2.0.0-1build2`

Binary Packages:

- `libfreexl-dev:amd64=2.0.0-1build2`
- `libfreexl1:amd64=2.0.0-1build2`

Licenses: (parsed from: `/usr/share/doc/libfreexl-dev/copyright`, `/usr/share/doc/libfreexl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fribidi=1.0.13-3build1`

Binary Packages:

- `libfribidi0:amd64=1.0.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fyba=4.1.1-11build1`

Binary Packages:

- `libfyba-dev:amd64=4.1.1-11build1`
- `libfyba0t64:amd64=4.1.1-11build1`

Licenses: (parsed from: `/usr/share/doc/libfyba-dev/copyright`, `/usr/share/doc/libfyba0t64/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `game-music-emu=0.6.3-7build1`

Binary Packages:

- `libgme0:amd64=0.6.3-7build1`

Licenses: (parsed from: `/usr/share/doc/libgme0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gcc-13=13.3.0-6ubuntu2~24.04`

Binary Packages:

- `cpp-13=13.3.0-6ubuntu2~24.04`
- `cpp-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04`
- `g++-13=13.3.0-6ubuntu2~24.04`
- `g++-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04`
- `gcc-13=13.3.0-6ubuntu2~24.04`
- `gcc-13-base:amd64=13.3.0-6ubuntu2~24.04`
- `gcc-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04`
- `gfortran-13=13.3.0-6ubuntu2~24.04`
- `gfortran-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04`
- `libgcc-13-dev:amd64=13.3.0-6ubuntu2~24.04`
- `libgfortran-13-dev:amd64=13.3.0-6ubuntu2~24.04`
- `libstdc++-13-dev:amd64=13.3.0-6ubuntu2~24.04`

Licenses: (parsed from: `/usr/share/doc/cpp-13/copyright`, `/usr/share/doc/cpp-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-13/copyright`, `/usr/share/doc/g++-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-13/copyright`, `/usr/share/doc/gcc-13-base/copyright`, `/usr/share/doc/gcc-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran-13/copyright`, `/usr/share/doc/gfortran-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/libgcc-13-dev/copyright`, `/usr/share/doc/libgfortran-13-dev/copyright`, `/usr/share/doc/libstdc++-13-dev/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-13=13.3.0-6ubuntu2~24.04
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.3.0-6ubuntu2%7e24.04.dsc' gcc-13_13.3.0-6ubuntu2~24.04.dsc 39532 SHA512:57de6461f2370233f418d6041794db86104bfb47be2e1514061b8a1d53c4e9ccecc8fed0b475c148a43dddc646c3e5362ba2248457debdc76067198b97dac385
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.3.0.orig.tar.gz' gcc-13_13.3.0.orig.tar.gz 92761021 SHA512:78a3040d19618d2264544d6db9b237180735213af3d1e578641cc1e6809fa04bb39c5e8da67f9c637a213c3a24ec03688b2fa67dd30515eaaa41ac50733233e1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.3.0-6ubuntu2%7e24.04.debian.tar.xz' gcc-13_13.3.0-6ubuntu2~24.04.debian.tar.xz 646192 SHA512:217913c9e14a6ee123588a688df164f593db23fb40b29cbcf174aee7841866cfb56624870bb6d1291f62410497c8ed0adcc78dcf9552c54dda1958330f1602c1
```

### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2~24.04`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-4ubuntu2~24.04`
- `libasan8:amd64=14.2.0-4ubuntu2~24.04`
- `libatomic1:amd64=14.2.0-4ubuntu2~24.04`
- `libcc1-0:amd64=14.2.0-4ubuntu2~24.04`
- `libgcc-s1:amd64=14.2.0-4ubuntu2~24.04`
- `libgfortran5:amd64=14.2.0-4ubuntu2~24.04`
- `libgomp1:amd64=14.2.0-4ubuntu2~24.04`
- `libhwasan0:amd64=14.2.0-4ubuntu2~24.04`
- `libitm1:amd64=14.2.0-4ubuntu2~24.04`
- `liblsan0:amd64=14.2.0-4ubuntu2~24.04`
- `libquadmath0:amd64=14.2.0-4ubuntu2~24.04`
- `libstdc++6:amd64=14.2.0-4ubuntu2~24.04`
- `libtsan2:amd64=14.2.0-4ubuntu2~24.04`
- `libubsan1:amd64=14.2.0-4ubuntu2~24.04`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-4ubuntu2~24.04
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.dsc' gcc-14_14.2.0-4ubuntu2~24.04.dsc 46922 SHA512:95abfd5811a313d7f7571376f927cd956a29d33927b4ffe37f2d795dfa4475e371795b25977373617df61c32f85b87fcf46f2f66a1c67147e82a68db3c5d279f
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 97158172 SHA512:88621e344786a78d825110dbd46a9dc811ab0a3414bde97a700b0c90991020dc31dbba89cdbed24ef2875a63ae9c0adffdbc1064262e5270d80920c9964bfb21
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.debian.tar.xz' gcc-14_14.2.0-4ubuntu2~24.04.debian.tar.xz 1950240 SHA512:2b1894ebcb104b85da3c614e0a6c2e24b1f6c1f548645996d2cb0d274301284f1f4db0809c8355997b05fe64b76a73ee1b9499c7b1c229547bad79fee1954d59
```

### `dpkg` source package: `gcc-defaults=1.214ubuntu1`

Binary Packages:

- `cpp=4:13.2.0-7ubuntu1`
- `cpp-x86-64-linux-gnu=4:13.2.0-7ubuntu1`
- `g++=4:13.2.0-7ubuntu1`
- `g++-x86-64-linux-gnu=4:13.2.0-7ubuntu1`
- `gcc=4:13.2.0-7ubuntu1`
- `gcc-x86-64-linux-gnu=4:13.2.0-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdal=3.8.4+dfsg-3ubuntu3`

Binary Packages:

- `gdal-data=3.8.4+dfsg-3ubuntu3`
- `gdal-plugins:amd64=3.8.4+dfsg-3ubuntu3`
- `libgdal-dev=3.8.4+dfsg-3ubuntu3`
- `libgdal34t64:amd64=3.8.4+dfsg-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/gdal-data/copyright`, `/usr/share/doc/gdal-plugins/copyright`, `/usr/share/doc/libgdal-dev/copyright`, `/usr/share/doc/libgdal34t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `Base64`
- `Expat`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `HPND-3i`
- `HPND-disclaimer`
- `HPND-eos`
- `HPND-p-sl-sgi`
- `HPND-sl-gl-sgi`
- `HPND-sl-sgi`
- `IJG`
- `ISC`
- `ITT`
- `Info-ZIP`
- `LGPL-2`
- `LGPL-2+`
- `PostgreSQL`
- `Qhull`
- `cpl-mem-cache`
- `fontconfig`
- `libpng`
- `public-domain`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdbm=1.23-5.1build1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.23-5.1build1`
- `libgdbm6t64:amd64=1.23-5.1build1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdcm=3.0.22-2.1ubuntu1`

Binary Packages:

- `libgdcm-dev=3.0.22-2.1ubuntu1`
- `libgdcm3.0t64:amd64=3.0.22-2.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgdcm-dev/copyright`, `/usr/share/doc/libgdcm3.0t64/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause-alike-Alexander-Chemeris`
- `BSD-3-clause-alike-CREATIS`
- `BSD-3-clause-alike-Jan-de-Vaan`
- `BSD-3-clause-alike-Mathieu-Malaterre`
- `BSD-3-clause-alike-Theodore-Ts`
- `BSD-4-clause`
- `BSL`
- `Expat`
- `LGPL-2`
- `LGPL-2+`
- `Zlib`
- `gdcmjpeg`
- `public-domain`
- `socketxx`
- `zlib/libpng`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdk-pixbuf=2.42.10+dfsg-3ubuntu3.2`

Binary Packages:

- `libgdk-pixbuf-2.0-0:amd64=2.42.10+dfsg-3ubuntu3.2`
- `libgdk-pixbuf2.0-common=2.42.10+dfsg-3ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libgdk-pixbuf-2.0-0/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-common/copyright`)

- `CC0-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.10+dfsg-3ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.10%2bdfsg-3ubuntu3.2.dsc' gdk-pixbuf_2.42.10+dfsg-3ubuntu3.2.dsc 3187 SHA512:e455481b5d70fa26e5fe8020f922282df0dcd4a9e1135030d4d064ae6d7fee63d3ee266cb7bb4327d4e07080a2230e48d3bbc2c4e080a00a93a662427daee662
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.10%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.10+dfsg.orig.tar.xz 6439240 SHA512:34f8d7d44d12308c57bd9622efdb7344bad5a89bad7043b40d4d1cab4112ff505ebb9df98d788068ddd2e44cee193e7bcb4f1d56f0432cc859075425652a06fc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.10%2bdfsg-3ubuntu3.2.debian.tar.xz' gdk-pixbuf_2.42.10+dfsg-3ubuntu3.2.debian.tar.xz 29380 SHA512:7bd6b18bf45467261595c9f73169913a038809607c1e98497a4e538a875da0309a1568e7f40581d248735fa615be51d748403b8928316c99e370afffff5b0b08
```

### `dpkg` source package: `geos=3.12.1-3build1`

Binary Packages:

- `libgeos-c1t64:amd64=3.12.1-3build1`
- `libgeos-dev=3.12.1-3build1`
- `libgeos3.12.1t64:amd64=3.12.1-3build1`

Licenses: (parsed from: `/usr/share/doc/libgeos-c1t64/copyright`, `/usr/share/doc/libgeos-dev/copyright`, `/usr/share/doc/libgeos3.12.1t64/copyright`)

- `Apache-2.0`
- `BSL-1.0`
- `Expat`
- `LGPL-2.1`
- `LGPL-2.1+`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `giflib=5.2.2-1ubuntu1`

Binary Packages:

- `libgif-dev:amd64=5.2.2-1ubuntu1`
- `libgif7:amd64=5.2.2-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgif-dev/copyright`, `/usr/share/doc/libgif7/copyright`)

- `ISC`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `git=1:2.43.0-1ubuntu7.3`

Binary Packages:

- `git=1:2.43.0-1ubuntu7.3`
- `git-man=1:2.43.0-1ubuntu7.3`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-3-clause`
- `Boost`
- `EDL-1.0`
- `Expat`
- `GPL`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.43.0-1ubuntu7.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0-1ubuntu7.3.dsc' git_2.43.0-1ubuntu7.3.dsc 2972 SHA512:dd6d41c0bbe04243367bf9198b1883826573159c89262e0bb68500710b6ea3aa171a33d83560f8b60bd14fb2caa834c831e449db80ca59085d9c6f0360154cd3
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0.orig.tar.xz' git_2.43.0.orig.tar.xz 7382996 SHA512:d0c1694ae23ff7d523e617b98d7c9a9753a2ee58f92c21b67a192d1c57398a62ff9c1a34558ae31af8dc8d95122c219f39f654e99a3b4e7cfc3dd07be9e13203
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0-1ubuntu7.3.debian.tar.xz' git_2.43.0-1ubuntu7.3.debian.tar.xz 795448 SHA512:b02a6c69c994ef229c1c75a4b09bbf0b95f89d3274dc9750c9e0fd5effb1e1b6376d5aa7cc88710e9aec47ee1475d0c251a83386bfb0e3f4f54b2c5c516e7b30
```

### `dpkg` source package: `gl2ps=1.4.2+dfsg1-2build1`

Binary Packages:

- `libgl2ps-dev=1.4.2+dfsg1-2build1`
- `libgl2ps1.4=1.4.2+dfsg1-2build1`

Licenses: (parsed from: `/usr/share/doc/libgl2ps-dev/copyright`, `/usr/share/doc/libgl2ps1.4/copyright`)

- `GL2PS-2+`
- `GPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glew=2.2.0-4build1`

Binary Packages:

- `libglew-dev:amd64=2.2.0-4build1`
- `libglew2.2:amd64=2.2.0-4build1`

Licenses: (parsed from: `/usr/share/doc/libglew-dev/copyright`, `/usr/share/doc/libglew2.2/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `Mesa`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glib2.0=2.80.0-6ubuntu3.6`

Binary Packages:

- `libglib2.0-0t64:amd64=2.80.0-6ubuntu3.6`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glibc=2.39-0ubuntu8.6`

Binary Packages:

- `libc-bin=2.39-0ubuntu8.6`
- `libc-dev-bin=2.39-0ubuntu8.6`
- `libc6:amd64=2.39-0ubuntu8.6`
- `libc6-dev:amd64=2.39-0ubuntu8.6`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.39-0ubuntu8.6
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.6.dsc' glibc_2.39-0ubuntu8.6.dsc 9387 SHA512:6467b02c2dcf5a07856a3526ece393fdcd0f7c6aa9d22f20fd42a45a02ad050f995dabd7068f1ddd9aee6ab5ae7810590e00173ecf2ded40231c880d9bf28fe8
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz' glibc_2.39.orig.tar.xz 18520988 SHA512:818f58172a52815b4338ea9f2a69ecaa3335492b9f8f64cbf8afb24c0d737982341968ecd79631cae3d3074ab0ae4bc6056fc4ba3ffe790849dc374835cd57e2
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz.asc' glibc_2.39.orig.tar.xz.asc 833 SHA512:5c054af523bbf5c2453363c023eadd1a75b6a5ff55c739011030115d3b117dbfc7d80cc74fbf157ea74a8d24aa14ff560c675374f875ec5c1ed3030e26a5ee07
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.6.debian.tar.xz' glibc_2.39-0ubuntu8.6.debian.tar.xz 467000 SHA512:5670e98edb2396b6f9fcf021c1f3da5fbb95ba7330e309f9039a5d0a3f148f4298454de70c565fdf9dfeb97edb4e9de6eeb65bd8e19d054c6346642867172d03
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2ubuntu6.1`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu6.1`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-2ubuntu6.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu6.1.dsc' gmp_6.3.0+dfsg-2ubuntu6.1.dsc 2345 SHA512:e6e58b32456ebc4fcb86e1a82553030439ff5c26bbbf48d9a26bca5ebab4d0f81fb587f262a94f8e7158edb14b538bcf3f5bc0ed0bd32ea5b1d950820b286a88
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu6.1.debian.tar.xz' gmp_6.3.0+dfsg-2ubuntu6.1.debian.tar.xz 38908 SHA512:6c64c2cacd9736f7bd88fe6364a2f6f7281d0f3031b602d3dbfed8b9035bc2f024462498dda0efdec4d3a411d15a80c6c8fa3283c149d3d0fb2f77665c470880
```

### `dpkg` source package: `gnupg2=2.4.4-2ubuntu17.4`

Binary Packages:

- `dirmngr=2.4.4-2ubuntu17.4`
- `gnupg=2.4.4-2ubuntu17.4`
- `gnupg-utils=2.4.4-2ubuntu17.4`
- `gnupg2=2.4.4-2ubuntu17.4`
- `gpg=2.4.4-2ubuntu17.4`
- `gpg-agent=2.4.4-2ubuntu17.4`
- `gpgconf=2.4.4-2ubuntu17.4`
- `gpgsm=2.4.4-2ubuntu17.4`
- `gpgv=2.4.4-2ubuntu17.4`
- `keyboxd=2.4.4-2ubuntu17.4`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gnupg2/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`, `/usr/share/doc/keyboxd/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
- `GPL-2+`
- `GPL-2.0`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.4.4-2ubuntu17.4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.dsc' gnupg2_2.4.4-2ubuntu17.4.dsc 3984 SHA512:a6a2f49070db5db2bb85b7fd916728ed4e24e21e2746b2386b27f5573c13f9c2d9d55deabeac1fd9c0ce977d66706157a31e1ed386d663d1962176d3c0df74de
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2' gnupg2_2.4.4.orig.tar.bz2 7886036 SHA512:3d1a3b08d1ce2319d238d8be96591e418ede1dc0b4ede33a4cc2fe40e9c56d5bbc27b1984736d8a786e7f292ddbc836846a8bdb4bf89f064e953c37cb54b94ef
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2.asc' gnupg2_2.4.4.orig.tar.bz2.asc 386 SHA512:abb44c8bfa59e589bdcd660f1d1a2e268bade8729d95b34263e3d3b5388d1d2276420313989777938f17f97739c554808f97a63257ca0f53d2122a346d70ec85
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz' gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz 97376 SHA512:61b874e2aa964df31649d1344281b7f99f1bde0b414719f1ff525f2e631729480d0eabf3c3e94643178a6674b3816e40ea92658e84ace8474351ef35620a464b
```

### `dpkg` source package: `gnutls28=3.8.3-1.1ubuntu3.4`

Binary Packages:

- `libgnutls30t64:amd64=3.8.3-1.1ubuntu3.4`

Licenses: (parsed from: `/usr/share/doc/libgnutls30t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `CC0 license`
- `Expat`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `GPLv3+`
- `LGPL`
- `LGPL-3`
- `LGPLv2.1+`
- `LGPLv3+_or_GPLv2+`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.3-1.1ubuntu3.4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.4.dsc' gnutls28_3.8.3-1.1ubuntu3.4.dsc 3397 SHA512:f0ba3871d3cf4b1325b0c0efa412146468fbf2fb0007972427cef545c6e84694b647b3a420e34ebfa689ccc3e2cc00166f42f84cb57f46c6d3fe9b9c6462af78
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz' gnutls28_3.8.3.orig.tar.xz 6463720 SHA512:74eddba01ce4c2ffdca781c85db3bb52c85f1db3c09813ee2b8ceea0608f92ca3912fd9266f55deb36a8ba4d01802895ca5d5d219e7d9caec45e1a8534e45a84
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz.asc' gnutls28_3.8.3.orig.tar.xz.asc 854 SHA512:8a13a834b57172b9504313eeb7d733d2c3d72971dd8adaa837bbd9d73b12fe2a67f7d07fbbaf643a34ff95acaa82458a88ce4118152ede8ece9be5a089b693c8
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.4.debian.tar.xz' gnutls28_3.8.3-1.1ubuntu3.4.debian.tar.xz 100104 SHA512:aab92b406ef2b833d663f7662fd2ac61cada09251710b44d689c1ff73bbc5b451dce04675893a752392564048b78b19118ce23532d9ce7e726a678d92e7e3d1d
```

### `dpkg` source package: `googletest=1.14.0-1`

Binary Packages:

- `google-mock:amd64=1.14.0-1`
- `googletest=1.14.0-1`
- `libgtest-dev:amd64=1.14.0-1`

Licenses: (parsed from: `/usr/share/doc/google-mock/copyright`, `/usr/share/doc/googletest/copyright`, `/usr/share/doc/libgtest-dev/copyright`)

- `BSD-C3`
- `GAP`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/googletest/1.14.0-1/


### `dpkg` source package: `graphite2=1.3.14-2build1`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `graphviz=2.42.2-9ubuntu0.1`

Binary Packages:

- `graphviz=2.42.2-9ubuntu0.1`
- `libcdt5:amd64=2.42.2-9ubuntu0.1`
- `libcgraph6:amd64=2.42.2-9ubuntu0.1`
- `libgvc6=2.42.2-9ubuntu0.1`
- `libgvpr2:amd64=2.42.2-9ubuntu0.1`
- `liblab-gamut1:amd64=2.42.2-9ubuntu0.1`
- `libpathplan4:amd64=2.42.2-9ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/graphviz/copyright`, `/usr/share/doc/libcdt5/copyright`, `/usr/share/doc/libcgraph6/copyright`, `/usr/share/doc/libgvc6/copyright`, `/usr/share/doc/libgvpr2/copyright`, `/usr/share/doc/liblab-gamut1/copyright`, `/usr/share/doc/libpathplan4/copyright`)

- `EPL-1.0`
- `MIT`
- `X/MIT`
- `zlib-style`

Source:

```console
$ apt-get source -qq --print-uris graphviz=2.42.2-9ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2-9ubuntu0.1.dsc' graphviz_2.42.2-9ubuntu0.1.dsc 3295 SHA512:5884ad13dcf56c100036eec968d16faf9c8d5368c9e62fcf0aed09f4b01d9b531b725eaf7b1a7950246fa767bd44e247bab8fe9297df1fc48652dd46a288a0d4
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2.orig.tar.bz2' graphviz_2.42.2.orig.tar.bz2 30740923 SHA512:7dab159539179df1febf4396d6bea2c071e0f311745941a07861d54b1db96a52f1328bee08148e099fa06ce5f1c9a9b6272ba60bb6147bf51b55de881a431fb3
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2-9ubuntu0.1.debian.tar.xz' graphviz_2.42.2-9ubuntu0.1.debian.tar.xz 39936 SHA512:6e42379d735552d41df6180e0c318bcedef05ce79b2222e6e18d6b8acf19aa9e5abbe365b5965fa3bf5e2da1a7cbbb77fdb2fa4d44db9ca0a783d462ab6a3dcf
```

### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gst-plugins-base1.0=1.24.2-1ubuntu0.3`

Binary Packages:

- `libgstreamer-plugins-base1.0-0:amd64=1.24.2-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libgstreamer-plugins-base1.0-0/copyright`)

- `BSD (2 clause)`
- `BSD (3 clause)`
- `GPL-2+`
- `LGPL`
- `LGPL-2+`
- `MIT/X11 (BSD like) LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris gst-plugins-base1.0=1.24.2-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2-1ubuntu0.3.dsc' gst-plugins-base1.0_1.24.2-1ubuntu0.3.dsc 4113 SHA512:6e3d08f96eb814fb623804a9ee5e3051057ea312fa35a0090c556f425a6c095676042bd8e0c719d7959e426f3df79cf097f2dab57abff34f43440d997219ce50
'http://archive.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2.orig.tar.xz' gst-plugins-base1.0_1.24.2.orig.tar.xz 2421032 SHA512:8b4ffbbf427859c4d8ba889034b00ea8314e4357645c788f6b52d65a512ce76fa1840f2a4fd562d92b213ad9dc9636db44de289bc56600ae19bce39e156b1579
'http://archive.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2.orig.tar.xz.asc' gst-plugins-base1.0_1.24.2.orig.tar.xz.asc 833 SHA512:996a9c50facd6d6b4e9496874320fcb1aa374b0ec0a14b9945238b7e233f933856f3b91cc332da2f1e246c870f51373b3d1b9de455bd3d70e51b5a32be429f70
'http://archive.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2-1ubuntu0.3.debian.tar.xz' gst-plugins-base1.0_1.24.2-1ubuntu0.3.debian.tar.xz 57212 SHA512:69318ed81bde1a8765f64aefa58680c17571444a82260646d27bed3a6f9086438c6f543286b0f80cee3624d00fb248377970302fb829538790da2fcbdedc1d5f
```

### `dpkg` source package: `gstreamer1.0=1.24.2-1ubuntu0.1`

Binary Packages:

- `libgstreamer1.0-0:amd64=1.24.2-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libgstreamer1.0-0/copyright`)

- `GPL-2+`
- `GPL-3+`
- `LGPL`
- `LGPL-2+`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris gstreamer1.0=1.24.2-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2-1ubuntu0.1.dsc' gstreamer1.0_1.24.2-1ubuntu0.1.dsc 3161 SHA512:c44b2bcb46e1bc27fa70dfbb338ef53dee528ae63614cc1727438d59de8ae60dadad8b9ec90d0dbe5e7f2457f618891fcf8b049b007010659bf4d5a93e0a74b9
'http://archive.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2.orig.tar.xz' gstreamer1.0_1.24.2.orig.tar.xz 1850672 SHA512:8d7b3e129025d66b0c3938fcb51574c378f5104cf44d1c827795f25687efc98e85bc0dac76bd8e8c4adf6434457495816a8a91a04734269722dcf7c2ed67f88b
'http://archive.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2.orig.tar.xz.asc' gstreamer1.0_1.24.2.orig.tar.xz.asc 833 SHA512:191caa06febb372a402adbfd3b1e52cc702a6c98cff1de2a47aa96edeed197a46a5fc1f14fbd43791c67bb9336dd89f45b38f7e31781464d564609bd3f5a87ff
'http://archive.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2-1ubuntu0.1.debian.tar.xz' gstreamer1.0_1.24.2-1ubuntu0.1.debian.tar.xz 50960 SHA512:a4dd33a3381c59ef061dedd01f76d4e7638fb68771437890daff17c71ee5a78f7958b363bbeef38aa04f27869038ef53756ef52c59079eecb1529ff3cdd0a508
```

### `dpkg` source package: `gtk+3.0=3.24.41-4ubuntu1.3`

Binary Packages:

- `gtk-update-icon-cache=3.24.41-4ubuntu1.3`
- `libgtk-3-0t64:amd64=3.24.41-4ubuntu1.3`
- `libgtk-3-common=3.24.41-4ubuntu1.3`

Licenses: (parsed from: `/usr/share/doc/gtk-update-icon-cache/copyright`, `/usr/share/doc/libgtk-3-0t64/copyright`, `/usr/share/doc/libgtk-3-common/copyright`)

- `Apache-2.0`
- `CC-BY-SA-4.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `SWL`
- `X11R5-permissive`
- `ZPL-2.1`
- `check-gdk-cairo-permissive`
- `other`
- `unencumbered`

Source:

```console
$ apt-get source -qq --print-uris gtk+3.0=3.24.41-4ubuntu1.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gtk%2b3.0/gtk%2b3.0_3.24.41-4ubuntu1.3.dsc' gtk+3.0_3.24.41-4ubuntu1.3.dsc 4996 SHA512:84d76dbea2324bbe2f25c07273e532050207ec8e475d2a2e410a203d32143f5a6e33f932c95e723cc224f34dd434798f83ff957c17de69b43e7440fe0db19698
'http://archive.ubuntu.com/ubuntu/pool/main/g/gtk%2b3.0/gtk%2b3.0_3.24.41.orig.tar.xz' gtk+3.0_3.24.41.orig.tar.xz 13188312 SHA512:aaf061d846fac592e71089feace302bdef1bb64bb2ad6ff30d51d90000da9084cad2fa5bf88cb75adcd789c911d94231ae60a2ca7cf97a2f5720687369a3da98
'http://archive.ubuntu.com/ubuntu/pool/main/g/gtk%2b3.0/gtk%2b3.0_3.24.41-4ubuntu1.3.debian.tar.xz' gtk+3.0_3.24.41-4ubuntu1.3.debian.tar.xz 3666360 SHA512:07bb1cfc019cd04ac0b83097d4f176729118b3d89f956c65e2845f71476e4949ae2af4d845e460b4775032bb92a750e910aef4ac4cf9b4acf75d0d78d0f57b1e
```

### `dpkg` source package: `gts=0.7.6+darcs121130-5.2build1`

Binary Packages:

- `libgts-0.7-5t64:amd64=0.7.6+darcs121130-5.2build1`

Licenses: (parsed from: `/usr/share/doc/libgts-0.7-5t64/copyright`)

- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gzip=1.12-1ubuntu3.1`

Binary Packages:

- `gzip=1.12-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu3.1.dsc' gzip_1.12-1ubuntu3.1.dsc 2042 SHA512:724f7290e5acc87e29768d9cbfa191760f3558778f2c059689535b5bccf5738ceb6f341c301e9730703060bae88e7022c396a026b7d83abfe030fe4d8619b83d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA512:116326fe991828227de150336a0c016f4fe932dfbb728a16b4a84965256d9929574a4f5cfaf3cf6bb4154972ef0d110f26ab472c93e62ec9a5fd7a5d65abea24
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu3.1.debian.tar.xz' gzip_1.12-1ubuntu3.1.debian.tar.xz 21180 SHA512:e7353110d35f58a3a5628f05f05a1744112715e9691b3c17aa0b4d0e8441997bb06c2e1d4ddbda9a4f7decadb561b43b808bab25a57f6a146c124336bc1f16ec
```

### `dpkg` source package: `harfbuzz=8.3.0-2build2`

Binary Packages:

- `libharfbuzz0b:amd64=8.3.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz0b/copyright`)

- `Apache-2.0`
- `CC0-1.0`
- `Expat`
- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with AutoConf exception`
- `GPL-2+ with Font exception`
- `GPL-2+ with LibTool exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with AutoConf exception`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `Monotype`
- `OFL-1.1`
- `UFL-1.0`
- `Unicode`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hdf5=1.10.10+repack-3.1ubuntu4`

Binary Packages:

- `hdf5-helpers=1.10.10+repack-3.1ubuntu4`
- `libhdf5-103-1t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-cpp-103-1t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-dev=1.10.10+repack-3.1ubuntu4`
- `libhdf5-fortran-102t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-hl-100t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-hl-cpp-100t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-hl-fortran-100t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-mpi-dev=1.10.10+repack-3.1ubuntu4`
- `libhdf5-openmpi-103-1t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-openmpi-cpp-103-1t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-openmpi-dev=1.10.10+repack-3.1ubuntu4`
- `libhdf5-openmpi-fortran-102t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-openmpi-hl-100t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-openmpi-hl-cpp-100t64:amd64=1.10.10+repack-3.1ubuntu4`
- `libhdf5-openmpi-hl-fortran-100t64:amd64=1.10.10+repack-3.1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/hdf5-helpers/copyright`, `/usr/share/doc/libhdf5-103-1t64/copyright`, `/usr/share/doc/libhdf5-cpp-103-1t64/copyright`, `/usr/share/doc/libhdf5-dev/copyright`, `/usr/share/doc/libhdf5-fortran-102t64/copyright`, `/usr/share/doc/libhdf5-hl-100t64/copyright`, `/usr/share/doc/libhdf5-hl-cpp-100t64/copyright`, `/usr/share/doc/libhdf5-hl-fortran-100t64/copyright`, `/usr/share/doc/libhdf5-mpi-dev/copyright`, `/usr/share/doc/libhdf5-openmpi-103-1t64/copyright`, `/usr/share/doc/libhdf5-openmpi-cpp-103-1t64/copyright`, `/usr/share/doc/libhdf5-openmpi-dev/copyright`, `/usr/share/doc/libhdf5-openmpi-fortran-102t64/copyright`, `/usr/share/doc/libhdf5-openmpi-hl-100t64/copyright`, `/usr/share/doc/libhdf5-openmpi-hl-cpp-100t64/copyright`, `/usr/share/doc/libhdf5-openmpi-hl-fortran-100t64/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hicolor-icon-theme=0.17-2`

Binary Packages:

- `hicolor-icon-theme=0.17-2`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/hicolor-icon-theme/0.17-2/


### `dpkg` source package: `highway=1.0.7-8.1build1`

Binary Packages:

- `libhwy1t64:amd64=1.0.7-8.1build1`

Licenses: (parsed from: `/usr/share/doc/libhwy1t64/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hostname=3.23+nmu2ubuntu2`

Binary Packages:

- `hostname=3.23+nmu2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `humanity-icon-theme=0.6.16`

Binary Packages:

- `humanity-icon-theme=0.6.16`

Licenses: (parsed from: `/usr/share/doc/humanity-icon-theme/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hwloc=2.10.0-1build1`

Binary Packages:

- `libhwloc-dev:amd64=2.10.0-1build1`
- `libhwloc-plugins:amd64=2.10.0-1build1`
- `libhwloc15:amd64=2.10.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libhwloc-dev/copyright`, `/usr/share/doc/libhwloc-plugins/copyright`, `/usr/share/doc/libhwloc15/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hyphen=2.8.8-7build3`

Binary Packages:

- `libhyphen0:amd64=2.8.8-7build3`

Licenses: (parsed from: `/usr/share/doc/libhyphen0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `icu=74.2-1ubuntu3.1`

Binary Packages:

- `icu-devtools=74.2-1ubuntu3.1`
- `libicu-dev:amd64=74.2-1ubuntu3.1`
- `libicu74:amd64=74.2-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu74/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=74.2-1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu3.1.dsc' icu_74.2-1ubuntu3.1.dsc 2350 SHA512:97c4d28b6887488adcf0079fbb43ec668ba2f38b9b924c391989316e6698c48fe430e5b7dd8cf5323915becbb98fe1748e19ce19402d2a3ed8416bd465de2d9a
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz' icu_74.2.orig.tar.gz 26618071 SHA512:0cbe29122370ba03a8fb5b0f1494f598748044ad2aa4d66ba65fe98ebeb88da2d73d324ad6bfc44e004846e0ab5c9a34d1fdf3d6bdb3095c0d47e929b943e6db
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz.asc' icu_74.2.orig.tar.gz.asc 659 SHA512:e961664f91a66afe898041fb42950f925854cfe7f5a287f691b90ad79c215a14300cdd1aad94a310aa2b1cdda3d850ab978d1fe2eadba5fd46f375f4bcefcd11
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu3.1.debian.tar.xz' icu_74.2-1ubuntu3.1.debian.tar.xz 64432 SHA512:967f2dfd11ea2a11f0cee4558b78b067ae2e169d279b39a1f2796457554f9147f23bb79c9f7873314c197f6a17598a989a58ab7bd3f12d49f0ec5b71a9666ed4
```

### `dpkg` source package: `imath=3.1.9-3.1ubuntu2`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.9-3.1ubuntu2`
- `libimath-dev:amd64=3.1.9-3.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `infinipath-psm=3.3+20.604758e7-6.3build1`

Binary Packages:

- `libpsm-infinipath1=3.3+20.604758e7-6.3build1`

Licenses: (parsed from: `/usr/share/doc/libpsm-infinipath1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `init-system-helpers=1.66ubuntu1`

Binary Packages:

- `init-system-helpers=1.66ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `isl=0.26-3build1.1`

Binary Packages:

- `libisl23:amd64=0.26-3build1.1`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.26-3build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26-3build1.1.dsc' isl_0.26-3build1.1.dsc 1918 SHA512:ca4cf05c5994d9b0365eee726267328a5737165723e407b29b3f61cdc91dd0d1097ee8ae4bb6d276b2877496e47e16b4296c652096d568cb92916a7db388d59c
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26.orig.tar.xz' isl_0.26.orig.tar.xz 2035560 SHA512:9b5ec16d14e48f9ac9bf9cd379d3022959cfc617ade9e0d4caf2862299564fecba09d67dbdf1a4071f2f743a4fd0fabd0b0c3d15f5cddfe7226cdd5d6c2a0c66
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26-3build1.1.debian.tar.xz' isl_0.26-3build1.1.debian.tar.xz 24948 SHA512:7e673c0e763db0be37459c38ed4523e10d3f90121f2a055d4be07acc9d07bb7a6660154baeca9157a3be624be0abf7577e792af40f535ca9161ba055d4eaf145
```

### `dpkg` source package: `iso-codes=4.16.0-1`

Binary Packages:

- `iso-codes=4.16.0-1`

Licenses: (parsed from: `/usr/share/doc/iso-codes/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/iso-codes/4.16.0-1/


### `dpkg` source package: `jansson=2.14-2build2`

Binary Packages:

- `libjansson4:amd64=2.14-2build2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `java-common=0.75+exp1`

Binary Packages:

- `default-jdk=2:1.21-75+exp1`
- `default-jdk-headless=2:1.21-75+exp1`
- `default-jre=2:1.21-75+exp1`
- `default-jre-headless=2:1.21-75+exp1`
- `java-common=0.75+exp1`

Licenses: (parsed from: `/usr/share/doc/default-jdk/copyright`, `/usr/share/doc/default-jdk-headless/copyright`, `/usr/share/doc/default-jre/copyright`, `/usr/share/doc/default-jre-headless/copyright`, `/usr/share/doc/java-common/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/java-common/0.75+exp1/


### `dpkg` source package: `jbigkit=2.1-6.1ubuntu2`

Binary Packages:

- `libjbig-dev:amd64=2.1-6.1ubuntu2`
- `libjbig0:amd64=2.1-6.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `jpeg-xl=0.7.0-10.2ubuntu6.1`

Binary Packages:

- `libjxl0.7:amd64=0.7.0-10.2ubuntu6.1`

Licenses: (parsed from: `/usr/share/doc/libjxl0.7/copyright`)

- `BSD-3-clause-Google`
- `ISC-License`

Source:

```console
$ apt-get source -qq --print-uris jpeg-xl=0.7.0-10.2ubuntu6.1
'http://archive.ubuntu.com/ubuntu/pool/universe/j/jpeg-xl/jpeg-xl_0.7.0-10.2ubuntu6.1.dsc' jpeg-xl_0.7.0-10.2ubuntu6.1.dsc 3202 SHA512:48536b4375380e14f3597382b2d111826a03e7257f761f1ca7efebc6bf4aae36e4695c96e0d043f6ca68b34f48669cadc643ca489bb9f16488faf6245f31f26c
'http://archive.ubuntu.com/ubuntu/pool/universe/j/jpeg-xl/jpeg-xl_0.7.0.orig.tar.gz' jpeg-xl_0.7.0.orig.tar.gz 1505917 SHA512:c73039606acf7b2cbc331c6787af5167d711fd1af22bc616e1f478c531b087da82c98f2cb7e88c4d1f8bcfdc4e053ae0dc99cc9a811545b7f9658041489ed04b
'http://archive.ubuntu.com/ubuntu/pool/universe/j/jpeg-xl/jpeg-xl_0.7.0-10.2ubuntu6.1.debian.tar.xz' jpeg-xl_0.7.0-10.2ubuntu6.1.debian.tar.xz 26684 SHA512:e31f68369824436364d0ebff9e7f077784aeec565a3e84f5cb2ddd1d2d6dbcc7351fc143dcfdc6e03a759169b857f0e868958fe7732ac9d86ab14d73e27fffac
```

### `dpkg` source package: `jqueryui=1.13.2+dfsg-1`

Binary Packages:

- `libjs-jquery-ui=1.13.2+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libjs-jquery-ui/copyright`)

- `CC-BY-SA-3.0`
- `CC0`
- `Expat`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/jqueryui/1.13.2+dfsg-1/


### `dpkg` source package: `json-c=0.17-1build1`

Binary Packages:

- `libjson-c-dev:amd64=0.17-1build1`
- `libjson-c5:amd64=0.17-1build1`

Licenses: (parsed from: `/usr/share/doc/libjson-c-dev/copyright`, `/usr/share/doc/libjson-c5/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `keyutils=1.6.3-3build1`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-3build1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `kmod=31+20240202-2ubuntu7.1`

Binary Packages:

- `libkmod2:amd64=31+20240202-2ubuntu7.1`

Licenses: (parsed from: `/usr/share/doc/libkmod2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris kmod=31+20240202-2ubuntu7.1
'http://archive.ubuntu.com/ubuntu/pool/main/k/kmod/kmod_31%2b20240202-2ubuntu7.1.dsc' kmod_31+20240202-2ubuntu7.1.dsc 2288 SHA512:64558f5c34ab88a3eb2d87b138efc6a6e9e23e30e67d1c8ca8c654c5fe9db5386ba23191184031e573e33995bc22257ac13ee3cca01e0ea10f1fd97af1c60c16
'http://archive.ubuntu.com/ubuntu/pool/main/k/kmod/kmod_31%2b20240202.orig.tar.xz' kmod_31+20240202.orig.tar.xz 253852 SHA512:9f9f344fbbcde8d3d479ff0c48adabb96442ccdf4190dcfde1c5ee797e2e85c6518b4a9d9451ebb0cf6d36364cd3e6a8f4301f87659b6b9b0b0cb0c7d3535a93
'http://archive.ubuntu.com/ubuntu/pool/main/k/kmod/kmod_31%2b20240202-2ubuntu7.1.debian.tar.xz' kmod_31+20240202-2ubuntu7.1.debian.tar.xz 15108 SHA512:e4c0c7aaec0900878ffafa2511e177fcde2a3a3b8178daa39e4f8e3546259be08401b770bfd111b78f2083571de3557da3524a75026b6d6eb3cd58859e379fac
```

### `dpkg` source package: `krb5=1.20.1-6ubuntu2.6`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.20.1-6ubuntu2.6`
- `libk5crypto3:amd64=1.20.1-6ubuntu2.6`
- `libkrb5-3:amd64=1.20.1-6ubuntu2.6`
- `libkrb5support0:amd64=1.20.1-6ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.20.1-6ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.dsc' krb5_1.20.1-6ubuntu2.6.dsc 4125 SHA512:6bafe41a37f8bf133ccd7e1aa0d63a1464b411af60ee408a03de69debae259794606011ff42370d168f6bf74af34d90b635c007c9876657af7124259af84c99a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA512:6f57479f13f107cd84f30de5c758eb6b9fc59171329c13e5da6073b806755f8d163eb7bd84767ea861ad6458ea0c9eeb00ee044d3bcad01ef136e9888564b6a2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA512:1d3312bd67581e07adfdadf2c5fe394179631d8add8bd075efefe982a0de22369004e60a14422d426382c8c591e4181b9897088afe9d4e86f0b5a97e5954c67a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.debian.tar.xz' krb5_1.20.1-6ubuntu2.6.debian.tar.xz 122284 SHA512:402e34a374db1ece1ce0a604d84d697c590596d5e99601895d9c50c96fcbd8cb08d21b04201296411324b3ae4f169f2295aff825cee182cbbf139ccb16588fc9
```

### `dpkg` source package: `lame=3.100-6build1`

Binary Packages:

- `libmp3lame0:amd64=3.100-6build1`

Licenses: (parsed from: `/usr/share/doc/libmp3lame0/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-1+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `zlib/libpng`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lapack=3.12.0-3build1.1`

Binary Packages:

- `libblas-dev:amd64=3.12.0-3build1.1`
- `libblas3:amd64=3.12.0-3build1.1`
- `liblapack-dev:amd64=3.12.0-3build1.1`
- `liblapack3:amd64=3.12.0-3build1.1`

Licenses: (parsed from: `/usr/share/doc/libblas-dev/copyright`, `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack-dev/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.12.0-3build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0-3build1.1.dsc' lapack_3.12.0-3build1.1.dsc 3417 SHA512:76e42e9014e007655171abcca32667d3d200dd35bc9fc5cca0a1402e79cfb56132334fbc2c19493f9dde445c101a1ac34aa46af3fcea2c5a468a2435ab293c4d
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0.orig.tar.gz' lapack_3.12.0.orig.tar.gz 7933607 SHA512:f8f3c733a0221be0b3f5618235408ac59cbd4e5f1c4eab5f509b831a6ec6a9ef14b8849aa6ea10810df1aff90186ca454d15e9438d1dd271c2449d42d3da9dda
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0-3build1.1.debian.tar.xz' lapack_3.12.0-3build1.1.debian.tar.xz 28916 SHA512:42ca6ffeaec371df0f7242aa6fa932a9cfc3044baa941063dae3be23a4645c5c12e94e51d6c20969a1f5627dbedd165c7e72532d336379fb70248338fed89242
```

### `dpkg` source package: `lcms2=2.14-2build1`

Binary Packages:

- `liblcms2-2:amd64=2.14-2build1`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `leptonlib=1.82.0-3build4`

Binary Packages:

- `liblept5:amd64=1.82.0-3build4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lerc=4.0.0+ds-4ubuntu2`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-4ubuntu2`
- `liblerc4:amd64=4.0.0+ds-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libaec=1.1.2-1build1`

Binary Packages:

- `libaec-dev:amd64=1.1.2-1build1`
- `libaec0:amd64=1.1.2-1build1`
- `libsz2:amd64=1.1.2-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libarchive=3.7.2-2ubuntu0.5`

Binary Packages:

- `libarchive13t64:amd64=3.7.2-2ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/libarchive13t64/copyright`)

- `Apache-2.0`
- `BSD-1-clause-UCB`
- `BSD-124-clause-UCB`
- `BSD-2-clause`
- `BSD-3-clause-UCB`
- `BSD-4-clause-UCB`
- `CC0-1.0`
- `Expat`
- `OpenSSL+SSLeay`
- `PD`

Source:

```console
$ apt-get source -qq --print-uris libarchive=3.7.2-2ubuntu0.5
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2-2ubuntu0.5.dsc' libarchive_3.7.2-2ubuntu0.5.dsc 2558 SHA512:e79445b3eaf1f19733ff9032f30ea854ff8749d3c33edc3f308d3c4a13af2fb38180ae4986f7dbc8060bf613ebdfd335839e6791f0281e8a7653025a478b06e3
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2.orig.tar.xz' libarchive_3.7.2.orig.tar.xz 5237056 SHA512:a21bebb27b808cb7d2ed13a70739904a1b7b55661d8dea83c9897a0129cf71e20c962f13666c571782ff0f4f753ca885619c2097d9e7691c2dee4e6e4b9a2971
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2.orig.tar.xz.asc' libarchive_3.7.2.orig.tar.xz.asc 659 SHA512:c2ce850088245d7723720737d74d1cc1819984d01b3f9e4ed96b0757f4c6d6d511b78792181a12400c563632d74edcd0c2c3a4b7527cba40ada7ef74488078fc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2-2ubuntu0.5.debian.tar.xz' libarchive_3.7.2-2ubuntu0.5.debian.tar.xz 34236 SHA512:5b91c3314610755887e439998c5c4d5a3c016e83068c81a9a8c0c07e2d30cfd2c84c0c59674ecff25dea838fbbe4fb98cface151d2f05f95e62f80b06b9bcd1a
```

### `dpkg` source package: `libassuan=2.5.6-1build1`

Binary Packages:

- `libassuan0:amd64=2.5.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libassuan0/copyright`)

- `GAP`
- `GAP~FSF`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with libtool exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libbluray=1:1.3.4-1build1`

Binary Packages:

- `libbluray2:amd64=1:1.3.4-1build1`

Licenses: (parsed from: `/usr/share/doc/libbluray2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.0`
- `custom`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libbsd=0.12.1-1build1.1`

Binary Packages:

- `libbsd0:amd64=0.12.1-1build1.1`

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
$ apt-get source -qq --print-uris libbsd=0.12.1-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1-1build1.1.dsc' libbsd_0.12.1-1build1.1.dsc 2458 SHA512:2193901671b12cfde5d8c16e84603d49effd3dbc0f0161848df294cf2eeb4db2680e3c0a698e27d760e563e98bc68b738c7a92021a8e847fc211eca0083b136b
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1.orig.tar.xz' libbsd_0.12.1.orig.tar.xz 444048 SHA512:c45c7861b63295c118f53ce868437ad73887b6764708d0a348b796f5abe2cefc9adbb0dd3be23f6348d6bf63a9920a13b7f90d065299cac5a05ce0376211073a
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1.orig.tar.xz.asc' libbsd_0.12.1.orig.tar.xz.asc 833 SHA512:f6c545317b9fe06ce6cfd34e579a5959524ad40f2b25d13617888dd9b79cd5b483e7d24aead540a0bf30a71cd11cc7ca932f41ae60a797b0e881474de9f30543
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1-1build1.1.debian.tar.xz' libbsd_0.12.1-1build1.1.debian.tar.xz 18732 SHA512:7c71721236a65058e265e1a47ae4c81aaeab16e3340c6bf734da85c61069150e817194e87087c6a6315c4e0dd0678acaca55fa60463fa1156ee811b5d963abfd
```

### `dpkg` source package: `libcap-ng=0.8.4-2build2`

Binary Packages:

- `libcap-ng0:amd64=0.8.4-2build2`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap2=1:2.66-5ubuntu2.2`

Binary Packages:

- `libcap2:amd64=1:2.66-5ubuntu2.2`
- `libcap2-bin=1:2.66-5ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`, `/usr/share/doc/libcap2-bin/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.66-5ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu2.2.dsc' libcap2_2.66-5ubuntu2.2.dsc 2319 SHA512:563c9151918f788fb7ea210505c3f2f4c6375af6fa58f760d4efd051ac3bcb9a0dff8fc0407486c834b5a477831af8a50aaeb14728c93ffe88edf48e2a86391f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA512:ac005b622f6e065f30ce282a5c87240e7b9da75366ee537aa4835bc501b44bc242c10a4ba4dc070e2415fc7f635d1c3c4e45fbeeaf962cf7973dda82bf6377f0
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu2.2.debian.tar.xz' libcap2_2.66-5ubuntu2.2.debian.tar.xz 23076 SHA512:fd58def706a8d3f3f594ad986bf9385c2cba8af6f73f4bb04011815fe8b1e700368a2a15e7390842b3aba9ae72de9928009731bf1f318b48d8975e505f8f7f33
```

### `dpkg` source package: `libcbor=0.10.2-1.2ubuntu2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-1.2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdatrie=0.2.13-3build1`

Binary Packages:

- `libdatrie1:amd64=0.2.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdc1394=2.2.6-4build1`

Binary Packages:

- `libdc1394-25:amd64=2.2.6-4build1`
- `libdc1394-dev:amd64=2.2.6-4build1`

Licenses: (parsed from: `/usr/share/doc/libdc1394-25/copyright`, `/usr/share/doc/libdc1394-dev/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libde265=1.0.15-1build3`

Binary Packages:

- `libde265-0:amd64=1.0.15-1build3`
- `libde265-dev:amd64=1.0.15-1build3`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`, `/usr/share/doc/libde265-dev/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdeflate=1.19-1build1.1`

Binary Packages:

- `libdeflate-dev:amd64=1.19-1build1.1`
- `libdeflate0:amd64=1.19-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.19-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.19-1build1.1.dsc' libdeflate_1.19-1build1.1.dsc 2306 SHA512:aaa78d544ad00e43f6e425498c77690fd65f3441b88d9501cc2238532ed8414de7794be34bb7e1e37519d5be0c5f2d45c123b3694571271b2a8641d77f440482
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.19.orig.tar.gz' libdeflate_1.19.orig.tar.gz 187684 SHA512:fe57542a0d28ad61d70bef9b544bb6805f9f30930b16432712b3b1caab041f1f4e64315a4306a0635b96c2632239c5af0e45a3915581d0b89975729fc2e95613
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.19-1build1.1.debian.tar.xz' libdeflate_1.19-1build1.1.debian.tar.xz 5004 SHA512:1a5ea09ac798d5c426db489bbee748e18c05e2a3dfc38c1e6d3c59612b006b0f26ef2058a4ece36e693d458d5c631c79c653beb2ca074b57f7fda7d0e0fb7f45
```

### `dpkg` source package: `libdrm=2.4.122-1~ubuntu0.24.04.2`

Binary Packages:

- `libdrm-amdgpu1:amd64=2.4.122-1~ubuntu0.24.04.2`
- `libdrm-common=2.4.122-1~ubuntu0.24.04.2`
- `libdrm-intel1:amd64=2.4.122-1~ubuntu0.24.04.2`
- `libdrm2:amd64=2.4.122-1~ubuntu0.24.04.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libedit=3.1-20230828-1build1`

Binary Packages:

- `libedit2:amd64=3.1-20230828-1build1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libepoxy=1.5.10-1build1`

Binary Packages:

- `libepoxy0:amd64=1.5.10-1build1`

Licenses: (parsed from: `/usr/share/doc/libepoxy0/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `liberror-perl=0.17029-2`

Binary Packages:

- `liberror-perl=0.17029-2`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/liberror-perl/0.17029-2/


### `dpkg` source package: `libevdev=1.13.1+dfsg-1build1`

Binary Packages:

- `libevdev2:amd64=1.13.1+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libevdev2/copyright`)

- `Apache-2.0`
- `BSD-3`
- `GPL-2`
- `GPL-2+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libevent=2.1.12-stable-9ubuntu2`

Binary Packages:

- `libevent-2.1-7t64:amd64=2.1.12-stable-9ubuntu2`
- `libevent-core-2.1-7t64:amd64=2.1.12-stable-9ubuntu2`
- `libevent-dev=2.1.12-stable-9ubuntu2`
- `libevent-extra-2.1-7t64:amd64=2.1.12-stable-9ubuntu2`
- `libevent-openssl-2.1-7t64:amd64=2.1.12-stable-9ubuntu2`
- `libevent-pthreads-2.1-7t64:amd64=2.1.12-stable-9ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libevent-2.1-7t64/copyright`, `/usr/share/doc/libevent-core-2.1-7t64/copyright`, `/usr/share/doc/libevent-dev/copyright`, `/usr/share/doc/libevent-extra-2.1-7t64/copyright`, `/usr/share/doc/libevent-openssl-2.1-7t64/copyright`, `/usr/share/doc/libevent-pthreads-2.1-7t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSL`
- `Expat`
- `FSFUL`
- `FSFULLR`
- `FSFULLR-No-Warranty`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libexif=0.6.24-1build2`

Binary Packages:

- `libexif-dev:amd64=0.6.24-1build2`
- `libexif12:amd64=0.6.24-1build2`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-2-Clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libfabric=1.17.0-3build2`

Binary Packages:

- `libfabric1:amd64=1.17.0-3build2`

Licenses: (parsed from: `/usr/share/doc/libfabric1/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libffi=3.4.6-1build1`

Binary Packages:

- `libffi8:amd64=3.4.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

- `Expat`
- `GPL`
- `GPL-2+`
- `GPL-3+`
- `LGPL-2.1+`
- `MPL-1.1`
- `X11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libfido2=1.14.0-1build3`

Binary Packages:

- `libfido2-1:amd64=1.14.0-1build3`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgcrypt20=1.10.3-2build1`

Binary Packages:

- `libgcrypt20:amd64=1.10.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgd2=2.3.3-9ubuntu5`

Binary Packages:

- `libgd3:amd64=2.3.3-9ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libgd3/copyright`)

- `BSD-3-clause`
- `GAP~Makefile.in`
- `GAP~configure`
- `GD`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `HPND`
- `MIT`
- `WEBP`
- `XFIG`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgeotiff=1.7.1-5build1`

Binary Packages:

- `libgeotiff-dev:amd64=1.7.1-5build1`
- `libgeotiff5:amd64=1.7.1-5build1`

Licenses: (parsed from: `/usr/share/doc/libgeotiff-dev/copyright`, `/usr/share/doc/libgeotiff5/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `GPL-2`
- `GPL-2+`
- `HPND-sl-sgi`
- `MIT`
- `attribution`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libglu=9.0.2-1.1build1`

Binary Packages:

- `libglu1-mesa:amd64=9.0.2-1.1build1`
- `libglu1-mesa-dev:amd64=9.0.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libglu1-mesa/copyright`, `/usr/share/doc/libglu1-mesa-dev/copyright`)

- `GPL-2`
- `SGI-1.1`
- `SGI-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libglvnd=1.7.0-1build1`

Binary Packages:

- `libegl-dev:amd64=1.7.0-1build1`
- `libegl1:amd64=1.7.0-1build1`
- `libgl-dev:amd64=1.7.0-1build1`
- `libgl1:amd64=1.7.0-1build1`
- `libgles-dev:amd64=1.7.0-1build1`
- `libgles1:amd64=1.7.0-1build1`
- `libgles2:amd64=1.7.0-1build1`
- `libglvnd-core-dev:amd64=1.7.0-1build1`
- `libglvnd-dev:amd64=1.7.0-1build1`
- `libglvnd0:amd64=1.7.0-1build1`
- `libglx-dev:amd64=1.7.0-1build1`
- `libglx0:amd64=1.7.0-1build1`
- `libopengl-dev:amd64=1.7.0-1build1`
- `libopengl0:amd64=1.7.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libegl-dev/copyright`, `/usr/share/doc/libegl1/copyright`, `/usr/share/doc/libgl-dev/copyright`, `/usr/share/doc/libgl1/copyright`, `/usr/share/doc/libgles-dev/copyright`, `/usr/share/doc/libgles1/copyright`, `/usr/share/doc/libgles2/copyright`, `/usr/share/doc/libglvnd-core-dev/copyright`, `/usr/share/doc/libglvnd-dev/copyright`, `/usr/share/doc/libglvnd0/copyright`, `/usr/share/doc/libglx-dev/copyright`, `/usr/share/doc/libglx0/copyright`, `/usr/share/doc/libopengl-dev/copyright`, `/usr/share/doc/libopengl0/copyright`)

- `Apache-2.0`
- `BSD-1-clause`
- `GPL`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgpg-error=1.47-3build2.1`

Binary Packages:

- `libgpg-error0:amd64=1.47-3build2.1`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.47-3build2.1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build2.1.dsc' libgpg-error_1.47-3build2.1.dsc 3007 SHA512:4123fef7fe452ad802c1f3d38e63d9bfc0b97610a9b32359316a5cb1fc4d85e7842804360e341e0ad9e52d876c5a0a992a76d094a9c08831af829c6462bfa127
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2' libgpg-error_1.47.orig.tar.bz2 1020862 SHA512:bbb4b15dae75856ee5b1253568674b56ad155524ae29a075cb5b0a7e74c4af685131775c3ea2226fff2f84ef80855e77aa661645d002b490a795c7ae57b66a30
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2.asc' libgpg-error_1.47.orig.tar.bz2.asc 228 SHA512:babf3a17429aa7ad5d952099ea8d21bb5c9ba1bc74ea46f3027e0293449c32365208a05e141fa0bf033491320679b0b212f49919452f3dc63cce5d7f355d7195
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build2.1.debian.tar.xz' libgpg-error_1.47-3build2.1.debian.tar.xz 18776 SHA512:7e9c008e3d0501fe45d0f9b342d8a8bf88ef7995bba63b458aa419a4592606ad71f731c54287e6e32e6533c84420206f97f8e031a999df6d57a8fd45328f6f55
```

### `dpkg` source package: `libgphoto2=2.5.31-2.1build2`

Binary Packages:

- `libgphoto2-6t64:amd64=2.5.31-2.1build2`
- `libgphoto2-dev:amd64=2.5.31-2.1build2`
- `libgphoto2-port12t64:amd64=2.5.31-2.1build2`

Licenses: (parsed from: `/usr/share/doc/libgphoto2-6t64/copyright`, `/usr/share/doc/libgphoto2-dev/copyright`, `/usr/share/doc/libgphoto2-port12t64/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `IJG`
- `LGPL-1.1+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `other-2`
- `other-3`
- `public-domain`
- `public-domain-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgsm=1.0.22-1build1`

Binary Packages:

- `libgsm1:amd64=1.0.22-1build1`

Licenses: (parsed from: `/usr/share/doc/libgsm1/copyright`)

- `TU-Berlin-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgudev=238-5ubuntu1`

Binary Packages:

- `libgudev-1.0-0:amd64=1:238-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgudev-1.0-0/copyright`)

- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libhdf4=4.2.16-4build1`

Binary Packages:

- `libhdf4-0-alt:amd64=4.2.16-4build1`
- `libhdf4-alt-dev=4.2.16-4build1`

Licenses: (parsed from: `/usr/share/doc/libhdf4-0-alt/copyright`, `/usr/share/doc/libhdf4-alt-dev/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `HDF4`
- `HPND-sl-gl-sgi`
- `NetCDF`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libheif=1.17.6-1ubuntu4.2`

Binary Packages:

- `libheif-dev:amd64=1.17.6-1ubuntu4.2`
- `libheif-plugin-aomdec:amd64=1.17.6-1ubuntu4.2`
- `libheif-plugin-libde265:amd64=1.17.6-1ubuntu4.2`
- `libheif1:amd64=1.17.6-1ubuntu4.2`

Licenses: (parsed from: `/usr/share/doc/libheif-dev/copyright`, `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

- `BOOST-1.0`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libheif=1.17.6-1ubuntu4.2
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6-1ubuntu4.2.dsc' libheif_1.17.6-1ubuntu4.2.dsc 3350 SHA512:98daa684a4a1ca36ee8064934ab5e4ca564012e22a3aeeac35f2413a159600602712e98b1884b49496c0a88641efb59eb34143e2bd2464e89925061a92dcb3dc
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6.orig.tar.gz' libheif_1.17.6.orig.tar.gz 1433302 SHA512:47d93df4f584979cea26af74cd8543b13398356b5fd46b1b378f7738cee471e80b7e117f6ce307674a549182f5ce22a577c6e79a6e72fe166421efc4be04687a
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6-1ubuntu4.2.debian.tar.xz' libheif_1.17.6-1ubuntu4.2.debian.tar.xz 12620 SHA512:9759bc78516a2bc9d0780f570f25efd295a5525373adefaa2733c0bf53e5e8cd7664bd6c0a4f03fa84bda9604a7e90d67b097f520371eba154365a5f0c9c8987
```

### `dpkg` source package: `libice=2:1.0.10-1build3`

Binary Packages:

- `libice-dev:amd64=2:1.0.10-1build3`
- `libice6:amd64=2:1.0.10-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libidn2=2.3.7-2build1.1`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2build1.1`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.7-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build1.1.dsc' libidn2_2.3.7-2build1.1.dsc 2651 SHA512:5e382469d7280794c3eac36d0837cdf31bf2719e1dd6332d428da56de2960e7375558e65102359bb46af8c23724cf8d812a2900d36deb70d977e2069dc82db32
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA512:eab5702bc0baed45492f8dde43a4d2ea3560ad80645e5f9e0cfa8d3b57bccd7fd782d04638e000ba07924a5d9f85e760095b55189188c4017b94705bef9b4a66
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA512:00e5f8c3b6b1aef9ee341db99b339217080a57dbe65fba56798d60ad4be971a9535d8ae27e1f243b18b9fc9e900ada6c452b040a6c8094d5e05d8a76d1d79c03
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build1.1.debian.tar.xz' libidn2_2.3.7-2build1.1.debian.tar.xz 16468 SHA512:5f8a3e69bcf2dfe58617153b4da23ea1fd9cf9c6aaf894045b8e8f6cb2ab0d8ce73df204fe165fd7ebad3dfda1ddfc1b1442ce5c99fa00d224e3924df64e133c
```

### `dpkg` source package: `libinput=1.25.0-1ubuntu3.2`

Binary Packages:

- `libinput-bin=1.25.0-1ubuntu3.2`
- `libinput10:amd64=1.25.0-1ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libinput-bin/copyright`, `/usr/share/doc/libinput10/copyright`)

- `Expat`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris libinput=1.25.0-1ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libinput/libinput_1.25.0-1ubuntu3.2.dsc' libinput_1.25.0-1ubuntu3.2.dsc 2590 SHA512:418a1bb1db1dec484ed6ed9457bf08782a59c093ad91e6ea21da5f7f0b26d5c1e4c7b9b7271e0da211a3662cbff418e0672c31d9b6001722cfbbf9c655015f5e
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libinput/libinput_1.25.0.orig.tar.gz' libinput_1.25.0.orig.tar.gz 1016846 SHA512:17c668d04e3ff7d3e99519f7e7fe37377bd25e90ff36acc8c3f06f6de31265514780a0823b6fbd5712272a6b6f759bf768cb35b4f68c29828c1964899e9ee752
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libinput/libinput_1.25.0-1ubuntu3.2.debian.tar.xz' libinput_1.25.0-1ubuntu3.2.debian.tar.xz 12912 SHA512:4fb77fe5bb166691dc541ca19f64c543cbe0e73022428b65a04b76bc5bd9c1ab05188caae06527278190b479c6e23ad6f71b0cd4620a9469772b38387e5b02d0
```

### `dpkg` source package: `libjpeg-turbo=2.1.5-2ubuntu2`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-2ubuntu2`
- `libjpeg-turbo8-dev:amd64=2.1.5-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`, `/usr/share/doc/libjpeg-turbo8-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu11`

Binary Packages:

- `libjpeg-dev:amd64=8c-2ubuntu11`
- `libjpeg8:amd64=8c-2ubuntu11`
- `libjpeg8-dev:amd64=8c-2ubuntu11`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg8/copyright`, `/usr/share/doc/libjpeg8-dev/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libjsoncpp=1.9.5-6build1`

Binary Packages:

- `libjsoncpp-dev:amd64=1.9.5-6build1`
- `libjsoncpp25:amd64=1.9.5-6build1`

Licenses: (parsed from: `/usr/share/doc/libjsoncpp-dev/copyright`, `/usr/share/doc/libjsoncpp25/copyright`)

- `Expat_or_PublicDomain_or_DualExpatPD`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libkml=1.3.0-12build1`

Binary Packages:

- `libkml-dev:amd64=1.3.0-12build1`
- `libkmlbase1t64:amd64=1.3.0-12build1`
- `libkmlconvenience1t64:amd64=1.3.0-12build1`
- `libkmldom1t64:amd64=1.3.0-12build1`
- `libkmlengine1t64:amd64=1.3.0-12build1`
- `libkmlregionator1t64:amd64=1.3.0-12build1`
- `libkmlxsd1t64:amd64=1.3.0-12build1`

Licenses: (parsed from: `/usr/share/doc/libkml-dev/copyright`, `/usr/share/doc/libkmlbase1t64/copyright`, `/usr/share/doc/libkmlconvenience1t64/copyright`, `/usr/share/doc/libkmldom1t64/copyright`, `/usr/share/doc/libkmlengine1t64/copyright`, `/usr/share/doc/libkmlregionator1t64/copyright`, `/usr/share/doc/libkmlxsd1t64/copyright`)

- `BSD-3-Clause`
- `GPL-3`
- `GPL-3+`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libksba=1.6.6-1build1`

Binary Packages:

- `libksba8:amd64=1.6.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libmd=1.1.0-2build1.1`

Binary Packages:

- `libmd0:amd64=1.1.0-2build1.1`

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
$ apt-get source -qq --print-uris libmd=1.1.0-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build1.1.dsc' libmd_1.1.0-2build1.1.dsc 2391 SHA512:f8b23db30a025da74030294c8580158376e908df287cf62cd8d7901e600c015514080a48a069d141c86ab7d157a9dce220d1186a9d6d693fe6916ffa5747b289
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build1.1.debian.tar.xz' libmd_1.1.0-2build1.1.debian.tar.xz 8448 SHA512:b013b32fbc71ca9195e4ce9b25f5440cf746e539d72090a0f50e226783ee4885050f8e245fe75fe76775c84d6dcaf6ce684cbd9dd89d09265fae3c9f27a885af
```

### `dpkg` source package: `libnl3=3.7.0-0.3build1.1`

Binary Packages:

- `libnl-3-200:amd64=3.7.0-0.3build1.1`
- `libnl-3-dev:amd64=3.7.0-0.3build1.1`
- `libnl-route-3-200:amd64=3.7.0-0.3build1.1`
- `libnl-route-3-dev:amd64=3.7.0-0.3build1.1`

Licenses: (parsed from: `/usr/share/doc/libnl-3-200/copyright`, `/usr/share/doc/libnl-3-dev/copyright`, `/usr/share/doc/libnl-route-3-200/copyright`, `/usr/share/doc/libnl-route-3-dev/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libnl3=3.7.0-0.3build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnl3/libnl3_3.7.0-0.3build1.1.dsc' libnl3_3.7.0-0.3build1.1.dsc 3415 SHA512:41a04ef3f5d47bedab878719438437786dc8dae2530eb8507f902e76171b9864196f37ffbbfe9cc474e43904e1eb9f87c5a6a0c11d9333d171c09944029b7603
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnl3/libnl3_3.7.0.orig.tar.gz' libnl3_3.7.0.orig.tar.gz 1000913 SHA512:80fbbc079299c90afd2a5eda62e4d4f98bf4ef23958c3ce5101f4ed4d81d783af733213bb3bab15f218555d8460bc2394898f909f4ac024fc27281faec86a041
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnl3/libnl3_3.7.0.orig.tar.gz.asc' libnl3_3.7.0.orig.tar.gz.asc 862 SHA512:8934b6fb3a9c2aac9519f0eed80da79ae407ee53900c910a238d5c7767b8b0ae642889b78aef5af00a6de74e11ba4d2066ac75e5fa2cb8ed2eb7301da9ac4e5e
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnl3/libnl3_3.7.0-0.3build1.1.debian.tar.xz' libnl3_3.7.0-0.3build1.1.debian.tar.xz 26600 SHA512:618659dbbb5986a344da8e1d113265fad392cea572d6ec80a452c20f5b9821e284cb50f3c1627e8b02bfbe6d1a9883cb0f95829ca3c81c1a6fa52724e11b39e6
```

### `dpkg` source package: `libogg=1.3.5-3build1`

Binary Packages:

- `libogg-dev:amd64=1.3.5-3build1`
- `libogg0:amd64=1.3.5-3build1`

Licenses: (parsed from: `/usr/share/doc/libogg-dev/copyright`, `/usr/share/doc/libogg0/copyright`)

- `BSD-3-clause`
- `rfc3533-license`
- `rfc5334-license`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libopenmpt=0.7.3-1.1build3`

Binary Packages:

- `libopenmpt0t64:amd64=0.7.3-1.1build3`

Licenses: (parsed from: `/usr/share/doc/libopenmpt0t64/copyright`)

- `BSD-3-clause`
- `BSL-1.0`
- `GNU-All-Permissive-License`
- `GNU-All-Permissive-License-FSF`
- `GPL-2`
- `GPL-2+ with Autoconf exception`
- `GPL-2+ with LibTool exception`
- `GPL-3`
- `GPL-3+ with AutoConf exception`
- `GPL-3+ with Autoconf Macros exception`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpcap=1.10.4-4.1ubuntu3`

Binary Packages:

- `libpcap0.8t64:amd64=1.10.4-4.1ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpciaccess=0.17-3ubuntu0.24.04.2`

Binary Packages:

- `libpciaccess0:amd64=0.17-3ubuntu0.24.04.2`

Licenses: (parsed from: `/usr/share/doc/libpciaccess0/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libpciaccess=0.17-3ubuntu0.24.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.17-3ubuntu0.24.04.2.dsc' libpciaccess_0.17-3ubuntu0.24.04.2.dsc 2430 SHA512:95e0f9ffae52e8d53494c9efc6dcfc94df0ea87c9b10c6789ab4e35d247a338c070feff26690361b4520043aff38fcd3c849605ddfa410b3e58915503f499bc6
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.17.orig.tar.gz' libpciaccess_0.17.orig.tar.gz 490419 SHA512:94d55cea42213f372f29ed3f57502b7d57be3b2bc5fc28d709133c9d8acf8b8fd67bb5e42ba5787fb88dd70602780c7f111e575ffdddeca24bec9226ae7cd534
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.17.orig.tar.gz.asc' libpciaccess_0.17.orig.tar.gz.asc 801 SHA512:fe1374fb37c68fd4ba560aae3958e70974f43f2efe00004c218d18a56faafef3f24073a30900eca77bac7d781ae253e49f03b95b68951056fb498efc3e0e92de
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.17-3ubuntu0.24.04.2.diff.gz' libpciaccess_0.17-3ubuntu0.24.04.2.diff.gz 34865 SHA512:b22fc51530c95a641291049ab66fa39a83c9e9b221480721d169ca98aed897721d91e49284620f6087655fd252c8e34faf906eb8882cbd02c553fb4ee52f78ed
```

### `dpkg` source package: `libpgm=5.3.128~dfsg-2.1build1`

Binary Packages:

- `libpgm-5.3-0t64:amd64=5.3.128~dfsg-2.1build1`

Licenses: (parsed from: `/usr/share/doc/libpgm-5.3-0t64/copyright`)

- `BSD-3-clause`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpng1.6=1.6.43-5ubuntu0.3`

Binary Packages:

- `libpng-dev:amd64=1.6.43-5ubuntu0.3`
- `libpng16-16t64:amd64=1.6.43-5ubuntu0.3`

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


### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpsm2=11.2.185-2build1`

Binary Packages:

- `libpsm2-2=11.2.185-2build1`

Licenses: (parsed from: `/usr/share/doc/libpsm2-2/copyright`)

- `BSD-3-Clause/Intel`
- `BSD-3-Clause/TT`
- `BSD-3-Clause/zlib`
- `BSD-4-Clause/UC`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpthread-stubs=0.4-1build3`

Binary Packages:

- `libpthread-stubs0-dev:amd64=0.4-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `librabbitmq=0.11.0-1build2`

Binary Packages:

- `librabbitmq4:amd64=0.11.0-1build2`

Licenses: (parsed from: `/usr/share/doc/librabbitmq4/copyright`)

- `BSD-Author`
- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libraw1394=2.1.2-2build3`

Binary Packages:

- `libraw1394-11:amd64=2.1.2-2build3`
- `libraw1394-dev:amd64=2.1.2-2build3`

Licenses: (parsed from: `/usr/share/doc/libraw1394-11/copyright`, `/usr/share/doc/libraw1394-dev/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `librist=0.2.10+dfsg-2`

Binary Packages:

- `librist4:amd64=0.2.10+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/librist4/copyright`)

- `BSD-1-clause`
- `BSD-2-clause`
- `ISC`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/librist/0.2.10+dfsg-2/


### `dpkg` source package: `librsvg=2.58.0+dfsg-1build1`

Binary Packages:

- `librsvg2-2:amd64=2.58.0+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/librsvg2-2/copyright`)

- `0BSD`
- `0BSD,`
- `Apache-2.0`
- `Apache-2.0,`
- `BSD-2-clause`
- `BSD-2-clause,`
- `BSD-3-clause`
- `BSD-3-clause,`
- `Boost-1.0`
- `Boost-1.0,`
- `CC-zero-waive-1.0-us`
- `Expat`
- `Expat,`
- `FSFAP`
- `LGPL-2`
- `LGPL-2+`
- `MPL-2.0`
- `MPL-2.0,`
- `OFL-1.1`
- `Sun-permissive`
- `Sun-permissive,`
- `Unlicense`
- `Unlicense,`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `librttopo=1.1.0-3build2`

Binary Packages:

- `librttopo-dev:amd64=1.1.0-3build2`
- `librttopo1:amd64=1.1.0-3build2`

Licenses: (parsed from: `/usr/share/doc/librttopo-dev/copyright`, `/usr/share/doc/librttopo1/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libseccomp=2.5.5-1ubuntu3.1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu3.1.dsc' libseccomp_2.5.5-1ubuntu3.1.dsc 2838 SHA512:bb64748ac6031e104c70a59a06e1b00ab4c516e3342b2bef50a7cd0dcf4fe3bfc316288da871994cfe39b42da968831efb20a8c51c3df74ab82983d9ecffdfc4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA512:f630e7a7e53a21b7ccb4d3e7b37616b89aeceba916677c8e3032830411d77a14c2d74dcf594cd193b1acc11f52595072e28316dc44300e54083d5d7b314a38da
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA512:a32a7146598f9183179ad15603181d1066e806d01f7c5f215d5405ad8618c06a265d05fff3b4a6cc49c50a577d93d6b920e85f6a581786b3db7389f52a4638e2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu3.1.debian.tar.xz' libseccomp_2.5.5-1ubuntu3.1.debian.tar.xz 24484 SHA512:89e68d82dd1985352e7ff0057fb1682c6b5beb0857c7329034d696bdc81e880f395309f065c23ff1f92ac7ad1a3c5ca46fe264309ce2be7dcbd0367d9e39cbde
```

### `dpkg` source package: `libselinux=3.5-2ubuntu2.1`

Binary Packages:

- `libselinux1:amd64=3.5-2ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-2ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu2.1.dsc' libselinux_3.5-2ubuntu2.1.dsc 3098 SHA512:bcf60f1ab7020ca57ad20b8b4dbd3d6c0b0f97a768c1c0c047c562a2b50ed8c73ffa13c002729ef7aba353768c03e72749d29fc9882982a531fda950b3a17de8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA512:4e13261a5821018a5f3cdce676f180bb62e5bc225981ca8a498ece0d1c88d9ba8eaa0ce4099dd0849309a8a7c5a9a0953df841a9922f2c284e5a109e5d937ba7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA512:ba486d29c92801a02f75213ef5bcc4a0c4a87afe9dfa797aa9bb495ded40f21e37b22d6ea114c0e480d669b090d1116e8b9cac9fa9ea29678d3647bc58d8bb29
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu2.1.debian.tar.xz' libselinux_3.5-2ubuntu2.1.debian.tar.xz 38112 SHA512:0e09406649d1a80e9c96b7791a2e4fbf6b5818b21d3ffa40dd2191c92be737cd506cd21ea375f25f2582e3a9bfc75d157816e33473b2ad676dcb3d346743e9a4
```

### `dpkg` source package: `libsemanage=3.5-1build5`

Binary Packages:

- `libsemanage-common=3.5-1build5`
- `libsemanage2:amd64=3.5-1build5`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsepol=3.5-2build1`

Binary Packages:

- `libsepol2:amd64=3.5-2build1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsm=2:1.2.3-1build3`

Binary Packages:

- `libsm-dev:amd64=2:1.2.3-1build3`
- `libsm6:amd64=2:1.2.3-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsodium=1.0.18-1ubuntu0.24.04.1`

Binary Packages:

- `libsodium23:amd64=1.0.18-1ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libsodium23/copyright`)

- `BSD-2-clause`
- `CC0`
- `CC0-1.0`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libsodium=1.0.18-1ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsodium/libsodium_1.0.18-1ubuntu0.24.04.1.dsc' libsodium_1.0.18-1ubuntu0.24.04.1.dsc 2052 SHA512:8474b64b17a9ee559542df02a06a3bf045149f3ac947ed6397454ea6fd61633682128d8b7496d78ce4b073ee93d41158dbe3ca0c7c8cc0a96a039507e0fa64e4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsodium/libsodium_1.0.18.orig.tar.gz' libsodium_1.0.18.orig.tar.gz 1619527 SHA512:727fe50a5fb1df86ec5d807770f408a52609cbeb8510b4f4183b2a35a537905719bdb6348afcb103ff00ce946a8094ac9559b6e3e5b2ccc2a2d0c08f75577eeb
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsodium/libsodium_1.0.18-1ubuntu0.24.04.1.debian.tar.xz' libsodium_1.0.18-1ubuntu0.24.04.1.debian.tar.xz 8508 SHA512:01aac286eb0df943d6c8d1a86396aee009cfa9e2bf9c4266634a7853d015d5af3de1da9b836bf96a17290df83c5da43e808271cdeac421ea41b9bc59380ac9ec
```

### `dpkg` source package: `libsoxr=0.1.3-4build3`

Binary Packages:

- `libsoxr0:amd64=0.1.3-4build3`

Licenses: (parsed from: `/usr/share/doc/libsoxr0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`
- `Spherepack`
- `permissive1`
- `permissive2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libssh=0.10.6-2ubuntu0.2`

Binary Packages:

- `libssh-4:amd64=0.10.6-2ubuntu0.2`
- `libssh-gcrypt-4:amd64=0.10.6-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`, `/usr/share/doc/libssh-gcrypt-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.10.6-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.2.dsc' libssh_0.10.6-2ubuntu0.2.dsc 2723 SHA512:0ce4ad1a7c238fa3dca8523f49833309c47aa55535c7d438d0c7d6a985e5346d2071d791c1847cbeea76502ca73276e1235dda81f075fc3e0ce90240656065f0
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz' libssh_0.10.6.orig.tar.xz 561036 SHA512:40c62d63c44e882999b71552c237d73fc7364313bd00b15a211a34aeff1b73693da441d2c8d4e40108d00fb7480ec7c5b6d472f9c0784b2359a179632ab0d6c1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz.asc' libssh_0.10.6.orig.tar.xz.asc 833 SHA512:214d7920bebc80a8e6838c64ed06e070709a96fabfb4fff657b55f9588bc0e1612887fe887d23de73ad3540f3bb85288e62eb6a11ccd4bc80afbd44d34ba70d4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.2.debian.tar.xz' libssh_0.10.6-2ubuntu0.2.debian.tar.xz 47820 SHA512:92e9d5c401b22570cabac5c80c984b809d8fbcc537b464b7e5ec69eae254046cb56bb1d5029cc7ac11c0e8010f5501bf8495261f1022770eded064e4f6bb637c
```

### `dpkg` source package: `libtasn1-6=4.19.0-3ubuntu0.24.04.2`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3ubuntu0.24.04.2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.19.0-3ubuntu0.24.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc' libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc 2801 SHA512:1f6d7b3a05b8f9b804d00fe726dbcd0ae0ed60d38483cecb45c8ddc6607a7cf11e1f7ea8e1001afc56b5c74be98893f063aa2dfd203df3f4c25fe211ca229692
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA512:287f5eddfb5e21762d9f14d11997e56b953b980b2b03a97ed4cd6d37909bda1ed7d2cdff9da5d270a21d863ab7e54be6b85c05f1075ac5d8f0198997cf335ef4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA512:e0417625f8df22c6421914bf2d4f19d7f27260c24c04f50e59669681f326debe06ddef9dc5a2e20fda50feb30bbbf3f41597e64961257304ec2c407aa76d107e
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz' libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz 25112 SHA512:b64b55ad6138f12b1191039c1db36cba1b6add98bab5c399b338517284b4091ede2ce7a2e71f46f97c50584fb670bc2dd295caab108973aed0552353c1cb3158
```

### `dpkg` source package: `libthai=0.1.29-2build1`

Binary Packages:

- `libthai-data=0.1.29-2build1`
- `libthai0:amd64=0.1.29-2build1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libtheora=1.1.1+dfsg.1-16.1build3`

Binary Packages:

- `libtheora-dev:amd64=1.1.1+dfsg.1-16.1build3`
- `libtheora0:amd64=1.1.1+dfsg.1-16.1build3`

Licenses: (parsed from: `/usr/share/doc/libtheora-dev/copyright`, `/usr/share/doc/libtheora0/copyright`)

- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libtirpc=1.3.4+ds-1.1build1`

Binary Packages:

- `libtirpc-common=1.3.4+ds-1.1build1`
- `libtirpc-dev:amd64=1.3.4+ds-1.1build1`
- `libtirpc3t64:amd64=1.3.4+ds-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libtirpc-common/copyright`, `/usr/share/doc/libtirpc-dev/copyright`, `/usr/share/doc/libtirpc3t64/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-4-Clause`
- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PERMISSIVE`
- `__AUTO_PERMISSIVE__`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libtool=2.4.7-7build1`

Binary Packages:

- `libltdl-dev:amd64=2.4.7-7build1`
- `libltdl7:amd64=2.4.7-7build1`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libudfread=1.1.2-1build1`

Binary Packages:

- `libudfread0:amd64=1.1.2-1build1`

Licenses: (parsed from: `/usr/share/doc/libudfread0/copyright`)

- `GPL-2`
- `GPL-2+ with autoconf-macro exception`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libunistring=1.1-2build1.1`

Binary Packages:

- `libunistring5:amd64=1.1-2build1.1`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-NIV-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.1-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2build1.1.dsc' libunistring_1.1-2build1.1.dsc 2292 SHA512:94e0463201534ac0db023f29ffde1c63b479ead150a59a0bd27b9e0fc425976e3eb057657bf4f9e0c572816dc5219d8df9cb5ec872bc433d4166a888f8ab69c8
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz' libunistring_1.1.orig.tar.xz 2397676 SHA512:01a4267bbd301ea5c389b17ee918ae5b7d645da8b2c6c6f0f004ff2dead9f8e50cda2c6047358890a5fceadc8820ffc5154879193b9bb8970f3fb1fea1f411d6
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz.asc' libunistring_1.1.orig.tar.xz.asc 833 SHA512:f94912a52df8d7863de271315c8b5a7e1e0ab7aabb66273fcdb81c48aa0b23360b80fdb1df9f768aede47dd5a92a280868db41147139dfabecbc82511715db4d
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2build1.1.debian.tar.xz' libunistring_1.1-2build1.1.debian.tar.xz 14188 SHA512:c8c03af60f056eeb8d5b16ca5e6df6029506266f383d1f5ca61be8ae6a64ad50a918b5c818db1f1d88fc9086169290df1e25749c9aacb0054ea308c1f92ecdb8
```

### `dpkg` source package: `libunwind=1.6.2-3build1.1`

Binary Packages:

- `libunwind8:amd64=1.6.2-3build1.1`

Licenses: (parsed from: `/usr/share/doc/libunwind8/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libunwind=1.6.2-3build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.6.2-3build1.1.dsc' libunwind_1.6.2-3build1.1.dsc 2919 SHA512:50ad24ece273cf93e5dd3d25e1eb665334d83307bed1e896f3ed14c104d3926ad3f5c161c13533cd68b9286722a1385852c6f3b37e3995f0d4a064ba30e0ae29
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.6.2.orig.tar.gz' libunwind_1.6.2.orig.tar.gz 901392 SHA512:1d17dfb14f99a894a6cda256caf9ec481c14068aaf8f3a85fa3befa7c7cca7fca0f544a91a3a7c2f2fc55bab19b06a67ca79f55ac9081151d94478c7f611f8f7
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.6.2.orig.tar.gz.asc' libunwind_1.6.2.orig.tar.gz.asc 659 SHA512:53aa6a89b471856d4f62976476c81c576bbf8e27f00b9229fd2722424c1888f13e2f6745240e085a4e36a8043f0b14a633bfddf6c61603d8723db3faf9dad1ac
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.6.2-3build1.1.debian.tar.xz' libunwind_1.6.2-3build1.1.debian.tar.xz 16904 SHA512:ef73541340d65ce1adb7ca763fe8e9635b80f2e84386310d683968ec8d8d32591b76998bfb30bbd7c79ff493346171dd1619409cfe90565d25eed5bf92869ca8
```

### `dpkg` source package: `liburcu=0.14.0-3.1build1`

Binary Packages:

- `liburcu-dev:amd64=0.14.0-3.1build1`
- `liburcu8t64:amd64=0.14.0-3.1build1`

Licenses: (parsed from: `/usr/share/doc/liburcu-dev/copyright`, `/usr/share/doc/liburcu8t64/copyright`)

- `BSD-2-clause`
- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2 with Autoconf-data exception`
- `GPL-2+`
- `GPL-2+ with Autoconf-2.0~Archive exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-2.0~Archive exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT-MINIMAL`
- `MIT~Boehm`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libusb-1.0=2:1.0.27-1`

Binary Packages:

- `libusb-1.0-0:amd64=2:1.0.27-1`
- `libusb-1.0-0-dev:amd64=2:1.0.27-1`

Licenses: (parsed from: `/usr/share/doc/libusb-1.0-0/copyright`, `/usr/share/doc/libusb-1.0-0-dev/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libusb-1.0/2:1.0.27-1/


### `dpkg` source package: `libuv1=1.48.0-1.1build1`

Binary Packages:

- `libuv1t64:amd64=1.48.0-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libuv1t64/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `CC-BY-4.0`
- `Expat`
- `GPL3+ with autoconf exception`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libva=2.20.0-2build1`

Binary Packages:

- `libva-drm2:amd64=2.20.0-2build1`
- `libva-x11-2:amd64=2.20.0-2build1`
- `libva2:amd64=2.20.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libva-drm2/copyright`, `/usr/share/doc/libva-x11-2/copyright`, `/usr/share/doc/libva2/copyright`)

- `Expat`
- `Expat-advertising`
- `GPL-2`
- `GPL-2+`
- `other`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libvdpau=1.5-2build1`

Binary Packages:

- `libvdpau1:amd64=1.5-2build1`

Licenses: (parsed from: `/usr/share/doc/libvdpau1/copyright`)

- `Expat`
- `other`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libvorbis=1.3.7-1build3`

Binary Packages:

- `libvorbis0a:amd64=1.3.7-1build3`
- `libvorbisenc2:amd64=1.3.7-1build3`
- `libvorbisfile3:amd64=1.3.7-1build3`

Licenses: (parsed from: `/usr/share/doc/libvorbis0a/copyright`, `/usr/share/doc/libvorbisenc2/copyright`, `/usr/share/doc/libvorbisfile3/copyright`)

- `BSD-3-Clause`
- `RFC-special`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libvpx=1.14.0-1ubuntu2.2`

Binary Packages:

- `libvpx9:amd64=1.14.0-1ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/libvpx9/copyright`)

- `BSD-3-Clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libvpx=1.14.0-1ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvpx/libvpx_1.14.0-1ubuntu2.2.dsc' libvpx_1.14.0-1ubuntu2.2.dsc 2415 SHA512:bc910e527e33645c3ed5b2ea4203a96918a05f1162f62be46e1b7aa88913dd55fb2634f7fb0a296a92a6c20536dccde0e0562a9792e07850225eb5d0d3256b65
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvpx/libvpx_1.14.0.orig.tar.xz' libvpx_1.14.0.orig.tar.xz 4374856 SHA512:fcf13ac4a4dde93e691949146ee3a7c75e39076c3c239293c10911bb67aee31eea78c5fadcb4b5f01676e1298d859fae1dceafeea429c1fe2a315797d39b1a0a
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvpx/libvpx_1.14.0-1ubuntu2.2.debian.tar.xz' libvpx_1.14.0-1ubuntu2.2.debian.tar.xz 17980 SHA512:67c5ea569c016295c6d98cc0c968e6e66c8e30503bafa4ad4e496bffb81f080437259cc82059086719ff54b9340b3369c1ce7331ca82175bd173c16d0bb1deaf
```

### `dpkg` source package: `libwacom=2.10.0-2`

Binary Packages:

- `libwacom-common=2.10.0-2`
- `libwacom9:amd64=2.10.0-2`

Licenses: (parsed from: `/usr/share/doc/libwacom-common/copyright`, `/usr/share/doc/libwacom9/copyright`)

- `MIT`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libwacom/2.10.0-2/


### `dpkg` source package: `libwebp=1.3.2-0.4build3`

Binary Packages:

- `libsharpyuv-dev:amd64=1.3.2-0.4build3`
- `libsharpyuv0:amd64=1.3.2-0.4build3`
- `libwebp-dev:amd64=1.3.2-0.4build3`
- `libwebp7:amd64=1.3.2-0.4build3`
- `libwebpdecoder3:amd64=1.3.2-0.4build3`
- `libwebpdemux2:amd64=1.3.2-0.4build3`
- `libwebpmux3:amd64=1.3.2-0.4build3`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libx11=2:1.8.7-1build1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1build1`
- `libx11-data=2:1.8.7-1build1`
- `libx11-dev:amd64=2:1.8.7-1build1`
- `libx11-xcb1:amd64=2:1.8.7-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxau=1:1.0.9-1build6`

Binary Packages:

- `libxau-dev:amd64=1:1.0.9-1build6`
- `libxau6:amd64=1:1.0.9-1build6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxaw=2:1.0.14-1build2`

Binary Packages:

- `libxaw7:amd64=2:1.0.14-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxcb=1.15-1ubuntu2`

Binary Packages:

- `libxcb-dri3-0:amd64=1.15-1ubuntu2`
- `libxcb-glx0:amd64=1.15-1ubuntu2`
- `libxcb-present0:amd64=1.15-1ubuntu2`
- `libxcb-randr0:amd64=1.15-1ubuntu2`
- `libxcb-render0:amd64=1.15-1ubuntu2`
- `libxcb-shape0:amd64=1.15-1ubuntu2`
- `libxcb-shm0:amd64=1.15-1ubuntu2`
- `libxcb-sync1:amd64=1.15-1ubuntu2`
- `libxcb-xfixes0:amd64=1.15-1ubuntu2`
- `libxcb-xinerama0:amd64=1.15-1ubuntu2`
- `libxcb-xinput0:amd64=1.15-1ubuntu2`
- `libxcb-xkb1:amd64=1.15-1ubuntu2`
- `libxcb1:amd64=1.15-1ubuntu2`
- `libxcb1-dev:amd64=1.15-1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxcomposite=1:0.4.5-1build3`

Binary Packages:

- `libxcomposite1:amd64=1:0.4.5-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxcrypt=1:4.4.36-4build1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-4build1`
- `libcrypt1:amd64=1:4.4.36-4build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxcursor=1:1.2.1-1build1`

Binary Packages:

- `libxcursor1:amd64=1:1.2.1-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxdamage=1:1.1.6-1build1`

Binary Packages:

- `libxdamage1:amd64=1:1.1.6-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu6`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.3-0ubuntu6`
- `libxdmcp6:amd64=1:1.1.3-0ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxext=2:1.3.4-1build2`

Binary Packages:

- `libxext-dev:amd64=2:1.3.4-1build2`
- `libxext6:amd64=2:1.3.4-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxfixes=1:6.0.0-2build1`

Binary Packages:

- `libxfixes3:amd64=1:6.0.0-2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxi=2:1.8.1-1build1`

Binary Packages:

- `libxi6:amd64=2:1.8.1-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxinerama=2:1.1.4-3build1`

Binary Packages:

- `libxinerama1:amd64=2:1.1.4-3build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxkbcommon=1.6.0-1build1`

Binary Packages:

- `libxkbcommon-x11-0:amd64=1.6.0-1build1`
- `libxkbcommon0:amd64=1.6.0-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxml2=2.9.14+dfsg-1.3ubuntu3.6`

Binary Packages:

- `libxml2:amd64=2.9.14+dfsg-1.3ubuntu3.6`
- `libxml2-dev:amd64=2.9.14+dfsg-1.3ubuntu3.6`
- `libxml2-utils=2.9.14+dfsg-1.3ubuntu3.6`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`, `/usr/share/doc/libxml2-utils/copyright`)

- `ISC`
- `MIT-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxmu=2:1.1.3-3build2`

Binary Packages:

- `libxmu6:amd64=2:1.1.3-3build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxpm=1:3.5.17-1build2`

Binary Packages:

- `libxpm4:amd64=1:3.5.17-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxrandr=2:1.5.2-2build1`

Binary Packages:

- `libxrandr2:amd64=2:1.5.2-2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxrender=1:0.9.10-1.1build1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.10-1.1build1`
- `libxrender1:amd64=1:0.9.10-1.1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxshmfence=1.3-1build5`

Binary Packages:

- `libxshmfence1:amd64=1.3-1build5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxslt=1.1.39-0exp1ubuntu0.24.04.3`

Binary Packages:

- `libxslt1.1:amd64=1.1.39-0exp1ubuntu0.24.04.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.39-0exp1ubuntu0.24.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc' libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc 2352 SHA512:7709b2e2900154e58c792fa288a99ab1b90863e7e02400e510507b78aeb7b1e0e302995146e247c371fe8311cfe42d4861e8d6c176b045dc118d65902dbf61ff
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39.orig.tar.xz' libxslt_1.1.39.orig.tar.xz 1578216 SHA512:c0c99dc63f8b2acb6cc3ad7ad684ffa2a427ee8d1740495cbf8a7c9b9c8679f96351b4b676c73ccc191014db4cb4ab42b9a0070f6295565f39dbc665c5c16f89
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz' libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz 24380 SHA512:e9ea90695741f2a81ccf3ca36c1ffd3806ce158242a77e29f0282bf4b124d5dcc0f8b60bd870c56d168a71f61f43b667720c37741a23dd9a4280b0c22063c69f
```

### `dpkg` source package: `libxss=1:1.2.3-1build3`

Binary Packages:

- `libxss-dev:amd64=1:1.2.3-1build3`
- `libxss1:amd64=1:1.2.3-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxt=1:1.2.1-1.2build1`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.2build1`
- `libxt6t64:amd64=1:1.2.1-1.2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxtst=2:1.2.3-1.1build1`

Binary Packages:

- `libxtst6:amd64=2:1.2.3-1.1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxxf86vm=1:1.1.4-1build4`

Binary Packages:

- `libxxf86vm1:amd64=1:1.1.4-1build4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libyaml=0.2.5-1build1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-1build1`
- `libyaml-dev:amd64=0.2.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libzstd=1.5.5+dfsg2-2build1.1`

Binary Packages:

- `libzstd-dev:amd64=1.5.5+dfsg2-2build1.1`
- `libzstd1:amd64=1.5.5+dfsg2-2build1.1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.5+dfsg2-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2build1.1.dsc' libzstd_1.5.5+dfsg2-2build1.1.dsc 2485 SHA512:58915fc819994cbf1e5db663bcdf266ebf0d9967a25e549645be22c27fe7390a5cc000af3a40494895c0102b95c41caf54cb0ed1b3331e9921bfae181a9603b9
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2.orig.tar.xz' libzstd_1.5.5+dfsg2.orig.tar.xz 1784164 SHA512:0b24cf71636b36ae17f617f0a4a2e1253ba6a7bfcd8b6f4717cc59310e92d23bde0945f885fa80622d84961b85fa6ba74e3436ab1badc687e8a13ac428a71b8d
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2build1.1.debian.tar.xz' libzstd_1.5.5+dfsg2-2build1.1.debian.tar.xz 21288 SHA512:8d57d913e68ec6722378c7d04b1513ac565b8bdda527f615aaa13f3270c423c1f1ee9575b50330c827de64dc66b25a60cbfe5b53d197346a0cff27d5fb735e40
```

### `dpkg` source package: `linux=6.8.0-90.91`

Binary Packages:

- `linux-libc-dev:amd64=6.8.0-90.91`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=6.8.0-90.91
'http://security.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.8.0-90.91.dsc' linux_6.8.0-90.91.dsc 9362 SHA512:42abcfe6580eb6570fd83c3f819d27acfc94c00b40ddea17d1e7ac91b2b45b7f006bf9fa8b1acfe4c911040fb8ba878b3afb73d05494cd06cc44279b61b17890
'http://security.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.8.0.orig.tar.gz' linux_6.8.0.orig.tar.gz 230060117 SHA512:296f93b24e1f7d116377ba8ccd0d8a977e82248ef469586e52db496190092572e90bc05704760424d215261fcbf62e7240819dffd0976b0f6407361e1eac380c
'http://security.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.8.0-90.91.diff.gz' linux_6.8.0-90.91.diff.gz 6075998 SHA512:e63209e51a8b6c9d38b3177e85a1a22f5c67eb9ab6eba8830caae022c155abee8ce44fb570b8ea87c3b8166f5d5f508928322932f4273356a46ab822eda98497
```

### `dpkg` source package: `llvm-toolchain-15=1:15.0.7-14build3`

Binary Packages:

- `libclang1-15t64=1:15.0.7-14build3`
- `libllvm15t64:amd64=1:15.0.7-14build3`

Licenses: (parsed from: `/usr/share/doc/libclang1-15t64/copyright`, `/usr/share/doc/libllvm15t64/copyright`)

- `APACHE-2-LLVM-EXCEPTIONS`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-clause`
- `MIT`
- `Python`
- `solar-public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `llvm-toolchain-17=1:17.0.6-9ubuntu1`

Binary Packages:

- `libllvm17t64:amd64=1:17.0.6-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libllvm17t64/copyright`)

- `APACHE-2-LLVM-EXCEPTIONS`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-clause`
- `MIT`
- `Python`
- `solar-public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `llvm-toolchain-20=1:20.1.2-0ubuntu1~24.04.2`

Binary Packages:

- `libllvm20:amd64=1:20.1.2-0ubuntu1~24.04.2`

Licenses: (parsed from: `/usr/share/doc/libllvm20/copyright`)

- `APACHE-2-LLVM-EXCEPTIONS`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-clause`
- `MIT`
- `Python`
- `solar-public-domain`

Source:

```console
$ apt-get source -qq --print-uris llvm-toolchain-20=1:20.1.2-0ubuntu1~24.04.2
'http://archive.ubuntu.com/ubuntu/pool/universe/l/llvm-toolchain-20/llvm-toolchain-20_20.1.2-0ubuntu1%7e24.04.2.dsc' llvm-toolchain-20_20.1.2-0ubuntu1~24.04.2.dsc 8545 SHA512:8427c7abf7a9b2de976244288b1bb073d85ca004eca5747ee98c92dc3d48167edb608d43afdd5df8f3eef5addbe188e7e9e6733705353a7ed943f4f22b13e5e1
'http://archive.ubuntu.com/ubuntu/pool/universe/l/llvm-toolchain-20/llvm-toolchain-20_20.1.2.orig-integration-test-suite.tar.gz' llvm-toolchain-20_20.1.2.orig-integration-test-suite.tar.gz 195387 SHA512:96adfec213099ae1e8f2f564c4d6a5025d957b951a29e4e87fa90fa57bd03e4831465bd39cd570e03430d96099c100fa7f43c20e3b01cd1b806b25e3b06495d5
'http://archive.ubuntu.com/ubuntu/pool/universe/l/llvm-toolchain-20/llvm-toolchain-20_20.1.2.orig.tar.gz' llvm-toolchain-20_20.1.2.orig.tar.gz 226701433 SHA512:0550571718623a16d85b58222bc61bd6a47ab7a8d9183e58d3b66f33424ed0bfa45c75687312b43515a00815e955f64328db214f4ea4656dcfd652cea949467e
'http://archive.ubuntu.com/ubuntu/pool/universe/l/llvm-toolchain-20/llvm-toolchain-20_20.1.2-0ubuntu1%7e24.04.2.debian.tar.xz' llvm-toolchain-20_20.1.2-0ubuntu1~24.04.2.debian.tar.xz 155044 SHA512:ddcfe7f271844d8bb38042eaa422eab19bc8d34c3e06e5f58de2e4a34fde213c744843654194a6cf9451399494b33e12f110398a62bbea4f280a7ba5490e2d1e
```

### `dpkg` source package: `lm-sensors=1:3.6.0-9build1`

Binary Packages:

- `libsensors-config=1:3.6.0-9build1`
- `libsensors5:amd64=1:3.6.0-9build1`

Licenses: (parsed from: `/usr/share/doc/libsensors-config/copyright`, `/usr/share/doc/libsensors5/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lsb-release-minimal=12.0-2`

Binary Packages:

- `lsb-release=12.0-2`

Licenses: (parsed from: `/usr/share/doc/lsb-release/copyright`)

- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lsb-release-minimal/12.0-2/


### `dpkg` source package: `lto-disabled-list=47`

Binary Packages:

- `lto-disabled-list=47`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ltt-control=2.13.11-2.1build4`

Binary Packages:

- `liblttng-ctl0t64:amd64=2.13.11-2.1build4`
- `lttng-tools=2.13.11-2.1build4`

Licenses: (parsed from: `/usr/share/doc/liblttng-ctl0t64/copyright`, `/usr/share/doc/lttng-tools/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lvm2=2.03.16-3ubuntu3.2`

Binary Packages:

- `libdevmapper1.02.1:amd64=2:1.02.185-3ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libdevmapper1.02.1/copyright`)

- `BSD-2-Clause`
- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris lvm2=2.03.16-3ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lvm2/lvm2_2.03.16-3ubuntu3.2.dsc' lvm2_2.03.16-3ubuntu3.2.dsc 3243 SHA512:5c92cbfa2f96bb8c49fcf909dcbc804e6343b46d7e489592a03fb87b96cde31a595b45c2396db7fdd27ad6f6a37bda4851ed1cf5f915bef50fafe4f46486a7f7
'http://archive.ubuntu.com/ubuntu/pool/main/l/lvm2/lvm2_2.03.16.orig.tar.xz' lvm2_2.03.16.orig.tar.xz 1790340 SHA512:9c8691c9d4b8ca843cd94520ac6e7e4b7671c45a8d267d86e3f515f007c5e82dca85d670decb7a888919af34eef782f390b51c2455ef92cfb41451d2229d5b31
'http://archive.ubuntu.com/ubuntu/pool/main/l/lvm2/lvm2_2.03.16-3ubuntu3.2.debian.tar.xz' lvm2_2.03.16-3ubuntu3.2.debian.tar.xz 46896 SHA512:0348161e5efa2e04b076bff267a5e5f43b6352be8d9c74f684fd642e9e021f3291b5900eaf3fd03a18e3d1b3c0f608dc800311edba3cd52a4a7eb83702829416
```

### `dpkg` source package: `lxml=5.2.1-1`

Binary Packages:

- `python3-lxml:amd64=5.2.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-lxml/copyright`)

- `GPL`
- `GPL2`
- `later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lxml/5.2.1-1/


### `dpkg` source package: `lz4=1.9.4-1build1.1`

Binary Packages:

- `liblz4-1:amd64=1.9.4-1build1.1`
- `liblz4-dev:amd64=1.9.4-1build1.1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`, `/usr/share/doc/liblz4-dev/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1build1.1.dsc' lz4_1.9.4-1build1.1.dsc 2061 SHA512:92ed13e86d10857d6a9d0398ce200b54b6aa66d45f9f72bda5fddec53fb00291d48e6efb932085a57361c364c551a8d0e2dfe12331abcafc92b7f61884a239cd
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA512:043a9acb2417624019d73db140d83b80f1d7c43a6fd5be839193d68df8fd0b3f610d7ed4d628c2a9184f7cde9a0fd1ba9d075d8251298e3eb4b3a77f52736684
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1build1.1.debian.tar.xz' lz4_1.9.4-1build1.1.debian.tar.xz 8356 SHA512:deb05c99d5ba5702997608b9c5fbe72b1a383bce253e0e25c409746c44d98245c559c0744767a18d32bdb5303a575c18f5c784fe4ad0b03565a13450c86c74f1
```

### `dpkg` source package: `m4=1.4.19-4build1`

Binary Packages:

- `m4=1.4.19-4build1`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `make-dfsg=4.3-4.1build2`

Binary Packages:

- `make=4.3-4.1build2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mawk=1.3.4.20240123-1build1`

Binary Packages:

- `mawk=1.3.4.20240123-1build1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mbedtls=2.28.8-1`

Binary Packages:

- `libmbedcrypto7t64:amd64=2.28.8-1`

Licenses: (parsed from: `/usr/share/doc/libmbedcrypto7t64/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mbedtls/2.28.8-1/


### `dpkg` source package: `md4c=0.4.8-1build1`

Binary Packages:

- `libmd4c0:amd64=0.4.8-1build1`

Licenses: (parsed from: `/usr/share/doc/libmd4c0/copyright`)

- `BSD-2-clause`
- `CC-BY-SA-4.0`
- `Expat`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/media-types/10.1.0/


### `dpkg` source package: `mesa=25.0.7-0ubuntu0.24.04.2`

Binary Packages:

- `libegl-mesa0:amd64=25.0.7-0ubuntu0.24.04.2`
- `libgbm1:amd64=25.0.7-0ubuntu0.24.04.2`
- `libgl1-mesa-dev:amd64=25.0.7-0ubuntu0.24.04.2`
- `libgl1-mesa-dri:amd64=25.0.7-0ubuntu0.24.04.2`
- `libglx-mesa0:amd64=25.0.7-0ubuntu0.24.04.2`
- `mesa-libgallium:amd64=25.0.7-0ubuntu0.24.04.2`

Licenses: (parsed from: `/usr/share/doc/libegl-mesa0/copyright`, `/usr/share/doc/libgbm1/copyright`, `/usr/share/doc/libgl1-mesa-dev/copyright`, `/usr/share/doc/libgl1-mesa-dri/copyright`, `/usr/share/doc/libglx-mesa0/copyright`, `/usr/share/doc/mesa-libgallium/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-google`
- `BSL`
- `GPL`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `Khronos`
- `MIT`
- `MLAA`
- `SGI`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `more-itertools=10.2.0-1`

Binary Packages:

- `python3-more-itertools=10.2.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-more-itertools/copyright`)

- `MIT-style`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/more-itertools/10.2.0-1/


### `dpkg` source package: `mpclib3=1.3.1-1build1.1`

Binary Packages:

- `libmpc3:amd64=1.3.1-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build1.1.dsc' mpclib3_1.3.1-1build1.1.dsc 1963 SHA512:08fca205a53d76e0fe8f58ee1e882773cf84bb3822af7ebba10588db4fc6c996bd15d60f76f39d79133ae905c279286a389aed699ca58234a3dfe242b6ac7d0e
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA512:4bab4ef6076f8c5dfdc99d810b51108ced61ea2942ba0c1c932d624360a5473df20d32b300fc76f2ba4aa2a97e1f275c9fd494a1ba9f07c4cb2ad7ceaeb1ae97
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build1.1.debian.tar.xz' mpclib3_1.3.1-1build1.1.debian.tar.xz 4844 SHA512:7f118d341a37e2ea18a989a4dfa64b49fce745075faed72b9793b25b1cca3b3b029f27114f2597734c24c7723226425fff1c5085b988ef1e68dd4b69e609857e
```

### `dpkg` source package: `mpfr4=4.2.1-1build1.1`

Binary Packages:

- `libmpfr6:amd64=4.2.1-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.1-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build1.1.dsc' mpfr4_4.2.1-1build1.1.dsc 2045 SHA512:a7f344a44db1cc40dd5c175b6d7b999e6bf5b3f8f1155c21237bb2266fa2bc06f45b0083cc46033b0de354b2cfe54aa84b45ef64319d353802ac3557796cb698
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA512:bc68c0d755d5446403644833ecbb07e37360beca45f474297b5d5c40926df1efc3e2067eecffdf253f946288bcca39ca89b0613f545d46a9e767d1d4cf358475
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build1.1.debian.tar.xz' mpfr4_4.2.1-1build1.1.debian.tar.xz 12760 SHA512:5ad5f1f5495c9695b3b882cc4e9aaa172744177e6184a0431a6add6c4def3c0c948ee6b691ff36eb1a53788387af5ae62c37ec9998d9f7c8fc158710b219a8f6
```

### `dpkg` source package: `mpg123=1.32.5-1ubuntu1.1`

Binary Packages:

- `libmpg123-0t64:amd64=1.32.5-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libmpg123-0t64/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris mpg123=1.32.5-1ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpg123/mpg123_1.32.5-1ubuntu1.1.dsc' mpg123_1.32.5-1ubuntu1.1.dsc 2479 SHA512:610beb67cedb6d44e6c3912a43a2b3e924c3ef023acced8530624e1cd6550fe5c51148fbebc37f2aadaac806becee5281da0bbd6ebfeb1b02e8b00e57615773e
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpg123/mpg123_1.32.5.orig.tar.xz' mpg123_1.32.5.orig.tar.xz 927136 SHA512:145ededa22ccc9f2ab449014eb4bc64c5fcd33ac7f0d2958762c67abf0a021119789fc9bafade7fbf6a083a5afb602e40de7928bcb4cd7002e6c5df1fc5d2256
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpg123/mpg123_1.32.5-1ubuntu1.1.debian.tar.xz' mpg123_1.32.5-1ubuntu1.1.debian.tar.xz 35592 SHA512:b2578627cac7b6e605d228384c6780bb06f811a1dc0e91cd1540f7c89a146333f6d10e0c6c2ca7869dc3529cb8bc4763b92505e1776b87ebd41feeab64b534b5
```

### `dpkg` source package: `mpi-defaults=1.15build1`

Binary Packages:

- `mpi-default-bin=1.15build1`
- `mpi-default-dev=1.15build1`

Licenses: (parsed from: `/usr/share/doc/mpi-default-bin/copyright`, `/usr/share/doc/mpi-default-dev/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mpi4py=3.1.5-5ubuntu2`

Binary Packages:

- `python3-mpi4py=3.1.5-5ubuntu2`

Licenses: (parsed from: `/usr/share/doc/python3-mpi4py/copyright`)

- `BSD-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mtdev=1.1.6-1.1build1`

Binary Packages:

- `libmtdev1t64:amd64=1.1.6-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libmtdev1t64/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `munge=0.5.15-4build1`

Binary Packages:

- `libmunge2:amd64=0.5.15-4build1`

Licenses: (parsed from: `/usr/share/doc/libmunge2/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+-and-LGPL-3+`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mysql-8.0=8.0.44-0ubuntu0.24.04.2`

Binary Packages:

- `libmysqlclient-dev=8.0.44-0ubuntu0.24.04.2`
- `libmysqlclient21:amd64=8.0.44-0ubuntu0.24.04.2`

Licenses: (parsed from: `/usr/share/doc/libmysqlclient-dev/copyright`, `/usr/share/doc/libmysqlclient21/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-like`
- `Boost-1.0`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `public-domain`
- `zlib/libpng`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mysql-defaults=1.1.0build1`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.0build1`
- `mysql-common=5.8+1.1.0build1`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ncurses=6.4+20240113-1ubuntu2`

Binary Packages:

- `libncursesw6:amd64=6.4+20240113-1ubuntu2`
- `libtinfo6:amd64=6.4+20240113-1ubuntu2`
- `ncurses-base=6.4+20240113-1ubuntu2`
- `ncurses-bin=6.4+20240113-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `netbase=6.4`

Binary Packages:

- `netbase=6.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/netbase/6.4/


### `dpkg` source package: `netcdf=1:4.9.2-5ubuntu4`

Binary Packages:

- `libnetcdf-dev=1:4.9.2-5ubuntu4`
- `libnetcdf19t64:amd64=1:4.9.2-5ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libnetcdf-dev/copyright`, `/usr/share/doc/libnetcdf19t64/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `CC-BY-4.0`
- `Expat`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `HDF5`
- `NetCDF`
- `Unicode-data`
- `Zlib`
- `ncxml`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nettle=3.9.1-2.2build1.1`

Binary Packages:

- `libhogweed6t64:amd64=3.9.1-2.2build1.1`
- `libnettle8t64:amd64=3.9.1-2.2build1.1`

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
$ apt-get source -qq --print-uris nettle=3.9.1-2.2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.2build1.1.dsc' nettle_3.9.1-2.2build1.1.dsc 2325 SHA512:4673af3a6485b78bb8bd7fff908aaf86fabe2220f26ab8acee89ae6b1fa0d2ca12c529c677d7b9b5709068d3c0fbf38d88d2eddacf55aabe01e10d6e8451c832
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz' nettle_3.9.1.orig.tar.gz 2396741 SHA512:5939c4b43cf9ff6c6272245b85f123c81f8f4e37089fa4f39a00a570016d837f6e706a33226e4bbfc531b02a55b2756ff312461225ed88de338a73069e031ced
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz.asc' nettle_3.9.1.orig.tar.gz.asc 573 SHA512:2ca8ab90c2a437c587987492be2a4c71658256020af725b48ee8f25771b7af28a9c1a8e300826dce58c4b691545d450ec44e668187daaa351a63a77eca4cedcb
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.2build1.1.debian.tar.xz' nettle_3.9.1-2.2build1.1.debian.tar.xz 24848 SHA512:6d53ab1bd7e520c8ed10b36db6a5c584dd034ace0ef71f88445b74e566ffd35b7cc2d33267f51ce391c5833ff978d93eadd10fdb16373aee163a8434032348c8
```

### `dpkg` source package: `nghttp2=1.59.0-1ubuntu0.2`

Binary Packages:

- `libnghttp2-14:amd64=1.59.0-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.59.0-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0-1ubuntu0.2.dsc' nghttp2_1.59.0-1ubuntu0.2.dsc 2624 SHA512:f0162428c3f2f3663af8a36ca08b732f3d70240387533816945a6164aff280ae53a9060bc322d619463dbbe28c9a8bafc93c6b0106c3d40c0dd56e561dd2f075
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0.orig.tar.gz' nghttp2_1.59.0.orig.tar.gz 1055492 SHA512:bcb53ff45afae003f11a9feaa21dd80a3abfcde9b3a7fd1f04fc4382d71b5d4430e2d015765a7ae8d68454fcf06e4560c4cb585133aefb237d6ea526f61a8ebd
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0-1ubuntu0.2.debian.tar.xz' nghttp2_1.59.0-1ubuntu0.2.debian.tar.xz 14204 SHA512:b2ca6c685f1366b42eca185a76451f33223b59f172f8842e910394244d7e4bd14b8ceca4e03ccf6658e9cb2649213924f304ed8d5ba143f680388053c7289e66
```

### `dpkg` source package: `node-jquery=3.6.1+dfsg+~3.5.14-1`

Binary Packages:

- `libjs-jquery=3.6.1+dfsg+~3.5.14-1`

Licenses: (parsed from: `/usr/share/doc/libjs-jquery/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/node-jquery/3.6.1+dfsg+~3.5.14-1/


### `dpkg` source package: `norm=1.5.9+dfsg-3.1build1`

Binary Packages:

- `libnorm1t64:amd64=1.5.9+dfsg-3.1build1`

Licenses: (parsed from: `/usr/share/doc/libnorm1t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause-UC`
- `NRL-2-clause`
- `NRL-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `npth=1.6-3.1build1`

Binary Packages:

- `libnpth0t64:amd64=1.6-3.1build1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nspr=2:4.35-1.1build1`

Binary Packages:

- `libnspr4:amd64=2:4.35-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libnspr4/copyright`)

- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nss=2:3.98-1build1`

Binary Packages:

- `libnss3:amd64=2:3.98-1build1`

Licenses: (parsed from: `/usr/share/doc/libnss3/copyright`)

- `BSD-3`
- `MPL-2.0`
- `Zlib`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `numactl=2.0.18-1build1`

Binary Packages:

- `libnuma-dev:amd64=2.0.18-1build1`
- `libnuma1:amd64=2.0.18-1build1`

Licenses: (parsed from: `/usr/share/doc/libnuma-dev/copyright`, `/usr/share/doc/libnuma1/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `numpy=1:1.26.4+ds-6ubuntu1`

Binary Packages:

- `python3-numpy=1:1.26.4+ds-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-numpy/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `Expat`
- `ZLib`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nvidia-settings=510.47.03-0ubuntu4`

Binary Packages:

- `libxnvctrl0:amd64=510.47.03-0ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libxnvctrl0/copyright`)

- `Expat`
- `Expat-NVIDIA`
- `Expat-Precision`
- `Expat-RedHat`
- `GPL-2`
- `other-MetroLink`
- `other-Metrolink`
- `other-XFree`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ocl-icd=2.3.2-1build1`

Binary Packages:

- `ocl-icd-libopencl1:amd64=2.3.2-1build1`

Licenses: (parsed from: `/usr/share/doc/ocl-icd-libopencl1/copyright`)

- `BSD-2-Clause`

Source:

```console
$ apt-get source -qq --print-uris ocl-icd=2.3.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/o/ocl-icd/ocl-icd_2.3.2-1build1.dsc' ocl-icd_2.3.2-1build1.dsc 2303 SHA512:83f217e63516c3e19bc7071671b7eaa0452cfb6e65ea9710a25909c63da9d36edf41fd449c8089b380096a98730fe6cb3405c801421318305192a1359ca52cac
'http://archive.ubuntu.com/ubuntu/pool/main/o/ocl-icd/ocl-icd_2.3.2.orig.tar.gz' ocl-icd_2.3.2.orig.tar.gz 108988 SHA512:5129975a10ffade76d20444345a59c82506914347391ad6c0b4c3826f51dcc641924b4a5abcc65c41766597af9cc7a76b9e5821f41898ff0251a05963e117796
'http://archive.ubuntu.com/ubuntu/pool/main/o/ocl-icd/ocl-icd_2.3.2-1build1.debian.tar.xz' ocl-icd_2.3.2-1build1.debian.tar.xz 12196 SHA512:0604806e152499210809b81acc2ddf237672ea26925f4cc353b650a7cf32aa070b0a2a9faf55a347f5f740197503508439b4cc4bfc1d3c31002245f25dbccc76
```

### `dpkg` source package: `ogdi-dfsg=4.1.1+ds-3build1`

Binary Packages:

- `libogdi-dev=4.1.1+ds-3build1`
- `libogdi4.1:amd64=4.1.1+ds-3build1`

Licenses: (parsed from: `/usr/share/doc/libogdi-dev/copyright`, `/usr/share/doc/libogdi4.1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `OGDI-3I`
- `OGDI-LAS`
- `OGDI-QUEEN`
- `VPFLIB`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `onetbb=2021.11.0-2ubuntu2`

Binary Packages:

- `libtbb-dev:amd64=2021.11.0-2ubuntu2`
- `libtbb12:amd64=2021.11.0-2ubuntu2`
- `libtbbbind-2-5:amd64=2021.11.0-2ubuntu2`
- `libtbbmalloc2:amd64=2021.11.0-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libtbb-dev/copyright`, `/usr/share/doc/libtbb12/copyright`, `/usr/share/doc/libtbbbind-2-5/copyright`, `/usr/share/doc/libtbbmalloc2/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-like-bzip2`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `onevpl=2023.3.0-1build1`

Binary Packages:

- `libvpl2=2023.3.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libvpl2/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `opencv=4.6.0+dfsg-13.1ubuntu1`

Binary Packages:

- `libopencv-calib3d-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-calib3d406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-contrib-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-contrib406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-core-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-core406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-dev=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-dnn-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-dnn406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-features2d-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-features2d406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-flann-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-flann406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-highgui-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-highgui406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-imgcodecs-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-imgcodecs406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-imgproc-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-imgproc406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-ml-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-ml406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-objdetect-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-objdetect406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-photo-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-photo406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-shape-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-shape406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-stitching-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-stitching406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-superres-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-superres406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-video-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-video406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-videoio-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-videoio406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-videostab-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-videostab406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-viz-dev:amd64=4.6.0+dfsg-13.1ubuntu1`
- `libopencv-viz406t64:amd64=4.6.0+dfsg-13.1ubuntu1`
- `python3-opencv:amd64=4.6.0+dfsg-13.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libopencv-calib3d-dev/copyright`, `/usr/share/doc/libopencv-calib3d406t64/copyright`, `/usr/share/doc/libopencv-contrib-dev/copyright`, `/usr/share/doc/libopencv-contrib406t64/copyright`, `/usr/share/doc/libopencv-core-dev/copyright`, `/usr/share/doc/libopencv-core406t64/copyright`, `/usr/share/doc/libopencv-dev/copyright`, `/usr/share/doc/libopencv-dnn-dev/copyright`, `/usr/share/doc/libopencv-dnn406t64/copyright`, `/usr/share/doc/libopencv-features2d-dev/copyright`, `/usr/share/doc/libopencv-features2d406t64/copyright`, `/usr/share/doc/libopencv-flann-dev/copyright`, `/usr/share/doc/libopencv-flann406t64/copyright`, `/usr/share/doc/libopencv-highgui-dev/copyright`, `/usr/share/doc/libopencv-highgui406t64/copyright`, `/usr/share/doc/libopencv-imgcodecs-dev/copyright`, `/usr/share/doc/libopencv-imgcodecs406t64/copyright`, `/usr/share/doc/libopencv-imgproc-dev/copyright`, `/usr/share/doc/libopencv-imgproc406t64/copyright`, `/usr/share/doc/libopencv-ml-dev/copyright`, `/usr/share/doc/libopencv-ml406t64/copyright`, `/usr/share/doc/libopencv-objdetect-dev/copyright`, `/usr/share/doc/libopencv-objdetect406t64/copyright`, `/usr/share/doc/libopencv-photo-dev/copyright`, `/usr/share/doc/libopencv-photo406t64/copyright`, `/usr/share/doc/libopencv-shape-dev/copyright`, `/usr/share/doc/libopencv-shape406t64/copyright`, `/usr/share/doc/libopencv-stitching-dev/copyright`, `/usr/share/doc/libopencv-stitching406t64/copyright`, `/usr/share/doc/libopencv-superres-dev/copyright`, `/usr/share/doc/libopencv-superres406t64/copyright`, `/usr/share/doc/libopencv-video-dev/copyright`, `/usr/share/doc/libopencv-video406t64/copyright`, `/usr/share/doc/libopencv-videoio-dev/copyright`, `/usr/share/doc/libopencv-videoio406t64/copyright`, `/usr/share/doc/libopencv-videostab-dev/copyright`, `/usr/share/doc/libopencv-videostab406t64/copyright`, `/usr/share/doc/libopencv-viz-dev/copyright`, `/usr/share/doc/libopencv-viz406t64/copyright`, `/usr/share/doc/python3-opencv/copyright`)

- `Apache-2.0`
- `Apache-2.0 AND BSD-3-Clause`
- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2.0+`
- `ISC`
- `STEREO_CALIB_PERMISSIVE`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openexr=3.1.5-5.1build3`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.5-5.1build3`
- `libopenexr-dev=3.1.5-5.1build3`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openjdk-21=21.0.9+10-1~24.04`

Binary Packages:

- `openjdk-21-jdk:amd64=21.0.9+10-1~24.04`
- `openjdk-21-jdk-headless:amd64=21.0.9+10-1~24.04`
- `openjdk-21-jre:amd64=21.0.9+10-1~24.04`
- `openjdk-21-jre-headless:amd64=21.0.9+10-1~24.04`

Licenses: (parsed from: `/usr/share/doc/openjdk-21-jdk/copyright`, `/usr/share/doc/openjdk-21-jdk-headless/copyright`, `/usr/share/doc/openjdk-21-jre/copyright`, `/usr/share/doc/openjdk-21-jre-headless/copyright`)

- `BSD-C3`
- `GPL with Classpath exception`
- `GPL-2`
- `LGPL`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris openjdk-21=21.0.9+10-1~24.04
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjdk-21/openjdk-21_21.0.9%2b10-1%7e24.04.dsc' openjdk-21_21.0.9+10-1~24.04.dsc 5043 SHA512:0eca26a893f1566448ec47fd5c9ea8d7cd957ecdb8c782b239336bed428f54942da5438c4f44b6d82bbeecf153a5bd9c558502cdb4d0ba11c2cdd09d7547ec7c
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjdk-21/openjdk-21_21.0.9%2b10.orig-googletest.tar.xz' openjdk-21_21.0.9+10.orig-googletest.tar.xz 616792 SHA512:f9f419254f9346dea707dc6ab2ed185dbe046677c057117730dc6844cc2cc9a910d494f7f868652e52e5d0879b49358e80fe6750600b8a9ce788f488b04b4289
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjdk-21/openjdk-21_21.0.9%2b10.orig.tar.xz' openjdk-21_21.0.9+10.orig.tar.xz 67600676 SHA512:546c7c4f4e4591fe949d6e02fe5db86ced2f3994481f63253a7876f432fd64102386e5bcd0250eac56104b37efe71b1c3e299c4155a5a55d81c94260d3148195
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjdk-21/openjdk-21_21.0.9%2b10-1%7e24.04.debian.tar.xz' openjdk-21_21.0.9+10-1~24.04.debian.tar.xz 216504 SHA512:2de0f2fc13ce029d3964195be497ab62ec262be5c2fbfb406d7abefd81bafb85ae36560b32b5992b18e4100a2dde352e50efc390b3a3a40f8da5b5a96c5ec33c
```

### `dpkg` source package: `openjpeg2=2.5.0-2ubuntu0.4`

Binary Packages:

- `libopenjp2-7:amd64=2.5.0-2ubuntu0.4`
- `libopenjp2-7-dev:amd64=2.5.0-2ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.0-2ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2ubuntu0.4.dsc' openjpeg2_2.5.0-2ubuntu0.4.dsc 2788 SHA512:504ee1b73f90ab1b56d1dd7c66685d9ac215975ed572e3d44e2a2ca4403453eb4ee18f40bc2d4c409d77ab8dcf06b0fea02cb4a7e7b0a16bca69312514b9aee0
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0.orig.tar.xz' openjpeg2_2.5.0.orig.tar.xz 1221108 SHA512:a266297d60ff93e14dbee890b01a76870bda69f082dbe8932fc444ccd260c27aaaac8b22e3c00ca71930b2555a1cad6cf6ed0d5d882d9d13f472cc494cab8234
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2ubuntu0.4.debian.tar.xz' openjpeg2_2.5.0-2ubuntu0.4.debian.tar.xz 20344 SHA512:4d19bfd8fdc6a3a6baa4cf37fb5e3d1f30bc7a57b80307f15d7f35cd7541993e4ce9a743f2c230606433fcdc3e90c82c31d94c6557597e2eadce15fea08f9e3a
```

### `dpkg` source package: `openldap=2.6.7+dfsg-1~exp1ubuntu8.2`

Binary Packages:

- `libldap2:amd64=2.6.7+dfsg-1~exp1ubuntu8.2`

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
$ apt-get source -qq --print-uris openldap=2.6.7+dfsg-1~exp1ubuntu8.2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.7%2bdfsg-1%7eexp1ubuntu8.2.dsc' openldap_2.6.7+dfsg-1~exp1ubuntu8.2.dsc 3488 SHA512:b262ce1ec8742801dadaa6c50393cd2da7359200f6c42c0f2573be883deb13b2e71b85169ba8db1edf5ec11ef5e0122c2f839f4320ead4041423e9a3fa03b679
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.7%2bdfsg.orig.tar.xz' openldap_2.6.7+dfsg.orig.tar.xz 3774648 SHA512:84e02268b096347049b61947a56b5aa13d4d8548eed1bd472821c99fcd0208293d300b6bb78c4acd0e30a20fdd1851894c2f89f6365a359de856e1b095506014
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.7%2bdfsg-1%7eexp1ubuntu8.2.debian.tar.xz' openldap_2.6.7+dfsg-1~exp1ubuntu8.2.debian.tar.xz 186792 SHA512:276056a2c445949ab7cba305eb760f8793b5bae6c487c9301da94553b1c8d83ada9279a537800deef7fc434af4352585071514bafdc9172ac766feb739c590cc
```

### `dpkg` source package: `openmpi=4.1.6-7ubuntu2`

Binary Packages:

- `libopenmpi-dev:amd64=4.1.6-7ubuntu2`
- `libopenmpi3t64:amd64=4.1.6-7ubuntu2`
- `openmpi-bin=4.1.6-7ubuntu2`
- `openmpi-common=4.1.6-7ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libopenmpi-dev/copyright`, `/usr/share/doc/libopenmpi3t64/copyright`, `/usr/share/doc/openmpi-bin/copyright`, `/usr/share/doc/openmpi-common/copyright`)

- `LGPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openni2=2.2.0.33+dfsg-18`

Binary Packages:

- `libopenni2-0:amd64=2.2.0.33+dfsg-18`
- `libopenni2-dev:amd64=2.2.0.33+dfsg-18`

Licenses: (parsed from: `/usr/share/doc/libopenni2-0/copyright`, `/usr/share/doc/libopenni2-dev/copyright`)

- `APACHE-2.0`
- `BSD-3-clause-NVIDIA-LICENSE`
- `GPL-3`
- `GPL-3+`
- `Google`
- `LGPL-2.1`
- `LibJPEG`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/openni2/2.2.0.33+dfsg-18/


### `dpkg` source package: `openni=1.5.4.0+dfsg-7.1build1`

Binary Packages:

- `libopenni-dev:amd64=1.5.4.0+dfsg-7.1build1`
- `libopenni0t64=1.5.4.0+dfsg-7.1build1`

Licenses: (parsed from: `/usr/share/doc/libopenni-dev/copyright`, `/usr/share/doc/libopenni0t64/copyright`)

- `GPL-3`
- `GPL-3+`
- `Google`
- `LGPL-3`
- `LGPL-3+`
- `LibJPEG`
- `TinyXML`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openssh=1:9.6p1-3ubuntu13.14`

Binary Packages:

- `openssh-client=1:9.6p1-3ubuntu13.14`

Licenses: (parsed from: `/usr/share/doc/openssh-client/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat-with-advertising-restriction`
- `Mazieres-BSD-style`
- `OpenSSH`
- `Powell-BSD-style`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openssh=1:9.6p1-3ubuntu13.14
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.6p1-3ubuntu13.14.dsc' openssh_9.6p1-3ubuntu13.14.dsc 3346 SHA512:c2e1c8ad4d1ecba42638a259f5d21f99e2e46f1181572c98b41c514e3e33b421afa2d575f7276773f8812c7211bcdb2789160d0f1cd617b040419f244f03ccc9
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.6p1.orig.tar.gz' openssh_9.6p1.orig.tar.gz 1857862 SHA512:0ebf81e39914c3a90d7777a001ec7376a94b37e6024baf3e972c58f0982b7ddef942315f5e01d56c00ff95603b4a20ee561ab918ecc55511df007ac138160509
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.6p1.orig.tar.gz.asc' openssh_9.6p1.orig.tar.gz.asc 833 SHA512:aec5a5bd6ce480a8e5b5879dc55f8186aec90fe61f085aa92ad7d07f324574aa781be09c83b7443a32848d091fd44fb12c1842d49cee77afc351e550ffcc096d
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.6p1-3ubuntu13.14.debian.tar.xz' openssh_9.6p1-3ubuntu13.14.debian.tar.xz 207248 SHA512:17d6fc517e8d700ae43ee9a8049ab27482fcce1119ddd615b49c30458d22412c2dd8a641ad41f9dbc09d4b4e6c726fb5ffe8594fd310cb5748d3f4c38c17e5c9
```

### `dpkg` source package: `openssl=3.0.13-0ubuntu3.6`

Binary Packages:

- `libssl-dev:amd64=3.0.13-0ubuntu3.6`
- `libssl3t64:amd64=3.0.13-0ubuntu3.6`
- `openssl=3.0.13-0ubuntu3.6`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `opus=1.4-1build1`

Binary Packages:

- `libopus0:amd64=1.4-1build1`

Licenses: (parsed from: `/usr/share/doc/libopus0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `orc=1:0.4.38-1ubuntu0.1`

Binary Packages:

- `liborc-0.4-0t64:amd64=1:0.4.38-1ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris orc=1:0.4.38-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38-1ubuntu0.1.dsc' orc_0.4.38-1ubuntu0.1.dsc 2571 SHA512:cae63b07c180dcee83afdf1b294e9694d4449696fd29a9c5a8bd302b1535b016030d43f3a2f2a4622b0a0fcc79ad2ae10768314959827bf2265fabd399856c81
'http://archive.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38.orig.tar.xz' orc_0.4.38.orig.tar.xz 227152 SHA512:49f34be85f6980e4b5e94f848016f5788b658323f3a120110bc237722ac99938c02976efbe96022d148054330432899533305d4dd21be8fab76fd1995179339a
'http://archive.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38.orig.tar.xz.asc' orc_0.4.38.orig.tar.xz.asc 833 SHA512:5b1a348471fe0854731cc6e26b4e4b31a1f7e325aff85a998d6446f2d77296d1f3bd5d5212690aa8e23591dda2588374b854eaf5037d8d7ba0a9c7a5c2d205a4
'http://archive.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38-1ubuntu0.1.debian.tar.xz' orc_0.4.38-1ubuntu0.1.debian.tar.xz 14488 SHA512:d4f8f81b7a0bd71435da74ca83cbc1b32bd1e5a28b13fe591d4d7edec8e0da81a4c34a5e314673692b94cf438fdec8b033b95aa0450a74a7c324316cc4b03ebf
```

### `dpkg` source package: `orocos-kdl=1.5.1-4build1`

Binary Packages:

- `liborocos-kdl-dev:amd64=1.5.1-4build1`
- `liborocos-kdl1.5:amd64=1.5.1-4build1`
- `python3-pykdl:amd64=1.5.1-4build1`

Licenses: (parsed from: `/usr/share/doc/liborocos-kdl-dev/copyright`, `/usr/share/doc/liborocos-kdl1.5/copyright`, `/usr/share/doc/python3-pykdl/copyright`)

- `BSD-2-clause`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.25.3-4ubuntu2.1`

Binary Packages:

- `libp11-kit0:amd64=0.25.3-4ubuntu2.1`

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
- `customFSFUL`
- `customFSFULLRWD`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.25.3-4ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-4ubuntu2.1.dsc' p11-kit_0.25.3-4ubuntu2.1.dsc 2405 SHA512:8333b22df20f4febfcc6bdf987695d9bee2f0c578a60d15d76fc4099c22fd294dff01772bed717fc220773524a8b674f4ef1ad6b3343856c3c5f8e4adbafc5dc
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz' p11-kit_0.25.3.orig.tar.xz 991528 SHA512:ad2d393bf122526cbba18dc9d5a13f2c1cad7d70125ec90ffd02059dfa5ef30ac59dfc0bb9bc6380c8f317e207c9e87e895f1945634f56ddf910c2958868fb4c
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-4ubuntu2.1.debian.tar.xz' p11-kit_0.25.3-4ubuntu2.1.debian.tar.xz 26028 SHA512:531ecb33634ae9056eac7bac90579b12113a3800fca4d2e4e2e42266e34ed9b96bdbe322b9c6e54ee1fad20ae9760d92e5fc0bae558477add44f3a587913806b
```

### `dpkg` source package: `pam=1.5.3-5ubuntu5.5`

Binary Packages:

- `libpam-modules:amd64=1.5.3-5ubuntu5.5`
- `libpam-modules-bin=1.5.3-5ubuntu5.5`
- `libpam-runtime=1.5.3-5ubuntu5.5`
- `libpam0g:amd64=1.5.3-5ubuntu5.5`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pam=1.5.3-5ubuntu5.5
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.dsc' pam_1.5.3-5ubuntu5.5.dsc 2727 SHA512:59b875e301869358617068f0e2ebcc884ae8c2fad24c487b15d347ee4b826df9a008aa74fa14aa99fc1300ab9fd07dbef6f025e50a005937a093df692f9befc0
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA512:af88e8c1b6a9b737ffaffff7dd9ed8eec996d1fbb5804fb76f590bed66d8a1c2c6024a534d7a7b6d18496b300f3d6571a08874cf406cd2e8cea1d5eff49c136a
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.debian.tar.xz' pam_1.5.3-5ubuntu5.5.debian.tar.xz 204688 SHA512:9c4e286ce3ea8bce267b7571f518e434a704d8c9a46c5de8cee1d0bf4b5303474a5549e5b188ba8b306b282a1797ab3418d299195557da8e275c5f005776f10d
```

### `dpkg` source package: `pango1.0=1.52.1+ds-1build1`

Binary Packages:

- `libpango-1.0-0:amd64=1.52.1+ds-1build1`
- `libpangocairo-1.0-0:amd64=1.52.1+ds-1build1`
- `libpangoft2-1.0-0:amd64=1.52.1+ds-1build1`

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


### `dpkg` source package: `patch=2.7.6-7build3`

Binary Packages:

- `patch=2.7.6-7build3`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pcl=1.14.0+dfsg-1`

Binary Packages:

- `libpcl-apps1.14:amd64=1.14.0+dfsg-1`
- `libpcl-common1.14:amd64=1.14.0+dfsg-1`
- `libpcl-dev=1.14.0+dfsg-1`
- `libpcl-features1.14:amd64=1.14.0+dfsg-1`
- `libpcl-filters1.14:amd64=1.14.0+dfsg-1`
- `libpcl-io1.14:amd64=1.14.0+dfsg-1`
- `libpcl-kdtree1.14:amd64=1.14.0+dfsg-1`
- `libpcl-keypoints1.14:amd64=1.14.0+dfsg-1`
- `libpcl-ml1.14:amd64=1.14.0+dfsg-1`
- `libpcl-octree1.14:amd64=1.14.0+dfsg-1`
- `libpcl-outofcore1.14:amd64=1.14.0+dfsg-1`
- `libpcl-people1.14:amd64=1.14.0+dfsg-1`
- `libpcl-recognition1.14:amd64=1.14.0+dfsg-1`
- `libpcl-registration1.14:amd64=1.14.0+dfsg-1`
- `libpcl-sample-consensus1.14:amd64=1.14.0+dfsg-1`
- `libpcl-search1.14:amd64=1.14.0+dfsg-1`
- `libpcl-segmentation1.14:amd64=1.14.0+dfsg-1`
- `libpcl-stereo1.14:amd64=1.14.0+dfsg-1`
- `libpcl-surface1.14:amd64=1.14.0+dfsg-1`
- `libpcl-tracking1.14:amd64=1.14.0+dfsg-1`
- `libpcl-visualization1.14:amd64=1.14.0+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libpcl-apps1.14/copyright`, `/usr/share/doc/libpcl-common1.14/copyright`, `/usr/share/doc/libpcl-dev/copyright`, `/usr/share/doc/libpcl-features1.14/copyright`, `/usr/share/doc/libpcl-filters1.14/copyright`, `/usr/share/doc/libpcl-io1.14/copyright`, `/usr/share/doc/libpcl-kdtree1.14/copyright`, `/usr/share/doc/libpcl-keypoints1.14/copyright`, `/usr/share/doc/libpcl-ml1.14/copyright`, `/usr/share/doc/libpcl-octree1.14/copyright`, `/usr/share/doc/libpcl-outofcore1.14/copyright`, `/usr/share/doc/libpcl-people1.14/copyright`, `/usr/share/doc/libpcl-recognition1.14/copyright`, `/usr/share/doc/libpcl-registration1.14/copyright`, `/usr/share/doc/libpcl-sample-consensus1.14/copyright`, `/usr/share/doc/libpcl-search1.14/copyright`, `/usr/share/doc/libpcl-segmentation1.14/copyright`, `/usr/share/doc/libpcl-stereo1.14/copyright`, `/usr/share/doc/libpcl-surface1.14/copyright`, `/usr/share/doc/libpcl-tracking1.14/copyright`, `/usr/share/doc/libpcl-visualization1.14/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-FreeBSD`
- `BSD-3-clause`
- `BSL-1`
- `CC-BY-SA-3`
- `Expat`
- `LGPL-3`
- `LGPL-3+`
- `Open-Source`
- `OpenNURBS`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pcl/1.14.0+dfsg-1/


### `dpkg` source package: `pcre2=10.42-4ubuntu2.1`

Binary Packages:

- `libpcre2-16-0:amd64=10.42-4ubuntu2.1`
- `libpcre2-32-0:amd64=10.42-4ubuntu2.1`
- `libpcre2-8-0:amd64=10.42-4ubuntu2.1`
- `libpcre2-dev:amd64=10.42-4ubuntu2.1`
- `libpcre2-posix3:amd64=10.42-4ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu2.1.dsc' pcre2_10.42-4ubuntu2.1.dsc 2277 SHA512:4a66de3dd3c3f3ef6fa078cbdfacd59282da53206c0753f9ddd01fa67b501425ea5e9350e0cece9d31b4194fca5b107146fe8bba97a06c02c431a91891226a6d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA512:a3db6c5c620775838819be616652e73ce00f5ef5c1f49f559ff3efb51a119d02f01254c5901c1f7d0c47c0ddfcf4313e38d6ca32c35381b8f87f36896d10e6f7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu2.1.diff.gz' pcre2_10.42-4ubuntu2.1.diff.gz 8431 SHA512:a739c00ba25573d4e57490d487efcd1f4afbafb820ccb6063fe9d25f22d9a1f9bf7cc91cd89c5ffbb0b533f06133e4beaa16e5aee7f64e8939872ebb933c2f00
```

### `dpkg` source package: `pcsc-lite=2.0.3-1build1`

Binary Packages:

- `libpcsclite1:amd64=2.0.3-1build1`

Licenses: (parsed from: `/usr/share/doc/libpcsclite1/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `perl=5.38.2-3.2ubuntu0.2`

Binary Packages:

- `libperl5.38t64:amd64=5.38.2-3.2ubuntu0.2`
- `perl=5.38.2-3.2ubuntu0.2`
- `perl-base=5.38.2-3.2ubuntu0.2`
- `perl-modules-5.38=5.38.2-3.2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libperl5.38t64/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.38/copyright`)

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
$ apt-get source -qq --print-uris perl=5.38.2-3.2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.dsc' perl_5.38.2-3.2ubuntu0.2.dsc 3036 SHA512:bdd956f4f04ef15d13659bac27cce96c4d98caaacc586525302c9e14c865e7c9ae81b7369caf636fd73074edcbc56a6e204e3c2ab0c8f2db52f8fece9f0d4b6c
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA512:c4ea40ce9eda247c2ced678a75bdbd8bc292baee5ec3490cb00b1947277e1e0e9e5160d108676380efff13d4f1304f0c8d4eaa2c7e66e543ecd57e513075cb8c
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA512:0ca51e447c7a18639627c281a1c7ae6662c773745ea3c86bede46336d5514ecc97ded2c61166e1ac15635581489dc596368907aa3a775b34db225b76d7402d10
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.debian.tar.xz' perl_5.38.2-3.2ubuntu0.2.debian.tar.xz 171736 SHA512:9511993218de5c72dabb87e2ba13a00b034fbb96637b3791515cbac26fa9820067d95d48f165766cce1086304936c1de6150140023915437a91050f27aced32e
```

### `dpkg` source package: `pinentry=1.2.1-3ubuntu5`

Binary Packages:

- `pinentry-curses=1.2.1-3ubuntu5`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pixman=0.42.2-1build1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pkgconf=1.8.1-2build1`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-2build1`
- `pkg-config:amd64=1.8.1-2build1`
- `pkgconf:amd64=1.8.1-2build1`
- `pkgconf-bin=1.8.1-2build1`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkg-config/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pmix=5.0.1-4.1build1`

Binary Packages:

- `libpmix-dev:amd64=5.0.1-4.1build1`
- `libpmix2t64:amd64=5.0.1-4.1build1`

Licenses: (parsed from: `/usr/share/doc/libpmix-dev/copyright`, `/usr/share/doc/libpmix2t64/copyright`)

- `GPL-2`
- `LGPL-2`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `poppler=24.02.0-1ubuntu9.8`

Binary Packages:

- `libpoppler-dev:amd64=24.02.0-1ubuntu9.8`
- `libpoppler-private-dev:amd64=24.02.0-1ubuntu9.8`
- `libpoppler134:amd64=24.02.0-1ubuntu9.8`

Licenses: (parsed from: `/usr/share/doc/libpoppler-dev/copyright`, `/usr/share/doc/libpoppler-private-dev/copyright`, `/usr/share/doc/libpoppler134/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris poppler=24.02.0-1ubuntu9.8
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_24.02.0-1ubuntu9.8.dsc' poppler_24.02.0-1ubuntu9.8.dsc 3940 SHA512:d0d0bfcb54b77b1de1ef3a91b957e9bafd4a7609df7f96b1d93b1416c3fc12dd3d3c20ca8edb6eaa32fca823e5e482c7a0af923e77ea86775235fdde243603f5
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_24.02.0.orig.tar.gz' poppler_24.02.0.orig.tar.gz 1975230 SHA512:75fc41f94ad6848b834eab1cc9199c5ba55b30b12ffbe26d53fa85e86b9918999e752c82d2c5965d6669ace4d9658b1236159c9bfa4bbf40da2660dc00a19f37
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_24.02.0-1ubuntu9.8.debian.tar.xz' poppler_24.02.0-1ubuntu9.8.debian.tar.xz 43812 SHA512:0dcb44752aba54269f1215c9a865375a90250143d9500efb21886c3e2b1e8c35d80a0789a3dab407f2b5944b74f7c735475960a8c603789b182bdefcb4f34113
```

### `dpkg` source package: `popt=1.19+dfsg-1build1`

Binary Packages:

- `libpopt0:amd64=1.19+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libpopt0/copyright`)

- `GPL-2`
- `GPL-2+`
- `expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `postgresql-16=16.11-0ubuntu0.24.04.1`

Binary Packages:

- `libpq-dev=16.11-0ubuntu0.24.04.1`
- `libpq5:amd64=16.11-0ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libpq-dev/copyright`, `/usr/share/doc/libpq5/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `Custom-Unicode`
- `Custom-pg_dump`
- `Custom-regex`
- `GPL-1`
- `PostgreSQL`
- `Tcl`
- `double-metaphone`
- `nagaysau-ishii`

Source:

```console
$ apt-get source -qq --print-uris postgresql-16=16.11-0ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.11-0ubuntu0.24.04.1.dsc' postgresql-16_16.11-0ubuntu0.24.04.1.dsc 4336 SHA512:e55fa28ebad270e8cf26313b1747eedba633d9f3338db906e870830ff97aa1d7e6ee3c467a7e98c06a059b6c531b9a6502e4d5760c2a5e820c4bfc45caaa2c9a
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.11.orig.tar.gz' postgresql-16_16.11.orig.tar.gz 32913275 SHA512:f664fef64dc704f424ac7dfb9f72cf942260b28d7142ff85815f6b1d66e4c2b402e681fdff2b60ab2dfc362609910dfcfee894c8511483f5b0fa3f9a9cae66bd
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.11-0ubuntu0.24.04.1.debian.tar.xz' postgresql-16_16.11-0ubuntu0.24.04.1.debian.tar.xz 37224 SHA512:4836682bcd30238087cea4ad1cb3a9ef5709ceea18d76fb64d8159f96d367e33317dff2dadc17cc5638dff7de02098c87e97004edc9006b5ef1671856e714508
```

### `dpkg` source package: `procps=2:4.0.4-4ubuntu3.2`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-4ubuntu3.2`
- `procps=2:4.0.4-4ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-4ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu3.2.dsc' procps_4.0.4-4ubuntu3.2.dsc 2251 SHA512:3c342f5b82345d0320eefb03be09254259f33a08058ebdaa4bb8130bc8dc295138e2b19729c0f14752ecdad774fd24aae942b1ffa6a591fc0365487031c595d9
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu3.2.debian.tar.xz' procps_4.0.4-4ubuntu3.2.debian.tar.xz 38784 SHA512:51e3e1f8f9e206eecf009e8cb9d32147b12f5961288a07d458e270ae77a9048baef52ec11d921dfd9d8362d3db48d987bac74afcab89f266a0138718ef20844a
```

### `dpkg` source package: `proj=9.4.0-1build2`

Binary Packages:

- `libproj-dev:amd64=9.4.0-1build2`
- `libproj25:amd64=9.4.0-1build2`
- `proj-data=9.4.0-1build2`

Licenses: (parsed from: `/usr/share/doc/libproj-dev/copyright`, `/usr/share/doc/libproj25/copyright`, `/usr/share/doc/proj-data/copyright`)

- `Apache-2.0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LRUCache11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `protobuf=3.21.12-8.2ubuntu0.2`

Binary Packages:

- `libprotobuf32t64:amd64=3.21.12-8.2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libprotobuf32t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause~Google`
- `Expat`
- `GPL-2`
- `GPL-3`
- `GPLWithACException`
- `Public-Domain`

Source:

```console
$ apt-get source -qq --print-uris protobuf=3.21.12-8.2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/protobuf/protobuf_3.21.12-8.2ubuntu0.2.dsc' protobuf_3.21.12-8.2ubuntu0.2.dsc 3162 SHA512:66012c5ac11d2175db17a9df9feeeba3d586785aca5c68bd2e0cf9c926c0044de048385f901bc7338c291b73680cadcb987135eeff7a4b01ca5d614fb98ccc57
'http://archive.ubuntu.com/ubuntu/pool/main/p/protobuf/protobuf_3.21.12.orig.tar.gz' protobuf_3.21.12.orig.tar.gz 5141502 SHA512:152f8441c325e808b942153c15e82fdb533d5273b50c25c28916ec568ada880f79242bb61ee332ac5fb0d20f21239ed6f8de02ef6256cc574b1fc354d002c6b0
'http://archive.ubuntu.com/ubuntu/pool/main/p/protobuf/protobuf_3.21.12-8.2ubuntu0.2.debian.tar.xz' protobuf_3.21.12-8.2ubuntu0.2.debian.tar.xz 44716 SHA512:abd1b31d494d241dc9c9f5cb093b841f977145b5f98b5648be69eebc28adeff3b5ffbd5335b073170283753c28bca445da2772770d05c7d8b9c13179315c6c22
```

### `dpkg` source package: `pybind11=2.11.1-2`

Binary Packages:

- `pybind11-dev=2.11.1-2`

Licenses: (parsed from: `/usr/share/doc/pybind11-dev/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-3-Clause+CLA`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pybind11/2.11.1-2/


### `dpkg` source package: `pycodestyle=2.11.1-1`

Binary Packages:

- `python3-pycodestyle=2.11.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-pycodestyle/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pycodestyle/2.11.1-1/


### `dpkg` source package: `pydocstyle=6.3.0-1.1`

Binary Packages:

- `pydocstyle=6.3.0-1.1`
- `python3-pydocstyle=6.3.0-1.1`

Licenses: (parsed from: `/usr/share/doc/pydocstyle/copyright`, `/usr/share/doc/python3-pydocstyle/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pydocstyle/6.3.0-1.1/


### `dpkg` source package: `pyflakes=3.2.0-1`

Binary Packages:

- `python3-pyflakes=3.2.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-pyflakes/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pyflakes/3.2.0-1/


### `dpkg` source package: `pygments=2.17.2+dfsg-1`

Binary Packages:

- `python3-pygments=2.17.2+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/python3-pygments/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `ISO-1986`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pygments/2.17.2+dfsg-1/


### `dpkg` source package: `pyparsing=3.1.1-1`

Binary Packages:

- `python3-pyparsing=3.1.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-pyparsing/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `MIT/X11`
- `ellis-and-grant`
- `salvolainen`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pyparsing/3.1.1-1/


### `dpkg` source package: `pytest=7.4.4-1`

Binary Packages:

- `python3-pytest=7.4.4-1`

Licenses: (parsed from: `/usr/share/doc/python3-pytest/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pytest/7.4.4-1/


### `dpkg` source package: `python-argcomplete=3.1.4-1ubuntu0.1`

Binary Packages:

- `python3-argcomplete=3.1.4-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-argcomplete/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris python-argcomplete=3.1.4-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4-1ubuntu0.1.dsc' python-argcomplete_3.1.4-1ubuntu0.1.dsc 2509 SHA512:5ae742ceebbfc3f34cd8fbeed2c0744afc0c6dccdeb93acb9e3b83229f83f6f0f3eaead2357773b2e913d801222caaaaf09c95d6abae12f8f6af78c869c7dbc0
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4.orig.tar.gz' python-argcomplete_3.1.4.orig.tar.gz 79529 SHA512:d5108273fb570ec42667acefd1cf397e2fbedb3d4fbc31bb2b3206cdbb3275fde88b4d40e9dc65045b6a94334e6b5b9136054c6291edc21dcd0542f1369fe4b1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4-1ubuntu0.1.debian.tar.xz' python-argcomplete_3.1.4-1ubuntu0.1.debian.tar.xz 8116 SHA512:7dc0b8cbb1d6beec393ef3d29ff16bbd856779fb98448513e501b5504a2a024065a1786ba0d54b481542746a38bc440fa42f2e82e70d1c215ffbf98188e4e0c3
```

### `dpkg` source package: `python-cffi=1.16.0-2build1`

Binary Packages:

- `python3-cffi-backend:amd64=1.16.0-2build1`

Licenses: (parsed from: `/usr/share/doc/python3-cffi-backend/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-cryptography=41.0.7-4ubuntu0.1`

Binary Packages:

- `python3-cryptography=41.0.7-4ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-cryptography/copyright`)

- `Apache`
- `Apache-2.0`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-cryptography=41.0.7-4ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7-4ubuntu0.1.dsc' python-cryptography_41.0.7-4ubuntu0.1.dsc 3412 SHA512:8fc7b6ef5dc010bae649968fef2031111225764ebcb9770127f2ef1a94d725fc50d5a1eb8e1515b4184a6e4d49f5a493d340b96e935cdd4f960082e90ee66b9d
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7.orig.tar.gz' python-cryptography_41.0.7.orig.tar.gz 630892 SHA512:c678da6dfc02d84ca9a26bc42844da8ba356f5dc839fefa0b63636c99107b18415b5970d721b72075fc0f8aefc3785dbf143327ceb7f4ebd075df41291b63219
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7-4ubuntu0.1.debian.tar.xz' python-cryptography_41.0.7-4ubuntu0.1.debian.tar.xz 11512 SHA512:039007135ac2cf4c9f848160cf8bb1562d8a593d92ec37f3282f5800f2f51262c5b7c85ecfc692d921251a4866890a73b8e8b31e864420c5b4664872b909dec6
```

### `dpkg` source package: `python-dateutil=2.8.2-3ubuntu1`

Binary Packages:

- `python3-dateutil=2.8.2-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-dateutil/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-deprecated=1.2.14-1`

Binary Packages:

- `python3-deprecated=1.2.14-1`

Licenses: (parsed from: `/usr/share/doc/python3-deprecated/copyright`)

- `Expat`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-deprecated/1.2.14-1/


### `dpkg` source package: `python-distro=1.9.0-1`

Binary Packages:

- `python3-distro=1.9.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-distro/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-distro/1.9.0-1/


### `dpkg` source package: `python-docutils=0.20.1+dfsg-3`

Binary Packages:

- `docutils-common=0.20.1+dfsg-3`
- `python3-docutils=0.20.1+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/docutils-common/copyright`, `/usr/share/doc/python3-docutils/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `Python-2.1.1`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-docutils/0.20.1+dfsg-3/


### `dpkg` source package: `python-flake8=7.0.0-1`

Binary Packages:

- `python3-flake8=7.0.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-flake8/7.0.0-1/


### `dpkg` source package: `python-importlib-metadata=4.12.0-1`

Binary Packages:

- `python3-importlib-metadata=4.12.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-importlib-metadata/copyright`)

- `Apache-2`
- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-importlib-metadata/4.12.0-1/


### `dpkg` source package: `python-iniconfig=1.1.1-2`

Binary Packages:

- `python3-iniconfig=1.1.1-2`

Licenses: (parsed from: `/usr/share/doc/python3-iniconfig/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-iniconfig/1.1.1-2/


### `dpkg` source package: `python-lark=1.1.9-1`

Binary Packages:

- `python3-lark=1.1.9-1`

Licenses: (parsed from: `/usr/share/doc/python3-lark/copyright`)

- `GPL-2`
- `GPL-2+-with-bootloader-exception`
- `MIT`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-lark/1.1.9-1/


### `dpkg` source package: `python-mccabe=0.7.0-1`

Binary Packages:

- `python3-mccabe=0.7.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-mccabe/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-mccabe/0.7.0-1/


### `dpkg` source package: `python-notify2=0.3-5`

Binary Packages:

- `python3-notify2=0.3-5`

Licenses: (parsed from: `/usr/share/doc/python3-notify2/copyright`)

- `BSD-3-Clause`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-notify2/0.3-5/


### `dpkg` source package: `python-packaging=24.0-1`

Binary Packages:

- `python3-packaging=24.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-packaging/24.0-1/


### `dpkg` source package: `python-pluggy=1.4.0-1`

Binary Packages:

- `python3-pluggy=1.4.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-pluggy/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-pluggy/1.4.0-1/


### `dpkg` source package: `python-psutil=5.9.8-2build2`

Binary Packages:

- `python3-psutil=5.9.8-2build2`

Licenses: (parsed from: `/usr/share/doc/python3-psutil/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-roman=3.3-3`

Binary Packages:

- `python3-roman=3.3-3`

Licenses: (parsed from: `/usr/share/doc/python3-roman/copyright`)

- `Python-2.1.1`
- `ZPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-roman/3.3-3/


### `dpkg` source package: `python-semver=2.10.2-3`

Binary Packages:

- `python3-semver=2.10.2-3`

Licenses: (parsed from: `/usr/share/doc/python3-semver/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-semver/2.10.2-3/


### `dpkg` source package: `python-wrapt=1.15.0-2build3`

Binary Packages:

- `python3-wrapt=1.15.0-2build3`

Licenses: (parsed from: `/usr/share/doc/python3-wrapt/copyright`)

- `BSD-2-clause`
- `PSF-License`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-zipp=1.0.0-6ubuntu0.1`

Binary Packages:

- `python3-zipp=1.0.0-6ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-zipp/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-zipp=1.0.0-6ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-6ubuntu0.1.dsc' python-zipp_1.0.0-6ubuntu0.1.dsc 1616 SHA512:114339a929ac0ea228882adeeb5d4e13856151fcc88c77ee1e531abff30e9c47cf1dc22ba84a3a04391611fdf733cea02c6b28315d028fc48c489fdaf00067e6
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0.orig.tar.gz' python-zipp_1.0.0.orig.tar.gz 10821 SHA512:dbfadfedd30ca4cb31ac4163f367134d96e57405ef00d5f4c19c0af7a141f78487dec29a0ba94975584fcb462d22c8b536bf29c67b7e298368072e897b0e9d82
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-6ubuntu0.1.debian.tar.xz' python-zipp_1.0.0-6ubuntu0.1.debian.tar.xz 4188 SHA512:5d6b7d14ded6a5c2ae9769a023a01c37c85eab5013bf9c747b086d39a0fe43294c48a2ccc92f81df14e399872d36a4cfb19b03dcc51318e32da8a7cc3ecf66e7
```

### `dpkg` source package: `python3-catkin-pkg-modules=1.1.0-2`

Binary Packages:

- `python3-catkin-pkg-modules=1.1.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-argcomplete=0.3.3+upstream-1`

Binary Packages:

- `python3-colcon-argcomplete=0.3.3+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-bash=0.5.0-100`

Binary Packages:

- `python3-colcon-bash=0.5.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-cd=0.2.1-100`

Binary Packages:

- `python3-colcon-cd=0.2.1-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-cmake=0.2.29-100`

Binary Packages:

- `python3-colcon-cmake=0.2.29-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-common-extensions=0.3.0-100`

Binary Packages:

- `python3-colcon-common-extensions=0.3.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-core=0.20.1+upstream-1`

Binary Packages:

- `python3-colcon-core=0.20.1+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-defaults=0.2.9+upstream-1`

Binary Packages:

- `python3-colcon-defaults=0.2.9+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-devtools=0.3.0-100`

Binary Packages:

- `python3-colcon-devtools=0.3.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-library-path=0.2.1-100`

Binary Packages:

- `python3-colcon-library-path=0.2.1-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-metadata=0.2.5-100`

Binary Packages:

- `python3-colcon-metadata=0.2.5-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-mixin=0.2.3-100`

Binary Packages:

- `python3-colcon-mixin=0.2.3-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-notification=0.3.0-100`

Binary Packages:

- `python3-colcon-notification=0.3.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-output=0.2.13-100`

Binary Packages:

- `python3-colcon-output=0.2.13-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-package-information=0.4.0-100`

Binary Packages:

- `python3-colcon-package-information=0.4.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-package-selection=0.2.10-100`

Binary Packages:

- `python3-colcon-package-selection=0.2.10-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-parallel-executor=0.3.0-100`

Binary Packages:

- `python3-colcon-parallel-executor=0.3.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-pkg-config=0.1.0-100`

Binary Packages:

- `python3-colcon-pkg-config=0.1.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-powershell=0.4.0-100`

Binary Packages:

- `python3-colcon-powershell=0.4.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-python-setup-py=0.2.9-100`

Binary Packages:

- `python3-colcon-python-setup-py=0.2.9-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-recursive-crawl=0.2.3-100`

Binary Packages:

- `python3-colcon-recursive-crawl=0.2.3-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-ros=0.5.0+upstream-1`

Binary Packages:

- `python3-colcon-ros=0.5.0+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-test-result=0.3.8-100`

Binary Packages:

- `python3-colcon-test-result=0.3.8-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-zsh=0.5.0-100`

Binary Packages:

- `python3-colcon-zsh=0.5.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-defaults=3.12.3-0ubuntu2.1`

Binary Packages:

- `libpython3-dev:amd64=3.12.3-0ubuntu2.1`
- `libpython3-stdlib:amd64=3.12.3-0ubuntu2.1`
- `python3=3.12.3-0ubuntu2.1`
- `python3-dev=3.12.3-0ubuntu2.1`
- `python3-minimal=3.12.3-0ubuntu2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.12.3-0ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.dsc' python3-defaults_3.12.3-0ubuntu2.1.dsc 3116 SHA512:34bd93d70a55ea6e57e2c8adb7fab3a23507161c2ca61b2c089208cf3706455ef7e072cc04b68af9c1ecb04ed9636e65524501d9e2eb837319f220f275582c4b
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.tar.gz' python3-defaults_3.12.3-0ubuntu2.1.tar.gz 147765 SHA512:9a729a8df22e37d473d39b8c9c95b8c5a7ad8dfd244b3c87576d389f48543edeeaa0bd8b0557de3224d0dbd0f06e02b573cb18adf685a54c02bb485a21ec36e5
```

### `dpkg` source package: `python3-rosdep-modules=0.26.0-1`

Binary Packages:

- `python3-rosdep-modules=0.26.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rosdep=0.26.0-1`

Binary Packages:

- `python3-rosdep=0.26.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rosdistro-modules=1.0.1-1`

Binary Packages:

- `python3-rosdistro-modules=1.0.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rospkg-modules=1.6.1-1`

Binary Packages:

- `python3-rospkg-modules=1.6.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-vcstool=0.3.0-1`

Binary Packages:

- `python3-vcstool=0.3.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3.12=3.12.3-1ubuntu0.10`

Binary Packages:

- `libpython3.12-dev:amd64=3.12.3-1ubuntu0.10`
- `libpython3.12-minimal:amd64=3.12.3-1ubuntu0.10`
- `libpython3.12-stdlib:amd64=3.12.3-1ubuntu0.10`
- `libpython3.12t64:amd64=3.12.3-1ubuntu0.10`
- `python3.12=3.12.3-1ubuntu0.10`
- `python3.12-dev=3.12.3-1ubuntu0.10`
- `python3.12-minimal=3.12.3-1ubuntu0.10`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-dev/copyright`, `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/libpython3.12t64/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-dev/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

- `* Permission to use this software in any way is granted without`
- `By obtaining, using, and/or copying this software and/or its`
- `GPL-2`
- `Permission  is  hereby granted,  free  of charge,  to  any person`
- `Permission is hereby granted, free of charge, to any person obtaining`
- `Permission to use, copy, modify,`
- `Redistribution`
- `This software is provided 'as-is', without any express`
- `This software is provided as-is, without express`
- `binary forms, with`
- `distribute this software`
- `distribute this software and`
- `distribute this software for any`
- `implied`
- `its`
- `use in source`
- `without`

Source:

```console
$ apt-get source -qq --print-uris python3.12=3.12.3-1ubuntu0.10
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3-1ubuntu0.10.dsc' python3.12_3.12.3-1ubuntu0.10.dsc 3311 SHA512:74aac82ac030451df73fdf73dc4431284114c3da3e3d9eccc9a1c494d9a4e023cb7dda5ad43fa72ac3d95c1758d5987ab8638f924515032278bcf6ba5d4d597e
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3.orig.tar.xz' python3.12_3.12.3.orig.tar.xz 20625068 SHA512:4a2213b108e7f1f1525baa8348e68b2a2336d925e60d0a59f0225fc470768a2c8031edafc0b8243f94dbae18afda335ee5adf2785328c2218fd64cbb439f13a4
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3-1ubuntu0.10.debian.tar.xz' python3.12_3.12.3-1ubuntu0.10.debian.tar.xz 263188 SHA512:5631baea6248a5e60e4e49aaa12e48aa9d78315d361a1969aed1a72aca9c320ebad9d5b795996205d4c1bac037d34aed07ee8f76d2e772c662441ed9926682ce
```

### `dpkg` source package: `pyyaml=6.0.1-2build2`

Binary Packages:

- `python3-yaml=6.0.1-2build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `qhull=2020.2-6build1`

Binary Packages:

- `libqhull-dev:amd64=2020.2-6build1`
- `libqhull-r8.0:amd64=2020.2-6build1`
- `libqhull8.0:amd64=2020.2-6build1`
- `libqhullcpp8.0:amd64=2020.2-6build1`

Licenses: (parsed from: `/usr/share/doc/libqhull-dev/copyright`, `/usr/share/doc/libqhull-r8.0/copyright`, `/usr/share/doc/libqhull8.0/copyright`, `/usr/share/doc/libqhullcpp8.0/copyright`)

- `GPL-3`
- `GPL-3+`
- `Qhull`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `qtbase-opensource-src=5.15.13+dfsg-1ubuntu1`

Binary Packages:

- `libqt5concurrent5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5core5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5dbus5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5gui5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5network5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5opengl5-dev:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5opengl5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5printsupport5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5sql5-sqlite:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5sql5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5test5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5widgets5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `libqt5xml5t64:amd64=5.15.13+dfsg-1ubuntu1`
- `qt5-qmake:amd64=5.15.13+dfsg-1ubuntu1`
- `qt5-qmake-bin=5.15.13+dfsg-1ubuntu1`
- `qtbase5-dev:amd64=5.15.13+dfsg-1ubuntu1`
- `qtbase5-dev-tools=5.15.13+dfsg-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libqt5concurrent5t64/copyright`, `/usr/share/doc/libqt5core5t64/copyright`, `/usr/share/doc/libqt5dbus5t64/copyright`, `/usr/share/doc/libqt5gui5t64/copyright`, `/usr/share/doc/libqt5network5t64/copyright`, `/usr/share/doc/libqt5opengl5-dev/copyright`, `/usr/share/doc/libqt5opengl5t64/copyright`, `/usr/share/doc/libqt5printsupport5t64/copyright`, `/usr/share/doc/libqt5sql5-sqlite/copyright`, `/usr/share/doc/libqt5sql5t64/copyright`, `/usr/share/doc/libqt5test5t64/copyright`, `/usr/share/doc/libqt5widgets5t64/copyright`, `/usr/share/doc/libqt5xml5t64/copyright`, `/usr/share/doc/qt5-qmake/copyright`, `/usr/share/doc/qt5-qmake-bin/copyright`, `/usr/share/doc/qtbase5-dev/copyright`, `/usr/share/doc/qtbase5-dev-tools/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Bitstream`
- `CC0-1.0`
- `Expat`
- `FTL`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3 with Qt-1.0 exception`
- `Harfbuzz`
- `Hybrid-BSD`
- `ICC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `MPL-2.0`
- `Unicode`
- `W3C`
- `Zlib`
- `brg-endian`
- `libjpeg`
- `libpng`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `qtchooser=66-2build2`

Binary Packages:

- `qtchooser=66-2build2`

Licenses: (parsed from: `/usr/share/doc/qtchooser/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1 with Digia-1.1 exception`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `qtdeclarative-opensource-src=5.15.13+dfsg-1ubuntu0.1`

Binary Packages:

- `libqt5qml5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `libqt5qmlmodels5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `libqt5qmlworkerscript5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `libqt5quick5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `libqt5quickparticles5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `libqt5quickshapes5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `libqt5quicktest5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `libqt5quickwidgets5:amd64=5.15.13+dfsg-1ubuntu0.1`
- `qt5-qmltooling-plugins:amd64=5.15.13+dfsg-1ubuntu0.1`
- `qtdeclarative5-dev:amd64=5.15.13+dfsg-1ubuntu0.1`
- `qtdeclarative5-dev-tools=5.15.13+dfsg-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libqt5qml5/copyright`, `/usr/share/doc/libqt5qmlmodels5/copyright`, `/usr/share/doc/libqt5qmlworkerscript5/copyright`, `/usr/share/doc/libqt5quick5/copyright`, `/usr/share/doc/libqt5quickparticles5/copyright`, `/usr/share/doc/libqt5quickshapes5/copyright`, `/usr/share/doc/libqt5quicktest5/copyright`, `/usr/share/doc/libqt5quickwidgets5/copyright`, `/usr/share/doc/qt5-qmltooling-plugins/copyright`, `/usr/share/doc/qtdeclarative5-dev/copyright`, `/usr/share/doc/qtdeclarative5-dev-tools/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Ecma`
- `Bitstream`
- `CC0`
- `Expat`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3 with Qt-1.0 exception`
- `LGPL-2.1`
- `LGPL-3`
- `MPL-1.1`
- `daniel-font`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris qtdeclarative-opensource-src=5.15.13+dfsg-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/q/qtdeclarative-opensource-src/qtdeclarative-opensource-src_5.15.13%2bdfsg-1ubuntu0.1.dsc' qtdeclarative-opensource-src_5.15.13+dfsg-1ubuntu0.1.dsc 5442 SHA512:49071e4f5b04920df8ecaad9d13a92e5ab5a8d0749b87c92ae1c01d65c0342fabd164576e320df0143a81c5f0e7da483a229fdf55b101dfa03bce62381c6f79e
'http://archive.ubuntu.com/ubuntu/pool/universe/q/qtdeclarative-opensource-src/qtdeclarative-opensource-src_5.15.13%2bdfsg.orig.tar.xz' qtdeclarative-opensource-src_5.15.13+dfsg.orig.tar.xz 21701956 SHA512:96425b310cb4295a81e056cfd79eb796eb4dab8dff590505cb97815a74c56be934dc8a97b55c5f92f435429549aa36509e0ad5ffd49c8ab73ba70ce298b8af0c
'http://archive.ubuntu.com/ubuntu/pool/universe/q/qtdeclarative-opensource-src/qtdeclarative-opensource-src_5.15.13%2bdfsg-1ubuntu0.1.debian.tar.xz' qtdeclarative-opensource-src_5.15.13+dfsg-1ubuntu0.1.debian.tar.xz 53016 SHA512:914e7f7a757eb381ed5539cc1b4c27391ce1ca4f11f3379a6d02082c38b6d0d897428eab7018cab5a78c5a8b7fab53ff7d5176124408c15740167f0656929f18
```

### `dpkg` source package: `qtlocation-opensource-src=5.15.13+dfsg-1`

Binary Packages:

- `libqt5positioning5:amd64=5.15.13+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libqt5positioning5/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSL-1.0`
- `Expat`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-3`
- `GPL-3 with Qt-1.0 exception`
- `ISC`
- `LGPL-3`
- `Zlib`
- `curl`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/qtlocation-opensource-src/5.15.13+dfsg-1/


### `dpkg` source package: `qtsensors-opensource-src=5.15.13-1`

Binary Packages:

- `libqt5sensors5:amd64=5.15.13-1`

Licenses: (parsed from: `/usr/share/doc/libqt5sensors5/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2,`
- `GPL-3`
- `GPL-3 with Qt-1.0 exception`
- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/qtsensors-opensource-src/5.15.13-1/


### `dpkg` source package: `qttools-opensource-src=5.15.13-1`

Binary Packages:

- `libqt5designer5:amd64=5.15.13-1`
- `libqt5designercomponents5:amd64=5.15.13-1`
- `libqt5help5:amd64=5.15.13-1`
- `qdoc-qt5=5.15.13-1`
- `qhelpgenerator-qt5=5.15.13-1`
- `qt5-assistant=5.15.13-1`
- `qtattributionsscanner-qt5=5.15.13-1`
- `qttools5-dev:amd64=5.15.13-1`
- `qttools5-dev-tools=5.15.13-1`
- `qttools5-private-dev:amd64=5.15.13-1`

Licenses: (parsed from: `/usr/share/doc/libqt5designer5/copyright`, `/usr/share/doc/libqt5designercomponents5/copyright`, `/usr/share/doc/libqt5help5/copyright`, `/usr/share/doc/qdoc-qt5/copyright`, `/usr/share/doc/qhelpgenerator-qt5/copyright`, `/usr/share/doc/qt5-assistant/copyright`, `/usr/share/doc/qtattributionsscanner-qt5/copyright`, `/usr/share/doc/qttools5-dev/copyright`, `/usr/share/doc/qttools5-dev-tools/copyright`, `/usr/share/doc/qttools5-private-dev/copyright`)

- `BSD-3-clause`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3 with Qt-1.0 exception`
- `LGPL-3`
- `MIT-Unicode`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/qttools-opensource-src/5.15.13-1/


### `dpkg` source package: `qtwebchannel-opensource-src=5.15.13-1`

Binary Packages:

- `libqt5webchannel5:amd64=5.15.13-1`

Licenses: (parsed from: `/usr/share/doc/libqt5webchannel5/copyright`)

- `BSD-3-clause`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2-or-3 with KDE Exception`
- `GPL-3`
- `GPL-3 with Qt-1.0 exception`
- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/qtwebchannel-opensource-src/5.15.13-1/


### `dpkg` source package: `qtwebkit-opensource-src=5.212.0~alpha4-36`

Binary Packages:

- `libqt5webkit5:amd64=5.212.0~alpha4-36`
- `libqt5webkit5-dev:amd64=5.212.0~alpha4-36`

Licenses: (parsed from: `/usr/share/doc/libqt5webkit5/copyright`, `/usr/share/doc/libqt5webkit5-dev/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `CC-BY-SA-3.0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with AutoConf exception`
- `GPL-3+ with Bison exception`
- `ISC`
- `ISC-like-dmgfp`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT-like-Wayland`
- `MIT-like-XSLTExtensions`
- `MIT-like-icu`
- `MPL-1.1`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/qtwebkit-opensource-src/5.212.0~alpha4-36/


### `dpkg` source package: `rdma-core=50.0-2ubuntu0.2`

Binary Packages:

- `ibverbs-providers:amd64=50.0-2ubuntu0.2`
- `libibverbs-dev:amd64=50.0-2ubuntu0.2`
- `libibverbs1:amd64=50.0-2ubuntu0.2`
- `librdmacm1t64:amd64=50.0-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/ibverbs-providers/copyright`, `/usr/share/doc/libibverbs-dev/copyright`, `/usr/share/doc/libibverbs1/copyright`, `/usr/share/doc/librdmacm1t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-MIT`
- `CC0`
- `CPL-1.0`
- `GPL-2`
- `GPL-2+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris rdma-core=50.0-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/r/rdma-core/rdma-core_50.0-2ubuntu0.2.dsc' rdma-core_50.0-2ubuntu0.2.dsc 3237 SHA512:7c2e72c055e0a1d30ac473ebea4e1b936507422568c7396323d5fb7f6c99e8585c21e55d47d3f3c6d78d344e2efb02976de4f9097c3fb9f240040444014af607
'http://archive.ubuntu.com/ubuntu/pool/main/r/rdma-core/rdma-core_50.0.orig.tar.gz' rdma-core_50.0.orig.tar.gz 1961247 SHA512:0d341300dde2a8756ab0e80bf8d316627c997e85661d50b51897aa03e1b7326f4ca7a6f24e370354779482a2d9455e58dbb07e6292ed8b511e7f195e4e2d1850
'http://archive.ubuntu.com/ubuntu/pool/main/r/rdma-core/rdma-core_50.0-2ubuntu0.2.debian.tar.xz' rdma-core_50.0-2ubuntu0.2.debian.tar.xz 45744 SHA512:e0d558ca20e04bc1c7752bcb3d7a2558596d631fd4c45b5ff285c37ea52e9a3ce4dfc866e4ed0988ede572e11a8cf122f5effe3bf18bdd1153395f0f9f35293b
```

### `dpkg` source package: `readline=8.2-4build1`

Binary Packages:

- `libreadline8t64:amd64=8.2-4build1`
- `readline-common=8.2-4build1`

Licenses: (parsed from: `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rhash=1.4.3-3build1`

Binary Packages:

- `librhash0:amd64=1.4.3-3build1`

Licenses: (parsed from: `/usr/share/doc/librhash0/copyright`)

- `0BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rocm-compilersupport=6.0+git20231212.4510c28+dfsg-3build2`

Binary Packages:

- `libamd-comgr2:amd64=6.0+git20231212.4510c28+dfsg-3build2`

Licenses: (parsed from: `/usr/share/doc/libamd-comgr2/copyright`)

- `Expat`
- `NCSA`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rocm-hipamd=5.7.1-3`

Binary Packages:

- `libamdhip64-5=5.7.1-3`

Licenses: (parsed from: `/usr/share/doc/libamdhip64-5/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-2-clause`
- `Expat`
- `Khronos`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/rocm-hipamd/5.7.1-3/


### `dpkg` source package: `rocr-runtime=5.7.1-2build1`

Binary Packages:

- `libhsa-runtime64-1=5.7.1-2build1`

Licenses: (parsed from: `/usr/share/doc/libhsa-runtime64-1/copyright`)

- `BSD-3-clause`
- `Expat`
- `Expat-Intel`
- `NCSA`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `roct-thunk-interface=5.7.0-1build1`

Binary Packages:

- `libhsakmt1:amd64=5.7.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libhsakmt1/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `NCSA`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-apt-source=1.1.0~noble`

Binary Packages:

- `ros2-apt-source=1.1.0~noble`

Licenses: (parsed from: `/usr/share/doc/ros2-apt-source/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-action-msgs=2.0.3-1noble.20251007.204356`

Binary Packages:

- `ros-jazzy-action-msgs=2.0.3-1noble.20251007.204356`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-action-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-actionlib-msgs=5.3.6-1noble.20251007.220001`

Binary Packages:

- `ros-jazzy-actionlib-msgs=5.3.6-1noble.20251007.220001`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-actionlib-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-auto=2.5.4-1noble.20250424.110435`

Binary Packages:

- `ros-jazzy-ament-cmake-auto=2.5.4-1noble.20250424.110435`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-copyright=0.17.3-1noble.20250805.112604`

Binary Packages:

- `ros-jazzy-ament-cmake-copyright=0.17.3-1noble.20250805.112604`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-core=2.5.4-1noble.20250424.102850`

Binary Packages:

- `ros-jazzy-ament-cmake-core=2.5.4-1noble.20250424.102850`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-core/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-cppcheck=0.17.3-1noble.20250805.112316`

Binary Packages:

- `ros-jazzy-ament-cmake-cppcheck=0.17.3-1noble.20250805.112316`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-cpplint=0.17.3-1noble.20250805.112450`

Binary Packages:

- `ros-jazzy-ament-cmake-cpplint=0.17.3-1noble.20250805.112450`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-cpplint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-definitions=2.5.4-1noble.20250424.105216`

Binary Packages:

- `ros-jazzy-ament-cmake-export-definitions=2.5.4-1noble.20250424.105216`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-definitions/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-dependencies=2.5.4-1noble.20250424.105204`

Binary Packages:

- `ros-jazzy-ament-cmake-export-dependencies=2.5.4-1noble.20250424.105204`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-include-directories=2.5.4-1noble.20250424.105215`

Binary Packages:

- `ros-jazzy-ament-cmake-export-include-directories=2.5.4-1noble.20250424.105215`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-interfaces=2.5.4-1noble.20250424.105241`

Binary Packages:

- `ros-jazzy-ament-cmake-export-interfaces=2.5.4-1noble.20250424.105241`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-libraries=2.5.4-1noble.20250424.105214`

Binary Packages:

- `ros-jazzy-ament-cmake-export-libraries=2.5.4-1noble.20250424.105214`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-link-flags=2.5.4-1noble.20250424.105220`

Binary Packages:

- `ros-jazzy-ament-cmake-export-link-flags=2.5.4-1noble.20250424.105220`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-link-flags/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-targets=2.5.4-1noble.20250424.105255`

Binary Packages:

- `ros-jazzy-ament-cmake-export-targets=2.5.4-1noble.20250424.105255`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-targets/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-flake8=0.17.3-1noble.20250805.112646`

Binary Packages:

- `ros-jazzy-ament-cmake-flake8=0.17.3-1noble.20250805.112646`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gen-version-h=2.5.4-1noble.20250424.105221`

Binary Packages:

- `ros-jazzy-ament-cmake-gen-version-h=2.5.4-1noble.20250424.105221`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gen-version-h/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gmock=2.5.4-1noble.20250424.110352`

Binary Packages:

- `ros-jazzy-ament-cmake-gmock=2.5.4-1noble.20250424.110352`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gmock/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gtest=2.5.4-1noble.20250424.110324`

Binary Packages:

- `ros-jazzy-ament-cmake-gtest=2.5.4-1noble.20250424.110324`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gtest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-include-directories=2.5.4-1noble.20250424.105225`

Binary Packages:

- `ros-jazzy-ament-cmake-include-directories=2.5.4-1noble.20250424.105225`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-libraries=2.5.4-1noble.20250424.105129`

Binary Packages:

- `ros-jazzy-ament-cmake-libraries=2.5.4-1noble.20250424.105129`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-lint-cmake=0.17.3-1noble.20250805.112325`

Binary Packages:

- `ros-jazzy-ament-cmake-lint-cmake=0.17.3-1noble.20250805.112325`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-pep257=0.17.3-1noble.20250805.112551`

Binary Packages:

- `ros-jazzy-ament-cmake-pep257=0.17.3-1noble.20250805.112551`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-pep257/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-pytest=2.5.4-1noble.20250424.121852`

Binary Packages:

- `ros-jazzy-ament-cmake-pytest=2.5.4-1noble.20250424.121852`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-pytest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-python=2.5.4-1noble.20250424.105135`

Binary Packages:

- `ros-jazzy-ament-cmake-python=2.5.4-1noble.20250424.105135`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-python/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-ros=0.12.0-3noble.20250424.132322`

Binary Packages:

- `ros-jazzy-ament-cmake-ros=0.12.0-3noble.20250424.132322`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-target-dependencies=2.5.4-1noble.20250424.105252`

Binary Packages:

- `ros-jazzy-ament-cmake-target-dependencies=2.5.4-1noble.20250424.105252`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-target-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-test=2.5.4-1noble.20250424.110207`

Binary Packages:

- `ros-jazzy-ament-cmake-test=2.5.4-1noble.20250424.110207`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-test/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-uncrustify=0.17.3-1noble.20250805.112332`

Binary Packages:

- `ros-jazzy-ament-cmake-uncrustify=0.17.3-1noble.20250805.112332`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-version=2.5.4-1noble.20250424.105248`

Binary Packages:

- `ros-jazzy-ament-cmake-version=2.5.4-1noble.20250424.105248`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-version/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-xmllint=0.17.3-1noble.20250805.112540`

Binary Packages:

- `ros-jazzy-ament-cmake-xmllint=0.17.3-1noble.20250805.112540`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake=2.5.4-1noble.20250424.110322`

Binary Packages:

- `ros-jazzy-ament-cmake=2.5.4-1noble.20250424.110322`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-copyright=0.17.3-1noble.20250805.112453`

Binary Packages:

- `ros-jazzy-ament-copyright=0.17.3-1noble.20250805.112453`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cppcheck=0.17.3-1noble.20250805.112227`

Binary Packages:

- `ros-jazzy-ament-cppcheck=0.17.3-1noble.20250805.112227`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cpplint=0.17.3-1noble.20250805.112209`

Binary Packages:

- `ros-jazzy-ament-cpplint=0.17.3-1noble.20250805.112209`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cpplint/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-flake8=0.17.3-1noble.20250805.112455`

Binary Packages:

- `ros-jazzy-ament-flake8=0.17.3-1noble.20250805.112455`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-index-cpp=1.8.1-1noble.20250424.120900`

Binary Packages:

- `ros-jazzy-ament-index-cpp=1.8.1-1noble.20250424.120900`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-index-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-index-python=1.8.1-1noble.20250424.105330`

Binary Packages:

- `ros-jazzy-ament-index-python=1.8.1-1noble.20250424.105330`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-index-python/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-auto=0.17.3-1noble.20250805.112212`

Binary Packages:

- `ros-jazzy-ament-lint-auto=0.17.3-1noble.20250805.112212`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-cmake=0.17.3-1noble.20250805.112225`

Binary Packages:

- `ros-jazzy-ament-lint-cmake=0.17.3-1noble.20250805.112225`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-common=0.17.3-1noble.20250805.112704`

Binary Packages:

- `ros-jazzy-ament-lint-common=0.17.3-1noble.20250805.112704`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-common/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint=0.17.3-1noble.20250805.112323`

Binary Packages:

- `ros-jazzy-ament-lint=0.17.3-1noble.20250805.112323`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-package=0.16.4-1noble.20250406.073531`

Binary Packages:

- `ros-jazzy-ament-package=0.16.4-1noble.20250406.073531`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-package/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-pep257=0.17.3-1noble.20250805.112455`

Binary Packages:

- `ros-jazzy-ament-pep257=0.17.3-1noble.20250805.112455`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-pep257/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-uncrustify=0.17.3-1noble.20250805.112224`

Binary Packages:

- `ros-jazzy-ament-uncrustify=0.17.3-1noble.20250805.112224`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-xmllint=0.17.3-1noble.20250805.112456`

Binary Packages:

- `ros-jazzy-ament-xmllint=0.17.3-1noble.20250805.112456`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-angles=1.16.1-1noble.20250923.225554`

Binary Packages:

- `ros-jazzy-angles=1.16.1-1noble.20250923.225554`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-angles/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-builtin-interfaces=2.0.3-1noble.20251007.174212`

Binary Packages:

- `ros-jazzy-builtin-interfaces=2.0.3-1noble.20251007.174212`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-builtin-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-camera-calibration-parsers=5.1.7-1noble.20251025.091547`

Binary Packages:

- `ros-jazzy-camera-calibration-parsers=5.1.7-1noble.20251025.091547`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-camera-calibration-parsers/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-camera-calibration=5.0.11-1noble.20251025.092211`

Binary Packages:

- `ros-jazzy-camera-calibration=5.0.11-1noble.20251025.092211`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-camera-calibration/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-camera-info-manager=5.1.7-1noble.20251025.100231`

Binary Packages:

- `ros-jazzy-camera-info-manager=5.1.7-1noble.20251025.100231`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-camera-info-manager/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-class-loader=2.7.0-3noble.20250822.213808`

Binary Packages:

- `ros-jazzy-class-loader=2.7.0-3noble.20250822.213808`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-class-loader/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-common-interfaces=5.3.6-1noble.20251007.222809`

Binary Packages:

- `ros-jazzy-common-interfaces=5.3.6-1noble.20251007.222809`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-common-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-composition-interfaces=2.0.3-1noble.20251007.205937`

Binary Packages:

- `ros-jazzy-composition-interfaces=2.0.3-1noble.20251007.205937`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-composition-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-compressed-depth-image-transport=4.0.6-1noble.20251025.094518`

Binary Packages:

- `ros-jazzy-compressed-depth-image-transport=4.0.6-1noble.20251025.094518`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-compressed-depth-image-transport/copyright`)

- `BSD`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-compressed-image-transport=4.0.6-1noble.20251025.094523`

Binary Packages:

- `ros-jazzy-compressed-image-transport=4.0.6-1noble.20251025.094523`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-compressed-image-transport/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-console-bridge-vendor=1.7.1-3noble.20250424.111236`

Binary Packages:

- `ros-jazzy-console-bridge-vendor=1.7.1-3noble.20250424.111236`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-console-bridge-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-cv-bridge=4.1.0-1noble.20251025.091614`

Binary Packages:

- `ros-jazzy-cv-bridge=4.1.0-1noble.20251025.091614`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-cv-bridge/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-depth-image-proc=5.0.11-1noble.20251108.000606`

Binary Packages:

- `ros-jazzy-depth-image-proc=5.0.11-1noble.20251108.000606`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-depth-image-proc/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-diagnostic-msgs=5.3.6-1noble.20251007.222514`

Binary Packages:

- `ros-jazzy-diagnostic-msgs=5.3.6-1noble.20251007.222514`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-diagnostic-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-diagnostic-updater=4.2.6-1noble.20251025.083217`

Binary Packages:

- `ros-jazzy-diagnostic-updater=4.2.6-1noble.20251025.083217`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-diagnostic-updater/copyright`)

- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-domain-coordinator=0.12.0-3noble.20250424.105456`

Binary Packages:

- `ros-jazzy-domain-coordinator=0.12.0-3noble.20250424.105456`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-domain-coordinator/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-eigen3-cmake-module=0.3.0-3noble.20250424.120917`

Binary Packages:

- `ros-jazzy-eigen3-cmake-module=0.3.0-3noble.20250424.120917`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-eigen3-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastcdr=2.2.5-1noble.20250424.105503`

Binary Packages:

- `ros-jazzy-fastcdr=2.2.5-1noble.20250424.105503`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastcdr/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastrtps-cmake-module=3.6.2-1noble.20250805.113744`

Binary Packages:

- `ros-jazzy-fastrtps-cmake-module=3.6.2-1noble.20250805.113744`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastrtps-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastrtps=2.14.5-2noble.20250801.162203`

Binary Packages:

- `ros-jazzy-fastrtps=2.14.5-2noble.20250801.162203`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastrtps/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-filters=2.2.2-1noble.20251025.091952`

Binary Packages:

- `ros-jazzy-filters=2.2.2-1noble.20251025.091952`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-filters/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-foonathan-memory-vendor=1.3.1-3noble.20250424.105505`

Binary Packages:

- `ros-jazzy-foonathan-memory-vendor=1.3.1-3noble.20250424.105505`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-foonathan-memory-vendor/copyright`)

- `Apache License 2.0`
- `zlib License`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-geometry-msgs=5.3.6-1noble.20251007.214105`

Binary Packages:

- `ros-jazzy-geometry-msgs=5.3.6-1noble.20251007.214105`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-geometry-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-geometry2=0.36.16-1noble.20251107.234417`

Binary Packages:

- `ros-jazzy-geometry2=0.36.16-1noble.20251107.234417`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-geometry2/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-gmock-vendor=1.14.9000-2noble.20250424.105626`

Binary Packages:

- `ros-jazzy-gmock-vendor=1.14.9000-2noble.20250424.105626`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-gmock-vendor/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-gtest-vendor=1.14.9000-2noble.20250424.105519`

Binary Packages:

- `ros-jazzy-gtest-vendor=1.14.9000-2noble.20250424.105519`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-gtest-vendor/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-common=5.1.7-1noble.20251025.101642`

Binary Packages:

- `ros-jazzy-image-common=5.1.7-1noble.20251025.101642`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-common/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-geometry=4.1.0-1noble.20251007.222653`

Binary Packages:

- `ros-jazzy-image-geometry=4.1.0-1noble.20251007.222653`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-geometry/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-pipeline=5.0.11-1noble.20251108.005008`

Binary Packages:

- `ros-jazzy-image-pipeline=5.0.11-1noble.20251108.005008`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-pipeline/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-proc=5.0.11-1noble.20251107.235928`

Binary Packages:

- `ros-jazzy-image-proc=5.0.11-1noble.20251107.235928`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-proc/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-publisher=5.0.11-1noble.20251025.100722`

Binary Packages:

- `ros-jazzy-image-publisher=5.0.11-1noble.20251025.100722`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-publisher/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-rotate=5.0.11-1noble.20251107.235558`

Binary Packages:

- `ros-jazzy-image-rotate=5.0.11-1noble.20251107.235558`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-rotate/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-transport-plugins=4.0.6-1noble.20251025.095230`

Binary Packages:

- `ros-jazzy-image-transport-plugins=4.0.6-1noble.20251025.095230`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-transport-plugins/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-transport=5.1.7-1noble.20251025.085726`

Binary Packages:

- `ros-jazzy-image-transport=5.1.7-1noble.20251025.085726`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-transport/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-image-view=5.0.11-1noble.20251025.092220`

Binary Packages:

- `ros-jazzy-image-view=5.0.11-1noble.20251025.092220`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-image-view/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-kdl-parser=2.11.0-3noble.20251014.164903`

Binary Packages:

- `ros-jazzy-kdl-parser=2.11.0-3noble.20251014.164903`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-kdl-parser/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-keyboard-handler=0.3.1-2noble.20250424.121057`

Binary Packages:

- `ros-jazzy-keyboard-handler=0.3.1-2noble.20250424.121057`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-keyboard-handler/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-laser-filters=2.0.9-1noble.20251107.235035`

Binary Packages:

- `ros-jazzy-laser-filters=2.0.9-1noble.20251107.235035`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-laser-filters/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-laser-geometry=2.7.2-1noble.20251107.230441`

Binary Packages:

- `ros-jazzy-laser-geometry=2.7.2-1noble.20251107.230441`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-laser-geometry/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-ros=0.26.10-1noble.20251107.230345`

Binary Packages:

- `ros-jazzy-launch-ros=0.26.10-1noble.20251107.230345`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing-ament-cmake=3.4.9-1noble.20251107.233352`

Binary Packages:

- `ros-jazzy-launch-testing-ament-cmake=3.4.9-1noble.20251107.233352`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing-ament-cmake/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing-ros=0.26.10-1noble.20251107.233353`

Binary Packages:

- `ros-jazzy-launch-testing-ros=0.26.10-1noble.20251107.233353`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing=3.4.9-1noble.20251107.230454`

Binary Packages:

- `ros-jazzy-launch-testing=3.4.9-1noble.20251107.230454`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-xml=3.4.9-1noble.20251107.230347`

Binary Packages:

- `ros-jazzy-launch-xml=3.4.9-1noble.20251107.230347`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-xml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-yaml=3.4.9-1noble.20251107.230358`

Binary Packages:

- `ros-jazzy-launch-yaml=3.4.9-1noble.20251107.230358`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-yaml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch=3.4.9-1noble.20251107.230234`

Binary Packages:

- `ros-jazzy-launch=3.4.9-1noble.20251107.230234`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-liblz4-vendor=0.26.9-1noble.20250812.082450`

Binary Packages:

- `ros-jazzy-liblz4-vendor=0.26.9-1noble.20250812.082450`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-liblz4-vendor/copyright`)

- `Apache License 2.0`
- `BSD`
- `GPLv2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-libstatistics-collector=1.7.4-1noble.20251025.081135`

Binary Packages:

- `ros-jazzy-libstatistics-collector=1.7.4-1noble.20251025.081135`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-libstatistics-collector/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-libyaml-vendor=1.6.3-2noble.20250424.112946`

Binary Packages:

- `ros-jazzy-libyaml-vendor=1.6.3-2noble.20250424.112946`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-libyaml-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-lifecycle-msgs=2.0.3-1noble.20251007.205940`

Binary Packages:

- `ros-jazzy-lifecycle-msgs=2.0.3-1noble.20251007.205940`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-lifecycle-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-mcap-vendor=0.26.9-1noble.20250812.082736`

Binary Packages:

- `ros-jazzy-mcap-vendor=0.26.9-1noble.20250812.082736`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-mcap-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-message-filters=4.11.9-1noble.20251025.083409`

Binary Packages:

- `ros-jazzy-message-filters=4.11.9-1noble.20251025.083409`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-message-filters/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-nav-msgs=5.3.6-1noble.20251007.214617`

Binary Packages:

- `ros-jazzy-nav-msgs=5.3.6-1noble.20251007.214617`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-nav-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-orocos-kdl-vendor=0.5.1-2noble.20250424.121040`

Binary Packages:

- `ros-jazzy-orocos-kdl-vendor=0.5.1-2noble.20250424.121040`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-orocos-kdl-vendor/copyright`)

- `Apache License 2.0`
- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-osrf-pycommon=2.1.7-1noble.20250806.145758`

Binary Packages:

- `ros-jazzy-osrf-pycommon=2.1.7-1noble.20250806.145758`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-osrf-pycommon/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pcl-conversions=2.6.2-1noble.20251025.085029`

Binary Packages:

- `ros-jazzy-pcl-conversions=2.6.2-1noble.20251025.085029`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pcl-conversions/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pcl-msgs=1.0.0-9noble.20251007.215622`

Binary Packages:

- `ros-jazzy-pcl-msgs=1.0.0-9noble.20251007.215622`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pcl-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pcl-ros=2.6.2-1noble.20251107.235627`

Binary Packages:

- `ros-jazzy-pcl-ros=2.6.2-1noble.20251107.235627`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pcl-ros/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-perception-pcl=2.6.2-1noble.20251108.004749`

Binary Packages:

- `ros-jazzy-perception-pcl=2.6.2-1noble.20251108.004749`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-perception-pcl/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-perception=0.11.0-1noble.20251108.005042`

Binary Packages:

- `ros-jazzy-perception=0.11.0-1noble.20251108.005042`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-perception/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pluginlib=5.4.3-1noble.20251014.160510`

Binary Packages:

- `ros-jazzy-pluginlib=5.4.3-1noble.20251014.160510`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pluginlib/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pybind11-vendor=3.1.3-1noble.20250424.113112`

Binary Packages:

- `ros-jazzy-pybind11-vendor=3.1.3-1noble.20250424.113112`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pybind11-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-python-cmake-module=0.11.1-2noble.20250424.121311`

Binary Packages:

- `ros-jazzy-python-cmake-module=0.11.1-2noble.20250424.121311`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-python-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-python-orocos-kdl-vendor=0.5.1-2noble.20250424.121418`

Binary Packages:

- `ros-jazzy-python-orocos-kdl-vendor=0.5.1-2noble.20250424.121418`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-python-orocos-kdl-vendor/copyright`)

- `Apache License 2.0`
- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-action=9.2.8-1noble.20251025.073213`

Binary Packages:

- `ros-jazzy-rcl-action=9.2.8-1noble.20251025.073213`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-interfaces=2.0.3-1noble.20251007.205439`

Binary Packages:

- `ros-jazzy-rcl-interfaces=2.0.3-1noble.20251007.205439`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-lifecycle=9.2.8-1noble.20251025.073253`

Binary Packages:

- `ros-jazzy-rcl-lifecycle=9.2.8-1noble.20251025.073253`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-logging-interface=3.1.1-1noble.20250822.213636`

Binary Packages:

- `ros-jazzy-rcl-logging-interface=3.1.1-1noble.20250822.213636`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-logging-interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-logging-spdlog=3.1.1-1noble.20250822.213802`

Binary Packages:

- `ros-jazzy-rcl-logging-spdlog=3.1.1-1noble.20250822.213802`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-logging-spdlog/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-yaml-param-parser=9.2.8-1noble.20251025.071256`

Binary Packages:

- `ros-jazzy-rcl-yaml-param-parser=9.2.8-1noble.20251025.071256`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-yaml-param-parser/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl=9.2.8-1noble.20251025.072955`

Binary Packages:

- `ros-jazzy-rcl=9.2.8-1noble.20251025.072955`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-action=28.1.13-1noble.20251025.084420`

Binary Packages:

- `ros-jazzy-rclcpp-action=28.1.13-1noble.20251025.084420`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-components=28.1.13-1noble.20251025.085132`

Binary Packages:

- `ros-jazzy-rclcpp-components=28.1.13-1noble.20251025.085132`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-components/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-lifecycle=28.1.13-1noble.20251025.095015`

Binary Packages:

- `ros-jazzy-rclcpp-lifecycle=28.1.13-1noble.20251025.095015`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp=28.1.13-1noble.20251025.081428`

Binary Packages:

- `ros-jazzy-rclcpp=28.1.13-1noble.20251025.081428`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclpy=7.1.6-1noble.20251025.073438`

Binary Packages:

- `ros-jazzy-rclpy=7.1.6-1noble.20251025.073438`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclpy/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcpputils=2.11.2-1noble.20250822.213640`

Binary Packages:

- `ros-jazzy-rcpputils=2.11.2-1noble.20250822.213640`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcpputils/copyright`)

- `Apache License 2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcutils=6.7.4-1noble.20250822.213450`

Binary Packages:

- `ros-jazzy-rcutils=6.7.4-1noble.20250822.213450`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcutils/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-dds-common=3.1.0-2noble.20251007.214255`

Binary Packages:

- `ros-jazzy-rmw-dds-common=3.1.0-2noble.20251007.214255`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-dds-common/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-fastrtps-cpp=8.4.3-1noble.20251007.222258`

Binary Packages:

- `ros-jazzy-rmw-fastrtps-cpp=8.4.3-1noble.20251007.222258`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-fastrtps-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-fastrtps-shared-cpp=8.4.3-1noble.20251007.221648`

Binary Packages:

- `ros-jazzy-rmw-fastrtps-shared-cpp=8.4.3-1noble.20251007.221648`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-fastrtps-shared-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-implementation-cmake=7.3.2-1noble.20250424.121413`

Binary Packages:

- `ros-jazzy-rmw-implementation-cmake=7.3.2-1noble.20250424.121413`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-implementation-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-implementation=2.15.6-1noble.20251025.072752`

Binary Packages:

- `ros-jazzy-rmw-implementation=2.15.6-1noble.20251025.072752`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-implementation/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw=7.3.2-1noble.20250822.213956`

Binary Packages:

- `ros-jazzy-rmw=7.3.2-1noble.20250822.213956`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-robot-state-publisher=3.3.3-3noble.20251108.002618`

Binary Packages:

- `ros-jazzy-robot-state-publisher=3.3.3-3noble.20251108.002618`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-robot-state-publisher/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-base=0.11.0-1noble.20251108.003726`

Binary Packages:

- `ros-jazzy-ros-base=0.11.0-1noble.20251108.003726`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-base/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-core=0.11.0-1noble.20251108.001621`

Binary Packages:

- `ros-jazzy-ros-core=0.11.0-1noble.20251108.001621`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-core/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-environment=4.2.1-1noble.20250424.105249`

Binary Packages:

- `ros-jazzy-ros-environment=4.2.1-1noble.20250424.105249`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-environment/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-workspace=1.0.3-7noble.20250424.104106`

Binary Packages:

- `ros-jazzy-ros-workspace=1.0.3-7noble.20250424.104106`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-workspace/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2action=0.32.6-1noble.20251025.083524`

Binary Packages:

- `ros-jazzy-ros2action=0.32.6-1noble.20251025.083524`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2bag=0.26.9-1noble.20251025.100903`

Binary Packages:

- `ros-jazzy-ros2bag=0.26.9-1noble.20251025.100903`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2bag/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2cli-common-extensions=0.3.0-3noble.20251108.001245`

Binary Packages:

- `ros-jazzy-ros2cli-common-extensions=0.3.0-3noble.20251108.001245`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2cli-common-extensions/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2cli=0.32.6-1noble.20251025.083450`

Binary Packages:

- `ros-jazzy-ros2cli=0.32.6-1noble.20251025.083450`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2cli/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2component=0.32.6-1noble.20251025.093130`

Binary Packages:

- `ros-jazzy-ros2component=0.32.6-1noble.20251025.093130`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2component/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2doctor=0.32.6-1noble.20251025.083527`

Binary Packages:

- `ros-jazzy-ros2doctor=0.32.6-1noble.20251025.083527`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2doctor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2interface=0.32.6-1noble.20251025.093127`

Binary Packages:

- `ros-jazzy-ros2interface=0.32.6-1noble.20251025.093127`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2launch=0.26.10-1noble.20251107.233403`

Binary Packages:

- `ros-jazzy-ros2launch=0.26.10-1noble.20251107.233403`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2lifecycle=0.32.6-1noble.20251025.083657`

Binary Packages:

- `ros-jazzy-ros2lifecycle=0.32.6-1noble.20251025.083657`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2multicast=0.32.6-1noble.20251025.093203`

Binary Packages:

- `ros-jazzy-ros2multicast=0.32.6-1noble.20251025.093203`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2multicast/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2node=0.32.6-1noble.20251025.083529`

Binary Packages:

- `ros-jazzy-ros2node=0.32.6-1noble.20251025.083529`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2node/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2param=0.32.6-1noble.20251025.083649`

Binary Packages:

- `ros-jazzy-ros2param=0.32.6-1noble.20251025.083649`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2param/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2pkg=0.32.6-1noble.20251025.093102`

Binary Packages:

- `ros-jazzy-ros2pkg=0.32.6-1noble.20251025.093102`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2pkg/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2run=0.32.6-1noble.20251025.093203`

Binary Packages:

- `ros-jazzy-ros2run=0.32.6-1noble.20251025.093203`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2run/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2service=0.32.6-1noble.20251025.083609`

Binary Packages:

- `ros-jazzy-ros2service=0.32.6-1noble.20251025.083609`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2service/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2topic=0.32.6-1noble.20251025.083536`

Binary Packages:

- `ros-jazzy-ros2topic=0.32.6-1noble.20251025.083536`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2topic/copyright`)

- `Apache License 2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-compression-zstd=0.26.9-1noble.20251025.102926`

Binary Packages:

- `ros-jazzy-rosbag2-compression-zstd=0.26.9-1noble.20251025.102926`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-compression-zstd/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-compression=0.26.9-1noble.20251025.095220`

Binary Packages:

- `ros-jazzy-rosbag2-compression=0.26.9-1noble.20251025.095220`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-compression/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-cpp=0.26.9-1noble.20251025.092404`

Binary Packages:

- `ros-jazzy-rosbag2-cpp=0.26.9-1noble.20251025.092404`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-interfaces=0.26.9-1noble.20251007.205529`

Binary Packages:

- `ros-jazzy-rosbag2-interfaces=0.26.9-1noble.20251007.205529`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-py=0.26.9-1noble.20251025.100437`

Binary Packages:

- `ros-jazzy-rosbag2-py=0.26.9-1noble.20251025.100437`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage-default-plugins=0.26.9-1noble.20251025.102933`

Binary Packages:

- `ros-jazzy-rosbag2-storage-default-plugins=0.26.9-1noble.20251025.102933`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage-default-plugins/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage-mcap=0.26.9-1noble.20251025.095231`

Binary Packages:

- `ros-jazzy-rosbag2-storage-mcap=0.26.9-1noble.20251025.095231`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage-mcap/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage-sqlite3=0.26.9-1noble.20251025.095229`

Binary Packages:

- `ros-jazzy-rosbag2-storage-sqlite3=0.26.9-1noble.20251025.095229`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage-sqlite3/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage=0.26.9-1noble.20251025.092133`

Binary Packages:

- `ros-jazzy-rosbag2-storage=0.26.9-1noble.20251025.092133`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-transport=0.26.9-1noble.20251025.100007`

Binary Packages:

- `ros-jazzy-rosbag2-transport=0.26.9-1noble.20251025.100007`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-transport/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2=0.26.9-1noble.20251025.103135`

Binary Packages:

- `ros-jazzy-rosbag2=0.26.9-1noble.20251025.103135`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosgraph-msgs=2.0.3-1noble.20251007.205623`

Binary Packages:

- `ros-jazzy-rosgraph-msgs=2.0.3-1noble.20251007.205623`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosgraph-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-adapter=4.6.6-1noble.20250805.113911`

Binary Packages:

- `ros-jazzy-rosidl-adapter=4.6.6-1noble.20250805.113911`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-adapter/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-cli=4.6.6-1noble.20250805.113749`

Binary Packages:

- `ros-jazzy-rosidl-cli=4.6.6-1noble.20250805.113749`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-cli/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-cmake=4.6.6-1noble.20250805.114541`

Binary Packages:

- `ros-jazzy-rosidl-cmake=4.6.6-1noble.20250805.114541`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-core-generators=0.2.0-3noble.20251007.163926`

Binary Packages:

- `ros-jazzy-rosidl-core-generators=0.2.0-3noble.20251007.163926`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-core-generators/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-core-runtime=0.2.0-3noble.20251007.163928`

Binary Packages:

- `ros-jazzy-rosidl-core-runtime=0.2.0-3noble.20251007.163928`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-core-runtime/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-default-generators=1.6.0-3noble.20251007.205127`

Binary Packages:

- `ros-jazzy-rosidl-default-generators=1.6.0-3noble.20251007.205127`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-default-generators/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-default-runtime=1.6.0-3noble.20251007.205126`

Binary Packages:

- `ros-jazzy-rosidl-default-runtime=1.6.0-3noble.20251007.205126`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-default-runtime/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-dynamic-typesupport-fastrtps=0.1.0-3noble.20250822.213955`

Binary Packages:

- `ros-jazzy-rosidl-dynamic-typesupport-fastrtps=0.1.0-3noble.20250822.213955`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-dynamic-typesupport-fastrtps/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-dynamic-typesupport=0.1.2-3noble.20250822.213811`

Binary Packages:

- `ros-jazzy-rosidl-dynamic-typesupport=0.1.2-3noble.20250822.213811`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-dynamic-typesupport/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-c=4.6.6-1noble.20250822.213637`

Binary Packages:

- `ros-jazzy-rosidl-generator-c=4.6.6-1noble.20250822.213637`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-cpp=4.6.6-1noble.20250822.214013`

Binary Packages:

- `ros-jazzy-rosidl-generator-cpp=4.6.6-1noble.20250822.214013`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-py=0.22.2-1noble.20251007.163814`

Binary Packages:

- `ros-jazzy-rosidl-generator-py=0.22.2-1noble.20251007.163814`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-type-description=4.6.6-1noble.20250805.114415`

Binary Packages:

- `ros-jazzy-rosidl-generator-type-description=4.6.6-1noble.20250805.114415`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-type-description/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-parser=4.6.6-1noble.20250805.114345`

Binary Packages:

- `ros-jazzy-rosidl-parser=4.6.6-1noble.20250805.114345`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-parser/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-pycommon=4.6.6-1noble.20250805.114412`

Binary Packages:

- `ros-jazzy-rosidl-pycommon=4.6.6-1noble.20250805.114412`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-pycommon/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-c=4.6.6-1noble.20250822.213646`

Binary Packages:

- `ros-jazzy-rosidl-runtime-c=4.6.6-1noble.20250822.213646`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-cpp=4.6.6-1noble.20250822.213826`

Binary Packages:

- `ros-jazzy-rosidl-runtime-cpp=4.6.6-1noble.20250822.213826`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-py=0.13.1-2noble.20250805.114417`

Binary Packages:

- `ros-jazzy-rosidl-runtime-py=0.13.1-2noble.20250805.114417`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-c=3.2.2-1noble.20250822.213951`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-c=3.2.2-1noble.20250822.213951`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-cpp=3.2.2-1noble.20250822.214409`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-cpp=3.2.2-1noble.20250822.214409`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-fastrtps-c=3.6.2-1noble.20250822.214325`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-fastrtps-c=3.6.2-1noble.20250822.214325`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-fastrtps-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-fastrtps-cpp=3.6.2-1noble.20250822.214204`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-fastrtps-cpp=3.6.2-1noble.20250822.214204`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-fastrtps-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-interface=4.6.6-1noble.20250805.113752`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-interface=4.6.6-1noble.20250805.113752`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-introspection-c=4.6.6-1noble.20250822.213824`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-introspection-c=4.6.6-1noble.20250822.213824`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-introspection-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-introspection-cpp=4.6.6-1noble.20250822.214216`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-introspection-cpp=4.6.6-1noble.20250822.214216`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-introspection-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rpyutils=0.4.2-1noble.20250919.223519`

Binary Packages:

- `ros-jazzy-rpyutils=0.4.2-1noble.20250919.223519`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rpyutils/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sensor-msgs-py=5.3.6-1noble.20251007.220112`

Binary Packages:

- `ros-jazzy-sensor-msgs-py=5.3.6-1noble.20251007.220112`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sensor-msgs-py/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sensor-msgs=5.3.6-1noble.20251007.214825`

Binary Packages:

- `ros-jazzy-sensor-msgs=5.3.6-1noble.20251007.214825`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sensor-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-service-msgs=2.0.3-1noble.20251007.204108`

Binary Packages:

- `ros-jazzy-service-msgs=2.0.3-1noble.20251007.204108`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-service-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-shape-msgs=5.3.6-1noble.20251007.215708`

Binary Packages:

- `ros-jazzy-shape-msgs=5.3.6-1noble.20251007.215708`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-shape-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-spdlog-vendor=1.6.1-1noble.20250424.113136`

Binary Packages:

- `ros-jazzy-spdlog-vendor=1.6.1-1noble.20250424.113136`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-spdlog-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sqlite3-vendor=0.26.9-1noble.20250812.082434`

Binary Packages:

- `ros-jazzy-sqlite3-vendor=0.26.9-1noble.20250812.082434`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sqlite3-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sros2-cmake=0.13.4-1noble.20251025.093113`

Binary Packages:

- `ros-jazzy-sros2-cmake=0.13.4-1noble.20251025.093113`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sros2-cmake/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sros2=0.13.4-1noble.20251025.083537`

Binary Packages:

- `ros-jazzy-sros2=0.13.4-1noble.20251025.083537`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sros2/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-statistics-msgs=2.0.3-1noble.20251007.205628`

Binary Packages:

- `ros-jazzy-statistics-msgs=2.0.3-1noble.20251007.205628`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-statistics-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-std-msgs=5.3.6-1noble.20251007.205629`

Binary Packages:

- `ros-jazzy-std-msgs=5.3.6-1noble.20251007.205629`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-std-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-std-srvs=5.3.6-1noble.20251007.214409`

Binary Packages:

- `ros-jazzy-std-srvs=5.3.6-1noble.20251007.214409`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-std-srvs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-stereo-image-proc=5.0.11-1noble.20251108.004345`

Binary Packages:

- `ros-jazzy-stereo-image-proc=5.0.11-1noble.20251108.004345`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-stereo-image-proc/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-stereo-msgs=5.3.6-1noble.20251007.215701`

Binary Packages:

- `ros-jazzy-stereo-msgs=5.3.6-1noble.20251007.215701`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-stereo-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-bullet=0.36.16-1noble.20251107.232511`

Binary Packages:

- `ros-jazzy-tf2-bullet=0.36.16-1noble.20251107.232511`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-bullet/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-eigen-kdl=0.36.16-1noble.20251107.233903`

Binary Packages:

- `ros-jazzy-tf2-eigen-kdl=0.36.16-1noble.20251107.233903`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-eigen-kdl/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-eigen=0.36.16-1noble.20251107.232850`

Binary Packages:

- `ros-jazzy-tf2-eigen=0.36.16-1noble.20251107.232850`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-eigen/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-geometry-msgs=0.36.16-1noble.20251107.234112`

Binary Packages:

- `ros-jazzy-tf2-geometry-msgs=0.36.16-1noble.20251107.234112`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-geometry-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-kdl=0.36.16-1noble.20251107.234123`

Binary Packages:

- `ros-jazzy-tf2-kdl=0.36.16-1noble.20251107.234123`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-kdl/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-msgs=0.36.16-1noble.20251107.230017`

Binary Packages:

- `ros-jazzy-tf2-msgs=0.36.16-1noble.20251107.230017`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-py=0.36.16-1noble.20251107.233823`

Binary Packages:

- `ros-jazzy-tf2-py=0.36.16-1noble.20251107.233823`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-py/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-ros-py=0.36.16-1noble.20251107.234043`

Binary Packages:

- `ros-jazzy-tf2-ros-py=0.36.16-1noble.20251107.234043`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-ros-py/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-ros=0.36.16-1noble.20251107.230257`

Binary Packages:

- `ros-jazzy-tf2-ros=0.36.16-1noble.20251107.230257`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-ros/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-sensor-msgs=0.36.16-1noble.20251107.234124`

Binary Packages:

- `ros-jazzy-tf2-sensor-msgs=0.36.16-1noble.20251107.234124`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-sensor-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-tools=0.36.16-1noble.20251107.234141`

Binary Packages:

- `ros-jazzy-tf2-tools=0.36.16-1noble.20251107.234141`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-tools/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2=0.36.16-1noble.20251107.230009`

Binary Packages:

- `ros-jazzy-tf2=0.36.16-1noble.20251107.230009`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-theora-image-transport=4.0.6-1noble.20251025.092248`

Binary Packages:

- `ros-jazzy-theora-image-transport=4.0.6-1noble.20251025.092248`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-theora-image-transport/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tinyxml2-vendor=0.9.1-3noble.20250424.121610`

Binary Packages:

- `ros-jazzy-tinyxml2-vendor=0.9.1-3noble.20250424.121610`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tinyxml2-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tracetools-image-pipeline=5.0.11-1noble.20250523.130939`

Binary Packages:

- `ros-jazzy-tracetools-image-pipeline=5.0.11-1noble.20250523.130939`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tracetools-image-pipeline/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tracetools=8.2.4-1noble.20250805.123634`

Binary Packages:

- `ros-jazzy-tracetools=8.2.4-1noble.20250805.123634`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tracetools/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-trajectory-msgs=5.3.6-1noble.20251007.214856`

Binary Packages:

- `ros-jazzy-trajectory-msgs=5.3.6-1noble.20251007.214856`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-trajectory-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-type-description-interfaces=2.0.3-1noble.20251007.204357`

Binary Packages:

- `ros-jazzy-type-description-interfaces=2.0.3-1noble.20251007.204357`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-type-description-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-uncrustify-vendor=3.0.1-1noble.20250424.113218`

Binary Packages:

- `ros-jazzy-uncrustify-vendor=3.0.1-1noble.20250424.113218`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-uncrustify-vendor/copyright`)

- `Apache License 2.0`
- `GNU General Public License v2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-unique-identifier-msgs=2.5.0-3noble.20251007.174227`

Binary Packages:

- `ros-jazzy-unique-identifier-msgs=2.5.0-3noble.20251007.174227`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-unique-identifier-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdf-parser-plugin=2.10.0-3noble.20250424.134356`

Binary Packages:

- `ros-jazzy-urdf-parser-plugin=2.10.0-3noble.20250424.134356`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdf-parser-plugin/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdf=2.10.0-3noble.20251014.161545`

Binary Packages:

- `ros-jazzy-urdf=2.10.0-3noble.20251014.161545`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdf/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdfdom-headers=1.1.2-1noble.20250424.110139`

Binary Packages:

- `ros-jazzy-urdfdom-headers=1.1.2-1noble.20250424.110139`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdfdom-headers/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdfdom=4.0.2-1noble.20250520.160646`

Binary Packages:

- `ros-jazzy-urdfdom=4.0.2-1noble.20250520.160646`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdfdom/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-vision-opencv=4.1.0-1noble.20251025.095203`

Binary Packages:

- `ros-jazzy-vision-opencv=4.1.0-1noble.20251025.095203`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-vision-opencv/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-visualization-msgs=5.3.6-1noble.20251007.215329`

Binary Packages:

- `ros-jazzy-visualization-msgs=5.3.6-1noble.20251007.215329`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-visualization-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-yaml-cpp-vendor=9.0.1-1noble.20250424.113219`

Binary Packages:

- `ros-jazzy-yaml-cpp-vendor=9.0.1-1noble.20250424.113219`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-yaml-cpp-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-zstd-image-transport=4.0.6-1noble.20251025.094638`

Binary Packages:

- `ros-jazzy-zstd-image-transport=4.0.6-1noble.20251025.094638`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-zstd-image-transport/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-zstd-vendor=0.26.9-1noble.20250812.082425`

Binary Packages:

- `ros-jazzy-zstd-vendor=0.26.9-1noble.20250812.082425`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-zstd-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rpcsvc-proto=1.4.2-0ubuntu7`

Binary Packages:

- `rpcsvc-proto=1.4.2-0ubuntu7`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rust-rav1e=0.7.1-2`

Binary Packages:

- `librav1e0:amd64=0.7.1-2`

Licenses: (parsed from: `/usr/share/doc/librav1e0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/rust-rav1e/0.7.1-2/


### `dpkg` source package: `sed=4.9-2build1`

Binary Packages:

- `sed=4.9-2build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sensible-utils=0.0.22`

Binary Packages:

- `sensible-utils=0.0.22`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sensible-utils/0.0.22/


### `dpkg` source package: `setuptools=68.1.2-2ubuntu1.2`

Binary Packages:

- `python3-pkg-resources=68.1.2-2ubuntu1.2`
- `python3-setuptools=68.1.2-2ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/python3-pkg-resources/copyright`, `/usr/share/doc/python3-setuptools/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris setuptools=68.1.2-2ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2ubuntu1.2.dsc' setuptools_68.1.2-2ubuntu1.2.dsc 2296 SHA512:4d7bf690b646aaaef52f1bdddba79dc2402fb941afb24f2fd4ad0339018c285ea77e7d856ce839bf99a82b3c27d99e1dfb4b6ffc27b2a5dceacf2e017292b109
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2.orig.tar.gz' setuptools_68.1.2.orig.tar.gz 2198001 SHA512:a5a84102ce72f38162b190b91286013cb8660b45f383df04fba65e38c658a5c5b93cdf05f789436618fa596b3ca6688a7c54d31d6d10b729124d3b135660c328
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2ubuntu1.2.debian.tar.xz' setuptools_68.1.2-2ubuntu1.2.debian.tar.xz 17712 SHA512:48a17f679f1122b494c68d35436ebc5f248a42bea2f0deea70b81f6d29496b15ce62e71f1e6ef35ca851a77bb0ebac94452aea32779fbecddbe832ef93184c65
```

### `dpkg` source package: `sgml-base=1.31`

Binary Packages:

- `sgml-base=1.31`

Licenses: (parsed from: `/usr/share/doc/sgml-base/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sgml-base/1.31/


### `dpkg` source package: `shadow=1:4.13+dfsg1-4ubuntu3.2`

Binary Packages:

- `login=1:4.13+dfsg1-4ubuntu3.2`
- `passwd=1:4.13+dfsg1-4ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.13+dfsg1-4ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-4ubuntu3.2.dsc' shadow_4.13+dfsg1-4ubuntu3.2.dsc 2400 SHA512:705091aa67f89349a8eb829d3abbac649a417080b7c2d9aa46d0a887dacee4a1cb52642c0bc4e7cdb4b277e5747ae516330174d959522bb5d33bc8c54449a190
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1.orig.tar.xz' shadow_4.13+dfsg1.orig.tar.xz 1811752 SHA512:27106ca26d6e4c9e5833cf79811b10f656ade547bbc18b87faf79bbe0581a9e1467cbb6c354320e2d5233d17208d77742ebf197d32b6d2f08439e37e368ded1d
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-4ubuntu3.2.debian.tar.xz' shadow_4.13+dfsg1-4ubuntu3.2.debian.tar.xz 96392 SHA512:67cd7c7f869250d39ebb7af023ae4aca6eef88de143a85510135d547bb6988895ef02d9aff798888e5d507f415d7d17193c354b2437764b0c4bea18b1178531d
```

### `dpkg` source package: `shared-mime-info=2.4-4`

Binary Packages:

- `shared-mime-info=2.4-4`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/shared-mime-info/2.4-4/


### `dpkg` source package: `shine=3.1.1-2build1`

Binary Packages:

- `libshine3:amd64=3.1.1-2build1`

Licenses: (parsed from: `/usr/share/doc/libshine3/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `six=1.16.0-4`

Binary Packages:

- `python3-six=1.16.0-4`

Licenses: (parsed from: `/usr/share/doc/python3-six/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/six/1.16.0-4/


### `dpkg` source package: `snappy=1.1.10-1build1`

Binary Packages:

- `libsnappy1v5:amd64=1.1.10-1build1`

Licenses: (parsed from: `/usr/share/doc/libsnappy1v5/copyright`)

- `BSD-3-Clause`
- `CC-BY-3.0`
- `CC-BY-4.0`
- `MIT`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `snowball=2.2.0-4build1`

Binary Packages:

- `python3-snowballstemmer=2.2.0-4build1`

Licenses: (parsed from: `/usr/share/doc/python3-snowballstemmer/copyright`)

- `BSD-3-snowball`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `socket++=1.12.13+git20131030.5d039ba-1build1`

Binary Packages:

- `libsocket++1:amd64=1.12.13+git20131030.5d039ba-1build1`

Licenses: (parsed from: `/usr/share/doc/libsocket++1/copyright`)

- `AS_IS`
- `PD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `spatialite=5.1.0-3build1`

Binary Packages:

- `libspatialite-dev:amd64=5.1.0-3build1`
- `libspatialite8t64:amd64=5.1.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libspatialite-dev/copyright`, `/usr/share/doc/libspatialite8t64/copyright`)

- `BSD-4-Clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `spdlog=1:1.12.0+ds-2build1`

Binary Packages:

- `libspdlog-dev:amd64=1:1.12.0+ds-2build1`
- `libspdlog1.12:amd64=1:1.12.0+ds-2build1`

Licenses: (parsed from: `/usr/share/doc/libspdlog-dev/copyright`, `/usr/share/doc/libspdlog1.12/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `speex=1.2.1-2ubuntu2.24.04.1`

Binary Packages:

- `libspeex1:amd64=1.2.1-2ubuntu2.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libspeex1/copyright`)

- `BSD-3-Clause`
- `GFDL-1.1-or-later`
- `GFDL-1.2`
- `LGPL-2`
- `LGPL-2.0-or-later`
- `custom-1`

Source:

```console
$ apt-get source -qq --print-uris speex=1.2.1-2ubuntu2.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/speex/speex_1.2.1-2ubuntu2.24.04.1.dsc' speex_1.2.1-2ubuntu2.24.04.1.dsc 2460 SHA512:c78f8e14352cf31a1fa0333ac4350c97da749430426cf1975843dce7a9bcfa83ef8683aa4c389e351901b3d3a8f37472010bc4b2b45e7fbaa8f4e2553d30a697
'http://archive.ubuntu.com/ubuntu/pool/main/s/speex/speex_1.2.1.orig.tar.gz' speex_1.2.1.orig.tar.gz 1043278 SHA512:52e00300df82e1c7fb527b245af02b99a1f37faef74d004b7cd981052f1aa22a412cb18f5c7a5618df4c958f727c97eb7385beec99d68548d5b02e76192d4e0a
'http://archive.ubuntu.com/ubuntu/pool/main/s/speex/speex_1.2.1.orig.tar.gz.asc' speex_1.2.1.orig.tar.gz.asc 488 SHA512:1da77c67a3c2e779c8b84174fb240f7738751230a33fcfe06959a9013bfb07ea25d36d7886b968b6b93469ebc78d97c098e65e14ba725fa1930a7d589cf8c98f
'http://archive.ubuntu.com/ubuntu/pool/main/s/speex/speex_1.2.1-2ubuntu2.24.04.1.debian.tar.xz' speex_1.2.1-2ubuntu2.24.04.1.debian.tar.xz 11120 SHA512:f6112fbdb31db90f12a475b5861cfce55cc17b0d4b4cd2ff637f1fa71e027c8e20a1231e7dedaf88c40c753a786eb139949d8e0e28c635ec0bff6ee8657c1be8
```

### `dpkg` source package: `sphinx=7.2.6-6`

Binary Packages:

- `libjs-sphinxdoc=7.2.6-6`

Licenses: (parsed from: `/usr/share/doc/libjs-sphinxdoc/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sphinx/7.2.6-6/


### `dpkg` source package: `sqlite3=3.45.1-1ubuntu2.5`

Binary Packages:

- `libsqlite3-0:amd64=3.45.1-1ubuntu2.5`
- `libsqlite3-dev:amd64=3.45.1-1ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.45.1-1ubuntu2.5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.dsc' sqlite3_3.45.1-1ubuntu2.5.dsc 2601 SHA512:fb56794498668ca451db41d705708b505877abaa88f4bd36b47d7642f3f9513fb3597c77517e05dd821c90a341de8c032c3f7f39ebdc40a33b99a1802f51907a
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig-www.tar.xz' sqlite3_3.45.1.orig-www.tar.xz 5693812 SHA512:dbbf32bad3912dca4d1d3366053c66dc53745d4e5c6892c10470b7452f338de03eee1406cb6c5a972c9890bd71a7b30563e4863f27bf0f2813a92ffdfd95832f
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig.tar.xz' sqlite3_3.45.1.orig.tar.xz 8257884 SHA512:8ea4a50fe730b072271978bbeee074d567bc8cbaa3bb4a8b8802e012d470fd482d800532eedea48a54fd64785f3b02aab7b033c8e2767a5e8b9f02a9cc844b80
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz' sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz 35260 SHA512:a031e8f6aeefbb9ea45439a24dc82f9e74b12c3e92b6444057648cc07187c00a0ca6cf32a6c51c0e50787f41d525c687cc3dad7492b46d785fa1088b04d10ea1
```

### `dpkg` source package: `srt=1.5.3-1build2`

Binary Packages:

- `libsrt1.5-gnutls:amd64=1.5.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libsrt1.5-gnutls/copyright`)

- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-2.0`
- `Zlib`
- `unlicense`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sudo=1.9.15p5-3ubuntu5.24.04.1`

Binary Packages:

- `sudo=1.9.15p5-3ubuntu5.24.04.1`

Licenses: (parsed from: `/usr/share/doc/sudo/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `Zlib`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sudo=1.9.15p5-3ubuntu5.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5-3ubuntu5.24.04.1.dsc' sudo_1.9.15p5-3ubuntu5.24.04.1.dsc 2763 SHA512:13b69793dfb87be6cda062f3bb6834e7515bd3159ad32180e83c0cb8afbc58d43b683fb5b75d3c120fee22272d1703b4bad8227124d3f6c00303366d4b9713ee
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5.orig.tar.gz' sudo_1.9.15p5.orig.tar.gz 5306611 SHA512:ebac69719de2fe7bd587924701bdd24149bf376a68b17ec02f69b2b96d4bb6fa5eb8260a073ec5ea046d3ac69bb5b1c0b9d61709fe6a56f1f66e40817a70b15a
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5.orig.tar.gz.asc' sudo_1.9.15p5.orig.tar.gz.asc 833 SHA512:2447b8b660d8902594a9e809cd96fef8c6074223ced086c1a81453fbe509c387f48f6c2817c802c7d7f3225fcea2539a0e420a4fb120384de5535abec8d60f34
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5-3ubuntu5.24.04.1.debian.tar.xz' sudo_1.9.15p5-3ubuntu5.24.04.1.debian.tar.xz 70264 SHA512:966c349d788dfff7421eff8287cecae8809bad01f331198e27804c45807968aeafb28bbeae75d2a9187f59777018a1a336381121b7b846e0f59ec0e133906b90
```

### `dpkg` source package: `superlu=6.0.1+dfsg1-1build1`

Binary Packages:

- `libsuperlu-dev:amd64=6.0.1+dfsg1-1build1`
- `libsuperlu6:amd64=6.0.1+dfsg1-1build1`

Licenses: (parsed from: `/usr/share/doc/libsuperlu-dev/copyright`, `/usr/share/doc/libsuperlu6/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `permissive`
- `permissive-colamd`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `svt-av1=1.7.0+dfsg-2build1`

Binary Packages:

- `libsvtav1enc1d1:amd64=1.7.0+dfsg-2build1`

Licenses: (parsed from: `/usr/share/doc/libsvtav1enc1d1/copyright`)

- `BSD-2-clause`
- `BSD-3-Clause-Clear`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `systemd=255.4-1ubuntu8.12`

Binary Packages:

- `libpam-systemd:amd64=255.4-1ubuntu8.12`
- `libsystemd-shared:amd64=255.4-1ubuntu8.12`
- `libsystemd0:amd64=255.4-1ubuntu8.12`
- `libudev1:amd64=255.4-1ubuntu8.12`
- `systemd=255.4-1ubuntu8.12`
- `systemd-dev=255.4-1ubuntu8.12`
- `systemd-sysv=255.4-1ubuntu8.12`

Licenses: (parsed from: `/usr/share/doc/libpam-systemd/copyright`, `/usr/share/doc/libsystemd-shared/copyright`, `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`, `/usr/share/doc/systemd/copyright`, `/usr/share/doc/systemd-dev/copyright`, `/usr/share/doc/systemd-sysv/copyright`)

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
$ apt-get source -qq --print-uris systemd=255.4-1ubuntu8.12
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.12.dsc' systemd_255.4-1ubuntu8.12.dsc 7324 SHA512:ff1c3392b079861cdfdb41e0624166d6a7e0459b7e2a7ce13fdc0814c5d593e3ceba6c73e53c6ab617fb455d8fe07904c55c0081a1d94d1e40e3c3b3667eb321
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4.orig.tar.gz' systemd_255.4.orig.tar.gz 14952427 SHA512:8a2bde11a55f7f788ba7751789a5e9be6ce9634e88d54e49f6e832c4c49020c6cacaf2a610fe26f92998b0cbf43c6c2150a96b2c0953d23261009f57d71ea979
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.12.debian.tar.xz' systemd_255.4-1ubuntu8.12.debian.tar.xz 257724 SHA512:0394efde0f11cee00b37b232373e400ef1a3cae666fbbab6c732fe4de241ef32b588619bdfd1101be9752370d16958505ea42c8ac5681d1448c780faa0233227
```

### `dpkg` source package: `sysvinit=3.08-6ubuntu3`

Binary Packages:

- `sysvinit-utils=3.08-6ubuntu3`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tar=1.35+dfsg-3build1`

Binary Packages:

- `tar=1.35+dfsg-3build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tcl8.6=8.6.14+dfsg-1build1`

Binary Packages:

- `libtcl8.6:amd64=8.6.14+dfsg-1build1`
- `tcl8.6=8.6.14+dfsg-1build1`
- `tcl8.6-dev:amd64=8.6.14+dfsg-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tcltk-defaults=8.6.14build1`

Binary Packages:

- `tcl=8.6.14build1`
- `tcl-dev:amd64=8.6.14build1`
- `tk=8.6.14build1`
- `tk-dev:amd64=8.6.14build1`

Licenses: (parsed from: `/usr/share/doc/tcl/copyright`, `/usr/share/doc/tcl-dev/copyright`, `/usr/share/doc/tk/copyright`, `/usr/share/doc/tk-dev/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tesseract=5.3.4-1build5`

Binary Packages:

- `libtesseract5:amd64=5.3.4-1build5`

Licenses: (parsed from: `/usr/share/doc/libtesseract5/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tiff=4.5.1+git230720-4ubuntu2.4`

Binary Packages:

- `libtiff-dev:amd64=4.5.1+git230720-4ubuntu2.4`
- `libtiff6:amd64=4.5.1+git230720-4ubuntu2.4`
- `libtiffxx6:amd64=4.5.1+git230720-4ubuntu2.4`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-4ubuntu2.4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu2.4.dsc' tiff_4.5.1+git230720-4ubuntu2.4.dsc 2488 SHA512:ee2188d0a1e0fa447ac5bfe8ac86aa6989081c78a5204b9f8dd1e890249cf7b74f46d69e9ff64e249ba583065c7918cbdba366f57a0a384c4815f3bb059bfe8c
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA512:6bf9653f5c65d17c2944b20d14a5d5ab3b89d461bc6eb935a54aa8df99ce7221aeb2172f06b44affd06d81aeaab5698b90b07fde883167d0abf51debaaa6f71b
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu2.4.debian.tar.xz' tiff_4.5.1+git230720-4ubuntu2.4.debian.tar.xz 32700 SHA512:e1452bc15b6212755b9e5e5fb4f7e15b28f7506a08cfb17ae3b1931174af229f459f4fb02dc0bd07c7faded43d3e59744c2dd6659ad188b8874ed4e90a7ae09b
```

### `dpkg` source package: `tinyxml2=10.0.0+dfsg-2`

Binary Packages:

- `libtinyxml2-10:amd64=10.0.0+dfsg-2`
- `libtinyxml2-dev:amd64=10.0.0+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libtinyxml2-10/copyright`, `/usr/share/doc/libtinyxml2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `zlib/libpng`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tinyxml2/10.0.0+dfsg-2/


### `dpkg` source package: `tinyxml=2.6.2-6.1`

Binary Packages:

- `libtinyxml2.6.2v5:amd64=2.6.2-6.1`

Licenses: (parsed from: `/usr/share/doc/libtinyxml2.6.2v5/copyright`)

- `ZLIB`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tinyxml/2.6.2-6.1/


### `dpkg` source package: `tk8.6=8.6.14-1build1`

Binary Packages:

- `libtk8.6:amd64=8.6.14-1build1`
- `tk8.6=8.6.14-1build1`
- `tk8.6-dev:amd64=8.6.14-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `twolame=0.4.0-2build3`

Binary Packages:

- `libtwolame0:amd64=0.4.0-2build3`

Licenses: (parsed from: `/usr/share/doc/libtwolame0/copyright`)

- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tzdata=2025b-0ubuntu0.24.04.1`

Binary Packages:

- `tzdata=2025b-0ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-0ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.24.04.1.dsc' tzdata_2025b-0ubuntu0.24.04.1.dsc 2728 SHA512:e717b51a15bbdd64183841b5136194f75bc2affece27101e3d03ed5b4614959a7810d7e1cfc8e59d846fe87dec7ed01c1cc739a25a0abf95552215f0929ea318
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA512:7d83741f3cae81fac8131994b43c55b6da7328df18b706e5ee40e9b3212bc506e6f8fc90988b18da424ed59eff69bce593f2783b7b5f18eb483a17aeb94258d6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA512:ad39fe16b32fad7eee27ff968b4e8af23267ce586629ad70e7625136d2c3cc3a42295a87b3dc770c291aa9112c56301629c1fe379735f70008e62864ce4e735a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.24.04.1.debian.tar.xz' tzdata_2025b-0ubuntu0.24.04.1.debian.tar.xz 188052 SHA512:8120a6b7f4381ce8f5e67b58f0cdc144905c8eed387c5b3ea820c19464308b0b2c9010ad498fe69e5161f4c23ccba78ee7f6d9dc7ac0caa23b18509ea4d8dad4
```

### `dpkg` source package: `ubuntu-keyring=2023.11.28.1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ubuntu-themes=24.04-0ubuntu1`

Binary Packages:

- `ubuntu-mono=24.04-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-mono/copyright`)

- `CC-BY-SA-3.0`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ucx=1.16.0+ds-5ubuntu1`

Binary Packages:

- `libucx0:amd64=1.16.0+ds-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libucx0/copyright`)

- `BSD-3-Clause`
- `FSF-Free`
- `Google-3-BSD`
- `Public-Domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `uncrustify=0.78.1+dfsg1-1`

Binary Packages:

- `uncrustify=0.78.1+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/uncrustify/copyright`)

- `Artistic`
- `GPL`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/uncrustify/0.78.1+dfsg1-1/


### `dpkg` source package: `underscore=1.13.4~dfsg+~1.11.4-3`

Binary Packages:

- `libjs-underscore=1.13.4~dfsg+~1.11.4-3`

Licenses: (parsed from: `/usr/share/doc/libjs-underscore/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/underscore/1.13.4~dfsg+~1.11.4-3/


### `dpkg` source package: `unixodbc=2.3.12-1ubuntu0.24.04.1`

Binary Packages:

- `libodbc2:amd64=2.3.12-1ubuntu0.24.04.1`
- `libodbccr2:amd64=2.3.12-1ubuntu0.24.04.1`
- `libodbcinst2:amd64=2.3.12-1ubuntu0.24.04.1`
- `unixodbc-common=2.3.12-1ubuntu0.24.04.1`
- `unixodbc-dev:amd64=2.3.12-1ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libodbc2/copyright`, `/usr/share/doc/libodbccr2/copyright`, `/usr/share/doc/libodbcinst2/copyright`, `/usr/share/doc/unixodbc-common/copyright`, `/usr/share/doc/unixodbc-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `ppowell`

Source:

```console
$ apt-get source -qq --print-uris unixodbc=2.3.12-1ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unixodbc/unixodbc_2.3.12-1ubuntu0.24.04.1.dsc' unixodbc_2.3.12-1ubuntu0.24.04.1.dsc 2346 SHA512:083cbd9f20a05b5eb97cce76b18c679ac41423817dcdea1e0bf63e89c41f7e071cdf461af32fbd9f57ff362fa689bba630157279953fe77aa844a5c3d82b95ba
'http://archive.ubuntu.com/ubuntu/pool/main/u/unixodbc/unixodbc_2.3.12.orig.tar.gz' unixodbc_2.3.12.orig.tar.gz 866774 SHA512:f0c0a995c90ff3abd00a031430e2f2034d45ca96c7fba34adc826a668c4eeb77ee2e1be27b7b1817c706f43df4fa434746362e746a39e779256e006deeb790c7
'http://archive.ubuntu.com/ubuntu/pool/main/u/unixodbc/unixodbc_2.3.12-1ubuntu0.24.04.1.debian.tar.xz' unixodbc_2.3.12-1ubuntu0.24.04.1.debian.tar.xz 17644 SHA512:a1c6e2d3a8746fdf3f692c64baa589cf8994ac72eb7a5e86bdd625d56ba45c069ed6fd3bc3d20ae5fc7608634a8820f5463687b331ac2c38404af124ed273510
```

### `dpkg` source package: `unminimize=0.2.1`

Binary Packages:

- `unminimize=0.2.1`

Licenses: (parsed from: `/usr/share/doc/unminimize/copyright`)

- `GPL-2`
- `GPL-2.0+`

Source:

```console
$ apt-get source -qq --print-uris unminimize=0.2.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unminimize/unminimize_0.2.1.dsc' unminimize_0.2.1.dsc 1554 SHA512:28b51904aaf6edb27c93d250e5b91caa1d39ff749e059be036be4bf8ff710ee9812b5080c678b155db45dfbbb01dd30ea7908728aa5d0129108aa630db1c2aef
'http://archive.ubuntu.com/ubuntu/pool/main/u/unminimize/unminimize_0.2.1.tar.xz' unminimize_0.2.1.tar.xz 9400 SHA512:692ed9d0bb2d42ab5c74ef0f4c86d8f5922e4d1ee9d8efa8a03490437aff35c13b0114f7a62aa5464e95d4014db2745605a83fe7d9bfc81977de8ad56e3e901e
```

### `dpkg` source package: `uriparser=0.9.7+dfsg-2build1`

Binary Packages:

- `liburiparser-dev=0.9.7+dfsg-2build1`
- `liburiparser1:amd64=0.9.7+dfsg-2build1`

Licenses: (parsed from: `/usr/share/doc/liburiparser-dev/copyright`, `/usr/share/doc/liburiparser1/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ust=2.13.7-1.1ubuntu2`

Binary Packages:

- `liblttng-ust-common1t64:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust-ctl5t64:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust-dev:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust-python-agent1t64:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust1t64:amd64=2.13.7-1.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblttng-ust-common1t64/copyright`, `/usr/share/doc/liblttng-ust-ctl5t64/copyright`, `/usr/share/doc/liblttng-ust-dev/copyright`, `/usr/share/doc/liblttng-ust-python-agent1t64/copyright`, `/usr/share/doc/liblttng-ust1t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `utfcpp=3.2.5+really3.2.4-1`

Binary Packages:

- `libutfcpp-dev=3.2.5+really3.2.4-1`

Licenses: (parsed from: `/usr/share/doc/libutfcpp-dev/copyright`)

- `BSL-1.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/utfcpp/3.2.5+really3.2.4-1/


### `dpkg` source package: `util-linux=2.39.3-9ubuntu6.4`

Binary Packages:

- `bsdutils=1:2.39.3-9ubuntu6.4`
- `libblkid1:amd64=2.39.3-9ubuntu6.4`
- `libfdisk1:amd64=2.39.3-9ubuntu6.4`
- `libmount1:amd64=2.39.3-9ubuntu6.4`
- `libsmartcols1:amd64=2.39.3-9ubuntu6.4`
- `libuuid1:amd64=2.39.3-9ubuntu6.4`
- `mount=2.39.3-9ubuntu6.4`
- `util-linux=2.39.3-9ubuntu6.4`
- `uuid-dev:amd64=2.39.3-9ubuntu6.4`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libfdisk1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

- `BSD-3-clause`
- `BSD-4-clause`
- `BSLA`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.39.3-9ubuntu6.4
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.4.dsc' util-linux_2.39.3-9ubuntu6.4.dsc 4755 SHA512:600d87df4b7d5484d1313e12d57f5691266becd893b4818ef7da4471939138d67d0e8aad624c61ba36afa351b764dfadfdff60eb26d8005721e530b9ad342f2d
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3.orig.tar.xz' util-linux_2.39.3.orig.tar.xz 8526168 SHA512:a2de1672f06ca5d2d431db1265a8499808770c3781019ec4a3a40170df4685826d8e3ca120841dcc5df4681ca8c935a993317bd0dc70465b21bf8e0efef65afa
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.4.debian.tar.xz' util-linux_2.39.3-9ubuntu6.4.debian.tar.xz 146780 SHA512:3a86146601d3d0a1b39fc6bc899d570cc11f65e214ab3e33f1286c7a8ffdaaef9537ea946f6618571eb32f7bc207087ac55f82bfc5fbdec3e63d7d3c21023ead
```

### `dpkg` source package: `vtk9=9.1.0+really9.1.0+dfsg2-7.1build3`

Binary Packages:

- `libvtk9-dev=9.1.0+really9.1.0+dfsg2-7.1build3`
- `libvtk9-java=9.1.0+really9.1.0+dfsg2-7.1build3`
- `libvtk9-qt-dev:amd64=9.1.0+really9.1.0+dfsg2-7.1build3`
- `libvtk9.1t64:amd64=9.1.0+really9.1.0+dfsg2-7.1build3`
- `libvtk9.1t64-qt:amd64=9.1.0+really9.1.0+dfsg2-7.1build3`
- `python3-vtk9=9.1.0+really9.1.0+dfsg2-7.1build3`
- `vtk9=9.1.0+really9.1.0+dfsg2-7.1build3`

Licenses: (parsed from: `/usr/share/doc/libvtk9-dev/copyright`, `/usr/share/doc/libvtk9-java/copyright`, `/usr/share/doc/libvtk9-qt-dev/copyright`, `/usr/share/doc/libvtk9.1t64/copyright`, `/usr/share/doc/libvtk9.1t64-qt/copyright`, `/usr/share/doc/python3-vtk9/copyright`, `/usr/share/doc/vtk9/copyright`)

- `Apache-2`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-notice`
- `BSD-3-clause-notice-2`
- `BSD-like`
- `BSL-1`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `MIT`
- `MIT-exception`
- `Zlib`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `vulkan-loader=1.3.275.0-1build1`

Binary Packages:

- `libvulkan-dev:amd64=1.3.275.0-1build1`
- `libvulkan1:amd64=1.3.275.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libvulkan-dev/copyright`, `/usr/share/doc/libvulkan1/copyright`)

- `Apache-2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `wayland=1.22.0-2.1build1`

Binary Packages:

- `libwayland-client0:amd64=1.22.0-2.1build1`
- `libwayland-cursor0:amd64=1.22.0-2.1build1`
- `libwayland-egl1:amd64=1.22.0-2.1build1`
- `libwayland-server0:amd64=1.22.0-2.1build1`

Licenses: (parsed from: `/usr/share/doc/libwayland-client0/copyright`, `/usr/share/doc/libwayland-cursor0/copyright`, `/usr/share/doc/libwayland-egl1/copyright`, `/usr/share/doc/libwayland-server0/copyright`)

- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `woff2=1.0.2-2build1`

Binary Packages:

- `libwoff1:amd64=1.0.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libwoff1/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `x264=2:0.164.3108+git31e19f9-1`

Binary Packages:

- `libx264-164:amd64=2:0.164.3108+git31e19f9-1`

Licenses: (parsed from: `/usr/share/doc/libx264-164/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with other exception`
- `ISC`
- `LGPL-2.1+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/x264/2:0.164.3108+git31e19f9-1/


### `dpkg` source package: `x265=3.5-2build1`

Binary Packages:

- `libx265-199:amd64=3.5-2build1`
- `libx265-dev:amd64=3.5-2build1`

Licenses: (parsed from: `/usr/share/doc/libx265-199/copyright`, `/usr/share/doc/libx265-dev/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xcb-util-image=0.4.0-2build1`

Binary Packages:

- `libxcb-image0:amd64=0.4.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libxcb-image0/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT/X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xcb-util-keysyms=0.4.0-1build4`

Binary Packages:

- `libxcb-keysyms1:amd64=0.4.0-1build4`

Licenses: (parsed from: `/usr/share/doc/libxcb-keysyms1/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT/X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xcb-util-renderutil=0.3.9-1build4`

Binary Packages:

- `libxcb-render-util0:amd64=0.3.9-1build4`

Licenses: (parsed from: `/usr/share/doc/libxcb-render-util0/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT/X Consortium License`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xcb-util-wm=0.4.1-1.1build3`

Binary Packages:

- `libxcb-icccm4:amd64=0.4.1-1.1build3`

Licenses: (parsed from: `/usr/share/doc/libxcb-icccm4/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT/X Consortium License`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xcb-util=0.4.0-1build3`

Binary Packages:

- `libxcb-util1:amd64=0.4.0-1build3`

Licenses: (parsed from: `/usr/share/doc/libxcb-util1/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xerces-c=3.2.4+debian-1.2ubuntu2`

Binary Packages:

- `libxerces-c-dev:amd64=3.2.4+debian-1.2ubuntu2`
- `libxerces-c3.2t64:amd64=3.2.4+debian-1.2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libxerces-c-dev/copyright`, `/usr/share/doc/libxerces-c3.2t64/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-2+ with Autoconf exception`
- `GPL-2+ with Libtool exception`
- `GPL-3`
- `GPL-3+ with Autoconf exception`
- `X11-install-sh`
- `permissive-configure`
- `permissive-fsf`
- `xerces-Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xft=2.3.6-1build1`

Binary Packages:

- `libxft-dev:amd64=2.3.6-1build1`
- `libxft2:amd64=2.3.6-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xkeyboard-config=2.41-2ubuntu1.1`

Binary Packages:

- `xkb-data=2.41-2ubuntu1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xkeyboard-config=2.41-2ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xkeyboard-config/xkeyboard-config_2.41-2ubuntu1.1.dsc' xkeyboard-config_2.41-2ubuntu1.1.dsc 2227 SHA512:ef3b993097b5eecada8dd5b321e88e7b1476bd6b8f2b18050f30d31342cfbd6f36f8cd3db3ff66d2f97110d84ee1e94488d2cee47ed9a78c9e0fea5dedb2f7c4
'http://archive.ubuntu.com/ubuntu/pool/main/x/xkeyboard-config/xkeyboard-config_2.41.orig.tar.gz' xkeyboard-config_2.41.orig.tar.gz 1697731 SHA512:16b039683e41c1b10ebca4dda49bdb4f6346561b21c820fee81d002b78e0f08b1e23a713fb546d60200e2a74f51f86a1221b9e164e696e787cc2467694cd6a9a
'http://archive.ubuntu.com/ubuntu/pool/main/x/xkeyboard-config/xkeyboard-config_2.41-2ubuntu1.1.diff.gz' xkeyboard-config_2.41-2ubuntu1.1.diff.gz 43597 SHA512:ae1823a7dcf2ec759533cb87d91793982654e4175139887549890840e0398875754a67a61a3e3735f934ea947fbd146c798c023165e64f41da13cc30837e6319
```

### `dpkg` source package: `xml-core=0.19`

Binary Packages:

- `xml-core=0.19`

Licenses: (parsed from: `/usr/share/doc/xml-core/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xml-core/0.19/


### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1.1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xorg-sgml-doctools/1:1.11-1.1/


### `dpkg` source package: `xorg=1:7.7+23ubuntu3`

Binary Packages:

- `x11-common=1:7.7+23ubuntu3`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xorgproto=2023.2-1`

Binary Packages:

- `x11proto-dev=2023.2-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xorgproto/2023.2-1/


### `dpkg` source package: `xtrans=1.4.0-1`

Binary Packages:

- `xtrans-dev=1.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xtrans/1.4.0-1/


### `dpkg` source package: `xvidcore=2:1.3.7-1build1`

Binary Packages:

- `libxvidcore4:amd64=2:1.3.7-1build1`

Licenses: (parsed from: `/usr/share/doc/libxvidcore4/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xxhash=0.8.2-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xz-utils=5.6.1+really5.4.5-1ubuntu0.2`

Binary Packages:

- `liblzma-dev:amd64=5.6.1+really5.4.5-1ubuntu0.2`
- `liblzma5:amd64=5.6.1+really5.4.5-1ubuntu0.2`
- `xz-utils=5.6.1+really5.4.5-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/liblzma-dev/copyright`, `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

- `Autoconf`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `config-h`
- `noderivs`
- `none`
- `permissive-fsf`
- `permissive-nowarranty`
- `probably-PD`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.6.1+really5.4.5-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.dsc' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.dsc 2639 SHA512:b10ba1ba72e3f1ea6c12b5d1f84bf21b2651e5e796d35b821c14370ecb65953a02e32e3d5f21587191e5b62757b34ae0af2ba64b399670b4c4fd46e04b9b7811
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5.orig.tar.xz' xz-utils_5.6.1+really5.4.5.orig.tar.xz 1680520 SHA512:5cbc3b5bb35a9f5773ad657788fe77013471e3b621c5a8149deb7389d48535926e5bed103456fcfe5ecb044b236b1055b03938a6cc877cfc749372b899fc79e5
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.debian.tar.xz' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.debian.tar.xz 30776 SHA512:1891c935b3915749aaa4f29b494c3d3156dd7a04b4637148d6a668ab5fb464a0bd2be441108750e5601244921f38e47c2d25490cf07d0066da566e5d36756582
```

### `dpkg` source package: `yaml-cpp=0.8.0+dfsg-6build1`

Binary Packages:

- `libyaml-cpp-dev:amd64=0.8.0+dfsg-6build1`
- `libyaml-cpp0.8:amd64=0.8.0+dfsg-6build1`

Licenses: (parsed from: `/usr/share/doc/libyaml-cpp-dev/copyright`, `/usr/share/doc/libyaml-cpp0.8/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zeromq3=4.3.5-1build2`

Binary Packages:

- `libzmq5:amd64=4.3.5-1build2`

Licenses: (parsed from: `/usr/share/doc/libzmq5/copyright`)

- `LGPL-2`
- `LGPL-2.0+`
- `MIT`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zlib=1:1.3.dfsg-3.1ubuntu2.1`

Binary Packages:

- `libminizip-dev:amd64=1:1.3.dfsg-3.1ubuntu2.1`
- `libminizip1t64:amd64=1:1.3.dfsg-3.1ubuntu2.1`
- `zlib1g:amd64=1:1.3.dfsg-3.1ubuntu2.1`
- `zlib1g-dev:amd64=1:1.3.dfsg-3.1ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libminizip-dev/copyright`, `/usr/share/doc/libminizip1t64/copyright`, `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3.1ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.dsc' zlib_1.3.dfsg-3.1ubuntu2.1.dsc 3116 SHA512:5cf00ba3f81611c9e94321e524dfcbbe19b7f7d8570e0bc15da334ecf72d212cc22366659ed5ede3e1716ba1ebd2e05c65663e64f1e283fb1f84a3956fd2f4c3
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA512:be6f020c691c61fe4ddcb27d3f8b2515435f544177e0b97286b5e85afc3862c1de6cd74a14ff6b065d620d046d35bf029fabfd1cf473f43a2cad60bf9ad55afe
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz' zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz 61028 SHA512:18f491ffac55e6f9464befc89bbe3067030dfd30d8093c06cd7aa511e4534123b87cecf8f2dde4c7447c77de7965b488de6f407637b4a1ace2f55afc0adae170
```

### `dpkg` source package: `zvbi=0.2.42-2`

Binary Packages:

- `libzvbi-common=0.2.42-2`
- `libzvbi0t64:amd64=0.2.42-2`

Licenses: (parsed from: `/usr/share/doc/libzvbi-common/copyright`, `/usr/share/doc/libzvbi0t64/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/zvbi/0.2.42-2/

