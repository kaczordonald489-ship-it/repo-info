# `buildpack-deps:noble`

## Docker Metadata

- Image ID: `sha256:aa71cd6ae89dbd75282d20c4fb41a63d96bdb7ea7945b7be39bade127a6135ce`
- Created: `2025-11-14T01:12:58.996713498Z`
- Virtual Size: ~ 795.54 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
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

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu1.dsc' adduser_3.137ubuntu1.dsc 1862 SHA512:4e32edd8d12689bc8f6fb2b5280b0504bbd19bdd963cebb32a016d87fbeb837cbfb9c4c544b37943adf346d33137c684936591ccbf5c89856a91f2777f00ae49
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu1.tar.xz' adduser_3.137ubuntu1.tar.xz 280408 SHA512:46979160ef2f6b85097958cd11e549ae48efa24e1719155fd90ae7b322c0adac087cac7d0a709cd084ee11557575b05dfde89a9d63bcfd80fb47779c41098d48
```

### `dpkg` source package: `aom=3.8.2-2ubuntu0.1`

Binary Packages:

- `libaom3:amd64=3.8.2-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

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

### `dpkg` source package: `apr-util=1.6.3-1.1ubuntu7`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-1.1ubuntu7`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-1.1ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-1.1ubuntu7.dsc' apr-util_1.6.3-1.1ubuntu7.dsc 2947 SHA512:67c60bb82cce5913648560305202055bfd02c55d70e4e16644965130b884477a2a60e1e50b80ad2c218d0844ff37f1cace5b87e09731f00cad7548e4e4173b04
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA512:8050a481eeda7532ef3751dbd8a5aa6c48354d52904a856ef9709484f4b0cc2e022661c49ddf55ec58253db22708ee0607dfa7705d9270e8fee117ae4f06a0fe
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2.asc' apr-util_1.6.3.orig.tar.bz2.asc 833 SHA512:6c483e823fb032b161b6bcf77f9a43945aee9afbe40050ebf042865434bc533d21168af20d4cdff597b60b782d8ac9322409a5c2a64bf921b22f5add2451d79d
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-1.1ubuntu7.debian.tar.xz' apr-util_1.6.3-1.1ubuntu7.debian.tar.xz 342276 SHA512:64a09f76917cef4552b9494c54677d6c21938c31f0a957f09e6a601849fd14c7461b1d4ca39e854d41a42d723c0ec254cc2751e81600e9e0176d064c73cfb600
```

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

Source:

```console
$ apt-get source -qq --print-uris autoconf=2.71-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.71-3.dsc' autoconf_2.71-3.dsc 1988 SHA512:77b5211bc883080da398a9b16ea5455b6e1562c4be7459844b58a61bcf57183bf6440547ef3bcc55b4ece3213347aaaa12dbf1603d5528d037cfb956413e29f6
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.71.orig.tar.gz' autoconf_2.71.orig.tar.gz 2003781 SHA512:2bc5331f9807da8754b2ee623a30299cc0d103d6f98068a4c22263aab67ff148b7ad3a1646bd274e604bc08a8ef0ac2601e6422e641ad0cfab2222d60a58c5a8
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.71-3.debian.tar.xz' autoconf_2.71-3.debian.tar.xz 23896 SHA512:12debf9cd25329130b7d9b00b77bbbfb7f3f26cdf6dbe60188203e3a66ed933f693de02c3816856e4157d5843647d7c834c3bd924345a7ac41ad35aac3689f63
```

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

Source:

```console
$ apt-get source -qq --print-uris automake-1.16=1:1.16.5-1.3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3ubuntu1.dsc' automake-1.16_1.16.5-1.3ubuntu1.dsc 2657 SHA512:8000fe08014aaa9da51cefe063499a6f8932515916e81cd9b4a3201313609804ce69a353a0bbb5d6e0b574107259e0e8e61a7af21f1932f4b2cfcea359ed619f
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz' automake-1.16_1.16.5.orig.tar.xz 1601740 SHA512:3084ae543aa3fb5a05104ffb2e66cfa9a53080f2343c44809707fd648516869511500dba50dae67ff10f92a1bf3b5a92b2a0fa01cda30adb69b9da03994d9d88
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz.asc' automake-1.16_1.16.5.orig.tar.xz.asc 833 SHA512:032a7c39abb4cabbefa4eb9c15263baec0902e48c0c81364307361a41fd55be282b9640707c789f5ae572e8e60240e34d1b575a671b5710f5d2a5716fafc2d51
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3ubuntu1.debian.tar.xz' automake-1.16_1.16.5-1.3ubuntu1.debian.tar.xz 14624 SHA512:95bf57bcfe7f509c2c1c5e3c6fbe9a407af96dca49ccde0e990580720b301974c882a3a4ae7a9e9bb26c0129918f0847fb480749a315a52204b705a0a277f2c2
```

### `dpkg` source package: `autotools-dev=20220109.1`

Binary Packages:

- `autotools-dev=20220109.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20220109.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20220109.1.dsc' autotools-dev_20220109.1.dsc 1661 SHA512:aca60be8ed006832005e58bf176f8c7e8abe85986dbcc6d15d8b5c092c89322a132601784ef1f977d7e071c8b033debcef7c3cb5712765be00c2d298d9812d71
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20220109.1.tar.xz' autotools-dev_20220109.1.tar.xz 87340 SHA512:5427cc6897685355018db547ec39fd6bcc0ecbd73ba25869fb841f3503c1753af9a323d963a2b3150ef40ff07486f39377acdec878b2c054c1fa51de9afe01bb
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

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.3build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.3build1.dsc' base-passwd_3.6.3build1.dsc 1779 SHA512:b22ef01978e2b6aed82e54c28b7f06550cc0a41518f1561054148df9d3adb567e203b793e532924a9ae27201c5a2a31fef149f77217d06d8b12f8fce05e2f34d
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.3build1.tar.xz' base-passwd_3.6.3build1.tar.xz 58252 SHA512:981b05acb6727b32fe343e761eeacee2a2061da3802999de7e10f95dfae3fdb0bd52b96001e13bf302f7be137ac6b85d6d36041ee29b9eb62f6fa21622a00ac9
```

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

Source:

```console
$ apt-get source -qq --print-uris bash=5.2.21-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21-2ubuntu4.dsc' bash_5.2.21-2ubuntu4.dsc 2437 SHA512:7e783b1a20b339b2c15070e1cf3419a10e94a17c9dda520025b6eeb07f285dcbe8455aa1647254fc422cb314dd1382ef97c65cab088793de699d4714f65eaa0d
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21.orig.tar.xz' bash_5.2.21.orig.tar.xz 5598816 SHA512:ccfd5201ebc32feb302db324868bec42a525a6b08176c77e16feb191fcd6ee4240182dcad783e6e3f010c6d33f356b2c628758f0387ef488ab8b3f932e54babb
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21-2ubuntu4.debian.tar.xz' bash_5.2.21-2ubuntu4.debian.tar.xz 94124 SHA512:cbe580880995984a6ceb6c980d2fa87bbb1ace85d834a147ce39eaf44692af654c2c537716a19c8ed21b20e8abad9240d3f3349cc51020aeba2cd6e490802725
```

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

### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2build2`
- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build2.dsc' brotli_1.1.0-2build2.dsc 2401 SHA512:74b6f53c8917622cf69f3a5ec7d2032a5ffaf3673700efa7c0f1a095280024a48bee2518c17329d0d23a0c54d1868d0fa247e663aeca9b4587883b5f88eea1b6
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA512:7a94f8b1ca1d3a411c6b5681bd2ed66183468f7b37a24741601d77ed4353577805de84c810dd26086d4afe6b11bfc4791db3ba7f6f9986bc7acbb8e9b43f488b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build2.debian.tar.xz' brotli_1.1.0-2build2.debian.tar.xz 5644 SHA512:d7f430be5228cfb92ccc2908b915ab817d6165291671721112c1b5511949e92a2bfd1017f7ad44afd00fa0a133c3724c02e9d22f81e2a726d9958bbdae9f44f0
```

### `dpkg` source package: `build-essential=12.10ubuntu1`

Binary Packages:

- `build-essential=12.10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris build-essential=12.10ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/build-essential/build-essential_12.10ubuntu1.dsc' build-essential_12.10ubuntu1.dsc 2367 SHA512:7ca7db214eca918ef292b78eb57b0616c3d03975aa2d2ed938b4f2da11d87d270a711f213d3f87a9e5da525fd8c02baed39c97fa8084ffdf05e07ae66a76c1f6
'http://archive.ubuntu.com/ubuntu/pool/main/b/build-essential/build-essential_12.10ubuntu1.tar.xz' build-essential_12.10ubuntu1.tar.xz 51788 SHA512:0a8dd8183658a93325dee583a99b39f1fa0e4563825865602abeae29f96e53eb97407bf2d1e85b2d7bc5e64a47da193a021ca492061dce4c4be48b12fd546bb4
```

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

### `dpkg` source package: `ca-certificates=20240203`

Binary Packages:

- `ca-certificates=20240203`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203.dsc' ca-certificates_20240203.dsc 1766 SHA512:3cd6d9322800a3469be7dcea1136daa0f9311ae148b258bbf6689d5992f4dda82351fba34d52bc07c505bf407f3f4feb4e284ecfc2fec18bb1c23b1652b98986
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203.tar.xz' ca-certificates_20240203.tar.xz 263276 SHA512:e9d7b5283c2be9425d18eb4a9b54b1fa54db0b9d1bdb28f9c6db7f8b2e03fd93442ac973f9b024b7a148d71ac2789edbc1207c2048ce4be589eb1a5376640670
```

### `dpkg` source package: `cairo=1.18.0-3build1`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.0-3build1`
- `libcairo-script-interpreter2:amd64=1.18.0-3build1`
- `libcairo2:amd64=1.18.0-3build1`
- `libcairo2-dev:amd64=1.18.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.0-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.0-3build1.dsc' cairo_1.18.0-3build1.dsc 2780 SHA512:c128d3701258e805a082d0366f274087c02d978bc030acbb814023831d5844170d73a1a05dafcfee5dcdc70731e6b4e986784222edf9c1e3ff98f07343d47049
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.0.orig.tar.xz' cairo_1.18.0.orig.tar.xz 33761148 SHA512:6366c7d5e3fd3e12df2edc43aa4ed4c3a517de2ef0b1b3b30dfa8b69a7cae1dd55765801228cec308d2e9792037d0704ae49d95b7b12c06f20df092fa0534e1c
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.0-3build1.debian.tar.xz' cairo_1.18.0-3build1.debian.tar.xz 29880 SHA512:afedd81be380b7da33f60da05faf8f39b3dc84b6932c092410adf3f0bae9ef43eb60adec2cd67fa9ec119fc560e9f050fe1213dfd3c61a86d6bd13f83680b671
```

### `dpkg` source package: `cdebconf=0.271ubuntu3`

Binary Packages:

- `libdebconfclient0:amd64=0.271ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.271ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.271ubuntu3.dsc' cdebconf_0.271ubuntu3.dsc 2910 SHA512:1c3864532126b71702307dfa4385e844363dcb8faf3f30009073dc0ebf6167ed97dd225679c3f6fb9650c5c41be8f5309668f2e4fe2d8ba798bd2cfc9dd18f36
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.271ubuntu3.tar.xz' cdebconf_0.271ubuntu3.tar.xz 285500 SHA512:f9a3204842db5e0f0e042c9df72dee17692422bc4c745bc0c332317ec87dc219e26eda94404c1d7b0a6d5d6c2105da0b9ebe615c4897f012883bc8222f9ac85d
```

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

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-6ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-6ubuntu5.dsc' dash_0.5.12-6ubuntu5.dsc 2124 SHA512:f29c60c6d01fdf8d5c12b2924fcb2ba7a9e27025976b3158900c3e33eba7100dfe3158a1efb641177527b672fff0e9b1659ace0711063decca17e4e6f3d6dada
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-6ubuntu5.debian.tar.xz' dash_0.5.12-6ubuntu5.debian.tar.xz 39616 SHA512:2524c1aaf0cf2f86a5fa87de998c8324a247760b59c86ef1b02ef6af298648842b1b467d3f8c6beda31bed3cc0db17fa189f20aab8305503b67df4f0c25a23d1
```

### `dpkg` source package: `db-defaults=1:5.3.21ubuntu2`

Binary Packages:

- `libdb-dev:amd64=1:5.3.21ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=1:5.3.21ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu2.dsc' db-defaults_5.3.21ubuntu2.dsc 1663 SHA512:018dc4aedcf739f611a55d1ad1ee6ad62f0ed60d33ebfeb493ac9709e743f5cb2bd318ee246a3f52f0274424048c94c25f685889a82c16b24357c023f63917df
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu2.tar.xz' db-defaults_5.3.21ubuntu2.tar.xz 2644 SHA512:7a41ab8046316afe6da9623ba36bf6803b6de49059f29acdb5d931009e3f317381713c3d2f68c4aeefa5bbed2e625196359b4735421d8e9caffd07f0f06184b4
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-7`

Binary Packages:

- `libdb5.3-dev=5.3.28+dfsg2-7`
- `libdb5.3t64:amd64=5.3.28+dfsg2-7`

Licenses: (parsed from: `/usr/share/doc/libdb5.3-dev/copyright`, `/usr/share/doc/libdb5.3t64/copyright`)

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-7
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.dsc' db5.3_5.3.28+dfsg2-7.dsc 2374 SHA512:3877ed17196ea9d9bac87112b81461ba3bfa02fd5017043baf277728cc151bed2238a90f707464d0a4e24aab865bf5f6c0c6ee6d0eb5ec866efe4cea91f7b93c
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.debian.tar.xz' db5.3_5.3.28+dfsg2-7.debian.tar.xz 35232 SHA512:9e91cdf98925d94c7f318e534474e208ce8796113867f290bcaf8ca9c3f35d309266a35e17eb5624246c5e0bf94e5893c203f5154d7d0ba50b13babf53339156
```

### `dpkg` source package: `debconf=1.5.86ubuntu1`

Binary Packages:

- `debconf=1.5.86ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.86ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.86ubuntu1.dsc' debconf_1.5.86ubuntu1.dsc 2030 SHA512:d06dc6bfa5e60ddb38839b25437641dcbd06acabc59dfa46955db87bf47370b381906916bde881de51a8dc4beaf1be9c3288bb25292718e608077c755a491988
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.86ubuntu1.tar.xz' debconf_1.5.86ubuntu1.tar.xz 574112 SHA512:e63b3d4241e8b347fcd71f7ae838e6b0c40123bea65298a9492ae6dabb24e54d31176c11a8b1870edb5a96ea346080d2f9ca8821cef74e73f20c03265aafd95d
```

### `dpkg` source package: `debianutils=5.17build1`

Binary Packages:

- `debianutils=5.17build1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.17build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.17build1.dsc' debianutils_5.17build1.dsc 1771 SHA512:4303221ace648a071b5de66dd570e334579cae327c5ad4f1bda10c957fca2f8f023f9ef6a0e1bf852ed378405a83106e85a76daf6fe9870b8f48655f1d15e8fe
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.17build1.tar.xz' debianutils_5.17build1.tar.xz 80468 SHA512:a076c0457c2e8423ecbf2ea01c4ba029feb8eacadb5c2622422a22b24ed1d52b785fc7e651406b533e7f1e26466d6570a3719852885d5270ee058fde1d336742
```

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

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.10-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1build1.dsc' diffutils_3.10-1build1.dsc 2192 SHA512:60bfa2bb6c9316393e21d03863c0f7a837280bccd4bf20818ca6bc749328172f4dd433603c231d5ce17b6ed68d4070c7e5037546a94f71d8bc50b81578b9645f
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1build1.debian.tar.xz' diffutils_3.10-1build1.debian.tar.xz 14068 SHA512:36cb15f987cfd57dbe5bfe347a990887ffe52f8ba3756c4f806e78ba702d2b1acc2f316292bf1096a1a7db158358b4cd6261cabe70a77fd292945e07d5808cb5
```

### `dpkg` source package: `djvulibre=3.5.28-2ubuntu0.24.04.1`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.28-2ubuntu0.24.04.1`
- `libdjvulibre-text=3.5.28-2ubuntu0.24.04.1`
- `libdjvulibre21:amd64=3.5.28-2ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.28-2ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2ubuntu0.24.04.1.dsc' djvulibre_3.5.28-2ubuntu0.24.04.1.dsc 2506 SHA512:fffad2f15719ca84b398ab422e21c9c4754bb452d31525e6372df98f93815ec5560d9468427a69c9d1475448660fec621411837780079feb0315a6b6800c7e02
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28.orig.tar.xz' djvulibre_3.5.28.orig.tar.xz 2959024 SHA512:4fdbecd2b7b583ee4211c9cda6638a3a831c883e2552b3c8ad09f69e8734831addc14f590faab8c58d7f9f017b527abccc384f6066e674e341cf43c96db49cb7
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2ubuntu0.24.04.1.debian.tar.xz' djvulibre_3.5.28-2ubuntu0.24.04.1.debian.tar.xz 18304 SHA512:e9fdd8a60bcb9dfe5f8c7df4882578b717604c25d300f5404caef60e0ec97be70f016ec72bf63c1b84a77e5d6e80e5937378335095c4aeb96fd781de559d1dc5
```

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

- `comerr-dev:amd64=2.1-1.47.0-2.4~exp1ubuntu4.1`
- `e2fsprogs=1.47.0-2.4~exp1ubuntu4.1`
- `libcom-err2:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `libext2fs2t64:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `libss2:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `logsave=1.47.0-2.4~exp1ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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

### `dpkg` source package: `elfutils=0.190-1.1ubuntu0.1`

Binary Packages:

- `libelf1t64:amd64=0.190-1.1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libelf1t64/copyright`)

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

### `dpkg` source package: `fftw3=3.3.10-1ubuntu3`

Binary Packages:

- `libfftw3-double3:amd64=3.3.10-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libfftw3-double3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-1ubuntu3.dsc' fftw3_3.3.10-1ubuntu3.dsc 2890 SHA512:5e7ee03298273c37c7308704861fecfa5ee011160c8789cbb1385c936a10001df5762652481434048132dad71d576c95554243a4ce48c328931b3b39b821f4d6
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4262403 SHA512:fa2ea740449fd06c833a82e1fff82bacd554188d500cbedff5a0bc185551799ef9ef9b8b1c227283abdbbdd185424d19df9c0f06ed88d5fe3d9c001d6fab6109
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-1ubuntu3.debian.tar.xz' fftw3_3.3.10-1ubuntu3.debian.tar.xz 14864 SHA512:219d9d15aa005c1f98d32bd9b9c2cc748ae2b43e24b04f10918c39b73ba8d13dc38a3f0f8fc3ac9152db19e416a3aeadca52af2db37ee07471c949e9182eb8d5
```

### `dpkg` source package: `file=1:5.45-3build1`

Binary Packages:

- `file=1:5.45-3build1`
- `libmagic-mgc=1:5.45-3build1`
- `libmagic1t64:amd64=1:5.45-3build1`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.45-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-3build1.dsc' file_5.45-3build1.dsc 2408 SHA512:366c97f8faa11661879e0907bda25730f24dd6369455d60723790152a6d3e67b858ce99de82b095cae396d0621efff6dcd25ae11ce8e5e4af75006623ad85f19
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz' file_5.45.orig.tar.gz 1246503 SHA512:12611a59ff766c22a55db4b4a9f80f95a0a2e916a1d8593612c6ead32c247102a8fdc23693c6bf81bda9b604d951a62c0051e91580b1b79e190a3504c0efc20a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz.asc' file_5.45.orig.tar.gz.asc 169 SHA512:4bda3c9b23e534e31d8726eae110e108c538c88ca4884666989da9bedc5dcfd9cfcb3754e68885ca5310db67bff151f9bf4f21913f7b5046f158a9ca38bc00a4
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-3build1.debian.tar.xz' file_5.45-3build1.debian.tar.xz 35964 SHA512:292021c05c73e2ea593af147e6df690a73df6ebf5b10408760be48c161ed341d974145aed93161d09fcea6a7ce0348edfea8a4c0ece9fdf54e1c33e5d3673b86
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

Source:

```console
$ apt-get source -qq --print-uris findutils=4.9.0-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0-5build1.dsc' findutils_4.9.0-5build1.dsc 2404 SHA512:5cf7d85b815176d007607c61b6220ed1b9f921e1292b6ebe8603dcdc51c132040831b664c1da5a9e5c41afe350c7d9a6f6765b7f1404e36ed47aaa3735960680
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz' findutils_4.9.0.orig.tar.xz 2046252 SHA512:ba4844f4403de0148ad14b46a3dbefd5a721f6257c864bf41a6789b11705408524751c627420b15a52af95564d8e5b52f0978474f640a62ab86a41d20cf14be9
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz.asc' findutils_4.9.0.orig.tar.xz.asc 488 SHA512:b8e0b5471242912a20b9e468fa27b7f27339af5f7be8918173105262dee0152183bf4cf516844d348b206a694e028490d5d3b190f3aed8c698ba5444941f8dfc
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0-5build1.debian.tar.xz' findutils_4.9.0-5build1.debian.tar.xz 32864 SHA512:501c6e0100ac4a7b304700518c9d45c2f8a1f76bd5f12914c9b136e3b3d117115090177d5e6c863333982ca8ded70d188bbde2ff98d51c1d3c51ff247f5eb95b
```

### `dpkg` source package: `fontconfig=2.15.0-1.1ubuntu2`

Binary Packages:

- `fontconfig=2.15.0-1.1ubuntu2`
- `fontconfig-config=2.15.0-1.1ubuntu2`
- `libfontconfig-dev:amd64=2.15.0-1.1ubuntu2`
- `libfontconfig1:amd64=2.15.0-1.1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-1.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-1.1ubuntu2.dsc' fontconfig_2.15.0-1.1ubuntu2.dsc 2817 SHA512:cd0eff27460c679b9d7db384bba94d4468f9cbf9d7bec41db6b12965f3d4ed48af35e73d3739d8ad8f5575bbc769379582e5e92e676dbe229260340f479c6d40
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA512:754cd5fffa198fc07a39cf7df683e9adfa7f54ab41fdff8c0eacc078fd35d3e01069ba343f2b045e0b40df88d9f1fc1ee0f7565799f9cb194a59cf95b64c4417
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-1.1ubuntu2.debian.tar.xz' fontconfig_2.15.0-1.1ubuntu2.debian.tar.xz 30556 SHA512:a09fe533b6a684bc6e2bfc25eda89cad9f1020c3ba5738ff9799d770a3b6c09d6a12edfeeacffe38a73d8a3f28313e7108fa6f6acff70ba1eb346007f4bc73cb
```

### `dpkg` source package: `fonts-dejavu=2.37-8`

Binary Packages:

- `fonts-dejavu-core=2.37-8`
- `fonts-dejavu-mono=2.37-8`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`, `/usr/share/doc/fonts-dejavu-mono/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

Source:

```console
$ apt-get source -qq --print-uris fonts-dejavu=2.37-8
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.dsc' fonts-dejavu_2.37-8.dsc 2156 SHA512:c5632f8cf1fa690efc292e7ae8239265ac3a04e13423601d9a151b200ea36ae5242a0867428e3c7148c0cd5fa6b4ff3c368b53451f3234e20634f2fc6fe5c1fa
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA512:e61fc8c675ef76edb49dd9a8caee62087280929bb8144b52aca2f8def30025c56246589ad8a6a806b9574e6876eedd16d57c70a6ce9c86817a2dfe39d8a2bb2b
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.debian.tar.xz' fonts-dejavu_2.37-8.debian.tar.xz 13176 SHA512:7a19189a106a1243c64d43b050f87cba6f6c32d070f246aceb5ccc687401366825a31a653e45fa700e1593f7ed32340581988cfc1a489b5f8b705e80c2a891ee
```

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

Source:

```console
$ apt-get source -qq --print-uris freetype=2.13.2+dfsg-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1build3.dsc' freetype_2.13.2+dfsg-1build3.dsc 3805 SHA512:a5d5084abbf710ff0cd16a2f268f6ae71db390ee4bbfd99ca30d37411a2a85cc81034618e05c6520fe061598a0dd5569aaa5fbf497cc43ab57e77a31da8925d8
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA512:aa83ba4212ff7c4453b72f036136cb9b04cacf7d196388a3e4752613e000b3bb45a4dcf63d3d1d5b3d6ada10720304b532fb6e33ed6a5b399dcce45c27af9ade
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:07680e2919643cb1b964c311f1590fddd38f42189944b3e5e46a9c6a84688255749506f8a745d52255e3599e5136f3e8761d746a67cdcd6e565b8eaecb9fd792
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA512:ca3438dcf6f995af556d8db3cb3cfdcabb81ab5a7dd88464ff757e3e418b3219b0011857cde8a338372e30d8375486ac8e50914da2ea948dc874f70010bce60c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:b346579fcc8f073e586135c72140c64bb3d5ca46201b879e3976b39a62a14f6668a5009d39b078e51d51a7301e346b4de6f7e9ee365f9b44146e67579aaf6500
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA512:8809693981ea7ef274d882245e3257305b65ad73e5ae36bb7e4ffc769a97b726d6bd07f1627dae456519e02e3eaa43269769d7ad363f49b9247d27d2c6f47d6d
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1build3.debian.tar.xz' freetype_2.13.2+dfsg-1build3.debian.tar.xz 44000 SHA512:d0559397ed00e767a30915f9562a2c75d93d059a7f69100fea092b9c4a45d09ad07fac55e669eae145893a326b2f984105c65ad4bed7a29077b99cda579a4e0b
```

### `dpkg` source package: `fribidi=1.0.13-3build1`

Binary Packages:

- `libfribidi0:amd64=1.0.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.13-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.13-3build1.dsc' fribidi_1.0.13-3build1.dsc 2439 SHA512:3f2dfad48107ebb7477654414f1f2818040a63bb017a865bf9ff6bb669c22c584e984bf90cc023abe4fec63933e779bc2cf89ca57d2c796bbd319329c5efdf15
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.13.orig.tar.xz' fribidi_1.0.13.orig.tar.xz 1170100 SHA512:09357d842ff9e05b918f826e28e4a25ad996e17f73242ee9ce53fae9f37ec6c639f9cae4271577f6e0269f34265afc893858225c4a94610f0a6ee7580fb1fe07
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.13-3build1.debian.tar.xz' fribidi_1.0.13-3build1.debian.tar.xz 8992 SHA512:a772c10d41ed7ae62ce042cf89563c64f26959b7bdcbe285d5dbc4b848ddf64005d658ac3cbdfa65d3327be6cf028bff87e5adfe025f78749b67f790316efa7b
```

### `dpkg` source package: `gcc-13=13.3.0-6ubuntu2~24.04`

Binary Packages:

- `cpp-13=13.3.0-6ubuntu2~24.04`
- `cpp-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04`
- `g++-13=13.3.0-6ubuntu2~24.04`
- `g++-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04`
- `gcc-13=13.3.0-6ubuntu2~24.04`
- `gcc-13-base:amd64=13.3.0-6ubuntu2~24.04`
- `gcc-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04`
- `libgcc-13-dev:amd64=13.3.0-6ubuntu2~24.04`
- `libstdc++-13-dev:amd64=13.3.0-6ubuntu2~24.04`

Licenses: (parsed from: `/usr/share/doc/cpp-13/copyright`, `/usr/share/doc/cpp-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-13/copyright`, `/usr/share/doc/g++-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-13/copyright`, `/usr/share/doc/gcc-13-base/copyright`, `/usr/share/doc/gcc-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/libgcc-13-dev/copyright`, `/usr/share/doc/libstdc++-13-dev/copyright`)

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
- `libgomp1:amd64=14.2.0-4ubuntu2~24.04`
- `libhwasan0:amd64=14.2.0-4ubuntu2~24.04`
- `libitm1:amd64=14.2.0-4ubuntu2~24.04`
- `liblsan0:amd64=14.2.0-4ubuntu2~24.04`
- `libquadmath0:amd64=14.2.0-4ubuntu2~24.04`
- `libstdc++6:amd64=14.2.0-4ubuntu2~24.04`
- `libtsan2:amd64=14.2.0-4ubuntu2~24.04`
- `libubsan1:amd64=14.2.0-4ubuntu2~24.04`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.214ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.214ubuntu1.dsc' gcc-defaults_1.214ubuntu1.dsc 38086 SHA512:92a05fd0a26767c0e74913e73264fb344f18d418b8826dd9e349de60911b3bbae0f4ed7b8e464b48cfc9024360fe55f98a07431914803fe25e4455bc23c89b23
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.214ubuntu1.tar.xz' gcc-defaults_1.214ubuntu1.tar.xz 56660 SHA512:be93edc8ae05a557021f3f6c283af75cd6f08c53fe26f3d09230275c74efeeedd0ef2dd1383b96f3265f81a640afb31bcc56bf6966feed2bc9f278011663e519
```

### `dpkg` source package: `gdbm=1.23-5.1build1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.23-5.1build1`
- `libgdbm-dev:amd64=1.23-5.1build1`
- `libgdbm6t64:amd64=1.23-5.1build1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.23-5.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23-5.1build1.dsc' gdbm_1.23-5.1build1.dsc 2608 SHA512:306270e281aa258ed61084ecceb7e9543edecb2178ab4ed584f95df9fcf22572fe4517d59c1f4a3ed26793ea0c3b289ca24f290431cfd1994bc0a03621d8fb99
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz' gdbm_1.23.orig.tar.gz 1115854 SHA512:918080cb0225b221c11eb7339634a95e00c526072395f7a3d46ccf42ef020dea7c4c5bec34aff2c4f16033e1fff6583252b7e978f68b8d7f8736b0e025838e10
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz.asc' gdbm_1.23.orig.tar.gz.asc 181 SHA512:6653751c04584f10aa3325bd1cb5b9f7970a786dd2a99602ea620c11a86a9ba5c342aa52627bd06c03da822e9e1600dc034d9a8f42856a287fd67f6b9f161c71
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23-5.1build1.debian.tar.xz' gdbm_1.23-5.1build1.debian.tar.xz 18524 SHA512:93936a3cb86632d3ba4c2c4275e045749d04cd0ef3caf88fce52e2de46ac419ef75478f7ccb1b8d89de0f8c6835fe5231aa85884e2ba095950f3831e26947855
```

### `dpkg` source package: `gdk-pixbuf=2.42.10+dfsg-3ubuntu3.2`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.10+dfsg-3ubuntu3.2`
- `libgdk-pixbuf-2.0-0:amd64=2.42.10+dfsg-3ubuntu3.2`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.10+dfsg-3ubuntu3.2`
- `libgdk-pixbuf2.0-bin=2.42.10+dfsg-3ubuntu3.2`
- `libgdk-pixbuf2.0-common=2.42.10+dfsg-3ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/gir1.2-gdkpixbuf-2.0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-dev/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-bin/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-common/copyright`)

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

### `dpkg` source package: `glib2.0=2.80.0-6ubuntu3.4`

Binary Packages:

- `gir1.2-glib-2.0:amd64=2.80.0-6ubuntu3.4`
- `gir1.2-glib-2.0-dev:amd64=2.80.0-6ubuntu3.4`
- `libgirepository-2.0-0:amd64=2.80.0-6ubuntu3.4`
- `libglib2.0-0t64:amd64=2.80.0-6ubuntu3.4`
- `libglib2.0-bin=2.80.0-6ubuntu3.4`
- `libglib2.0-data=2.80.0-6ubuntu3.4`
- `libglib2.0-dev:amd64=2.80.0-6ubuntu3.4`
- `libglib2.0-dev-bin=2.80.0-6ubuntu3.4`

Licenses: (parsed from: `/usr/share/doc/gir1.2-glib-2.0/copyright`, `/usr/share/doc/gir1.2-glib-2.0-dev/copyright`, `/usr/share/doc/libgirepository-2.0-0/copyright`, `/usr/share/doc/libglib2.0-0t64/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

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
$ apt-get source -qq --print-uris glib2.0=2.80.0-6ubuntu3.4
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0-6ubuntu3.4.dsc' glib2.0_2.80.0-6ubuntu3.4.dsc 4508 SHA512:a3c543aa79c11ed9653c715326890da9cee05154bc00e029d262bb7710391a8e10c4829187e7d0d5b0204473e1a6b5654f3f8331e029b8ce3fb651f6773feb28
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0.orig-unicode-data.tar.xz' glib2.0_2.80.0.orig-unicode-data.tar.xz 263364 SHA512:1d1c00d7416d90aac86d851fc2df94f2a97cb100a3b99f2ac28a0660deea64b994f56bbc7c05b6c7ef3b6c3a2cb18267ebc5d189abf58bd922321b509c86e2b6
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0.orig.tar.xz' glib2.0_2.80.0.orig.tar.xz 5510536 SHA512:1514d62aeb4c4a1a1048ae0f84f7db7f0dbf355772b2dadf6a34ec547045b163a5e28331b096e7616fe3c9c19bed98025a0202b05073f5d7ee901d0efaffe143
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0-6ubuntu3.4.debian.tar.xz' glib2.0_2.80.0-6ubuntu3.4.debian.tar.xz 152380 SHA512:d7b6f2d78aa5a0995eb252bd8dd6c796e7c821f4651432eeca6d8d11cf5c0ed5bd663643f88cc1d2468ee3455b8d692f160ed3f47456851b88f7ec18e5b4c12a
```

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

- `libgmp-dev:amd64=2:6.3.0+dfsg-2ubuntu6.1`
- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu6.1`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-2ubuntu6.1`

Licenses: (parsed from: `/usr/share/doc/libgmp-dev/copyright`, `/usr/share/doc/libgmp10/copyright`, `/usr/share/doc/libgmpxx4ldbl/copyright`)

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

### `dpkg` source package: `gobject-introspection=1.80.1-1`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.80.1-1`
- `gir1.2-freedesktop-dev:amd64=1.80.1-1`
- `gir1.2-girepository-2.0:amd64=1.80.1-1`
- `gir1.2-girepository-2.0-dev:amd64=1.80.1-1`
- `gobject-introspection:amd64=1.80.1-1`
- `gobject-introspection-bin=1.80.1-1`
- `libgirepository-1.0-1:amd64=1.80.1-1`
- `libgirepository-1.0-dev:amd64=1.80.1-1`
- `libgirepository1.0-dev=1.80.1-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-freedesktop/copyright`, `/usr/share/doc/gir1.2-freedesktop-dev/copyright`, `/usr/share/doc/gir1.2-girepository-2.0/copyright`, `/usr/share/doc/gir1.2-girepository-2.0-dev/copyright`, `/usr/share/doc/gobject-introspection/copyright`, `/usr/share/doc/gobject-introspection-bin/copyright`, `/usr/share/doc/libgirepository-1.0-1/copyright`, `/usr/share/doc/libgirepository-1.0-dev/copyright`, `/usr/share/doc/libgirepository1.0-dev/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `BSD-2-clause`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `FSFAP`
- `FSFULLR`
- `GPL with Autoconf exception`
- `GPL-2`
- `GPL-2+`
- `Kuchling-PD`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`

Source:

```console
$ apt-get source -qq --print-uris gobject-introspection=1.80.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1-1.dsc' gobject-introspection_1.80.1-1.dsc 4044 SHA512:0f39713385d11bbe4cd68d722f9a206688e27960b7e69465b29f0c7a73394e8f25c912033101736db5d8cc2b40801ae574ed6bc461eb011b246ebf8031bcf7dd
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1.orig-glib.tar.xz' gobject-introspection_1.80.1.orig-glib.tar.xz 5475296 SHA512:6968ac28451a72f2d8d50ce31a887be2c26ae2bc5ddba1a4aadaafb955c1bb11576017084006d78a6e6f09e88696534b94eb50c61b0b0509695a547de34c7620
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1.orig.tar.xz' gobject-introspection_1.80.1.orig.tar.xz 1040228 SHA512:f45c2c1b105086488d974c6134db9910746df8edb187772f2ecd249656a1047c8ac88ba51f5bf7393c3d99c3ace143ecd09be256c2f4d0ceee110c9ad51a839a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1-1.debian.tar.xz' gobject-introspection_1.80.1-1.debian.tar.xz 56948 SHA512:817d7a9bdd8aff7625fcb11120e8e7d18b71c0563dc89ceef104ae482cf05457949f5bec9ac62cfb49f984d66eaf0d75e6f52c5786e4ef6ad8dc762e5b1f7813
```

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

Source:

```console
$ apt-get source -qq --print-uris graphite2=1.3.14-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2build1.dsc' graphite2_1.3.14-2build1.dsc 2675 SHA512:12a79a966967fa153b271171b7f0d07607fcd2f6f1ebb64e0367846aa131e420fb593e8481a27a77c5a027d4f1d9336b1e417f9aa4a91acc4401828e90654045
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA512:49d127964d3f5c9403c7aecbfb5b18f32f25fe4919a81c49e0534e7123fe845423e16b0b8c8baaae21162b1150ab3e0f1c22c344e07d4364b6b8473c40a0822c
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2build1.debian.tar.xz' graphite2_1.3.14-2build1.debian.tar.xz 14300 SHA512:84ef56d43d1ee5478e382c90513bbbd0e7fb66eaa731f03233959bf582d01f0eb678afab93ce3cf16eeeca5844cd3ece0b22f434cd69532a54d6b36ee1776b15
```

### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.dsc' grep_3.11-4build1.dsc 2379 SHA512:5106f25775f36ba92fd7d73634d8c271fcea7dc9defef2f84d6080eb6a47dd0b1194272807267413807aa35d945c9bb66f076162d3eba539cc35eca5d255d2f9
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA512:f254a1905a08c8173e12fbdd4fd8baed9a200217fba9d7641f0d78e4e002c1f2a621152d67027d9b25f0bb2430898f5233dc70909d8464fd13d7dd9298e65c42
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA512:487aba063373ca0594c519991f19b2a6a33b3da0d74735c890f3828fd0880e7e6f64495d2c8f9efa5da53d1eb2d446609bab2399a4b89dcb4510a632e31ffb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.debian.tar.xz' grep_3.11-4build1.debian.tar.xz 20584 SHA512:212c903c240071dda1d8e966991908730af26746558078262aa32b6b0683487cb510d9b9a2c40cafb31024e78e2c74d17eb5681e329aa142b0921b88cacef7eb
```

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

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=8.3.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_8.3.0-2build2.dsc' harfbuzz_8.3.0-2build2.dsc 3032 SHA512:7d99c24b6c03e0b201d6eec8f6c7214756330468b0b40996f68f172ca9fb1bb755991d1d774e5e7bfd7702c5c8e6d9668ce75100eda80db3e2154cb32d7f2204
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_8.3.0.orig.tar.xz' harfbuzz_8.3.0.orig.tar.xz 19002808 SHA512:6b8753c0b55d34a1a46a64466b9b0de8bc4748c42b29fa9463616a5f48db08ceb4a80cce416e10861778b98dc96d0638d9dd8d7204e404662154f419f3f61f21
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_8.3.0-2build2.debian.tar.xz' harfbuzz_8.3.0-2build2.debian.tar.xz 19928 SHA512:c68ac1d147a288fcf2b3f6e7fb102f046e3f7775985737741f2d1027a14e344de3f06791e99fe7f2c82415f91458b6167849d1d180b342f6ac987b42010f0438
```

### `dpkg` source package: `hicolor-icon-theme=0.17-2`

Binary Packages:

- `hicolor-icon-theme=0.17-2`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.17-2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17-2.dsc' hicolor-icon-theme_0.17-2.dsc 2053 SHA512:5b8b3088f8d9469076d5d2a3448e1115a910958a4ba4b3bbeae287ae3e91fa3a26b87f544a1f92925230e33f6f20e96df51bc5ec01b2735e07bb3f9be2e06c3c
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17.orig.tar.xz' hicolor-icon-theme_0.17.orig.tar.xz 53016 SHA512:eca8655930aa7e234f42630041c0053fde067b970fad1f81c55fcd4c5046c03edfdf2ede72a3e78fba2908e7da53e9463d3c5ae12ab9f5ef261e29a49f9c7a8d
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17-2.debian.tar.xz' hicolor-icon-theme_0.17-2.debian.tar.xz 3536 SHA512:74b8de58f18f861f0f724419514b787495cf67b39abcfdbdc7be6923e44112b86710c015ea5e4c83301d201b503a1014fca335c6dadc522d7f7edca80f638489
```

### `dpkg` source package: `hostname=3.23+nmu2ubuntu2`

Binary Packages:

- `hostname=3.23+nmu2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu2ubuntu2.dsc' hostname_3.23+nmu2ubuntu2.dsc 1567 SHA512:a61538c601492aaba10aafc2b181f3db3f7f0ef768ce5fe4da1c4dece8655247627a77df89a7700938c665792cd134a46bfa8dd20ae59e7d0ccc199bd43b06a6
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu2ubuntu2.tar.xz' hostname_3.23+nmu2ubuntu2.tar.xz 13276 SHA512:ce7606f7bd3be9a2a2089955c1510244c8b5ef76d9e1978547870f2ff6e5fbb6cd12c040f38dc5473c46a2d77e7e7257da5787638cf5619adcced206c2c34419
```

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

### `dpkg` source package: `imagemagick=8:6.9.12.98+dfsg1-5.2build2`

Binary Packages:

- `imagemagick=8:6.9.12.98+dfsg1-5.2build2`
- `imagemagick-6-common=8:6.9.12.98+dfsg1-5.2build2`
- `imagemagick-6.q16=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickcore-6-arch-config:amd64=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickcore-6-headers=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickcore-6.q16-7-extra:amd64=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickcore-6.q16-7t64:amd64=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickcore-6.q16-dev:amd64=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickcore-dev=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickwand-6-headers=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickwand-6.q16-7t64:amd64=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickwand-6.q16-dev:amd64=8:6.9.12.98+dfsg1-5.2build2`
- `libmagickwand-dev=8:6.9.12.98+dfsg1-5.2build2`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-6-common/copyright`, `/usr/share/doc/imagemagick-6.q16/copyright`, `/usr/share/doc/libmagickcore-6-arch-config/copyright`, `/usr/share/doc/libmagickcore-6-headers/copyright`, `/usr/share/doc/libmagickcore-6.q16-7-extra/copyright`, `/usr/share/doc/libmagickcore-6.q16-7t64/copyright`, `/usr/share/doc/libmagickcore-6.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-6-headers/copyright`, `/usr/share/doc/libmagickwand-6.q16-7t64/copyright`, `/usr/share/doc/libmagickwand-6.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

- `Artistic`
- `BSD-with-FSF-change-public-domain`
- `GNU-All-Permissive-License`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL2+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception-GNU`
- `ImageMagick`
- `ImageMagickLicensePartEZXML`
- `ImageMagickLicensePartFIG`
- `ImageMagickLicensePartGsview`
- `ImageMagickLicensePartOpenSSH`
- `ImageMagickPartGraphicsMagick`
- `ImageMagickPartlibjpeg`
- `ImageMagickPartlibsquish`
- `Imagemagick`
- `LGPL-3`
- `LGPL-3+`
- `Magick++`
- `Makefile-in`
- `Perllikelicence`
- `aclocal`

Source:

```console
$ apt-get source -qq --print-uris imagemagick=8:6.9.12.98+dfsg1-5.2build2
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.12.98%2bdfsg1-5.2build2.dsc' imagemagick_6.9.12.98+dfsg1-5.2build2.dsc 5232 SHA512:b47adcbaad827bac1bcdd5211691b85648180fcf4a278c90d520e9d7b06ae99c095605a76fa76bd76855c99b1c2ded5a80306f549395f1c58833684be1cdac84
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.12.98%2bdfsg1.orig.tar.xz' imagemagick_6.9.12.98+dfsg1.orig.tar.xz 9606104 SHA512:9e7c96f4f84e3ea6a75e9fc3db06509fe091057f7c0c6f69c68464ce8337f39f81654897f4cf22bdbf326a3c886fc9951141301485699682396e20efdfff344e
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.12.98%2bdfsg1-5.2build2.debian.tar.xz' imagemagick_6.9.12.98+dfsg1-5.2build2.debian.tar.xz 260836 SHA512:e66e5db8b06154d7bc0ab8c8796157d469f90bf09d72203f1c028bceac9ae9bc564f65a0ae3ec5389d8f6133090b6e631330e274944cdd2296d6ff993bda4a28
```

### `dpkg` source package: `imath=3.1.9-3.1ubuntu2`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.9-3.1ubuntu2`
- `libimath-dev:amd64=3.1.9-3.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.9-3.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9-3.1ubuntu2.dsc' imath_3.1.9-3.1ubuntu2.dsc 2760 SHA512:ed8a9bee88c349d5e78bf3dee09ad5a000175d9571aee61ae972ea3fdd70caadc9168d755000a5cea5a04c2e9b7aa54d2f91404e1ffbbf0b65389b165fc05520
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9.orig.tar.gz' imath_3.1.9.orig.tar.gz 598497 SHA512:ad96b2ac306fc13c01e8ea3256f885499c3f545be327feaba0f5e093b70b544bcca6f8b353fa7e35107aae515c19caced44331a95d0414f367ead4691ec73564
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9.orig.tar.gz.asc' imath_3.1.9.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9-3.1ubuntu2.debian.tar.xz' imath_3.1.9-3.1ubuntu2.debian.tar.xz 10220 SHA512:53cacf3e1c998794226d94bd06ff3e2949a383577ced09fc76e9e2fa13558f59226198161c81a7fcc82be6385775d16adf92a899729981764aa9e4f650364515
```

### `dpkg` source package: `init-system-helpers=1.66ubuntu1`

Binary Packages:

- `init-system-helpers=1.66ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.66ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.dsc' init-system-helpers_1.66ubuntu1.dsc 2353 SHA512:f6aafcef04d63b54d6ff273312ff2a9194345b8725bfbbaac69793a3d016cbda730f2de8de9862d8038c36ca0fba39b868d6d640701ccf8db417094816d0e9db
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.tar.xz' init-system-helpers_1.66ubuntu1.tar.xz 45100 SHA512:222f73347b0ce9eb137c8ce5dc36e9fedbc8dc5ed3f1fde7fbf52258a5437d0a10d3d610ca1d1b206646bb92a5355d1061705440b2d22d9109b5de6d1cb92e98
```

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

### `dpkg` source package: `jansson=2.14-2build2`

Binary Packages:

- `libjansson4:amd64=2.14-2build2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.dsc' jansson_2.14-2build2.dsc 2120 SHA512:46ec9f5477e738ee6ed2c10b7406dd0edcfe0148a394af3ca3ee214b14c9de95e691fefa34c3aa9770c1e23ec77d26b1f5149cc8faa4201f15680ba9f3a6d754
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.debian.tar.xz' jansson_2.14-2build2.debian.tar.xz 5580 SHA512:1eec1f274a77512033b857a64bb26f8bc2fa98212c33c17dcfedbbd7f82711d32a803ad4ea4d8d158ef9949be2a69f3d5d4126fc4ac3b63c9200c361bba0f939
```

### `dpkg` source package: `jbigkit=2.1-6.1ubuntu2`

Binary Packages:

- `libjbig-dev:amd64=2.1-6.1ubuntu2`
- `libjbig0:amd64=2.1-6.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu2.dsc' jbigkit_2.1-6.1ubuntu2.dsc 2199 SHA512:6c5e2f89ed58fd018e27fa73352952192a347c19f8c0a454a2c9e3f9ab90d06bc578f522b32d074100f5de44a8d9d62b3d096fbb7f5f01e2bd803b37a8104de3
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA512:c4127480470ef90db1ef3bd2caa444df10b50ed8df0bc9997db7612cb48b49278baf44965028f1807a21028eb965d677e015466306b44683c4ec75a23e1922cf
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu2.debian.tar.xz' jbigkit_2.1-6.1ubuntu2.debian.tar.xz 11172 SHA512:1ecf331f4e530f5f3105c57c2d7b366591f113220745f143b9335f3e383bf04dd963d61aecc4c8eb16ef4ecc74a2f5e2743779d95dcd8626dc6eaea8b2824c18
```

### `dpkg` source package: `keyutils=1.6.3-3build1`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-3build1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-3build1.dsc' keyutils_1.6.3-3build1.dsc 2211 SHA512:8a40b63e5c4ef4ae645ffdfc865ed91192a7dfc65c8271e59388e63d867b43ac0da90ca1f5e85682886e4561681b83f3bf8bc6a3d90f205dd0feea116f7a30b8
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-3build1.debian.tar.xz' keyutils_1.6.3-3build1.debian.tar.xz 13456 SHA512:ef729447f8f4adebdb986d115e227bd908b346e26115eb7a0385a084ad69f6772c914744d8c24928587247cd5fc329ed1305e9b006db276d0445b9614f20603f
```

### `dpkg` source package: `krb5=1.20.1-6ubuntu2.6`

Binary Packages:

- `krb5-multidev:amd64=1.20.1-6ubuntu2.6`
- `libgssapi-krb5-2:amd64=1.20.1-6ubuntu2.6`
- `libgssrpc4t64:amd64=1.20.1-6ubuntu2.6`
- `libk5crypto3:amd64=1.20.1-6ubuntu2.6`
- `libkadm5clnt-mit12:amd64=1.20.1-6ubuntu2.6`
- `libkadm5srv-mit12:amd64=1.20.1-6ubuntu2.6`
- `libkdb5-10t64:amd64=1.20.1-6ubuntu2.6`
- `libkrb5-3:amd64=1.20.1-6ubuntu2.6`
- `libkrb5-dev:amd64=1.20.1-6ubuntu2.6`
- `libkrb5support0:amd64=1.20.1-6ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.20.1-6ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.dsc' krb5_1.20.1-6ubuntu2.6.dsc 4125 SHA512:6bafe41a37f8bf133ccd7e1aa0d63a1464b411af60ee408a03de69debae259794606011ff42370d168f6bf74af34d90b635c007c9876657af7124259af84c99a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA512:6f57479f13f107cd84f30de5c758eb6b9fc59171329c13e5da6073b806755f8d163eb7bd84767ea861ad6458ea0c9eeb00ee044d3bcad01ef136e9888564b6a2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA512:1d3312bd67581e07adfdadf2c5fe394179631d8add8bd075efefe982a0de22369004e60a14422d426382c8c591e4181b9897088afe9d4e86f0b5a97e5954c67a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.debian.tar.xz' krb5_1.20.1-6ubuntu2.6.debian.tar.xz 122284 SHA512:402e34a374db1ece1ce0a604d84d697c590596d5e99601895d9c50c96fcbd8cb08d21b04201296411324b3ae4f169f2295aff825cee182cbbf139ccb16588fc9
```

### `dpkg` source package: `lcms2=2.14-2build1`

Binary Packages:

- `liblcms2-2:amd64=2.14-2build1`
- `liblcms2-dev:amd64=2.14-2build1`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.14-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14-2build1.dsc' lcms2_2.14-2build1.dsc 2076 SHA512:a07321bc0c14d05183402f5aafac34d2a151a70b3095bfa4380a7fd69bbe443bade7f0079dadfdbb61b6b839caa73b367453697c4fb856fdc668fb5e464e92e0
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14.orig.tar.gz' lcms2_2.14.orig.tar.gz 7406694 SHA512:92fba0a457ea81590eba0b8d98b7b621da6a83e3857948585e0b524235954954f9ac1670cf6a19b457c0fce22a87899ea4c5810db1ff2acf7c6b6e0dc4b61a1b
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14-2build1.debian.tar.xz' lcms2_2.14-2build1.debian.tar.xz 11848 SHA512:a594544bd5350b53112fd18838886859a83178348f0e69cf97f29fc2c9ca89101616527b06f41f31ce1578ab7a90eddaee3653ce139daec6d7abfc3e0bae6e54
```

### `dpkg` source package: `lerc=4.0.0+ds-4ubuntu2`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-4ubuntu2`
- `liblerc4:amd64=4.0.0+ds-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-4ubuntu2.dsc' lerc_4.0.0+ds-4ubuntu2.dsc 2733 SHA512:b9fcf936ebc688ac277f11bc4a1233460d4745269c69d26a71867fc92c06ad7540a81c9275c235b66a9623e7360b03db6a9e1ea7aa668aaa084cae22b174edfc
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA512:d5539360fa92f40319466fea73a66d0d03aedff886fb75985bfcaeeb77ef516b9fa24b8d83da09c114bf6090bbd68e64d9ac2649a19315895134fa86023478e1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-4ubuntu2.debian.tar.xz' lerc_4.0.0+ds-4ubuntu2.debian.tar.xz 7344 SHA512:61f8c1a0b20e3c3016a7787307325e0a56549ff13f88af815bbdfa5e24285e0a090c05ae51b9c9b068b917a64e808cd329c7204e81273169489ba0727e59d1c7
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

Source:

```console
$ apt-get source -qq --print-uris libassuan=2.5.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1build1.dsc' libassuan_2.5.6-1build1.dsc 2734 SHA512:5a430eef8b98b19d7750ab96717a36749fd586533290ae3ab0129d4d7236f34c524e5fcdb7cc1105cf1fa16c64f604956ef36af0eb952cbf1308b61819364f57
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2' libassuan_2.5.6.orig.tar.bz2 577012 SHA512:dcca942d222a2c226a7e34ba7988ee0c3c55bd6032166eb472caf2053db89aeeea7a40e93d8c2887c7ee73c5f838e8b0725e8cfb595accc1606646559362f7ee
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2.asc' libassuan_2.5.6.orig.tar.bz2.asc 228 SHA512:aaa1222607320c260d7339a95cca6532947782520b07df3198a5a228129e0247b87f6f3b6fea17590147fbc7345ea36bfa8da45116d3d85c6fc2d4a3df0f629b
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1build1.debian.tar.xz' libassuan_2.5.6-1build1.debian.tar.xz 14412 SHA512:a09775ff7ab780566ec1385cacb7dcd34b8b418f4472b5285b57d442ab21a4482fa720c43fdd81dda7e042300ff7ff97efa0bdb0ebdf7aa29d71b83ae3ee7b00
```

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

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.4-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4-2build2.dsc' libcap-ng_0.8.4-2build2.dsc 2351 SHA512:bbe5c806e1495dbdd84b80217db334517f792caff349575687e181371c81b2ab503bc120d73eb91bdd084d2a86bec16c852f800fec60ef3ae5c237776f5122f7
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4.orig.tar.gz' libcap-ng_0.8.4.orig.tar.gz 59317 SHA512:3e640ba4bfa2d5b5d0eb463abca3b2c745b10e929571c0ec32eb068bdc41fd95e19f7131893a22ceebb4d1f1083d3d87d9a32f0808442d594ac5940791152acf
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4-2build2.debian.tar.xz' libcap-ng_0.8.4-2build2.debian.tar.xz 7384 SHA512:c21cf4b7df670034773ab883e5149bc28606d11416a5f075c85106395a6d46ea529227e270f9342c910631059b8cf94a55dc5cfa5ec908a6f57d6a8c0a32277e
```

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

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-1.2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-1.2ubuntu2.dsc' libcbor_0.10.2-1.2ubuntu2.dsc 2283 SHA512:69f6e793bc9fc1a23f298a3738fc2d810b8aa243c2426347be18d9bebe7a6b0c7b82177545ec0bb4cc3deb5932228e72576c03026da0d5fe95f34b034ebb0bc1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA512:23c6177443778d4b4833ec7ed0d0e639a0d4863372e3a38d772fdce2673eae6d5cb2a31a2a021d1a699082ea53494977c907fd0e94149b97cb23a4b6d039228a
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-1.2ubuntu2.debian.tar.xz' libcbor_0.10.2-1.2ubuntu2.debian.tar.xz 6560 SHA512:d42dc2b89e3af8c1b65c3d227f1c98a2025f620645052fba062c9bf415830970ed4b3ed47878d5de316661201dafbd69c6c30bb3b40e242dc0b6738df8e6323b
```

### `dpkg` source package: `libdatrie=0.2.13-3build1`

Binary Packages:

- `libdatrie1:amd64=0.2.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-3build1.dsc' libdatrie_0.2.13-3build1.dsc 2368 SHA512:37dc9a866dc340d8291bcb07cdb8a20f39ba8ee0dca0c8c37cbbfb9403afe0a8229b18f1d019a54d19855977ac499df9067e7ecdf0a297cedc4d239e67353272
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA512:db3c879d825ead5871c12ef3a06bb093cb1708a6e7e20775eaf82356af9dd6ad54c6b5cabbe1773f2494d3dfa2426528fdd49441038b6294b70ccb1a3d90099a
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-3build1.debian.tar.xz' libdatrie_0.2.13-3build1.debian.tar.xz 9776 SHA512:a44919cfcb079af400a09c4f9468cf16edc3fc05fe46bf57b7a22abd80130da91b5ce3b6d8c8cacfa8c0f48b751220b0b74bc624be433db01b3ab1aac9bc6524
```

### `dpkg` source package: `libde265=1.0.15-1build3`

Binary Packages:

- `libde265-0:amd64=1.0.15-1build3`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`

Source:

```console
$ apt-get source -qq --print-uris libde265=1.0.15-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.15-1build3.dsc' libde265_1.0.15-1build3.dsc 2320 SHA512:c8eecbe84945f0f003aebce4faeeada1cb109d73e8adeb161605a257ad62f9328a468a901c279fc736f76de312eae57434912a44d1eb358a0d82aef6c9d34400
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.15.orig.tar.gz' libde265_1.0.15.orig.tar.gz 846016 SHA512:375d8e781108247e0e8b4d7a036d20cc5d0670bdbf6ddb40a6d3dbf912fa776d2f001fb762301cb97e4d43be29eb415b0cdbfc6e07aa18b3f2346f7409c64fce
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.15-1build3.debian.tar.xz' libde265_1.0.15-1build3.debian.tar.xz 136752 SHA512:1ad17c30fa4cbea21b694af718d5f3b7f36f747dd4605bdd2b872f22e6a15e34fd88588896c617b195f06acca5e011b2821bad771ab93376c82eab9e6f0cdd65
```

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

### `dpkg` source package: `libedit=3.1-20230828-1build1`

Binary Packages:

- `libedit2:amd64=3.1-20230828-1build1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20230828-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20230828-1build1.dsc' libedit_3.1-20230828-1build1.dsc 2399 SHA512:4cd638bfcb6204c6c3e141fb25b5fe8e06ec328a24dd32414d96a061c3f314c25bf498dfa1ed74e8626eed42fd96fe34c72adcf18ceaaa35f6e9bd948dae6a47
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20230828.orig.tar.gz' libedit_3.1-20230828.orig.tar.gz 534072 SHA512:c7232376ef1bc128ed79f950a5f1f207f874011218682d7e6186f76443927df5483b46c4daa8cf02e327079259aee1a56e2b791aa682491eb802d90ff8940cca
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20230828-1build1.debian.tar.xz' libedit_3.1-20230828-1build1.debian.tar.xz 16748 SHA512:68b5c9a1ec13f38993a2a04976ec8471ad7ca8ece5dc17ae7501c143dbb29dca922594f82bff6240136abf7948fbf5d3791fc9cfa7ebb60c225fd86c9dfe04c7
```

### `dpkg` source package: `liberror-perl=0.17029-2`

Binary Packages:

- `liberror-perl=0.17029-2`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17029-2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.dsc' liberror-perl_0.17029-2.dsc 2085 SHA512:9b469f24ebdd65c5aacfa41b7099cb1fec5214d98e6e0d793d55a56bc0f0edae8f2ad3c0e09f44558249ff5456f05704c213d7e84661e0e4d774e644d3fd405a
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029.orig.tar.gz' liberror-perl_0.17029.orig.tar.gz 33304 SHA512:266ba1feff897c1d162e69a83e595cb40da9a6e1d8b10cc5531626eff392c6da94be03ba722c74827fc2ea0d9d1c1e62e824d9021e098b700db65dd0b3acbd0a
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.debian.tar.xz' liberror-perl_0.17029-2.debian.tar.xz 4608 SHA512:beb596444319797a60470e98c14e8e736fd5be9c307ba5482fe96bf77c1382603b1f2a58d68406ecbf2bc5469cab4654645f5469cf059336fef24605b235cb61
```

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

Source:

```console
$ apt-get source -qq --print-uris libevent=2.1.12-stable-9ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-9ubuntu2.dsc' libevent_2.1.12-stable-9ubuntu2.dsc 2551 SHA512:8a52a85db1ad2dab17ad21cb4f90776fbc5ba554bf1936132e70d44c4ddbd92e2b2b76fdae5651ef552d56f66c01c2839783499e09cb1cd8a80d731f809ef695
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA512:88d8944cd75cbe78bc4e56a6741ca67c017a3686d5349100f1c74f8a68ac0b6410ce64dff160be4a4ba0696ee29540dfed59aaf3c9a02f0c164b00307fcfe84f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-9ubuntu2.debian.tar.xz' libevent_2.1.12-stable-9ubuntu2.debian.tar.xz 18092 SHA512:6e97ccc6586c201ae5c6c785c371a914331a2c65d41b10d8a09899867d5c74f9407abb37f05b173c8b2e475e50a34560c6526ebdbd957bbab0f30741c9640165
```

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

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.24-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24-1build2.dsc' libexif_0.6.24-1build2.dsc 2211 SHA512:d0172894995cb89f271addf6b735d6e3a79e55f4d1dd8c71b4475f277ffe2f16516b843c72a9351e493470365a9274264ed242aed537c1effdbecf9ed3ac5310
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24.orig.tar.gz' libexif_0.6.24.orig.tar.gz 1140079 SHA512:0b15a157c1030490bf1c4239487dffda90daad467ac6281db2a1b34a8419fca32b4b5265452e75cbcd2c9dc9a829643231cd3749e88251ed1b596756d1c5a9f4
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24-1build2.debian.tar.xz' libexif_0.6.24-1build2.debian.tar.xz 11872 SHA512:24a2e46cd80073ed6b943d13f42078dbf9eac53c156c53d7c1f17e4a3a2b63b4e431d3d869bb38e675c39fe22bbc9ccc5e846d7d718397665c7d995b1c4916cc
```

### `dpkg` source package: `libffi=3.4.6-1build1`

Binary Packages:

- `libffi-dev:amd64=3.4.6-1build1`
- `libffi8:amd64=3.4.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libffi-dev/copyright`, `/usr/share/doc/libffi8/copyright`)

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
$ apt-get source -qq --print-uris libffi=3.4.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6-1build1.dsc' libffi_3.4.6-1build1.dsc 2055 SHA512:21cc7b6880fac7c143e88a81c47e5144d38bea3fd66f71182d1408f56bfc6801d39481638e04c02bb29dfc2429e3d968b65591cf95d20cfeca6769684d3c86ac
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6.orig.tar.gz' libffi_3.4.6.orig.tar.gz 598175 SHA512:cbacde8911aa6a9fae5c0a8d5959221a25bf8a3310c44a7f4ef755e6676f5226b9f2d1c6cfb36c117ebed10d379aa24b4b7516c3e0dca3bf73f9439057463eb8
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6-1build1.debian.tar.xz' libffi_3.4.6-1build1.debian.tar.xz 10736 SHA512:432e6e7ddb9aecca508f982293112b2bf86f5da2d6d646437b10b2857dadaf2c8aecb1646d2e592c259df26a5240f69cc1411155cbad8c3d942748d6856e587c
```

### `dpkg` source package: `libfido2=1.14.0-1build3`

Binary Packages:

- `libfido2-1:amd64=1.14.0-1build3`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.14.0-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0-1build3.dsc' libfido2_1.14.0-1build3.dsc 2577 SHA512:1f0c68213816f6d8584c56db3dd02af78300a252a1582eb4c632716d3612876bcec28ed1fd06718b9fc49f47d34afe94dd5517800b99f53ece6e426da1fbe9cd
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0.orig.tar.gz' libfido2_1.14.0.orig.tar.gz 660289 SHA512:83454b0db0cc8546f377d0dd59f95785fe6b73cf28e499a6182a6ece4b7bce17c3e750155262adf71f339ec0b3b6c3d3d64a07b01c8428b4b91de97ae768f0e6
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0.orig.tar.gz.asc' libfido2_1.14.0.orig.tar.gz.asc 228 SHA512:0f0116e1eb13d1fb18bddba6817e8f279a316fe0d74631fb350ba4c71a09cfdeffc12f4f5664e49575bfb1a334794e9f82c3151a02ab6d3fd27c21d9f5f60c20
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0-1build3.debian.tar.xz' libfido2_1.14.0-1build3.debian.tar.xz 53020 SHA512:b72646b327d602059f6dd2c3e8ac57118ce75e4342b94665e1fd3771b2d3c132831ae51b67d2512a383f30d9d51903e8a423003825e3f75e8470b8f5ab9c63d6
```

### `dpkg` source package: `libgcrypt20=1.10.3-2build1`

Binary Packages:

- `libgcrypt20:amd64=1.10.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.10.3-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2build1.dsc' libgcrypt20_1.10.3-2build1.dsc 2931 SHA512:bb535ccbaaac49199a4483dbf31799f9b4ecccdeec42294baa850879187df7afe57f187c7f16ec3e248905f99e01ba3a46b7a56e23780596716e8e8f4237b772
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2' libgcrypt20_1.10.3.orig.tar.bz2 3783827 SHA512:8a8d4c61a6622d8481ceb9edc88ec43f58da32e316f79f8d4775325a48f8936aaa9eb355923b39e2c267b784e9c390600daeb62e0c94f00e30bbadb0d8c0865d
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2.asc' libgcrypt20_1.10.3.orig.tar.bz2.asc 390 SHA512:9b176a7bca3b8521fe03c3f771a3d039c4e1da98f6ce61f6c1bbb485e5785ca58e191c4eb54d6c69a1ae79e82d786c22836bef96d30d7b9852b508f3b65fb15a
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2build1.debian.tar.xz' libgcrypt20_1.10.3-2build1.debian.tar.xz 36604 SHA512:f203bb66fdbc4f45c512c768e36e13510bdf26eb04e8f78940299dc5bfed9ddf624a65a0a49b734314dee9362a178721d148aaf6b9723bcd9c7e627a52816a75
```

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

### `dpkg` source package: `libheif=1.17.6-1ubuntu4.1`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.17.6-1ubuntu4.1`
- `libheif-plugin-libde265:amd64=1.17.6-1ubuntu4.1`
- `libheif1:amd64=1.17.6-1ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

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
$ apt-get source -qq --print-uris libheif=1.17.6-1ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6-1ubuntu4.1.dsc' libheif_1.17.6-1ubuntu4.1.dsc 2919 SHA512:99daf14e1a3a62edc74662f4f5debd96683ca535847efd9651b03b1d471ffe0473ade05537e4e5f1870563da3e7e641cfcf6765c8c51e75f479a408399250902
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6.orig.tar.gz' libheif_1.17.6.orig.tar.gz 1433302 SHA512:47d93df4f584979cea26af74cd8543b13398356b5fd46b1b378f7738cee471e80b7e117f6ce307674a549182f5ce22a577c6e79a6e72fe166421efc4be04687a
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6-1ubuntu4.1.debian.tar.xz' libheif_1.17.6-1ubuntu4.1.debian.tar.xz 11888 SHA512:c82432484bb5b248a421a1c20d8512ddce57b6fcb1b2b9b4799e7b68037b05e30ee1981433275d6000086307d10494feb7a39bb77f8fb00682e08109f4f106e4
```

### `dpkg` source package: `libice=2:1.0.10-1build3`

Binary Packages:

- `libice-dev:amd64=2:1.0.10-1build3`
- `libice6:amd64=2:1.0.10-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build3.dsc' libice_1.0.10-1build3.dsc 2181 SHA512:7f380aeae73731a89a717a8374072b7beb2bfcccc89086b2e1f5d3f9e790783e318c337c4282f7fb73b6512d04667c1a66818617b6089548032bcd226aee58aa
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA512:2d4757f7325eb01180b5d7433cc350eb9606bd3afe82dabc8aa164feda75ef03a0624d74786e655c536c24a80d0ccb2f1e3ecbb04d3459b23f85455006ca8a91
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build3.diff.gz' libice_1.0.10-1build3.diff.gz 11722 SHA512:a643009809766e385b9eaf7fddbf4ff4acdc5dc98b5a8a8bb940c4ead4e635d13123494e5cbecad487cb7b7d1cf4ae826f957ef1e552362f2efe483057cb9916
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

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.5-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2ubuntu2.dsc' libjpeg-turbo_2.1.5-2ubuntu2.dsc 2535 SHA512:aaf83542c31e42beb369561f0eee167e6bbb117d535f145a82c029926ba8cbc66a4e2593a608375d63e5aa0fd5d3d0bfa0d4d638168918afd9a62959e3a38079
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA512:20036303fbe5703a5742dc3778cc5deb2eb98d00a9852e7e80ba73c195bba011ec206c090589c482f1153f74505c3fe06d96af00f6beaa65a7fcf7ffaf626fc2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2ubuntu2.debian.tar.xz' libjpeg-turbo_2.1.5-2ubuntu2.debian.tar.xz 108492 SHA512:52a61609f8aa4397be2ff97f40fe8429543d82a1a0bd3bcdee43e79640a0342b537ce7a2d31268172760d9de75683a534609db9ce66874fb20eac3dcb9419038
```

### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu11`

Binary Packages:

- `libjpeg-dev:amd64=8c-2ubuntu11`
- `libjpeg8:amd64=8c-2ubuntu11`
- `libjpeg8-dev:amd64=8c-2ubuntu11`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg8/copyright`, `/usr/share/doc/libjpeg8-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg8-empty=8c-2ubuntu11
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.dsc' libjpeg8-empty_8c-2ubuntu11.dsc 1579 SHA512:345994a54ea05e741e0e6d35f0a7fc39f45c3fc34a995e972ae6b2843baf0b2fcc0bf4726aa7bb86249e39f46a7e23a273d2430d0fcb9bb88f03c6e9d3c912aa
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.tar.gz' libjpeg8-empty_8c-2ubuntu11.tar.gz 1959 SHA512:eb9cec5b6f3fa5e65950b72c14709d33e638b52a2bd2ac2f2297e0edb9e9e224e6da9bbe355e082026b92d980614e8fe40196e4a3ed7cdd560a65f03b138782b
```

### `dpkg` source package: `libksba=1.6.6-1build1`

Binary Packages:

- `libksba8:amd64=1.6.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6-1build1.dsc' libksba_1.6.6-1build1.dsc 2622 SHA512:9905b22e5b0cdce554951103b8fe95a259aca936f96e90380538f05065d3f1b27a7eee8f54f9372731413c245aa2506614baa8567cdba1a56850765dfb8572fd
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6.orig.tar.bz2' libksba_1.6.6.orig.tar.bz2 708510 SHA512:3b30bef9452ae0c52b4a52e9145fbd6dc57cf7a2b59302e3af063db6b45384e8ed7af62604efd7939b9e0cb5931e946b15609888e9699fafe4acbb0cbf138087
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6.orig.tar.bz2.asc' libksba_1.6.6.orig.tar.bz2.asc 228 SHA512:5bfd9441b3e46b24391c5d9360747c9eaabf9d645ceae27af241d4ed1f7e9cc0fb538dc6d8db757d444eefa8d45b2082fd055256160c59d97bf5121f05d750ef
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6-1build1.debian.tar.xz' libksba_1.6.6-1build1.debian.tar.xz 14816 SHA512:12251deb546de2d2ba6dc2a7f8c01a22218579de7e9a16ae6ecf728e07404fc601bd85f43ce907c056dfdbe9c584887acef9f9a5a7090c75a3fb2c8d2e50d0c3
```

### `dpkg` source package: `liblqr=0.4.2-2.1build2`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.1build2`
- `liblqr-1-0-dev:amd64=0.4.2-2.1build2`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.1build2
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1build2.dsc' liblqr_0.4.2-2.1build2.dsc 2096 SHA512:30b38f252c27f4d20ef46e5c923eb0da2ba7e32fdb4277181980c6e0f82de4d5624cfd51339a3a16883357b1f6db4f6b8cf827be09f14c882752ec866ed5ca08
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA512:acfa5868c41ea145092711e84d6c9eb62cb725b3d7531917b0d91b7d4af2a9912b18a96edc2594a826f09dabe0a0a82936ceea7d1f31301a23d558b1450d2547
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1build2.debian.tar.xz' liblqr_0.4.2-2.1build2.debian.tar.xz 5448 SHA512:ff140c20c1683b3fc3c4a91682d72214a39ce60b4a3ecaf9bbfdf6229b79a48e2d38e26009f2243dafc953bad3c54ef8520de2dad51b762ba0d019691a678ce2
```

### `dpkg` source package: `libmaxminddb=1.9.1-1build1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.9.1-1build1`
- `libmaxminddb0:amd64=1.9.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `CC-BY-SA-3.0`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.9.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.9.1-1build1.dsc' libmaxminddb_1.9.1-1build1.dsc 2454 SHA512:1a91edbd7ca9637e4b3acd1f13322934f079be91c727cc4f540adb1d7104df708f37b428b5f988e4dd05b475b94f78df12b565f0ccf8be958fe49a4819739462
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.9.1.orig.tar.gz' libmaxminddb_1.9.1.orig.tar.gz 243507 SHA512:bd3d0f65a80df52da39be77457dd68fc1bc64f2cf37c3ec0f24af97e6ff00fd0423969a9016cc7bd97dbb04dbdf3bd56597c88039b9d98526032ab845c070c2e
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.9.1-1build1.debian.tar.xz' libmaxminddb_1.9.1-1build1.debian.tar.xz 12604 SHA512:906cd6a42c21ed640527d8234de1264285c0e5c934b059b43d170059fba08c6846a39f0c53af7dd71105f96b503d0934626a9025e0aaf921263a4a9e6cb5c052
```

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

- `libpng-dev:amd64=1.6.43-5build1`
- `libpng16-16t64:amd64=1.6.43-5build1`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16t64/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-like-with-advertising-clause`
- `GPL-2`
- `GPL-2+`
- `expat`
- `libpng`
- `libpng OR Apache-2.0 OR BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libpng1.6=1.6.43-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5build1.dsc' libpng1.6_1.6.43-5build1.dsc 2409 SHA512:487fe71c92bdbe2836e4080a88672d98b43460d80a2862083a49483d6e7bab5526aac351ce265dfb4c8624d638fae92e92ce94051ed066290db4e894400ff452
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43.orig.tar.gz' libpng1.6_1.6.43.orig.tar.gz 1554715 SHA512:3bb2a7b73113be42b09c2116e6c6f5a7ddb4e2ab06e0b13e10b7314acdccc4bb624ff602e16140c0484f6cde80efa190296226be3da195c6926819f07c723c12
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5build1.debian.tar.xz' libpng1.6_1.6.43-5build1.debian.tar.xz 31552 SHA512:17ba92df092d8ab879bf2069ba21c194d793e5bc4b70e21d55dc03623a92bf2a292c678611761d2d76cfed9e0a12de03fd73e919b1419a27e39fbb25a3968f33
```

### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.dsc' libpsl_0.21.2-1.1build1.dsc 2425 SHA512:f6036e1386802ab44ad0d65b81f4e81dd2ac084da738752f058d58f8d96074b2ab7b00e8275cdd73bedb18d5ae6ba1fc4b19fb95d4b61e58df5695225629ef7c
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.debian.tar.xz' libpsl_0.21.2-1.1build1.debian.tar.xz 12244 SHA512:316b41dc3611a45c0b7ab0ec7fc617d2c710f8e11d943daefa524fc92155b63e777504a11dbe1b8427e1ad6d15f98095c90cd115df71fb8f90449a461dc9cd3d
```

### `dpkg` source package: `libpthread-stubs=0.4-1build3`

Binary Packages:

- `libpthread-stubs0-dev:amd64=0.4-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libpthread-stubs=0.4-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpthread-stubs/libpthread-stubs_0.4-1build3.dsc' libpthread-stubs_0.4-1build3.dsc 2034 SHA512:40fdd1e868a59c32e39f3cfad4665d2279e97f2005967bc94e62d5f3b3a02bb1cad1b5e506173ed7e2ac4caeb56827b86cf196e06df16bf57251aea400345b5f
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpthread-stubs/libpthread-stubs_0.4.orig.tar.gz' libpthread-stubs_0.4.orig.tar.gz 71252 SHA512:5293c847f5d0c47a6956dd85b6630866f717e51e1e9c48fa10f70aa1e8268adc778eaf92504989c5df58c0dcde656f036248993b0ea5f79d4303012bfeff3c72
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpthread-stubs/libpthread-stubs_0.4-1build3.diff.gz' libpthread-stubs_0.4-1build3.diff.gz 2591 SHA512:b5e76d1bf48a277e5422be4b237c7b439e8a5c9cc0d9802053a995df38b9e84c47a77d07fbd673d0a251cdcf1cc00d915c562b9d60809a0d8d9ddaf791d23e75
```

### `dpkg` source package: `libraw=0.21.2-2.1ubuntu0.24.04.1`

Binary Packages:

- `libraw23t64:amd64=0.21.2-2.1ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.2-2.1ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.2-2.1ubuntu0.24.04.1.dsc' libraw_0.21.2-2.1ubuntu0.24.04.1.dsc 2185 SHA512:3e1292e4048be1750642a3562e66d675ea0ba20b7cc371bb1bcc2892e88f1814aa72e8f2d124fd2e2d927417526cb9d5ad0d5a045ff682b2ff0a0850de7a69f5
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.2.orig.tar.gz' libraw_0.21.2.orig.tar.gz 565383 SHA512:a8b0ec275cc0055d6eb2069008c3312ae007cd86e481111f68d5d60544afcd76b728f8418bf63a80d35d7d00283536da63e03f5eecb4cc28f4cc8d92070e8b39
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.2-2.1ubuntu0.24.04.1.debian.tar.xz' libraw_0.21.2-2.1ubuntu0.24.04.1.debian.tar.xz 26708 SHA512:aa0c99fdb4a308a4371e8c6f27e4f28461d0641b882904e3a1cec6922478e4b9b449eb9ef64876cc24edf1bc69991f5cd7f8a235061465b16042c6da67119717
```

### `dpkg` source package: `librsvg=2.58.0+dfsg-1build1`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.58.0+dfsg-1build1`
- `librsvg2-2:amd64=2.58.0+dfsg-1build1`
- `librsvg2-common:amd64=2.58.0+dfsg-1build1`
- `librsvg2-dev:amd64=2.58.0+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-rsvg-2.0/copyright`, `/usr/share/doc/librsvg2-2/copyright`, `/usr/share/doc/librsvg2-common/copyright`, `/usr/share/doc/librsvg2-dev/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris librsvg=2.58.0+dfsg-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.58.0%2bdfsg-1build1.dsc' librsvg_2.58.0+dfsg-1build1.dsc 3208 SHA512:fcc1491830d429dedff8a131269a86b9f96f9c86cf0120edc2c6d5d884b35e8a6931534628fd8dc3c5cb8ef886fb8b9196afcfbe15df92e4bfba5936dd4a49a6
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.58.0%2bdfsg.orig.tar.xz' librsvg_2.58.0+dfsg.orig.tar.xz 5736316 SHA512:30458b535b88a3c49645aee444dd690b6b70d332f54eb7b0159c26fab816ee7ee9443ee52f6f61a5e93f37cf0ab18351d27deb43b3419bdf8a93162fa964234a
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.58.0%2bdfsg-1build1.debian.tar.xz' librsvg_2.58.0+dfsg-1build1.debian.tar.xz 29508816 SHA512:323561cc3b7df571f2e975e98895637056e4513392f141877b7a5b71e3e10f188de7fd6a73b481a066d9aeb8b4c6875f69bb3984842f0a08529f016fb63b3906
```

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
- `libselinux1-dev:amd64=3.5-2ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1build5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build5.dsc' libsemanage_3.5-1build5.dsc 3105 SHA512:310dd2c109462b4f44ddaef331f6a72758efd42d31591daba762fc629e2915c6dc6a16fccbb933089a406aea65b886e3408e10b49e2471abbad37a30c260ed0d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA512:959fbd0d6bc6849da6caa13dc41c3f8818cbbd29f04b5d2ac7246c4b395b4f370f113a04cc9cfcb52be2afebfa636013ac4ad4011384c58c7ce066a45cae2751
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA512:c0a5ddb69c32ddefa26b3d1ec676bcc373e959dd8b4a7fcf6e1f74a3ca8e9af22af851ca66d3c43a704215ff79d27244e33d23038ef2f52ccc321aeb5f0c2790
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build5.debian.tar.xz' libsemanage_3.5-1build5.debian.tar.xz 30188 SHA512:13561dae7133d128bc5db3528e38be2e9469e35a4796e92f192af3c95c29abb3934542244777d0f0754cc1f652ea816334b7fc5fe94d637fb35bf76a399059cd
```

### `dpkg` source package: `libsepol=3.5-2build1`

Binary Packages:

- `libsepol-dev:amd64=3.5-2build1`
- `libsepol2:amd64=3.5-2build1`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.5-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-2build1.dsc' libsepol_3.5-2build1.dsc 2458 SHA512:d28b899278cfcb721f13e512142e2540c2ec064458d6d5bee607b3b313b260a2a19e5d5131fc7dcde6edfbf24d73eaede6597444770d6be31011d861a1d72676
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz' libsepol_3.5.orig.tar.gz 497522 SHA512:66f45a9f4951589855961955db686b006b4c0cddead6ac49ad238a0e4a34775905bd10fb8cf0c0ff2ab64f9b7d8366b97fcd5b19c382dec39971a2835cc765c8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz.asc' libsepol_3.5.orig.tar.gz.asc 981 SHA512:5aa46c3a7a5d7fa0d4376766b9444cdea1b14f3ec61725950a24fcb5ba2caae271a415c613807d06e4d9b04b40cda1525c12c442eed8a7e60fb5e5beacdaba3b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-2build1.debian.tar.xz' libsepol_3.5-2build1.debian.tar.xz 27716 SHA512:9b2b126368c5e4f80d80940f7611103745b1da92bec6319f43f64cc3f6a5e13bab25758bad645e973773a4aab74fa3600694061a8368ca2176252320c0d9ebf6
```

### `dpkg` source package: `libsm=2:1.2.3-1build3`

Binary Packages:

- `libsm-dev:amd64=2:1.2.3-1build3`
- `libsm6:amd64=2:1.2.3-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build3.dsc' libsm_1.2.3-1build3.dsc 2170 SHA512:8a520e3ffb431799786f69aecf52ad9ebd54d0c2146aa9ba79cd7c7d301aff12da18fa10cb3c9abdab3a6ff7f36f08c3ebf3625312ec306453bf54a5e370f704
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA512:03b77d86b33cdb3df4f9d65131a0025182f3cb0c17b33a90d236e8563b3011d225b9d006186302d07850edafa5b899aec6a086b8d437d357cd69fedd5f22d94b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build3.diff.gz' libsm_1.2.3-1build3.diff.gz 9110 SHA512:9d091a10e743ee293094e270865b4499e77d0cee4815dfb21d42a53832d50ea82a599e6bf8945bfd1c51add353de20d77eb672dc666400c98b5c8a390b6dec2c
```

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

### `dpkg` source package: `libthai=0.1.29-2build1`

Binary Packages:

- `libthai-data=0.1.29-2build1`
- `libthai0:amd64=0.1.29-2build1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.29-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-2build1.dsc' libthai_0.1.29-2build1.dsc 2451 SHA512:63a4a7a95532beb3aed3d7311b7f341689b89b0ff87e112a02a03448408a14464c4ad3339e16a1fae76fefacb8e72286850494c907d8c49e0c7eb83651d7ab36
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA512:0ba1261581a1705a2a2546a3071acb3c63892dbf111f0dad415667165a6b9542a5e4549061c67b11ec53de7c9e70fceb3c04d794fd12a22d991a539dbacebda1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-2build1.debian.tar.xz' libthai_0.1.29-2build1.debian.tar.xz 12744 SHA512:40ede6bac42730219a2df5db772814ff4185e5464ea33ebde225b8a068bbbb277c5201ba6f0e6f8e57fdf2733925ead1b54a86463073cb79c402fde101774577
```

### `dpkg` source package: `libtool=2.4.7-7build1`

Binary Packages:

- `libltdl-dev:amd64=2.4.7-7build1`
- `libltdl7:amd64=2.4.7-7build1`
- `libtool=2.4.7-7build1`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.4.7-7build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7-7build1.dsc' libtool_2.4.7-7build1.dsc 2389 SHA512:7617c6e809ba2cd2be45b5da2142386214c7c3badd4655efe135032706e285655a407eba20615e59173b36cf437039fbc2819e865a973a93fc2664b43cf0fa8a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7.orig.tar.xz' libtool_2.4.7.orig.tar.xz 1026028 SHA512:424f4549aa713917859dc31e62153934c67b8b9d5718452f0e50bb8f6ef48ae6274cc4d4ddd905b15858d19c60daf8c194471e6ed0c8f76e7d55e7ef932a8d3a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7-7build1.debian.tar.xz' libtool_2.4.7-7build1.debian.tar.xz 41052 SHA512:a96fff303067f7e0bb71534f5ec2777c737127cb6540a196a5cdad7dc1731a83d006b13addf0d4c422a4b2a7526df65a5f19ae52aa2063518871c6b04d7ece29
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

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.3.2-0.4build3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.3.2-0.4build3.dsc' libwebp_1.3.2-0.4build3.dsc 2468 SHA512:6ff5c7d8eb701dbf23e729287e65b20c0d1140f2a7b0054d30e1fd51545796f1b4dda83e8e6ca62e44ee96f8ebb42d4a7521931526ecd5ff49d7cfa43e868843
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.3.2.orig.tar.gz' libwebp_1.3.2.orig.tar.gz 4162949 SHA512:2b624d2ecfbff6b4db2719e38f146722638ae262acd96327073a04451dd05fb27ef70c5681187821d251df728a6be7e89209c861c561a13bfb786495a830bc20
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.3.2-0.4build3.debian.tar.xz' libwebp_1.3.2-0.4build3.debian.tar.xz 15816 SHA512:67796f091daf95214880955c3c6a430b6622d525e2db65d52cc4072364a253fb0263e5faa0307cd50e59c62ed3dbfbc3ea234134d3ffac3967fb45da9c9546fd
```

### `dpkg` source package: `libwmf=0.2.13-1.1build3`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-1.1build3`
- `libwmf-dev=0.2.13-1.1build3`
- `libwmflite-0.2-7:amd64=0.2.13-1.1build3`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-1.1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1build3.dsc' libwmf_0.2.13-1.1build3.dsc 2635 SHA512:c14c4480ca692ed9652cb54f75bac5ddbb79dc9a4fc2c3661ee6d52979e1f5d6fe454c5df1a418838383fb1eff3fcf4b151f770d156cbd3fed5a01d557f09bc7
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA512:f45a936c9bc98fc1a5f2b0808b497119e4dcd3c132615fdddb7583e5719c7d1d7f85c16ebf313cad453e5b7ae3508bf6b80c4ed2b42322b7dec295d8f4eb86ce
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1build3.debian.tar.xz' libwmf_0.2.13-1.1build3.debian.tar.xz 25912 SHA512:0a2a4aeef81c7644eeebaa5ed800c26107472244667814477b153b0597c7fc9c8f2684e6e3a2bc4f3607e84adbcfa09c88116795eb21146b5fa792f0e87372be
```

### `dpkg` source package: `libx11=2:1.8.7-1build1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1build1`
- `libx11-data=2:1.8.7-1build1`
- `libx11-dev:amd64=2:1.8.7-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.7-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7-1build1.dsc' libx11_1.8.7-1build1.dsc 2612 SHA512:a18064c14d2b134395187fb20df777148669e91b3d48ff92bff35ab120daa3ca267d9d66ca5dc43315714a395a978021669d4ced1ac3d77feb11f1861f4fd20a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz' libx11_1.8.7.orig.tar.gz 3185363 SHA512:67575740356aecc6a7a4898e92ff1007aa6a44ff506d80fe577c1bdc3d64a900edf545cf3e082e9f17c25f4afe28e724145d5e82ae428bdc44348d368d9451a6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz.asc' libx11_1.8.7.orig.tar.gz.asc 833 SHA512:92c410ca14412092680bd511f9536fcf1eb1f32632c33fb833246f8c90bb6dcb8045b9e12cbffa0b6093bf91fe8897ba76d2abb4303a343b4b7deb3b586098b4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7-1build1.diff.gz' libx11_1.8.7-1build1.diff.gz 74380 SHA512:009bf70e5acec4708f2d734f69c224674497c6a8eb9cbb2bff511ffb141fa79d3041e1dbcea669278626358ac03b9a918f5b4d8a03ac9ab49fd9c2ef792dcb9c
```

### `dpkg` source package: `libxau=1:1.0.9-1build6`

Binary Packages:

- `libxau-dev:amd64=1:1.0.9-1build6`
- `libxau6:amd64=1:1.0.9-1build6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-1build6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build6.dsc' libxau_1.0.9-1build6.dsc 2315 SHA512:7cb47244c991544aed1268a831fbbd157713cbefb6252c8fe863522b6f1e3f1bd4dab892fbecdb253246c2fe34cd48a838b1139bdbc59e2cbd54cf1581af57df
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA512:3b22f34a4e35d17421189df8ce3f858b0914aef0cea0b12689dd8576f14eb811e39d6e32384251573daa7e3daba400deea98e7c0e29b4105138cf82195d7f875
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz.asc' libxau_1.0.9.orig.tar.gz.asc 801 SHA512:e59b2944591499d0c0291a8d80ad8ee2cb13ee00c32b0d26c6af12a2bb96c947d4d15924ef15b377b8d7640b75b50f9b8127ba53c582090b3f73b7bcf9e00b01
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build6.diff.gz' libxau_1.0.9-1build6.diff.gz 10712 SHA512:49c075d30bcadd86ea03acc160824d06f32c65c5cd71e6f08ba2aece7ef719980f595f54f106d0c4d8e3d35d00e922289516907e7ba56741065253879faeba03
```

### `dpkg` source package: `libxcb=1.15-1ubuntu2`

Binary Packages:

- `libxcb-render0:amd64=1.15-1ubuntu2`
- `libxcb-render0-dev:amd64=1.15-1ubuntu2`
- `libxcb-shm0:amd64=1.15-1ubuntu2`
- `libxcb-shm0-dev:amd64=1.15-1ubuntu2`
- `libxcb1:amd64=1.15-1ubuntu2`
- `libxcb1-dev:amd64=1.15-1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.15-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.15-1ubuntu2.dsc' libxcb_1.15-1ubuntu2.dsc 5372 SHA512:6dc4a78314ca9afd78fbbdd5fd5d966819d72815815052e192b95c0a390cf15b5ac5551832072cbc2a9522e6022063c633883ccf0a537aeca894fc596da8b5fb
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.15.orig.tar.gz' libxcb_1.15.orig.tar.gz 650774 SHA512:4099899c37fdda62a9a0883863ee9e50b5072e8f396ba6f4594965d9f1743fb6ea991974a99974c6f39bac14ce9aad5669fa633ac1ad2390280d613cc66eb00e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.15-1ubuntu2.diff.gz' libxcb_1.15-1ubuntu2.diff.gz 26975 SHA512:ad67cab4521b787432cd2b0387eb84131903c5d135e0f2bd7ddbc2cc9966da769692591c2c53372f558e74210d998e5d57f4674635461be577b29c177ee0825c
```

### `dpkg` source package: `libxcrypt=1:4.4.36-4build1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-4build1`
- `libcrypt1:amd64=1:4.4.36-4build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4build1.dsc' libxcrypt_4.4.36-4build1.dsc 2300 SHA512:5e9c4a5c26299ac291eb755a9a386ddaac65d6af2e6b9cc37c2803101e1d8b257a83eb36c12f2955873ee99a0a95f61ad2a204e5e5a2c88d33f043a426121c32
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA512:82839d70fc068a4d4d5e14488ea7599e2430091ace53640d639628330eff52a058ac589b6b5a39bc6c83166e68cbf9b9e2024e0371df1f949336f633f2a1726e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4build1.debian.tar.xz' libxcrypt_4.4.36-4build1.debian.tar.xz 8356 SHA512:d181e5637d40e322cf03d80dff03acb9982c0a07a73229d660d8b2fcd02f31783347c0b0208d2ebb077bdf44e87330b04a8cd10a4bc272dbb0feca7f1adfe013
```

### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu6`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.3-0ubuntu6`
- `libxdmcp6:amd64=1:1.1.3-0ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.3-0ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu6.dsc' libxdmcp_1.1.3-0ubuntu6.dsc 2252 SHA512:daa70b073691db6046dfb0900d5dac63daa213b96b8e019e132dafc12d0cd0c9167c9216d823191ddfbabf16e6290073229f3b6ba310c86234a13e05c3cbc28a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3.orig.tar.gz' libxdmcp_1.1.3.orig.tar.gz 429668 SHA512:edd05654ad9ea893e9e08269e25ea050d10eaf9f997a08494e24127d1ba0c896cd5338b4595b155c8cbf576e1d910b76e6ad7820fee62d74644f1f276551e2f2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu6.diff.gz' libxdmcp_1.1.3-0ubuntu6.diff.gz 18400 SHA512:5b6effc30e3f6dba946dd95c73d3242210d99612aec3dc8df4fe986a42758e7d9c6ddc7a713375edb0c78a1875e64872ca9329c8d5be83984c66e8457c355c23
```

### `dpkg` source package: `libxext=2:1.3.4-1build2`

Binary Packages:

- `libxext-dev:amd64=2:1.3.4-1build2`
- `libxext6:amd64=2:1.3.4-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build2.dsc' libxext_1.3.4-1build2.dsc 2250 SHA512:6b9b001f4dd81843f12ca625bb90a8ea78dda531f80d6fc9c90c071b6cc925d94c53b2d20abc42d21df77904ff5ba059025ce426cf25838918040da71b1a6ea4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA512:4eebd639fd57cb9b84a1e17e368f82fbf3d9f021eef5ad3fe31dd128500db57862a82c1e0d214d447cb7641b2be3fd7e949ee1196f2a482793c6628fb1e5cd70
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build2.diff.gz' libxext_1.3.4-1build2.diff.gz 12720 SHA512:6ec71960a93504538ef944620b0af7bb2ffdf21270ddaf1715dec4faf79d0d1ec1372a148e9acb64a014b2a761eadf01f0b83955dda7ff2fdf942b5998bd1b34
```

### `dpkg` source package: `libxml2=2.9.14+dfsg-1.3ubuntu3.6`

Binary Packages:

- `libxml2:amd64=2.9.14+dfsg-1.3ubuntu3.6`
- `libxml2-dev:amd64=2.9.14+dfsg-1.3ubuntu3.6`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.14+dfsg-1.3ubuntu3.6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.6.dsc' libxml2_2.9.14+dfsg-1.3ubuntu3.6.dsc 3038 SHA512:7335b471c95fe73974736ded5dbd85cb1fcf24e0168ab939e7ff9df9735b02f5c550a1d96021023e14db18bf6defa2c72888a35641136cca75f23a45863f03bc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg.orig.tar.xz' libxml2_2.9.14+dfsg.orig.tar.xz 2351200 SHA512:1eacc9ac2cd8d38b8466659b3b9d84b94eb765c8f869d6cca0da131060bbc35c2b31c6148d59690547871a20cea339eac8fbe953b4fe37cf0900862f3fd9621b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.6.debian.tar.xz' libxml2_2.9.14+dfsg-1.3ubuntu3.6.debian.tar.xz 48472 SHA512:8e9d2a8032b59da05cbe5be6850867e5b3ca18c4c4d8679b4a80afd36306ac4099abddecc208f90cc9067b746d9c8eb9dc7f732d8cea4187423803f7f43f34d0
```

### `dpkg` source package: `libxrender=1:0.9.10-1.1build1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.10-1.1build1`
- `libxrender1:amd64=1:0.9.10-1.1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1build1.dsc' libxrender_0.9.10-1.1build1.dsc 2204 SHA512:ac21ce52dc62e66c8e0e6c94c727a978b8b285755dd7c3de9b8bd34057bdef1ee23acdfbdd3efb2052734b763904c02e98cd71b4b0bb28a1673a6da3eb7cb8f6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA512:7768e62b500f468460f88f27bc1130170b204b478573d9e4406867e557b5638b7c1e21d88d51f9e774ce2344780a384e3c3be51421275d2ee880f9a978a3a232
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1build1.diff.gz' libxrender_0.9.10-1.1build1.diff.gz 15274 SHA512:dca2b6bf90a6ce1ec30376a001f6f24f2d95e917c3a4890242022bf5eefa20c9c1e775c66c229cbb7ee47482650b9a0a750e7bf1890aec89d3bec6b692f4174a
```

### `dpkg` source package: `libxslt=1.1.39-0exp1ubuntu0.24.04.2`

Binary Packages:

- `libxslt1-dev:amd64=1.1.39-0exp1ubuntu0.24.04.2`
- `libxslt1.1:amd64=1.1.39-0exp1ubuntu0.24.04.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.39-0exp1ubuntu0.24.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.2.dsc' libxslt_1.1.39-0exp1ubuntu0.24.04.2.dsc 2307 SHA512:bf099df8a7c64ea8b60c0d09342aba717b68167fab27327b4b2cac15d16fc8cefca8920d96825e38b5391f8ee65c40f0230049ef58adceb17683275eff51b3c1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39.orig.tar.xz' libxslt_1.1.39.orig.tar.xz 1578216 SHA512:c0c99dc63f8b2acb6cc3ad7ad684ffa2a427ee8d1740495cbf8a7c9b9c8679f96351b4b676c73ccc191014db4cb4ab42b9a0070f6295565f39dbc665c5c16f89
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.2.debian.tar.xz' libxslt_1.1.39-0exp1ubuntu0.24.04.2.debian.tar.xz 23028 SHA512:7aeb7c8ff58ce30c820e378aa677ea2fe92c5b235e75b420c3b96615115102760ea0c37676f629d39b64bd79367c5749505c1b661260ed1a7ff4be04a11ce8d5
```

### `dpkg` source package: `libxt=1:1.2.1-1.2build1`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.2build1`
- `libxt6t64:amd64=1:1.2.1-1.2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.2build1.dsc' libxt_1.2.1-1.2build1.dsc 2488 SHA512:ebe5d28a22400920f1ce994c3977affdb7da2033a8a6fe0d8b460b90d9eb37de4053843c9e6cc0addd0e712928870eae79d7bdbed0690577701f6d1bca400265
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA512:73c2fd8a6590ab5ee93cf646e4f41fb71d424961ecbf9bc13c68abdf539c63ab0c59a4d3b22195ba21859523f4cf0e937648424532794a1350a5891061096503
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA512:135e01b8a79beac9530087dee1a5458c359b4f1ae8346e2502f72f4fc24be400477fda90944315c585e3416e80cb74d1a140d5dfec81e854a4996199a8b221dc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.2build1.diff.gz' libxt_1.2.1-1.2build1.diff.gz 45676 SHA512:e16fcaaba4f0574d31b7418b2a364a09eb9cee3008c4022a09ebd606ee2eecdcbb49c8e1562f1479b1eda5bdea977b3777c384848c21c437793a6a76cc007467
```

### `dpkg` source package: `libyaml=0.2.5-1build1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-1build1`
- `libyaml-dev:amd64=0.2.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-1build1.dsc' libyaml_0.2.5-1build1.dsc 2203 SHA512:872e28e7564a127ef6da7a47c401d2cd7a339d789b2e8fa6c514baad5fa986e96698661649e77fbfcdc31e38c1bea058fb1e004d7b2340854802bc90bfcae3f6
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA512:a0f01e3fc616b65b18a4aa17692ee8ea1a84dc6387d1cf02ac7ef7ab7f46b9744c2aac0a047ff69d6c2da1d2a2d7b355c877da0db57e34d95cd4f37213ab6e7e
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-1build1.debian.tar.xz' libyaml_0.2.5-1build1.debian.tar.xz 5496 SHA512:d1b42bf0a1076d970298ca762a51f57c1ed76a2eac44d5385928709ce5876617f2629dab7841f8e1b6837264098cfc4c9c2aa214466f781b66077fa1979c809a
```

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

### `dpkg` source package: `linux=6.8.0-87.88`

Binary Packages:

- `linux-libc-dev:amd64=6.8.0-87.88`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lto-disabled-list=47`

Binary Packages:

- `lto-disabled-list=47`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lto-disabled-list=47
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_47.dsc' lto-disabled-list_47.dsc 1435 SHA512:fb23ada0a2c9e1d707f93c8563a653ee4dec5abecca81a71ba2913732b8d5c8af7d533b543b89e2f8dbc059103bb87dab2f2af633c36c985d545f907374bec3e
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_47.tar.xz' lto-disabled-list_47.tar.xz 13464 SHA512:8365c7c06c3b69705d6370bc67a7d71423912cbaaefae1eff8cb6aa78ff76abbf8a15306c3c11f7b7c8e8168f3fc67513e60a6536e7a17eb1bcb1e66aa37a0d5
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

### `dpkg` source package: `lzo2=2.10-2build4`

Binary Packages:

- `liblzo2-2:amd64=2.10-2build4`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lzo2=2.10-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-2build4.dsc' lzo2_2.10-2build4.dsc 2058 SHA512:0f8b41c3996156109afc6ff36d35347191f57231fceebc16753f842937242748bded54442b2bb20df75263115f7158367e7ecf30848414b1ffdba7b541e9fc38
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10.orig.tar.gz' lzo2_2.10.orig.tar.gz 600622 SHA512:a3dae5e4a6b93b1f5bf7435e8ab114a9be57252e9efc5dd444947d7a2d031b0819f34bcaeb35f60b5629a01b1238d738735a64db8f672be9690d3c80094511a4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-2build4.debian.tar.xz' lzo2_2.10-2build4.debian.tar.xz 7120 SHA512:f8705ebdca5a759ca415e6234c31b9eec3a1fd28ef992f7db1e126efd65039858188bc32a989ca4a194b94f27edf8ae96887a1f20ebc7e2f1428169f2887c479
```

### `dpkg` source package: `m4=1.4.19-4build1`

Binary Packages:

- `m4=1.4.19-4build1`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.19-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-4build1.dsc' m4_1.4.19-4build1.dsc 2114 SHA512:af4b77797c56d650ba50831f6730de1b45c9ee9a22e6875db30145b46c972b94507fc075b1ecfeee75c47616b3aaba5a9247d4c4989e1fe33ad33641613ad87d
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz' m4_1.4.19.orig.tar.xz 1654908 SHA512:47f595845c89709727bda0b3fc78e3188ef78ec818965b395532e7041cabe9e49677ee4aca3d042930095a7f8df81de3da1026b23b6897be471f6cf13ddd512b
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz.asc' m4_1.4.19.orig.tar.xz.asc 488 SHA512:d6ac9c6a54c57e9b53fb3e34a60d49df2f46a6e494da0a0c9ae8246b984e68a853b5d8c42677c1a0485c3f36b0bce10a481d3775c0edc1dbdfb27b43545bc31e
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-4build1.debian.tar.xz' m4_1.4.19-4build1.debian.tar.xz 17460 SHA512:cd8501c3323749074e702ced7c648506034f69e25442b648876aa46a186b9ff613e969a737437757ad8595b660aa298e677c8ebfd4dc8797a36510acc3d359f9
```

### `dpkg` source package: `make-dfsg=4.3-4.1build2`

Binary Packages:

- `make=4.3-4.1build2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.3-4.1build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3-4.1build2.dsc' make-dfsg_4.3-4.1build2.dsc 2151 SHA512:78402aabf7f2d9cf40f9bc2ecb5d0063e005ce8ecd131145863dd4c57c2f78ecdc0d98f8c78861903472b211f37975c6004a05fc88c9bce1c6f405569aca89cb
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3.orig.tar.gz' make-dfsg_4.3.orig.tar.gz 1845906 SHA512:bdc150f9d256145923380d6e7058ab9b2b4e43fcb1d75ab2984fa8f859eab6852a68e4ea5f626633e0bec76fbebf1477378e268e8ffdb5cb2a53b29cbc439bc1
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3-4.1build2.diff.gz' make-dfsg_4.3-4.1build2.diff.gz 50933 SHA512:84074f8c50818009fc0beeb1a61bb74d9fba8b277f2911cfb20ba1f5807e72f18d83b69a318b0799bd3568d0756e790c8a27d09d382b8379d79a22ad58db5f9e
```

### `dpkg` source package: `mako=1.3.2-1`

Binary Packages:

- `python3-mako=1.3.2-1`

Licenses: (parsed from: `/usr/share/doc/python3-mako/copyright`)

- `BSD-3-clause`
- `Expat`
- `WTFPL`

Source:

```console
$ apt-get source -qq --print-uris mako=1.3.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mako/mako_1.3.2-1.dsc' mako_1.3.2-1.dsc 2399 SHA512:73a981c8fa5a2e2e06a2e60af1df8a043d8552fe96615e152a1a5a9f4e4f5df5ba219c52ad0bb08a3c8224b71c413ea5b2780d317b82f10ed8cbbd836fe09e47
'http://archive.ubuntu.com/ubuntu/pool/main/m/mako/mako_1.3.2.orig.tar.gz' mako_1.3.2.orig.tar.gz 197955 SHA512:1e394faeaf576c79bde85f2546f5b91bf4b5b7a595c852b3f0e843a9735f5858fb336c83ee91eb1e51f29655490b6051194b0cbe705611443e918eeba0958cac
'http://archive.ubuntu.com/ubuntu/pool/main/m/mako/mako_1.3.2-1.debian.tar.xz' mako_1.3.2-1.debian.tar.xz 13244 SHA512:09f021cdd5560a22ddfc17ff16fe61df65c17170b48ad4c9e0feb18596bb0a8acf3c841bd3d8dea05a936dd3a3b997234e11faee1bf7db1e9ab4c3d393d4ac87
```

### `dpkg` source package: `markupsafe=2.1.5-1build2`

Binary Packages:

- `python3-markupsafe=2.1.5-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris markupsafe=2.1.5-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/markupsafe/markupsafe_2.1.5-1build2.dsc' markupsafe_2.1.5-1build2.dsc 2193 SHA512:65313010aa8b4df3ce9a0fcb4666a4d54b557ce9a3ce570a5ba146546c27ba15578ec47c3e85f3997f61d61549e17fdaea7ced377bd487b4802f11220485b23b
'http://archive.ubuntu.com/ubuntu/pool/main/m/markupsafe/markupsafe_2.1.5.orig.tar.gz' markupsafe_2.1.5.orig.tar.gz 19384 SHA512:3ba5af43d23c266377f5d32b11e1faa7955ea8c67eb1c32886c308527f93e75e387294d0eec7794c0c20aad0c705b27f3d1f86b04202f3b63068d12d4053cc71
'http://archive.ubuntu.com/ubuntu/pool/main/m/markupsafe/markupsafe_2.1.5-1build2.debian.tar.xz' markupsafe_2.1.5-1build2.debian.tar.xz 3812 SHA512:c4997a14ea90fc1eb0c2e56b4d7b9c3f7e61f63d5803cfcbced0d39967d69bc1b80e61730a130b909dab95d1f83bfb164416f3cdec7c22ace066f8ce93ba8f0d
```

### `dpkg` source package: `mawk=1.3.4.20240123-1build1`

Binary Packages:

- `mawk=1.3.4.20240123-1build1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240123-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123-1build1.dsc' mawk_1.3.4.20240123-1build1.dsc 2312 SHA512:ce2caf84e1323bee8329421cbda06d3cc6748c3e026a885996ca9cc1dad7b553f865f837821982e048c6456c09b6750d88da0412571011920f7f8a7239a45688
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz' mawk_1.3.4.20240123.orig.tar.gz 413943 SHA512:f6d5da44280afeac4a9bb6d3788ed71ee816daaa5816f49b9d40add5292f3ae06e5af007a6c993d14405238cbb70ba4997fdd2fcd5901c9a1a4b61357045c4a6
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz.asc' mawk_1.3.4.20240123.orig.tar.gz.asc 729 SHA512:3b4b8b8b7b74aff7061158a7c284d1949c09d52d78003b678c9dcc1da036a4d84b873103d76362866daf914d5a7d717c71baf13d30d7e882b03c5f87c8e4c452
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123-1build1.debian.tar.xz' mawk_1.3.4.20240123-1build1.debian.tar.xz 15704 SHA512:53a4367656e29f5897ba29cf38b30e2b3a2758d990bbd3a90bdbceb5d3c467615496407af8bd437b4df2e9518096865b7ec6739b0465e8bba20d87ed71782268
```

### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=10.1.0
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_10.1.0.dsc' media-types_10.1.0.dsc 1624 SHA512:78ee4c91efa0eea0314213b1df7cc659f3b47556a648e07c4044f1ae7ae08ccd6c4d479e6425297ac79c38a2a607a157ed781c66751235cecee1eb1ed8edf6b5
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_10.1.0.tar.xz' media-types_10.1.0.tar.xz 59052 SHA512:db92986166c6eedd44d839617c75a1f60704af6d87f92a5c9bb5f207a8e4e27f67b86e340745f6f41e793908d48eb609575678495194a21d368db2fc102b35c9
```

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

### `dpkg` source package: `mysql-8.0=8.0.43-0ubuntu0.24.04.2`

Binary Packages:

- `libmysqlclient-dev=8.0.43-0ubuntu0.24.04.2`
- `libmysqlclient21:amd64=8.0.43-0ubuntu0.24.04.2`

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

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.1.0build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.0build1.dsc' mysql-defaults_1.1.0build1.dsc 2411 SHA512:cb22278ef04b2f9de5f799994531f0302811b903eba79f2ea7c8d70f36cf42e23550db252c1d1a93da53c9e2cbd6e46d40c6b109690f4baca77d7d7529bcc6b7
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.0build1.tar.xz' mysql-defaults_1.1.0build1.tar.xz 7524 SHA512:19dc3288a7f9200ba3b62b097f259ecfcbcec998cd846371b35901530da2f59510ad17bdb24185ce4ba5fff88cfd1b106880e0bdabb816a7d65ecf1ddb8ad75e
```

### `dpkg` source package: `ncurses=6.4+20240113-1ubuntu2`

Binary Packages:

- `libncurses-dev:amd64=6.4+20240113-1ubuntu2`
- `libncurses6:amd64=6.4+20240113-1ubuntu2`
- `libncursesw6:amd64=6.4+20240113-1ubuntu2`
- `libtinfo6:amd64=6.4+20240113-1ubuntu2`
- `ncurses-base=6.4+20240113-1ubuntu2`
- `ncurses-bin=6.4+20240113-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.4+20240113-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113-1ubuntu2.dsc' ncurses_6.4+20240113-1ubuntu2.dsc 3963 SHA512:6a7865bb7f27ba20f443c43c00825aa8b4be3fd0dbd8da10571186c0a3ca074d82e30a08f854b6ec324a3663dae09d4d57c4e77617b08715a18b182a164a3c26
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113.orig.tar.gz' ncurses_6.4+20240113.orig.tar.gz 3688489 SHA512:45a4fbfa7d6fa51f7226b35698f2ca9b9f5bbbf3243cfee28886751244d238f698d5eaae1498ae9f7965b2d618a669ff827cfbba830e3a52a26bef825dec8ed9
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113.orig.tar.gz.asc' ncurses_6.4+20240113.orig.tar.gz.asc 729 SHA512:df94456e47857abfbb47f3a5a69f03b3d418a44542e1fa699c4b13eba812e5a85173cd651d77d07973f8f8d96bc301d7e413ad379f9ba1e9feb434c4da019f13
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113-1ubuntu2.debian.tar.xz' ncurses_6.4+20240113-1ubuntu2.debian.tar.xz 49372 SHA512:02fdd8f135b415d72ef4051b1002d0721a240f80b164d437592d5d6dfe44c4d3a0cd92baf5071047d826ca3b2039190ed19f3a092169d2a7af501c09e7ec45d0
```

### `dpkg` source package: `netbase=6.4`

Binary Packages:

- `netbase=6.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.4
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.4.dsc' netbase_6.4.dsc 898 SHA512:243ea79c8566581ff6137d0525195c0c9ceea2234cf74eb28aef5f6791ba35003e91bc063ce508c7be3038c05cf081db1d8f717d193f78554b7aa4a215d7c9ef
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.4.tar.xz' netbase_6.4.tar.xz 32712 SHA512:cbc588e5fbef5e3e2c8a2dc49214237e8340bf3fae66973237d1714f67c039d4b8d6886581d92b45a004fa23ff016ad8c82cb15b6f752d1ffa23e3284fe0b80a
```

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

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-3.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3.1build1.dsc' npth_1.6-3.1build1.dsc 2107 SHA512:83fc5c562da895742de6b46585a0707052e053804e3187525d290e0cc05938feb7681bb9a7dd053ed930a3774c7abc95a4d1a9e437930ca72c438e29cb7183d8
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA512:2ed1012e14a9d10665420b9a23628be7e206fd9348111ec751349b93557ee69f1176bcf7e6b195b35b1c44a5e0e81ee33b713f03d79a33d1ecd9037035afeda2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3.1build1.debian.tar.xz' npth_1.6-3.1build1.debian.tar.xz 11036 SHA512:caf36d8727c335bbcf996421e65cf044d6468d95d70e9b671b57196341e49e67f687d6c80cab78d6c0388a90f795e4ed0ff28aaa0d4e7dd6f4701abdfc77a09a
```

### `dpkg` source package: `openexr=3.1.5-5.1build3`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.5-5.1build3`
- `libopenexr-dev=3.1.5-5.1build3`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.5-5.1build3
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1build3.dsc' openexr_3.1.5-5.1build3.dsc 2629 SHA512:6754aafb095ee18dbd5f3df736e9e619af5189e3fb6d61245d64d18aaec9874e23b75daa51b8e55b61c93732163575f85496e1e61baf97de1470939dfe8eae8e
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz' openexr_3.1.5.orig.tar.gz 20327926 SHA512:01ef16eacd2dde83c67b81522bae87f47ba272a41ce7d4e35d865dbdcaa03093e7ac504b95d2c1b3a19535f2364a4f937b0e0570c74243bb1c6e021fce7b620c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz.asc' openexr_3.1.5.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1build3.debian.tar.xz' openexr_3.1.5-5.1build3.debian.tar.xz 18952 SHA512:717a1362e1150abf4d555725539bd4b873591646f1c48859c200cb9a7b46946e00824d58ce68cb5dbee4ab3231e77f01cb75624a3eca99f633a4a99ba72e4e09
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

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.52.1+ds-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.52.1%2bds-1build1.dsc' pango1.0_1.52.1+ds-1build1.dsc 3654 SHA512:1e3fc5e9547deb7955af472ce03dbd554f91fbe4c42abf2ab4ff38fa787580540fe74417f0d3cc4641ceb8942a72672f500e0a08e171d33a50a1cbb29c930005
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.52.1%2bds.orig.tar.xz' pango1.0_1.52.1+ds.orig.tar.xz 1738052 SHA512:4aa6e423f2fdb72d564f13251d263e74831113f8b8e515b8473f7d030ac62c29c7665d92ed89ce5d5a3750d56e19f7105b138b1c734a88f7e0882be53c27c8fa
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.52.1%2bds-1build1.debian.tar.xz' pango1.0_1.52.1+ds-1build1.debian.tar.xz 41748 SHA512:086e4e6b5e311fc84896292ed6f99f1cfdb9107adad199b1c192827f1101225ef5acbffaeb3522b2d006a74479132e96065b4c5114dfe1f650bbeb00435fa08e
```

### `dpkg` source package: `patch=2.7.6-7build3`

Binary Packages:

- `patch=2.7.6-7build3`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7build3
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build3.dsc' patch_2.7.6-7build3.dsc 1838 SHA512:205ad1e6f47a5c039c878387f95ee3a91e2115ccd740f6d2e6ce0b7d9996bad38332739418e3cb70d215f93a083c3fc5174269893f5d3e200caf18ef0d8e1f05
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA512:fcca87bdb67a88685a8a25597f9e015f5e60197b9a269fa350ae35a7991ed8da553939b4bbc7f7d3cfd863c67142af403b04165633acbce4339056a905e87fbd
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build3.debian.tar.xz' patch_2.7.6-7build3.debian.tar.xz 15324 SHA512:46d2d3d5da88ddf723891df3288165405794cf414c6fdad65723a0f7333e918676a04eaa254d2dbc7b682e4e214d6089af461b490c51a5c8e7e02d4743b4249f
```

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

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.2.1-3ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu5.dsc' pinentry_1.2.1-3ubuntu5.dsc 3322 SHA512:86814cb072f65755573416f567476616d001aefa000362e84b751c85ed42b02297391fc67d7dfabcfd70d7e953e0b9d95b63d98222f8ea79aec527da37fc0c15
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2' pinentry_1.2.1.orig.tar.bz2 547698 SHA512:a665315628f4dcf07e16a22db3f3be15d7e7e93b3deec0546c7275b71b0e3bd65535a08af5e12d6339fd6595132df86529401d9d12bd17c428a3466e8dfafab6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2.asc' pinentry_1.2.1.orig.tar.bz2.asc 390 SHA512:60b63b7fe2d6793840be55635f9a704cd42eda69ccaea2453d47b5f7a5198d313b8f23555972584f7f087fd5d0fc2a379bfc5f7512f325b018cc5c3e2e54a47e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu5.debian.tar.xz' pinentry_1.2.1-3ubuntu5.debian.tar.xz 19244 SHA512:7d4a8fe8920f1d6ef656ab485e2625bc646c5726ba18f91eedb3f4c95241680f2169b80791355e34a707bbebdb0de9986e264f2d8f36848e48a8300fc8497481
```

### `dpkg` source package: `pixman=0.42.2-1build1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1build1`
- `libpixman-1-dev:amd64=0.42.2-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.42.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2-1build1.dsc' pixman_0.42.2-1build1.dsc 2153 SHA512:433d3a48159ab6d981bc4a6c40abfb7cef8aa6ca7c893420042d071e1c236ad78471df956ac83d2e88df25e107b36b3ce808fa97bc701178804d452523ba0826
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2.orig.tar.gz' pixman_0.42.2.orig.tar.gz 959669 SHA512:0a4e327aef89c25f8cb474fbd01de834fd2a1b13fdf7db11ab72072082e45881cd16060673b59d02054b1711ae69c6e2395f6ae9214225ee7153939efcd2fa5d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2-1build1.diff.gz' pixman_0.42.2-1build1.diff.gz 327276 SHA512:a07846ba47b3f3407e43aefee37efe6265445a8c1e81589a715f175e426ed2a75822cce7545ac94bb368c3eecaaa2ccd7b0c7944aba9b51f0e939403b2f57d1e
```

### `dpkg` source package: `pkgconf=1.8.1-2build1`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-2build1`
- `pkgconf:amd64=1.8.1-2build1`
- `pkgconf-bin=1.8.1-2build1`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-2build1.dsc' pkgconf_1.8.1-2build1.dsc 2262 SHA512:2f42caf03cbabdd31c642775890e4914d00cb2572d0ec8a6b76d670b680870913572c0d14c0e074a6ab134a4b7d6929c88e3e0e049e982c7eca31a2762e5840b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA512:7a7d5204c1c9bfb6578bda56f299d1fa0300e69a133a65730b10ad77aefbf26fceb74ae77cecda326b3ed5db5736f27fcce94764b3a56d40f4bb99fecdc80bba
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-2build1.debian.tar.xz' pkgconf_1.8.1-2build1.debian.tar.xz 15672 SHA512:737cdc1f7867ee564085b78256acd259d62721f0f385f8b551ff8eafa9ccaffd7d4f2d3765b058f89c918c0c0192761fd72c19c8714fb98c5f4ebd7e55a604f7
```

### `dpkg` source package: `postgresql-16=16.10-0ubuntu0.24.04.1`

Binary Packages:

- `libpq-dev=16.10-0ubuntu0.24.04.1`
- `libpq5:amd64=16.10-0ubuntu0.24.04.1`

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
$ apt-get source -qq --print-uris postgresql-16=16.10-0ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.10-0ubuntu0.24.04.1.dsc' postgresql-16_16.10-0ubuntu0.24.04.1.dsc 4336 SHA512:f4c504910339d48ef7122dd9167bf0e6fd72f627a1251fb324f230346ab072718c2bb416755517723de45c29ee79ce0d9f3798526c7bc096bfacdc9f0af9ffa0
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.10.orig.tar.gz' postgresql-16_16.10.orig.tar.gz 32861700 SHA512:6ed4c77fea346536dbad5eaa427d97dc6f68b70951a2d4e658087351f68b99ba4873192d3266fa84fdc9e09f7ee97eb6f2e3ede4a09994db6d56da391cafe765
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.10-0ubuntu0.24.04.1.debian.tar.xz' postgresql-16_16.10-0ubuntu0.24.04.1.debian.tar.xz 36932 SHA512:3e77f09daf886b687eafecba2d4cfff978c477271d5008c10423bc7c2356b93bd5e811ea973a0ee6e40002d5a1740bb07ec42bb537660fb47ffe06b04ba92338
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

### `dpkg` source package: `python-markdown=3.5.2-1`

Binary Packages:

- `python3-markdown=3.5.2-1`

Licenses: (parsed from: `/usr/share/doc/python3-markdown/copyright`)

- `BSD-3-clause`
- `etree13`

Source:

```console
$ apt-get source -qq --print-uris python-markdown=3.5.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-markdown/python-markdown_3.5.2-1.dsc' python-markdown_3.5.2-1.dsc 2610 SHA512:8a400cae0b3b147b15bb36a748c91317e8c8c1ea796de678af3587ce9323ac6f069a24a2a3460caf9c844b54a5a794f5a610760b2e752310527e30101fca2086
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-markdown/python-markdown_3.5.2.orig.tar.gz' python-markdown_3.5.2.orig.tar.gz 349398 SHA512:a112620162cb0764848dbe766bd23df6b7220ec3db6eb60d5663757092300c5c6abb9af6a412280fc3f59e617263c3abf0ed4a969eebacd3e964228525165f24
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-markdown/python-markdown_3.5.2-1.debian.tar.xz' python-markdown_3.5.2-1.debian.tar.xz 12324 SHA512:454bd51f85060d924a3fc92b9e586b2618f3d2fed27b02fd0ae18a6ed8e73cb616d95b49845c1299fbe172243345cde5b89f9f76e22cdf5174b581323f7f5829
```

### `dpkg` source package: `python-packaging=24.0-1`

Binary Packages:

- `python3-packaging=24.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=24.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.0-1.dsc' python-packaging_24.0-1.dsc 1932 SHA512:c302a450bebacef271040baa539e790e68b5a58f55316820a60f7fecfb3e9c1de0ebdb9e784a21eb1bcede5df7f6036cfe170fe367bea52f84d3d2bf9ae8499e
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.0.orig.tar.gz' python-packaging_24.0.orig.tar.gz 147882 SHA512:b6af704f93bcb7611a06eb2bfa94d8dc4bb1e5e9898af7c0eb85e67cf1ebdb858e272ca18019be4daaa43ac3f73b1cb2e690d8b50a4252380a2dc9f2d0e03a58
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.0-1.debian.tar.xz' python-packaging_24.0-1.debian.tar.xz 2928 SHA512:019649bd458d772025f1465e3df7daee7b206652c0f247a9596202975913cdcf2b75827ffec1583fd62d08d8d8f22573d2a2440cc7f3a0002471c36a07aad170
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
- `python3.12=3.12.3-1ubuntu0.8`
- `python3.12-minimal=3.12.3-1ubuntu0.8`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

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


### `dpkg` source package: `readline=8.2-4build1`

Binary Packages:

- `libreadline-dev:amd64=8.2-4build1`
- `libreadline8t64:amd64=8.2-4build1`
- `readline-common=8.2-4build1`

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
$ apt-get source -qq --print-uris readline=8.2-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-4build1.dsc' readline_8.2-4build1.dsc 2926 SHA512:8ad7e70792466e093ff1202b123e24c6fa1a9850e57ca0b775b06bfe4e502ef8ffc876eda32fb164565cda1e4e048f3f80e6ff69ae9c56f87841f15c759a7658
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-4build1.debian.tar.xz' readline_8.2-4build1.debian.tar.xz 33816 SHA512:b8c92282e25f3d28acd02c1431088f5f29aa1398ce919c312de50813e8a0df07d973ffd49fccde51505538ed7e29f666d812931961746b12ebde219d16be914f
```

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

Source:

```console
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.2-0ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu7.dsc' rpcsvc-proto_1.4.2-0ubuntu7.dsc 2113 SHA512:898f925a91776d16b8f6934b502f0a05983079af42a633245d2f5e25975daf3eece0be7a999dc640739b0c29315a657d33c1d5e5ed03e74ab5b911638571a96c
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2.orig.tar.xz' rpcsvc-proto_1.4.2.orig.tar.xz 171620 SHA512:631fbfc00af94c5d7def0759f27e97dc14d400b4468c906719ae18ecef74815730798c882d1aaa4f90359224e7b829019b786baddc3097905b54f940ca85a714
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu7.debian.tar.xz' rpcsvc-proto_1.4.2-0ubuntu7.debian.tar.xz 4336 SHA512:faf9f6eb4e7da5e4fed0e358e836cc4137f783079127cbabe3bed82f8ad2d08250d827d62f0f49df23604d685b7c55d6c30b8ec69dff0f14e3267ae180cb9f96
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.dsc 2439 SHA512:5e2fb3986c0f0e2150c6054e0428adbf1719bb0c33f92ae4acb74a11e625d731ede0262f0d8887c769a95a61f3cd4d23d44bf2f375f0153eba6c0f25b68719c5
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.debian.tar.xz 8464 SHA512:812edf4f933ad0f723404192bfbfceca86e58303169a30e3b1f47781b709b91a259621293533d31d7abd16bc522824e2db325426a4ce9a6b428b88d492ae4c6c
```

### `dpkg` source package: `rust-sequoia-sq=0.33.0-3`

Binary Packages:

- `sq=0.33.0-3`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=0.33.0-3
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.33.0-3.dsc' rust-sequoia-sq_0.33.0-3.dsc 3613 SHA512:393234c00940c618d43e109ddf12169566fb82076e703b04adb1bf2579c80887563b833d059c64595dc222cc096810a8025d70b890f15316a1568423b8bda5ad
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.33.0.orig.tar.gz' rust-sequoia-sq_0.33.0.orig.tar.gz 388309 SHA512:c366c7c2f2fcc398194f20922fed72bf18ede12164f8d0438bac0ca08f0900004f3c1039f8cd3ee480ded3e42104cf6ac4365020b9f258dc115594112ec3b101
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.33.0-3.debian.tar.xz' rust-sequoia-sq_0.33.0-3.debian.tar.xz 5524 SHA512:81d510431bc0116e4aa79f005e28bc054b1712b28c76206e4d663111598ec257170d91a865c013ba5c957f1979d4570873393fa2119f24b09ada10151c56a38d
```

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

Source:

```console
$ apt-get source -qq --print-uris sed=4.9-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.dsc' sed_4.9-2build1.dsc 1992 SHA512:c1fb23ca19645e3c77d7d466818b0ff15ec2fefa423d03c60746d3c441a767af9a551c0af022a5c17e69e58589b8004bc6e127dbb63d806c6269ba0ee2c1e8fd
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.debian.tar.xz' sed_4.9-2build1.debian.tar.xz 62896 SHA512:e9e57380873aa800f7892d99dbebb362a2ba9f27cc984180753d306592d6ca572d0baa3c4faf4b10dbc2aa33985e759f668f1efb4e0b09e4ae2ae689e32969ad
```

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

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.22
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.22.dsc' sensible-utils_0.0.22.dsc 1737 SHA512:be6eb8a63de0912e56d7039e616fa1ef362f1081e2edb893f3cfa8ccc3c5d2ed65ad2f477d6013b6a5ecf0f4b98a39de45ee073cdeeb3802f3eb51c754fda40d
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.22.tar.xz' sensible-utils_0.0.22.tar.xz 74412 SHA512:c35ac6f9a27bf21bd496acb5ada2fd2e5eb101d661fe49a505a80dc507eea314b8b29388ae4852c14aff547fef8938f48a14898c49cf951d7ab13ccf48e77ed5
```

### `dpkg` source package: `serf=1.3.10-1ubuntu0.24.04.1`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-1ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.4-4
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-4.dsc' shared-mime-info_2.4-4.dsc 2237 SHA512:c33bb340414ba0813877e431be1c57d674255306e4165b308f1cfc38c390c39584743f592ff4ba96cea6c18890e9910fada839f1f931038e2b725f11ae4cd81f
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4.orig.tar.bz2' shared-mime-info_2.4.orig.tar.bz2 7096347 SHA512:712f414e80919bf2a0f5083ced44c54a350948a526850466a6e9f35365dcfd97fad8bcdbb29945de2715a8f9b70a108e931c8500209a4d6e3dddf97af02771cb
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-4.debian.tar.xz' shared-mime-info_2.4-4.debian.tar.xz 10688 SHA512:579ea2e748879023c746b18cc019ef2a0192de0baaaf804d19a74760af3a02b7cb042cbc787b5ebbece862f10164057a5cff9265d6a7a638f43c390b1a8b59bf
```

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

Source:

```console
$ apt-get source -qq --print-uris subversion=1.14.3-1build4
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3-1build4.dsc' subversion_1.14.3-1build4.dsc 3873 SHA512:568ed9b4135d16062f6d1423f3412bbdfcae4e28a7e43d37fcb7a1a4f4b2a734e6596cce946f396ed4ab0b2eb506f64deb22cfce61ef999bae38893c9c51d26b
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3.orig.tar.gz' subversion_1.14.3.orig.tar.gz 11621442 SHA512:12188a1c07b8b72594d27b1058c13b2ab81d0306d6da2853400be5a73f12ac5d5ff5ae80b6bfd0320e58d8d797b813d71d6c688ba230d3a010ebaf8bdd910c13
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3.orig.tar.gz.asc' subversion_1.14.3.orig.tar.gz.asc 1724 SHA512:d3922207f672cf17446ce05aa1c7361f4c15279fd1182f7c44cab18be63b086cbac4f22830377f8a4e6ca3cc130dfd5cccaa5536c190b5ac8d786af6ecb7ef30
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3-1build4.debian.tar.xz' subversion_1.14.3-1build4.debian.tar.xz 337036 SHA512:62a40df50e32846f25ffde6e806575427cca51b0f7ff24f184d1dc73b58c120b19739893280371764e23d174bab4b714ae6caf95eaf620fde5bd28cd35b6ace8
```

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

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.08-6ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-6ubuntu3.dsc' sysvinit_3.08-6ubuntu3.dsc 2495 SHA512:8200c0fa7220e8922a8546f4f1a4beb3a7194b23abd8730c82ea0cfa57bc6fba01e0b7883a0a9b5b1f10c7b7be805689db80df2930c6d345754a3b85a4ddac02
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08.orig.tar.gz' sysvinit_3.08.orig.tar.gz 513674 SHA512:63ed7ebd50944adce1a35af7798d0e2d6248f36a606f63bb7a567424555ec33e83c33b897528c801b4b4ac61b24d2a3555c9a690031c50a94e7ead83f37f8e96
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-6ubuntu3.debian.tar.xz' sysvinit_3.08-6ubuntu3.debian.tar.xz 140128 SHA512:fa53bd172bf4ce998743f3011b44ebf188948ed436f202181fc6eb7d4535e4d1426aeeac76cda4a650b040d22f9487b890e9f826cd222ddc5e939901c5f7c67c
```

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

Source:

```console
$ apt-get source -qq --print-uris tar=1.35+dfsg-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3build1.dsc' tar_1.35+dfsg-3build1.dsc 2141 SHA512:bb080610adc480448cf511d591eaaeb301395e5bbe01b16b254ad33edb33233aba18af79a4cf505fec330c83dac9570d84122432ff11b781a12c5dc409a173f6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3build1.debian.tar.xz' tar_1.35+dfsg-3build1.debian.tar.xz 20948 SHA512:82b1a9f70c99c17f5288a4a9fbe8b1bef0adcd9543f97f876ee81afc16e3ac02e46182557406ff434ae90c81950f22346c3229ee3e5f5f9578dcf09a20053e9f
```

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

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2023.11.28.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.dsc' ubuntu-keyring_2023.11.28.1.dsc 1872 SHA512:4d3c094e1e01367eb8303808ea5bfea696ee672d855a64272c9222400bec397ebbaa57783bbc8eb4365f0631c9951edeb1b12f04efb3e34275408ef57620f023
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.tar.xz' ubuntu-keyring_2023.11.28.1.tar.xz 20236 SHA512:b17824a91d6e25c5658eae8d9ae509a4158b406768d5d4a8e117a230226ab7cd4327cf7e5b9bbb7baae7c66f3807d27926de85a1ea5c11a82684a890aeb8fd18
```

### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0043+nmu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043%2bnmu1.dsc' ucf_3.0043+nmu1.dsc 1567 SHA512:608423c255fa2c1072bcaa9c71addd0f393f008ebd321ef4939ed4d714aa43bea4c90979fa5817c19e3d7355415cc70aa8c80ff79760b4286411cfbd58242d77
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043%2bnmu1.tar.xz' ucf_3.0043+nmu1.tar.xz 70916 SHA512:8949f197f6aec35ef7ff8c076ed9f863ef369c65de1a17947445c7182623393633e0094e882d50eadbb0435bf03b9a5cb5d11b6e3bd40e33d5d7b15425583b38
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

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.9.0-1build1
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1build1.dsc' utf8proc_2.9.0-1build1.dsc 2294 SHA512:0a183389b81b1ad614d5a5bf1ace1a2fac8cd91ea7724da25b8443a006c71099cd5ea0d2dc909bfa4a580e816e9e34cc9c4f64a752fef5b0ece510e092690491
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0.orig.tar.gz' utf8proc_2.9.0.orig.tar.gz 193465 SHA512:544ed59812279af4135e5622e2e77b3f067765df819cf8b78e679dfc481e9baa5a357a33c40426c5053c1d5107109e3c4c191ed83f3f7c4a6b1769d04b17715c
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1build1.debian.tar.xz' utf8proc_2.9.0-1build1.debian.tar.xz 5956 SHA512:66f918055be1f55b39929c504521094860b66518c99f644a2d826a52076416a7e79d0ed6ec260617e47202e4907f69d7489549737d38ff920942c173e0867693
```

### `dpkg` source package: `util-linux=2.39.3-9ubuntu6.3`

Binary Packages:

- `bsdutils=1:2.39.3-9ubuntu6.3`
- `libblkid-dev:amd64=2.39.3-9ubuntu6.3`
- `libblkid1:amd64=2.39.3-9ubuntu6.3`
- `libmount-dev:amd64=2.39.3-9ubuntu6.3`
- `libmount1:amd64=2.39.3-9ubuntu6.3`
- `libsmartcols1:amd64=2.39.3-9ubuntu6.3`
- `libuuid1:amd64=2.39.3-9ubuntu6.3`
- `mount=2.39.3-9ubuntu6.3`
- `util-linux=2.39.3-9ubuntu6.3`
- `uuid-dev:amd64=2.39.3-9ubuntu6.3`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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

### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1.1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xorg-sgml-doctools=1:1.11-1.1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.dsc' xorg-sgml-doctools_1.11-1.1.dsc 1987 SHA512:1682e1a4d4be1bfb1242adfa22b2764a9425b035cbfae9fd58925d4904eb301fe48bf92fc5935e973d7653db001ab221a8eac8cc5e2840d5a2e0cb4f1bb4895c
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11.orig.tar.gz' xorg-sgml-doctools_1.11.orig.tar.gz 150367 SHA512:a2386e41a8e2f7deaded61e00eaeab922647c0d0f4e36268c4337dc71d2412b0ec433140d080a0fd118b6112ed0a4f960280f932fe8d4a90ea9dc8bedf1eb75e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.diff.gz' xorg-sgml-doctools_1.11-1.1.diff.gz 3296 SHA512:0ea09f6de75cf649fb82705a0470e5ba04edbe59ccfa26132e60120e04036b86e9ff47785fdcee2499fa005cbbdfc9e04ebdca619d0253ea558e2fe5501b9ec4
```

### `dpkg` source package: `xorg=1:7.7+23ubuntu3`

Binary Packages:

- `x11-common=1:7.7+23ubuntu3`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu3.dsc' xorg_7.7+23ubuntu3.dsc 2095 SHA512:dd0091767574109a7e1308a0222f8e5115529baa9def0d822f9812c1761eb43b03caa440ba80874a9c1470a52911e94e6e03f52dc94cf2339006e6bd9ea372a0
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu3.tar.gz' xorg_7.7+23ubuntu3.tar.gz 301634 SHA512:16e7194bcbbc38f185130de2115817c2a34238a1541bbfff08239b0a84e3a5637d907dc1465556061645c6ff0845c47047231a0b384758162ace93d20db6e4d0
```

### `dpkg` source package: `xorgproto=2023.2-1`

Binary Packages:

- `x11proto-core-dev=2023.2-1`
- `x11proto-dev=2023.2-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-core-dev/copyright`, `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

Source:

```console
$ apt-get source -qq --print-uris xorgproto=2023.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2-1.dsc' xorgproto_2023.2-1.dsc 3336 SHA512:d6459c917da1e6cc44e5661744780998f1cd3663dafb70621d304b6bc5113a6bd1d16f13a2b13739b065ea8fbf535096a3d1f0a5e9d145d823a86610baa247a4
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2.orig.tar.gz' xorgproto_2023.2.orig.tar.gz 1150326 SHA512:9f03dcf7b2e7363523cdae6618f7c7db0041335aad505e0322571c391f2ef294957012a755b70e1dd24c3c0178e0423a36554032f552786d724eb9be31891436
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2.orig.tar.gz.asc' xorgproto_2023.2.orig.tar.gz.asc 195 SHA512:bf84acc1adc37a2fe17193dec431a628980707200d8dd571c85f009bd5218d5470b3ac76d31756d10551dc75dfcfc791ec262c933837d0b8554181c2b99893b5
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2-1.diff.gz' xorgproto_2023.2-1.diff.gz 25092 SHA512:ce40310bb67106bfe53052506d277c94e5a16a0c82a20e43944cdf57de1c724bc88af72aff3cd946f4d1f8527bc898f2d43ed9caa4d02a9dbf0647b6e3f3c798
```

### `dpkg` source package: `xtrans=1.4.0-1`

Binary Packages:

- `xtrans-dev=1.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.4.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.dsc' xtrans_1.4.0-1.dsc 1919 SHA512:ac171ce0f00e1741e97a4ddad630ccff69070c0ef60047071b3f940fad08cb468d5ded7b2d4f0f500aeda73f2b703d55a7a4bbe0d5fff88cc3381486a111f580
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0.orig.tar.gz' xtrans_1.4.0.orig.tar.gz 225941 SHA512:21287ccf18fe2ebd458765496b026d175bf47c6e8e5c21d5b9ea17203967efc0cf6928fa2f3385d289a680c7002c3640e4731937029e99933c2a64bb9fab5326
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.diff.gz' xtrans_1.4.0-1.diff.gz 9522 SHA512:d6deaa9579fb61e6ffd296ffe6b083eb9de572001c0a5bc82229ecc3d50bf2ee2f6504b3daa533bd34f3d647d6bd2235728084ec0b59869f6446652b998797f7
```

### `dpkg` source package: `xxhash=0.8.2-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2build1.dsc' xxhash_0.8.2-2build1.dsc 2076 SHA512:9a1bc162cefe90fd63c2f1225ba28eda45a3972e2bf45fc851bc3c7adcf70e5be65a294aedebc47aedc05516f0c0d9fca065d64196d237497c44840dbf5305e9
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA512:3e3eef21432fe88bc4dd9940ccad0308fdea3537b06fa5ac0e74c1bde53413dff29c8b3fc617a8a42b9ce88fcf213311d338a31b1ce73b3729342c9e68f06c78
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2build1.debian.tar.xz' xxhash_0.8.2-2build1.debian.tar.xz 5048 SHA512:c789fd0a22fd40db8983c0f69054141647ebaab94251598723ce1fdf894d0ed2d48c2d5a7f0df7d61e2d874485286e5742a546748d17cc22d5227ad61f6b4ef2
```

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

### `dpkg` source package: `zlib=1:1.3.dfsg-3.1ubuntu2.1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3.1ubuntu2.1`
- `zlib1g-dev:amd64=1:1.3.dfsg-3.1ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3.1ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.dsc' zlib_1.3.dfsg-3.1ubuntu2.1.dsc 3116 SHA512:5cf00ba3f81611c9e94321e524dfcbbe19b7f7d8570e0bc15da334ecf72d212cc22366659ed5ede3e1716ba1ebd2e05c65663e64f1e283fb1f84a3956fd2f4c3
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA512:be6f020c691c61fe4ddcb27d3f8b2515435f544177e0b97286b5e85afc3862c1de6cd74a14ff6b065d620d046d35bf029fabfd1cf473f43a2cad60bf9ad55afe
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz' zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz 61028 SHA512:18f491ffac55e6f9464befc89bbe3067030dfd30d8093c06cd7aa511e4534123b87cecf8f2dde4c7447c77de7965b488de6f407637b4a1ace2f55afc0adae170
```
