# `ubuntu:25.10`

## Docker Metadata

- Image ID: `sha256:96327d6d348566a536ad7709787cdcbe264b446f6925f339749f1cd5fb28246b`
- Created: `2025-12-17T06:59:19.228235913Z`
- Virtual Size: ~ 89.91 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=25.10`

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

### `dpkg` source package: `apt=3.1.6ubuntu2`

Binary Packages:

- `apt=3.1.6ubuntu2`
- `libapt-pkg7.0:amd64=3.1.6ubuntu2`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris apt=3.1.6ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_3.1.6ubuntu2.dsc' apt_3.1.6ubuntu2.dsc 3206 SHA512:54d163f5cae0c7bf38fa92fff32eeb88d621396e1d183c07c72cd412d68860dd53e8d7141be530b134791753d65606cd151164dec1143feaf15b96bdcecd18f5
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_3.1.6ubuntu2.tar.xz' apt_3.1.6ubuntu2.tar.xz 2440776 SHA512:630604ff50edc3778741054d93ae0780fa5ab177f825b287faa19cf3611c6bcebc9756e2a113dc847d151265f72c8cf528978224cb468a0181e0dcc93caef6d3
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

### `dpkg` source package: `audit=1:4.0.5-1build1`

Binary Packages:

- `libaudit-common=1:4.0.5-1build1`
- `libaudit1:amd64=1:4.0.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5-1build1.dsc' audit_4.0.5-1build1.dsc 2576 SHA512:684bb33442b2995a90b0cd6b7577135d4ee42031b46e25e12e2de06b2f213376fb92429e4bf638ad828831ffa948077a4f82d4aca8a662fca81a7325bfd7f09c
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5.orig.tar.gz' audit_4.0.5.orig.tar.gz 622404 SHA512:14fa19922cf6436284e1448d5a0e069ce5066d2d49d28679fe3ad019be60c133aee6e345b36e0f482ea1fdeadad7d78676f931aab1c25b91a2d0b445dce3eedf
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5-1build1.debian.tar.xz' audit_4.0.5-1build1.debian.tar.xz 19924 SHA512:df9fce2087ebff93487997ee048b214d3d9b48cb21814b8d339ea9dbdd9c0f5a8033087a04439459a53f3719d1cbc96d45567b6b92182c1f2323894ccec65b46
```

### `dpkg` source package: `base-files=14ubuntu3`

Binary Packages:

- `base-files=14ubuntu3`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=14ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu3.dsc' base-files_14ubuntu3.dsc 1756 SHA512:d4b168776d4d6bb6750f43fc3b6732f211aace293d6b0095865189f1a5be2313ea2ea176a49f8bbcf383132957076edbe4120deddffcfa69125a49cf10d318c7
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu3.tar.xz' base-files_14ubuntu3.tar.xz 96844 SHA512:36e8f6b058d598b9de7d25f3c95e07b1d96efbefe134f087508996d81922400fe0d15032d68ee853a16c860e69e0449f7b041b5455556c84e0fd7e806996f7ac
```

### `dpkg` source package: `base-passwd=3.6.7`

Binary Packages:

- `base-passwd=3.6.7`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.7
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.7.dsc' base-passwd_3.6.7.dsc 1891 SHA512:e56a81c1b38b1a83dd66119a7e7359843f27b5504a0423d5c8679a6c7ef3f5c27814bb6c3e3cbae7633dd61df67ebbcfd19d746f0cda7faf402f88479e7f4f62
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.7.tar.xz' base-passwd_3.6.7.tar.xz 60872 SHA512:9a0f6c0b33396828e7aca57041ab3cf3dc800b2f9057360df2350558c668798c29774f540890f524643405c4b969e80b28c649757cf67cf1edc5e498718990e7
```

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

Source:

```console
$ apt-get source -qq --print-uris bash=5.2.37-2ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-2ubuntu5.dsc' bash_5.2.37-2ubuntu5.dsc 2267 SHA512:988e7ed288ba04a20543e688517c23d88f7c3413f09dc36faa0deddea07aec2730a6ddfa7c00587a699e63f7595576e477d8be2bb7bd5e1dbfe7f80714266c6d
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA512:c5380301114967378ace9ae4c510564cb7a827c221470aa532f2360a35000e7719ae081151f3d2ac86dff1d1465f64e60d9202fa6657d716ed6e449f77552158
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-2ubuntu5.debian.tar.xz' bash_5.2.37-2ubuntu5.debian.tar.xz 96036 SHA512:db2ffaf9c19ec2e61d210bdab670b07ee25de813e68393706b0390170d723a23542343f9ad2b4ffee2aa713e2762ca6929833d295f4bbc207a1cd26096ffce79
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

### `dpkg` source package: `cdebconf=0.279ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.279ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.279ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.279ubuntu1.dsc' cdebconf_0.279ubuntu1.dsc 2873 SHA512:fc4801dcb7bf517035d838096503f484bc7443588f17e8f177c5cdc6b865f861d8b14d2d735b82cca59d6583f65e36ea058daed37d1dd71b2890bed2fc42fa04
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.279ubuntu1.tar.xz' cdebconf_0.279ubuntu1.tar.xz 287008 SHA512:f02dec8fe7b34d3ddcabdc5570cb13e34835211d24729f36ea9dd9cc079e746688480b41d7400c5819cbb0340fe82171ed4701b74b1f73645a209305340f67b8
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

### `dpkg` source package: `coreutils=9.5-1ubuntu4`

Binary Packages:

- `gnu-coreutils=9.5-1ubuntu4`

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

Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9ubuntu1.dsc' db5.3_5.3.28+dfsg2-9ubuntu1.dsc 2306 SHA512:b90c086966dda1c74b398aa0a75ab4ebfcdc94a46690e2967ce43884860b7de3764e4880c1d92905849989fc2afb3c471b590e05255bbd3db47c5108e05a558c
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9ubuntu1.debian.tar.xz' db5.3_5.3.28+dfsg2-9ubuntu1.debian.tar.xz 36528 SHA512:4745c078e4f4ff8750370d5f35ce6acdfe03043faae63beb973a495bdf2850fe2660c1cc87b05c763969628be25bfd130a04b81843a8cf30896c3730970e4dbb
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

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.10-4
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-4.dsc' diffutils_3.10-4.dsc 1875 SHA512:7bf4b24fa79e6c436125eb5c5926e7f4460c1108142a0d2d5662d9e6ee40e9425e22e282c784850790ae02032d6c1dc724c3b38a592e7f74949f732d4ce854bd
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-4.debian.tar.xz' diffutils_3.10-4.debian.tar.xz 14304 SHA512:447d360101e549e520210cd6da9573cce293c1b59266d960b066da4eeff8ce473c19d2269e30cd82e33e162cd6c6b870755b3bb292d8592a51511ca19e974350
```

### `dpkg` source package: `dpkg=1.22.21ubuntu3.1`

Binary Packages:

- `dpkg=1.22.21ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.21ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu3.1.dsc' dpkg_1.22.21ubuntu3.1.dsc 3486 SHA512:142ea330912e6c2c9fdc6de497b5613de30b394850ef2faf4888c09a50e58b48ee94d7883ea7b257432c02f50d3f9520fe6a4998c538da6e3c0abe41976663b9
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu3.1.tar.xz' dpkg_1.22.21ubuntu3.1.tar.xz 5672872 SHA512:7e49ffdf72eaa89e1b165aa7c54bd254c5382eb674bbec64e3f4c62037560f20c6b331661cf4022ddd81ece73df6e0e7c1085ab578523a2fcc183626118be386
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

### `dpkg` source package: `gcc-15=15.2.0-4ubuntu4`

Binary Packages:

- `gcc-15-base:amd64=15.2.0-4ubuntu4`
- `libgcc-s1:amd64=15.2.0-4ubuntu4`
- `libstdc++6:amd64=15.2.0-4ubuntu4`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-15=15.2.0-4ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-4ubuntu4.dsc' gcc-15_15.2.0-4ubuntu4.dsc 52458 SHA512:ca0d3243f95a96b1993099490ff530335c32fa4c28afe6030e64fbcf43f25bd9f4d23306ed83d40e8c211bcb8cc36ab19e10bb45a19ca6ffd636aad00c35e109
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0.orig.tar.gz' gcc-15_15.2.0.orig.tar.gz 105962230 SHA512:83887af5c7798105d1ad85f0e9c794daa3cf030638bf40b3bff48771b8325d95c9a0d99d7d2c86c8e45499ff87f975e1914d00b72482862357645cc7ec330d38
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-4ubuntu4.debian.tar.xz' gcc-15_15.2.0-4ubuntu4.debian.tar.xz 2651048 SHA512:ba4fb206a14166e4b236083ea0cfed8fbb83b39fe723d1470391458ce944464e48af246ccecaf662b2408b06061c728574e4442e9ed84b7d1b62ddb1fd34b4ba
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

Source:

```console
$ apt-get source -qq --print-uris glibc=2.42-0ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-0ubuntu3.dsc' glibc_2.42-0ubuntu3.dsc 7889 SHA512:8a71274b5ce5cc7bb2359835306bd3fd259fa52b49d48f62d76ac4d4f73c88990dbca629eaf01a619f737d9026d9c97fd6059ae170755b85a35c03d47bdfb3ca
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz' glibc_2.42.orig.tar.xz 19930508 SHA512:73a617db8e0f0958c0575f7a1c5a35b72b7e070b6cbdd02a9bb134995ca7ca0909f1e50d7362c53d2572d72f1879bb201a61d5275bac16136895d9a34ef0c068
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz.asc' glibc_2.42.orig.tar.xz.asc 981 SHA512:d868220778e98d24aead10a585e6a903892e4d043cd96a404634c8aa03d001d624a46a5c0fe13c86f83f66396a1f360a10990966fe377e98a722914b5087575d
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-0ubuntu3.debian.tar.xz' glibc_2.42-0ubuntu3.debian.tar.xz 446852 SHA512:d6d11e5907c217d4805494fd57ccdc462dce9b3b2736317805867922ad8be25dc026f66e8a1e0310c557da036961d5c66eb3f0ed26c25c6605364906a0c95f0d
```

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

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.4.8-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8-2ubuntu2.dsc' gnupg2_2.4.8-2ubuntu2.dsc 4577 SHA512:3f56ea4e2c9ea77a52134eeefd5243e05213157175ab857ce8e0355b28fb0b43f3fcb76e6ed1cfea1209f78dfce2d3d909af367ac7cc7d50023c7857b0b40510
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8.orig.tar.bz2' gnupg2_2.4.8.orig.tar.bz2 8017685 SHA512:d7f07a258141a583bc8be18c0984d7dfe8508f12c624c053881ee63dfee11adcda8de216bcaaef9f5d24a1e217de70bf69ee2e3cc43b0da66a0e571ce9c4b436
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8.orig.tar.bz2.asc' gnupg2_2.4.8.orig.tar.bz2.asc 228 SHA512:f739eb41481149e145724969e94907ac55e082da0456e1343da24488958ecd020225b45e1d5dc4c93abc06fe89d942e892b488a460f3278f9f2bcff5f51c8ca0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8-2ubuntu2.debian.tar.xz' gnupg2_2.4.8-2ubuntu2.debian.tar.xz 120704 SHA512:14ab0e0704441e010638b7399d46eeef55ec101b43da71920b3c6de9b92769f48d8882e010e53d309896462ad4274cd3c62296025ca91ac544aa635860a7d1f7
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

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.68
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.68.dsc' init-system-helpers_1.68.dsc 2209 SHA512:4c8477f718287a3001fc378938e2e3bdbf15dca7a8aac93fdb65fe458408294b15c7e05ad6b5bcf04eda927ba934ca7f201cea2ff93090c8906b7b5abadf920e
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.68.tar.xz' init-system-helpers_1.68.tar.xz 45168 SHA512:3962845b388ee5c22de26a17e216ddd7f706d4f67729c80891c1457bf3e3fd70484b04f6d9d42adde7dad72da5529ac6feda97c9e2d4c0f4ccbfec2217a8e1b4
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

### `dpkg` source package: `libcap-ng=0.8.5-4build2`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4build2`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4build2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build2.dsc' libcap-ng_0.8.5-4build2.dsc 2307 SHA512:5c700373e21c245ffdb700c550dba4edf7027e40cf2fd7b4c5e648cddc96142437398b09f9e634d4c7f04868d651a4e189bc217d9a78b344644a19a20e2b6615
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA512:3bd868c7f263b77edd2feda831470b407f1086b434618e54336fb78bbf8bf3bad53f4c006a2118fb594b16554f8f7ec2acb76e08be5586d0261684e9ba139231
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build2.debian.tar.xz' libcap-ng_0.8.5-4build2.debian.tar.xz 7952 SHA512:5fd5b3c3d8abcfb4ffeb000b8361dbaef690de70380dee9a7eacd05e0da308f4d2d864f89707580367e4b2d201b4ab654b2f58dc5c10e70b20825bf5ca0f4875
```

### `dpkg` source package: `libcap2=1:2.75-7ubuntu2`

Binary Packages:

- `libcap2:amd64=1:2.75-7ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.75-7ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-7ubuntu2.dsc' libcap2_2.75-7ubuntu2.dsc 2785 SHA512:717f69d1c240665517ac9a251474829c5def267d50b76e9aa0260393df327ce17258e48ca27d81a5d235fd9ffe4706321fb2ebf268c0954528aae2fbe34c44b2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA512:229e9b62a1d54024107cbf321fffcb152c0071154554a3fcee6e09e19cc47fd1fd862575135a4fc589b79a043f760bf40d26ea9fd58638f26e809533c017d65f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA512:6a6af52ef3a48356d8c205827aa039ed852ec4a1cfea44f00613457380478ebd4946caf933a8ebdf98899b14340b9a7ef9b7151c4659329e2fd80590667d59d9
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-7ubuntu2.debian.tar.xz' libcap2_2.75-7ubuntu2.debian.tar.xz 23112 SHA512:42f78ae537cc6acb4c0f77b4b05ee6ec5b45b464a619a20287d0534b8133fab4bfda2b5df84b4847b36cebebe687f26fc71dcb10038d7a31d15aa4fe82be5ed8
```

### `dpkg` source package: `libgcrypt20=1.11.0-7build1`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-7build1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-7build1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-7build1.dsc' libgcrypt20_1.11.0-7build1.dsc 2969 SHA512:ddcf45fa9b1d7ea8b073edede2f24595742648efbf44e1b0fa6c784c58e64f24f7730f21da041d32763547ee47b5477730366c3ab809372082a2aeec1e6de947
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA512:8e093e69e3c45d30838625ca008e995556f0d5b272de1c003d44ef94633bcc0d0ef5d95e8725eb531bfafb4490ac273488633e0c801200d4666194f86c3e270e
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA512:eebd4c599bd8f375445566c3c73df5a223f256cb650cf18d8fed033a1f13a1fb8b9b10a17d686be21ad2bced60fc8e27d71b07e5f556a854a893e44c5dd81ae7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-7build1.debian.tar.xz' libgcrypt20_1.11.0-7build1.debian.tar.xz 40536 SHA512:78707fbd9e51eeed55e3ecdf6e9192698932b561f5bc51bedbb008b9bb79fb80e62fb4b22a67ec240e27984a404da2101087b0a75b3eb8fd425118cdc6c69fe0
```

### `dpkg` source package: `libgpg-error=1.51-4`

Binary Packages:

- `libgpg-error0:amd64=1.51-4`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.51-4
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51-4.dsc' libgpg-error_1.51-4.dsc 2956 SHA512:acc7f3b775e622d69b8cb62a249bbfd2bee8fe3f09568ed7bb80c17536b45effb228531a4e0edad795d77a2267aad5267416938603a22113dc265dfdb8c756e8
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2' libgpg-error_1.51.orig.tar.bz2 1085510 SHA512:4489f615c6a0389577a7d1fd7d3917517bb2fe032abd9a6d87dfdbd165dabcf53f8780645934020bf27517b67a064297475888d5b368176cf06bc22f1e735e2b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2.asc' libgpg-error_1.51.orig.tar.bz2.asc 228 SHA512:526890917db6547b6b2fb5a462c2a74501187579e4f156845952ebfb01595a77a0eda94b24350349abaee3ee8caac1d7ea6da005115467b5892c758842af3003
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51-4.debian.tar.xz' libgpg-error_1.51-4.debian.tar.xz 22332 SHA512:b94a5e257e623e40c02a0495b1b3abb3e08daa6c0be307a829910c1c156f9612049619db0b4cacebc9134a14347e9e12881e6df9e8ad49aed7f92fd98e8f7342
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

### `dpkg` source package: `libseccomp=2.6.0-2ubuntu2`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu2.dsc' libseccomp_2.6.0-2ubuntu2.dsc 2745 SHA512:775c8e1370ab47b57ee43400c59f373e58f8d2534f62093e28528bfa36e5d93b3b7378ee3cb3be6ed70c01f82fd0583c05140f0d372b9df4d0e803059996b275
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA512:9039478656d9b670af2ff4cb67b6b1fa315821e59d2f82ba6247e988859ddc7e3d15fea159eccca161bf2890828bb62aa6ab4d6b7ff55f27a9d6bd9532eeee1b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA512:973b69c58085a1567f860e621e3a197be02c0ca71dad664234418cf5c00c39767efd37a7c4016f1be5bd588262617b6603855262db2ee6f31bc16061bc130e0f
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu2.debian.tar.xz' libseccomp_2.6.0-2ubuntu2.debian.tar.xz 27840 SHA512:226734472b73370d0e82f3529e578cc4cea0e272cd982e499add8b041523550a978fdcf06b7014937e708a278d72f6f3b993e6ef1b76a13fa6d8e1c4404ae2ee
```

### `dpkg` source package: `libselinux=3.8.1-1build1`

Binary Packages:

- `libselinux1:amd64=3.8.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.8.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1-1build1.dsc' libselinux_3.8.1-1build1.dsc 3036 SHA512:79bb54b7b972d2cb752bd762d47a0448b41e68de864a7d12621490b8c38ff1af9de33b1ecd476011d5faa26f54d0657cf793ba4dbfae8f74850588551d07cee4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz' libselinux_3.8.1.orig.tar.gz 204411 SHA512:646a31dff3b670a530adb9fc2fdc3ca9fe34a58e67e0fac52cc33bc7a01fa63c175987ef254c6c3bc7299cef137bc6f258dc378f4d70ae5c0fa0ece3bef42ab4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz.asc' libselinux_3.8.1.orig.tar.gz.asc 833 SHA512:ece79feb7758eafb8cf60092039596971140d8af7049671dfa8a7be6cc3167e928e361d8a9b26abfd855520413533890c280eec1e8107b260e3bbadb79c5159a
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1-1build1.debian.tar.xz' libselinux_3.8.1-1build1.debian.tar.xz 37892 SHA512:a1e558f9b37265227df9c7a7e60c4cb2481405589578ead7eb35a5feae5d7520ebe31837fcf6e4694fd5445ca75538a163232f7b8f8c4825a17a035896e1dac7
```

### `dpkg` source package: `libsemanage=3.8.1-1`

Binary Packages:

- `libsemanage-common=3.8.1-1`
- `libsemanage2:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.8.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1-1.dsc' libsemanage_3.8.1-1.dsc 2992 SHA512:4f7a5bb878ca14f351e6e15e0519f311dfe206aa318637349dad52f1b102cb360a4c4247d49396823745199c0bcd5b305e5c400a6cf2a08eeb5ab61efcd829f1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz' libsemanage_3.8.1.orig.tar.gz 184618 SHA512:ac3729ba4934a48a33e082af35baa9e25e6806855afb0f0e4e22aa67be201518c3d4933b8cf4dec83e5acbe178301276f51850bb1b16bc13e027a470ac7f1eb5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz.asc' libsemanage_3.8.1.orig.tar.gz.asc 833 SHA512:b21cf3e0a5e28ddddaaded81fc00080d13a8aaac44357bf980fa1c28899e50e0791b66f407eaffd6ce0719caee356e02e576947949cf5cb34665fe0bb90f7108
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1-1.debian.tar.xz' libsemanage_3.8.1-1.debian.tar.xz 37572 SHA512:70cd6ee56d4af85bdd944267519ba90482c85a294baa0b634316e464c260f3f00a1f0084120a0cc257ee4179eedb3765dd91318648b184d678ad18980663674c
```

### `dpkg` source package: `libsepol=3.8.1-1`

Binary Packages:

- `libsepol2:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.8.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1-1.dsc' libsepol_3.8.1-1.dsc 2347 SHA512:a87f034f24b7bba40b77f66cee5bfaa42121c2a55d70e9f86fd4d3cd760fe52aca247176ea904ead56bf5d0257e8d31215816dc3df697de5391b6d395fcc6e04
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz' libsepol_3.8.1.orig.tar.gz 513830 SHA512:6a66fbbc25f4ca5f58b07d19a70f3f6c233594ea5bc5a9f5d9f008eb03a83cea84ae0f03329f340b95e4f7135981d06cb9e66a7b3ca2f1494a71bbdcb5a01665
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz.asc' libsepol_3.8.1.orig.tar.gz.asc 833 SHA512:855233e6aec9e1cdff00c45edabd0a3a8de06bcd92edb0e3d3cf825e4cf4490c00c7094ca5350407e48e4ee40611a0405d58a54bde72491a8aff28f81771a54d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1-1.debian.tar.xz' libsepol_3.8.1-1.debian.tar.xz 21432 SHA512:a2d773bb641dda5e9d1c08f7ff1c6b9963801beb57126b30d60d5146692179e01d97b80cd12a388fec9e0a0545351fbaa4618dc8797b29a84b02e0e69711bab6
```

### `dpkg` source package: `libxcrypt=1:4.4.38-1build1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.38-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.38-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1build1.dsc' libxcrypt_4.4.38-1build1.dsc 2028 SHA512:5868d85c1c6ac7364f04633a99d0595a4c0d85ebeaf09bdbf5fc4dab6d8f91aa33a6e32180df7ae359fcf42c680075b90992cd21df4c2cd82f17ccd644253fbe
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38.orig.tar.xz' libxcrypt_4.4.38.orig.tar.xz 394216 SHA512:4310a38e7cb8c337f52ea4ed47561ea548583426276f5ec1f6a52f9435e0508b8c81427947e69e7dc77dee6187fe0c16d1e90d261d857d52d0e58e737230dce4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1build1.debian.tar.xz' libxcrypt_4.4.38-1build1.debian.tar.xz 8596 SHA512:52dfac83bdbd2be82e8b7a3ff8c71d3412ea3b2bb4239bd94bc01169499e78c6938b99ea45ee2cc7ee2a132e7610b36662f5d3957f0ee32a0f8f6622742a7156
```

### `dpkg` source package: `libzstd=1.5.7+dfsg-1build2`

Binary Packages:

- `libzstd1:amd64=1.5.7+dfsg-1build2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1build2.dsc' libzstd_1.5.7+dfsg-1build2.dsc 2395 SHA512:84176b8751e7aa6bc84b8cecfb52760d8c4ce882a6c75bd39f7fb4878a53fbaf3fbc66f0e6679fc3f69bfd9e2595e889e7b0cebcb1a9190d5e10662799207bac
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA512:74604a877f899df6a47e88b895334c0fe35af9d096d472f535e772b156bf61e5529833173ea766dbf5e58fc20ce40a2e47ff1cbed8ff7f2bbd506c6634ae5145
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1build2.debian.tar.xz' libzstd_1.5.7+dfsg-1build2.debian.tar.xz 23184 SHA512:6431392a74b281afaac2b9eed4f6f5dd00c0103cec987380312f23b9607c58c3cdeafbdc005102e637b89b3a06f855faf3a5df04d720e0b20ce41690bdbe9e0f
```

### `dpkg` source package: `lz4=1.10.0-4build1`

Binary Packages:

- `liblz4-1:amd64=1.10.0-4build1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4build1.dsc' lz4_1.10.0-4build1.dsc 1965 SHA512:ede20a0c3a1c8824d1b008cce662dc6593ffcf3eeb72e89e535f84eb8b91396e2b2def6ce86ebd42710955892b10f9b6764eec3ac8b230efb0c0ca7d594e3b53
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA512:8c4ceb217e6dc8e7e0beba99adc736aca8963867bcf9f970d621978ba11ce92855912f8b66138037a1d2ae171e8e17beb7be99281fea840106aa60373c455b28
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4build1.debian.tar.xz' lz4_1.10.0-4build1.debian.tar.xz 8152 SHA512:19dfb1fca73af402bcd18dab9436017767e4a66c7d759623f6cc60a0f08b287ad984c79b887df729a8307cf9b6dd28d41c6c5cd1addf85d2e4e9c59ca1cb1b4d
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

### `dpkg` source package: `rust-coreutils=0.2.2-0ubuntu2.1`

Binary Packages:

- `rust-coreutils=0.2.2-0ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/rust-coreutils/copyright`)

- `Apache-2.0`
- `MIT`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris rust-coreutils=0.2.2-0ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2-0ubuntu2.1.dsc' rust-coreutils_0.2.2-0ubuntu2.1.dsc 8098 SHA512:889ac86cee4ae6a400c4ad335c68dac5e18f0cab46c3c2f2c8c8fe6f182301120fc7faf2b7690c3f373da1d4fd48d89a551774046df720aead1673f2acac18c7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2.orig-rust-vendor.tar.xz' rust-coreutils_0.2.2.orig-rust-vendor.tar.xz 10803468 SHA512:a9b29f06270f216da761f535f303db4a840535259030695a8bbe7a5269fdab872941785700b22ab21a570b105ad0ade2750015dc1648ca4ec385b9fe4b414c52
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2.orig.tar.gz' rust-coreutils_0.2.2.orig.tar.gz 2827753 SHA512:58def9fe8f01640c6eb7c16cd182061bf62fab22124bdedcb931cdb39b25c2bd3f31523561e321a4822d9e09107dc0c5cc2ddf8e20333138ddaa19d284db609f
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.2.2-0ubuntu2.1.debian.tar.xz' rust-coreutils_0.2.2-0ubuntu2.1.debian.tar.xz 19448 SHA512:e63052b47df74ae3411db007b17fd7e1be606c84eb87583c1aef774f2f72b7ac8921dc1560363f35de11cc2d60b2caa969a998e646bb0f7928c381a77f34c43f
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

### `dpkg` source package: `sensible-utils=0.0.25`

Binary Packages:

- `sensible-utils=0.0.25`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.25
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.25.dsc' sensible-utils_0.0.25.dsc 1718 SHA512:db01b4591b5aa5c047df49de49bb154b02063d06a221cd590ed3211eb549b68c6b4493c96fe50b2ad0f3ceafa28b53fbc082d4433ac2d4f2a6f93558af0ac41b
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.25.tar.xz' sensible-utils_0.0.25.tar.xz 76132 SHA512:42b3536abbbc70f0c8ac69a6b34ed7c3576d7835ec690f9acd8bb4e57cb22386dd7e22ac5a43b33f3a1f5d04ec2bbc4255119a1e45008cbe632baf61c87fb1e9
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

### `dpkg` source package: `util-linux=2.41-4ubuntu4.1`

Binary Packages:

- `bsdutils=1:2.41-4ubuntu4.1`
- `libblkid1:amd64=2.41-4ubuntu4.1`
- `liblastlog2-2:amd64=2.41-4ubuntu4.1`
- `libmount1:amd64=2.41-4ubuntu4.1`
- `libsmartcols1:amd64=2.41-4ubuntu4.1`
- `libuuid1:amd64=2.41-4ubuntu4.1`
- `login=1:4.16.0-2+really2.41-4ubuntu4.1`
- `mount=2.41-4ubuntu4.1`
- `util-linux=2.41-4ubuntu4.1`

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
$ apt-get source -qq --print-uris util-linux=2.41-4ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41-4ubuntu4.1.dsc' util-linux_2.41-4ubuntu4.1.dsc 5086 SHA512:c373a65a0164a033f5be210864dc11db05d68ee0a1494bd17f47c4552470bb93f2c32b629e748c1c44be415d37cec78711ea3104cb699f925775c64d3f9506d4
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.orig.tar.xz' util-linux_2.41.orig.tar.xz 9535724 SHA512:800ff92ee7a047732c0accb9dd759d6ed659947373ca72e0dd3ca601d0a6fed9db92c0838cfaff6bcdb8c08bdc1ffa675721893f42945885c57ccd59ab676318
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41-4ubuntu4.1.debian.tar.xz' util-linux_2.41-4ubuntu4.1.debian.tar.xz 127456 SHA512:9ca20fd849d2d5711fa3edf0b047add1f4f81dbfa55e930c123465dabb6c7fea619fad27184bb4cd7cccb742b6f3f8176a0c169c1aaade30ce272a1f3298d877
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

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.8.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1-1build2.dsc' xz-utils_5.8.1-1build2.dsc 2728 SHA512:7f873a4c974f0fd5afeb93ad07443a48b32dad1e1bdaf4695b2b6b57ef0367b827123cd8060f311b9eda1e4929d8e4494412203f68aefa654b98aeb5157c8fdf
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz' xz-utils_5.8.1.orig.tar.xz 1461872 SHA512:34dbc874a697f4fd17127b3dc828236dd7fd35120a77e0867325273c5d56c4ecddc8a39dce6cbdb3141fff32c56001f4ab18edfa572076d10f2fd55b07ff2b9e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz.asc' xz-utils_5.8.1.orig.tar.xz.asc 833 SHA512:0d851011a5fdd3d36f42c9ddaf163cacfefb8a38e2ad2a2004cb65cfce7fc5bb3df518f6f4fdd3465881246a578d7c36623fd4ef69f83614604fe1b8c343218b
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1-1build2.debian.tar.xz' xz-utils_5.8.1-1build2.debian.tar.xz 24756 SHA512:9b28162663a8dc3a3d8c1f06e842da364d51338fc3ef2e72ac446c17780074e519afdd007e06c9e0c626496acfbe35f5c21d0a6a7deec3ef37627c4f57c82369
```

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
