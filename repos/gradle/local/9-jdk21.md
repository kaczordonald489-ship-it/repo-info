# `gradle:9.2.1-jdk21`

## Docker Metadata

- Image ID: `sha256:3726866a1ffbd6955790133d357d8092b7ce3eadbc93923883bcf3d60cb1206c`
- Created: `2025-11-17T19:59:13.153325652Z`
- Virtual Size: ~ 791.80 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/__cacert_entrypoint.sh"]`
- Command: `["gradle"]`
- Environment:
  - `PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-21.0.9+10`
  - `GRADLE_HOME=/opt/gradle`
  - `GRADLE_VERSION=9.2.1`
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


### `dpkg` source package: `apr-util=1.6.3-1.1ubuntu7`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-1.1ubuntu7`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `apr=1.7.2-3.1ubuntu0.1`

Binary Packages:

- `libapr1t64:amd64=1.7.2-3.1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.2-3.1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.1ubuntu0.1.dsc' apr_1.7.2-3.1ubuntu0.1.dsc 1808 SHA512:429a77d6c512856fad8593d2484f60f25877003b46696467a721a99bc3308335619e41412446a4c147aa4f8cd039df4084cca6261bf63ec0b9e21cb22242d318
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2' apr_1.7.2.orig.tar.bz2 890218 SHA512:0a3a27ccc97bbe4865c1bc0b803012e3da6d5b1f17d4fb0da6f5f58eec01f6d2ae1f25e52896ea5f9c5ac04c5fddcfd1ac606b301c322cf40d5c4d4ce0a1b76e
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2.asc' apr_1.7.2.orig.tar.bz2.asc 833 SHA512:77da1e516b30032419b36da8453f56c6149ad18631772613adb095b6eccb7606dc51589d33d422572d3fcefe8f6129bfbb06d0ab7fde5848d873856f4ed93940
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.1ubuntu0.1.debian.tar.xz' apr_1.7.2-3.1ubuntu0.1.debian.tar.xz 55364 SHA512:3d5aa043c300f8e505f1ac00d543710b3945638587cd39dad94519f61305270276866549523c0df4d1c962c2dde0a07e01a0da93f5a9399e7a194a25618ef63a
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


### `dpkg` source package: `binutils=2.42-4ubuntu2.6`

Binary Packages:

- `binutils=2.42-4ubuntu2.6`
- `binutils-common:amd64=2.42-4ubuntu2.6`
- `binutils-x86-64-linux-gnu=2.42-4ubuntu2.6`
- `libbinutils:amd64=2.42-4ubuntu2.6`
- `libctf-nobfd0:amd64=2.42-4ubuntu2.6`
- `libctf0:amd64=2.42-4ubuntu2.6`
- `libgprofng0:amd64=2.42-4ubuntu2.6`
- `libsframe1:amd64=2.42-4ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.42-4ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.6.dsc' binutils_2.42-4ubuntu2.6.dsc 10148 SHA512:9b5f805529b5aa0daefe004546184133989d04322017d7009c7bb39bb0a1c03f5e53f950763c27fb68c2b3c90337e29b2d640febaa34e55f187e63926f80a2cf
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42.orig.tar.xz' binutils_2.42.orig.tar.xz 27567160 SHA512:155f3ba14cd220102f4f29a4f1e5cfee3c48aa03b74603460d05afb73c70d6657a9d87eee6eb88bf13203fe6f31177a5c9addc04384e956e7da8069c8ecd20a6
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.6.debian.tar.xz' binutils_2.42-4ubuntu2.6.debian.tar.xz 187016 SHA512:4209ef77a41d474615c39305ca7b3a29981ce60f0554658867b59861be484c28121c68bdd9093782e94c2b0b62380efc0696c7510a4c745c183e6bba1ade43a1
```

### `dpkg` source package: `breezy=3.3.5-6build2`

Binary Packages:

- `brz=3.3.5-6build2`
- `python3-breezy=3.3.5-6build2`

Licenses: (parsed from: `/usr/share/doc/brz/copyright`, `/usr/share/doc/python3-breezy/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bzip2=1.0.8-5.1build0.1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5.1build0.1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5.1build0.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.dsc' bzip2_1.0.8-5.1build0.1.dsc 2220 SHA512:1233c3065a9355482c826f35f7859450a868a6e98ef7793dcc1ae68d68360c840ed8bd21af872501d36803c10b9b2516556e8bb716f3d0ff5cdaa877a1ab95df
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.debian.tar.bz2' bzip2_1.0.8-5.1build0.1.debian.tar.bz2 26927 SHA512:ee39a01bcd6b31d70b3dfaa14bf7f943cb3711d073569cf9e35092062742077801ca287425c855a499114335748f2f791a7ff07eb502f2601a3d58f5041e7413
```

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


### `dpkg` source package: `configobj=5.0.8-3`

Binary Packages:

- `python3-configobj=5.0.8-3`

Licenses: (parsed from: `/usr/share/doc/python3-configobj/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/configobj/5.0.8-3/


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

### `dpkg` source package: `curl=8.5.0-2ubuntu10.6`

Binary Packages:

- `curl=8.5.0-2ubuntu10.6`
- `libcurl3t64-gnutls:amd64=8.5.0-2ubuntu10.6`
- `libcurl4t64:amd64=8.5.0-2ubuntu10.6`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

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


### `dpkg` source package: `dpkg=1.22.6ubuntu6.5`

Binary Packages:

- `dpkg=1.22.6ubuntu6.5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.6ubuntu6.5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.dsc' dpkg_1.22.6ubuntu6.5.dsc 3156 SHA512:6c6f43612ac5f74937a2a83525ebb66a21af81e4678fd2b3bafbcb490e0e33be6a611b1475c205de378b64efdf7c615abd46b78c58b6c232145e7d2b75fe9d7b
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.tar.xz' dpkg_1.22.6ubuntu6.5.tar.xz 5547360 SHA512:a52c556b632205b84bf8e795f68f54fe7e78b251561d032be76ecde9c5e3d9a74c5358476956ab8c3b2fb0266a5f4a03f3d67ec7039e62dc56905ee8c52d2d5d
```

### `dpkg` source package: `dulwich=0.21.6-1build2`

Binary Packages:

- `python3-dulwich=0.21.6-1build2`

Licenses: (parsed from: `/usr/share/doc/python3-dulwich/copyright`)

- `Apache-2`
- `Apache-2.0`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `expat=2.6.1-2ubuntu0.3`

Binary Packages:

- `libexpat1:amd64=2.6.1-2ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.1-2ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.3.dsc' expat_2.6.1-2ubuntu0.3.dsc 1474 SHA512:2331ab71158152f87fffa9e05e04b6f79bbeee7842cd957e3237847684b3508fb193850ca47049f1ed3284cc54d553183d9886de595a5ada114da20bf0119c69
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1.orig.tar.gz' expat_2.6.1.orig.tar.gz 8414649 SHA512:cf6c64fc0ca55dd172ca8a6ca10d1fb2c915d0f941b0068f42cb90488022dea73e04119c49a1bd4ab9a5d425ddc132ae5f22260ff6d2e25204637a1169e7bd4f
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.3.debian.tar.xz' expat_2.6.1-2ubuntu0.3.debian.tar.xz 30100 SHA512:9b71cdafaacb1148f3e22cef6bde49f2701339a15c78ccf0df954c19bdba6b6f8ee778ab2227c8543f75bcc8b6e5f8e380e99d6d0c7ea4660526669e4d97df0e
```

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


### `dpkg` source package: `fontconfig=2.15.0-1.1ubuntu2`

Binary Packages:

- `fontconfig=2.15.0-1.1ubuntu2`
- `fontconfig-config=2.15.0-1.1ubuntu2`
- `libfontconfig1:amd64=2.15.0-1.1ubuntu2`

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

- `libfreetype6:amd64=2.13.2+dfsg-1build3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2~24.04`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-4ubuntu2~24.04`
- `libgcc-s1:amd64=14.2.0-4ubuntu2~24.04`
- `libstdc++6:amd64=14.2.0-4ubuntu2~24.04`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

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


### `dpkg` source package: `git-lfs=3.4.1-1ubuntu0.3`

Binary Packages:

- `git-lfs=3.4.1-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/git-lfs/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris git-lfs=3.4.1-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/universe/g/git-lfs/git-lfs_3.4.1-1ubuntu0.3.dsc' git-lfs_3.4.1-1ubuntu0.3.dsc 2785 SHA512:1500b4de4ce4d9890aa573e51bda030459d445ac2f82b7a0d9b3667dea642371023ead21490792e5525a11a644e6d51a4788cce44786a98dc82c6fe25dbe9c88
'http://archive.ubuntu.com/ubuntu/pool/universe/g/git-lfs/git-lfs_3.4.1.orig.tar.gz' git-lfs_3.4.1.orig.tar.gz 674163 SHA512:ef30b7906548594edf28e75046bb78f70043d0363390ec3a241fc2ff7790b0f6ab1869b8a6b10d13a4cbcd559db7ea51aa4c1d64e75707357b84f1ddc0f7095c
'http://archive.ubuntu.com/ubuntu/pool/universe/g/git-lfs/git-lfs_3.4.1-1ubuntu0.3.debian.tar.xz' git-lfs_3.4.1-1ubuntu0.3.debian.tar.xz 4756 SHA512:da054387f81a7fed3eb997dcd01c235befbb349a35aa548b7ab3d436cd0d4b83d6bfb144e86f6d9f962437ea255b71b02cd294866e43f62c9c1f35765ad51ef7
```

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

### `dpkg` source package: `glibc=2.39-0ubuntu8.6`

Binary Packages:

- `libc-bin=2.39-0ubuntu8.6`
- `libc6:amd64=2.39-0ubuntu8.6`
- `locales=2.39-0ubuntu8.6`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/locales/copyright`)

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

### `dpkg` source package: `gnupg2=2.4.4-2ubuntu17.3`

Binary Packages:

- `dirmngr=2.4.4-2ubuntu17.3`
- `gnupg=2.4.4-2ubuntu17.3`
- `gnupg-utils=2.4.4-2ubuntu17.3`
- `gpg=2.4.4-2ubuntu17.3`
- `gpg-agent=2.4.4-2ubuntu17.3`
- `gpgconf=2.4.4-2ubuntu17.3`
- `gpgsm=2.4.4-2ubuntu17.3`
- `gpgv=2.4.4-2ubuntu17.3`
- `keyboxd=2.4.4-2ubuntu17.3`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`, `/usr/share/doc/keyboxd/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.4.4-2ubuntu17.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.3.dsc' gnupg2_2.4.4-2ubuntu17.3.dsc 3602 SHA512:41cc969eb1ee7acdf08f578843fc17d8954c727194ff05e6373588950a809ba9827a488a1745806f7ea19ea8d55542306d2166a53fadf6fcf5d4d8404c814eb1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2' gnupg2_2.4.4.orig.tar.bz2 7886036 SHA512:3d1a3b08d1ce2319d238d8be96591e418ede1dc0b4ede33a4cc2fe40e9c56d5bbc27b1984736d8a786e7f292ddbc836846a8bdb4bf89f064e953c37cb54b94ef
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2.asc' gnupg2_2.4.4.orig.tar.bz2.asc 386 SHA512:abb44c8bfa59e589bdcd660f1d1a2e268bade8729d95b34263e3d3b5388d1d2276420313989777938f17f97739c554808f97a63257ca0f53d2122a346d70ec85
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.3.debian.tar.xz' gnupg2_2.4.4-2ubuntu17.3.debian.tar.xz 96100 SHA512:b4a92c8aad8808950eb94a5597eb0db4e4e6e76cc69ad405fad1240abafd7467c346618430ba1147151a3cbde66c5f9803f20ba2668a86dc4da97812433ddd7f
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

### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

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

### `dpkg` source package: `hostname=3.23+nmu2ubuntu2`

Binary Packages:

- `hostname=3.23+nmu2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

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


### `dpkg` source package: `jansson=2.14-2build2`

Binary Packages:

- `libjansson4:amd64=2.14-2build2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

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

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

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


### `dpkg` source package: `libedit=3.1-20230828-1build1`

Binary Packages:

- `libedit2:amd64=3.1-20230828-1build1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

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

### `dpkg` source package: `libpng1.6=1.6.43-5build1`

Binary Packages:

- `libpng16-16t64:amd64=1.6.43-5build1`

Licenses: (parsed from: `/usr/share/doc/libpng16-16t64/copyright`)

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


### `dpkg` source package: `libssh=0.10.6-2ubuntu0.2`

Binary Packages:

- `libssh-4:amd64=0.10.6-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

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

### `dpkg` source package: `libtasn1-6=4.19.0-3ubuntu0.24.04.1`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.19.0-3ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.1.dsc' libtasn1-6_4.19.0-3ubuntu0.24.04.1.dsc 2846 SHA512:1f83726190ebe1fb9a52fc330cf794629df8180e803110a38825a4ea59c4a70ee2d973089f07dac1f06d258f37548f3bf557798ee5a832388b19c0c5c6403eb7
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA512:287f5eddfb5e21762d9f14d11997e56b953b980b2b03a97ed4cd6d37909bda1ed7d2cdff9da5d270a21d863ab7e54be6b85c05f1075ac5d8f0198997cf335ef4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA512:e0417625f8df22c6421914bf2d4f19d7f27260c24c04f50e59669681f326debe06ddef9dc5a2e20fda50feb30bbbf3f41597e64961257304ec2c407aa76d107e
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.1.debian.tar.xz' libtasn1-6_4.19.0-3ubuntu0.24.04.1.debian.tar.xz 24752 SHA512:6353360456b2fe7079f9ee98d82d065c85c488ae6103e68f374267be6e55ebb1e3fe251f2c738b96cf9fc67d36e2b9329d43acb2605d74994b957320649f5687
```

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

### `dpkg` source package: `libxcrypt=1:4.4.36-4build1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.36-4build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libyaml=0.2.5-1build1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`)

- `Expat`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libzstd=1.5.5+dfsg2-2build1.1`

Binary Packages:

- `libzstd1:amd64=1.5.5+dfsg2-2build1.1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

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

### `dpkg` source package: `lz4=1.9.4-1build1.1`

Binary Packages:

- `liblz4-1:amd64=1.9.4-1build1.1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

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


### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/media-types/10.1.0/


### `dpkg` source package: `mercurial=6.7.2-1ubuntu2.2`

Binary Packages:

- `mercurial=6.7.2-1ubuntu2.2`
- `mercurial-common=6.7.2-1ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=6.7.2-1ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.7.2-1ubuntu2.2.dsc' mercurial_6.7.2-1ubuntu2.2.dsc 2929 SHA512:f7a7047a830d2d8f8d1f85bdcad491364503f1fa3da76a4002b35f0e3b22f70e21372cf7d3656ebfac431047c1b6a91c798b8c6a7a2e81e1133ecc9f95aaf584
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.7.2.orig.tar.gz' mercurial_6.7.2.orig.tar.gz 8302143 SHA512:cb64daf885451d606ad34c408fbefc900be0fab7c0e0c2fc63dda32676de1c77a9d194c8c4974a608020a0f09e326682443537769eaa97acaf89ad7e385e0ce5
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.7.2.orig.tar.gz.asc' mercurial_6.7.2.orig.tar.gz.asc 659 SHA512:197fe9434ac3d978978ee549a8c891cbe2078f08c34906169cb84cffda9b56af33be275c8e528078249b198ed167e8bc436c385e65f8f102fa7ccb5f6d5e63e2
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.7.2-1ubuntu2.2.debian.tar.xz' mercurial_6.7.2-1ubuntu2.2.debian.tar.xz 75080 SHA512:4b4debd4c4b24af944b60ff7cebf2d65b2778bc34a54071f25f187a24567c3a8ac32b9c21a75c6b4db4af795daa07504aefc20858ff39331096269a792bb7f4b
```

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

### `dpkg` source package: `npth=1.6-3.1build1`

Binary Packages:

- `libnpth0t64:amd64=1.6-3.1build1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

- `libssl3t64:amd64=3.0.13-0ubuntu3.6`
- `openssl=3.0.13-0ubuntu3.6`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.13-0ubuntu3.6
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.6.dsc' openssl_3.0.13-0ubuntu3.6.dsc 2512 SHA512:e57effde33e3e978184e1c2d5167d8f8c1c881aae59f81dfbedeca0004488434c3dff227bec9ca6e3f701c01a9c5a7a3c8ffb3fef3533d9dee0f46b64d03e535
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13.orig.tar.gz' openssl_3.0.13.orig.tar.gz 15294843 SHA512:22f4096781f0b075f5bf81bd39a0f97e111760dfa73b6f858f6bb54968a7847944d74969ae10f9a51cc21a2f4af20d9a4c463649dc824f5e439e196d6764c4f9
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.6.debian.tar.xz' openssl_3.0.13-0ubuntu3.6.debian.tar.xz 169500 SHA512:bc33f7a4d5c577cc622062b2337a2b897bc06dd6592f6e636832529ff8ebde4f5fcb5d35589d041ec498386d7ec63df2b76f37aaab0b0cddf35a4d53c8a5cc3f
```

### `dpkg` source package: `p11-kit=0.25.3-4ubuntu2.1`

Binary Packages:

- `libp11-kit0:amd64=0.25.3-4ubuntu2.1`
- `p11-kit=0.25.3-4ubuntu2.1`
- `p11-kit-modules:amd64=0.25.3-4ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`, `/usr/share/doc/p11-kit/copyright`, `/usr/share/doc/p11-kit-modules/copyright`)

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

### `dpkg` source package: `patiencediff=0.2.13-1build2`

Binary Packages:

- `python3-patiencediff=0.2.13-1build2`

Licenses: (parsed from: `/usr/share/doc/python3-patiencediff/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pcre2=10.42-4ubuntu2.1`

Binary Packages:

- `libpcre2-8-0:amd64=10.42-4ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

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

### `dpkg` source package: `python-fastbencode=0.2-1build2`

Binary Packages:

- `python3-fastbencode=0.2-1build2`

Licenses: (parsed from: `/usr/share/doc/python3-fastbencode/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-merge3=0.0.8-1`

Binary Packages:

- `python3-merge3=0.0.8-1`

Licenses: (parsed from: `/usr/share/doc/python3-merge3/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-merge3/0.0.8-1/


### `dpkg` source package: `python-tzlocal=5.2-1.1`

Binary Packages:

- `python3-tzlocal=5.2-1.1`

Licenses: (parsed from: `/usr/share/doc/python3-tzlocal/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-tzlocal/5.2-1.1/


### `dpkg` source package: `python-urllib3=2.0.7-1ubuntu0.2`

Binary Packages:

- `python3-urllib3=2.0.7-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/python3-urllib3/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-urllib3=2.0.7-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_2.0.7-1ubuntu0.2.dsc' python-urllib3_2.0.7-1ubuntu0.2.dsc 2781 SHA512:348a6bc80611168528eb0990663c51b3d19d0a15338f35eef466efea719f7cbcb85de81f19b0947458182bcc95511a868ce463b840ce341656d63e3c9d73367b
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_2.0.7.orig.tar.gz' python-urllib3_2.0.7.orig.tar.gz 282546 SHA512:ca21dd330cfc7f53e6f00a92be1df1d24acbe61b6ca31c52a272dccd6f50d1bb797eece9132860adc84c21a9bebc3030a12816081451fcb8384c11a6cd2d1e8b
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_2.0.7-1ubuntu0.2.debian.tar.xz' python-urllib3_2.0.7-1ubuntu0.2.debian.tar.xz 13560 SHA512:84654672e0bc47bee1d8c7d9bf4fda2fc371369088acb4111c7f28978605b1f6287374f189ee9a6bd7ca3064f7731b1aa9e9c2394ec4f0b6ffe67a7ba9eba699
```

### `dpkg` source package: `python3-defaults=3.12.3-0ubuntu2.1`

Binary Packages:

- `libpython3-stdlib:amd64=3.12.3-0ubuntu2.1`
- `python3=3.12.3-0ubuntu2.1`
- `python3-minimal=3.12.3-0ubuntu2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.12.3-0ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.dsc' python3-defaults_3.12.3-0ubuntu2.1.dsc 3116 SHA512:34bd93d70a55ea6e57e2c8adb7fab3a23507161c2ca61b2c089208cf3706455ef7e072cc04b68af9c1ecb04ed9636e65524501d9e2eb837319f220f275582c4b
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.tar.gz' python3-defaults_3.12.3-0ubuntu2.1.tar.gz 147765 SHA512:9a729a8df22e37d473d39b8c9c95b8c5a7ad8dfd244b3c87576d389f48543edeeaa0bd8b0557de3224d0dbd0f06e02b573cb18adf685a54c02bb485a21ec36e5
```

### `dpkg` source package: `python3.12=3.12.3-1ubuntu0.8`

Binary Packages:

- `libpython3.12-minimal:amd64=3.12.3-1ubuntu0.8`
- `libpython3.12-stdlib:amd64=3.12.3-1ubuntu0.8`
- `libpython3.12t64:amd64=3.12.3-1ubuntu0.8`
- `python3.12=3.12.3-1ubuntu0.8`
- `python3.12-minimal=3.12.3-1ubuntu0.8`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/libpython3.12t64/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pyyaml=6.0.1-2build2`

Binary Packages:

- `python3-yaml=6.0.1-2build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `serf=1.3.10-1ubuntu0.24.04.1`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-1ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris serf=1.3.10-1ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serf/serf_1.3.10-1ubuntu0.24.04.1.dsc' serf_1.3.10-1ubuntu0.24.04.1.dsc 2283 SHA512:876947a65af37239fc60f6e771f72bf1072cda4a30a5fdd1fe1c72695d1311a94be1c0f44ac0917513985e1ffeb39c38a91904ca0166d4990c35c647cd69c473
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serf/serf_1.3.10.orig.tar.bz2' serf_1.3.10.orig.tar.bz2 147744 SHA512:19165274d35c694935cda33f99ef92a7663a5d9c540fb7fd6792aa0efe39941b2fa87ff8b61afd060c6676baec634fd33dc2e9d34ecbee45ed99dfaed077802c
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serf/serf_1.3.10.orig.tar.bz2.asc' serf_1.3.10.orig.tar.bz2.asc 819 SHA512:6cb51a1a0cebc605c6a73330f55241191943393015cab1028326c17b5bc86be293c43365f50eceb77e81dc88a04af198305a2da971989b15082e91792c4a754c
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serf/serf_1.3.10-1ubuntu0.24.04.1.debian.tar.xz' serf_1.3.10-1ubuntu0.24.04.1.debian.tar.xz 70196 SHA512:eea058bcbf1b5d06f77708279271f4e2fb9f710e3e08dd45733e08743e9d52bd541230de0edb657facd466dbe1e27073bf616d98ace70d6a37b3b566275a6e2d
```

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

### `dpkg` source package: `sqlite3=3.45.1-1ubuntu2.5`

Binary Packages:

- `libsqlite3-0:amd64=3.45.1-1ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

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

### `dpkg` source package: `subversion=1.14.3-1build4`

Binary Packages:

- `libsvn1:amd64=1.14.3-1build4`
- `subversion=1.14.3-1build4`

Licenses: (parsed from: `/usr/share/doc/libsvn1/copyright`, `/usr/share/doc/subversion/copyright`)

- `AFL-3`
- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BoostAcMacros`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `Svnwrap`
- `Unicode`
- `Utfwidth`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `systemd=255.4-1ubuntu8.11`

Binary Packages:

- `libsystemd0:amd64=255.4-1ubuntu8.11`
- `libudev1:amd64=255.4-1ubuntu8.11`

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
$ apt-get source -qq --print-uris systemd=255.4-1ubuntu8.11
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.11.dsc' systemd_255.4-1ubuntu8.11.dsc 7324 SHA512:911c29309ba54128641ff4dac6bc86a3b2e276778fb8446daa29747385a7f6781f339ec4ab82bf34085d8156e08da2e9965e1bcabcd1d65ee575b5d82ef18ddf
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4.orig.tar.gz' systemd_255.4.orig.tar.gz 14952427 SHA512:8a2bde11a55f7f788ba7751789a5e9be6ce9634e88d54e49f6e832c4c49020c6cacaf2a610fe26f92998b0cbf43c6c2150a96b2c0953d23261009f57d71ea979
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.11.debian.tar.xz' systemd_255.4-1ubuntu8.11.debian.tar.xz 256052 SHA512:b8bf683caee235c8c46725592dd8b9c5acc08c3c0709ded98e039c089bc34c04618fc70dae70efdf8ee8bec09f2e124951d31574973c9d6f752ab935b700f7f8
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


### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ucf/3.0043+nmu1/


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

### `dpkg` source package: `unzip=6.0-28ubuntu4.1`

Binary Packages:

- `unzip=6.0-28ubuntu4.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu4.1.dsc' unzip_6.0-28ubuntu4.1.dsc 1891 SHA512:ff71afdca87465e64b9c58e154fa82ab59da90f416054492902077fa646955ea76d1c9c30558565e3af9c552aee8885de5e749dbff6da676af3013b713d87b26
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu4.1.debian.tar.xz' unzip_6.0-28ubuntu4.1.debian.tar.xz 42948 SHA512:59effec60c41e20fe2f36782a62cf5456dd799b5432b75a4f46b8bcb6ff6d1b32d4ad2139183d99e76de573fb370b0745b97d3f207640a0872a4accfc9f4f3fa
```

### `dpkg` source package: `utf8proc=2.9.0-1build1`

Binary Packages:

- `libutf8proc3:amd64=2.9.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `util-linux=2.39.3-9ubuntu6.3`

Binary Packages:

- `bsdutils=1:2.39.3-9ubuntu6.3`
- `libblkid1:amd64=2.39.3-9ubuntu6.3`
- `libmount1:amd64=2.39.3-9ubuntu6.3`
- `libsmartcols1:amd64=2.39.3-9ubuntu6.3`
- `libuuid1:amd64=2.39.3-9ubuntu6.3`
- `mount=2.39.3-9ubuntu6.3`
- `util-linux=2.39.3-9ubuntu6.3`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.39.3-9ubuntu6.3
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.3.dsc' util-linux_2.39.3-9ubuntu6.3.dsc 4726 SHA512:8abb6a898719a36cf33ef3f9464d78256c05ce68b1eedfe820113d3d85e336277843a8558e37320a4eeaa8a7a5dcaf2df54e0b68baf4a555dd70e71dbb1e373b
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3.orig.tar.xz' util-linux_2.39.3.orig.tar.xz 8526168 SHA512:a2de1672f06ca5d2d431db1265a8499808770c3781019ec4a3a40170df4685826d8e3ca120841dcc5df4681ca8c935a993317bd0dc70465b21bf8e0efef65afa
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.3.debian.tar.xz' util-linux_2.39.3-9ubuntu6.3.debian.tar.xz 146444 SHA512:525b2bcd406b962ac32bfa558a276a77515a6a12cefca3c8ad5417d9eee6520c7e928e9d88757d3518998cecb6265d3630b54b80bb7c76d418464113dc91d108
```

### `dpkg` source package: `wget=1.21.4-1ubuntu4.1`

Binary Packages:

- `wget=1.21.4-1ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.21.4-1ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4-1ubuntu4.1.dsc' wget_1.21.4-1ubuntu4.1.dsc 2251 SHA512:d7b0fab6350ba51e5783ff8e931fd20894c8334c9f78f9f1c970a755d93e54ae501bdc5f5050d536a99472b536acb141ae67a4cbd43f014acbcaf2828ab3e6fb
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4.orig.tar.gz' wget_1.21.4.orig.tar.gz 5059591 SHA512:7a1539045174f6b97ab6980811c2ac1799edc20db72987b5ba9b1710cffb19669a7736813d15c8da3aa2d4a384246ff946b77ecb0baeb6fd3e12ae591f1bf6a3
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4.orig.tar.gz.asc' wget_1.21.4.orig.tar.gz.asc 854 SHA512:72603493c2d799dca08700175a2010d8736fd6d3cb9bea3987db8814e9f133ab0fbd1477892115f7fbbd1a7d4d416ec370bdbff6dbe8f00d1eea84f0c4f8d84b
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4-1ubuntu4.1.debian.tar.xz' wget_1.21.4-1ubuntu4.1.debian.tar.xz 65000 SHA512:7f8d94188f21aeddf4a2b845839994f1ec90a1727891ad5496bdc3841600abed8d58b3c111a2ef33329d85b57dcd8364b4ab174acf93cfd5a0c3eb8487c917da
```

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

- `liblzma5:amd64=5.6.1+really5.4.5-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

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

### `dpkg` source package: `zlib=1:1.3.dfsg-3.1ubuntu2.1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3.1ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3.1ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.dsc' zlib_1.3.dfsg-3.1ubuntu2.1.dsc 3116 SHA512:5cf00ba3f81611c9e94321e524dfcbbe19b7f7d8570e0bc15da334ecf72d212cc22366659ed5ede3e1716ba1ebd2e05c65663e64f1e283fb1f84a3956fd2f4c3
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA512:be6f020c691c61fe4ddcb27d3f8b2515435f544177e0b97286b5e85afc3862c1de6cd74a14ff6b065d620d046d35bf029fabfd1cf473f43a2cad60bf9ad55afe
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz' zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz 61028 SHA512:18f491ffac55e6f9464befc89bbe3067030dfd30d8093c06cd7aa511e4534123b87cecf8f2dde4c7447c77de7965b488de6f407637b4a1ace2f55afc0adae170
```
