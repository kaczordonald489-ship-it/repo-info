# `buildpack-deps:resolute-scm`

## Docker Metadata

- Image ID: `sha256:9fbaa3ac9fa2a71b15176d870f50c0be8825285f9579026ea346b2f43e805f19`
- Created: `2026-01-15T23:06:30.994337428Z`
- Virtual Size: ~ 281.51 Mb  
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

### `dpkg` source package: `adduser=3.153ubuntu1`

Binary Packages:

- `adduser=3.153ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.153ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.153ubuntu1.dsc' adduser_3.153ubuntu1.dsc 1807 SHA512:29c8a19c57ce30211a3facb7ee7cfe03df68dbb0282fb88cc28aa810ca0d60a2caa08228372e8b72ec54508fc96187bbf9f978f127eded41d94b77d0ec7d084c
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.153ubuntu1.tar.xz' adduser_3.153ubuntu1.tar.xz 339348 SHA512:d01e1aa88a84afb8cf55e5afbe920e00b5ade6456d59d7a16a092027442fc6de2c2200fec8508ebd5fc09241c2b4409fd437e2d92a0689fb1a2ea4038f0d8223
```

### `dpkg` source package: `apr-util=1.6.3-3ubuntu3`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu3.dsc' apr-util_1.6.3-3ubuntu3.dsc 2647 SHA512:3ebd82905a9f82a3ff57b91e22b3423473c656b4e2b375f9633294de9f55128e9464f4c22ba2e31f253604627ca39e43a41362e95ea6c6568b5fcea2511d4554
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA512:8050a481eeda7532ef3751dbd8a5aa6c48354d52904a856ef9709484f4b0cc2e022661c49ddf55ec58253db22708ee0607dfa7705d9270e8fee117ae4f06a0fe
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu3.debian.tar.xz' apr-util_1.6.3-3ubuntu3.debian.tar.xz 342676 SHA512:92724a96f75695a81d68f9cf2a9a10bef86ab62965a6d0fc4af05fe78fd17277ce71c01ab9549632011393786e34430756d4b098ed80f14b39964b825cc904f9
```

### `dpkg` source package: `apr=1.7.6-3`

Binary Packages:

- `libapr1t64:amd64=1.7.6-3`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.6-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6-3.dsc' apr_1.7.6-3.dsc 2402 SHA512:4f8e25a2f05c2c0530e832f12b339ec0e44131f04e0d95008f345eba2bac88201e179a85fde6c2f1f86988fd16b2ded3d92bef4a471ef702ebabe8fa66b28cee
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6.orig.tar.bz2' apr_1.7.6.orig.tar.bz2 899670 SHA512:629b60680d1244641828019db903a1b199e8a19c8f27a5132b93faacb381ce561f88463345ab019258f1f1e8cfdf8aa986ac815153a8e7e04a22b3932f9fedd2
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6.orig.tar.bz2.asc' apr_1.7.6.orig.tar.bz2.asc 898 SHA512:e20000b14e94f164a37c90c122f6e7469f2b26f62792ced4573a0aebc80d0a53d864f14ecf62c6f30531e5ab42b987ce7faffec1d9207acddfaa21378550e282
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6-3.debian.tar.xz' apr_1.7.6-3.debian.tar.xz 42384 SHA512:64ea438a1601a4e0c91c9da54f91e4bf4237d5b7b426c2bddf9a925f8590fe431c3b63c8f7fe4c7724d2c4b65bd54c50c35670467fe5985d8ef971e1b25853d5
```

### `dpkg` source package: `apt=3.1.12`

Binary Packages:

- `apt=3.1.12`
- `libapt-pkg7.0:amd64=3.1.12`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/3.1.12/


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

### `dpkg` source package: `base-files=14ubuntu5`

Binary Packages:

- `base-files=14ubuntu5`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=14ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu5.dsc' base-files_14ubuntu5.dsc 1727 SHA512:cd864000c1c3b385f8c995899be30e64b653c482abcf74da9f52b8b26275c94fcaf082f48faba584a90b28b29fba19f0ac06db506bef264e7e09e99d5875bd86
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu5.tar.xz' base-files_14ubuntu5.tar.xz 97972 SHA512:73bb888d0691426ea5d9637a00ad82c99907485a6db473ef078596c5705f4882d4d19acc85944cf51badea9c6f0713c95dc60040fa6315370e24afbad04f90a1
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
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.8.dsc' base-passwd_3.6.8.dsc 2044 SHA512:cacd3929c178191cacd4b08f810e28a76987938db2efd2c3a9a990ad8400f75f69760c21fc9c6b370bd7f181a678ae52a01817776972475f75b6d855dc72afbc
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.8.tar.xz' base-passwd_3.6.8.tar.xz 61840 SHA512:f8d58fa5fa7c4242793121f43220012b328d55796af69b2def61630de2a180bff3bc72e816a24d4ab96cc3dd98bb677b68f6d00f9ee54568189822959f8a475e
```

### `dpkg` source package: `bash=5.3-1ubuntu1`

Binary Packages:

- `bash=5.3-1ubuntu1`

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
$ apt-get source -qq --print-uris bash=5.3-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3-1ubuntu1.dsc' bash_5.3-1ubuntu1.dsc 2072 SHA512:0e9bf07ed7528c4dc660d44d64942567dd4ea62b05525b78e906a5b2a623051d2c3312c446cd338cda496fb79191bfbe44630d5e9836be2fcefebf4c4028a559
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3.orig.tar.xz' bash_5.3.orig.tar.xz 5571836 SHA512:79a1800b6b579a1cc4247c67fc2aceed9a7197f2ea91a3528365297eee1b20a860af27d6d8cadc3c4a3c91a9f8ac9e04c34d7a5e80b605e1252adffedd26e932
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3-1ubuntu1.debian.tar.xz' bash_5.3-1ubuntu1.debian.tar.xz 96008 SHA512:3621ed62eb49c9ba6415003942805ccbdd6c4a0448d59d6a7b569b9ba1c8446babed51e1484821237ebcae81cf8fefd6e202df7a7eaad14fa1ded11e138d96ff
```

### `dpkg` source package: `brotli=1.1.0-2build6`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build6`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2build6
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build6.dsc' brotli_1.1.0-2build6.dsc 2364 SHA512:98ac8a8db58de8f98e74563b1f9fc7517a6e644c4139d07321a2e3e01b2f46dc1a78633793f8429c1ad86c3505204b58112777ebcebdf8b432e90b520649504b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA512:7a94f8b1ca1d3a411c6b5681bd2ed66183468f7b37a24741601d77ed4353577805de84c810dd26086d4afe6b11bfc4791db3ba7f6f9986bc7acbb8e9b43f488b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build6.debian.tar.xz' brotli_1.1.0-2build6.debian.tar.xz 5844 SHA512:0841453eb7c7dd1e3cd8d2efb758bb5aed170dafc64685be7cb0233352f8e79dee96bc02dcb616c7bdf8b2f37ecbe03f43bf2dfda5d48f1b6c9abbe3acb3fde5
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20250419.dsc' ca-certificates_20250419.dsc 1766 SHA512:a23a4c3bda0d9d16cf5575044d58b5dcee545e164cf455e31522927738dcf62cbccb8ff0520afdd36d53b22cff824388c492bcf85ebf28a9c5a35e8fcdafd745
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20250419.tar.xz' ca-certificates_20250419.tar.xz 277504 SHA512:5a66a4aabbc18bce752b9e2d362309812cb685e24c0bb52cbb04cde3284b023034955c0ba8c9a3fa065392ab8372d166e6cb17b82fb336cb485e2b63485e9631
```

### `dpkg` source package: `cdebconf=0.280ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.280ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.280ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.280ubuntu1.dsc' cdebconf_0.280ubuntu1.dsc 2873 SHA512:bd0f7dd6a9e3b19040f726c966775955569f29c4f63c1a6680549a42f8bd591a93574346f0dba3fd5f46f60b2cbe75d77422fa09e85e908c1ea6a83b390ef1a9
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.280ubuntu1.tar.xz' cdebconf_0.280ubuntu1.tar.xz 287352 SHA512:24bb2f3083730194bf76ecf9039d92429550e5e3f52aa417ae628b9805433b42227e56941671d7c549f86c0302c43c22e3b62b3d01d609b6f79869e3e2ef53d7
```

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


### `dpkg` source package: `curl=8.17.0-1ubuntu1`

Binary Packages:

- `curl=8.17.0-1ubuntu1`
- `libcurl3t64-gnutls:amd64=8.17.0-1ubuntu1`
- `libcurl4t64:amd64=8.17.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

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


### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-9ubuntu1`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-9ubuntu1`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-9ubuntu1`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9ubuntu1.dsc' cyrus-sasl2_2.1.28+dfsg1-9ubuntu1.dsc 3583 SHA512:68941067eed1b29cc03e6d006c93bffc3c22d9e074e78b97dee825b12fef26d52f88c73cf3e52cebefb46942c6151766156f0a9a8c6ad6e654f532fae3808d7e
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9ubuntu1.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-9ubuntu1.debian.tar.xz 99304 SHA512:cf638d3bf7111761818d7abfcbbcd33d5a4214b1a0030b000996052c400d5560690d6b93d0b4502c7bb406d1d83686747600e0a84101ff8bced0740ba8ff3307
```

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

### `dpkg` source package: `db5.3=5.3.28+dfsg2-10ubuntu1`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-10ubuntu1`

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-10ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-10ubuntu1.dsc' db5.3_5.3.28+dfsg2-10ubuntu1.dsc 2484 SHA512:3767fbb8ada0b2aa00a107e6b6f2eb06ec9bf0fbb20f7a22645098ec5f52fae5930e359f119c09116ed6eab2f46734ec80ddbbbdd60cf675bf17ed2116a9d81b
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-10ubuntu1.debian.tar.xz' db5.3_5.3.28+dfsg2-10ubuntu1.debian.tar.xz 36572 SHA512:3c8afc4f013a54d163f90c26ba6a616f4e95ce0f3f40d328d6602498adfa6a691e6a44d2f32f5467712a2ee3566b5315a05f44e68792d9d4d5b835bf810114b9
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12-1.dsc' diffutils_3.12-1.dsc 1875 SHA512:1560e462c0645f104cb7e37e1c6d82d0de0f7cd0a31ea5676d3604dbcdbb4ecd325123057ce96b6da3b7d2218a49fc9392528893321920b81c37f325ed710735
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz' diffutils_3.12.orig.tar.xz 1938800 SHA512:10b17cf1dcdfa9ca0e5db91d62c4a079ebe9fd7eafa3aaebd4eb7e6206e4d753f348496622aa281e1bd7f7fcde65ce4a886dcc4acbb59332ef980f224197b4e4
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz.asc' diffutils_3.12.orig.tar.xz.asc 833 SHA512:8eb59b40156741fbfcac947f29f76aa0eefb9c8f819206cab9474da0ffe0154c6aa8b38435eccdd82ceb8c3565a6c548e8d2a0f771f1e8e1af15635854ec9c62
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12-1.debian.tar.xz' diffutils_3.12-1.debian.tar.xz 14752 SHA512:e2054eac9f98935f28d8335e2d06ac7ee55bf9d1f0ea0d4ff0eed2efe2e2cb2e717d732f04a6197027a8146e78931cc13bbb96dc3223cbdecb4e259549125515
```

### `dpkg` source package: `dpkg=1.22.21ubuntu5`

Binary Packages:

- `dpkg=1.22.21ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `expat=2.7.3-1`

Binary Packages:

- `libexpat1:amd64=2.7.3-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.7.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.3-1.dsc' expat_2.7.3-1.dsc 1964 SHA512:6e1aa9b52d435a30bc0274f89d00418247d352740c3d95b4995a8f6267dd8b05f4f76cb257ad6fb3097806764bb7ef4cedf75447c5c5b54fda976d1abce0fa96
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.3.orig.tar.gz' expat_2.7.3.orig.tar.gz 8441347 SHA512:34400f7dff0151a38c5ff7d73b65b57c7fdf648cf407ed94beddf2d11511b650c4ea16e417a15ebe1707456e7279210e929cc97a0caf7a1ff45bf1d07275e815
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.3-1.debian.tar.xz' expat_2.7.3-1.debian.tar.xz 13480 SHA512:206335f0ff93e361dc6f72f0cac7dc78e7151c669f8b62f24afffe6df3d3cbcccb52b0c8b32f68370890c26d525c21b012a8691fd5e751acd5e0b09cabec832b
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

### `dpkg` source package: `gcc-15=15.2.0-11ubuntu1`

Binary Packages:

- `gcc-15-base:amd64=15.2.0-11ubuntu1`
- `libgcc-s1:amd64=15.2.0-11ubuntu1`
- `libstdc++6:amd64=15.2.0-11ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-15=15.2.0-11ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-11ubuntu1.dsc' gcc-15_15.2.0-11ubuntu1.dsc 52487 SHA512:0827e20f50c9fa9d11f434e2087b1a6806df2df6cd9b1b98b06e1a9d7d16e8c2ca99858418bed67fb1e29c3fa4470c5a5a065f9420b2640376d873d725cb2e16
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0.orig.tar.gz' gcc-15_15.2.0.orig.tar.gz 105962230 SHA512:83887af5c7798105d1ad85f0e9c794daa3cf030638bf40b3bff48771b8325d95c9a0d99d7d2c86c8e45499ff87f975e1914d00b72482862357645cc7ec330d38
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-11ubuntu1.debian.tar.xz' gcc-15_15.2.0-11ubuntu1.debian.tar.xz 2825792 SHA512:f4573538a8a3a960025fd4181a622767cb596aad6b94f3b1e7e93d8beb1fb47d60e58aec1cc5cb1bfc178dba3b752e55bb32e06af381a9bba4cfb31356dd2c21
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
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26-1.dsc' gdbm_1.26-1.dsc 2234 SHA512:b323eaf698fd6ef3749ff671725565ae8f49f9fdcadeac003700c3a5dcaee9c6efdd4e2af75ba42c51d429c2e1c356afb62e59484889ae8ccb4b5df5d694ee83
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26.orig.tar.gz' gdbm_1.26.orig.tar.gz 1226591 SHA512:44aafe254f0950a8f5215d8f1337674f07b19f2a375f6eb19a7e39690028c80c3774b705c2b76b470ae74042b21f2ca77d02f6f57aa2ee50296db801220a3352
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26-1.debian.tar.xz' gdbm_1.26-1.debian.tar.xz 16832 SHA512:192efb75c21e1035ad5427375422385fc4534163bda7d11653d65a42429d8e39043ed3b76300e6b2d20abe8eb86fc4ac866a00626b198afe50dc47d3f48d5285
```

### `dpkg` source package: `git=1:2.51.0-1ubuntu1`

Binary Packages:

- `git=1:2.51.0-1ubuntu1`
- `git-man=1:2.51.0-1ubuntu1`

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
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.51.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0-1ubuntu1.dsc' git_2.51.0-1ubuntu1.dsc 2656 SHA512:995c8ac6af4331625936708fb1f4309bf7349dfc8b5037566c6a54238131a95c52dc7518ac6c4628a1ad8dbeb078b4bb9e8c5c3585afbb6a37dc6eea9f89acfe
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0.orig.tar.xz' git_2.51.0.orig.tar.xz 7857228 SHA512:2b8c59589266c0c9e58a9f4fda4a970a8a492e2e0ecbafc414fcfacac4a04251f0115b3676f4599a415b53906f1dea312b18a42e9bde455286abd62ec327beaf
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0-1ubuntu1.debian.tar.xz' git_2.51.0-1ubuntu1.debian.tar.xz 821848 SHA512:e5f8451664c213ba067010d0fca4121da7a813be833fdc0606fc99306c4aade63784db63162f5bd167312d247778a4393a24a82cd850fd93b18ecade75382511
```

### `dpkg` source package: `glibc=2.42-2ubuntu2`

Binary Packages:

- `libc-bin=2.42-2ubuntu2`
- `libc-gconv-modules-extra:amd64=2.42-2ubuntu2`
- `libc6:amd64=2.42-2ubuntu2`

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

### `dpkg` source package: `gnupg2=2.4.8-4ubuntu1`

Binary Packages:

- `dirmngr=2.4.8-4ubuntu1`
- `gnupg=2.4.8-4ubuntu1`
- `gpg=2.4.8-4ubuntu1`
- `gpg-agent=2.4.8-4ubuntu1`
- `gpgconf=2.4.8-4ubuntu1`
- `gpgsm=2.4.8-4ubuntu1`
- `gpgv=2.4.8-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

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


### `dpkg` source package: `gnutls28=3.8.10-3ubuntu1`

Binary Packages:

- `libgnutls30t64:amd64=3.8.10-3ubuntu1`

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
$ apt-get source -qq --print-uris gnutls28=3.8.10-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10-3ubuntu1.dsc' gnutls28_3.8.10-3ubuntu1.dsc 3356 SHA512:7348f62fd6d994dd015c823a05f15a5672fec80c42865c19eb4e97ea243eefc0b66d5d0b5f43661c815cb84fb645dd8e131516761639cd6fed6276ce0f9d3343
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10.orig.tar.xz' gnutls28_3.8.10.orig.tar.xz 6909856 SHA512:d453bd4527af95cb3905ce8753ceafd969e3f442ad1d148544a233ebf13285b999930553a805a0511293cc25390bb6a040260df5544a7c55019640f920ad3d92
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10.orig.tar.xz.asc' gnutls28_3.8.10.orig.tar.xz.asc 833 SHA512:8f79f17db7c1d38f2e96daeb8fc709faa34216e56fcc7f724b875692437126ecbc91544bf53f16f6e9f65ad64436cc61ba4c1c4aed057a0acc373be102fd5945
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10-3ubuntu1.debian.tar.xz' gnutls28_3.8.10-3ubuntu1.debian.tar.xz 177332 SHA512:4ebe267faa0e30cbec597ae38953d82516e6ab428f9990bb97e0a5728048a721501fd2ec93162d7a37d49a835df61d4f326f196b463c611f150fc8a43a5355e3
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

### `dpkg` source package: `hostname=3.25build1`

Binary Packages:

- `hostname=3.25build1`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25build1
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25build1.dsc' hostname_3.25build1.dsc 1543 SHA512:f9f180a2b477d4e3d5e08714d8978c961558f289086a0f221d0483d223fc9201512ba554c5e356102c438216ffaadcda6d21e9db9e644dce41652388878c454e
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25build1.tar.xz' hostname_3.25build1.tar.xz 12896 SHA512:b99c6e870198c1be17e5a4e68cecfe40e1f28b1e43595ab960c79afdd94877f0e34903dbb33d845060fa76e9ed64298c250bd27a03446ba6e0b61d135ed97e11
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
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.69.dsc' init-system-helpers_1.69.dsc 2234 SHA512:f8055fa3cf3eaefff9178c737845464de128a3f4682c421c5a65b6e2a45d615e166bfbdb4326dedc98ea2426f243b1b24b51f59d0bf78b968b1558b44b90ccd5
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.69.tar.xz' init-system-helpers_1.69.tar.xz 45648 SHA512:3b08b93194523af989177616a5e8cfa1ffa9ba31650a09325a98e704f7e4e8291febcaeea8e66e32784ce45e286d136091d3d83a8416859368ae59b8897f3d9d
```

### `dpkg` source package: `keyutils=1.6.3-6ubuntu2`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-6ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-6ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-6ubuntu2.dsc' keyutils_1.6.3-6ubuntu2.dsc 2186 SHA512:d99a25727a1cc335e6556b211484947dea99f5beb56bb1b3ab131b0dee231e4953a32178c9ec6f169171a9acb13848437e2adef9291636615c1eea462f2ec628
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-6ubuntu2.debian.tar.xz' keyutils_1.6.3-6ubuntu2.debian.tar.xz 17508 SHA512:40c3260e3d6c7d8c2b81b723e22dac20495d16cc5ff3159f1897f85c82c14c1e88fc0161b109ce83baa779bdd75adf6c3f833639d86ce0701e9d99c25ea65e7d
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
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1-2.dsc' krb5_1.22.1-2.dsc 3378 SHA512:41e045d9b0ef3d793c32c26c2b4995a197e9dfd6e820e6d9c7edd85f102f9ea825f7af9ff3f69acfa830a9ea91a090055f90d8126c135772f53d83f8bb855bc1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz' krb5_1.22.1.orig.tar.gz 8747101 SHA512:c33bfada5e0c035133436031d9818ad97b0ff08578691c832b743c55751a2cf9460501d3cc658ab79655ed7a0f9f4795ba94b363d6b616795d9bdca668825c52
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz.asc' krb5_1.22.1.orig.tar.gz.asc 833 SHA512:83354b1e4f71cfb52ba8b921740c5abd4941563f4f8ed880f1feacb173aec2d1b6efbe94d21b062418a73b47d81e2e734fdd47805a07278dbc4945975b9f1267
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1-2.debian.tar.xz' krb5_1.22.1-2.debian.tar.xz 102864 SHA512:e345b670cb39866f7f7d3ba2495b28fd0470795feb5405a4ce781971beccfb94fb739d9e93ac716b086ea6c01dae96c9dc7091f60511f7d756d0c785f9436ee3
```

### `dpkg` source package: `libassuan=3.0.2-2build1`

Binary Packages:

- `libassuan9:amd64=3.0.2-2build1`

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
$ apt-get source -qq --print-uris libassuan=3.0.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2build1.dsc' libassuan_3.0.2-2build1.dsc 2705 SHA512:7efac2cb818028a1f44fa6239fcae17774bf52a772518cdb936e780491e1c63e99a8c684051a71673d7f4e040fe24ea945903f7621d9a5a40e543b57de9560b8
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2' libassuan_3.0.2.orig.tar.bz2 593917 SHA512:a591eda350ecbf4fe8568b5087f69830df31f36ec67e2a50672aacea9bee16020f374a0bface459aeac1897c048072415ab5962a97034ce6fa413100b2a427fb
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2.asc' libassuan_3.0.2.orig.tar.bz2.asc 228 SHA512:56e0a8288e498bbba504fdaa84060ef6dd30c72efd691d6d0e39069113a394f2da407d83adfd14f7ae25b8e8531f8e9dee859b52471261653dc2ed5f44ef22dc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2build1.debian.tar.xz' libassuan_3.0.2-2build1.debian.tar.xz 17596 SHA512:b4fc08de67862598c8440001b427ef8ce30e9bfcd15d91788ba8dc962a87711b36cd25006feda8a32121a43da385d3df5a4b19b0c4bc96799446403aeb2b0dcb
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap2=1:2.75-10ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.75-10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.75-10ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-10ubuntu1.dsc' libcap2_2.75-10ubuntu1.dsc 2789 SHA512:6585867897ab6b136b319376f7269ea1a0d04c46b865a633515ef34c3326f6683d0830d0c7c60201161dd2dab2300ab91fbb21636e5bb235f144109efdb502d9
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA512:229e9b62a1d54024107cbf321fffcb152c0071154554a3fcee6e09e19cc47fd1fd862575135a4fc589b79a043f760bf40d26ea9fd58638f26e809533c017d65f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA512:6a6af52ef3a48356d8c205827aa039ed852ec4a1cfea44f00613457380478ebd4946caf933a8ebdf98899b14340b9a7ef9b7151c4659329e2fd80590667d59d9
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-10ubuntu1.debian.tar.xz' libcap2_2.75-10ubuntu1.debian.tar.xz 23640 SHA512:deddc0d08ad985e22cbefa63f65c8c29731af8eb9d5c7d34a4597d2609fe29900b4354337c8ef7ce5a99c808c481d46572136448268742bdc3505e0bb1ba75cb
```

### `dpkg` source package: `libcbor=0.10.2-2ubuntu2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu2.dsc' libcbor_0.10.2-2ubuntu2.dsc 2238 SHA512:13dfefa6219a21743816cdff9a1fff1ef7c41ef70f276c6759090dd82a5972cb5bd9b2d84f3a5a045b2ff727aa5a8404981f3e3d67123f48e290ecf641bdeae6
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA512:23c6177443778d4b4833ec7ed0d0e639a0d4863372e3a38d772fdce2673eae6d5cb2a31a2a021d1a699082ea53494977c907fd0e94149b97cb23a4b6d039228a
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu2.debian.tar.xz' libcbor_0.10.2-2ubuntu2.debian.tar.xz 7392 SHA512:cb259804ef47078f998955a3534148fe7c96aea3f619a999e7c4d479b837b50138899abb8a22db6e5ef70b5acbd8b0aae6aa010cab8751e6c6f4b8da50dcacab
```

### `dpkg` source package: `libedit=3.1-20251016-1`

Binary Packages:

- `libedit2:amd64=3.1-20251016-1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20251016-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20251016-1.dsc' libedit_3.1-20251016-1.dsc 2264 SHA512:6bcd222ac7cf37173bbe651d17d87d47cc48c26c6ed25de85ff34dc7324221c83ceb1fdc4289c91c75bd3589907c3ad4722487b6624b95774f3012d986fe1cff
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20251016.orig.tar.gz' libedit_3.1-20251016.orig.tar.gz 549005 SHA512:a084895f92d7b373eb5aff7d4497d395fb141343fdce86de5387fedd5f77b0695ea68f061e461e35d248e66cf4cc0c62a364309f908a42db27e4fa70b530e2cf
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20251016-1.debian.tar.xz' libedit_3.1-20251016-1.debian.tar.xz 16716 SHA512:8248a63a1f95b382ad2f436e24b18ab048b47db357043303c772f7f9a8e4e99ac333c8504d1b96dc84df1c28740d6ec559b1b93385df1995d374ea4964aedeae
```

### `dpkg` source package: `liberror-perl=0.17030-1`

Binary Packages:

- `liberror-perl=0.17030-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17030-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.dsc' liberror-perl_0.17030-1.dsc 2337 SHA512:1c039478eb6721fb61ac62f0daedf0e32e935f40625564a1dbc6f240776bb9bfaa05a2f0176296f08fcf939e7d967fd31274aca9d7522b05809bd32c97e511ec
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030.orig.tar.gz' liberror-perl_0.17030.orig.tar.gz 33488 SHA512:842e33fbc2f2bd6eaf03459263070311fde9ae06105438baf8920826ca26d3f46c18d0d49bfe85a3eb25dfe94e671db0e7d1f30a143b8d82bea47410bfbf7f01
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.debian.tar.xz' liberror-perl_0.17030-1.debian.tar.xz 4660 SHA512:7a7d03e838840c466c34bcea97b43a1cc12f4baa87ed260164a04c01ca2aeec50286104b98ac074e5af44e8e68fac36823ba0ad04729fb2d8046487b42a2553b
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
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-3.dsc' libffi_3.5.2-3.dsc 1954 SHA512:52348c55c957433105c47137fab4d787071580bea2199949b5982be59ba46d81fd43639e23e906bbe362706371e6bae8fe5cd08a6f68a6bc8f2fe2e611bae91a
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2.orig.tar.gz' libffi_3.5.2.orig.tar.gz 598870 SHA512:4579932becbe33b2cb3c7a6327a9b47fee67f225ebb4677870ed4402bb7c186966a5b8645dc8a09128af51dcba27c23537e6a34567dbea4e3dc3728cfb51e038
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-3.debian.tar.xz' libffi_3.5.2-3.debian.tar.xz 10928 SHA512:ee5ecb07a2b656c2c269a2e906792e2eac86cb167e2be9012a4bada201b47072fa5bfe4e55769927e2490b7b7859e821712b4a15ab0af8a73e1faaa7d23943dd
```

### `dpkg` source package: `libfido2=1.16.0-2`

Binary Packages:

- `libfido2-1:amd64=1.16.0-2`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.16.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0-2.dsc' libfido2_1.16.0-2.dsc 2490 SHA512:d588b4d1bc4c9a2495626b2cfeb6d2e8d79c610686663c510538dfd0faf5172637e3a44fe2d2fae59d9034ba517b00f382454c7a4c73d5b16e8b9bcd645dc2ab
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0.orig.tar.xz' libfido2_1.16.0.orig.tar.xz 599884 SHA512:f85b5f8bb8c85a4371035f2875eb70f0e8dc8450279020d853cc19e200e4e68bddf93829b7c7675ac078e3b04c267e8cc6fb044302b9080913e2ba89e877cc38
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0-2.debian.tar.xz' libfido2_1.16.0-2.debian.tar.xz 65832 SHA512:26d499b0b4113d0ebf103b672aed3420f841f67f8c9fff714482a1f3655fe357c08f8668f03b27587d10d10d321970894fdda2ba21517eedd47cd916248007b3
```

### `dpkg` source package: `libgcrypt20=1.11.2-3`

Binary Packages:

- `libgcrypt20:amd64=1.11.2-3`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2-3.dsc' libgcrypt20_1.11.2-3.dsc 2945 SHA512:a68caae63f6f21910bf0794ea9826930bc4e712e53669a2e670b8b2fb05e4ee13cacf9d3a46b15bcd730f636bc89bd65c00547f34dfce1e61aae64349eb4c410
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2.orig.tar.bz2' libgcrypt20_1.11.2.orig.tar.bz2 4237802 SHA512:b706cea602cc8f0896e57ce979643bf78974b05faec27c1b053b773c57d8b04250e30e95a4ef5899e1df981d01d8d08f0a36e10b5820a5ec4183e74c02e5f1f0
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2.orig.tar.bz2.asc' libgcrypt20_1.11.2.orig.tar.bz2.asc 265 SHA512:236edbd12f904a75497eba1b04fd79826a9553406a4301f90e91c5598d4b6ae9f20b894027ae8f5e821d776fbaef3c8203b9ee6e077e5659782ce750aecd5e57
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2-3.debian.tar.xz' libgcrypt20_1.11.2-3.debian.tar.xz 43012 SHA512:bf95402293c26873a8a29996b66d16e657c322073b54ad3e72a4eb1b69807e1fdf2b48b296b4427191a4466d06afdcc6e60c1c292c83a93fca42380beba7f474
```

### `dpkg` source package: `libgpg-error=1.58-1`

Binary Packages:

- `libgpg-error0:amd64=1.58-1`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgpg-error/1.58-1/


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
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-4.dsc' libidn2_2.3.8-4.dsc 2811 SHA512:0bf433efbaf75dadf72ba6c13d914f45cdd8b6c0c82432c1a1b7265b37488ccbdaa3799995d57a6c5afdfa1cfa233ed88a4c14f5e807d3a8d43fc7b0d374f7d8
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA512:e3f4ec5113f531d2b1827a11d7292318fdc49032c013b0076911b075b0e879428db9b45fe137aa37bf9c60e672b6883c035f9f45b2b42625031534965d518bc1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA512:f5c7f1676018b1cd362e250dd8ad59150c34b11ede9a21dbaf6f2e88fa943c881db6e59bf3e9180567379173cb21c4c893d835db99f4ed9e94bd80f84fb8ee2c
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-4.debian.tar.xz' libidn2_2.3.8-4.debian.tar.xz 18116 SHA512:af9e4879f9d3ee6e0c215a2860f5b18907641cc7f33fc0b00b17521ec8fa65ea9d18bfd945311b37d5fe5acb853a600f277af3cacc1f8d592fd607a36a0d5cd3
```

### `dpkg` source package: `libksba=1.6.7-2build1`

Binary Packages:

- `libksba8:amd64=1.6.7-2build1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.7-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2build1.dsc' libksba_1.6.7-2build1.dsc 2506 SHA512:46a2817fba077f8e55afa5f251b64f46c63a5afa8638eaf1481ca2456a93f83c6117d26d74a634b3b9e29de07f252eac9b7deb839f67dc6770524b2a3a3a249b
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA512:60cb9df9f502ca479818f45b78c4bc2b78f6f359be2b8da489ea98f8896a43ab2c20cf97526b79a3220fb32f1701e62a6481fe61e91e567186ecf4f33d8e64d3
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA512:66208b8e4fe76a753943f13a0e65b765eb496013f7f9aeb0b66a454dfb8c67794d1b70841a4014ef0c7ac4642d7b56c38b35cb34be9d8ee8ea6820cc13db53aa
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2build1.debian.tar.xz' libksba_1.6.7-2build1.debian.tar.xz 14928 SHA512:dc92b03ca9390333cb728f8b2f82c1916d57645f49cec39104c99013df57cdcdb57956bb26c35a9925ae49ac0170b8c6b43004694b6c99bc459cbb73f1c932c5
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

### `dpkg` source package: `libpsl=0.21.2-1.1build2`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1build2`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build2.dsc' libpsl_0.21.2-1.1build2.dsc 2388 SHA512:9736ca1e4a00bbb2ce19eaf7a7e04e98fb5dfcc51f8ecfc2ce0eb6785708f34aabfea67ee63f01a4af5eca9d17b4941b16a0a803f2b79021f2d87fb8895e97b8
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build2.debian.tar.xz' libpsl_0.21.2-1.1build2.debian.tar.xz 12292 SHA512:7b9235d134029f52920c657e163738c1dd319ea5e9862a3d3e8f7619a6d6b72c23ba0130a454201a52ed943b117d6be770ac2ab11cae59d6679a7da01872398f
```

### `dpkg` source package: `libseccomp=2.6.0-2ubuntu3`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.8.1-1build2`

Binary Packages:

- `libselinux1:amd64=3.8.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsemanage=3.8.1-1build1`

Binary Packages:

- `libsemanage-common=3.8.1-1build1`
- `libsemanage2:amd64=3.8.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `libssh2=1.11.1-1build1`

Binary Packages:

- `libssh2-1t64:amd64=1.11.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1build1.dsc' libssh2_1.11.1-1build1.dsc 2343 SHA512:b8255d13b5f547f6ea8d438b7a147c88467decfd2f08b432bfde885f3e03a294c8471b38c62bb17985706a8fa67a29208d5432189ad1c8f655089df9662ebdd1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA512:8703636fc28f0b12c8171712f3d605e0466a5bb9ba06e136c3203548fc3408ab07defd71dc801d7009a337e1e02fd60e8933a2a526d5ef0ce53153058d201233
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA512:83e600ddd676013932297c4f3d2cf2e65b5308f7700d818b34f30d760c7495180e6d8dae70579c8bea95ea2d7ccb12fc42641e545e11ec4b6630a0e6b350b282
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1build1.debian.tar.xz' libssh2_1.11.1-1build1.debian.tar.xz 17220 SHA512:a294d9e0354ddeff5656511853924f785d98eb9052f7a9c8c550f3e3b14cfde1a9bd38c2ed299472b67df54a49171793657fa836e084df2f4539ddfe08b5058e
```

### `dpkg` source package: `libtasn1-6=4.20.0-2ubuntu1`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libtext-charwidth-perl=0.04-11build4`

Binary Packages:

- `libtext-charwidth-perl:amd64=0.04-11build4`

Licenses: (parsed from: `/usr/share/doc/libtext-charwidth-perl/copyright`)

- `Artistic`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-charwidth-perl=0.04-11build4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11build4.dsc' libtext-charwidth-perl_0.04-11build4.dsc 2265 SHA512:0fe85b9e64a3837989d81ace4214eb550cb80d6a7895f572c8e043021bca9f44cc43c32965ed66bf018dbb034aa0cc7ac2800e9782a9b64ce4c3589e1db1ac9f
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04.orig.tar.bz2' libtext-charwidth-perl_0.04.orig.tar.bz2 8327 SHA512:37e47e23557a14fac3d1471017a2a9b637fa2c8a0b11d3feedfa40a2f2fdf48dbb7f1d9d855f5e56733e3da09436fd7e73360b105aa24194f31aabd8e87dddb4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11build4.debian.tar.xz' libtext-charwidth-perl_0.04-11build4.debian.tar.xz 3228 SHA512:cc89f58b8bc90cada87a10519f99aa344436eaa631b2fe5f09b817c9df8bf1ee761c35096d88329b9e4c52b8fd091ac68bbac258d86d4bd0a0a653f7b39b52ef
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
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.dsc' libtext-wrapi18n-perl_0.06-10.dsc 1829 SHA512:77c1d3d64cd6e31939367f8a5d5d8d5d1b0c4d3a9b2fd8edaf834b687ba9f212b6f33bfd708bb5983a51c7eb2f8e9058a26e3416526d681e6a9d87006399aa60
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06.orig.tar.gz' libtext-wrapi18n-perl_0.06.orig.tar.gz 3797 SHA512:08b26bae38eea906ced417f88b494862e5485fe8d8ddf8bc69582b57d3d427393ba6bec9320e79541ccd7d63b20c6c7e5194ccd649cf79ef7caf9892c757ad96
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.debian.tar.xz' libtext-wrapi18n-perl_0.06-10.debian.tar.xz 3452 SHA512:490da004cdfe1b1ff967deef2846de80e8868b8aa0faef501097509c5d0bf8c814defb3d760be9ffae782e8fe3f4a5640ddfe222e59ab733aec4bc3b9d15ced7
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
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2.dsc' libunistring_1.3-2.dsc 2215 SHA512:b5f352f94a03ff54581afe4cd88b1e5ffac6ae7fd45c95bc55f2cc3de24090a0c18d948a43405443388d42e537488c36d4638e33b81061f45f5c591d472148f9
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA512:864d42b1d4ae4941fe5c8327d6726ab8e3a35d2d5f9d25ce4859a72ab2f549a7b68f58638cf8767d863f58161d1a4053495d185860964a942d6750e42facf931
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA512:829229528acc8f9d13de4c43fea6caddacaf1f1cc201a7927b2c140d7ac5a81e213a1a20ba67766d6867fbe301ddddf78685f5af54e67906160807d6e8028b5a
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2.debian.tar.xz' libunistring_1.3-2.debian.tar.xz 28480 SHA512:31079e73da30c7e0eab7bf1fa81936d2655df6f7d216fdfae418c54b8c168828d467af9cde17c2f9102a4479260c74a63cb50701ede8652097efbe47eb6086e5
```

### `dpkg` source package: `libxcrypt=1:4.5.1-1`

Binary Packages:

- `libcrypt1:amd64=1:4.5.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.5.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.dsc' libxcrypt_4.5.1-1.dsc 2434 SHA512:3564b82caebdf85b4a85384ea44e532578e9a6f22f36b92bd048483f489226a1ea3587a10e0703ae206898c886fa6040c73a1fb6e1e4c864afd6442573020f2c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.5.1.orig.tar.xz' libxcrypt_4.5.1.orig.tar.xz 433264 SHA512:857e42b9680dbeb09d80316446738704d841ced7e0d1ae2148edb45bd1996fcc646e59ac26ec2dd79e9d765f5c151b89f970fd7d9ad4415223e022c3d5f384aa
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.debian.tar.xz' libxcrypt_4.5.1-1.debian.tar.xz 8684 SHA512:b3a5a0ecc7594f403975cd0c04648c0fc59c0418f4ce35eceff765d49fffd1f9ff49d97dd48a107e5db646bf388827e6beeb5eef234c9a1853ad7cec0580e969
```

### `dpkg` source package: `libzstd=1.5.7+dfsg-2`

Binary Packages:

- `libzstd1:amd64=1.5.7+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-2.dsc' libzstd_1.5.7+dfsg-2.dsc 2458 SHA512:9e8567d49a85a16c324336e081b88fb0053d0898f119b15e740fec0ee278ce4d4ca8fa01fd187fbbbaf3ea41eb0dc893d02a7ffe0813c2b8132d4c4d9d7d2370
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA512:74604a877f899df6a47e88b895334c0fe35af9d096d472f535e772b156bf61e5529833173ea766dbf5e58fc20ce40a2e47ff1cbed8ff7f2bbd506c6634ae5145
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-2.debian.tar.xz' libzstd_1.5.7+dfsg-2.debian.tar.xz 23020 SHA512:f736d759e541ea23d243d1b9e7bb3bd99b93ce433ba3ac4aa12707a30e82e937b38cd331753756d01876b2e59388fc6b4dc2200145a6cd748ee8667e00c37729
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
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-6.dsc' lz4_1.10.0-6.dsc 1941 SHA512:39bbc7ecc070543781a46a8a1dd8fce7d2f1458aad8b01d391dff05f1047686053196a4079427b5d647f18a436032900fcdf4f981b32aa1793c8f23f2e8303d8
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA512:8c4ceb217e6dc8e7e0beba99adc736aca8963867bcf9f970d621978ba11ce92855912f8b66138037a1d2ae171e8e17beb7be99281fea840106aa60373c455b28
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-6.debian.tar.xz' lz4_1.10.0-6.debian.tar.xz 9236 SHA512:ba2bac25a9bdb688132e28eed6712de0c087f2f031c6a8b72fb3a6d0b1e8a7e0052e861d5fe4506109ab5ff536c9a3d3f7d00a152253e81c937d433cfe2ad11d
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
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131-2.dsc' mawk_1.3.4.20250131-2.dsc 2969 SHA512:4902410b6ea68da87eca7ea33070ea00178c562d507bab694646cd44a81a0474c10b4cd2db4e827aa39aa4d1e435f4074fed0b162d0d6942630773f20f026fde
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz' mawk_1.3.4.20250131.orig.tar.gz 433213 SHA512:100b1f5ee190d2841d5dee449c53601a6d32453e47b232de919f3489f6f7040d0c6d21f6c7d30df616b04abde2db9799c5eb16570c1f88dbc10fcd75c5838042
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz.asc' mawk_1.3.4.20250131.orig.tar.gz.asc 729 SHA512:0d8ac93bdafcd8915b0d2d2b675f8d5cf2aeba655cd04af4b4037336b74b320e02db360b7d18b796aedc09fbabc8a42e471766ea24219bad7a1cbff4f7679552
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131-2.debian.tar.xz' mawk_1.3.4.20250131-2.debian.tar.xz 16120 SHA512:5f6b1f21dfce422c8cef9f8c7609deb2f07d9d9484c0df0400c074193688deef26dca809ddd493f8d12c8c5417839274d81a8ab4b88fb1d5c8f3eeb53858027e
```

### `dpkg` source package: `media-types=14.0.0build1`

Binary Packages:

- `media-types=14.0.0build1`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=14.0.0build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_14.0.0build1.dsc' media-types_14.0.0build1.dsc 1671 SHA512:fda7b5f6767b4628e94319e891b6e8110572ac12b8d10f30a7aabaad1abddba4e468dc8830365b0058c9a44fb5917f5c8fc80eca4df9c13f445ec5ffbb999e29
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_14.0.0build1.tar.xz' media-types_14.0.0build1.tar.xz 65280 SHA512:a4362a1aa1c07f9d3f514a8d5138de4d82cc4172fcad13ecb691a1ba38dbeaec9389838207f3ef80ded8346e4fccae31e0034e0613e6f81e9bbe1a5ae7faee04
```

### `dpkg` source package: `mercurial=7.1.1-1ubuntu1`

Binary Packages:

- `mercurial=7.1.1-1ubuntu1`
- `mercurial-common=7.1.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=7.1.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.1.1-1ubuntu1.dsc' mercurial_7.1.1-1ubuntu1.dsc 2955 SHA512:9fb96cdeab3dff56d53ddfd1fb90f5922c1eb0bbbe19e799b46028bf970caff999cacc2b3ab06b0c3d4b90e28a4169f17bfca9559f7f2b511d423920c01c213d
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.1.1.orig.tar.gz' mercurial_7.1.1.orig.tar.gz 9029304 SHA512:04ba564bbe664a825caa8740ab66ef973acb7795abea1786fdd0c502da7dfe14071b215c6384ac398d0f7b69d86d6da6f9a4dd7dfc9e7123b975ec1656c95092
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.1.1.orig.tar.gz.asc' mercurial_7.1.1.orig.tar.gz.asc 659 SHA512:d0965036a0a034f3067fc875f4c493c4a9528efbc7aa906b512251bbd9e467ee75399aca10ab8885ba90067d905cb1d3b7b6834462f2fd7f70d0907a31571b88
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.1.1-1ubuntu1.debian.tar.xz' mercurial_7.1.1-1ubuntu1.debian.tar.xz 54968 SHA512:8769bbd0ac192ea39edd8d8bedc1d5712e795744ba639abd10edd2eb1898ca787f3ee8c995fcce0fe4a131cd2dcc867e5ee745e0b3b7bb7f71bfcbed1b6227b8
```

### `dpkg` source package: `ncurses=6.6+20251231-1`

Binary Packages:

- `libncursesw6:amd64=6.6+20251231-1`
- `libtinfo6:amd64=6.6+20251231-1`
- `ncurses-base=6.6+20251231-1`
- `ncurses-bin=6.6+20251231-1`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.6+20251231-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.dsc' ncurses_6.6+20251231-1.dsc 4163 SHA512:2dbb2716c022c91ae15c1de5aa31844ee39d34c9e0e61f54365adb53c818d217eb8425e485b45c6b0de3541f8090974f77bc6bd41fd129ae9def1e8906154499
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz' ncurses_6.6+20251231.orig.tar.gz 3789898 SHA512:bb95db59e1a4ea5371efe77806af601460a9a4447fb5c98931d2e911aa5b1b760f1627c2ff8377d13128db5f11b1c20db89c52c5c4584adeed5622e909eef16f
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz.asc' ncurses_6.6+20251231.orig.tar.gz.asc 729 SHA512:3228642bd563bad6b920e883921e61dab4e42b3a53c8dc02112726fd63964484aff3b13ec666b4f253bc58edb666a8aa4fca8bafc23db0e6405c8f6a07a662fd
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.debian.tar.xz' ncurses_6.6+20251231-1.debian.tar.xz 50852 SHA512:fd0acff5a48336ba877a3bf2122eb889461fca98e2eae0ead561c027f442e6984852a1c3414f8439fbcb414f75f83ae20468f5196eeaa51d335065173c2bbbf8
```

### `dpkg` source package: `netbase=6.5`

Binary Packages:

- `netbase=6.5`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.5
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5.dsc' netbase_6.5.dsc 899 SHA512:1092aa10f8b59cbd88bd382fcd3042fdc1b1344af98de75b7cf2cfdaa005e164fcea2ea604652936dfdaeb0d79430b083782794a0f79d1cab5dec615e7acda26
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5.tar.xz' netbase_6.5.tar.xz 32544 SHA512:d64a5dc98bfa3ecef65cb061888fb8a948e853692fd56b523409304df9b5426369ec3c9b61731cacaadab5876ec24bb63631fece935641b533a8763792311fb3
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
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2-1.dsc' nettle_3.10.2-1.dsc 2297 SHA512:2429234b8b6d02c98245acb4ff246213e77682d2618c45436fd44ffd2e7dd1052e07a0d92bf3143c2cd36bf8f846d3ef65c10f834f1914f93da66149d5c6ce4b
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz' nettle_3.10.2.orig.tar.gz 2644644 SHA512:bf37ddd7dca8e78488da2a5286dcf16761d527d620572b42f2ad27bb8ee8c12999d92b0272e06f53766e7155a3f4a1ab7ad9c4b1c3caec47c031878b6b1772fb
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz.asc' nettle_3.10.2.orig.tar.gz.asc 573 SHA512:a998bb2e565ef4e36d8783cb78d5cb74dc3cd499d7706f381a75210194bff93e9ccd9102f6f6eca5a061e1172aaf9970c9ea109670027fbda23f299e78ba6c55
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2-1.debian.tar.xz' nettle_3.10.2-1.debian.tar.xz 25052 SHA512:45739e3af9c2ec00a1f7b9c0998e87bcf0a0803dd1aa52c6eae1a536e637435800aafee5aed570c7b8e9515d2838a445f74c0e648a944417de9298561c90bdd6
```

### `dpkg` source package: `nghttp2=1.64.0-1.1ubuntu1`

Binary Packages:

- `libnghttp2-14:amd64=1.64.0-1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.1ubuntu1.dsc' nghttp2_1.64.0-1.1ubuntu1.dsc 2621 SHA512:df8b8b22477a0c2a8a27614a273e501408e783274756b2bb52b371969a7c7b43424cfbe773b07b347c79096f4139ae4ab76150951b704ffaa47a61dacf05374c
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA512:35f8230a0fa2825f0bc400d4852d8e8b484f659c67b00639ccd074a0029088f016e967db2f62b6b64af1f8ef684f5809a833e7f922e38b9405f7cc7756bcfb75
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.1ubuntu1.debian.tar.xz' nghttp2_1.64.0-1.1ubuntu1.debian.tar.xz 39888 SHA512:e8cf5296fa68a6ec676401bb6b861f1f4ae63a7c370b11c85a268966a24f614791a1092d2723256fd93c7dfdb05f8463d1b6e572325169268e19c56f7add6192
```

### `dpkg` source package: `npth=1.8-3`

Binary Packages:

- `libnpth0t64:amd64=1.8-3`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.8-3
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-3.dsc' npth_1.8-3.dsc 2188 SHA512:8421638b6566673ba904e22d04efe1b6b9da3acf7a1481e5dd9d5d2feeeb15bcd68d19b57a484baf1e2133cba227c0c0173619519a6db8959fa71ca2f842480f
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2' npth_1.8.orig.tar.bz2 317739 SHA512:34fdeea3d8a7a594d8fdbcc6d5d389b5c8e282e8e84c1491b1e51960c0fa007df6a1d62543f0107f0772f3215557d4b25c2a9c7067cb0ae2f8de7b4d63d09fb4
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2.asc' npth_1.8.orig.tar.bz2.asc 390 SHA512:2d2d26d2bde77997187792f724b89b6c1ba7ad845c0087d78d7bd2eef688136df8fa8ea02c5199c0a3ad602bf228af0fadf82ecd3ff4b9ed35c71d009bb2e1a5
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-3.debian.tar.xz' npth_1.8-3.debian.tar.xz 8668 SHA512:a7fbc1c6106e04988fe6b18adf35a00bb7fe50e7212b046309a4dd42c90d7fc788a4d03abf2c628bd108db9ecfd2ec26aaa0d32b19a699a5f333daae446d5cc3
```

### `dpkg` source package: `openldap=2.6.10+dfsg-1ubuntu5`

Binary Packages:

- `libldap-common=2.6.10+dfsg-1ubuntu5`
- `libldap2:amd64=2.6.10+dfsg-1ubuntu5`

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
$ apt-get source -qq --print-uris openldap=2.6.10+dfsg-1ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1ubuntu5.dsc' openldap_2.6.10+dfsg-1ubuntu5.dsc 3426 SHA512:addfc27c84e83b2cce4c2efe398641eb87192f42d35ab6e25eaca4021b347f8070fef08d3f4a95e3d1e1999b7d9f1d666f535c6f54eb8c071808f4199b21d185
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA512:9c24cab12ea4002560670d1a6053c00582aea1713e3db262bbf5aae7666c6d50ef28e7b59ca4dbe5c5b5903e56268911a935a58ef852239c259830458e804f62
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1ubuntu5.debian.tar.xz' openldap_2.6.10+dfsg-1ubuntu5.debian.tar.xz 189056 SHA512:6955829975b20a8c45b6f958fcb7c0f88408df8c4befe6d407ef2020c0dbcfb8f5e147cc405db676922ffa2061d4cc700d12ce15bd3b7f79c40822be0bf091b4
```

### `dpkg` source package: `openssh=1:10.2p1-2ubuntu1`

Binary Packages:

- `openssh-client=1:10.2p1-2ubuntu1`

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
$ apt-get source -qq --print-uris openssh=1:10.2p1-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1-2ubuntu1.dsc' openssh_10.2p1-2ubuntu1.dsc 3499 SHA512:08eb87a6f300981e2ee35541582747b093d9d7bb9f9f45ae1c1b250df8c92e67972fd84b7267c1fd25bc6bcf2f32eec243e9da0735c6cfebea5a1686b03cbac2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1.orig.tar.gz' openssh_10.2p1.orig.tar.gz 1974519 SHA512:66f3dd646179e71aaf41c33b6f14a207dc873d71d24f11c130a89dee317ee45398b818e5b94887b5913240964a38630d7bca3e481e0f1eff2e41d9e1cfdbdfc5
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1.orig.tar.gz.asc' openssh_10.2p1.orig.tar.gz.asc 833 SHA512:f1f71700b1b0b2117aed505488b98b7ebb51ce26e53184b08df0b07aa2c5a1e54dc4d3cbcbe871b5ad849a2a0e22b02af318ff22a68c980ab53b04be03c9bf3c
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1-2ubuntu1.debian.tar.xz' openssh_10.2p1-2ubuntu1.debian.tar.xz 214552 SHA512:337a353a47f03a0acd9e4c3391cdd1d3a3e84b729620c5f30713623340a955403e1efbda18edf79ae782a15dfce7e3af1628181e73eec674366462cbd633f400
```

### `dpkg` source package: `openssl=3.5.3-1ubuntu2`

Binary Packages:

- `libssl3t64:amd64=3.5.3-1ubuntu2`
- `openssl=3.5.3-1ubuntu2`
- `openssl-provider-legacy=3.5.3-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10-1.dsc' p11-kit_0.25.10-1.dsc 2548 SHA512:31ae5779fcac1bae34128de7618597d2b2281ce48dd23cb9e3c96c7b77b103945f563249707735856f3e370ba14695664a7b00abbcb4b494bb8f973420618d38
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10.orig.tar.xz' p11-kit_0.25.10.orig.tar.xz 1053532 SHA512:c5a5dfb6bd46e8964a70f2fc601bd5b61bf88f79d1011c70e6f37a62130c4aad692d8bac83aff2fd2728543274e198d2946ded7a53636835aefb13b9a3155527
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10.orig.tar.xz.asc' p11-kit_0.25.10.orig.tar.xz.asc 228 SHA512:5c0e711fa1ef619bfd8ea479c45a6c76d22721549eb2a802f18644411fab6983fc09854677fac22b228e323a505e20036a9cfe4007f504567c5dd2bb1a3e6976
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10-1.debian.tar.xz' p11-kit_0.25.10-1.debian.tar.xz 24308 SHA512:e23a1108fb9d994d514b11ee7872a769207d70b9b8a7a9b566215249ce43d404e4ad8930cd34354c2189642e2a05b47497d888357892ff50628e638b0b6e9755
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

- `libperl5.40:amd64=5.40.1-6build1`
- `perl=5.40.1-6build1`
- `perl-base=5.40.1-6build1`
- `perl-modules-5.40=5.40.1-6build1`

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
$ apt-get source -qq --print-uris perl=5.40.1-6build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6build1.dsc' perl_5.40.1-6build1.dsc 2932 SHA512:249bedfe2613348fd33408c66d957102ac235c7d94473e90641bf60bdf7db600ac0300208b843145c5494f82988bfb6284018554bc78a84173e16884bc07a426
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6build1.debian.tar.xz' perl_5.40.1-6build1.debian.tar.xz 172908 SHA512:c8a4135968ee5a462f853a2651b570e9c9bff5305f4f6dc8dd5356904aa97d4f148eca8ce32cb12515e284f4067b8a4408cdb47f2675b43183017721c41b6dd3
```

### `dpkg` source package: `pinentry=1.3.2-3ubuntu1`

Binary Packages:

- `pinentry-curses=1.3.2-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.3.2-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2-3ubuntu1.dsc' pinentry_1.3.2-3ubuntu1.dsc 3373 SHA512:684e98947af437d702eae06d2ea2cd99a207a2c5736a3a5cc137ad95463a847f88176a61824829e84ea52ce9fedd5d03a400e2eba86b083be7670e20227304a2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2.orig.tar.bz2' pinentry_1.3.2.orig.tar.bz2 612858 SHA512:3b4d50a42d412d649a7830f7378aa966342c2bc0157d03b0ad79cf0aed29d6698d48c734e23b1dccada5f6ef81d0c09d3ead6cd703eadfc8082987e6bea0aafc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2.orig.tar.bz2.asc' pinentry_1.3.2.orig.tar.bz2.asc 427 SHA512:645e0bc78001dd1883f03437594588d2be8b0d1a32521c13d4ceea437652ca5675bd15977bdccdcfdabf96bc4edbaa567f547b46d7725d48c28e65be13654098
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2-3ubuntu1.debian.tar.xz' pinentry_1.3.2-3ubuntu1.debian.tar.xz 20348 SHA512:f8bb460c7411bca6c5fb69653f7ae2386ecbcd4f8fd641508cfaf8053820c2c0dda052c1f2a051bc648094721b2a0f3ca698206a56ba98dc1c8f6cbf75e510d2
```

### `dpkg` source package: `procps=2:4.0.4-9ubuntu1`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-9ubuntu1`
- `procps=2:4.0.4-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-9ubuntu1.dsc' procps_4.0.4-9ubuntu1.dsc 2247 SHA512:8b1abfba83a6d8ddbea36ec5bc5629769c73774cd02766dd2fb738c6c9ea7b333b51ce69905aca0d8aeb9cb8fe380bf3d1f28db8d32507efe65c34bf87951d50
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-9ubuntu1.debian.tar.xz' procps_4.0.4-9ubuntu1.debian.tar.xz 62072 SHA512:e7991c0546e67c6fe6db5c81f11dbb402999800b4665709da03eea8283e7b268845e460f78dbb7af4219b1708315c84dd0f080c8e834288ab95a8df4bf1b6976
```

### `dpkg` source package: `python3-defaults=3.13.7-1`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.7-1`
- `python3=3.13.7-1`
- `python3-minimal=3.13.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python3-defaults/3.13.7-1/


### `dpkg` source package: `python3.13=3.13.11-1`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.11-1`
- `libpython3.13-stdlib:amd64=3.13.11-1`
- `python3.13=3.13.11-1`
- `python3.13-minimal=3.13.11-1`

Licenses: (parsed from: `/usr/share/doc/libpython3.13-minimal/copyright`, `/usr/share/doc/libpython3.13-stdlib/copyright`, `/usr/share/doc/python3.13/copyright`, `/usr/share/doc/python3.13-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.13=3.13.11-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.11-1.dsc' python3.13_3.13.11-1.dsc 3699 SHA512:5f8ec535986e77fe4e25ddf81a3dc02df91ed559a7af9a9025fedfff6232a77475264c935e4037be1cac4e015ef2bbaf21f22f6afc2905ab3050d267738afc7e
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.11.orig.tar.xz' python3.13_3.13.11.orig.tar.xz 22704352 SHA512:11a910785bb3edeb3888331f29d2514d539f08b07d3125186364ab0e261dab29c7e7c70fe08d89718c38b6053cbe932ac4a6062ac291871e6f4173d29425264a
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.11.orig.tar.xz.asc' python3.13_3.13.11.orig.tar.xz.asc 963 SHA512:10beaba6d0e84f0335c0add480114e98a64133ec70d320593349de86091ccbdd69743559297f9c8c5e9926089890fd0e7881388e86084f46a413e9579c59d23c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.11-1.debian.tar.xz' python3.13_3.13.11-1.debian.tar.xz 261648 SHA512:0f473fd01f42015e1c47d34c2ba4058ec89e15f6427e08a635c7abd0602d7fce6186b56ad8b42a2be0552a7ffbad4cb2caa7fa5b5cb70d35eca7d14aa76debaa
```

### `dpkg` source package: `readline=8.3-3`

Binary Packages:

- `libreadline8t64:amd64=8.3-3`
- `readline-common=8.3-3`

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
$ apt-get source -qq --print-uris readline=8.3-3
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-3.dsc' readline_8.3-3.dsc 2817 SHA512:da2062b49605d9fec2bec460bd724b333b52464506013086d5912b27a0c429753d463830f58223a718c620cc3c47249b715360374f57ed299373b9fa1dee508a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3.orig.tar.gz' readline_8.3.orig.tar.gz 3419642 SHA512:513002753dcf5db9213dbbb61d51217245f6a40d33b1dd45238e8062dfa8eef0c890b87a5548e11db959e842724fb572c4d3d7fb433773762a63c30efe808344
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-3.debian.tar.xz' readline_8.3-3.debian.tar.xz 34188 SHA512:3296406f695d9828dccbc8ed6dde856951fc96a625e31cbf43e59986cefb48267514062c76818914b7402fda4f95016ce2ef7cc6ab62f0a7440b91a6edc49f58
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
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-3.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-3.dsc 2295 SHA512:b670257b456696972739f21b9306ad38a0a36c6962dac67dac66b1091548990acd765e76a450ea57bdba30f623026487b34d6d3b5ba674abf0c009f4955ec2e4
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-3.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-3.debian.tar.xz 8180 SHA512:63735f2e10b667d4aaa4258b581444f2e7b54ab8d223eb530acf42f4fc635e3163a00cb323aeb41ceeabf4ce94d8ec065e58c01d71efe4f71f376a9fbd66eb74
```

### `dpkg` source package: `rust-coreutils=0.2.2-0ubuntu2`

Binary Packages:

- `rust-coreutils=0.2.2-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/rust-coreutils/copyright`)

- `Apache-2.0`
- `MIT`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rust-sequoia-sq=1.3.1-6`

Binary Packages:

- `sq=1.3.1-6`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=1.3.1-6
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-6.dsc' rust-sequoia-sq_1.3.1-6.dsc 4451 SHA512:20dc5deef07b7f7fc1feba1aa9386fa8229caf5c711010ff418a2791d282bf9aab4831afcca08581c2219b03cc652f6c4117011aca8043beebe15dcf3b96052c
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1.orig.tar.gz' rust-sequoia-sq_1.3.1.orig.tar.gz 740320 SHA512:3aa4468b7bcb27532907ce759852e6b92b394a2fc91953b9f3723b9deaab3661c84fb298d79ef3332467aa7a5ca1158d6a8bd65dd961d30aafdcfb34a867c880
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-6.debian.tar.xz' rust-sequoia-sq_1.3.1-6.debian.tar.xz 5480 SHA512:514724c31df2eee0bbe2a9726cbd90bbaaab0b8a10db1196aaff1329e5f29ecbc2ffb8f32a13d20b057edad960f5755c9a18bbc971f2933cde8d55b61c2e2612
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

### `dpkg` source package: `sensible-utils=0.0.26build1`

Binary Packages:

- `sensible-utils=0.0.26build1`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.26build1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.26build1.dsc' sensible-utils_0.0.26build1.dsc 1730 SHA512:94ebf17d5aaa6c4ce36c6ebbe2dbce8d53d8724432a42971f6faf485ed1f7a855bbbeafbb0b9343227dbd34cfaaa3e0ed4cbe19d8f77eb3e7e43e7a2ab8893df
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.26build1.tar.xz' sensible-utils_0.0.26build1.tar.xz 76808 SHA512:e07fb2499d79d7fb8d50e9fb6b3f8be0cfd71722fc3275159395e4aa6d13fd5f95034454b8a669aa6f59f6997c7ebf3410739afd0700f26796bcd85f8dece713
```

### `dpkg` source package: `serf=1.3.10-3ubuntu1`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `subversion=1.14.5-5`

Binary Packages:

- `libsvn1:amd64=1.14.5-5`
- `subversion=1.14.5-5`

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
$ apt-get source -qq --print-uris subversion=1.14.5-5
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-5.dsc' subversion_1.14.5-5.dsc 4074 SHA512:d3967627842e76b30a2bec87e4eb577430425f6acd8ee893cd50c4897b62fa8d5cd2a1395956812692448ed6cbf3b8e8105c1c3b091ae08e354d88c26f544065
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz' subversion_1.14.5.orig.tar.gz 11645728 SHA512:a8e9f5bf9f32e4fa9a5873544c9228a392af0b4ec1126389a98cd8830c0644fc9d4b88bcb800c0e2c40bd58517cfaba23d79164c774d2cb3267a897c1d599634
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz.asc' subversion_1.14.5.orig.tar.gz.asc 2382 SHA512:b85c4d6e77194b5edff12e3e57c7d673226253048ddf3b622bb4dee6a8aed9153d3c69477876a7caae9eebe2ff5930e42993e34c8fc33d9fa65f9a57bc005d24
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-5.debian.tar.xz' subversion_1.14.5-5.debian.tar.xz 300656 SHA512:ed80ee81cb405ff7c6e487e49fa03d37c6f6ed33f0fd3ccd433e7ae72e8da5dce3627b2341c8b8c06f2dea40a469589c863b6df6aab247a50b4969fd8a3c222a
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sysvinit=3.15-5ubuntu1`

Binary Packages:

- `sysvinit-utils=3.15-5ubuntu1`

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
$ apt-get source -qq --print-uris sysvinit=3.15-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.15-5ubuntu1.dsc' sysvinit_3.15-5ubuntu1.dsc 2489 SHA512:1a2e3989915b6098334168ecbb5a259d0a8a528c57b3ca51a40de78b935942276901b3f01f431adce77651512859af0bfd462813312832dea973073efda91839
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.15.orig.tar.gz' sysvinit_3.15.orig.tar.gz 516469 SHA512:94613deefc08f2fe8191d08cfdd05e0ed569b9ffac40795acf6b3bddfc412ff13aeb546b279641c2b1722f505d34830e1f71cfb433c4ab94a343342a8d0f9d1b
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.15-5ubuntu1.debian.tar.xz' sysvinit_3.15-5ubuntu1.debian.tar.xz 124244 SHA512:4235cc11519557f7988a3ca93014dbd2bd43b3f72c7247e38c1ab844f8ef1b766d04643f29d307aeb187c07292e64b1677197242b9f093f474e1e9f0b15970f5
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

### `dpkg` source package: `tzdata=2025c-3ubuntu1`

Binary Packages:

- `tzdata=2025c-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ubuntu-keyring=2023.11.28.1build1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1build1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2023.11.28.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1build1.dsc' ubuntu-keyring_2023.11.28.1build1.dsc 1896 SHA512:07c3c2cfb1eb230ed745245d069a4c41c8ae3f9bb82d9aeed9d1823f7c398f13b996b4708e8ccdb509347ae2764982735cdfa5927d58b4e7fa8508068148293e
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1build1.tar.xz' ubuntu-keyring_2023.11.28.1build1.tar.xz 20300 SHA512:5f6d23d46b4f6d0b0e894ca54509aa4cc6fcd3904ab58ed275111d7a5612b05ddc07664e30e516c5315f73ac28a3d81c23618fcef185cde8599131f5775b64e5
```

### `dpkg` source package: `ucf=3.0052`

Binary Packages:

- `ucf=3.0052`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0052
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052.dsc' ucf_3.0052.dsc 1512 SHA512:04b2579fe93e2d7275325e229a045012e90535b2d795285403faf25096ec813c8895eef29733638e615f651950e591fe6fc68f0e47710b2c958edbab2254e112
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052.tar.xz' ucf_3.0052.tar.xz 71488 SHA512:388c59769867d510eb1583dd98168b3bd6cb678bf753cde781b09ad3ebc8d38a1811293253c15dad272cfa529967474dc629f1d27b00fc4473eea6745fdc0b42
```

### `dpkg` source package: `utf8proc=2.10.0-2`

Binary Packages:

- `libutf8proc3:amd64=2.10.0-2`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.10.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.10.0-2.dsc' utf8proc_2.10.0-2.dsc 1404 SHA512:022121ffe94a575224be0eb4a05260720bd9cf46548f0ca08720dff7d98f4afdb9a85c1b7ad8541accdb6d95b9726ec2b798762266735f7b8d4d2e8c99edd0a5
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.10.0.orig.tar.gz' utf8proc_2.10.0.orig.tar.gz 199045 SHA512:92a771606bcbecbb86c8d101931bc042dc7035938a665a7a449c2d8a7d3255df9df9c77c5cab0fc9dcaecb04be970149f60bfff463fc813e96727b7035ca9bb4
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.10.0-2.debian.tar.xz' utf8proc_2.10.0-2.debian.tar.xz 6088 SHA512:0193f58f08b2c3cf82afb24ee4e26047bcecee16d5bdfbe24f81b564ad03642e162a6a7ceda6b0950ff18cf7d3b30cb4e8321493dfe66d3e926a867fb9a7fdf5
```

### `dpkg` source package: `util-linux=2.41.2-4ubuntu1`

Binary Packages:

- `bsdutils=1:2.41.2-4ubuntu1`
- `libblkid1:amd64=2.41.2-4ubuntu1`
- `libmount1:amd64=2.41.2-4ubuntu1`
- `libsmartcols1:amd64=2.41.2-4ubuntu1`
- `libuuid1:amd64=2.41.2-4ubuntu1`
- `login=1:4.16.0-2+really2.41.2-4ubuntu1`
- `mount=2.41.2-4ubuntu1`
- `util-linux=2.41.2-4ubuntu1`

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


### `dpkg` source package: `wget=1.25.0-2ubuntu3`

Binary Packages:

- `wget=1.25.0-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.25.0-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0-2ubuntu3.dsc' wget_1.25.0-2ubuntu3.dsc 2120 SHA512:5159ef1e772838d024e07d7c41da8ca0477ad5d77e0e9f0b124e99125f82f2535d1b589a16a91796915f9783c0bbeca88596ea0b5d44c4608427bfdfcbd4ea80
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0.orig.tar.gz' wget_1.25.0.orig.tar.gz 5263736 SHA512:a7ce33c07a1a206a8574b6e9ea7cc5292315df0914edbcf05a014d35ae9e3d24699a46818b409b884ada57428cf30502f4bbb3767cae2c6934e4e7fb2d0c5036
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0-2ubuntu3.debian.tar.xz' wget_1.25.0-2ubuntu3.debian.tar.xz 31992 SHA512:a651d8813dda881509f85358a622b6ec48bf4d17f1bbd2ff2c173e8133d3d13f419a7876539cef0ba13cd88dece61272b8913959964aa14be05e07282d5659ce
```

### `dpkg` source package: `xxhash=0.8.3-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.3-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2build1.dsc' xxhash_0.8.3-2build1.dsc 1968 SHA512:c0724343c725447e14dcb6478eeb56db152fa4bb8e86cdd4f2764eaee7acb9682b165c74ce8f177047305ef33249d110436865840118e703f740c58eec0115d6
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA512:8b5c8b9aad4e869f28310b12cc314037feda81d92f26c23eaecdb35dc65042ca2e65f2e9606033e62a31bcc737a9a950500ffcbdb8677d6ab20e820ea14f2b79
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2build1.debian.tar.xz' xxhash_0.8.3-2build1.debian.tar.xz 5224 SHA512:ac6d91fa86c5273eaf27200b3f57ee716e8d54d346bfd950f3d2bc76a716e5765ebf1d0d1380b2bddacafa445ca7209a8ee78e2e1351b201bbe6d5c934b98390
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xz-utils/5.8.2-1/


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
