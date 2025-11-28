# `buildpack-deps:resolute`

## Docker Metadata

- Image ID: `sha256:28a230fde8792718e74eecf2cae834272496b5a700682ee7d584274b5a7363f3`
- Created: `2025-11-14T03:12:44.701298177Z`
- Virtual Size: ~ 801.77 Mb  
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

### `dpkg` source package: `aom=3.13.1-2`

Binary Packages:

- `libaom3:amd64=3.13.1-2`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.13.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.13.1-2.dsc' aom_3.13.1-2.dsc 2402 SHA512:cc86258464b3b5eb3a2be500c0f5387b1a93952336b057fade04c9ffa2bf2bec104e6cf6e7b3992458c6d16e26ee809678ea50dc6f483ab9639733986d4d95db
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.13.1.orig.tar.gz' aom_3.13.1.orig.tar.gz 6262920 SHA512:cde7b044131bdf642758948b6ccbcfa1c79d1d698badfc3a82d88f78ef09c55c6ac3a04e3c515af2f89becf94eb48f0af5145e0784628f95676a85e8dd350a7a
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.13.1-2.debian.tar.xz' aom_3.13.1-2.debian.tar.xz 20840 SHA512:082d2e163f7c1d4bcb4c6fe76d88e75c4e11339bef19c32f64a68c952db3cd5f23aee361ac4a726fb2febfe0863a2ec58ef2679df4df11f8e30ac0695e7def5e
```

### `dpkg` source package: `apr-util=1.6.3-3ubuntu2`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu2.dsc' apr-util_1.6.3-3ubuntu2.dsc 2684 SHA512:77084753ad19bf95ffefc897a560392ce9fad753cae1f3e53c8bfe39f97868cc76565c4256605f83c3271d8322797245bd02a03bd3ad4fc490ba43e96c005ea3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA512:8050a481eeda7532ef3751dbd8a5aa6c48354d52904a856ef9709484f4b0cc2e022661c49ddf55ec58253db22708ee0607dfa7705d9270e8fee117ae4f06a0fe
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu2.debian.tar.xz' apr-util_1.6.3-3ubuntu2.debian.tar.xz 342620 SHA512:e7a088f2fcf5d77bf5f7c3dbdd99e3cc120a6c1f81a3b04494159f37702b799bed18f592cc7e6916cbdfff5516a206afa9c7b20cd7b2ee499d4e8eb5facfd064
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


### `dpkg` source package: `architecture-properties=0.2.6`

Binary Packages:

- `native-architecture=0.2.6`

Licenses: (parsed from: `/usr/share/doc/native-architecture/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris architecture-properties=0.2.6
'http://archive.ubuntu.com/ubuntu/pool/main/a/architecture-properties/architecture-properties_0.2.6.dsc' architecture-properties_0.2.6.dsc 1803 SHA512:9afa5d7161746d22fe3415d5d8016e63d2c6db514285893863025ec29e575aa45c0f53058c25245d7bc86fa9073876f5948e4df0fbf350df1de12c676a18f9da
'http://archive.ubuntu.com/ubuntu/pool/main/a/architecture-properties/architecture-properties_0.2.6.tar.xz' architecture-properties_0.2.6.tar.xz 5368 SHA512:e698d5cd2dd19f4ec07d5732f4023c7e663a9de4f15da56614d624a90611ceba012b8688405def94bc61b0d2197f79000409fa9c471bf1d8ad15bb1b834f3f19
```

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

### `dpkg` source package: `autoconf=2.72-3.1ubuntu1`

Binary Packages:

- `autoconf=2.72-3.1ubuntu1`

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
$ apt-get source -qq --print-uris autoconf=2.72-3.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.1ubuntu1.dsc' autoconf_2.72-3.1ubuntu1.dsc 1926 SHA512:1b65c2f5dc49006d9dc0d764247c82ef662c3a4ea6c2a8acff8929761685fc8b60f2257193ba159944c9e1adab38c495dad89c2c5c389606a000befde3ad1b7a
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72.orig.tar.xz' autoconf_2.72.orig.tar.xz 1389680 SHA512:c4e9fbd858666d3e5c3b4fe7f89aa3e8e3a0a00dc7e166f8147d937d911b77ba3ac6a016f9d223ccdd830bc8960b3e60397c0607cc6a1fd2c50c7492839ddd17
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.1ubuntu1.debian.tar.xz' autoconf_2.72-3.1ubuntu1.debian.tar.xz 27368 SHA512:8857affd80e5ebed22acd25ea721acdefe1208df57be348a90d59e5a4b93ed4957e54eccf71ee3d56ed186bfba5a45424d2089e22fa3ddafdc335a9534557aaa
```

### `dpkg` source package: `automake=1:1.18.1-2`

Binary Packages:

- `automake=1:1.18.1-2`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/automake/1:1.18.1-2/


### `dpkg` source package: `autotools-dev=20240727.1`

Binary Packages:

- `autotools-dev=20240727.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20240727.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20240727.1.dsc' autotools-dev_20240727.1.dsc 1661 SHA512:0fc92985b4585e2281145cc7ed1425eda146f462666b3ec2aff6559053e991188f2cbc28c556df4d3a1d6e45269d35aae321d5ef201ef6e534bad98a18e8b5fd
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20240727.1.tar.xz' autotools-dev_20240727.1.tar.xz 99716 SHA512:464f1acda3a0a62a30510d7aa218137128e41f5152436016c44220154859e8a49bbd42513b2136b3c94502003792f49f5d6aa2ac7f4d9b6bf4c1556e84a2758e
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


### `dpkg` source package: `binutils=2.45-8ubuntu1`

Binary Packages:

- `binutils=2.45-8ubuntu1`
- `binutils-common:amd64=2.45-8ubuntu1`
- `binutils-x86-64-linux-gnu=2.45-8ubuntu1`
- `libbinutils:amd64=2.45-8ubuntu1`
- `libctf-nobfd0:amd64=2.45-8ubuntu1`
- `libctf0:amd64=2.45-8ubuntu1`
- `libgprofng0:amd64=2.45-8ubuntu1`
- `libsframe2:amd64=2.45-8ubuntu1`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe2/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.45-8ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.45-8ubuntu1.dsc' binutils_2.45-8ubuntu1.dsc 8951 SHA512:14e4a8d83880a7699a86b3ffa02ba807bf63ddc66094220f4c461686297fb141a3516b25e387c15fed5e0d6958b1a7f7b3f356fd16f75450167b6a515b13d975
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.45.orig.tar.xz' binutils_2.45.orig.tar.xz 27868232 SHA512:c7b10a7466d9fd398d7a0b3f2a43318432668d714f2ec70069a31bdc93c86d28e0fe83792195727167743707fbae45337c0873a0786416db53bbf22860c16ce7
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.45-8ubuntu1.debian.tar.xz' binutils_2.45-8ubuntu1.debian.tar.xz 159252 SHA512:195ee671c6b61238dcb3d8051d0e3629e0deb8ba57d1f13785af04bdd8e5dc911b843e0c16c3b12ce65eb1c53b019e9baaa2bb3085098c0146b56946865a18db
```

### `dpkg` source package: `brotli=1.1.0-2build6`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2build6`
- `libbrotli1:amd64=1.1.0-2build6`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

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

- `bzip2=1.0.8-6build1`
- `libbz2-1.0:amd64=1.0.8-6build1`
- `libbz2-dev:amd64=1.0.8-6build1`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

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

### `dpkg` source package: `cairo=1.18.4-1build1`

Binary Packages:

- `libcairo2:amd64=1.18.4-1build1`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.4-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4-1build1.dsc' cairo_1.18.4-1build1.dsc 2787 SHA512:c9588167e35c81d66db4cd88ff2c388c9b88a5db8ada4269fb079a9ee7e6e3a3423b1700a71d7fc57e251ef035990fceab9bf8e87bff966c49d96e2259ebd51d
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4.orig.tar.xz' cairo_1.18.4.orig.tar.xz 32578804 SHA512:863679f817ed67dc2c916c035d740916e27e7e69c04fca63936e37d274e7f4c79848d16c8f7c481798864602e8847c489f698df89b785cbc576c925dbd513316
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4-1build1.debian.tar.xz' cairo_1.18.4-1build1.debian.tar.xz 29988 SHA512:03645feedf5709386a369e10cdaba66ff028a36860dca47d02f58b7cae08ae8183962bc1c9af07e6b332feb7cbfdfc11c793e0a11df92becc1058d32778a112a
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


### `dpkg` source package: `curl=8.14.1-2ubuntu1`

Binary Packages:

- `curl=8.14.1-2ubuntu1`
- `libcurl3t64-gnutls:amd64=8.14.1-2ubuntu1`
- `libcurl4-openssl-dev:amd64=8.14.1-2ubuntu1`
- `libcurl4t64:amd64=8.14.1-2ubuntu1`

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
$ apt-get source -qq --print-uris curl=8.14.1-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1-2ubuntu1.dsc' curl_8.14.1-2ubuntu1.dsc 3259 SHA512:9d12f09b1d5ff9512dc01f6d8a5562ab4b2833aaeae3cc072d1a484d2847afede6cc0a29b34972db9412f0270cc3406727b1d59a17cb52b9398a9f5057e268d8
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1.orig.tar.gz' curl_8.14.1.orig.tar.gz 4250332 SHA512:22307bd41d5ded22e7e53e2412b3218763db9b7c32b1254df26172e6cf00d1650c66874dfc03037da89a5bd72ffbca1eeb83784be62a38d5779484376f3a53c7
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1.orig.tar.gz.asc' curl_8.14.1.orig.tar.gz.asc 488 SHA512:c9b7ad3407660e87fed16a4184a5d75f08815ab569dc8972115430fe750ca5a0a7c72b60e9bacc5ff50084256d1ebc80bb2141f664fa1e0fb239cb86b03f8819
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1-2ubuntu1.debian.tar.xz' curl_8.14.1-2ubuntu1.debian.tar.xz 55756 SHA512:bcc04c901cbb5b38f4a09b106c74b29692edf9dd06fd146e896aaaab05fd1ee7c6b7f8990cc6a249237bdf0677a07f863475dc87f61b7adc90b6455486e03cec
```

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

### `dpkg` source package: `db-defaults=1:5.3.21ubuntu3`

Binary Packages:

- `libdb-dev:amd64=1:5.3.21ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=1:5.3.21ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu3.dsc' db-defaults_5.3.21ubuntu3.dsc 1619 SHA512:679b84431228f1a5cfd06cd0ff57a55add21e3e050ee4fae5544f0db1b575558db1845b077612a39781d9e2cc0cac3ae36947c1a72db4dea41ae89f0cc4fc65a
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu3.tar.xz' db-defaults_5.3.21ubuntu3.tar.xz 2832 SHA512:d47a21da2f8129e2c067cdb2398e087f2bfd3a6a206e3f3167456c84fc2d168cd100605e6582b7c865b8b8e1e0a59a7795e4267d39428b9ef92bd23b5a5293e0
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-10ubuntu1`

Binary Packages:

- `libdb5.3-dev=5.3.28+dfsg2-10ubuntu1`
- `libdb5.3t64:amd64=5.3.28+dfsg2-10ubuntu1`

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


### `dpkg` source package: `djvulibre=3.5.29-1`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.29-1`
- `libdjvulibre-text=3.5.29-1`
- `libdjvulibre21:amd64=3.5.29-1`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.29-1
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.29-1.dsc' djvulibre_3.5.29-1.dsc 2389 SHA512:2addf124bbfc05bcfc21dfae644ac35f38198133c4dec5a00dc572b064d0729c13afb36d7459bdc89af82050af4effb01e3cd698fc46633c16440c093a8f4463
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.29.orig.tar.xz' djvulibre_3.5.29.orig.tar.xz 3214548 SHA512:e8f4631f29ee20fefea7abc92aed09b658a4abea4821d1fad534156679c0fd3736e2bedd26dc5d9360061be9629a76ae00aca57054256edb33afa53dbb13b987
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.29-1.debian.tar.xz' djvulibre_3.5.29-1.debian.tar.xz 16780 SHA512:3180f3d9bc8fe344fd94429accd72eb89c151ed8e94ed8fcda7514f121efc84d9235313673b5c2dd8422503a7a36fb97ff74053a8add754591897cf64080741c
```

### `dpkg` source package: `dpkg=1.22.21ubuntu5`

Binary Packages:

- `dpkg=1.22.21ubuntu5`
- `dpkg-dev=1.22.21ubuntu5`
- `libdpkg-perl=1.22.21ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

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

- `comerr-dev:amd64=2.1-1.47.2-3ubuntu2`
- `e2fsprogs=1.47.2-3ubuntu2`
- `libcom-err2:amd64=1.47.2-3ubuntu2`
- `libext2fs2t64:amd64=1.47.2-3ubuntu2`
- `libss2:amd64=1.47.2-3ubuntu2`
- `logsave=1.47.2-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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

### `dpkg` source package: `elfutils=0.194-1`

Binary Packages:

- `libelf1t64:amd64=0.194-1`

Licenses: (parsed from: `/usr/share/doc/libelf1t64/copyright`)

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
$ apt-get source -qq --print-uris elfutils=0.194-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194-1.dsc' elfutils_0.194-1.dsc 3317 SHA512:4d9877804f434ba81855b4416d8761575f073bef91e971d1558ad1e196fd8552e4ccd11d8100aa25a83c68c8e32f197160d21e4ab8fba893a95f25ae3f180e07
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194.orig.tar.bz2' elfutils_0.194.orig.tar.bz2 12003321 SHA512:5d00502f61b92643bf61dc61da4ddded36c423466388d992bcd388c5208761b8ed9db1a01492c085cd0984eef30c08f895a8e307e78e0df8df40b56ae35b78a5
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194-1.debian.tar.xz' elfutils_0.194-1.debian.tar.xz 44252 SHA512:f9313bac391509d3a637e0ac5ed03e466f1818e60c825d0d1052679badb449be7bf690a9f48b13728f4f62e3123244e7ef3a36dc50389514aa3540def4f22db9
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

### `dpkg` source package: `fftw3=3.3.10-2fakesync1build2`

Binary Packages:

- `libfftw3-bin=3.3.10-2fakesync1build2`
- `libfftw3-dev:amd64=3.3.10-2fakesync1build2`
- `libfftw3-double3:amd64=3.3.10-2fakesync1build2`
- `libfftw3-long3:amd64=3.3.10-2fakesync1build2`
- `libfftw3-quad3:amd64=3.3.10-2fakesync1build2`
- `libfftw3-single3:amd64=3.3.10-2fakesync1build2`

Licenses: (parsed from: `/usr/share/doc/libfftw3-bin/copyright`, `/usr/share/doc/libfftw3-dev/copyright`, `/usr/share/doc/libfftw3-double3/copyright`, `/usr/share/doc/libfftw3-long3/copyright`, `/usr/share/doc/libfftw3-quad3/copyright`, `/usr/share/doc/libfftw3-single3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-2fakesync1build2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build2.dsc' fftw3_3.3.10-2fakesync1build2.dsc 2893 SHA512:f87f249e4cdfe01455e70947cf2c3db3a87733f79a35a9fe9bea8efd7150b7d55f925b86a913ed29c1169816f39a73d3ff956e4a44f9704fe3c06fb1c6caa522
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4262403 SHA512:fa2ea740449fd06c833a82e1fff82bacd554188d500cbedff5a0bc185551799ef9ef9b8b1c227283abdbbdd185424d19df9c0f06ed88d5fe3d9c001d6fab6109
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build2.debian.tar.xz' fftw3_3.3.10-2fakesync1build2.debian.tar.xz 14828 SHA512:de62d3653d40d54e788285912ff6e2e31d5ddddab9d728f6b3f582253caf2e0cfa3e8e79883324f79a954d59a87f2e3369a0ed7fd8cce71c185ac1c356644932
```

### `dpkg` source package: `file=1:5.46-5build1`

Binary Packages:

- `file=1:5.46-5build1`
- `libmagic-mgc=1:5.46-5build1`
- `libmagic1t64:amd64=1:5.46-5build1`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.46-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5build1.dsc' file_5.46-5build1.dsc 2292 SHA512:3a7c29f9b78adda5049a56ec26f03679a51ba974bc36be0f7de8ff3eee33b933584840203b6923a79ab3a92a3d0e8eb17a64d6ea46c9d8991472c50c13291e7e
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz' file_5.46.orig.tar.gz 1312892 SHA512:a6cb7325c49fd4af159b7555bdd38149e48a5097207acbe5e36deb5b7493ad6ea94d703da6e0edece5bb32959581741f4213707e5cb0528cd46d75a97a5242dc
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz.asc' file_5.46.orig.tar.gz.asc 201 SHA512:a6e6fe92d909a9b153c88828942c2963b3b683cda5f6d7ae281e4ca42b30a582e82094b182976515ee85689200b8f6512d34b7f39291cbf9623d583ce688530a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5build1.debian.tar.xz' file_5.46-5build1.debian.tar.xz 37088 SHA512:16a41aec0f608438508a9d3ddb67eef430e3bd8ed874b0dc8e03b07c84d15d2653a21b9a450f872b70b9925383ca8897e7eccbbdd5bd0a5dae87c3700e57cfe2
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

### `dpkg` source package: `fontconfig=2.15.0-2.3ubuntu1`

Binary Packages:

- `fontconfig=2.15.0-2.3ubuntu1`
- `fontconfig-config=2.15.0-2.3ubuntu1`
- `libfontconfig1:amd64=2.15.0-2.3ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-2.3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-2.3ubuntu1.dsc' fontconfig_2.15.0-2.3ubuntu1.dsc 2780 SHA512:55ad92aada8da2ff73fd104e6bda124c4721b460209bd11a554672662b539570c82d4947ec7bcddaaf22cf95ef0e11103c72cd8e901ad281c31b0901211ebd81
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA512:754cd5fffa198fc07a39cf7df683e9adfa7f54ab41fdff8c0eacc078fd35d3e01069ba343f2b045e0b40df88d9f1fc1ee0f7565799f9cb194a59cf95b64c4417
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-2.3ubuntu1.debian.tar.xz' fontconfig_2.15.0-2.3ubuntu1.debian.tar.xz 33544 SHA512:f31328644fc622ad4f70fe04561d8ca67bd3f55079ffb051b428f8ae88b6c508915c8b73132f24bd1b2978ee7e4cdfa61f02d0efb13e6a46123fb937246ed9f7
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

### `dpkg` source package: `freetype=2.13.3+dfsg-1build1`

Binary Packages:

- `libfreetype-dev:amd64=2.13.3+dfsg-1build1`
- `libfreetype6:amd64=2.13.3+dfsg-1build1`

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
$ apt-get source -qq --print-uris freetype=2.13.3+dfsg-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1build1.dsc' freetype_2.13.3+dfsg-1build1.dsc 3683 SHA512:efa035db5286524e7410b5909397f935a7d5598068cd51a72257623cb0cf0ea9eec53d06830aad53bbaf3a90b94afdd4cefb9ec0efeee8b8b001b4868ab3a07d
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz 342404 SHA512:e662a20ad2ff80534e8ea0df2f299e8f61350f13d279f80f8257b18352e863dd2c266791b85d3410b0c83966cb12e3ff49cf398b83a651dc73772df9fcf5936c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:c676452fb04b49824ce0a7287b46dc0234cee301bf80d31da01f5a1e7009ddbc0479866bfca62086fe23105436b0c02b9fb729b8fa24e7ca703c0fc357fe3675
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz 2173852 SHA512:54ef9e3a4f0c298893268ed409f59aa1620a60c656ee3f8bdddbb91ffb2e70eea2f016a85c0a02eef699de362abee4aabae4482f0fa1cbf42967b5873fc84f2d
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:bd1699aa0bf9f93a02b87a9c59ee6b69e4b24626fbcfbf9e0a0739f2634923bd397ee51379f57aae88465823ceb6bfe5cf6708a2bfa32d76f4a64ad6a9c08e3b
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig.tar.xz' freetype_2.13.3+dfsg.orig.tar.xz 2201416 SHA512:634c2644bb70b93a605fae4d3e731cb13d149af4d01029ecf2d166b2e07cba07489303440a836057adc54f9bdabcceb7fde102dc5e5bf69f35c99ebae66f7293
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1build1.debian.tar.xz' freetype_2.13.3+dfsg-1build1.debian.tar.xz 43984 SHA512:d638ead967f431e69f24f9146dab812ba4f87b96a7378fe393a5d93e4d55ed364b24e531e9c7c4adf8fb89cf7145973d188fb1249b397933bc39b0519811ea56
```

### `dpkg` source package: `fribidi=1.0.16-3`

Binary Packages:

- `libfribidi0:amd64=1.0.16-3`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.16-3
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16-3.dsc' fribidi_1.0.16-3.dsc 2027 SHA512:aed3922de0de22004c039c593675dc1265c88b6e180f2f850d5ad0e024ffbcb9495246b26a4379641ed1d6a48edccd949ddc30875ea67065929473d96ab66fa9
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16.orig.tar.xz' fribidi_1.0.16.orig.tar.xz 1098260 SHA512:e3a56f36155f6813e3609473639fc533de742309f561c463012dc90b412a1ac7694b765d92669b2cbfaee973ca0e92fa5e926e68a1a078921f26ef17d82ab651
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16-3.debian.tar.xz' fribidi_1.0.16-3.debian.tar.xz 9032 SHA512:20414e9519ae4fb00fd1d9a2ace5b886d30d5446c8962d5b9934c174336daa42fc8cdffeb87a19b71ca0d1b74c07d68e8eb2051946542f9a3986f883be6b9611
```

### `dpkg` source package: `gcc-15=15.2.0-7ubuntu1`

Binary Packages:

- `cpp-15=15.2.0-7ubuntu1`
- `cpp-15-x86-64-linux-gnu=15.2.0-7ubuntu1`
- `g++-15=15.2.0-7ubuntu1`
- `g++-15-x86-64-linux-gnu=15.2.0-7ubuntu1`
- `gcc-15=15.2.0-7ubuntu1`
- `gcc-15-base:amd64=15.2.0-7ubuntu1`
- `gcc-15-x86-64-linux-gnu=15.2.0-7ubuntu1`
- `libasan8:amd64=15.2.0-7ubuntu1`
- `libatomic1:amd64=15.2.0-7ubuntu1`
- `libcc1-0:amd64=15.2.0-7ubuntu1`
- `libgcc-15-dev:amd64=15.2.0-7ubuntu1`
- `libgcc-s1:amd64=15.2.0-7ubuntu1`
- `libgomp1:amd64=15.2.0-7ubuntu1`
- `libhwasan0:amd64=15.2.0-7ubuntu1`
- `libitm1:amd64=15.2.0-7ubuntu1`
- `liblsan0:amd64=15.2.0-7ubuntu1`
- `libquadmath0:amd64=15.2.0-7ubuntu1`
- `libstdc++-15-dev:amd64=15.2.0-7ubuntu1`
- `libstdc++6:amd64=15.2.0-7ubuntu1`
- `libtsan2:amd64=15.2.0-7ubuntu1`
- `libubsan1:amd64=15.2.0-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp-15/copyright`, `/usr/share/doc/cpp-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-15/copyright`, `/usr/share/doc/g++-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-15/copyright`, `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/gcc-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-15-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-15-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gcc-defaults=1.229ubuntu1`

Binary Packages:

- `cpp=4:15.2.0-4ubuntu1`
- `cpp-x86-64-linux-gnu=4:15.2.0-4ubuntu1`
- `g++=4:15.2.0-4ubuntu1`
- `g++-x86-64-linux-gnu=4:15.2.0-4ubuntu1`
- `gcc=4:15.2.0-4ubuntu1`
- `gcc-x86-64-linux-gnu=4:15.2.0-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.229ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.229ubuntu1.dsc' gcc-defaults_1.229ubuntu1.dsc 38342 SHA512:814e39c4bb9a562e5c87b2c111c2b5af1ec641c0e5bfe84929c83bca9045859b73c900baa40ffc350515b6653142ba7e035cf0269a360adf163c2d8cbb3b9318
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.229ubuntu1.tar.xz' gcc-defaults_1.229ubuntu1.tar.xz 58296 SHA512:01038a0c30fd0fa724e08ec397361c2bf5b42040761508ff6297dc92ebe7b29eb8a0f8679b9e20128aebea78df77d325f2927343a4b7089dc49a3c8e92e5d892
```

### `dpkg` source package: `gdbm=1.26-1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.26-1`
- `libgdbm-dev:amd64=1.26-1`
- `libgdbm6t64:amd64=1.26-1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

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

### `dpkg` source package: `glib2.0=2.86.1-2`

Binary Packages:

- `girepository-tools:amd64=2.86.1-2`
- `libgio-2.0-dev:amd64=2.86.1-2`
- `libgio-2.0-dev-bin=2.86.1-2`
- `libgirepository-2.0-0:amd64=2.86.1-2`
- `libglib2.0-0t64:amd64=2.86.1-2`
- `libglib2.0-bin=2.86.1-2`
- `libglib2.0-data=2.86.1-2`
- `libglib2.0-dev:amd64=2.86.1-2`
- `libglib2.0-dev-bin=2.86.1-2`

Licenses: (parsed from: `/usr/share/doc/girepository-tools/copyright`, `/usr/share/doc/libgio-2.0-dev/copyright`, `/usr/share/doc/libgio-2.0-dev-bin/copyright`, `/usr/share/doc/libgirepository-2.0-0/copyright`, `/usr/share/doc/libglib2.0-0t64/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/glib2.0/2.86.1-2/


### `dpkg` source package: `glibc=2.42-0ubuntu3`

Binary Packages:

- `libc-bin=2.42-0ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`)

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


### `dpkg` source package: `glibc=2.42-2ubuntu2`

Binary Packages:

- `libc-dev-bin=2.42-2ubuntu2`
- `libc-gconv-modules-extra:amd64=2.42-2ubuntu2`
- `libc6:amd64=2.42-2ubuntu2`
- `libc6-dev:amd64=2.42-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-gconv-modules-extra/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

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
$ apt-get source -qq --print-uris glibc=2.42-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-2ubuntu2.dsc' glibc_2.42-2ubuntu2.dsc 8036 SHA512:f0c4f3c8010bb5dcde8eb9fe4ab9f38aff7d4d0bc5b0e7e7d06fa947def1d1e9b05ef13b733de58f1e642f9013339b7f8a36af8fbd69ad6c8b385eabb1a0ab6d
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz' glibc_2.42.orig.tar.xz 19930508 SHA512:73a617db8e0f0958c0575f7a1c5a35b72b7e070b6cbdd02a9bb134995ca7ca0909f1e50d7362c53d2572d72f1879bb201a61d5275bac16136895d9a34ef0c068
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz.asc' glibc_2.42.orig.tar.xz.asc 981 SHA512:d868220778e98d24aead10a585e6a903892e4d043cd96a404634c8aa03d001d624a46a5c0fe13c86f83f66396a1f360a10990966fe377e98a722914b5087575d
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-2ubuntu2.debian.tar.xz' glibc_2.42-2ubuntu2.debian.tar.xz 448632 SHA512:73fbf7614810eb4a7f35a611cf86b57f93660dca92b0e75cad1b4932d4bde09effc61d8dcc7ae2fc394aa22803d2c6daa8b7f374ee95ee5f47e4759f96ba408c
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-5ubuntu1`

Binary Packages:

- `libgmp-dev:amd64=2:6.3.0+dfsg-5ubuntu1`
- `libgmp10:amd64=2:6.3.0+dfsg-5ubuntu1`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-5ubuntu1`

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


### `dpkg` source package: `gnupg2=2.4.8-4ubuntu1`

Binary Packages:

- `dirmngr=2.4.8-4ubuntu1`
- `gnupg=2.4.8-4ubuntu1`
- `gpg=2.4.8-4ubuntu1`
- `gpg-agent=2.4.8-4ubuntu1`
- `gpgconf=2.4.8-4ubuntu1`
- `gpgsm=2.4.8-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.4.8-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8-4ubuntu1.dsc' gnupg2_2.4.8-4ubuntu1.dsc 4565 SHA512:895b4aa27ab9565e24d79bdde6a7bf68280be0782c5fce3c12901dfe4410df63860e5052f84c2c976115cfa8ba745da46a9fd5a007d45c12f0fd6aace39e91dd
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8.orig.tar.bz2' gnupg2_2.4.8.orig.tar.bz2 8017685 SHA512:d7f07a258141a583bc8be18c0984d7dfe8508f12c624c053881ee63dfee11adcda8de216bcaaef9f5d24a1e217de70bf69ee2e3cc43b0da66a0e571ce9c4b436
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8.orig.tar.bz2.asc' gnupg2_2.4.8.orig.tar.bz2.asc 228 SHA512:f739eb41481149e145724969e94907ac55e082da0456e1343da24488958ecd020225b45e1d5dc4c93abc06fe89d942e892b488a460f3278f9f2bcff5f51c8ca0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8-4ubuntu1.debian.tar.xz' gnupg2_2.4.8-4ubuntu1.debian.tar.xz 121004 SHA512:5f917b2219a89234434604955927c3d0d73d8dbb631e183dbce195a8c3816e89c99f873efc2d1fec7dc790b731b7508795a0b368d69da2432e001bae971310cc
```

### `dpkg` source package: `gnutls28=3.8.9-3ubuntu2`

Binary Packages:

- `libgnutls-dane0t64:amd64=3.8.9-3ubuntu2`
- `libgnutls-openssl27t64:amd64=3.8.9-3ubuntu2`
- `libgnutls28-dev:amd64=3.8.9-3ubuntu2`
- `libgnutls30t64:amd64=3.8.9-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libgnutls-dane0t64/copyright`, `/usr/share/doc/libgnutls-openssl27t64/copyright`, `/usr/share/doc/libgnutls28-dev/copyright`, `/usr/share/doc/libgnutls30t64/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `graphite2=1.3.14-2ubuntu1`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2ubuntu1`

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
$ apt-get source -qq --print-uris graphite2=1.3.14-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2ubuntu1.dsc' graphite2_1.3.14-2ubuntu1.dsc 2650 SHA512:76b4ecf1d5c2fdbd4e50b434d39b83f7661a79047d14733b22f3b58ba621164b341a14cc6d0b018bd5101ecd8e9bcdcaa25ea6c05fab45eba64c96c41cde0902
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA512:49d127964d3f5c9403c7aecbfb5b18f32f25fe4919a81c49e0534e7123fe845423e16b0b8c8baaae21162b1150ab3e0f1c22c344e07d4364b6b8473c40a0822c
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2ubuntu1.debian.tar.xz' graphite2_1.3.14-2ubuntu1.debian.tar.xz 14384 SHA512:6d25f7498c175c26533ae14088723110b9a35f5242e2b35e3a2cfe71bd92d2f855c013c11abce5c9cd058407c78940377c2fe97c1c6b3beaee41006ec24382a4
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

### `dpkg` source package: `harfbuzz=12.1.0-1`

Binary Packages:

- `libharfbuzz0b:amd64=12.1.0-1`

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
$ apt-get source -qq --print-uris harfbuzz=12.1.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.1.0-1.dsc' harfbuzz_12.1.0-1.dsc 2606 SHA512:d94042b85e43e18597d3df814e09ec69dfd1a6c9fcc93a761f3985dd01ca9740d7622b80d69b1469a721913d6a56fee3c09edae69ebd0b9fb102cbce7ce232cc
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.1.0.orig.tar.xz' harfbuzz_12.1.0.orig.tar.xz 18208424 SHA512:94cbc3fe8fad30f4f7871bdddc8b129c486ab55329f9b48c6336fdf15d05f09c3c96cac51f68a0218db113b4783c07ce5d6bb455ccc875b31fd2261e3e8dc559
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.1.0-1.debian.tar.xz' harfbuzz_12.1.0-1.debian.tar.xz 19680 SHA512:eacf3889ad343213e4bce21b92001bb8112fc88e78cabe9e9ead69fcc75977d55f41d00ff3efedeed84fc3cb48e4e22d59dbba4d78f30278ec3bc534b142d3a1
```

### `dpkg` source package: `hicolor-icon-theme=0.18-2`

Binary Packages:

- `hicolor-icon-theme=0.18-2`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.18-2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2.dsc' hicolor-icon-theme_0.18-2.dsc 2325 SHA512:737bfba6c257b01f0eb9091d99f21b7592c14410980d5aaa4a1a5c04b942a51eafae84ad1d9e0b642c269ae7ffecafa7af6508063af1b49f00b23f4888d3ce37
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz' hicolor-icon-theme_0.18.orig.tar.xz 29624 SHA512:07db44fb6bec797445740832fa2b3ba56f5f335834161a26a4e5f767a8c45c0885ef1189e887b56752bd20c4b1aac101c5d4a395df4177cd3817ee5105db0d37
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz.asc' hicolor-icon-theme_0.18.orig.tar.xz.asc 833 SHA512:e00447c8918250978622a9465ac16181206deed977743d71faa068341f3aab4a1e98e70aed9f03e62806f2b3d8e1df20ff3b09332d0feda70d4532496154f0c2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2.debian.tar.xz' hicolor-icon-theme_0.18-2.debian.tar.xz 9148 SHA512:2f29cfe942ddbe3cd3ca41006d1ab4e0014368767e6d8ac836ecf19bd7517301a422ee54c8970ee1d8b72b8bd8181aedb8cf4655bb88f6ebcd1903933077a8fb
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

### `dpkg` source package: `imagemagick=8:7.1.2.3+dfsg1-1`

Binary Packages:

- `imagemagick=8:7.1.2.3+dfsg1-1`
- `imagemagick-7-common=8:7.1.2.3+dfsg1-1`
- `imagemagick-7.q16=8:7.1.2.3+dfsg1-1`
- `libmagickcore-7-arch-config:amd64=8:7.1.2.3+dfsg1-1`
- `libmagickcore-7-headers=8:7.1.2.3+dfsg1-1`
- `libmagickcore-7.q16-10:amd64=8:7.1.2.3+dfsg1-1`
- `libmagickcore-7.q16-10-extra:amd64=8:7.1.2.3+dfsg1-1`
- `libmagickcore-7.q16-dev:amd64=8:7.1.2.3+dfsg1-1`
- `libmagickcore-dev=8:7.1.2.3+dfsg1-1`
- `libmagickwand-7-headers=8:7.1.2.3+dfsg1-1`
- `libmagickwand-7.q16-10:amd64=8:7.1.2.3+dfsg1-1`
- `libmagickwand-7.q16-dev:amd64=8:7.1.2.3+dfsg1-1`
- `libmagickwand-dev=8:7.1.2.3+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-7-common/copyright`, `/usr/share/doc/imagemagick-7.q16/copyright`, `/usr/share/doc/libmagickcore-7-arch-config/copyright`, `/usr/share/doc/libmagickcore-7-headers/copyright`, `/usr/share/doc/libmagickcore-7.q16-10/copyright`, `/usr/share/doc/libmagickcore-7.q16-10-extra/copyright`, `/usr/share/doc/libmagickcore-7.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-7-headers/copyright`, `/usr/share/doc/libmagickwand-7.q16-10/copyright`, `/usr/share/doc/libmagickwand-7.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/imagemagick/8:7.1.2.3+dfsg1-1/


### `dpkg` source package: `imath=3.1.12-1ubuntu3`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.12-1ubuntu3`
- `libimath-dev:amd64=3.1.12-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.12-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu3.dsc' imath_3.1.12-1ubuntu3.dsc 2728 SHA512:d63dc15bf0401348cf5b8f3b931d2ef070651076bc092343d9599754c8f5392b7e4ea801db890b7e6176a11de3537dcf825cc10db230feeed34473dce95b1f8a
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz' imath_3.1.12.orig.tar.gz 604232 SHA512:32628dfcacb610310b81ffe017a66215cf5fb84c2e0a6ac8c94a68c048be3d2b97eb57965dd253770184d5824cce1e5440b8eefb2834666b273b3193ff108343
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz.asc' imath_3.1.12.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu3.debian.tar.xz' imath_3.1.12-1ubuntu3.debian.tar.xz 10224 SHA512:a17231679aec8877a0c301068ea46b6c314d61a25c562ef4956f9957a209c72a58cb511733faa6faa204a9f91ff063a5c504df40f820244666fc22ada5e12c3f
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
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1.dsc' isl_0.27-1.dsc 1829 SHA512:1dd37f08556f5adea516dfe737edac400b4aaf394b6e6dcbdc0bc194d96983f9e03523c1ecacb275e28dc415feacf3198376348cb543672ad742c1d6bb51ecc6
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27.orig.tar.xz' isl_0.27.orig.tar.xz 2056436 SHA512:6d6f50c3f6f26e0d3f67586dee6427d87999c426c94069a6f3012ec3c9a41adeebd50f43b5d2705db6abc12e38eb01c19f55dba113c0799da5f667eef46b2be0
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1.debian.tar.xz' isl_0.27-1.debian.tar.xz 24868 SHA512:71f034e81f666ebafa4ec331430fd679643e5d157b094f196c1a1841a0a22f79f46052523c8469ec95b71005e53a82599fe37c08e27b60d5d7f60e94eb50c916
```

### `dpkg` source package: `jansson=2.14-2build3`

Binary Packages:

- `libjansson4:amd64=2.14-2build3`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2build3
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build3.dsc' jansson_2.14-2build3.dsc 1937 SHA512:efd4a1e53db5f253d06f16cf97d8a4388cffc853309f4b6b0a15729c23eb8eda426da1ee9f6af2372f7c2fd38620c2785dcbc4b50620ad9b734aab2e87c24130
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build3.debian.tar.xz' jansson_2.14-2build3.debian.tar.xz 5644 SHA512:707f7934f4dac1b8ce3da883b45a26db8382130dddecdb111da6d25d2235957c49d6649e68b2c4fba7193049240e5c7bc0adf83fd5e88e22d3320fb0c5d0e836
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

### `dpkg` source package: `krb5=1.21.3-5ubuntu2`

Binary Packages:

- `krb5-multidev:amd64=1.21.3-5ubuntu2`
- `libgssapi-krb5-2:amd64=1.21.3-5ubuntu2`
- `libgssrpc4t64:amd64=1.21.3-5ubuntu2`
- `libk5crypto3:amd64=1.21.3-5ubuntu2`
- `libkadm5clnt-mit12:amd64=1.21.3-5ubuntu2`
- `libkadm5srv-mit12:amd64=1.21.3-5ubuntu2`
- `libkdb5-10t64:amd64=1.21.3-5ubuntu2`
- `libkrb5-3:amd64=1.21.3-5ubuntu2`
- `libkrb5-dev:amd64=1.21.3-5ubuntu2`
- `libkrb5support0:amd64=1.21.3-5ubuntu2`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-5ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu2.dsc' krb5_1.21.3-5ubuntu2.dsc 3873 SHA512:aabd71b68ff6c98481fa82c02a78b7bd46315d5ef612a31c2d92dae0926075a009052cd4e7c766c04a6e99d65206e4854f8134a9cd1a065a77056226be01ae83
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA512:87bc06607f4d95ff604169cea22180703a42d667af05f66f1569b8bd592670c42820b335e5c279e8b4f066d1e7da20f1948a1e4def7c5d295c170cbfc7f49c71
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu2.debian.tar.xz' krb5_1.21.3-5ubuntu2.debian.tar.xz 169380 SHA512:3516c768ddd8ea7898ffa576d76c7774d1ddf1e8ccd77e12c219d7e8256318c1703c1f3fadad46f654500abd66f07a129655b79529218a0d3fc45ae77ea4a59b
```

### `dpkg` source package: `lcms2=2.16-2`

Binary Packages:

- `liblcms2-2:amd64=2.16-2`
- `liblcms2-dev:amd64=2.16-2`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lcms2/2.16-2/


### `dpkg` source package: `lerc=4.0.0+ds-5ubuntu1`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-5ubuntu1`
- `liblerc4:amd64=4.0.0+ds-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-5ubuntu1.dsc' lerc_4.0.0+ds-5ubuntu1.dsc 2739 SHA512:3b9c2a8238c78ab2fa82d8a2b0f30a9e627c70eeba450710da1346f14f1e78bece63c6220fa90d1f0eb69455bb5a085d08a66dedd7d59436258e0aad7ab26e7e
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA512:d5539360fa92f40319466fea73a66d0d03aedff886fb75985bfcaeeb77ef516b9fa24b8d83da09c114bf6090bbd68e64d9ac2649a19315895134fa86023478e1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-5ubuntu1.debian.tar.xz' lerc_4.0.0+ds-5ubuntu1.debian.tar.xz 8720 SHA512:82bc4623d2174185c1b82e316aedb1d55815aec0e67f6fd5e6c6b559b2668e23a2edb80dbb6502bca3dd15ef4dc9628767256d2ad7e157002f05c4eb31cc83fa
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


### `dpkg` source package: `libcbor=0.10.2-2ubuntu1`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu1.dsc' libcbor_0.10.2-2ubuntu1.dsc 2275 SHA512:1991707066f3fdeb160e41906b685d21493386c0d2451e792c6233bfa37bd4429b6c64ab24d64dd0752f382823a1089ad352f29101dcf772dcba69ffd700dbd8
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA512:23c6177443778d4b4833ec7ed0d0e639a0d4863372e3a38d772fdce2673eae6d5cb2a31a2a021d1a699082ea53494977c907fd0e94149b97cb23a4b6d039228a
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu1.debian.tar.xz' libcbor_0.10.2-2ubuntu1.debian.tar.xz 7308 SHA512:4105fe0d677f98d28da543995037818c756108cab254244584e669717c5874bda25e073579169d9dbc4075bb5957285c72deaa43c05ecb9a24fef608aca4854b
```

### `dpkg` source package: `libdatrie=0.2.13-4`

Binary Packages:

- `libdatrie1:amd64=0.2.13-4`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-4
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-4.dsc' libdatrie_0.2.13-4.dsc 2239 SHA512:d96e4fef8faacc25c229de91a605853620882ea231aca1f3bade1e67c4f5dce5ff9d6c0677f3c1d1bc0d064960ed957f4671dbd0d584994862032a5e95666893
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA512:db3c879d825ead5871c12ef3a06bb093cb1708a6e7e20775eaf82356af9dd6ad54c6b5cabbe1773f2494d3dfa2426528fdd49441038b6294b70ccb1a3d90099a
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-4.debian.tar.xz' libdatrie_0.2.13-4.debian.tar.xz 10068 SHA512:8cb5491476c00e9f05ad9148d6b056677ff8019a733ecf03011a53bfa4b614a177c9445eca3ddc71892a6505cc637b41b861ada1dc5f9e365a01d701cb7c133b
```

### `dpkg` source package: `libde265=1.0.16-1`

Binary Packages:

- `libde265-0:amd64=1.0.16-1`

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
$ apt-get source -qq --print-uris libde265=1.0.16-1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16-1.dsc' libde265_1.0.16-1.dsc 2246 SHA512:23f62a07b90a0f06ef2516dae6ce702cd2667c3fe3177adf00c3c325ba7ee2ee53e33d93cbaed372421fa084739ceaf15396b851a235c4c26800ce69cfe748f6
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16.orig.tar.gz' libde265_1.0.16.orig.tar.gz 835657 SHA512:07f4dd75238030ed86f1b86d990a5a1c31866d5217db2aa23757432da214a19c5f4094a6c2f8fe3453c64d36ee745ca4f1e22a19a80b2685b6530431a35eb4e1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16-1.debian.tar.xz' libde265_1.0.16-1.debian.tar.xz 136856 SHA512:32f390ab3fc42c5c5fdab23e6eb196433e6f1b34359553e82eb87c48101076479f6eb3c3fad150755f9b1a3711aaee8beeb34c32158442e27abc31f7a8e5cc58
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
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2.dsc' libdeflate_1.23-2.dsc 1743 SHA512:801a2cc0a6ceae6c8803993afb268324938fa63d2204ae2de03507c3465bc71a01799cceef8e73a2bfcac99dc405805e5fc84e8a3e25a25831bed8175364ed44
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA512:c1effb9c5ee8d65bc12ae3d0669a4a394acace13cc146300ed24a7f12a0ec058f66729e1ffbae268711bdcc4151143752ab2d56a099dd6394b2735e8e2f1b671
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2.debian.tar.xz' libdeflate_1.23-2.debian.tar.xz 5624 SHA512:2b3d9fb55fba97b0dbc37b0b2c65554011ba938a189492f3910f9469589c438b18ecf26b6434171db7170da327142b5a8f6f38f9916c114edd0f5eb0d4a5a4ab
```

### `dpkg` source package: `libedit=3.1-20250104-1build1`

Binary Packages:

- `libedit2:amd64=3.1-20250104-1build1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20250104-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20250104-1build1.dsc' libedit_3.1-20250104-1build1.dsc 2288 SHA512:b1b7350ea9c627c8376d45c976ac312a24f21daba0ff653fe725e46adf36096ae2c59150e932b893cde0c9cb6e8b5d06c927987c33a7628501cd6ac5f4133245
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20250104.orig.tar.gz' libedit_3.1-20250104.orig.tar.gz 546745 SHA512:4b4a8b4b1f2cb952bbb3d128605eba9bc7cd0ad35c44b2c099f067c8bea69455bd11faae4ff20384bbe0ea901b25a1249d8323dea4ccd6141a17393f62bb8df2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20250104-1build1.debian.tar.xz' libedit_3.1-20250104-1build1.debian.tar.xz 16784 SHA512:b8fed1c14886a8be6bd91c39a884d4d9104ad790f5c87ba23bef32980b591e2a9de4d66c74e4e814f3995b8388f589e36faec9535c2d3f2fd7f122055f3652ac
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

### `dpkg` source package: `libevent=2.1.12-stable-10build1`

Binary Packages:

- `libevent-2.1-7t64:amd64=2.1.12-stable-10build1`
- `libevent-core-2.1-7t64:amd64=2.1.12-stable-10build1`
- `libevent-dev=2.1.12-stable-10build1`
- `libevent-extra-2.1-7t64:amd64=2.1.12-stable-10build1`
- `libevent-openssl-2.1-7t64:amd64=2.1.12-stable-10build1`
- `libevent-pthreads-2.1-7t64:amd64=2.1.12-stable-10build1`

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
$ apt-get source -qq --print-uris libevent=2.1.12-stable-10build1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10build1.dsc' libevent_2.1.12-stable-10build1.dsc 2436 SHA512:6feef1caa05ef9bf802468c6a900f691499c625879abd7ab540e3c26fd0044f709644129aaf0de185efb0dc7ad785439892c7eb02735fb8f9733f1155a8c602d
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA512:88d8944cd75cbe78bc4e56a6741ca67c017a3686d5349100f1c74f8a68ac0b6410ce64dff160be4a4ba0696ee29540dfed59aaf3c9a02f0c164b00307fcfe84f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10build1.debian.tar.xz' libevent_2.1.12-stable-10build1.debian.tar.xz 17980 SHA512:f0f678b5c68cca560819bbf04358a61a12d6ee298be1690ce314b1610be510c50c56302ca742854523cc36b592d58eecb25fd1c57b291ff21b3149f982ea02b7
```

### `dpkg` source package: `libexif=0.6.25-1`

Binary Packages:

- `libexif-dev:amd64=0.6.25-1`
- `libexif12:amd64=0.6.25-1`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-3-Clause`
- `CC0-1.0`
- `GPL-2`
- `GPL-2.0`
- `LGPL-2.1`
- `LGPL-2.1-or-later`
- `LicenseRef-Wrobel`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.25-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-1.dsc' libexif_0.6.25-1.dsc 2091 SHA512:88aef3e10eeae981c444a91ac6df72ef36746160b6877fbf1a04a2e74e4efd949a5b523958be89e907beec71b7a57e69b78314287a5b5a8d4d2ad9326620b15f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25.orig.tar.gz' libexif_0.6.25.orig.tar.gz 1253324 SHA512:9e42af0d898a9d832d7b146a2085fb08eafdbb5ae476184aee1b495632172749d910f581246d22a0c68382ea9d969de54bd9539d4d877ad4dd6ca989e1b6d8db
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-1.debian.tar.xz' libexif_0.6.25-1.debian.tar.xz 12104 SHA512:6dfe96e1debf860c3aa81bbcdd7a04ae88219702205082e38b38804390b4c7e5ed664ffc68b4c73c3fb29c0535622cddbb26ef071c9efd09c93f9f13ed8cb2b5
```

### `dpkg` source package: `libffi=3.5.2-2`

Binary Packages:

- `libffi-dev:amd64=3.5.2-2`
- `libffi8:amd64=3.5.2-2`

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
$ apt-get source -qq --print-uris libffi=3.5.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-2.dsc' libffi_3.5.2-2.dsc 1954 SHA512:f177aa0cbc74f2bc9882fcbdb716c9b6260205ed1ecaf9a53aeff5bf558b9bb82c112b5b40653e77e81b3d09fb87bab13aa54a84087bab1de75ed453814e8a49
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2.orig.tar.gz' libffi_3.5.2.orig.tar.gz 598870 SHA512:4579932becbe33b2cb3c7a6327a9b47fee67f225ebb4677870ed4402bb7c186966a5b8645dc8a09128af51dcba27c23537e6a34567dbea4e3dc3728cfb51e038
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-2.debian.tar.xz' libffi_3.5.2-2.debian.tar.xz 10916 SHA512:c9de75ed9b29b62e5a1e6d2b87a3a040d3c9c9667c6d1a4ee71f828fea42a3bfdc0e96dc5bdbf9bb75cd35902158acee0ac0f14c9ea6a5a203765b5c0428cb4b
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

### `dpkg` source package: `libheif=1.20.2-2build1`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.20.2-2build1`
- `libheif-plugin-libde265:amd64=1.20.2-2build1`
- `libheif1:amd64=1.20.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `BSL-1.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libheif=1.20.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.20.2-2build1.dsc' libheif_1.20.2-2build1.dsc 3692 SHA512:947f85239989723e2c1b895bd4c2ae14812a4b319c4c78f497b4682fd113f5a4a3028f8728d2e0cbbcadd16e6542ca872544cb50087a75f1f767d8886fc6ae6f
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.20.2.orig.tar.gz' libheif_1.20.2.orig.tar.gz 1787518 SHA512:0ab8669d2ee1ed619c89cbe3fa3a7618c25d26a7e4c65801dd4db163d4a584fde13b32ed0996461e81bd42ed4def8f4eb7b296b15b7819e90c0a7d5a8c08b06b
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.20.2-2build1.debian.tar.xz' libheif_1.20.2-2build1.debian.tar.xz 13800 SHA512:9c62fdb14ef1b98e950cc1c53fbe31c5b0bc3847b884d8fa63a970be7430d1ab103ee447f5ff1f28837c38520399ef256b4db1befe466ef2d22da63c11b00fec
```

### `dpkg` source package: `libice=2:1.1.1-1`

Binary Packages:

- `libice-dev:amd64=2:1.1.1-1`
- `libice6:amd64=2:1.1.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.1.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1-1.dsc' libice_1.1.1-1.dsc 2021 SHA512:a96662e9557995e259d446b7272bc51c26250bbbb0884c2b1fe98d45276ef4ccca08d151b29d6669d6706c24d0978b49d0c75d19d3f5281c5d688a85de7ada98
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1.orig.tar.gz' libice_1.1.1.orig.tar.gz 489944 SHA512:e39fc7f76c19c4edc3e520b7cef16f9f65c4723f4d3603f7e664c54a5fe8fdd756f9a8bb2dc3b0ccf6646a8d1d202cba1cfa220e160b32e233a37c2cc7d13f1d
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1-1.diff.gz' libice_1.1.1-1.diff.gz 7355 SHA512:82b7e1a2049d0bca6d8df3c332f9de348668e144c4028bb376bdcee9b13b140bfcb32a7770bb4487ef81138a62ed1674c55c0611a0a948919af670bb3e02aa86
```

### `dpkg` source package: `libidn2=2.3.8-4`

Binary Packages:

- `libidn2-0:amd64=2.3.8-4`
- `libidn2-dev:amd64=2.3.8-4`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`, `/usr/share/doc/libidn2-dev/copyright`)

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

### `dpkg` source package: `libjpeg-turbo=2.1.5-4ubuntu2`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-4ubuntu2`
- `libjpeg-turbo8-dev:amd64=2.1.5-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`, `/usr/share/doc/libjpeg-turbo8-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.5-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4ubuntu2.dsc' libjpeg-turbo_2.1.5-4ubuntu2.dsc 2523 SHA512:8f34e6d7badb03e9c0dc2deb68f552c60a7ffdc47d956578fb4d6eac7471df7b1f80d1640cf4940cfb35a1b3e6dcfdc0470deae6f8084463ade83f0cc2fcf2ff
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA512:20036303fbe5703a5742dc3778cc5deb2eb98d00a9852e7e80ba73c195bba011ec206c090589c482f1153f74505c3fe06d96af00f6beaa65a7fcf7ffaf626fc2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4ubuntu2.debian.tar.xz' libjpeg-turbo_2.1.5-4ubuntu2.debian.tar.xz 109028 SHA512:9708c3d6fbeba88976618fb61cbece16e7ee3d6e11de2e940d8ec3521ac3d235d8d98005d59c944587f33f9240f6b434d7b64458804d6ea369181596c5439ffc
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

### `dpkg` source package: `libmaxminddb=1.12.2-1build1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.12.2-1build1`
- `libmaxminddb0:amd64=1.12.2-1build1`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `LGPL-3`
- `LGPL-3.0+`

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.12.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1build1.dsc' libmaxminddb_1.12.2-1build1.dsc 2259 SHA512:a9b53587aee8104b2ec0b8983afbb70d3177500af393f166d426b8a7b28565e32157623c5b557d32eb085f5050c126027b3b7c70a1caf1eab140f17b41541815
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2.orig.tar.gz' libmaxminddb_1.12.2.orig.tar.gz 369848 SHA512:88cbccecba2025128babcfb0102f7688982194601974bd3ceaa45ec1bd535e5b6a50c2ce2f214ba5774959987cc64e7f686f76e11672555c690b57a51b1575fa
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1build1.debian.tar.xz' libmaxminddb_1.12.2-1build1.debian.tar.xz 6988 SHA512:018bc37cf8462a86e55b0b258cac75854d98cb6206c04a500db399cbc684ad69c967651405beacf84881017340e82b38a5f316a678bf6aca432e78f542b0204b
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

### `dpkg` source package: `libpng1.6=1.6.50-1`

Binary Packages:

- `libpng-dev:amd64=1.6.50-1`
- `libpng16-16t64:amd64=1.6.50-1`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.50-1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.50-1.dsc' libpng1.6_1.6.50-1.dsc 2254 SHA512:286e2521f1834d640bd3e91775500f44e0cce363e45baa43334ec606fd974888fba3e575df382918257f6e60957571119b177a2f4a98bcbfa84c24091b93c368
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.50.orig.tar.gz' libpng1.6_1.6.50.orig.tar.gz 1582079 SHA512:34c806e0dda960b480ce2f5ea13e2e55a9540f07c51948be25d312b901c431bc814f730f9322a2e3b6f88d4104a0c49bde9e616762b342d07db44e2c7fd5f2dc
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.50-1.debian.tar.xz' libpng1.6_1.6.50-1.debian.tar.xz 33300 SHA512:c31aef43e649f7c060cb153449aea1bcfe0ff048b58ff95dc35ef77edfd011e4d86609742094e1e8cd444c5b8dd4177a21be16aae91e295825905179b2d8f352
```

### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl-dev:amd64=0.21.2-1.1build1`
- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl-dev/copyright`, `/usr/share/doc/libpsl5t64/copyright`)

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

### `dpkg` source package: `libraw=0.21.4-2`

Binary Packages:

- `libraw23t64:amd64=0.21.4-2`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.4-2
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4-2.dsc' libraw_0.21.4-2.dsc 2187 SHA512:fa920e02921a34543f86a5433821165f324f84e58293121da452ca7db48a21739f84a46f5581d0e300e35d8475c88a132384b0345659759dfa71b4d093aef5d7
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4.orig.tar.gz' libraw_0.21.4.orig.tar.gz 566327 SHA512:d8366d62f32f02466128ecfedf9a9b39289834a73d89d57004cf7df63919e66808ba283cddf5843b25fe903d72eb988ac5b490525083e2b5d84a05c7679b4014
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4-2.debian.tar.xz' libraw_0.21.4-2.debian.tar.xz 24312 SHA512:baa743a17360c6acf002d628e1b7a8c8fea3c6d6aaaa160e991f7fbc9252217ac1e0c0d642062b200f2a0e1b27f31bde1fa9a40c915a6a515594fd71f04fb1e6
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
- `libselinux1-dev:amd64=3.8.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

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

- `libsepol-dev:amd64=3.9-2`
- `libsepol2:amd64=3.9-2`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

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

### `dpkg` source package: `libsm=2:1.2.6-1`

Binary Packages:

- `libsm-dev:amd64=2:1.2.6-1`
- `libsm6:amd64=2:1.2.6-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.6-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6-1.dsc' libsm_1.2.6-1.dsc 2302 SHA512:e430e4fc18cc5dec8e39c9ec8634d48f97b2905ded3f768b8f49b6e80da6af571d63bcfb25c8550274a9bc65fb24bdf5747fefdf471c40050d1ecfe69d29d77d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz' libsm_1.2.6.orig.tar.gz 467497 SHA512:316df49f1573ace0bccbfcdf2b1d22c91ec7a1ceb5b320d142fd33cca81e0e0582a0256764aef594f9b31ac5f63d8823dc04c8a6113019ec54ee26eb9323ded4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz.asc' libsm_1.2.6.orig.tar.gz.asc 833 SHA512:b7a617bc09cdc9e4298576f014932165f6b3cc2dd3f96d35db92f46b7f93260705b37f501fbdefb5810eb8f64f64d9260c39cc5ad7660d226b292804798711ee
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6-1.diff.gz' libsm_1.2.6-1.diff.gz 13291 SHA512:bf69da3befddae272ffb2bdf2c893fe7f5dc87b48d903a7939787b2e8f8d4c998428d759a86275dc785fb51ce80d1404ebdbb1db67e2ac6fccf8814035083099
```

### `dpkg` source package: `libssh2=1.11.1-1build1`

Binary Packages:

- `libssh2-1-dev:amd64=1.11.1-1build1`
- `libssh2-1t64:amd64=1.11.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1-dev/copyright`, `/usr/share/doc/libssh2-1t64/copyright`)

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

### `dpkg` source package: `libtasn1-6=4.20.0-2build1`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2build1`
- `libtasn1-6-dev:amd64=4.20.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`, `/usr/share/doc/libtasn1-6-dev/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.20.0-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2build1.dsc' libtasn1-6_4.20.0-2build1.dsc 2689 SHA512:bad3f570158eba6a5ccc7aca64a6ef0db91dd6fc2811b34ce38408a98a6d653a74f020776556056f0e6dbe4c195959636af0f24134a3d1627fc40d560334f923
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz' libtasn1-6_4.20.0.orig.tar.gz 1783873 SHA512:0c0660085f5e80537aa3d65197967029be6cc5e27d7029789713902989c1694fdb49421ae0415b79b953e11893bb4bdaada85f7aff847dd0bb4075c91887e7b4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz.asc' libtasn1-6_4.20.0.orig.tar.gz.asc 1223 SHA512:bb5da128c20ed8f1e7c681c779ac3d2e455c661d779a4a7a70a6cabc1ea4139df9d0acfd145545acc8fe41df6490fd7d3c2df4b8d7560891291abbf56ac3afdb
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2build1.debian.tar.xz' libtasn1-6_4.20.0-2build1.debian.tar.xz 18700 SHA512:55a20d6b49eb49fde2ad47413e98ac7375bd3203f7db2e0d9620b02a908f3765a0b79292326d7838babbb5adbf9b11ba4b8d2eb1f3b2906327390d990c9cf938
```

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

### `dpkg` source package: `libtool=2.5.4-7`

Binary Packages:

- `libltdl-dev:amd64=2.5.4-7`
- `libltdl7:amd64=2.5.4-7`
- `libtool=2.5.4-7`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.5.4-7
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4-7.dsc' libtool_2.5.4-7.dsc 2240 SHA512:5c8460b88a64a3fe61358a2f033e11692f097b05426088fc73b7f74cfaad1c0298832c3939be4861c1ab5a994111636e70ce4c46e6fe829783339cfcbe54f913
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4.orig.tar.xz' libtool_2.5.4.orig.tar.xz 1069572 SHA512:c8ff1fc71373313185ecfff8d282bf3547b8a2d2e102aa4475d7db4945d4f4bfd45cd0d79a8e00a1c1394246908e586f8ccfd9f1cf86ff837b5c6ad7cc57a750
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4-7.debian.tar.xz' libtool_2.5.4-7.debian.tar.xz 37796 SHA512:9bc9fe65647d4c0ef69b68fc7ae75faa1653a8ebeac02127e67761f8c6918326af7dc7a08c705ae62b0ba346fadc2fc05cef5b1a52f7c2a29335cef961e400d6
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

### `dpkg` source package: `libwebp=1.5.0-0.1`

Binary Packages:

- `libsharpyuv-dev:amd64=1.5.0-0.1`
- `libsharpyuv0:amd64=1.5.0-0.1`
- `libwebp-dev:amd64=1.5.0-0.1`
- `libwebp7:amd64=1.5.0-0.1`
- `libwebpdecoder3:amd64=1.5.0-0.1`
- `libwebpdemux2:amd64=1.5.0-0.1`
- `libwebpmux3:amd64=1.5.0-0.1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.5.0-0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0-0.1.dsc' libwebp_1.5.0-0.1.dsc 2865 SHA512:49623160c996f394903114713989e1dcfc79702bfbbb4dd2251b155de86f154d0b2c6f413871fdb6bdb524953887e9814e31db60bead99866e42f5b47ffe3284
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz' libwebp_1.5.0.orig.tar.gz 4267494 SHA512:7a39594cf5585428f82d555b05e78aa63758a56841a313c0b74dfb4996afe37dddf92498d6123ff2a949a7209fb9097927f10ee75b5a38b481f110c892e5302b
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz.asc' libwebp_1.5.0.orig.tar.gz.asc 833 SHA512:892e6240b767d7b47fc4faa337aa78f1426359e155c94305377510b0a0c8a24830597b261ebb458f6310338afde487616bd6cca3347b624d8f46500487a3c067
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0-0.1.debian.tar.xz' libwebp_1.5.0-0.1.debian.tar.xz 11284 SHA512:6f0fd21ea400ecfb4668d6d427a4ab8c50b68bcf6372c3bc7281f385a742c05bbae0062105039016501bf2fab7bfdd9a277ef1dde44ade2625b7cd2122a25d00
```

### `dpkg` source package: `libwmf=0.2.13-2`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-2`
- `libwmf-dev=0.2.13-2`
- `libwmflite-0.2-7:amd64=0.2.13-2`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-2
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-2.dsc' libwmf_0.2.13-2.dsc 2368 SHA512:b683d69f0921cd71b1583dc5e275bc7617c4921dbf0cd5dc07516d097daa7feaeee136a1290c55ebf40b2afd5a116fcd1089b56c2045579c1a415fec55a5b0bd
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA512:f45a936c9bc98fc1a5f2b0808b497119e4dcd3c132615fdddb7583e5719c7d1d7f85c16ebf313cad453e5b7ae3508bf6b80c4ed2b42322b7dec295d8f4eb86ce
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-2.debian.tar.xz' libwmf_0.2.13-2.debian.tar.xz 25572 SHA512:d8b7a3bd1ca33896637f45eabcea4e58d2ce3ecd6397ab1b6b32507c5d268e54be304178943c701bdd8d799962597e0d50d275f3a5c82649a116a0037c4bd099
```

### `dpkg` source package: `libx11=2:1.8.12-1build1`

Binary Packages:

- `libx11-6:amd64=2:1.8.12-1build1`
- `libx11-data=2:1.8.12-1build1`
- `libx11-dev:amd64=2:1.8.12-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.12-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12-1build1.dsc' libx11_1.8.12-1build1.dsc 2514 SHA512:e7a0f289b8104e63662b44590673293d5dea0096d1781d221699c39b5d190830fcabb7dce7dbf32476dde8cc114a434fa0537bb9d0c3f7a6b68191dfe0fde02c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz' libx11_1.8.12.orig.tar.gz 3215077 SHA512:82d62d01176bbb8ee225f6dba741dcbccded62486ae4c70bc7158aa2a19dcf4a795ee9d475a875ed8843a4ae185eb4899d06dac4000b5fe8b5bbb5e13b450153
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz.asc' libx11_1.8.12.orig.tar.gz.asc 833 SHA512:37b5f57a55cb75cb218937175ad06752ab85391c23ac91006a19fe32b82fc86f4b5eca11dba9b38c7d38efbf98aba3eeadcf3cf7bddf11175334ebe8e4d94d23
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12-1build1.diff.gz' libx11_1.8.12-1build1.diff.gz 74565 SHA512:f1ce092475fd7063bbeb2015a2027da7f884b3563a5dacf4879689676fce54509f49cc3b09139aad0b778330cc899e88cfbe159336145cda9be452064830d29d
```

### `dpkg` source package: `libxau=1:1.0.11-1build1`

Binary Packages:

- `libxau-dev:amd64=1:1.0.11-1build1`
- `libxau6:amd64=1:1.0.11-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.11-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11-1build1.dsc' libxau_1.0.11-1build1.dsc 2208 SHA512:e383110de739531309b6ffa17dd467a0fc04f0bb34369fdbd1825f9c74dd3e163592ea87ac3084ab1cdfab8f11c3a21f9ad488ac1bd4f68db35896085b74d5b1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz' libxau_1.0.11.orig.tar.gz 404973 SHA512:315625ae6657e817c09c83da53029488bd5140bc1048eef1072b12958457fdec6c41f79b190cf10885559d2e4c7d47110cd08369b438ca47749790c51edd8492
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz.asc' libxau_1.0.11.orig.tar.gz.asc 358 SHA512:97e4425f90e720800cf91f45cf3dcb92b88017cba0db6fa4e39978ad8871b7312a048f4b51622176488edfb5b620ba0d6f0ffd087f0b177f9abfe3d8854fab30
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11-1build1.diff.gz' libxau_1.0.11-1build1.diff.gz 22792 SHA512:4e5dd8c8ba5d570cc2512a93841998b363185176339a295667778be758365ddaf31a71cbd576e09d5e3f426ce18169d3e9cbfa060a49cc3c1808d25f391eb39c
```

### `dpkg` source package: `libxcb=1.17.0-2build1`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2build1`
- `libxcb-shm0:amd64=1.17.0-2build1`
- `libxcb1:amd64=1.17.0-2build1`
- `libxcb1-dev:amd64=1.17.0-2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2build1.dsc' libxcb_1.17.0-2build1.dsc 5342 SHA512:b5699ae99bea4417bbe0a782d0baeadd37eaf884849f445e599f7f2aee2df82eabb9f6f9d8277173cbf89983ca13d72832d683690955b7214ab3814a6211368d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA512:58624a33d39371a7ff58368ed5a09c1c31bea3abd040173db1d41018de4208bc52d2fb8cfd7382ff34d01b98d01a3e314a71a808533880564cd51cd96624a7bb
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2build1.diff.gz' libxcb_1.17.0-2build1.diff.gz 28164 SHA512:9418678258175fe3159f983df25bafbb23224b986ff6ae201f165267beb2d0c99bf41956e7142746f4d76c9d3009a82539b0465ffb5fcf5b9856e9ff20b08c62
```

### `dpkg` source package: `libxcrypt=1:4.4.38-1build1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.38-1build1`
- `libcrypt1:amd64=1:4.4.38-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxdmcp=1:1.1.5-1build1`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.5-1build1`
- `libxdmcp6:amd64=1:1.1.5-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1build1.dsc' libxdmcp_1.1.5-1build1.dsc 2326 SHA512:00a19c645a5c65402ed85c30709cc852a87cbfa82b61564fff82629a46ca2c9cdb814cf6d604ba34f54fb3527c1110c0dc0ecd2494b1479fc51bfe4c7c54706d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz' libxdmcp_1.1.5.orig.tar.gz 442597 SHA512:400add8f47c28fe9cb80d6159a7268e7f5029d13a6219f3e07087455d99f807aa5b372242be9c14fbb7164b3c8180b8dc5edfeb620412bcbee246162f53c61d3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz.asc' libxdmcp_1.1.5.orig.tar.gz.asc 833 SHA512:e44c62904e5680ede9c3188c2fcf8e453c09d5f89e2958be34196e6f1130177f2e7bbd324337b5ee1902817c09357be0144dd91c2b6fd4e943edebe532c5193c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1build1.diff.gz' libxdmcp_1.1.5-1build1.diff.gz 9956 SHA512:18dcfe4a56b11a13f47d6376481d3e38c0724d5c8e89eb92c3594dd6e39dcb26295453cd100c0e874b0e10f0df32c1ea42c1cc0b9cc9a63be02475d06a671495
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

### `dpkg` source package: `libxml2=2.15.1+dfsg-0.3`

Binary Packages:

- `libxml2-16:amd64=2.15.1+dfsg-0.3`
- `libxml2-dev:amd64=2.15.1+dfsg-0.3`

Licenses: (parsed from: `/usr/share/doc/libxml2-16/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxml2/2.15.1+dfsg-0.3/


### `dpkg` source package: `libxrender=1:0.9.12-1`

Binary Packages:

- `libxrender1:amd64=1:0.9.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.12-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12-1.dsc' libxrender_0.9.12-1.dsc 2258 SHA512:b8b744c8946fffcaf089dcfe8001a52be38efd3f19bfc87a4d2d454913ad0c8059d83d336de8ccbdd7c7bc92f28981289f63f77c70dfd537d31d7373200c2886
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz' libxrender_0.9.12.orig.tar.gz 450034 SHA512:b7cbe8ead3a4eeb7c42acede8569361cf11818d98d05ede75a5f0c48c3fb6b1c0b3b62bb2ba6aea19b4804938512e63ebed127928b1a553b518e3ab974bd089d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz.asc' libxrender_0.9.12.orig.tar.gz.asc 833 SHA512:299b2654f2bd2b51033072a225a42f75b5e16aff65f6ff171defe9f692f95f69fbcda0b121caf7f4706ee0dd5f9ecef9b2d2ff50a729d40b280fbdeb80ff17cf
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12-1.diff.gz' libxrender_0.9.12-1.diff.gz 21464 SHA512:91501f3b9bd7a6e2ae0f6038fa7b4e0ac036dcd9c0e58e4f2dbe2a8b7730a54eb506e61727a2822c7008a3693a1fe0dac107937cc79ea31c611fe2ada7198a10
```

### `dpkg` source package: `libxslt=1.1.43-0.3`

Binary Packages:

- `libxslt1-dev:amd64=1.1.43-0.3`
- `libxslt1.1:amd64=1.1.43-0.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.43-0.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43-0.3.dsc' libxslt_1.1.43-0.3.dsc 2183 SHA512:988e63062b3b0ccfa76e5c54b87256da9a5cf5fcec2d024dd4765d429600e7b198045e5c2804c4c2128d60de4f2e72a4ad59b1d89888efe50eef190753546609
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43.orig.tar.xz' libxslt_1.1.43.orig.tar.xz 1518364 SHA512:96110b0397a8f5791f489127574e2143845feb61bea0581d7b7e3c1101fd0718483bae81a7ce417b971bd678293bfd95daddad0dadd3e256c87d41a69faed85a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43-0.3.debian.tar.xz' libxslt_1.1.43-0.3.debian.tar.xz 27452 SHA512:644ae78884010fd2cf29505c9a3f5c45bc0b6800b2ab04be3e60ef9862e150c6dfa8af5955abaedfc3b6078d306a1773514c38c6afe206ccf0ddbbe3d00295b1
```

### `dpkg` source package: `libxt=1:1.2.1-1.3`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.3`
- `libxt6t64:amd64=1:1.2.1-1.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.3.dsc' libxt_1.2.1-1.3.dsc 2359 SHA512:7dcadb318ab382b0af8e8b1406afae48249bc0ca4f490568a4929166091ef3106239027c1e6f3abe1a7a2464fcf65e4060225f0131f2dd54132f7b8f47ced884
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA512:73c2fd8a6590ab5ee93cf646e4f41fb71d424961ecbf9bc13c68abdf539c63ab0c59a4d3b22195ba21859523f4cf0e937648424532794a1350a5891061096503
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA512:135e01b8a79beac9530087dee1a5458c359b4f1ae8346e2502f72f4fc24be400477fda90944315c585e3416e80cb74d1a140d5dfec81e854a4996199a8b221dc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.3.diff.gz' libxt_1.2.1-1.3.diff.gz 46408 SHA512:427103983c1df7f82c4eeb845376a0f5ef547235e811c5b68fe8a9c83729207841a8ecf09b07afbb090d28235f19e6011e9148ec814523da2508ab6f1577b21e
```

### `dpkg` source package: `libyaml=0.2.5-2build2`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-2build2`
- `libyaml-dev:amd64=0.2.5-2build2`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2build2.dsc' libyaml_0.2.5-2build2.dsc 2064 SHA512:c8e1c8a965740c00c870dbc774722c5ad493a50d779031da73e3eb61bcf1028c3cfcd78538af5abbc774181cdd2a33fa8c385e4bafdd2fb0daf4c01b4d3d62a5
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA512:a0f01e3fc616b65b18a4aa17692ee8ea1a84dc6387d1cf02ac7ef7ab7f46b9744c2aac0a047ff69d6c2da1d2a2d7b355c877da0db57e34d95cd4f37213ab6e7e
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2build2.debian.tar.xz' libyaml_0.2.5-2build2.debian.tar.xz 5788 SHA512:9418ef05afc122f5245f1cd0e9ddfbc39c61ee4adac2037ae0728ca4a37eaa8d9ce3057ec29bfc7d80d81c6925330d6e46e3c817c2b0f5d73c870e4275c5631e
```

### `dpkg` source package: `libzstd=1.5.7+dfsg-2`

Binary Packages:

- `libzstd-dev:amd64=1.5.7+dfsg-2`
- `libzstd1:amd64=1.5.7+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

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

### `dpkg` source package: `linux=6.17.0-5.5`

Binary Packages:

- `linux-libc-dev:amd64=6.17.0-5.5`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=6.17.0-5.5
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.17.0-5.5.dsc' linux_6.17.0-5.5.dsc 8462 SHA512:c5f4b0119ef586b71ae33687756dd155f789a947a9dc8dc54193d0315f94ff27f1b28554f24c3716d93de418c3ab4f9f2dc5f15d9dce55fbed20993aa6244976
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.17.0-5.5.tar.gz' linux_6.17.0-5.5.tar.gz 257708484 SHA512:c1a472a72bfea9ac56e9fe79dfc8395283c5c3091a2de1d27f647878b2b35bf20ec12c9fdc56ad3fb1fad43478ada93166b848f2657e151bcd85048893fb0f6c
```

### `dpkg` source package: `lto-disabled-list=72`

Binary Packages:

- `lto-disabled-list=72`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lto-disabled-list=72
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_72.dsc' lto-disabled-list_72.dsc 1466 SHA512:c8f1e8ea0654cdc89821bc2b16dc677ee2e811fad0ea9145dfaf205a5013aade8165246b6c0cee3ae8a7c8892184273e3a2ed080ce26f0aef857f627d9570e81
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_72.tar.xz' lto-disabled-list_72.tar.xz 14308 SHA512:aea27b5b00485521aafc537795fc9b5ace2a842de26d02d32839a149fe4ada94df2c5571aff7a7b95270e5cee60e073b4735183dfaa6830eb58022945f321ee8
```

### `dpkg` source package: `lz4=1.10.0-4build1`

Binary Packages:

- `liblz4-1:amd64=1.10.0-4build1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `m4=1.4.20-2`

Binary Packages:

- `m4=1.4.20-2`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.20-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.20-2.dsc' m4_1.4.20-2.dsc 1783 SHA512:8adf4e06be8faacb0253c098b581f04b2b69fd1358f5b73f98952ebab00b2fb082bcec4c571f5e4f8786ab7d17254488657bedc1d97d30cecd8b63b9cdf95bd6
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.20.orig.tar.xz' m4_1.4.20.orig.tar.xz 2044756 SHA512:dc7b4f61452e564b095010029bf6ce4246e5a03959989cd76b09eb8012db7424c52819143020fab21a3471ff57ab026d3eccbd00dd3969819208980565a9fec0
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.20.orig.tar.xz.asc' m4_1.4.20.orig.tar.xz.asc 488 SHA512:bc75a64e47a87fe4073f26850a8344e82d15f156ac5b52cde1af701a0ba4e0d18f414323f86c868f114c4867b00c31ce205a9505343e588ad97825b05136c5eb
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.20-2.debian.tar.xz' m4_1.4.20-2.debian.tar.xz 17608 SHA512:2599d01caffb3de03397a8be5e5912bb6eed4a02fdfdb015eb97cf62a16370c6ff941ef96b782f6e934623d100c426cabee2b645c1e645e13a7be1b1eb6da0f9
```

### `dpkg` source package: `make-dfsg=4.4.1-2`

Binary Packages:

- `make=4.4.1-2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.4.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.dsc' make-dfsg_4.4.1-2.dsc 1976 SHA512:7b9ea0aeda776b1724c74b0aa2857d3effda31b029a7b47a9d77a509ef33185d72d61827eb2e2bc81170f2172bd961e60379e30b5d1382859aee8181339f0685
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA512:7efa533e7c85e0f394d2a9c422c1cf854f304871f0c692ff74eac18597fa53d1a79b41ba1c56b88d8c79f2e6dfb8c3c3ba8640af15756f455167d62e7ed7b04c
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.debian.tar.xz' make-dfsg_4.4.1-2.debian.tar.xz 44088 SHA512:dd9442a94e3cd75ec0f2cc3f2f349fd34c25a0ba1dd5e24a62f5778b5002d9b7a4768578b9f814266fceb51b69726c9d37d33f66f3d7f3effca9d1ec786e187f
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

### `dpkg` source package: `media-types=14.0.0`

Binary Packages:

- `media-types=14.0.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=14.0.0
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_14.0.0.dsc' media-types_14.0.0.dsc 1917 SHA512:542529bde4bee8b26d8f2941ca68ff202ac62353d378be6b78f15339dde1344a76e2f0c48b520471c3a5d07c2e1fa236abad67d38510749ea9c164554651ce7f
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_14.0.0.tar.xz' media-types_14.0.0.tar.xz 65204 SHA512:a1a973ea115068718fc3b6c57d33c6ad0c7db99b2fa32b4d789e51b80006b4ac2d685926ecc070e6b2a17c53e16c03a51a58e23323aa5e46975d535ab1eceef8
```

### `dpkg` source package: `mercurial=7.0.1-2`

Binary Packages:

- `mercurial=7.0.1-2`
- `mercurial-common=7.0.1-2`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=7.0.1-2
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1-2.dsc' mercurial_7.0.1-2.dsc 2881 SHA512:9c09f0df68a4eb043866ab2eb44cb33a79786fc104940bc251db2a2ab790b7e40457c2b5bebd9e2576c78e8d8bca40fa1e12da0c237d82c236f32b78fdcc70f8
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1.orig.tar.gz' mercurial_7.0.1.orig.tar.gz 8981165 SHA512:42abab36e17c2edee2dc715a1af684540b21ab2fc7058335e5a166db90c36f9217dc15bf94daeaf45e7ac725f1fc849bf0ec54d06e9fa307a041f34d768a8fb3
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1.orig.tar.gz.asc' mercurial_7.0.1.orig.tar.gz.asc 833 SHA512:74d47f413c4038cbfa4377f2177e26df0cc26795fd55fbc25a9b2e64005591b0e1646bd9778e6c6978004b0f9d37a828ecb9fab62f07bd581236826fa08d1dce
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1-2.debian.tar.xz' mercurial_7.0.1-2.debian.tar.xz 55672 SHA512:cea247268a72c2f47ad9f14bebe2941f9be2450ebf4e4a23d4c769617bc4458bc95ddf3500b87751839b907f6adf007645f83c33edb23e00973484dc032c9700
```

### `dpkg` source package: `mpclib3=1.3.1-2`

Binary Packages:

- `libmpc3:amd64=1.3.1-2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-2.dsc' mpclib3_1.3.1-2.dsc 1919 SHA512:72c0899f4380c63f7e00a94d7a3a018bd865775de903c9f7fc604d468563950338babba7675bb83a6b29bb02344616c83907b110985b3b68c299c4e912195b5f
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA512:4bab4ef6076f8c5dfdc99d810b51108ced61ea2942ba0c1c932d624360a5473df20d32b300fc76f2ba4aa2a97e1f275c9fd494a1ba9f07c4cb2ad7ceaeb1ae97
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-2.debian.tar.xz' mpclib3_1.3.1-2.debian.tar.xz 4628 SHA512:4cdefaa458efdbde8b48d42754446e348600f8320b2c0ade917441fabd46b01ac0872be18b7823e1326c4d9e2eee6a94a5338b14dee91862ec93076335bda42c
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
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2-2.dsc' mpfr4_4.2.2-2.dsc 2007 SHA512:8c723709afc9dc8c5f6f15c390c2e2abf9c76a269425b78360c2821db8719f5cfb7b768f1e51be7e6e6919e8f8531caeea3deb53ceb4f0c3383860b8b8fc7b32
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2.orig.tar.xz' mpfr4_4.2.2.orig.tar.xz 1505596 SHA512:eb9e7f51b5385fb349cc4fba3a45ffdf0dd53be6dfc74932dc01258158a10514667960c530c47dd9dfc5aa18be2bd94859d80499844c5713710581e6ac6259a9
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2-2.debian.tar.xz' mpfr4_4.2.2-2.debian.tar.xz 12616 SHA512:753266814daf020c393b4a40e2225c482855e21a49427622c9b785a8bbc0cb4e6408ab8d66c78427fa5c1ff953f7883a7aee8e156cd1fae6f69ae6fcf15c36f3
```

### `dpkg` source package: `mysql-8.4=8.4.7-0ubuntu2`

Binary Packages:

- `libmysqlclient-dev=8.4.7-0ubuntu2`
- `libmysqlclient24:amd64=8.4.7-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libmysqlclient-dev/copyright`, `/usr/share/doc/libmysqlclient24/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Boost-1.0`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `public-domain`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris mysql-8.4=8.4.7-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.7-0ubuntu2.dsc' mysql-8.4_8.4.7-0ubuntu2.dsc 3801 SHA512:2c61cb17114bf4ccdcc2e62179a21c45369b6b4871b142c9968927dc115baa7e03cc218b978a5f126987570bf0b533f6fa95940c3423bfd0205d4d66e7bf089f
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.7.orig.tar.gz' mysql-8.4_8.4.7.orig.tar.gz 478948308 SHA512:d9596395b176490d5e58be307c2f82f55c9acd3206c1ba29bdb8c96c67438bbe5594621f601161ccb77f56c8262d00255ab6fd8aa62db61c80a1721e3d4e45a2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.7.orig.tar.gz.asc' mysql-8.4_8.4.7.orig.tar.gz.asc 833 SHA512:51c22eef6e3611da0ce524784844339063ffabb378f0069e7abccee95a16cd8b9cc248b9eff1622adce6cb625322837b93f44fbd5668d18c79b0fd6875032798
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.7-0ubuntu2.debian.tar.xz' mysql-8.4_8.4.7-0ubuntu2.debian.tar.xz 135752 SHA512:d59d74cab353389d6cbbf6f52b8a8c2e7ca8b6bb1c8887e3fd3e3d73ffd53150fadf4722855c2783c11bf5b1bbb111a93bc85591c069d7b6b791f96adb6d5ceb
```

### `dpkg` source package: `mysql-defaults=1.1.1ubuntu1`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.1ubuntu1`
- `mysql-common=5.8+1.1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1ubuntu1.dsc' mysql-defaults_1.1.1ubuntu1.dsc 2346 SHA512:77e64232d994672d6faf8fede229f910b25255dc9a0b85272b6de36a64b3a295ed5649d7b2c0f7e1206da309c2f36176fa2a21c51ce4b57180901074fcf9024a
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1ubuntu1.tar.xz' mysql-defaults_1.1.1ubuntu1.tar.xz 7568 SHA512:8b0e5a51716845bcfa1f922f41ca83677c07587b0a14335e8251317406a14d53c126e9fefb6d5ac531bd27057533b869287b1d862ad95d277cfc57e0e131631c
```

### `dpkg` source package: `ncurses=6.5+20250216-2build1`

Binary Packages:

- `libncurses-dev:amd64=6.5+20250216-2build1`
- `libncurses6:amd64=6.5+20250216-2build1`
- `libncursesw6:amd64=6.5+20250216-2build1`
- `libtinfo6:amd64=6.5+20250216-2build1`
- `ncurses-base=6.5+20250216-2build1`
- `ncurses-bin=6.5+20250216-2build1`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

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
- `nettle-dev:amd64=3.10.2-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed6t64/copyright`, `/usr/share/doc/libnettle8t64/copyright`, `/usr/share/doc/nettle-dev/copyright`)

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
- `libnghttp2-dev:amd64=1.64.0-1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`, `/usr/share/doc/libnghttp2-dev/copyright`)

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

### `dpkg` source package: `openexr=3.1.13-2`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.13-2`
- `libopenexr-dev=3.1.13-2`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.13-2
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13-2.dsc' openexr_3.1.13-2.dsc 2144 SHA512:b6fb1b31c486856cb1df6b563adb672739e14d83c8ee02a00fa9ff054b4b7ade2109e6ef69231888b75a043b09a5ce522afdf0805181155a0a552427777eaca7
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13.orig.tar.gz' openexr_3.1.13.orig.tar.gz 20542408 SHA512:662ebfce32bc56e3b5140e7d1813b8c117ac6e806fe30c996b956465ce20ee43f1f535b97868a87a26d1d7909d7f59acbe383f335ab8d72ad1484408cbabf77b
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13-2.debian.tar.xz' openexr_3.1.13-2.debian.tar.xz 19268 SHA512:15bf6e5ac0acabe728ba2ef5c6f962be82ac410ab3fa882bb5f9adaa8b11c9ea6d0366f0eb590c47609fc08f444289a9585b04fdfd85f2f4c8417167ba3d0ab3
```

### `dpkg` source package: `openjpeg2=2.5.3-2.1`

Binary Packages:

- `libopenjp2-7:amd64=2.5.3-2.1`
- `libopenjp2-7-dev:amd64=2.5.3-2.1`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.3-2.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.3-2.1.dsc' openjpeg2_2.5.3-2.1.dsc 2571 SHA512:424df8f01abbc46082eb289c7b3c1af8fa75841c072d6ba96624844fc8e12519db7f346ddd8f26f22d02f886bb279353d686798c22e69f4c1b7f595bab6f0642
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.3.orig.tar.xz' openjpeg2_2.5.3.orig.tar.xz 1393716 SHA512:aae4bf4d677a5c8395886b6ab051ffccb9d7bc0de2f4df44932296ab54ef3d936ac4848856ed6011dfb77c349e3383766634bf3e2244c2cf2c42aff55b98471b
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.3-2.1.debian.tar.xz' openjpeg2_2.5.3-2.1.debian.tar.xz 15688 SHA512:4af7b0fb7b28acad335c4dbb40dd0bd17c2e30df3d6ef9cd31089c88ce83c197b218251398f7f17425e03036d2c0cf0e6962e6f8e7b3a49c6cbc9b37fef751a0
```

### `dpkg` source package: `openldap=2.6.10+dfsg-1ubuntu2`

Binary Packages:

- `libldap-common=2.6.10+dfsg-1ubuntu2`
- `libldap-dev:amd64=2.6.10+dfsg-1ubuntu2`
- `libldap2:amd64=2.6.10+dfsg-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libldap-common/copyright`, `/usr/share/doc/libldap-dev/copyright`, `/usr/share/doc/libldap2/copyright`)

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
$ apt-get source -qq --print-uris openldap=2.6.10+dfsg-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1ubuntu2.dsc' openldap_2.6.10+dfsg-1ubuntu2.dsc 3384 SHA512:085c9bc20ca2fef3bd3979420eba2553dfa61fda8fb636129b365febffaffd5a7c361fb6209be1c194b1c5105bd848aa14d917a69819d6fcf0ff2d722de02d4c
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA512:9c24cab12ea4002560670d1a6053c00582aea1713e3db262bbf5aae7666c6d50ef28e7b59ca4dbe5c5b5903e56268911a935a58ef852239c259830458e804f62
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1ubuntu2.debian.tar.xz' openldap_2.6.10+dfsg-1ubuntu2.debian.tar.xz 184436 SHA512:f21e268a12723adb55102d6cf0f1bee86b8c1f5b4aa8b8614a29a0980afed8fb5ea6aed65fc56d09be8ffeda70a97f5396dcd9090a9dc526e69a9608f21ee70c
```

### `dpkg` source package: `openssh=1:10.0p1-5ubuntu5`

Binary Packages:

- `openssh-client=1:10.0p1-5ubuntu5`

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
$ apt-get source -qq --print-uris openssh=1:10.0p1-5ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1-5ubuntu5.dsc' openssh_10.0p1-5ubuntu5.dsc 3499 SHA512:24b62c83391248d4e263df21f4f72b4f4167098189f27be52d4b5335d34fbefe9522fb15e1c992af9adc545fcf51563bad6844d636433321df1cd495c1a5a457
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1.orig.tar.gz' openssh_10.0p1.orig.tar.gz 1972675 SHA512:2daa1fcf95793b23810142077e68ddfabdf3732b207ef4f033a027f72d733d0e9bcdb6f757e7f3a5934b972de05bfaae3baae381cfc7a400cd8ab4d4e277a0ed
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1.orig.tar.gz.asc' openssh_10.0p1.orig.tar.gz.asc 833 SHA512:6ab9deb4233ff159e55a18c9fc07d5ff8a41723dad74aa3d803e1476b585f5662aba34f8a7a1f5fe1d248f3ff3cd663f2c2fb8e399c6a4723b6215b0eb423d13
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1-5ubuntu5.debian.tar.xz' openssh_10.0p1-5ubuntu5.debian.tar.xz 214060 SHA512:d3d6f3e9d342c0a87cac1c94f7425e58b3673ef73ecbefeabf9731fd7c4ae9e101f99f5ce357df5c2f122b48df3c1a0c5938b166f9688b19b872b8a48548824c
```

### `dpkg` source package: `openssl=3.5.3-1ubuntu2`

Binary Packages:

- `libssl-dev:amd64=3.5.3-1ubuntu2`
- `libssl3t64:amd64=3.5.3-1ubuntu2`
- `openssl=3.5.3-1ubuntu2`
- `openssl-provider-legacy=3.5.3-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

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

### `dpkg` source package: `p11-kit=0.25.9-2`

Binary Packages:

- `libp11-kit-dev:amd64=0.25.9-2`
- `libp11-kit0:amd64=0.25.9-2`

Licenses: (parsed from: `/usr/share/doc/libp11-kit-dev/copyright`, `/usr/share/doc/libp11-kit0/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/p11-kit/0.25.9-2/


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

### `dpkg` source package: `pango1.0=1.56.3-2`

Binary Packages:

- `libpango-1.0-0:amd64=1.56.3-2`
- `libpangocairo-1.0-0:amd64=1.56.3-2`
- `libpangoft2-1.0-0:amd64=1.56.3-2`

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
$ apt-get source -qq --print-uris pango1.0=1.56.3-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.3-2.dsc' pango1.0_1.56.3-2.dsc 3692 SHA512:45c17eadf20d4d4e74cc59c5956faa92a645a667ac8952570d0b9c26ad5d6667a2300d126f581a7fadfbac520ee7438da3a26f819432b0dbb4dadd634e6d09a1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.3.orig.tar.xz' pango1.0_1.56.3.orig.tar.xz 1883584 SHA512:adb5aa66ea0c45f7bb112867a77f25d31d39bbb18fd8d41df0c1fd329714def874aa3cb8a49847561a75b0824c2abf8ce09a610d088e88d7de015c36a1536ac0
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.3-2.debian.tar.xz' pango1.0_1.56.3-2.debian.tar.xz 44136 SHA512:094b2b282bdef266075ed43764a539211220600deb9dcff1c10852783433bb83221d4bcb1fcf5d325a12e4a3f235344b06e222798d71bf8733b2c1a96a6254c3
```

### `dpkg` source package: `patch=2.8-2`

Binary Packages:

- `patch=2.8-2`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris patch=2.8-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2.dsc' patch_2.8-2.dsc 1689 SHA512:cf43a4b896395c4dfe05ae87636a18c47f34c4d149029c19ae2826f700254eb484f760ff41c793b7eb066e1b91e097d3dd2e40636f47a6efd6cbfa3df7f49565
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8.orig.tar.xz' patch_2.8.orig.tar.xz 907208 SHA512:d689d696660a662753e8660792733c3be0a94c76abfe7a28b0f9f70300c3a42d6437d081553a59bfde6e1b0d5ee13ed89be48d0b00b6da2cadbfc14a15ada603
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2.debian.tar.xz' patch_2.8-2.debian.tar.xz 9460 SHA512:3881b0cbd510932ee06ecb5ba85786d44f1ea7336ad8bd1ebd23d0e0ff1db2c589111781a9565388296b46985303d5c4102953b12a9d0035500e4554d0ed8bcd
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

### `dpkg` source package: `pixman=0.46.4-1`

Binary Packages:

- `libpixman-1-0:amd64=0.46.4-1`

Licenses: (parsed from: `/usr/share/doc/libpixman-1-0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris pixman=0.46.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.46.4-1.dsc' pixman_0.46.4-1.dsc 2019 SHA512:9c059227bf84e62d4f6419406f7ea1c6b5e8a0a2dc9ace4c8ecbbc272b568ea9965c402508a7356747645bd98758fbd51488481fbd2151265e46eb20dd621fd7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.46.4.orig.tar.gz' pixman_0.46.4.orig.tar.gz 827198 SHA512:10ddb88b51f5456c440d77a7b4230600b099e818378a9b55f715bbe5ec3d9f1e9da2124d28a2bd3377f1ab20af87e0ec4fa9dadaa20a2f1f880dd2dc7f27ca6c
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.46.4-1.diff.gz' pixman_0.46.4-1.diff.gz 9639 SHA512:df40dca4e3663782f5431f1dfb4087fa659003bdf0ba3daa7fc527acf9bff03dabdb37cc7498e0b920c318714f1c42c2791b6281af8f2b3fac21cfd8602d2eae
```

### `dpkg` source package: `pkgconf=1.8.1-4build1`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-4build1`
- `pkgconf:amd64=1.8.1-4build1`
- `pkgconf-bin=1.8.1-4build1`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-4build1.dsc' pkgconf_1.8.1-4build1.dsc 2154 SHA512:9ef1f0bd26e6f3b8d1dc30d8709a96c25edc0c4f38979d33c5dfb769929f923eba53901ab87236510b3b355696c3291ac66e1305b3234f71a5b18d25a9fc4b83
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA512:7a7d5204c1c9bfb6578bda56f299d1fa0300e69a133a65730b10ad77aefbf26fceb74ae77cecda326b3ed5db5736f27fcce94764b3a56d40f4bb99fecdc80bba
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-4build1.debian.tar.xz' pkgconf_1.8.1-4build1.debian.tar.xz 17804 SHA512:72ed87055ac67f5dc74547cee6a81a3f3f19a498dbe17b0c5b744060723ed5f00963f56e088176449fbca4f003531596edfc8bfd9fadf2bc380c5e9400e84b6c
```

### `dpkg` source package: `postgresql-18=18.0-1`

Binary Packages:

- `libpq-dev=18.0-1`
- `libpq5:amd64=18.0-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/postgresql-18/18.0-1/


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

### `dpkg` source package: `python-packaging=25.0-1`

Binary Packages:

- `python3-packaging=25.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=25.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0-1.dsc' python-packaging_25.0-1.dsc 1674 SHA512:2327d61477f19538c65e214f809986e57e6696eb043dace1d0193398ff1584f3ec46ad98c2abe56602a87ac1149fb007cddad9990c17c38b38406bf4f7b0b331
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0.orig.tar.gz' python-packaging_25.0.orig.tar.gz 165727 SHA512:0672602d2e18c3aee71b3e567b0de572bc8613ee3d24a79a655ded23ac08ec4582193225bc0c0ea390ed81cf5efbb46e8afbe0798d14f2235f811f263c25728c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0-1.debian.tar.xz' python-packaging_25.0-1.debian.tar.xz 4144 SHA512:afcbcf5e090922e7e9935b41397056566c93180d4425d5c6d9a5eebc2c1c3d86c355cdc1189316c34fdb2343a6781d5634680425229aafb50e2c32434b7b562a
```

### `dpkg` source package: `python3-defaults=3.13.7-1`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.7-1`
- `python3=3.13.7-1`
- `python3-minimal=3.13.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.13.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.7-1.dsc' python3-defaults_3.13.7-1.dsc 2346 SHA512:d224c5ced2a34850c186f17b5d4ede11214507ba5135841ca3ecde9c2b891dbeba06a1e844a205fc039d214cec3a430138786d1a80f931993d17b30e279a5bbe
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.7-1.tar.gz' python3-defaults_3.13.7-1.tar.gz 146793 SHA512:58aee233ad3f34b28b0031ec77872f8a027160659cb7eb31e8839cf98f9c6d977f1d211f681d687a58444f043a0dd30885933973fbeb8226e8aeed3ef5e7c39a
```

### `dpkg` source package: `python3.13=3.13.9-1`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.9-1`
- `libpython3.13-stdlib:amd64=3.13.9-1`
- `python3.13=3.13.9-1`
- `python3.13-minimal=3.13.9-1`

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
$ apt-get source -qq --print-uris python3.13=3.13.9-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.9-1.dsc' python3.13_3.13.9-1.dsc 3689 SHA512:7c262d34a60f9626f017834486333a7077cee9216279ded79c06cc9fb247ecdad7cf6b60d7b518a86c4a4c4135e0d2f1124922fe8750fed4143d0e4be99d8f54
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.9.orig.tar.xz' python3.13_3.13.9.orig.tar.xz 22681368 SHA512:ffc9b6e545bf5cf8f3b945f85442eb4bd28cca9adb92d8c253f44078ec2e9758f802bf72c48e0d7e503c02b2dc754c58ee913cd3b7d8e8808fac2a0aa4e006a8
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.9.orig.tar.xz.asc' python3.13_3.13.9.orig.tar.xz.asc 963 SHA512:c33fba3a6b22dccc08beb7f13bd61a25a30f609a54da7c8dfd3b3b4a3490a7b24c11f9617a835388f22709fb09375d35febc417cf104a18f5bec3b43ec999e82
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.9-1.debian.tar.xz' python3.13_3.13.9-1.debian.tar.xz 261592 SHA512:b4861ba91a22fb8868e16e64846e9aa5b2ceee55cb4c064e0ca6112cf13a76c9de8be800e6bce08913acbd7ce42e53a58b57e2e953122237b66e02fa220cc488
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
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-3.dsc' readline_8.3-3.dsc 2817 SHA512:da2062b49605d9fec2bec460bd724b333b52464506013086d5912b27a0c429753d463830f58223a718c620cc3c47249b715360374f57ed299373b9fa1dee508a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3.orig.tar.gz' readline_8.3.orig.tar.gz 3419642 SHA512:513002753dcf5db9213dbbb61d51217245f6a40d33b1dd45238e8062dfa8eef0c890b87a5548e11db959e842724fb572c4d3d7fb433773762a63c30efe808344
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-3.debian.tar.xz' readline_8.3-3.debian.tar.xz 34188 SHA512:3296406f695d9828dccbc8ed6dde856951fc96a625e31cbf43e59986cefb48267514062c76818914b7402fda4f95016ce2ef7cc6ab62f0a7440b91a6edc49f58
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
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.dsc' rpcsvc-proto_1.4.3-1.dsc 1999 SHA512:3b63c54c958b9b1e8d76fe59bfb91d8ace5727427daad8bd421ddf149a373f4ab4de6c9b3b1350149f0bbc1a6d394648e50d764261a6f0f8ee5b653b10899358
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA512:e46ba9ccdd6c520128bf3a154db90742f288a4d593b094a630141cdc5aeb834ffebf9b0eb6d5d0aad9faef3c445c75e2355cbc3e1382b50d29f4d2799441c6e9
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.debian.tar.xz' rpcsvc-proto_1.4.3-1.debian.tar.xz 4228 SHA512:16c6107db0a7ba3971bed2ddbb95a5a3ba24bc387f7ef3b869504d2488080c2957bacb48961a5f8b46433e323151ed2644858fffdad566bc4a424da60965309f
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-3`

Binary Packages:

- `librtmp-dev:amd64=2.4+20151223.gitfa8646d.1-3`
- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-3`

Licenses: (parsed from: `/usr/share/doc/librtmp-dev/copyright`, `/usr/share/doc/librtmp1/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris rust-coreutils=0.2.2-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2-0ubuntu2.dsc' rust-coreutils_0.2.2-0ubuntu2.dsc 8098 SHA512:2d66b7fc43d187ac5ef00cd4d6ebb2a67b86287f0c72a1352a07b8b09a2cf38dbbb0b10be22506a5d049ec8a9974c552b5dd44ab00c50c89f5df7a2415acf1bb
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2.orig-rust-vendor.tar.xz' rust-coreutils_0.2.2.orig-rust-vendor.tar.xz 10803468 SHA512:a9b29f06270f216da761f535f303db4a840535259030695a8bbe7a5269fdab872941785700b22ab21a570b105ad0ade2750015dc1648ca4ec385b9fe4b414c52
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2.orig.tar.gz' rust-coreutils_0.2.2.orig.tar.gz 2827753 SHA512:58def9fe8f01640c6eb7c16cd182061bf62fab22124bdedcb931cdb39b25c2bd3f31523561e321a4822d9e09107dc0c5cc2ddf8e20333138ddaa19d284db609f
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2-0ubuntu2.debian.tar.xz' rust-coreutils_0.2.2-0ubuntu2.debian.tar.xz 17228 SHA512:d72221f314ba0429bec3378489392b42b4d7f91506eca6c8f2d2ffadc06ae45a369a0d4f07ee7c933db7525f1c3e1bf467732927435beca751b7ea1359175ff6
```

### `dpkg` source package: `rust-sequoia-sq=1.3.1-4`

Binary Packages:

- `sq=1.3.1-4`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=1.3.1-4
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-4.dsc' rust-sequoia-sq_1.3.1-4.dsc 4378 SHA512:98d591016a017218f223a58cc16e913ec87bf30ad4eb149c864a64ad2523cb5454e524e49f96e29eaa54b2063dc07edd962e70d6fd90f253d32c728e3bd603ab
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1.orig.tar.gz' rust-sequoia-sq_1.3.1.orig.tar.gz 740320 SHA512:3aa4468b7bcb27532907ce759852e6b92b394a2fc91953b9f3723b9deaab3661c84fb298d79ef3332467aa7a5ca1158d6a8bd65dd961d30aafdcfb34a867c880
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-4.debian.tar.xz' rust-sequoia-sq_1.3.1-4.debian.tar.xz 5372 SHA512:9fe30f2b775c2fedca922f03692c8709f384415093abcd9c0c00ddd8290e8e900e93c5369da959e4ac7872a36492fd380dc728c88a6add6cf9527dd96ef26019
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
- `libsqlite3-dev:amd64=3.46.1-8`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

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

### `dpkg` source package: `subversion=1.14.5-4`

Binary Packages:

- `libsvn1:amd64=1.14.5-4`
- `subversion=1.14.5-4`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/subversion/1.14.5-4/


### `dpkg` source package: `sysprof=49.0-1`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=49.0-1`

Licenses: (parsed from: `/usr/share/doc/libsysprof-capture-4-dev/copyright`)

- `BSD-2-Clause-Patent`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-3`
- `LGPL-3.0+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sysprof=49.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_49.0-1.dsc' sysprof_49.0-1.dsc 3085 SHA512:f45c551e3bdad5b90c5c43e00ead6ee9fe89bfc245852a9bc284b3b1b1fce282ce25437cc52f777f3820a6192d55f0c0a9c4dd1f259e258d49f9ed4e2594792e
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_49.0.orig.tar.xz' sysprof_49.0.orig.tar.xz 1239324 SHA512:ca94abd405e9765c36115a097ad2efcb388b04f1457d20c73b6ff058c46bc4db314dd0037951a43e18c7d218fbf036683e9cc076cfdecaede72c2f8fe2e2eb8d
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_49.0-1.debian.tar.xz' sysprof_49.0-1.debian.tar.xz 16376 SHA512:d82e04c83da71f3073eeb7cb50b0381698f1656de90cbd310c89be7d077c380848d9fb91b4ea6d6fff890f7944ef6b37cbc5af7746ff828ae49ab767011c1d4c
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

### `dpkg` source package: `tiff=4.7.0-3ubuntu3`

Binary Packages:

- `libtiff-dev:amd64=4.7.0-3ubuntu3`
- `libtiff6:amd64=4.7.0-3ubuntu3`
- `libtiffxx6:amd64=4.7.0-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.7.0-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu3.dsc' tiff_4.7.0-3ubuntu3.dsc 2368 SHA512:db14ba26d5bd5342e5e649b7ad4e47844141a4d3a0cea2ccd2b9159eae9508c58872c9c58b28ab1fe2e4224c3f370adb412dabd0ff64df344154f68e51a6025a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0.orig.tar.bz2' tiff_4.7.0.orig.tar.bz2 2111254 SHA512:6d6f39727a4403ffaae390d54f1d7a6ff926085480422cbc4e2168e8e6490bf283e69361860d0ca0d7951543f48be550641b76d814c24a1b4e4bff1da9e27c6d
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu3.debian.tar.xz' tiff_4.7.0-3ubuntu3.debian.tar.xz 27588 SHA512:d09eb851e20849139ad3069057dae7a1fc30db88c71deefb1c7927bbb5f90fecf86c86262d6984b79291bd399a844fe844199c4ecfdb32d649b8d1968890f865
```

### `dpkg` source package: `tzdata=2025b-5ubuntu1`

Binary Packages:

- `tzdata=2025b-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-5ubuntu1.dsc' tzdata_2025b-5ubuntu1.dsc 2439 SHA512:44b445d9e597886beb6374a23472354e8855d98f2eea5dd9de5bbe68d3751792cad0003b57fc8bbfb4c0f85caa68164e7b6184457eb46fe2b39814509be97418
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA512:7d83741f3cae81fac8131994b43c55b6da7328df18b706e5ee40e9b3212bc506e6f8fc90988b18da424ed59eff69bce593f2783b7b5f18eb483a17aeb94258d6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-5ubuntu1.debian.tar.xz' tzdata_2025b-5ubuntu1.debian.tar.xz 188720 SHA512:6c61a1cd62fb0e43324e3fde60dbf24d7d97d9374e6dbf00ebd5c890f534ce79e2b38f3e99a71290834d34f9b67485830b94fb3ec52ec53ac9ac797824b5f217
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

### `dpkg` source package: `unbound=1.22.0-2ubuntu4`

Binary Packages:

- `libunbound8:amd64=1.22.0-2ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libunbound8/copyright`)

- `BSD-2-VUT`
- `BSD-3-ADG`
- `BSD-3-CZ.NIC`
- `BSD-3-Farsight`
- `BSD-3-NLnetLabs`
- `BSD-3-NLnetLabs-Mekking`
- `BSD-3-Regents-DEC`
- `BSD-3-Todd-Miller`
- `BSD-3-VUT`
- `BSD-3-Viagénie`
- `BSD-3-WIDE`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris unbound=1.22.0-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0-2ubuntu4.dsc' unbound_1.22.0-2ubuntu4.dsc 3284 SHA512:8892e98650fc746d83449981d3783308beae0ad61cc2271fd7a0aec6b43cad1995b6406b23446e290195f8ea300458b83ece0df901bc12c08dc7b993c2a813a9
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0.orig.tar.gz' unbound_1.22.0.orig.tar.gz 6682466 SHA512:6c873e19902ce6cd59cec7084d5dba1a5bd5fe4437c827ae69bdf9273bcd8d2d1ec0dc183076f8d2e1fd38730bf8c10852d678399f0b2ea8ccf7e39119568978
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0.orig.tar.gz.asc' unbound_1.22.0.orig.tar.gz.asc 833 SHA512:afbf5a125f104a25576b1c416b32f68d715b41a025fc3a61e6ee3bc28f9988b4277c7f0dd188c51cbe5641f51ade20f740ea131d1a7b5db38e2d1462a9edbb69
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0-2ubuntu4.debian.tar.xz' unbound_1.22.0-2ubuntu4.debian.tar.xz 39284 SHA512:46f4fd26aae4abdcd7b77ecbfb65f3e19903f7da3b7ed6c4d5d7d477006dd478fbda181bf572e632286c1091fa874ac54f0e162aa1f68e8fab2fa41c5d8a70d7
```

### `dpkg` source package: `unzip=6.0-28ubuntu7`

Binary Packages:

- `unzip=6.0-28ubuntu7`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu7.dsc' unzip_6.0-28ubuntu7.dsc 1883 SHA512:6d902b4d6009a692dd83ff0a155ab86fe161b36336bfc8e0712376d87bb356d23651d69a50e2db0964fbd3326be2a2c94f789e650e48a426fe1184e3eb5fd7c1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu7.debian.tar.xz' unzip_6.0-28ubuntu7.debian.tar.xz 47392 SHA512:c485e88a03b7ede082d2df4cd035de9c6d25f52051b8ae90ae05a33f280da631da06d9a39eb693b6d89c6ec4f38079733d0868a76760adc7641d68a78edbfc53
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
- `libblkid-dev:amd64=2.41.2-4ubuntu1`
- `libblkid1:amd64=2.41.2-4ubuntu1`
- `liblastlog2-2:amd64=2.41.2-4ubuntu1`
- `libmount-dev:amd64=2.41.2-4ubuntu1`
- `libmount1:amd64=2.41.2-4ubuntu1`
- `libsmartcols1:amd64=2.41.2-4ubuntu1`
- `libuuid1:amd64=2.41.2-4ubuntu1`
- `login=1:4.16.0-2+really2.41.2-4ubuntu1`
- `mount=2.41.2-4ubuntu1`
- `util-linux=2.41.2-4ubuntu1`
- `uuid-dev:amd64=2.41.2-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/liblastlog2-2/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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

### `dpkg` source package: `xorg=1:7.7+24ubuntu1`

Binary Packages:

- `x11-common=1:7.7+24ubuntu1`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+24ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b24ubuntu1.dsc' xorg_7.7+24ubuntu1.dsc 2061 SHA512:5d509c36b48b1503b79eec13abc66cc1489c87fe6f54528b2caedf9b9004120e5dac65de1dd2250dea2c55a486a1bcf85d770709260cdccd131d732200ac9813
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b24ubuntu1.tar.xz' xorg_7.7+24ubuntu1.tar.xz 241796 SHA512:12171b148181e632f50141a0cf897cd97d0fb6145cffb781973579addecd92f572d4584a95227754a7bd803a039790a951eccdff0e224b61488d730e2c51efa4
```

### `dpkg` source package: `xorgproto=2024.1-1`

Binary Packages:

- `x11proto-dev=2024.1-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

Source:

```console
$ apt-get source -qq --print-uris xorgproto=2024.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1-1.dsc' xorgproto_2024.1-1.dsc 3336 SHA512:2e7799b28e6267936afdc2b1926c40326d5bc3040801f57e41fee6ab32ed2d49df8a36c42900604e3f4f19c0d4ae0fbee611cadff3c7da365f0beeea9c331fc1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz' xorgproto_2024.1.orig.tar.gz 1115486 SHA512:c2d67a98c5ba9b2f4d0b844c96dab342c497710753a8878b75dbf12ecd64b105c9ee3c5fd11eb91e45960420cf8dd7d02547072a32d5c53e58e009394fe33666
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz.asc' xorgproto_2024.1.orig.tar.gz.asc 195 SHA512:9dc7d40a50178f65b47bcd9a360b85f8d40f30e9151bf242d2eef9a12a3d8e5a1488af7e0c0c4c1dbc3e6cb447acd0735fe749290c46d021b4d7e10de3912a33
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1-1.diff.gz' xorgproto_2024.1-1.diff.gz 25061 SHA512:0ba012c2ecad1f6b23d6286c76cfc7f130635e8d30cdb6b2a9a7cb7a0731bb17a5f974d4dcab8efbd104977d95d438295f850c0242d7f46b64a1562891766a08
```

### `dpkg` source package: `xtrans=1.6.0-1`

Binary Packages:

- `xtrans-dev=1.6.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.6.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.6.0-1.dsc' xtrans_1.6.0-1.dsc 1883 SHA512:5259522e4ca78afc47fbb175f9cfccfd7d02e7ef97ed0d980c82ae76e519851948604c284c0cd3370e40a903951f0007256732a356465325aa00bb7527512660
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.6.0.orig.tar.gz' xtrans_1.6.0.orig.tar.gz 239113 SHA512:1165faf7e62ba3a1eb449867b7e626d21f4191a8980ab411ef4bae3875d60333739bb843559b9a1c7e01f7175e18fc9590cd340608d2939a7588989063cecb5f
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.6.0-1.diff.gz' xtrans_1.6.0-1.diff.gz 18507 SHA512:f72e121ee8b8c3e50b184c4d53c47e489d7d343c7a12cbb57a392ccea2e6e7df0cac0ca0dd65b7795a52f44095c60e64d2734214273148e49b0af4cfca0af7b0
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

### `dpkg` source package: `xz-utils=5.8.1-2`

Binary Packages:

- `liblzma-dev:amd64=5.8.1-2`
- `liblzma5:amd64=5.8.1-2`
- `xz-utils=5.8.1-2`

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
$ apt-get source -qq --print-uris xz-utils=5.8.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1-2.dsc' xz-utils_5.8.1-2.dsc 2530 SHA512:f4133f7e5af046d153ce5d76cfabf2c3a8d8e2cf6ab343dd8e4031869bc73ece546e09dd8e0f3444f9fa66ef86cf1cc35bec32d192ddab23b51e7f09ea4ee541
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz' xz-utils_5.8.1.orig.tar.xz 1461872 SHA512:34dbc874a697f4fd17127b3dc828236dd7fd35120a77e0867325273c5d56c4ecddc8a39dce6cbdb3141fff32c56001f4ab18edfa572076d10f2fd55b07ff2b9e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz.asc' xz-utils_5.8.1.orig.tar.xz.asc 833 SHA512:0d851011a5fdd3d36f42c9ddaf163cacfefb8a38e2ad2a2004cb65cfce7fc5bb3df518f6f4fdd3465881246a578d7c36623fd4ef69f83614604fe1b8c343218b
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1-2.debian.tar.xz' xz-utils_5.8.1-2.debian.tar.xz 24648 SHA512:b63c967bd7b00b83cb732ac1bef224a36404b981f3cfc0867a5d76c45b11a76bfd13ae4a5ee62ffa92481c49bfe8f70f5ce9a755b1888e85489a16fe54cb7c52
```

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu2`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu2`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu2.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu2.dsc 3167 SHA512:ff161ae844bd3e2071a129c7406bd85ea2fedfd60230735197c4eb7d7c406222d9d4d5b7dbe26cccf62ee5262b8dec5576052037b75af04012bf865818aa5c19
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu2.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu2.debian.tar.xz 59848 SHA512:72f243e7be9723973af1e98b66b265f37bb11ddeca227f6fd9b0ea298ebd7317a87b52152cbfce45848bc23a8cb450fa2e77a2e305f4b102ae840489a607eaa1
```
