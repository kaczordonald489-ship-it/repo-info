# `ubuntu:26.04`

## Docker Metadata

- Image ID: `sha256:22026488e3a9b12c40ae2b1a85e1aabaa79bf58c1679008f054f9b640a7a2811`
- Created: `2025-11-03T16:26:18.744397676Z`
- Virtual Size: ~ 90.02 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=26.04`

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

### `dpkg` source package: `apt=3.1.11`

Binary Packages:

- `apt=3.1.11`
- `libapt-pkg7.0:amd64=3.1.11`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/3.1.11/


### `dpkg` source package: `attr=1:2.5.2-3build1`

Binary Packages:

- `libattr1:amd64=1:2.5.2-3build1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3build1.dsc' attr_2.5.2-3build1.dsc 2501 SHA512:17905511e791b643ffcaf83181474b1d7a7d1c7287adc20e35011c51d729089a2922ef3a41a33337b8a9401567eb7bc4f61e7aed54ba6d9c29d709f9e51c1dd9
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3build1.debian.tar.xz' attr_2.5.2-3build1.debian.tar.xz 32316 SHA512:223b89e4a0056bfcde8b3392a703759e004114daafeaee1e17d34078363ba6bb86eb43a45bc397966b27e4b4bd5740f854347de52095d9d95400829e02e8af36
```

### `dpkg` source package: `audit=1:4.1.2-1`

Binary Packages:

- `libaudit-common=1:4.1.2-1`
- `libaudit1:amd64=1:4.1.2-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.1.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2-1.dsc' audit_4.1.2-1.dsc 2546 SHA512:e15a01ca5f2f34698c3e8fdf2d0f3c020c2e3e14efa7df3e9652db7663cf0f2b7c6cdd44abe8c90fa0388f03d6840ea6eef59978debde12782ff1fda630ea9f5
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2.orig.tar.gz' audit_4.1.2.orig.tar.gz 656095 SHA512:a47fec1041e11a76ad57b57bcf6e9b454188d95ec26cabf15e92e114d46c7c8f09ddb251d5aebef8bc7faacc6ccffe44c73543d8234af237548b4ad89a408fc3
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2-1.debian.tar.xz' audit_4.1.2-1.debian.tar.xz 19712 SHA512:517cbcfaad3e2310535c349c74a3173b3fbd30e8ff0828ba844204bab43cc0a69fde1227944bb449a2c7eb2d9e906cdbe08f4e6494014e632d11be14a9ef47c7
```

### `dpkg` source package: `base-files=14ubuntu4`

Binary Packages:

- `base-files=14ubuntu4`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=14ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu4.dsc' base-files_14ubuntu4.dsc 1727 SHA512:2cc9f9886eee185dd4041825b5d60babb83f5792b67631f6591d3971e3cc9ed83a6d52ec6c9b8907bf3ee9e2b4fb1a6a8dbe99ae955d74d49406c8cff33914bd
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu4.tar.xz' base-files_14ubuntu4.tar.xz 96880 SHA512:19a0b42cd1acdd580151aaeddf635bffed436a8eccfff06a3b0ebf213601710ae489ad11e2a908e3865e8a1453646ab955f3b7cbd200829e69c0b70ed9559e36
```

### `dpkg` source package: `base-passwd=3.6.7`

Binary Packages:

- `base-passwd=3.6.7`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/base-passwd/3.6.7/


### `dpkg` source package: `bash=5.2.37-2ubuntu5`

Binary Packages:

- `bash=5.2.37-2ubuntu5`

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


### `dpkg` source package: `bzip2=1.0.8-6build1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6build1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6build1.dsc' bzip2_1.0.8-6build1.dsc 2205 SHA512:47d8fdf23ef3206d24a55f853c22afe119fd7477b5b4216124e660ed1bb480dc1a1e50e37ebbbe230f83ed98ff8df5bf6757637970f4ba4fac16933f3a6ca24a
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6build1.debian.tar.bz2' bzip2_1.0.8-6build1.debian.tar.bz2 27106 SHA512:a2ff1b0103beb918d33f75d8e096e9af2c3911604f81468045aa5e7f659f7e203d1144977a52a52b9abc9f1348fff7ed5f2d5bc8874795e68335a939b58a9e13
```

### `dpkg` source package: `cdebconf=0.279ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.279ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `coreutils-from=0.0.0~ubuntu24`

Binary Packages:

- `coreutils=9.5-1ubuntu2+0.0.0~ubuntu24`
- `coreutils-from-uutils=0.0.0~ubuntu24`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`, `/usr/share/doc/coreutils-from-uutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils-from=0.0.0~ubuntu24
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu24.dsc' coreutils-from_0.0.0~ubuntu24.dsc 1966 SHA512:2e03843c71f35a5e24b63b81f4cf203558d1c59fe7fad42ab13173737281829e9e4cd1b4840349dc2d28726008223655700123c8b0beb490ecdb5028336a6c36
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu24.tar.xz' coreutils-from_0.0.0~ubuntu24.tar.xz 7384 SHA512:2841b9435326c202e040b260ebf067ea13d922ec498adc837a8f33ba50a7b0f0afe8682acebeb534e083f932adb71ac66895db8a3afd2bc72d945d2b81c0a5ac
```

### `dpkg` source package: `coreutils=9.7-3ubuntu1`

Binary Packages:

- `gnu-coreutils=9.7-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gnu-coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dash=0.5.12-12ubuntu2`

Binary Packages:

- `dash=0.5.12-12ubuntu2`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu2.dsc' dash_0.5.12-12ubuntu2.dsc 2060 SHA512:b909afc805e76237bc59b9b46d6d4db1fe1bbb1ca7dd5589f5b21d6fa157a8ae7460a6f7e1086b7ce54acf940891b6c755dfb939e53a545cc0f7b98e66bf83e8
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu2.debian.tar.xz' dash_0.5.12-12ubuntu2.debian.tar.xz 48056 SHA512:93b8cadfaa68c84296962261e988e416ffd434305a536f238fbc89d49196ed1be4fbf158ddf47da977868841a9e9a97f32b6eeffb034f790d41a95c1d9e618f7
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-9ubuntu1`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-9ubuntu1`

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


### `dpkg` source package: `debconf=1.5.91`

Binary Packages:

- `debconf=1.5.91`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.91
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.91.dsc' debconf_1.5.91.dsc 2035 SHA512:523a2aedd2925d7417f166daf896176225733d4f308959b7dbec80f4d8e9a177fb6b6d282297a7f8da13b50afadeda6210c095dd6cd75dfd41f6ffdef90a1c9f
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.91.tar.xz' debconf_1.5.91.tar.xz 609964 SHA512:3c79aec120e660d0e74ae6a35747818a555172685d1258fff3c6622abe795858779159440f39bcf641955c335a07de8386cf0d0518cdae8193fe4f28d8492df8
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
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.23.2.dsc' debianutils_5.23.2.dsc 1908 SHA512:d58e2cf09f0b2a4b90c5fa5f5da814ae46784a009e7395b47c1e88d48deacd8cd04598303ed18f8b628bfc59867cfb9ad3a4b1015dc21d420e24cb45f1d54d12
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.23.2.tar.xz' debianutils_5.23.2.tar.xz 82376 SHA512:2ccc3993abee6be0b9e861d7937984a096a29a677584665f638e5a51057051d48fcc54283c1f43ab1179505298735600e5ebedd3b41386aa5bc697c8c91cef6e
```

### `dpkg` source package: `diffutils=1:3.10-4`

Binary Packages:

- `diffutils=1:3.10-4`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/diffutils/1:3.10-4/


### `dpkg` source package: `dpkg=1.22.21ubuntu5`

Binary Packages:

- `dpkg=1.22.21ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.21ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu5.dsc' dpkg_1.22.21ubuntu5.dsc 3457 SHA512:bacfda2e74064f756ebf0d2d63d8934be79bf15759b0f3dbb1cadee6bf08b6b124ab13dc4575abe433d3eb60e31b47420c5019cfcbb6dc7b8bd3c801f5a2ba3e
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu5.tar.xz' dpkg_1.22.21ubuntu5.tar.xz 5672956 SHA512:9ad9a6c51523a782c07ba4a979b11717d1e122f1983395caceae3ca5f5d93ac1b670206b08f789d9579b4ec2cc77d19dd07049cd1a1917e38beb4dcf3e918e67
```

### `dpkg` source package: `e2fsprogs=1.47.2-3ubuntu2`

Binary Packages:

- `e2fsprogs=1.47.2-3ubuntu2`
- `libcom-err2:amd64=1.47.2-3ubuntu2`
- `libext2fs2t64:amd64=1.47.2-3ubuntu2`
- `libss2:amd64=1.47.2-3ubuntu2`
- `logsave=1.47.2-3ubuntu2`

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu2.dsc' e2fsprogs_1.47.2-3ubuntu2.dsc 3292 SHA512:8a406035cf48048d701fb111a2b005be8e6a2844f0ab6f45730c992bd69b54039fdfacc6a23254728b0c980215c25cf415e2fdc322416e0767c4d60e5532d905
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA512:dd89139c5e2bf999a22d999686ef06ab42f6ad537c6aeaa3fe68d9734d734b7396fd7ab2fd8002be26860c5653991a666d0df06c804c2f1f07f1274468ec728f
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA512:a22d46cc37497861d5a7e50076b40b8be6f459790f6eaacf0446200776fb74492ca9bfc7abc19edda3c9f7f722c318827b02f9cfbbb2118a8e86bce4d446d56b
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu2.debian.tar.xz' e2fsprogs_1.47.2-3ubuntu2.debian.tar.xz 105644 SHA512:8e4ad2ba2648b6a59682a2330e03d08fe60c14bc42ccacd65d433a2d97fdd3a4c17445b93ab262cd760d53820b5c06bd1d16cf682de4a635a7ed787d00e75adf
```

### `dpkg` source package: `findutils=4.10.0-3build1`

Binary Packages:

- `findutils=4.10.0-3build1`

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
$ apt-get source -qq --print-uris findutils=4.10.0-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3build1.dsc' findutils_4.10.0-3build1.dsc 2315 SHA512:86071c1b54ea862018bfd2d075bd5500a7e3e5743fbdf5ea7f8ee967ee8928a08ab03b76a73c385612dee17ad347b8584aea2b0ba33652950e3f172f6a91ba0c
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA512:b8b683d21cd26c6da4f41c56e83cadbda4780f8610a2bbd4b4e34bb1f339c3209721974b03e076d5eef0331fd876d947b398197aad37c29bbcc2e0405c641b34
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA512:a835153a0671309021be187bf78afee58d9682acb40545aaa9dd187f0ebdea0cfa5583bd03f363243633ea056ddb0a7a6603987ab5e34a608426cb4265ac6d8f
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3build1.debian.tar.xz' findutils_4.10.0-3build1.debian.tar.xz 33448 SHA512:c0181cf386b1da519d6e6b5fb81d1740f2a47cfa7cd0c3405509c2546c9d9c97fae5a879466f753d56cd6b3738084daefad65ee0e13bb1d389a6ac52bd1fa714
```

### `dpkg` source package: `gcc-15=15.2.0-7ubuntu1`

Binary Packages:

- `gcc-15-base:amd64=15.2.0-7ubuntu1`
- `libgcc-s1:amd64=15.2.0-7ubuntu1`
- `libstdc++6:amd64=15.2.0-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glibc=2.42-0ubuntu3`

Binary Packages:

- `libc-bin=2.42-0ubuntu3`
- `libc6:amd64=2.42-0ubuntu3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gmp=2:6.3.0+dfsg-5ubuntu1`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-5ubuntu1`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5ubuntu1.dsc' gmp_6.3.0+dfsg-5ubuntu1.dsc 2337 SHA512:bb1aeca249c2c1f1bc969af7263ce3ee41ac41f8d14b8df1e5e6d000427b93c0a75d35b533968e83a75d50bc8cebec4f0fe339527abd9ad04f06f6c65aab5685
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5ubuntu1.debian.tar.xz' gmp_6.3.0+dfsg-5ubuntu1.debian.tar.xz 40264 SHA512:a03385d079b3917af6d6760e8b1055499052562a532c4eea72ef8c5fd95422094b8c2435f7cd3ee4f0a2d007c07cf3947c23a42080cbf77e02c37febc97339c5
```

### `dpkg` source package: `gnupg2=2.4.8-2ubuntu2`

Binary Packages:

- `gpgv=2.4.8-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/gpgv/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12-1.dsc' grep_3.12-1.dsc 1647 SHA512:267043711608634df53a28221afeacb510ebeb85c10bb69257f3860552704651852097f2c447c14728f1c0c4212bfdc42f9ad69cfd11faf4232d702da717fae6
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12.orig.tar.xz' grep_3.12.orig.tar.xz 1918448 SHA512:c54b4db5a8b9afe098c088decd94977746305284d716666a60bac82b4edc0fae4acf828970b5b6fc7d58ecd549f638e17e6958f33a71fedcc7d7415b9228b161
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12.orig.tar.xz.asc' grep_3.12.orig.tar.xz.asc 833 SHA512:333755fd9e5879436789a19e9593667d6fb96c2d1b876a1c391eb9cd75d10bb7fbc10215db9838280e6006790c818ef4583b1ae22318a833a5b69264ca15dbf1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12-1.debian.tar.xz' grep_3.12-1.debian.tar.xz 24160 SHA512:b7e3aed1874a943a8fcef27e55040f64304c3ecd505b20e6dbec4ce9b5ec658de1b5434c21afe4f4cde31115cab5532ed728311b19c4ee99537697cd7ddb6ba0
```

### `dpkg` source package: `gzip=1.13-1ubuntu4`

Binary Packages:

- `gzip=1.13-1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu4.dsc' gzip_1.13-1ubuntu4.dsc 1933 SHA512:28e928fb761398aed1e66355c6cdba4042842bcd4f8288f89f2f711675ddfb310afc5fd84319a95360b9d532d18a059055f8b0915d834313cf51c5e627c4c85c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA512:e3d4d4aa4b2e53fdad980620307257c91dfbbc40bcec9baa8d4e85e8327f55e2ece552c9baf209df7b66a07103ab92d4954ac53c86c57fbde5e1dd461143f94c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu4.debian.tar.xz' gzip_1.13-1ubuntu4.debian.tar.xz 21444 SHA512:0fe5f34300df6de43d296bf03a4dc1a73c744b46b091afe4fab273efd1cc2abb50ad471b7b999399cf2c5405c128ec0b8df58dc4d4b0a2ec75913e57687e06f5
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/init-system-helpers/1.68/


### `dpkg` source package: `libbsd=0.12.2-2build1`

Binary Packages:

- `libbsd0:amd64=0.12.2-2build1`

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
$ apt-get source -qq --print-uris libbsd=0.12.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2build1.dsc' libbsd_0.12.2-2build1.dsc 2371 SHA512:640dd4f3b3c5ea0ca4992972f6b6288b807cd5ddc71587b7dab2dfaaf04a5598e0757120ad0576ae0374b2f2088f8285ce19270f4838d43b7c204d705548aaae
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA512:ce43e4f0486d5f00d4a8119ee863eaaa2f968cae4aa3d622976bb31ad601dfc565afacef7ebade5eba33fff1c329b5296c6387c008d1e1805d878431038f8b21
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA512:c2e56aa572ce50d6342c0e45622958eba40319e09d45dc3cff6296cb10eebc0c4154d6f758dd2470a1794251fc0273d05ac2d735698eae83183769df5f7d44c3
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2build1.debian.tar.xz' libbsd_0.12.2-2build1.debian.tar.xz 18772 SHA512:309194f4de6788370c496c0f7a3de4eac0312aa1afb1d33b73f66a2378b79160c1649d3cca8f07e7dd8a6974d93fec529ff489d231a80c021076d21a72b3792e
```

### `dpkg` source package: `libcap-ng=0.8.5-4build3`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4build3`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4build3
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build3.dsc' libcap-ng_0.8.5-4build3.dsc 2307 SHA512:2106b7d4acad64838bb09c143f6b14d13b23e29780458f2b6e99ba966e255ed7a5ce975f47d87dcf159d0d6a5ddb9683619ea5f804fe1908edd407eab9c93570
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA512:3bd868c7f263b77edd2feda831470b407f1086b434618e54336fb78bbf8bf3bad53f4c006a2118fb594b16554f8f7ec2acb76e08be5586d0261684e9ba139231
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build3.debian.tar.xz' libcap-ng_0.8.5-4build3.debian.tar.xz 7984 SHA512:ffdf06b1f2b298aecf0d177fa2c0a734f541a475f0f73115a2685088edf6ba32e71bb6dc5924c598d8e09174fe474f4c7c95b3a055211b6e1b1258957d7f84c2
```

### `dpkg` source package: `libcap2=1:2.75-7ubuntu2`

Binary Packages:

- `libcap2:amd64=1:2.75-7ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgcrypt20=1.11.2-2`

Binary Packages:

- `libgcrypt20:amd64=1.11.2-2`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgcrypt20/1.11.2-2/


### `dpkg` source package: `libgpg-error=1.56-2`

Binary Packages:

- `libgpg-error0:amd64=1.56-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.56-2
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.56-2.dsc' libgpg-error_1.56-2.dsc 2955 SHA512:8bc77179e6e81f6394382a174d7b3e6eeffd6ae2044655de9b32fab7dfa4c71ce5506d2361c6e6a0b8a69d5f465b4695975807cc7f7e8ea10bf54601f189cb5e
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.56.orig.tar.bz2' libgpg-error_1.56.orig.tar.bz2 1116017 SHA512:ff4160f4133cf1a90eddf5f59d6248214b59db4f021f124302be37bf04fa1f2eb665560914cbe289095e630a31ba141252e7a72a8e6dbbc622cb135a2066259a
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.56.orig.tar.bz2.asc' libgpg-error_1.56.orig.tar.bz2.asc 265 SHA512:467e926eecd8d1fa3f8ac0fc8a3d8698ac8b4c93d462483c817fe4328eb7f5a15f3ff230eee96054d8c3a5c4469ee57a89923f170128eca1c4a5ac734f4c7178
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.56-2.debian.tar.xz' libgpg-error_1.56-2.debian.tar.xz 19664 SHA512:c70469a302898538140e86da50371b7f077f7cb57a433fecbe8a71e075dd9ca256314ad4f4ec33dbb9656322791ef2080cc8ee642a8cca5e79835c90a94eead1
```

### `dpkg` source package: `libmd=1.1.0-2build3`

Binary Packages:

- `libmd0:amd64=1.1.0-2build3`

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
$ apt-get source -qq --print-uris libmd=1.1.0-2build3
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build3.dsc' libmd_1.1.0-2build3.dsc 2383 SHA512:d17d4917d2ee6a78b2cf321ce8316b67a1942be9f02969e4e1919b93bd7fcb60cc59961460a137fcd3f1f2a95aed0260627f6128b377f3e7fb3f735a860d6783
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build3.debian.tar.xz' libmd_1.1.0-2build3.debian.tar.xz 8496 SHA512:6606245527851f4221e19de38a6d6c18bffc4981bd1e9ed1db307ff9b204a0378742c714b127f5434a5434dae27eff1f227c17fe59d3107b2dcc4fd686175ab0
```

### `dpkg` source package: `libseccomp=2.6.0-2ubuntu3`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu3.dsc' libseccomp_2.6.0-2ubuntu3.dsc 2745 SHA512:464db24c875efa21af1d0436aeb6cebab6778d0d7974321a1feca750638a3d86e4b0322490b3345fe59569ee72114035e02bd9803fc9ea2a917383f214b875dd
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA512:9039478656d9b670af2ff4cb67b6b1fa315821e59d2f82ba6247e988859ddc7e3d15fea159eccca161bf2890828bb62aa6ab4d6b7ff55f27a9d6bd9532eeee1b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA512:973b69c58085a1567f860e621e3a197be02c0ca71dad664234418cf5c00c39767efd37a7c4016f1be5bd588262617b6603855262db2ee6f31bc16061bc130e0f
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu3.debian.tar.xz' libseccomp_2.6.0-2ubuntu3.debian.tar.xz 27864 SHA512:d97de13336aa498ad3362e9df40f6ccb0226b7f04c05561488bafc9c70c24df545ddd41fd00cc59ada193c7a9e4a9861837c984ce13877c033222581ab4b7ba2
```

### `dpkg` source package: `libselinux=3.8.1-1build2`

Binary Packages:

- `libselinux1:amd64=3.8.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.8.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1-1build2.dsc' libselinux_3.8.1-1build2.dsc 3036 SHA512:3e36fd4cd13a2f0c975cb25233f2d867f0a71e2520a01caab1302f2859db2234579f3829619c949834a85561ef7b3cc831f9a6ec7752b215e0b2e2448060264b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz' libselinux_3.8.1.orig.tar.gz 204411 SHA512:646a31dff3b670a530adb9fc2fdc3ca9fe34a58e67e0fac52cc33bc7a01fa63c175987ef254c6c3bc7299cef137bc6f258dc378f4d70ae5c0fa0ece3bef42ab4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz.asc' libselinux_3.8.1.orig.tar.gz.asc 833 SHA512:ece79feb7758eafb8cf60092039596971140d8af7049671dfa8a7be6cc3167e928e361d8a9b26abfd855520413533890c280eec1e8107b260e3bbadb79c5159a
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1-1build2.debian.tar.xz' libselinux_3.8.1-1build2.debian.tar.xz 37932 SHA512:2cdb957366d6b22717cc7943c1d7989f8d9ef2e519ad3114e73b825beb4b7a2f077b0d3005229a2ecaf27a03872c9df45545800f08015099807c887ac910f2e6
```

### `dpkg` source package: `libsemanage=3.8.1-1build1`

Binary Packages:

- `libsemanage-common=3.8.1-1build1`
- `libsemanage2:amd64=3.8.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.8.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1-1build1.dsc' libsemanage_3.8.1-1build1.dsc 3015 SHA512:06fcbce7b00d55e5a1fad0257a6a087c9981ab4c3a1c6d30994ea98098f9d54506374c3d52413693c410c5c9dd01bc07ac46d9ed3d87e76f1baa0d95fef1d4b6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz' libsemanage_3.8.1.orig.tar.gz 184618 SHA512:ac3729ba4934a48a33e082af35baa9e25e6806855afb0f0e4e22aa67be201518c3d4933b8cf4dec83e5acbe178301276f51850bb1b16bc13e027a470ac7f1eb5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz.asc' libsemanage_3.8.1.orig.tar.gz.asc 833 SHA512:b21cf3e0a5e28ddddaaded81fc00080d13a8aaac44357bf980fa1c28899e50e0791b66f407eaffd6ce0719caee356e02e576947949cf5cb34665fe0bb90f7108
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1-1build1.debian.tar.xz' libsemanage_3.8.1-1build1.debian.tar.xz 37624 SHA512:23855a5deb0d6a199be9bab7440f47b5ede1218fdc45d4383fa88d8045a0f9aa9d404cce0384429eedbb214c55e4e7b7c02add25ecfd0753b9a368ee2194b0bc
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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9-2.dsc' libsepol_3.9-2.dsc 2326 SHA512:8402a41b450fc815c37dd8163905ff9f04ae692372dd0ff7ed1aacd2d22144e2096ad69bb49685b0853317d7d11f870e2fecc30c76a4f6297407e6b2207d4e74
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz' libsepol_3.9.orig.tar.gz 515726 SHA512:9a198fb0b7f4981939e6556ba690892bda77446785c2015cdf4178fa303095186f255dfbebe04e6749a139379718a012349aa7a70fac94a860a3745c0536afe9
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz.asc' libsepol_3.9.orig.tar.gz.asc 833 SHA512:a84d39be1ab744d70c6df7f170f429f6625218e304c748317188670202de6bc2175a88b4b006c451aa3874c28881fbe09f6dfcc13022f3cbbef2acd4a886a992
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9-2.debian.tar.xz' libsepol_3.9-2.debian.tar.xz 21416 SHA512:f5c99799993c4950352f43c7e5fdae4383eb8f8ecabb50b51812ccdad8250cc31090348eef26da2ac9f6c4a66b4313607514249edd7eafd17ea1f6adfb047a97
```

### `dpkg` source package: `libxcrypt=1:4.4.38-1build1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.38-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libzstd=1.5.7+dfsg-1build2`

Binary Packages:

- `libzstd1:amd64=1.5.7+dfsg-1build2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lz4=1.10.0-4build1`

Binary Packages:

- `liblz4-1:amd64=1.10.0-4build1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `ncurses=6.5+20250216-2build1`

Binary Packages:

- `libncursesw6:amd64=6.5+20250216-2build1`
- `libtinfo6:amd64=6.5+20250216-2build1`
- `ncurses-base=6.5+20250216-2build1`
- `ncurses-bin=6.5+20250216-2build1`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5+20250216-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216-2build1.dsc' ncurses_6.5+20250216-2build1.dsc 3913 SHA512:2fad33a34cf46f3e07a44a190581f5256acfc4ffb4cfd8518bbe9343727591df0ecbeab915607dc27550ac0633a506c07f35a6a6f4e550fb004b6dc04593f8a5
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz' ncurses_6.5+20250216.orig.tar.gz 3774714 SHA512:c1f4b59469e553716371950036d707e1acc2363a100ba97fdc76713994fc20aa2003e97ad5b0f036f128546566f039cc6731ed32ceb06aae390937fe74a7f13f
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz.asc' ncurses_6.5+20250216.orig.tar.gz.asc 729 SHA512:245c5f9b521415da59e78d1ba830f291a97cbe0d231e0303c1dbf3bc4f0cfee58799ec96fb58aec453f12fda8a2a286ef25d421442d3535818d3653c7435f662
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216-2build1.debian.tar.xz' ncurses_6.5+20250216-2build1.debian.tar.xz 50504 SHA512:5545f0e1c10fcb635fb7801dbd73519ae5e2b27b202b028ad04ba4fc1db39e954cffbb7e910ecca6ae739c8f3ba838632afe15aca8881a200e95988953ba9e8d
```

### `dpkg` source package: `openssl=3.5.3-1ubuntu2`

Binary Packages:

- `libssl3t64:amd64=3.5.3-1ubuntu2`
- `openssl-provider-legacy=3.5.3-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.5.3-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.3-1ubuntu2.dsc' openssl_3.5.3-1ubuntu2.dsc 2600 SHA512:3ab238c4502490f90ea7d5227302d43baa1a8ae5b0b8536eaac6d387bdf11a75914d40c4ba0e0452113f50cac310788462c9ed34aa0fb280faa368d9dfa321c7
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.3.orig.tar.gz' openssl_3.5.3.orig.tar.gz 53183370 SHA512:58265c05d208a269418d4928d3127d22738e696d5d080ab8f1c0cbd2cd30e4e1e07e244a1d81c9b40f1a7f972fe835f4f122c098a7b2177ac48492881416aa78
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.3-1ubuntu2.debian.tar.xz' openssl_3.5.3-1ubuntu2.debian.tar.xz 67424 SHA512:8288788e75092aacd0789284f95a08707b131a37b5f1b31cec134f82debac4a6af63ed6a65dc6025e45bfe584e8ec63ed99037ef95ae02739479014c65a5f189
```

### `dpkg` source package: `pam=1.7.0-5ubuntu2`

Binary Packages:

- `libpam-modules:amd64=1.7.0-5ubuntu2`
- `libpam-modules-bin=1.7.0-5ubuntu2`
- `libpam-runtime=1.7.0-5ubuntu2`
- `libpam0g:amd64=1.7.0-5ubuntu2`

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
$ apt-get source -qq --print-uris pam=1.7.0-5ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu2.dsc' pam_1.7.0-5ubuntu2.dsc 2908 SHA512:56a7d6814c52d5a0fc4d0e080092bdaa781861e23e5dae6dd1b8acd0c769eefcc1e4b4338675b3347dfd198ce1f961921eea97283ea137178c77683e78231f2b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA512:ab5cadb0eb5e95e36146fdbbc77eef4e5e0f38aeee4e819b080a1316f69969c3c33e4a2daf3246ded4c2e58ce517d7f1acb0d8de02a4898ff753f4c3aeec51cf
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA512:573bef1d63c0ce4efb5d1efd71a582f6ff679f2e278c326f66e142175cf67e42404453d41b92c5ce201b7d41db7b0617695f0d0972a812f0ab19553dec37192e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu2.debian.tar.xz' pam_1.7.0-5ubuntu2.debian.tar.xz 194076 SHA512:5daf8f4f18754fb8c61a81888b2a2fe67b0c2cc7cab473d943410c0781b1f59cbabb784230c5f3e2962326c9b721333141d3238b2f7441b600b474cc93be48af
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46-1.dsc' pcre2_10.46-1.dsc 2337 SHA512:9b0e023c151a5f76178b0663b7b36c4650f352c3a3f86db04d845726414f35dff9e7452ae5812013a32e0aec66d729a16ae1cf7f47e60d06a6e46ca371bf5fc6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46.orig.tar.gz' pcre2_10.46.orig.tar.gz 2718545 SHA512:8bc85f1e47633f4cab07e00b65e9f94a38bb8db56d7ea0a3068774a5ccfe5b777e6645c0a345dd265a06aa6672448ad51c9e56636c48ec87dae9f884a998e00b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46-1.diff.gz' pcre2_10.46-1.diff.gz 8748 SHA512:b985f1cc087449f80ba19812bf903b798d3772bbddf599dbf377e5a41aedbec8c711bc7f1c2cfd51fbddc29f478961ab834dd64a34809c5bbeb6cd2cb8694165
```

### `dpkg` source package: `perl=5.40.1-6build1`

Binary Packages:

- `perl-base=5.40.1-6build1`

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
$ apt-get source -qq --print-uris perl=5.40.1-6build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6build1.dsc' perl_5.40.1-6build1.dsc 2932 SHA512:249bedfe2613348fd33408c66d957102ac235c7d94473e90641bf60bdf7db600ac0300208b843145c5494f82988bfb6284018554bc78a84173e16884bc07a426
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6build1.debian.tar.xz' perl_5.40.1-6build1.debian.tar.xz 172908 SHA512:c8a4135968ee5a462f853a2651b570e9c9bff5305f4f6dc8dd5356904aa97d4f148eca8ce32cb12515e284f4067b8a4408cdb47f2675b43183017721c41b6dd3
```

### `dpkg` source package: `procps=2:4.0.4-8ubuntu3`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-8ubuntu3`
- `procps=2:4.0.4-8ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-8ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-8ubuntu3.dsc' procps_4.0.4-8ubuntu3.dsc 2247 SHA512:425e7e66c65cb4d3ee2f2cc2e8482d86ad1aa661b14c6d3b0e03a8b086d288e8840ad40f177d48e73bbeb69b976eb1024dc339c45984526ec70dcd5f426c5120
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-8ubuntu3.debian.tar.xz' procps_4.0.4-8ubuntu3.debian.tar.xz 61416 SHA512:825338b985815a665150682ef2ad378bc0a72a9a3a3f53883469e4591fffb90b275fc2119960b8ae672160f8b2961798e8275b2f3175eec91f70c552e4fb9f7a
```

### `dpkg` source package: `rust-coreutils=0.2.2-0ubuntu2`

Binary Packages:

- `rust-coreutils=0.2.2-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/rust-coreutils/copyright`)

- `Apache-2.0`
- `MIT`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris rust-coreutils=0.2.2-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2-0ubuntu2.dsc' rust-coreutils_0.2.2-0ubuntu2.dsc 8098 SHA512:2d66b7fc43d187ac5ef00cd4d6ebb2a67b86287f0c72a1352a07b8b09a2cf38dbbb0b10be22506a5d049ec8a9974c552b5dd44ab00c50c89f5df7a2415acf1bb
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2.orig-rust-vendor.tar.xz' rust-coreutils_0.2.2.orig-rust-vendor.tar.xz 10803468 SHA512:a9b29f06270f216da761f535f303db4a840535259030695a8bbe7a5269fdab872941785700b22ab21a570b105ad0ade2750015dc1648ca4ec385b9fe4b414c52
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2.orig.tar.gz' rust-coreutils_0.2.2.orig.tar.gz 2827753 SHA512:58def9fe8f01640c6eb7c16cd182061bf62fab22124bdedcb931cdb39b25c2bd3f31523561e321a4822d9e09107dc0c5cc2ddf8e20333138ddaa19d284db609f
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2-0ubuntu2.debian.tar.xz' rust-coreutils_0.2.2-0ubuntu2.debian.tar.xz 17228 SHA512:d72221f314ba0429bec3378489392b42b4d7f91506eca6c8f2d2ffadc06ae45a369a0d4f07ee7c933db7525f1c3e1bf467732927435beca751b7ea1359175ff6
```

### `dpkg` source package: `sed=4.9-2build2`

Binary Packages:

- `sed=4.9-2build2`

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
$ apt-get source -qq --print-uris sed=4.9-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build2.dsc' sed_4.9-2build2.dsc 1963 SHA512:15ff40c4355c858d0d439a8ca519c2faefd2c391683da704172afc98c90be98e79124a85d5474da98716a0cbc4dcaf2d2b72b46635471bd0f582f38381ee9f0c
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build2.debian.tar.xz' sed_4.9-2build2.debian.tar.xz 62932 SHA512:898685b9dc1085482ff3fee15d8d5de9327dff6f130c63e66aee949215c61fe70b1ae91de6c4315a877c7123d24f63502e374bb8abba7947777666666cb8a3d8
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
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.26.dsc' sensible-utils_0.0.26.dsc 1706 SHA512:7597b6d0dc6bfcb3d63a7fa0b1191913ec1bb3c46c9cce8ac7fd1b270a99d237cdfa1452beef92487e4d35e5b6b2ef84758ee0de51fb071ac739e0b9c934ab06
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.26.tar.xz' sensible-utils_0.0.26.tar.xz 76736 SHA512:afc313ac57379987ef61f656386bb9e4ea14746a266584b4e49953449a1d4869d156d79211ab07826b2473c63e4e2903044751f67b905fab61363c6ba3967ec1
```

### `dpkg` source package: `shadow=1:4.17.4-2ubuntu2`

Binary Packages:

- `login.defs=1:4.17.4-2ubuntu2`
- `passwd=1:4.17.4-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.17.4-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4-2ubuntu2.dsc' shadow_4.17.4-2ubuntu2.dsc 2991 SHA512:c4840af9a81707fe496690d4e758226d849514d42e0fa14ff92382bbe811708f4d621584bf7dbbba1e9e0d3bf21350e2bcd7759b97f1e995c754724cbb160c67
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz' shadow_4.17.4.orig.tar.xz 2326584 SHA512:06830f654650312a79ccd6d729a51808b324d594abf1c05d56a2d0880936df292ec5c9fd6c7f4ad59a6d0f2bf5be0af42afe6386c24c2c087fd64fff301bade3
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz.asc' shadow_4.17.4.orig.tar.xz.asc 488 SHA512:24f14397a975e4b09be087705a96544ff8ad76e0aa8c708ed4a53db3a295ad0a33fd0797fc570dcbb2446d4e103a3e43922a93168f65012eba5d3fe31549ebdd
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4-2ubuntu2.debian.tar.xz' shadow_4.17.4-2ubuntu2.debian.tar.xz 181648 SHA512:0b7986cf221df54d692a6baf35504f32f7c510d85294a17340046ede4ab1314c1899a5dc4d38db2efe9ad1f7de029b0d67e9bb44f0212a5c04778e3817a5e5f2
```

### `dpkg` source package: `sqlite3=3.46.1-8`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-8`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.1-8
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-8.dsc' sqlite3_3.46.1-8.dsc 2632 SHA512:645ab3e91282c45ca08fcfbc583708bfbfe362fe7d10a8e32742fc3f7a6d962f7619213f152dd768ca3b1fd8d26f445936c336776c57c33b1f99b52ca7c9b3e1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA512:a5ec0f57d014b2f33d679cfbae0ca1935eb84871376b29216ffcc286a92a363a823ca0ec729a000d702054ee90b2fcc1887c1fb4bebfabcd14894f8ef91b7ad6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA512:47d3c900d95641c89d5d807881e20e97f3b7889cf44c76d48715066ba5c1860defcd17498440d79bcc49b15c2ea28e81ed4b5b159f9e947941e5c1ee27de06ba
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-8.debian.tar.xz' sqlite3_3.46.1-8.debian.tar.xz 35784 SHA512:77d689cf1b072fd2250e4f651ac55ebc36f1b7194149fb70b8595a845bd2d6c0733f0bb74a5bda62ed9f37f8aafebc252a84f157709b6da9c2941c0fdc509ce5
```

### `dpkg` source package: `systemd=257.9-0ubuntu2`

Binary Packages:

- `libsystemd0:amd64=257.9-0ubuntu2`
- `libudev1:amd64=257.9-0ubuntu2`

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
$ apt-get source -qq --print-uris systemd=257.9-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.9-0ubuntu2.dsc' systemd_257.9-0ubuntu2.dsc 8437 SHA512:c5a4b768e4bff2f1604ba074f1bdf9804d964710ef139b12ce9b7a7d4f6fc93a71147d590a36ef25775d8b916bce81ed693b9c7f3a579ad480d9a16d3f0b7a56
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.9.orig.tar.gz' systemd_257.9.orig.tar.gz 16401765 SHA512:23b3d2764e0f990d8373068ccb41177793413bc193f7bd34e38b03d6fc3cd32d07c86e9dcbf07e32904075bb5eeca208f65beab04d628ac0e0b81ba87a975c1b
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.9-0ubuntu2.debian.tar.xz' systemd_257.9-0ubuntu2.debian.tar.xz 248584 SHA512:5ddb5ec3cbe9aae2f5cb9c3bc6316270d5e33b0e0bf5179d0dd0f5d282e6ebd131a18512ca85d6b4e0594c49296a3ddf329ff0da028bdf3860a42fc8b3096319
```

### `dpkg` source package: `sysvinit=3.14-4ubuntu1`

Binary Packages:

- `sysvinit-utils=3.14-4ubuntu1`

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
$ apt-get source -qq --print-uris sysvinit=3.14-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14-4ubuntu1.dsc' sysvinit_3.14-4ubuntu1.dsc 2234 SHA512:be97da93ce36ad3b7711f196ea0ecb2ee3516a655c3dd6644a0bc1dcb8d39d77fe7de6b99e3e40c7c8f7759d6a01325b08d2077e18cb3155b8123c2e24ca2da4
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14.orig.tar.gz' sysvinit_3.14.orig.tar.gz 516357 SHA512:557b6ed9090e6594806b71c9fd054f32972fc6e7bffa4ef92a9dda42c5db08100f226b7b43c0433c1a1e9b16a3ebc483cb42d9aa29a5a3cfd5fc1c60984ef478
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14-4ubuntu1.debian.tar.xz' sysvinit_3.14-4ubuntu1.debian.tar.xz 123480 SHA512:64c33968bbd52ef4841aff5132ba9310fcbfeacbacdf5f502aa1f04ea4fe37f211fde5848ffb6efebee230ca6d9bbc6e66dc0f89b824caec5e7b152f7576a36e
```

### `dpkg` source package: `tar=1.35+dfsg-3.1build1`

Binary Packages:

- `tar=1.35+dfsg-3.1build1`

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
$ apt-get source -qq --print-uris tar=1.35+dfsg-3.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.1build1.dsc' tar_1.35+dfsg-3.1build1.dsc 2041 SHA512:97868dd7876d102bf99bf3b11c3519422c50618e6a7f9d26f8db513be9f49fb9bd141a3fbfc9830d64342021deb9624396b61e09349f552388a5cd3c87d0bc8a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.1build1.debian.tar.xz' tar_1.35+dfsg-3.1build1.debian.tar.xz 21616 SHA512:f43aea413a69b80c84188daf9cc04b353ca52bab147bd82fa345e2dd576604e375f68c8e1d986a12f87a9daf687f933d9e56485a45a87e8f7b7935405e634d0a
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

### `dpkg` source package: `util-linux=2.41.2-4ubuntu1`

Binary Packages:

- `bsdutils=1:2.41.2-4ubuntu1`
- `libblkid1:amd64=2.41.2-4ubuntu1`
- `liblastlog2-2:amd64=2.41.2-4ubuntu1`
- `libmount1:amd64=2.41.2-4ubuntu1`
- `libsmartcols1:amd64=2.41.2-4ubuntu1`
- `libuuid1:amd64=2.41.2-4ubuntu1`
- `login=1:4.16.0-2+really2.41.2-4ubuntu1`
- `mount=2.41.2-4ubuntu1`
- `util-linux=2.41.2-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/liblastlog2-2/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.41.2-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.2-4ubuntu1.dsc' util-linux_2.41.2-4ubuntu1.dsc 5035 SHA512:fcaa69cac04347bb10b0286585f26847812df5e7fe2127edebbc122340ebaf714e7e343e22752460d65e04c6dc06c3469e93dfad77c8f89719f06b5a9811a23e
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.2.orig.tar.xz' util-linux_2.41.2.orig.tar.xz 9612488 SHA512:696c87e7cf185acc9b4b969ddade6155ea2945ae494eaecfd7b1f35d9607166cb09be79878fb793dd31b4d4dcac8c9be4be76af3886185db7ae8b58c303fb0cf
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.2-4ubuntu1.debian.tar.xz' util-linux_2.41.2-4ubuntu1.debian.tar.xz 112548 SHA512:fd0d3e9cd669815e6133849e566a364894210ec1a5c86bf76c89286424e7b3520e3fddc9d68872900ba9b898090e383b88a9beed8008947ebb9c2ee15264f984
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
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA512:c5cc95f63ea3eab2a2459e01d48a50b729b3af63ad0e3121e2b3776b54f1ab097f827a7cfb95b5d13ff4a1465a3d88f8876b6651f825fedf2f481b77b3118639
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA512:8b5c8b9aad4e869f28310b12cc314037feda81d92f26c23eaecdb35dc65042ca2e65f2e9606033e62a31bcc737a9a950500ffcbdb8677d6ab20e820ea14f2b79
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA512:737e2b1da8c6abb1c6bd84de7815513dbcbb72312bab4325003bc6bb91e363a44f862360dfd6b47d7286a6a7b59ba8c6892f9027fcda5924ba3d8d7baaee0d38
```

### `dpkg` source package: `xz-utils=5.8.1-1build2`

Binary Packages:

- `liblzma5:amd64=5.8.1-1build2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu2`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu2.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu2.dsc 3167 SHA512:ff161ae844bd3e2071a129c7406bd85ea2fedfd60230735197c4eb7d7c406222d9d4d5b7dbe26cccf62ee5262b8dec5576052037b75af04012bf865818aa5c19
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu2.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu2.debian.tar.xz 59848 SHA512:72f243e7be9723973af1e98b66b265f37bb11ddeca227f6fd9b0ea298ebd7317a87b52152cbfce45848bc23a8cb450fa2e77a2e305f4b102ae840489a607eaa1
```
