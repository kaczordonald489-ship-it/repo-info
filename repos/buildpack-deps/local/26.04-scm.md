# `buildpack-deps:resolute-scm`

## Docker Metadata

- Image ID: `sha256:2b20e66677fdfc72694b600b0c3e43567983d6052475a7888f69f5be0386beba`
- Created: `2025-11-14T02:17:31.471053053Z`
- Virtual Size: ~ 281.41 Mb  
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
- `libcurl4t64:amd64=8.14.1-2ubuntu1`

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

- `libgnutls30t64:amd64=3.8.9-3ubuntu2`

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

- `libgssapi-krb5-2:amd64=1.21.3-5ubuntu2`
- `libk5crypto3:amd64=1.21.3-5ubuntu2`
- `libkrb5-3:amd64=1.21.3-5ubuntu2`
- `libkrb5support0:amd64=1.21.3-5ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-5ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu2.dsc' krb5_1.21.3-5ubuntu2.dsc 3873 SHA512:aabd71b68ff6c98481fa82c02a78b7bd46315d5ef612a31c2d92dae0926075a009052cd4e7c766c04a6e99d65206e4854f8134a9cd1a065a77056226be01ae83
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA512:87bc06607f4d95ff604169cea22180703a42d667af05f66f1569b8bd592670c42820b335e5c279e8b4f066d1e7da20f1948a1e4def7c5d295c170cbfc7f49c71
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu2.debian.tar.xz' krb5_1.21.3-5ubuntu2.debian.tar.xz 169380 SHA512:3516c768ddd8ea7898ffa576d76c7774d1ddf1e8ccd77e12c219d7e8256318c1703c1f3fadad46f654500abd66f07a129655b79529218a0d3fc45ae77ea4a59b
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

### `dpkg` source package: `libffi=3.5.2-2`

Binary Packages:

- `libffi8:amd64=3.5.2-2`

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

### `dpkg` source package: `libtasn1-6=4.20.0-2build1`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

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

### `dpkg` source package: `openldap=2.6.10+dfsg-1ubuntu2`

Binary Packages:

- `libldap-common=2.6.10+dfsg-1ubuntu2`
- `libldap2:amd64=2.6.10+dfsg-1ubuntu2`

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

### `dpkg` source package: `p11-kit=0.25.9-2`

Binary Packages:

- `libp11-kit0:amd64=0.25.9-2`

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
