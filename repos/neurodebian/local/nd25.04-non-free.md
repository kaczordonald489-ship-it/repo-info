# `neurodebian:plucky-non-free`

## Docker Metadata

- Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
- Created: `2025-09-23T14:32:09Z`
- Virtual Size: ~ 93.28 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=25.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA512:8376928f8a96880edce6e6f1073623ed03bf3da4489807d531c0ecd4c5ff09d19754007e3533922389134aa55a4b64d6f71caa7186133d5a5f559eecf7e33427
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA512:c2d061dbfd28c00cecbc1ae614d67f3138202bf4d39b383f2df4c6a8b10b830f33acec620fb211f268478737dde4037d338a5823af445253cb088c48a135099b
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA512:a425b385e3ce30e7146cf8b143ca269e3edd78af82a21dea76d10ea68215f9abcfb1ed8be24ce3b6dce24e6640df8d5d5f365a47399e37006a66c6a62a41fe41
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA512:58f4f202baa58a6912f85682b967dca282981c1b8d57ffcda1cd67784b5e3f1865ccd1c452d06a50978649d3cb5198d2d5d23004e103b5bd89352a7c1904444f
```

### `dpkg` source package: `adduser=3.137ubuntu2`

Binary Packages:

- `adduser=3.137ubuntu2`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu2.dsc' adduser_3.137ubuntu2.dsc 1688 SHA512:d0d9ec7cd37888ef35f697feb135951f5d929b889207911bda34519a9484f763324ed9f998ecbd97198b41613a5c7e4735f553ad23007af21aa6cccfd3586f6a
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu2.tar.xz' adduser_3.137ubuntu2.tar.xz 280520 SHA512:56ef280c99f93fffdd0e877a8592e51351f200df4dcafb5c3d81a459682838896563751f825718fb5bdf3b733781b93aee6b7343526d59cc467522f31f2b9859
```

### `dpkg` source package: `apt=3.0.0`

Binary Packages:

- `apt=3.0.0`
- `libapt-pkg7.0:amd64=3.0.0`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris apt=3.0.0
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_3.0.0.dsc' apt_3.0.0.dsc 3158 SHA512:d6c73f3b743b61868fef60a2f09f47ddc34bc68cca3c2010854e7730560e059ff08b62679f30e9086cc7936fb5cffe3467d2609f6a55a062fe145ade0c6fed38
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_3.0.0.tar.xz' apt_3.0.0.tar.xz 2420300 SHA512:08aad4abb878bdc26823db8bf21708f3ab220335299281285490aadb9e9687b29d49922206026b40190a367ee765dfe43c32c9e2cee339b29a481948691d9e39
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3.dsc' attr_2.5.2-3.dsc 2576 SHA512:042c7034d0c3273b4e6a4485b25e6f7591af0382b3aa2f47e37e840ec12ef023d453fe93281bc95279243d8888d5faa37b141db2890df0a7004967776e519374
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3.debian.tar.xz' attr_2.5.2-3.debian.tar.xz 32260 SHA512:9507aab496510a3d13feaa4dc4ae0e7837b9cd8a57d0198db2efd24c5a90ee1af1e9c1bd2e3df232f5e6c0c6be25874517bdcc668b7bc893fca6157a4723c8ef
```

### `dpkg` source package: `audit=1:4.0.2-2ubuntu2`

Binary Packages:

- `libaudit-common=1:4.0.2-2ubuntu2`
- `libaudit1:amd64=1:4.0.2-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.2-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.2-2ubuntu2.dsc' audit_4.0.2-2ubuntu2.dsc 2757 SHA512:168529e7b6d57c1d4b3d4624e5f81e8f31939907715c2f5104be4b78068641210fa5c8909dc9b3d0b5a400b7c354ce4a63facc7ea1d88423a4e65a3221152b50
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.2.orig.tar.gz' audit_4.0.2.orig.tar.gz 1198769 SHA512:13d4d07b316fc1380d75baefbb1345b34286015d52e758c14b2f82781cf4cffc16b6eb29d999563ff40caa6d005630a5dfc44741e49b71291c9beb84ddc452a4
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.2-2ubuntu2.debian.tar.xz' audit_4.0.2-2ubuntu2.debian.tar.xz 19532 SHA512:253bd3e605022824735845f050dce42948bd613751b7b2fc409771122a6ea58f462828c8a83f5a81fe123c4dcc12bf6f469f58915c8fc94e72c3f12a629947e2
```

### `dpkg` source package: `base-files=13.6ubuntu2`

Binary Packages:

- `base-files=13.6ubuntu2`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.6ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13.6ubuntu2.dsc' base-files_13.6ubuntu2.dsc 1373 SHA512:b8d3636c2261d48cb06c161310ef66daa5d9a1783caa209a05b9af2f786291b9569573a23c0ca68d7fa20f45522ed32eae3fb9dff20cf78c18248b32d87e0e89
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13.6ubuntu2.tar.xz' base-files_13.6ubuntu2.tar.xz 96424 SHA512:3b777603ef0c6570f32672df55bcd00132a4708ab3e8ab0b13e8ab58437858607496c7e9c9c49cac7d7518cc5315bb1e9e7a843c1d8f6dc5cb7d937271e13c60
```

### `dpkg` source package: `base-passwd=3.6.6`

Binary Packages:

- `base-passwd=3.6.6`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.6
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.6.dsc' base-passwd_3.6.6.dsc 1844 SHA512:3586766521057e97bbc62c575ab20aa5d0bde909fe8250678b6a92f65ec7c07185c964c999bb60ac290679e028abd9813d816ca32230e34a4b595b2af819827b
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.6.tar.xz' base-passwd_3.6.6.tar.xz 60116 SHA512:78de632029bd350486415ae23f3621009ad1cf3b729dafe17c7c6ae11028bf291ad99d6bb7eff3f054f31318e183243622f215c113106b86e5104cfc09184d58
```

### `dpkg` source package: `bash=5.2.37-1.1ubuntu1`

Binary Packages:

- `bash=5.2.37-1.1ubuntu1`

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
$ apt-get source -qq --print-uris bash=5.2.37-1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-1.1ubuntu1.dsc' bash_5.2.37-1.1ubuntu1.dsc 2408 SHA512:a8819417d76bac9cacd39183fc43890f8bf8595ea90837ca631db0e4d646e91d591f20d563ef94440eb2c2e3481aded570d3eccb8bf73c5e26e204d162aef646
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA512:c5380301114967378ace9ae4c510564cb7a827c221470aa532f2360a35000e7719ae081151f3d2ac86dff1d1465f64e60d9202fa6657d716ed6e449f77552158
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-1.1ubuntu1.debian.tar.xz' bash_5.2.37-1.1ubuntu1.debian.tar.xz 95552 SHA512:6fbceebae4fc1b00d67849546682f2ccf4a31d52d2d25ef89799f27321c73600ee847deb7b7d379b60df699b1d9a6af55b9b6d309ba175895cc272ecaf2eb883
```

### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA512:ff346848f80a2d85266e27db27289e126ed016b0ee65f777594e92be388c9f76010419efcbe93dc1d5dde7fe356ee02e797e3579687252b0ae8f4152a245dcb2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA512:29a0df15aab88f4df3e4b3e13a04a428bae850b251d4b70541896b93fe28bce3397f9a7c5e3b251c81a8abd3e0a7911d31f546c1fe30a28c764ded587462831c
```

### `dpkg` source package: `cdebconf=0.277ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.277ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.277ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.277ubuntu1.dsc' cdebconf_0.277ubuntu1.dsc 2873 SHA512:d02a094ef7249b90586cf2a1de7b512330d9b00569edd84392aed1611a22b9dfea63318378a748e72dc4c021281c355d3f3f2874350e2b5e74701054494059f1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.277ubuntu1.tar.xz' cdebconf_0.277ubuntu1.tar.xz 286968 SHA512:ebb8cee8ee8d84aaab49a03211d9cad56dec362d80e63f7375dad09e06eecb7a44811078327daf73d14f6bb9bbbba13adc1ac9ec03dbda0ea31c79532c5a6f12
```

### `dpkg` source package: `coreutils=9.5-1ubuntu1.25.04.2`

Binary Packages:

- `coreutils=9.5-1ubuntu1.25.04.2`

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
$ apt-get source -qq --print-uris coreutils=9.5-1ubuntu1.25.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.5-1ubuntu1.25.04.2.dsc' coreutils_9.5-1ubuntu1.25.04.2.dsc 2070 SHA512:504c83248e95eee6cdb6ea9de00286e7853b94498f9ef849e4631c15e1df97787db4ef5c5363e38ba357dbd7ac84789093a91e014d44dfd8a7594298786881f4
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.5.orig.tar.xz' coreutils_9.5.orig.tar.xz 6007136 SHA512:2ca0deac4dc10a80fd0c6fd131252e99d457fd03b7bd626a6bc74fe5a0529c0a3d48ce1f5da1d3b3a7a150a1ce44f0fbb6b68a6ac543dfd5baa3e71f5d65401c
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.5-1ubuntu1.25.04.2.debian.tar.xz' coreutils_9.5-1ubuntu1.25.04.2.debian.tar.xz 31736 SHA512:6c290618801df22112a7874ea3a423d55603f97485c1c2571e057415f2a7bcd69f64026f9939345a6133b6657c00419c6a62a912f71ffdfa8e02c635c44f2445
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-9`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-9`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-9`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-9
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.dsc' cyrus-sasl2_2.1.28+dfsg1-9.dsc 3306 SHA512:35f2c9b47fb70e13ccffbc269a183beb95f50eb381f753a700631bf76a345f9316aa1f665395ce450060bb4cc51e60e72cadec2fd3256b68bc7f0f8988bf9a6c
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-9.debian.tar.xz 99180 SHA512:1ff7193c671614f63632df7c5677f9c52e11eb172345068494b7dc739e7ff6f556f341a937239bbd7efab0d7a2fb12bd88d69da8a67e1ce77e27d08d8d99768b
```

### `dpkg` source package: `dash=0.5.12-12ubuntu1`

Binary Packages:

- `dash=0.5.12-12ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu1.dsc' dash_0.5.12-12ubuntu1.dsc 2060 SHA512:540bd534f36366297746f183d3613eb0848f4e18aa50b306d3e7c130cc2e107d6eb5b02bab2952efca336c20fbf8683d4f421e5cf82c81a026a6d385ab0c2f1c
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu1.debian.tar.xz' dash_0.5.12-12ubuntu1.debian.tar.xz 47976 SHA512:5e7603682e51045e053e5d014cc4fe1af15fe2d903ef1fcc1ebbec066d895705639f4a087254c933163cbbd2afd94f061cbda9d6d66b9040a269d45c757f48fd
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-9`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-9`

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-9
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.dsc' db5.3_5.3.28+dfsg2-9.dsc 2373 SHA512:f7b3ee10c42556df8b3fd016d9ebe4efc38d60aba8cbd7120d4573d8242c9260e7507cda3b7a2af3f5501ac3d7b27c5dcaccfc54235eb428f583d4d9adae21f5
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.debian.tar.xz' db5.3_5.3.28+dfsg2-9.debian.tar.xz 36412 SHA512:9ed5d57168a50b8adae1c08cc7d1b307904a06a506d85e2faa2bbb4edfaf614b1ef5c3efe11ad71fc5d0f200459a1628c7d092fe121a53a619943c1424031796
```

### `dpkg` source package: `debconf=1.5.87ubuntu1`

Binary Packages:

- `debconf=1.5.87ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.87ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.87ubuntu1.dsc' debconf_1.5.87ubuntu1.dsc 2060 SHA512:422e0a4d7376387151ab57a90edac973559c84fd493dba73e9dc78928d1dadfbdc916268c5216dc1ecf49fd5894647696b8ed14525222f5618014e396bc219d3
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.87ubuntu1.tar.xz' debconf_1.5.87ubuntu1.tar.xz 574428 SHA512:9e6b021155cd01c48552df9c3e61ee5b4dc7ed2355564819d595995715b1ba51301782b30f9710bb24769492844420973981c1e374841624897c703c642dfac9
```

### `dpkg` source package: `debianutils=5.21`

Binary Packages:

- `debianutils=5.21`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.21
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.21.dsc' debianutils_5.21.dsc 1631 SHA512:14068decc92bb615468ca43d2c24eb0734ee7f45274629f079ffe7cae670a91254654911d58f3e4ce058ff6fbec985cfa8fb65408191ef2fa9bde5e6246ad36c
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.21.tar.xz' debianutils_5.21.tar.xz 81916 SHA512:9d4c7505433e184d1b0467e3b0a0d649a5d20e5c75e70f0d8b0bffcf9694357a86cd36417b1d1b06285c6add4bf5c4361e49cba966c6993fb2dbe7c974366f98
```

### `dpkg` source package: `diffutils=1:3.10-3`

Binary Packages:

- `diffutils=1:3.10-3`

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
$ apt-get source -qq --print-uris diffutils=1:3.10-3
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-3.dsc' diffutils_3.10-3.dsc 1851 SHA512:9bfaf30887b57b90a5b91580aa612f801f41d3c8d3bc97e6e56bb91172ff2814440a5f56494438abe6f8a48709ceee95f9dd2e2fd66988a81050b465eee1ad68
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-3.debian.tar.xz' diffutils_3.10-3.debian.tar.xz 14284 SHA512:d14670c94e28b5cb1f074fb240c16d3f1405f681225c49e72e5332b4054acaa0aeb667c336e4bc10c5e6238c7c1d8697754c6d2c1b07a1e6a08cad35f699886b
```

### `dpkg` source package: `dpkg=1.22.18ubuntu2.2`

Binary Packages:

- `dpkg=1.22.18ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.18ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.18ubuntu2.2.dsc' dpkg_1.22.18ubuntu2.2.dsc 3422 SHA512:9ab4c75ed3a98fb9644ed6d8bbacace8772b9fa3daa587c8509127dfca7b3e9e3a22b5704a98dd5b31b82edbcd06206b68d5cceaf12df56a6656be7b61b112a9
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.18ubuntu2.2.tar.xz' dpkg_1.22.18ubuntu2.2.tar.xz 5678344 SHA512:e11f7c394b6d7ad66c8183b7570a629ccc8b8b4085202b44d63490e171da9b9f9f81d6c4078df87aa02b19e82183c0b50595bee9bca6bb5cf7c215e6fed6ccab
```

### `dpkg` source package: `e2fsprogs=1.47.2-1ubuntu1`

Binary Packages:

- `e2fsprogs=1.47.2-1ubuntu1`
- `libcom-err2:amd64=1.47.2-1ubuntu1`
- `libext2fs2t64:amd64=1.47.2-1ubuntu1`
- `libss2:amd64=1.47.2-1ubuntu1`
- `logsave=1.47.2-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1ubuntu1.dsc' e2fsprogs_1.47.2-1ubuntu1.dsc 3289 SHA512:86e1d742f5459eae99979a4f6ee780c0ce2e26089e802b0fc0c03932a43bbf7b6b321b3d1f426b030352b6aa375d4b19aea82d1a913f92b3ee64e62480c66088
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA512:dd89139c5e2bf999a22d999686ef06ab42f6ad537c6aeaa3fe68d9734d734b7396fd7ab2fd8002be26860c5653991a666d0df06c804c2f1f07f1274468ec728f
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA512:a22d46cc37497861d5a7e50076b40b8be6f459790f6eaacf0446200776fb74492ca9bfc7abc19edda3c9f7f722c318827b02f9cfbbb2118a8e86bce4d446d56b
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1ubuntu1.debian.tar.xz' e2fsprogs_1.47.2-1ubuntu1.debian.tar.xz 94228 SHA512:3d50e03fabc43643c1e7ad1eafecf3ea2da8967b339ab46a20817e90aead1fd5dd61ae4f06d7d8cd7a634105a3f9b7bc230cff8b843d210a43957f16a1295e16
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA512:7a651b7be4777d486eee6fc81ba656734e7952a1adae79c3c5d6a5f02441fa04841026dbbd3d9f2d627f4c627d7e0c54c6756e2ffaf3ba47222be3671c81d73b
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA512:b8b683d21cd26c6da4f41c56e83cadbda4780f8610a2bbd4b4e34bb1f339c3209721974b03e076d5eef0331fd876d947b398197aad37c29bbcc2e0405c641b34
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA512:a835153a0671309021be187bf78afee58d9682acb40545aaa9dd187f0ebdea0cfa5583bd03f363243633ea056ddb0a7a6603987ab5e34a608426cb4265ac6d8f
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA512:578c4fa152b39e0e0b9d5ab1ea146889ae53cb623d01f84a93d0ba936c9355b2bc5eb20bd761e5638226a040d131edaba60cc573bb3ef4f04889cd5067d167f5
```

### `dpkg` source package: `gcc-14=14.2.0-19ubuntu2`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-19ubuntu2`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-19ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-19ubuntu2.dsc' gcc-14_14.2.0-19ubuntu2.dsc 42459 SHA512:7c304fa2a43099084df38257044e71071266994c114462dc16621a17e5562f164613e4a7bcb59945db9d7bc5fd06f818302d60876a779f577d0f6e24346e2d97
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 97158172 SHA512:88621e344786a78d825110dbd46a9dc811ab0a3414bde97a700b0c90991020dc31dbba89cdbed24ef2875a63ae9c0adffdbc1064262e5270d80920c9964bfb21
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-19ubuntu2.debian.tar.xz' gcc-14_14.2.0-19ubuntu2.debian.tar.xz 2611952 SHA512:de1615d15b5bd326437ef1a6389f1e7b066d568a52f9bb482add2b5933a5f7ccdb7f9ecd0a67ee8d7bc93450b49dc62c09df89408adf31a04be7cc0e1bc42d73
```

### `dpkg` source package: `gcc-15=15-20250404-0ubuntu1`

Binary Packages:

- `gcc-15-base:amd64=15-20250404-0ubuntu1`
- `libgcc-s1:amd64=15-20250404-0ubuntu1`
- `libstdc++6:amd64=15-20250404-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-15=15-20250404-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15-20250404-0ubuntu1.dsc' gcc-15_15-20250404-0ubuntu1.dsc 52259 SHA512:25eece040d5d4b9376983287776589749cccd02d5c5b9b333574bf78b5cc1f5717b2f55f610d1ba8e508255686230b75f8097be2f8f46c1cdcfdc4788762fa1f
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15-20250404.orig.tar.gz' gcc-15_15-20250404.orig.tar.gz 96130378 SHA512:2d2e4ae8119deb4cdcb0674761e791341de44e5353a056a847e9cd64afec6cd248715e0fc13946a7f7a944a55758486fd986953f6bdf666a03e175e9ecf32429
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15-20250404-0ubuntu1.debian.tar.xz' gcc-15_15-20250404-0ubuntu1.debian.tar.xz 910700 SHA512:f5c3db85b95b30066881d49531da3a93058cccd8f4a970d4b8d5df0638ff10979f371e6ca6369f5101e68621add312aea5ef3fdcfde3e9825eabaf4dd529928a
```

### `dpkg` source package: `glibc=2.41-6ubuntu1.2`

Binary Packages:

- `libc-bin=2.41-6ubuntu1.2`
- `libc6:amd64=2.41-6ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

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
- `GFDL-1.3`
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
$ apt-get source -qq --print-uris glibc=2.41-6ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41-6ubuntu1.2.dsc' glibc_2.41-6ubuntu1.2.dsc 8035 SHA512:c9dd4bc8a005ea3251fa42a5a2a523fe59be31f963be9aad49653a87f39784d2e8c92d881a0f89dca8a257a662a617f2b529ccd845e94791e575a9addc380427
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41.orig.tar.xz' glibc_2.41.orig.tar.xz 19344868 SHA512:894a3e5a796bc13df30c26a5bfbe4d60b5dbdaac54e7763432235124b547070c7dda88c50584536870cab79183d8cad73a3ac6ed09bfe54fa8482aad07253169
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41.orig.tar.xz.asc' glibc_2.41.orig.tar.xz.asc 981 SHA512:98462e1a1abce7ae7214b48bce160ff95ffb6634708d9952a0997575ae1fb06f4499e01953bace0933e07fddf583f0dfe93221c44192957a894a4126ab073ce8
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41-6ubuntu1.2.debian.tar.xz' glibc_2.41-6ubuntu1.2.debian.tar.xz 463092 SHA512:ee8501aeefa9f4141b9ccf4eeb137167f92df677eb661781f4cab18c11ca691f3c76b685700e9fa0a7148af45e91fd5e4d07fe77a7a60a75ae7d73dfd1d4fb7a
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-3ubuntu1`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-3ubuntu1`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3ubuntu1.dsc' gmp_6.3.0+dfsg-3ubuntu1.dsc 2337 SHA512:88827f1cde0e5e1ed94c5218e9b05fbc39ba7f5116a07fded70e8e5269e2019c5b2f2636a7b29af1372b3a4b48f9fc915fe56d577cacd9003ebd3d4ac1f3619f
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3ubuntu1.debian.tar.xz' gmp_6.3.0+dfsg-3ubuntu1.debian.tar.xz 39716 SHA512:d40277a99b8f356cae8be53907cb089929c6757f0aa6042996b37f608b645b4e97b633bb17c1b4dc5aeb767b28efa51dda65239a896240c814c0bfe859404a2f
```

### `dpkg` source package: `gnupg2=2.4.4-2ubuntu23.1`

Binary Packages:

- `dirmngr=2.4.4-2ubuntu23.1`
- `gnupg=2.4.4-2ubuntu23.1`
- `gnupg-utils=2.4.4-2ubuntu23.1`
- `gpg=2.4.4-2ubuntu23.1`
- `gpg-agent=2.4.4-2ubuntu23.1`
- `gpgconf=2.4.4-2ubuntu23.1`
- `gpgsm=2.4.4-2ubuntu23.1`
- `gpgv=2.4.4-2ubuntu23.1`
- `keyboxd=2.4.4-2ubuntu23.1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnutls28=3.8.9-2ubuntu3.1`

Binary Packages:

- `libgnutls30t64:amd64=3.8.9-2ubuntu3.1`

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
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.9-2ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9-2ubuntu3.1.dsc' gnutls28_3.8.9-2ubuntu3.1.dsc 3351 SHA512:7851890e82962cf418cfdd3f1242cb497dc5dc5001f5332662c42c9390340ef2f5159f103043bfb92633b1942c7c1182ed06ab9afc562da63cc399e7bc89b543
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz' gnutls28_3.8.9.orig.tar.xz 6847364 SHA512:b3b201671bf4e75325610a0291d4cd36a669718e22b3685246b64bde97b5bd94f463ab376ed817869869714115f4ff11bdc53c32604bb04a8ff8e10daa6d1fc7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz.asc' gnutls28_3.8.9.orig.tar.xz.asc 833 SHA512:0eb265bbbc1ee735ecf4e3d308eacf3e3aebe4a9b0848af1fb340ec18e78bb516e1c74a6a72d4764bb03086d88d3ada3cd7ed82861a8f4ca7a403d9a5eb9a3a7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9-2ubuntu3.1.debian.tar.xz' gnutls28_3.8.9-2ubuntu3.1.debian.tar.xz 91256 SHA512:249843675237cb3d206a4bfb9cdee870d1d71240a9a1867c144d92354f262beb0aacd5b99b42a4028a20932bca2f273d218b0989dd9c0d68de24d15dbd9cd8ec
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

### `dpkg` source package: `gzip=1.13-1ubuntu3`

Binary Packages:

- `gzip=1.13-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu3.dsc' gzip_1.13-1ubuntu3.dsc 1933 SHA512:83f2c4c9726b75b65db28ced4450ec788d3e6dbab6aaf5ab80a6a20aca9fd23634344767ccfcfd109cceab9423d006b7a29b85b20c7c17319134c3e5afa6c97d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA512:e3d4d4aa4b2e53fdad980620307257c91dfbbc40bcec9baa8d4e85e8327f55e2ece552c9baf209df7b66a07103ab92d4954ac53c86c57fbde5e1dd461143f94c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu3.debian.tar.xz' gzip_1.13-1ubuntu3.debian.tar.xz 21364 SHA512:cc6c1acdb8ca29bfcdbc75c462504b57c867e13313bc229a8cebcf681ca0c347af8e5c36da072d1b6e38d13eeb06bca74b97cce4b67306d6d17be6ff66ba6537
```

### `dpkg` source package: `hostname=3.25`

Binary Packages:

- `hostname=3.25`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25.dsc' hostname_3.25.dsc 1519 SHA512:85590af72545c02ad4d84e63cf548b6277356f3b2cf448f5278409fbb87b40a2177a3bb983120effb838cdb8a546c5b243810ae558238fc5aff6f5fe1300e32b
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25.tar.xz' hostname_3.25.tar.xz 12804 SHA512:57b8e741cd3d895112d93ca8a7cbec95f3ad1a90c5691377ab8b242906bdcb932fa3401159432ec86f24bbbfe24c078832792c70e62e8d65a2317ee05a5efc64
```

### `dpkg` source package: `init-system-helpers=1.68`

Binary Packages:

- `init-system-helpers=1.68`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.68
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.68.dsc' init-system-helpers_1.68.dsc 2209 SHA512:4c8477f718287a3001fc378938e2e3bdbf15dca7a8aac93fdb65fe458408294b15c7e05ad6b5bcf04eda927ba934ca7f201cea2ff93090c8906b7b5abadf920e
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.68.tar.xz' init-system-helpers_1.68.tar.xz 45168 SHA512:3962845b388ee5c22de26a17e216ddd7f706d4f67729c80891c1457bf3e3fd70484b04f6d9d42adde7dad72da5529ac6feda97c9e2d4c0f4ccbfec2217a8e1b4
```

### `dpkg` source package: `libassuan=3.0.2-2`

Binary Packages:

- `libassuan9:amd64=3.0.2-2`

Licenses: (parsed from: `/usr/share/doc/libassuan9/copyright`)

- `FSFULLR`
- `FSFULLRWD`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-2.with.nonstandard.Autoconf-data.exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-2.0~Archive exception`
- `GPL-3+ with Autoconf-data exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libassuan=3.0.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2.dsc' libassuan_3.0.2-2.dsc 2682 SHA512:73edc82147084f103adf4791ac4ad41f4558edaa31cb3669839df1af46e3e078d7201e051a77dfc910019517974e6147cbd3b0a47c2c223242a8c37ab173bfab
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2' libassuan_3.0.2.orig.tar.bz2 593917 SHA512:a591eda350ecbf4fe8568b5087f69830df31f36ec67e2a50672aacea9bee16020f374a0bface459aeac1897c048072415ab5962a97034ce6fa413100b2a427fb
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2.asc' libassuan_3.0.2.orig.tar.bz2.asc 228 SHA512:56e0a8288e498bbba504fdaa84060ef6dd30c72efd691d6d0e39069113a394f2da407d83adfd14f7ae25b8e8531f8e9dee859b52471261653dc2ed5f44ef22dc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2.debian.tar.xz' libassuan_3.0.2-2.debian.tar.xz 17536 SHA512:45fce9ebcc65162f74790c67d6615ead69fd201e5933df68431e3696c76367bfe521c346fe0bf4a8b914139fd9dc644885bfda9805cf32b51de9044493f4f3ba
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
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA512:253b89208ff4acafb45c4294fe668d15d7a2f539745dffe6fdb4464fa672e39631dd92f17da4fe44f3084a967b783a39ea221cdd48fbbb30c49f520d60a0c447
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA512:ce43e4f0486d5f00d4a8119ee863eaaa2f968cae4aa3d622976bb31ad601dfc565afacef7ebade5eba33fff1c329b5296c6387c008d1e1805d878431038f8b21
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA512:c2e56aa572ce50d6342c0e45622958eba40319e09d45dc3cff6296cb10eebc0c4154d6f758dd2470a1794251fc0273d05ac2d735698eae83183769df5f7d44c3
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA512:82241267d3fdba624a118af842647cd2a57c202fb9a1f53b5303e258e3a55a9d33bf52e449c4d2656cd5baf8059f2976a082c592c30b0f4ac800ab48ab9d1dec
```

### `dpkg` source package: `libcap-ng=0.8.5-4build1`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4build1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build1.dsc' libcap-ng_0.8.5-4build1.dsc 2307 SHA512:445e82bbbd3ce274be18d37af59c4417c7278a6ff5497ee4b9dfa28054ebb58730eda206bdf0162de92e48e85ed5ca1d9ddcb9ef0c0d1ec54ae1a921ca6dcdbb
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA512:3bd868c7f263b77edd2feda831470b407f1086b434618e54336fb78bbf8bf3bad53f4c006a2118fb594b16554f8f7ec2acb76e08be5586d0261684e9ba139231
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build1.debian.tar.xz' libcap-ng_0.8.5-4build1.debian.tar.xz 7872 SHA512:8b0b4c8aa95667190a30e1e8c7883404b92dbfb76d2ef4a52b3d4cfac95dcfec2a7850727feb0084f6fa1b6d249ca82bd8be6adb7796148c79c419b5efafda71
```

### `dpkg` source package: `libcap2=1:2.73-4ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.73-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.73-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.73-4ubuntu1.dsc' libcap2_2.73-4ubuntu1.dsc 2311 SHA512:1989e68a69d332e00bffd99cc9311c4772a59788a5bdc9bb5a70c179b9803a43566c6b3e91cc0611994b76521afef3030537dc2ce5d1ccaa3c923b93ef2d0db4
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.73.orig.tar.xz' libcap2_2.73.orig.tar.xz 195276 SHA512:8ab72cf39bf029656b2a4a5972a0da4ab4b46a3d8a8da66d6cde925e06fe34df2fa5fc4d0b62c9cec4972b0b2678fdac6ef9421b6fb83c2a5bf869cf8d5fdb16
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.73-4ubuntu1.debian.tar.xz' libcap2_2.73-4ubuntu1.debian.tar.xz 20816 SHA512:5e0306bf245105e9958908f4671b37f6c3580b2875c08dcb364c4ee060930213e5a7e9520d41965e7814987e436c267b9adc04edfbbb6e087a5ff620188af775
```

### `dpkg` source package: `libeatmydata=131-2`

Binary Packages:

- `eatmydata=131-2`
- `libeatmydata1:amd64=131-2`

Licenses: (parsed from: `/usr/share/doc/eatmydata/copyright`, `/usr/share/doc/libeatmydata1/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libeatmydata=131-2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libeatmydata/libeatmydata_131-2.dsc' libeatmydata_131-2.dsc 2512 SHA512:b1d4b6ff9f3b2366479b7d39f9247fb8ec9369e166fe76440c12258c512a7fe7d6a24e84ad8725b0099f88fd79fff05eddedeb7d464609815c3cb32249042d75
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libeatmydata/libeatmydata_131.orig.tar.gz' libeatmydata_131.orig.tar.gz 368469 SHA512:064417dc085cb82e4baf1d160fcde2c6e0d9fed60e5c595799630b030053c373d888853055894c127c5b384be9204e8bbb251877651811b5fc5cdca8ffd9cf42
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libeatmydata/libeatmydata_131.orig.tar.gz.asc' libeatmydata_131.orig.tar.gz.asc 833 SHA512:56f3973131b31e4436d22fab43553937c6ecf5ec995dbc48dba01e0bed0a3347f54308477958297fdf2c72e77a531425073d0f80cb3e6112c88f3fb8a2d0b25d
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libeatmydata/libeatmydata_131-2.debian.tar.xz' libeatmydata_131-2.debian.tar.xz 16292 SHA512:9b9bef88513c93e91ccd5989521990cc066421651845ac422ad46eaca9401fa747fd6e719a274d6eb4f53a85128174c4921106761dbca0a43faeca597d7eddfe
```

### `dpkg` source package: `libffi=3.4.7-1`

Binary Packages:

- `libffi8:amd64=3.4.7-1`

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
$ apt-get source -qq --print-uris libffi=3.4.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.7-1.dsc' libffi_3.4.7-1.dsc 1948 SHA512:21fa6206acb5620ab9bea46342a7951cdefc0d07b7fab57cc75ced51b8cb5eb8d0ffd6fda4cd710d6f0945dad11580e3b37d9e2c24e6a9ddb81e6ed94fc4c143
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.7.orig.tar.gz' libffi_3.4.7.orig.tar.gz 593636 SHA512:fa852c9d9bd618bfe8089b6af4879e5440f9b7bdd89d52d1f1d193308cac35249a1243c254a4b6f7100d59a03e2705c32db822128e935fb24898675232403b30
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.7-1.debian.tar.xz' libffi_3.4.7-1.debian.tar.xz 10776 SHA512:25a6baeac0d2899e48b56426cf9c21cd914b302319014877a7da5975bd0a847bf8f6806326c62c8b0f90f7f23e82a02ba96f1d355d93867801af709bc85a6af6
```

### `dpkg` source package: `libgcrypt20=1.11.0-6ubuntu1`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6ubuntu1.dsc' libgcrypt20_1.11.0-6ubuntu1.dsc 2984 SHA512:4f63db3009d6a91aa989f0b8c45d1a6f722f89f99829b464222d1fdddc0c1df383cf6403fedfa9739637f219b9756f11a4c4c245fe42908968af8b7701fc844b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA512:8e093e69e3c45d30838625ca008e995556f0d5b272de1c003d44ef94633bcc0d0ef5d95e8725eb531bfafb4490ac273488633e0c801200d4666194f86c3e270e
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA512:eebd4c599bd8f375445566c3c73df5a223f256cb650cf18d8fed033a1f13a1fb8b9b10a17d686be21ad2bced60fc8e27d71b07e5f556a854a893e44c5dd81ae7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6ubuntu1.debian.tar.xz' libgcrypt20_1.11.0-6ubuntu1.debian.tar.xz 39784 SHA512:d7cb33ed130ba6de0339aa1030a13a5e272a2d43f26f9922107d1699f0c339c968aa538c014b817e8a2815141be2e2147deb7f0d3402be99ed256c14f621b105
```

### `dpkg` source package: `libgpg-error=1.51-3`

Binary Packages:

- `libgpg-error0:amd64=1.51-3`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.51-3
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51-3.dsc' libgpg-error_1.51-3.dsc 2955 SHA512:974e31ec297b7fa09f4557b5e8cdbb2f01df65b0252fb7e8b0233bb868dc66d2d701995f7a2ecdd08068cbed3dc8f1269e1be15b4384305fe6dad86a95abf3de
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2' libgpg-error_1.51.orig.tar.bz2 1085510 SHA512:4489f615c6a0389577a7d1fd7d3917517bb2fe032abd9a6d87dfdbd165dabcf53f8780645934020bf27517b67a064297475888d5b368176cf06bc22f1e735e2b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2.asc' libgpg-error_1.51.orig.tar.bz2.asc 228 SHA512:526890917db6547b6b2fb5a462c2a74501187579e4f156845952ebfb01595a77a0eda94b24350349abaee3ee8caac1d7ea6da005115467b5892c758842af3003
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51-3.debian.tar.xz' libgpg-error_1.51-3.debian.tar.xz 19888 SHA512:a06bad3675b611d473eacd8f10fbb09c2a4a2577be71bf3ea0e344e250d08c8e385d26b15eb683af7558a54908d95afbaa52cc564dd15547c82bb160cdc65d20
```

### `dpkg` source package: `libidn2=2.3.8-2`

Binary Packages:

- `libidn2-0:amd64=2.3.8-2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.8-2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-2.dsc' libidn2_2.3.8-2.dsc 2961 SHA512:142c67327595556c9e180da78aaf9792f7093742312cc3648a52c1d9f4a6ea934005f9c54b091b4d0fa7af7eed0819fe10012d50c3eae7d9a4ee6b774aef0179
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA512:e3f4ec5113f531d2b1827a11d7292318fdc49032c013b0076911b075b0e879428db9b45fe137aa37bf9c60e672b6883c035f9f45b2b42625031534965d518bc1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA512:f5c7f1676018b1cd362e250dd8ad59150c34b11ede9a21dbaf6f2e88fa943c881db6e59bf3e9180567379173cb21c4c893d835db99f4ed9e94bd80f84fb8ee2c
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-2.debian.tar.xz' libidn2_2.3.8-2.debian.tar.xz 17532 SHA512:4a321abeeee77f54d310481be841b14efebde37ebc58dc5ba5ef6397643f9f1d71bcd20ea3a52a5ab087bf0b3e3359de74172415264afa4c8bdf8fd62d3fff66
```

### `dpkg` source package: `libksba=1.6.7-2`

Binary Packages:

- `libksba8:amd64=1.6.7-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.7-2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2.dsc' libksba_1.6.7-2.dsc 2482 SHA512:239da32159ba455f0f76d8a89899e177a04e4621220d24c62b3faa341508d9ee9ac56fccee881b3c2bcba6965806f1c2083c49c47beb0c805ab8e8650975406b
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA512:60cb9df9f502ca479818f45b78c4bc2b78f6f359be2b8da489ea98f8896a43ab2c20cf97526b79a3220fb32f1701e62a6481fe61e91e567186ecf4f33d8e64d3
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA512:66208b8e4fe76a753943f13a0e65b765eb496013f7f9aeb0b66a454dfb8c67794d1b70841a4014ef0c7ac4642d7b56c38b35cb34be9d8ee8ea6820cc13db53aa
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2.debian.tar.xz' libksba_1.6.7-2.debian.tar.xz 14872 SHA512:92fd1450d10419f232cc0e0604f232aae57cff4b05b471b456ed21d40d36c1bfaba7f108cfc57a856d409cbd5421a47cb1d4ca848b127a73161e7f1c0e4e332e
```

### `dpkg` source package: `libmd=1.1.0-2build2`

Binary Packages:

- `libmd0:amd64=1.1.0-2build2`

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
$ apt-get source -qq --print-uris libmd=1.1.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build2.dsc' libmd_1.1.0-2build2.dsc 2383 SHA512:d5d7a38fe932fa60a25630e0ba3ab5ef231b47ac5190e3b04e5c6130f8121a440594955031f9bc52338a29af0b119c696171b3447c46ac71967d7878fd572cd0
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build2.debian.tar.xz' libmd_1.1.0-2build2.debian.tar.xz 8428 SHA512:3e4caf3b94503176a782241f319a5ed19fb3e9e8dd4056e59beb6fd7208c45ce77396fdd2e8a9c18ca19a65f93b49834853b13f2fbba59195e5499736113d776
```

### `dpkg` source package: `libseccomp=2.5.5-1ubuntu6`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu6`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu6.dsc' libseccomp_2.5.5-1ubuntu6.dsc 2831 SHA512:fe3adbb3791a96a88f0eb92791254eff386fb16a8501e3bd98aaa1bc88ff0aea7ff73ff071b5385e4abf8d970f0674ec4ce3f90e9a8c85b560ea4001caa1d4f1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA512:f630e7a7e53a21b7ccb4d3e7b37616b89aeceba916677c8e3032830411d77a14c2d74dcf594cd193b1acc11f52595072e28316dc44300e54083d5d7b314a38da
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA512:a32a7146598f9183179ad15603181d1066e806d01f7c5f215d5405ad8618c06a265d05fff3b4a6cc49c50a577d93d6b920e85f6a581786b3db7389f52a4638e2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu6.debian.tar.xz' libseccomp_2.5.5-1ubuntu6.debian.tar.xz 24524 SHA512:134db79f1009ce22ac1a2ab51ec970493d65c6ed74c67dec18b76b2ff3da201f05c8f9d43629ad3d744258f3785c3c3b02c20c3de5ba820a20a78e922f067412
```

### `dpkg` source package: `libselinux=3.7-3ubuntu3`

Binary Packages:

- `libselinux1:amd64=3.7-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.7-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.7-3ubuntu3.dsc' libselinux_3.7-3ubuntu3.dsc 3097 SHA512:e2a88420477dc313916ab9d87fe778406853c1b49c4649d793ae41043c72810a535f88fb43b9e7a7bf5a46a81be07b50418cd8411dd1d3efed452cf9802270c8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz' libselinux_3.7.orig.tar.gz 194834 SHA512:e949c20b606c50ad521b9592ce55ad6658e8c4b24d9838028f5aba0a4fc762b6d0d0d0d207f5bef7a2e41485e12d91382fa6090df27152dbb40071b273419352
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz.asc' libselinux_3.7.orig.tar.gz.asc 833 SHA512:5be2fdc0deda62f240276413d1b95a57d467fe989ddb31b34f7743cbd03d69385ac3321af10c97aded119ae5f0a4d8ec5894f8647a45f2902c0e8ff1e96787aa
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.7-3ubuntu3.debian.tar.xz' libselinux_3.7-3ubuntu3.debian.tar.xz 45060 SHA512:b5e0c9e2865a7749029510993623a318830e49b81f6bcb0b67dd0db8d02521f2e0c5ff65d06c58a7e39278858383ddd2b58cefbfd93bcddb6a1a3da552446d1e
```

### `dpkg` source package: `libsemanage=3.7-2.1build1`

Binary Packages:

- `libsemanage-common=3.7-2.1build1`
- `libsemanage2:amd64=3.7-2.1build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.7-2.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.7-2.1build1.dsc' libsemanage_3.7-2.1build1.dsc 2997 SHA512:3df874a1944cd8bd038171865995653998f66c96f7e91241f394fab788a97f5faba69b881ad15b2db3330d8c3c0cce99fb6f52c19121eb81f13a68527eba14dd
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz' libsemanage_3.7.orig.tar.gz 182896 SHA512:4b6370b02116364964ff24b93fb6629c885611de78419f649a027db38b4f1c3b3adf3b438efb34a92b49407ab8f9446ed4091fe4c99fa4752f0f5e3e31589415
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz.asc' libsemanage_3.7.orig.tar.gz.asc 833 SHA512:670ea358add41fd07828ffeb83aae676cd1fdc9abbad8afaa3fd9ee1f42891ec4ae03320e324bac99335159e4e2794bbc3c6f66715cae47b1745b609abd68e34
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.7-2.1build1.debian.tar.xz' libsemanage_3.7-2.1build1.debian.tar.xz 36736 SHA512:d3f9f0e179823af9bd93eb0a82e655f39df3e71b7b27a025389521874669a26e5d3c2a1622a1b0a021780a365c821fd7a6db49740052b8750c19d857b97dc7bb
```

### `dpkg` source package: `libsepol=3.7-1`

Binary Packages:

- `libsepol2:amd64=3.7-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.dsc' libsepol_3.7-1.dsc 2085 SHA512:f6739a13677ec7575fa3a84c3877780c23fbdc65a1a4d1d4a5d9657438fc6b66ddb59390271837d04266c02e087a862ea6ab49cb302596fc95abd7c931a0a467
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7.orig.tar.gz' libsepol_3.7.orig.tar.gz 511487 SHA512:85d12d0ba5a7a3225f08d041a18fd59641608db5e0a78a1e9649754e45be54a807cd422d4889b88da6e806b4af546336c7a0913448f08ac33dc6ffb983890ef8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.debian.tar.xz' libsepol_3.7-1.debian.tar.xz 27632 SHA512:9809b3b82c0f816c7fb9b2ec2eb5be8ced95d2d774aebb0834c6848621d0b337ef2950d98602b75e1619db08fb90e4e59e5a0025dfa1a782222addc9535318d5
```

### `dpkg` source package: `libtasn1-6=4.20.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.20.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.dsc' libtasn1-6_4.20.0-2.dsc 2665 SHA512:250e24dd3def4ee1fde380a2d1d323461e03fb54a8d729481ebffc4d81229aa5261b5045dd427b3e413d5a040cd8d882f98cc002c798d5ae5ebd1e2abab6a896
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz' libtasn1-6_4.20.0.orig.tar.gz 1783873 SHA512:0c0660085f5e80537aa3d65197967029be6cc5e27d7029789713902989c1694fdb49421ae0415b79b953e11893bb4bdaada85f7aff847dd0bb4075c91887e7b4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz.asc' libtasn1-6_4.20.0.orig.tar.gz.asc 1223 SHA512:bb5da128c20ed8f1e7c681c779ac3d2e455c661d779a4a7a70a6cabc1ea4139df9d0acfd145545acc8fe41df6490fd7d3c2df4b8d7560891291abbf56ac3afdb
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.debian.tar.xz' libtasn1-6_4.20.0-2.debian.tar.xz 18640 SHA512:9db15608ffaf0aaf9be92fe0654f4cdc37e59eebcc35cc0e136779965efdc53944f09aacabece25b3f571981ebd8659621f1e3f0a2b6a8ebb625eaa645f14a93
```

### `dpkg` source package: `libunistring=1.3-1`

Binary Packages:

- `libunistring5:amd64=1.3-1`

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
$ apt-get source -qq --print-uris libunistring=1.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-1.dsc' libunistring_1.3-1.dsc 1578 SHA512:ae608322cf14e0c63923e3afe3c4579e27cd1cd0e759f0bd4952ea6d7139c67d77235bc2e37af22319d5581528b5ddaae18df2296778c6f3d139dcccf003d3c6
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA512:864d42b1d4ae4941fe5c8327d6726ab8e3a35d2d5f9d25ce4859a72ab2f549a7b68f58638cf8767d863f58161d1a4053495d185860964a942d6750e42facf931
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA512:829229528acc8f9d13de4c43fea6caddacaf1f1cc201a7927b2c140d7ac5a81e213a1a20ba67766d6867fbe301ddddf78685f5af54e67906160807d6e8028b5a
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-1.debian.tar.xz' libunistring_1.3-1.debian.tar.xz 28376 SHA512:9a9af7fb85038a76176004113b534ae557b465e51b8c9cb883cd8c56384d38d2dbb9452c89bde5d1475dd668c9225bebd92e3a0bd04e8be6099dd50c38e60f28
```

### `dpkg` source package: `libxcrypt=1:4.4.38-1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.38-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.38-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.dsc' libxcrypt_4.4.38-1.dsc 1573 SHA512:b5eb8267ac958ceec61885d333358a326893e998c0e4c4b1f6ca03d96830fc2e95c627995ef6b96578bd69d0f2f408aa30e168b6a9bb34348ad08368f71b1b6d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38.orig.tar.xz' libxcrypt_4.4.38.orig.tar.xz 394216 SHA512:4310a38e7cb8c337f52ea4ed47561ea548583426276f5ec1f6a52f9435e0508b8c81427947e69e7dc77dee6187fe0c16d1e90d261d857d52d0e58e737230dce4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.debian.tar.xz' libxcrypt_4.4.38-1.debian.tar.xz 8512 SHA512:502912be5e86f84cdd66cae37fa615e2a151ed0ecc3ba904e1365be8230000aaefa20cdd60e27abeadb1960cc041fe05573cb153bb264a032e10db25ca937ad7
```

### `dpkg` source package: `libzstd=1.5.6+dfsg-2`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.dsc' libzstd_1.5.6+dfsg-2.dsc 2369 SHA512:28574f72ec7ca9d3d309ae09db9652327564c1544ea2ae669297ca873e654a9a3065802e646768382b3af8846f836219aa8dc25e1c450f23656746ef362b7cd7
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA512:487f37a3cf2a14c57606f0593d43bde00265f59093edf61f10c3c3190676bd7d9fe81d67dc3ef3c925b9e3d6a9ad5ea9e49590a28253965e93b0e72c43acd9c7
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.debian.tar.xz' libzstd_1.5.6+dfsg-2.debian.tar.xz 23088 SHA512:8b15a4c7a921237bc80558775e072c30f4e813b93b03f021c24ea2a81e30220975e9692e19d2589cbe244dec14337ef9c7615977f4b1e515d1b39de30cd7bb70
```

### `dpkg` source package: `lz4=1.10.0-4`

Binary Packages:

- `liblz4-1:amd64=1.10.0-4`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4.dsc' lz4_1.10.0-4.dsc 1941 SHA512:359c0b31d3ea1017f7beac58a54394ca547b5656d0d02fe6685ed854486166ab17f10fcfaf052d0b4e94d802f6ed3b7bdd555652ebbe6d79a6d079ffc19acd1c
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA512:8c4ceb217e6dc8e7e0beba99adc736aca8963867bcf9f970d621978ba11ce92855912f8b66138037a1d2ae171e8e17beb7be99281fea840106aa60373c455b28
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4.debian.tar.xz' lz4_1.10.0-4.debian.tar.xz 8080 SHA512:66d6522837ddda23e264f4cbf6c08506868c29183ce476f06297732b6d5d4746ece4e99f6797741f55accbed188d13ab9889cd571dedf38c3b0e8f365323e27e
```

### `dpkg` source package: `mawk=1.3.4.20250131-1`

Binary Packages:

- `mawk=1.3.4.20250131-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20250131-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131-1.dsc' mawk_1.3.4.20250131-1.dsc 2969 SHA512:59ace327f075ca3a95ecb593157d1b3d447ec1a8e82cd6b0c95fe721cec780261549d443d33f9745e655c711c2c2c9cfe1196bc9c6c1b10ee84cf6b02c059394
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz' mawk_1.3.4.20250131.orig.tar.gz 433213 SHA512:100b1f5ee190d2841d5dee449c53601a6d32453e47b232de919f3489f6f7040d0c6d21f6c7d30df616b04abde2db9799c5eb16570c1f88dbc10fcd75c5838042
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz.asc' mawk_1.3.4.20250131.orig.tar.gz.asc 729 SHA512:0d8ac93bdafcd8915b0d2d2b675f8d5cf2aeba655cd04af4b4037336b74b320e02db360b7d18b796aedc09fbabc8a42e471766ea24219bad7a1cbff4f7679552
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131-1.debian.tar.xz' mawk_1.3.4.20250131-1.debian.tar.xz 16008 SHA512:c4ebe147a302078a8dfe4f064a988f6dbce748c236c4df237a58190de56fc2abab6fd4c47cd0d6ea28dc44a3286d1cf7ad2e8f6661578495a0f168a574bc6cf8
```

### `dpkg` source package: `ncurses=6.5+20250216-2`

Binary Packages:

- `libncursesw6:amd64=6.5+20250216-2`
- `libtinfo6:amd64=6.5+20250216-2`
- `ncurses-base=6.5+20250216-2`
- `ncurses-bin=6.5+20250216-2`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5+20250216-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.dsc' ncurses_6.5+20250216-2.dsc 3890 SHA512:31270767544127e7606435e7f3c7863f6891527cf865172103c355ffca20ef541511aa34524d95a67fa0834d6db81007c933a4b44b1cb075a59048827a5156dd
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz' ncurses_6.5+20250216.orig.tar.gz 3774714 SHA512:c1f4b59469e553716371950036d707e1acc2363a100ba97fdc76713994fc20aa2003e97ad5b0f036f128546566f039cc6731ed32ceb06aae390937fe74a7f13f
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz.asc' ncurses_6.5+20250216.orig.tar.gz.asc 729 SHA512:245c5f9b521415da59e78d1ba830f291a97cbe0d231e0303c1dbf3bc4f0cfee58799ec96fb58aec453f12fda8a2a286ef25d421442d3535818d3653c7435f662
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.debian.tar.xz' ncurses_6.5+20250216-2.debian.tar.xz 50420 SHA512:9320a766d0122da06330f6bbcf14aa5fc13b600ea76b0a2a060a620c16e443c4f3d318c47668a0acb72ed257f8400fa3b262ce9c904332af482a81bceef889e7
```

### `dpkg` source package: `nettle=3.10.1-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10.1-1`
- `libnettle8t64:amd64=3.10.1-1`

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
$ apt-get source -qq --print-uris nettle=3.10.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.1-1.dsc' nettle_3.10.1-1.dsc 2053 SHA512:f72ed4ec2168e73e16a49f7af1730c3152503f544c9e4a3a75003db8b107b48c82cca0425dfb860cf33b110bd440077523980472559b128201d613e55a4331ad
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.1.orig.tar.gz' nettle_3.10.1.orig.tar.gz 2643267 SHA512:e8673bbcde9cde859ccae75ed6c9c30591e68a995a7c6d724106cfd67a5a5bd45b3468d742443b6565628849d0fd29505a28ca5ee4e89dd13197cdb51429f96c
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.1-1.debian.tar.xz' nettle_3.10.1-1.debian.tar.xz 25036 SHA512:2e28dec9813cae7fc0a28262f56c7e671521dac4b54266538c67f445773af41b7a8070caa5f40c39c2d4e50730993e12089297c7dd6f8efe65e8455f2a795902
```

### `dpkg` source package: `neurodebian=0.42.2`

Binary Packages:

- `neurodebian-freeze=0.42.2`

Licenses: (parsed from: `/usr/share/doc/neurodebian-freeze/copyright`)

- `BSD-2`
- `Expat`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris neurodebian=0.42.2
'http://archive.ubuntu.com/ubuntu/pool/universe/n/neurodebian/neurodebian_0.42.2.dsc' neurodebian_0.42.2.dsc 2109 SHA512:48b0d177c067e1a91c02b19e820ece08dd66093a15c5e5c42d81fabc531d770a13c99dd1fc647cfa3bb7c3ac720cf2cf196e1f18778f5f8d56c0bfa94238f255
'http://archive.ubuntu.com/ubuntu/pool/universe/n/neurodebian/neurodebian_0.42.2.tar.xz' neurodebian_0.42.2.tar.xz 8322504 SHA512:ca72f1a2f3b601cb2061d51dba81e4e8c0ccfc097a62295dd4603a7a907f4c1458148e26f4f09dec2050083f430822ec37407788c0d3bf1ad71049d1a96ffa9a
```

### `dpkg` source package: `npth=1.8-2`

Binary Packages:

- `libnpth0t64:amd64=1.8-2`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.8-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-2.dsc' npth_1.8-2.dsc 2188 SHA512:5f684de55b5c4a69e6f2d8debcd6011bea5bedd5a05f69cc6442a9692c43fa30685a213c1f66b157d2f6f9a6f7c7c03471af68f160618b43e5f5e619f6097a99
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2' npth_1.8.orig.tar.bz2 317739 SHA512:34fdeea3d8a7a594d8fdbcc6d5d389b5c8e282e8e84c1491b1e51960c0fa007df6a1d62543f0107f0772f3215557d4b25c2a9c7067cb0ae2f8de7b4d63d09fb4
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2.asc' npth_1.8.orig.tar.bz2.asc 390 SHA512:2d2d26d2bde77997187792f724b89b6c1ba7ad845c0087d78d7bd2eef688136df8fa8ea02c5199c0a3ad602bf228af0fadf82ecd3ff4b9ed35c71d009bb2e1a5
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-2.debian.tar.xz' npth_1.8-2.debian.tar.xz 8908 SHA512:496224bd84f7c1b369d540ca33213b6b58696ff4ac34285807734329d134f131f292092ab4a7b8f5b02f555b623c587d1d1fc424a79d2b541b33a411645dd6e4
```

### `dpkg` source package: `openldap=2.6.9+dfsg-2ubuntu1`

Binary Packages:

- `libldap-common=2.6.9+dfsg-2ubuntu1`
- `libldap2:amd64=2.6.9+dfsg-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libldap-common/copyright`, `/usr/share/doc/libldap2/copyright`)

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
$ apt-get source -qq --print-uris openldap=2.6.9+dfsg-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg-2ubuntu1.dsc' openldap_2.6.9+dfsg-2ubuntu1.dsc 3377 SHA512:2e96420e2415ed996eec4cac9fc98daa1a309db3a1849251008fc507cf1f714647ad401bd1387baa9139c09352b156b7c94ea5505228d8a2733f1e7d8da8ff11
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg.orig.tar.xz' openldap_2.6.9+dfsg.orig.tar.xz 3753260 SHA512:0789b8ad8b2ede51741e18e3f090a258edc7abeda90cfadae98b9a22126be901f3640d4121411836608918418108dfb71ae0957dbd251d9c3ce6bd1b854dd799
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg-2ubuntu1.debian.tar.xz' openldap_2.6.9+dfsg-2ubuntu1.debian.tar.xz 184328 SHA512:519c318c45e9d536aa71a8902746c5fe67ea3069939dc447a0534b4749f1f28ff88585b168b87e42f524a2dc92bc96d2345b1a5d0265f20857c42a7431e0b68d
```

### `dpkg` source package: `openssl=3.4.1-1ubuntu4`

Binary Packages:

- `libssl3t64:amd64=3.4.1-1ubuntu4`
- `openssl-provider-legacy=3.4.1-1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.4.1-1ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.4.1-1ubuntu4.dsc' openssl_3.4.1-1ubuntu4.dsc 2844 SHA512:7fff79b497236e824bc5fa2d4b8a6f87c08a4f1e295bb725660cacb96a709e4a4642cabdc4c03ffc7323154048baecc3825c4c835a998efaf5837fbd4ea89725
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.4.1.orig.tar.gz' openssl_3.4.1.orig.tar.gz 18346056 SHA512:1de6307c587686711f05d1e96731c43526fa3af51e4cd94c06c880954b67f6eb4c7db3177f0ea5937d41bc1f8cadcf5bce75025b5c1a46a469376960f1001c5f
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.4.1.orig.tar.gz.asc' openssl_3.4.1.orig.tar.gz.asc 833 SHA512:b007d5a35a7904d5d5e053e232a54b2ba75fb43f80bf1fe2175528e86e31cca8161da09d7417b50359008ce1955497e4d11c46794f15cc7c3220aa92eff99ccb
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.4.1-1ubuntu4.debian.tar.xz' openssl_3.4.1-1ubuntu4.debian.tar.xz 121720 SHA512:17ae44c4a95ee4c0d49236b706083e8a0054b78a6c25f14e1ef4d9b70375db404e96f39214dc02a1d8c92ca708eaa31662ac6041f7574c619ac95834705d1a97
```

### `dpkg` source package: `p11-kit=0.25.5-2ubuntu3`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2ubuntu3`

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
$ apt-get source -qq --print-uris p11-kit=0.25.5-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5-2ubuntu3.dsc' p11-kit_0.25.5-2ubuntu3.dsc 2398 SHA512:b1d2f2361307d39aedf39ed3500769eba9d8f9e35ba22d2e7e2d35304552c48638589207883e5e0028dece9e3639d9740019f73ca067136cbf9c0c86cd4bc77e
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA512:177ec6ff5eb891901078306dce2bf3f5c1a0e5c2a8c493bdf5a08ae1ff1240fdf6952961e973c373f80ac3d1d5a9927e07f4da49e4ff92269d992e744889fc94
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5-2ubuntu3.debian.tar.xz' p11-kit_0.25.5-2ubuntu3.debian.tar.xz 33532 SHA512:1debf9e41be4c2ea2af53981bb4a7e29d54e679409793637685a5ac8f3a1ec681f3b55d21382cbd94018705c820d6344792f29537af2c67f9e87cc86dfb10251
```

### `dpkg` source package: `pam=1.5.3-7ubuntu4.4`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7ubuntu4.4`
- `libpam-modules-bin=1.5.3-7ubuntu4.4`
- `libpam-runtime=1.5.3-7ubuntu4.4`
- `libpam0g:amd64=1.5.3-7ubuntu4.4`

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
$ apt-get source -qq --print-uris pam=1.5.3-7ubuntu4.4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-7ubuntu4.4.dsc' pam_1.5.3-7ubuntu4.4.dsc 2727 SHA512:9cca422499d6d68f5c73f408b9257b8e430c4fa47879cc69f81e60fb0a14f4af4423cdeac3d3a135ac36a00baca855692db99caf6a3c8f33fd121c1c6f516031
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA512:af88e8c1b6a9b737ffaffff7dd9ed8eec996d1fbb5804fb76f590bed66d8a1c2c6024a534d7a7b6d18496b300f3d6571a08874cf406cd2e8cea1d5eff49c136a
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-7ubuntu4.4.debian.tar.xz' pam_1.5.3-7ubuntu4.4.debian.tar.xz 204472 SHA512:172e0970c28848ec943e91671c3fcd0e82444f7013e278ce4de03106271113e6382a9b89ece1cbb3a6ab44ac5cf6c902019501d69c45efb06bf69d4cdd79f4ed
```

### `dpkg` source package: `pcre2=10.45-1ubuntu0.1`

Binary Packages:

- `libpcre2-8-0:amd64=10.45-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.45-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45-1ubuntu0.1.dsc' pcre2_10.45-1ubuntu0.1.dsc 2318 SHA512:5e2e9fb8f93b52d4345f7d8f30272ba37fe38fc7184e1fa1abaca41b495b97262d3f2855328134ece2c215c03e778520e36db2b75889999b38dca6f8d3292af7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45.orig.tar.gz' pcre2_10.45.orig.tar.gz 2715958 SHA512:6ec01a05ce65be61e5974dcc2ccd2e2b5c6db183e3a592530205c7d3259b730df3a9ab999d204f3c52e5a14ae88f32f94306b4501eb9629568ce6158985e2fa6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45-1ubuntu0.1.diff.gz' pcre2_10.45-1ubuntu0.1.diff.gz 163076 SHA512:0fc9d8f7fbd244ed7ff0f25da3e9ce9c34d8c39ab076e4d76eccca4d5c68f5657470378f5c37e031f19dfd05a74857e22f2b03c730e1251733a1fa5feed4d400
```

### `dpkg` source package: `perl=5.40.1-2ubuntu0.2`

Binary Packages:

- `perl-base=5.40.1-2ubuntu0.2`

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
$ apt-get source -qq --print-uris perl=5.40.1-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-2ubuntu0.2.dsc' perl_5.40.1-2ubuntu0.2.dsc 3023 SHA512:88af975b4783728a34ab86c29f0621a45ec72d4f90b1d57a0c74ae8c4aae9f8df4ee3014b1a71499aff34364a6ba5b91e23a06a28ee1e2525361149291e38f29
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-2ubuntu0.2.debian.tar.xz' perl_5.40.1-2ubuntu0.2.debian.tar.xz 173116 SHA512:4c45dad2a52718e18e738992098bca11ec36e8d23868d8556fdf6d723fda2611869ce83eb6bbda72ccf9b7e3393e9f5b57663b5bfb6305dd567052cc81191e23
```

### `dpkg` source package: `pinentry=1.3.1-2ubuntu3`

Binary Packages:

- `pinentry-curses=1.3.1-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.3.1-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1-2ubuntu3.dsc' pinentry_1.3.1-2ubuntu3.dsc 3384 SHA512:5772b45e2d27342da414c513462675f987b3673efc7147bf92a6c479c4b2a7ca2a0d1a6051edaefe2d2a0fb6b1d866ef15f6523a17bebed7dae10ebe4a4f697b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2' pinentry_1.3.1.orig.tar.bz2 611233 SHA512:3b72034dc1792b1475acb6d605ff7c1bd7647a0f02d1b6bdcd475acdef24bc802f49e275055436c3271261c4b7a64168477a698aab812a145962146b2f67a0e2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2.asc' pinentry_1.3.1.orig.tar.bz2.asc 390 SHA512:499926442059c8f349b66beb16b6cf22cf0919b65a601af1bd0d60c96f60d44e0ad2bd090324585da5cb09e75286e11a4b92c553aec43b87f6cbe8a1e599882c
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1-2ubuntu3.debian.tar.xz' pinentry_1.3.1-2ubuntu3.debian.tar.xz 23960 SHA512:ce3ac0abab9cc57ba9f2f41526190e5aef2e65aee09c8348b501abee1b7d604e95cfcf607737ceb5427c5f5258dee14143b02fa472382b8e498d3071822dfc16
```

### `dpkg` source package: `procps=2:4.0.4-7ubuntu1`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-7ubuntu1`
- `procps=2:4.0.4-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-7ubuntu1.dsc' procps_4.0.4-7ubuntu1.dsc 2231 SHA512:838b2c69725050eda8d6ab3e4297593a1e89f16b86ad5ff8d8fe3413efc3686f11d3e1c8e04ede0ab6e22106a360f1861db614614a8ad46fc98b76523ac1518f
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-7ubuntu1.debian.tar.xz' procps_4.0.4-7ubuntu1.debian.tar.xz 38588 SHA512:26b50f8931c1df0750e0f7f36d585253a1443367f45242365207b6281b045583397a59f69b40ece53a22115988afd190d4b8742801fe75f852b4565aae228f30
```

### `dpkg` source package: `readline=8.2-6`

Binary Packages:

- `libreadline8t64:amd64=8.2-6`
- `readline-common=8.2-6`

Licenses: (parsed from: `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.2-6
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-6.dsc' readline_8.2-6.dsc 2810 SHA512:b748d32b4dcb87a209cdecf6d28f5e799761577b787d8a116fb59dc73f2aa421d64687fd5f5359f5d46e8915676720b83685d8eb70e9d2840d8bf26a068d9e34
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-6.debian.tar.xz' readline_8.2-6.debian.tar.xz 38396 SHA512:6e8f28dd4b3f7e579f97235d31dd19d5a452edb61af247652ffa4c5fd70de23d34581da71e8bba66beb69aa63311ce27177c27e55972cceb6ae886369faa2217
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

### `dpkg` source package: `sensible-utils=0.0.24`

Binary Packages:

- `sensible-utils=0.0.24`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.24
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.24.dsc' sensible-utils_0.0.24.dsc 1743 SHA512:7f5abddecd7ca44b37c278dbd1ba9515667cfea27fb4819e8b2187da199871855c53ba5115979484ec5f5ac0767c5ef054788d0082e10b597d502c8a620d1ff5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.24.tar.xz' sensible-utils_0.0.24.tar.xz 73568 SHA512:2db2b14bb4b8e616d0e22ac39c56e4e995ba565da59f624ea5ce8958d3eaf545d69136a518e30bd7183adde411607465d7d07fa8e88cc0d980b5d464f8a3b902
```

### `dpkg` source package: `shadow=1:4.16.0-7ubuntu1`

Binary Packages:

- `login.defs=1:4.16.0-7ubuntu1`
- `passwd=1:4.16.0-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.16.0-7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.16.0-7ubuntu1.dsc' shadow_4.16.0-7ubuntu1.dsc 2579 SHA512:bf1e673a911f68bad1b56fa82527c19b296ce358f000233ddde5f5db862a55c146d58dccc4836e85712d4fdbdf8ea2b5bafeeceed7aba32b18f4de31b8f175b4
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.16.0.orig.tar.xz' shadow_4.16.0.orig.tar.xz 2053720 SHA512:fdb6835b54b6507f853d9dcdbf4c794d8f808638226d6baf32c5b33e1aaef79159d7f957f4d515c9c770c6a735d74eeb70fa83337374bd0689341ee001fbb756
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.16.0-7ubuntu1.debian.tar.xz' shadow_4.16.0-7ubuntu1.debian.tar.xz 184116 SHA512:ef799ce47e9d81a751e076297835776ecaeb6c8ffd2b6c6159bd55bbefdd1aade92e47539fc8813be83a6209051d31cb6ee89cd98ff5168dd001cc7227923f28
```

### `dpkg` source package: `sqlite3=3.46.1-3ubuntu0.3`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-3ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.1-3ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-3ubuntu0.3.dsc' sqlite3_3.46.1-3ubuntu0.3.dsc 2747 SHA512:7e5e6438523773ba92f9ea68c02fca235213d91c14e425c79da06a73078280c0c09da851126ea880718521fc5efa40b40e9132364fd68691102f8c0a325ebdfe
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA512:a5ec0f57d014b2f33d679cfbae0ca1935eb84871376b29216ffcc286a92a363a823ca0ec729a000d702054ee90b2fcc1887c1fb4bebfabcd14894f8ef91b7ad6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA512:47d3c900d95641c89d5d807881e20e97f3b7889cf44c76d48715066ba5c1860defcd17498440d79bcc49b15c2ea28e81ed4b5b159f9e947941e5c1ee27de06ba
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-3ubuntu0.3.debian.tar.xz' sqlite3_3.46.1-3ubuntu0.3.debian.tar.xz 35404 SHA512:8059f30364ed09166c590c6d7ce23ac2f6e513066ec1b22941c975b04ffb0225305f998a57bb278090da552a9b4d0be40a3037df3f32f25a712d5f9c32e15fff
```

### `dpkg` source package: `systemd=257.4-1ubuntu3.2`

Binary Packages:

- `libsystemd0:amd64=257.4-1ubuntu3.2`
- `libudev1:amd64=257.4-1ubuntu3.2`

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
$ apt-get source -qq --print-uris systemd=257.4-1ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.4-1ubuntu3.2.dsc' systemd_257.4-1ubuntu3.2.dsc 8321 SHA512:7d84906c1605bd0dccc3c1c57eeddcbd271e314c041d8f207f87c4ccf960f909b42da136351db062d686adf70bdb9f4682c78647efd2de9fa05447eea3a3f9b7
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.4.orig.tar.gz' systemd_257.4.orig.tar.gz 16228313 SHA512:dfa0f6de38fa30daffabf6b02d6533ca4e7027188186d7e2e9648b99dad5c4afa30773138f18a34111e7bb2e6ddae8302284429b98b580e757dc67535846afbe
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.4-1ubuntu3.2.debian.tar.xz' systemd_257.4-1ubuntu3.2.debian.tar.xz 260316 SHA512:f4b79abefed88462475c248af36716e1c2a0c6ca552dd2aa4dbaca2218f7df40d953e5835b1e977324e69cc2e0762d641cec68e816a66ae38bcd37cabe8b19a2
```

### `dpkg` source package: `sysvinit=3.14-1ubuntu1`

Binary Packages:

- `sysvinit-utils=3.14-1ubuntu1`

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
$ apt-get source -qq --print-uris sysvinit=3.14-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14-1ubuntu1.dsc' sysvinit_3.14-1ubuntu1.dsc 2468 SHA512:3fbff17813340564faf970fab51c2e7b8dc115ec0196f836eae5329f9ef45129eba673460677908d0431601eba4e10e6be18630be84c1e596a56405b3d4d5337
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14.orig.tar.gz' sysvinit_3.14.orig.tar.gz 516357 SHA512:557b6ed9090e6594806b71c9fd054f32972fc6e7bffa4ef92a9dda42c5db08100f226b7b43c0433c1a1e9b16a3ebc483cb42d9aa29a5a3cfd5fc1c60984ef478
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14-1ubuntu1.debian.tar.xz' sysvinit_3.14-1ubuntu1.debian.tar.xz 122080 SHA512:17bf826ac424055cc7d8d153446a7eb0a749643dacb720ae514e016ea2d45bcf1631ea09134b630c7a67520cac1c4b43f170129ee79bd73b4230cc1a0108fe49
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
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.1.dsc' tar_1.35+dfsg-3.1.dsc 2017 SHA512:5659687f13ffd338bb7fb31427d0945dfef0e31cee1f5e646e32884c3927699d007dcb4128c0e5d2c8d886080ba47cfadc7d00abe75ee16c8f5f5ddfbd109e03
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.1.debian.tar.xz' tar_1.35+dfsg-3.1.debian.tar.xz 21540 SHA512:dd2f35961b183870644c62191b1cc60c2ddf29127e895757c249e65f2299d8b642b43f57e875f0a68bf894637d83a45132e01eecff361655963dcc1d393b4198
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

### `dpkg` source package: `util-linux=2.40.2-14ubuntu1.1`

Binary Packages:

- `bsdutils=1:2.40.2-14ubuntu1.1`
- `libblkid1:amd64=2.40.2-14ubuntu1.1`
- `libmount1:amd64=2.40.2-14ubuntu1.1`
- `libsmartcols1:amd64=2.40.2-14ubuntu1.1`
- `libuuid1:amd64=2.40.2-14ubuntu1.1`
- `login=1:4.16.0-2+really2.40.2-14ubuntu1.1`
- `mount=2.40.2-14ubuntu1.1`
- `util-linux=2.40.2-14ubuntu1.1`

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
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA512:c5cc95f63ea3eab2a2459e01d48a50b729b3af63ad0e3121e2b3776b54f1ab097f827a7cfb95b5d13ff4a1465a3d88f8876b6651f825fedf2f481b77b3118639
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA512:8b5c8b9aad4e869f28310b12cc314037feda81d92f26c23eaecdb35dc65042ca2e65f2e9606033e62a31bcc737a9a950500ffcbdb8677d6ab20e820ea14f2b79
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA512:737e2b1da8c6abb1c6bd84de7815513dbcbb72312bab4325003bc6bb91e363a44f862360dfd6b47d7286a6a7b59ba8c6892f9027fcda5924ba3d8d7baaee0d38
```

### `dpkg` source package: `xz-utils=5.6.4-1ubuntu1`

Binary Packages:

- `liblzma5:amd64=5.6.4-1ubuntu1`

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
$ apt-get source -qq --print-uris xz-utils=5.6.4-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.4-1ubuntu1.dsc' xz-utils_5.6.4-1ubuntu1.dsc 2811 SHA512:4087bea2f5c95acd8479de712a4cdfe1c777758e70191ab7d5a8d2b1399f51e9ce0492a52447b68bb4d9bb65eabc01359f66e0b5136585f1184fa55110fca175
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.4.orig.tar.xz' xz-utils_5.6.4.orig.tar.xz 1340516 SHA512:8b7d014d94aadba3dcc423d8702dcefd6c9ec0a33eb45444008a8998d8a6cb60945a551af8d919e04808e37ddab79c7ee0537246046a5700c8c11f74ed050ad3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.4.orig.tar.xz.asc' xz-utils_5.6.4.orig.tar.xz.asc 833 SHA512:f2d1ef72fbf869e139194822267a1cd42f04c6f6963d2004644bb9768833035d22f63d105d0a48f7dc5de6d3d1e7692ee40371bb9071df176963dcfdc5bd5b1c
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.4-1ubuntu1.debian.tar.xz' xz-utils_5.6.4-1ubuntu1.debian.tar.xz 33372 SHA512:123f9f3873c045b455760921a539ee568fdef6af9dbd1dd4f67961e53c3643ed42ba49b3df21a7fb81b4430aa90030b3c4736e7c00b08fbd7f07fad5e1b7d3a0
```

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu1.dsc 2993 SHA512:b87b9b973aa22f9cea28d9653bba4383a27203ffb391ff0df537225bbca131eb47b08bc12178bf4d05348e379159be275bddf2d611c97a6bcebd80a0f1ca6e8f
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu1.debian.tar.xz 59676 SHA512:c4d82f270d4334711e26d5d328683d0214d3171a2cfaff0b5b613d4df28adabf01e69ec9f6093991ef8f124f289826f30f2fc64223956462d26c9d67866482fe
```
