# `silverpeas:6.4.4`

## Docker Metadata

- Image ID: `sha256:a99d46af11415490d691f370a6c6db970dcb6f9b6791d731f51727f091d42df4`
- Created: `2025-11-13T23:44:22.529394553Z`
- Virtual Size: ~ 2.87 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/opt/run.sh"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `TERM=xterm`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US.UTF-8`
  - `LC_ALL=en_US.UTF-8`
  - `PING_ON=1`
  - `JAVA_HOME=/docker-java-home`
  - `SILVERPEAS_HOME=/opt/silverpeas`
  - `JBOSS_HOME=/opt/wildfly`
  - `SILVERPEAS_VERSION=6.4.4`
  - `WILDFLY_VERSION=26.1.3`
- Labels:
  - `build=1`
  - `description=Image to install and to run Silverpeas 6.4.4`
  - `name=Silverpeas 6.4.4`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=22.04`
  - `vendor=Silverpeas`
  - `version=6.4.4`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `abseil=0~20210324.2-2ubuntu0.2`

Binary Packages:

- `libabsl20210324:amd64=0~20210324.2-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libabsl20210324/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris abseil=0~20210324.2-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/a/abseil/abseil_0%7e20210324.2-2ubuntu0.2.dsc' abseil_0~20210324.2-2ubuntu0.2.dsc 2647 SHA512:c17b0363d59d0c48aab92b7703c945d7297677803478f09cf42008de328218a8840f86ef02075a541b049b410bca2be6d0564dc9bdfe6809f5af58c3c4c8d88b
'http://archive.ubuntu.com/ubuntu/pool/main/a/abseil/abseil_0%7e20210324.2.orig.tar.gz' abseil_0~20210324.2.orig.tar.gz 1774104 SHA512:8d2b6728b3fca05c41fe866263b24c784a20da0851babcb10808d12b7da340d582c6943cc32033d48b280f282e3fc6d489ea180772c9ba07777531b4d24ebe0e
'http://archive.ubuntu.com/ubuntu/pool/main/a/abseil/abseil_0%7e20210324.2-2ubuntu0.2.debian.tar.xz' abseil_0~20210324.2-2ubuntu0.2.debian.tar.xz 38776 SHA512:2bbc683581533882ed8702adde6697276b97d90287fcdad253020a1737ce52877abe22660f434aef0d8dfd2e7948e2a3b93608ca24b6a38f179091fae3772e0c
```

### `dpkg` source package: `acl=2.3.1-1`

Binary Packages:

- `libacl1:amd64=2.3.1-1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1-1.dsc' acl_2.3.1-1.dsc 2486 SHA512:8eb7f71030d7c4d355886390f12ffd7f66605bb2082a9a9de2eea0918aefe7b7cf1c26a3f8872681f5b3074df1cf07c4d01ae564bcba5b400b048b0e34b233c2
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1.orig.tar.xz' acl_2.3.1.orig.tar.xz 355676 SHA512:7d02f05d17305f8587ab485395b00c7fdb8e44c1906d0d04b70a43a3020803e8b2b8c707abb6147f794867dfa87bd51769c2d3e11a3db55ecbd2006a6e6231dc
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1.orig.tar.xz.asc' acl_2.3.1.orig.tar.xz.asc 833 SHA512:be046f3bf1ac7e21d2a07bf6ea87c1fedeed2f9d370d8bf3de1aa0c448de5484b1523697415849b6b7ca23e48e3df5353f6aebe850eb20fc2044d2681c71f298
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1-1.debian.tar.xz' acl_2.3.1-1.debian.tar.xz 27732 SHA512:2fdfcd8daa1919e850cd3ed634b4141d65bbf7847eaf0a7899b6e8ae52fe2fa15de3378f6487a9224d00eb530cf5b285cc3b6272af66fcdcf1f29f2838648083
```

### `dpkg` source package: `adduser=3.118ubuntu5`

Binary Packages:

- `adduser=3.118ubuntu5`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.118ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.118ubuntu5.dsc' adduser_3.118ubuntu5.dsc 1766 SHA512:8d6e9894549dc9dd53db8480cb18ee9b012bc70ea7b53d72b0ad8ad713a1672d2e94750e1cde44d2b8f9fd7e66b1ea7c2ad20202fc7bcd90e2fba5cee63d5b5d
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.118ubuntu5.tar.xz' adduser_3.118ubuntu5.tar.xz 222904 SHA512:ded568a5a3f5a5ac1acc2098e37160194f8c4622e90c7044d599286a321fe8fd701c8554a4517e4d72a6089b8e3b5592b92d46668032bda81de64cc736bf0a75
```

### `dpkg` source package: `alsa-lib=1.2.6.1-1ubuntu1`

Binary Packages:

- `libasound2:amd64=1.2.6.1-1ubuntu1`
- `libasound2-data=1.2.6.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libasound2/copyright`, `/usr/share/doc/libasound2-data/copyright`)

- `LGPL-2.1`
- `LPGL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris alsa-lib=1.2.6.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.6.1-1ubuntu1.dsc' alsa-lib_1.2.6.1-1ubuntu1.dsc 3002 SHA512:fa3e6a475aeffa91fa07cfbe33552256dd54070085de1108e979ebb16a89c47c445f9fe807d5ea569dc0654ec0fd3dc758035aca9ed758f7c07565d3c8065cf7
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.6.1.orig.tar.bz2' alsa-lib_1.2.6.1.orig.tar.bz2 1079670 SHA512:70e539cf092b5d43e00e4134d8a3e184f0dc34312823e4b58a574320cbf06cb7369bc3251ecb1858033756a7a8c35d36faa8da48d49f6efe0cec905784adbd45
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.6.1.orig.tar.bz2.asc' alsa-lib_1.2.6.1.orig.tar.bz2.asc 833 SHA512:5499cae5dad0ec26aa7c4ab1af0bbfc0386e3c092aa40610ed851bb3b3b03201e5dcd9af5fd915ac9597c86df24fc734c5bdab51808021caae3161f0a91666bf
'http://archive.ubuntu.com/ubuntu/pool/main/a/alsa-lib/alsa-lib_1.2.6.1-1ubuntu1.debian.tar.xz' alsa-lib_1.2.6.1-1ubuntu1.debian.tar.xz 33288 SHA512:909623e6313605a1ae9c5ca703d52544e1795c58f7affdabf20f61bd635366cfb259e360edbbb2e4d841efa7db7c133392879c66b5c364b43b5eda87bc7c8268
```

### `dpkg` source package: `aom=3.3.0-1ubuntu0.1`

Binary Packages:

- `libaom3:amd64=3.3.0-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.3.0-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/a/aom/aom_3.3.0-1ubuntu0.1.dsc' aom_3.3.0-1ubuntu0.1.dsc 2175 SHA512:34be91d0dc147b88b7a53a29fbef0cb24696b2445bff6a703b7923acc7038368dbb3ad569c384dc8e297aa63e8dc02fe427f9b4ed033f3b0d17d6ca31f12b355
'http://archive.ubuntu.com/ubuntu/pool/universe/a/aom/aom_3.3.0.orig.tar.gz' aom_3.3.0.orig.tar.gz 4768166 SHA512:d385a38350a0dbfa9a032c6435a25426b9ed9a037e858add93cfc70cf8aedcc5e38270cd821ee48fff194894a238af85cf8904d206d15c1ba557ed7830558f88
'http://archive.ubuntu.com/ubuntu/pool/universe/a/aom/aom_3.3.0-1ubuntu0.1.debian.tar.xz' aom_3.3.0-1ubuntu0.1.debian.tar.xz 14276 SHA512:80d9f6443a54afb7ee40d370860658adbe515df712a1558026e06377dfea74674278aee13b3977cb346c1e0a2777d69f4678531404363d121a9b008e4c99c8fc
```

### `dpkg` source package: `apparmor=3.0.4-2ubuntu2.4`

Binary Packages:

- `libapparmor1:amd64=3.0.4-2ubuntu2.4`

Licenses: (parsed from: `/usr/share/doc/libapparmor1/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris apparmor=3.0.4-2ubuntu2.4
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_3.0.4-2ubuntu2.4.dsc' apparmor_3.0.4-2ubuntu2.4.dsc 3263 SHA512:fd0eb724b2d43077a3708bd51729e884c972e361a36952f0f7ba2a686f76630ab38478b3906843943d0515997ecdd8a8807f702b1a73a0b12667433ad9a50306
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_3.0.4.orig.tar.gz' apparmor_3.0.4.orig.tar.gz 7796852 SHA512:1edd800771f46fab9bc5274842e64482b7fd4a5ba4de9855d621baf1d08c8236bfa7752dd9ab3dee095f8e0798129241a9aebf68ed1c994ae5597086a4a1a8ca
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_3.0.4.orig.tar.gz.asc' apparmor_3.0.4.orig.tar.gz.asc 870 SHA512:870d3037562ae003e642adcd244b74191e9108cebd18e6a925959e595b5a375e2dbfda686349e4cc980981cdd38239a099d3e32f1e824b4a9b477584c8d311a9
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_3.0.4-2ubuntu2.4.debian.tar.xz' apparmor_3.0.4-2ubuntu2.4.debian.tar.xz 136888 SHA512:da616c757022828f738e09e0a04ab9a93b1575acc30318abd2e60ef193c8ef7e3acac4d3d545ee5f3b0310347187d09db8fe0c4ec8422893a6375b9f46c424f0
```

### `dpkg` source package: `apt=2.4.14`

Binary Packages:

- `apt=2.4.14`
- `apt-utils=2.4.14`
- `libapt-pkg6.0:amd64=2.4.14`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/apt-utils/copyright`, `/usr/share/doc/libapt-pkg6.0/copyright`)

- `GPL-2`
- `GPLv2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.4.14
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.4.14.dsc' apt_2.4.14.dsc 2801 SHA512:b1b8ce83cead480ab2c6fa2cbc9ed7384ab9d1dbcca437b96947653f16e7ef96df7d04269db20fa915325033845f5aaf7429f35741ada18e0a9b3b0cbf285cc9
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.4.14.tar.xz' apt_2.4.14.tar.xz 2323176 SHA512:16c3eee24d40d94e9e11f70002564331a35373db693f75cfefa028767b9bcd80307dda99c52953173d575ba6724fe7a7fb37724eb2dd44bf87db17ff36a94ef8
```

### `dpkg` source package: `attr=1:2.5.1-1build1`

Binary Packages:

- `libattr1:amd64=1:2.5.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1-1build1.dsc' attr_2.5.1-1build1.dsc 2134 SHA512:4beeec510cf7976a3b2c0de3b90974ef03886b3a98ccb2b74f6278ed988727af3a0fa432d86aefd3bdb4bc50e29b3351f11fd892512407203f3e61636290ae15
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1.orig.tar.xz' attr_2.5.1.orig.tar.xz 318188 SHA512:9e5555260189bb6ef2440c76700ebb813ff70582eb63d446823874977307d13dfa3a347dfae619f8866943dfa4b24ccf67dadd7e3ea2637239fdb219be5d2932
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1.orig.tar.xz.asc' attr_2.5.1.orig.tar.xz.asc 833 SHA512:be4f3629ef66bd400bcdeaf8b6b1564dc729472a514d59fb4909a30f3269711dedea16002283e9aabbf83c374e0a3d70bc00f1136da0fed66a8184acdfd7e78f
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1-1build1.debian.tar.xz' attr_2.5.1-1build1.debian.tar.xz 28032 SHA512:c9d0869a3bb9f8019e6764fee3a78d8b1b9a3cdb37968aac19a9a7e7bbeeaadcbad86d5363ce3b0e26b5a178a4d446e4097d095e17b7a6d7f3e595d07176675c
```

### `dpkg` source package: `audit=1:3.0.7-1build1`

Binary Packages:

- `libaudit-common=1:3.0.7-1build1`
- `libaudit1:amd64=1:3.0.7-1build1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.0.7-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.0.7-1build1.dsc' audit_3.0.7-1build1.dsc 2771 SHA512:beb14e23239ab9c87dd4a57821d7d557a14a3e67f66306110ef87cd77cd2c07426f3bc8413d757618f886c5059e9bf624347753170708e0ad39b90f96fd51053
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.0.7.orig.tar.gz' audit_3.0.7.orig.tar.gz 1180226 SHA512:b5662b32082fc2ac54e247aa0db5442d76afa30134ebba1d624a17004e9ccf6856bb75344af4ce9d9a0a66c03e1c6f18b7d45658d7df13ea71af0c8362e08d70
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.0.7-1build1.debian.tar.xz' audit_3.0.7-1build1.debian.tar.xz 17772 SHA512:cdf346fc7dc04e42b44a9089fb7c01e68ea54ccd20d3eef8100d0cd8eed8ebd0764d8fd6ceab133faa0bfeee18e3cfe7625d230600b0e34ed0c19a7b739ec783
```

### `dpkg` source package: `avahi=0.8-5ubuntu5.2`

Binary Packages:

- `libavahi-client3:amd64=0.8-5ubuntu5.2`
- `libavahi-common-data:amd64=0.8-5ubuntu5.2`
- `libavahi-common3:amd64=0.8-5ubuntu5.2`

Licenses: (parsed from: `/usr/share/doc/libavahi-client3/copyright`, `/usr/share/doc/libavahi-common-data/copyright`, `/usr/share/doc/libavahi-common3/copyright`)

- `GPL`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris avahi=0.8-5ubuntu5.2
'http://security.ubuntu.com/ubuntu/pool/main/a/avahi/avahi_0.8-5ubuntu5.2.dsc' avahi_0.8-5ubuntu5.2.dsc 3756 SHA512:f0bb10a4442b9d37cdfd5bb2ec2cd5d40d8a94e5219b6c132de61800b8337f2a08d89bdc393b7e790a4afb5de08f262190f04c578903a090197fb5ce06281e53
'http://security.ubuntu.com/ubuntu/pool/main/a/avahi/avahi_0.8.orig.tar.gz' avahi_0.8.orig.tar.gz 1591458 SHA512:c6ba76feb6e92f70289f94b3bf12e5f5c66c11628ce0aeb3cadfb72c13a5d1a9bd56d71bdf3072627a76cd103b9b056d9131aa49ffe11fa334c24ab3b596c7de
'http://security.ubuntu.com/ubuntu/pool/main/a/avahi/avahi_0.8-5ubuntu5.2.debian.tar.xz' avahi_0.8-5ubuntu5.2.debian.tar.xz 45172 SHA512:7953ba54ebe1c44a501825ce2b19112850b7c0854a229633ebe3d89bfb3d9bfbbabe5030d5a22f24d65d70af5fdab52d3153f803ec321853368a36e3347cc9f0
```

### `dpkg` source package: `base-files=12ubuntu4.7`

Binary Packages:

- `base-files=12ubuntu4.7`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=12ubuntu4.7
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_12ubuntu4.7.dsc' base-files_12ubuntu4.7.dsc 1277 SHA512:9421fa1b62eb1c09d8aa93bb7c96ceaa077aaa4841ed5e516a682cfcc7cefdb7a7fd87976ba9e2718791fda2583141710968c4ce7357e089f5e5c3f7a0683ccf
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_12ubuntu4.7.tar.xz' base-files_12ubuntu4.7.tar.xz 81888 SHA512:e3a9f3188f6f43a53818200ac110f504f81b2819e301d69931a18fb34673541c11b2fc43af256e0c52f4a6daa6bd4b408b99ba432fa1b2b6624658bf312b0db5
```

### `dpkg` source package: `base-passwd=3.5.52build1`

Binary Packages:

- `base-passwd=3.5.52build1`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.5.52build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.5.52build1.dsc' base-passwd_3.5.52build1.dsc 1320 SHA512:2071171adf14d276664526662fab08d34a45a259ebcdbee7ae57bb004d3d12793e629006a37b649f16c0f04856e9f7bb79fb92fe304525167f48e73dec0cc4fd
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.5.52build1.tar.xz' base-passwd_3.5.52build1.tar.xz 54252 SHA512:699ffe50f4a7fbdea2c0b25d3b2452d538598870cf39b84668d9b7efa20ec41284c331513e89c966e7248732b1ec1abdfdb871e31f8e9efa026c691e89236ffe
```

### `dpkg` source package: `bash=5.1-6ubuntu1.1`

Binary Packages:

- `bash=5.1-6ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris bash=5.1-6ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1-6ubuntu1.1.dsc' bash_5.1-6ubuntu1.1.dsc 2409 SHA512:8adffecbfd9ffe55500fb70616e4b441bccb95fda13762dc2cccc3605a25f34851b142d2c633f17a5a7e426f0c5010ad76b0a70d375f923e25f6c9f4c893c8e4
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1.orig.tar.xz' bash_5.1.orig.tar.xz 5802740 SHA512:95d3acc542231cb893e1347c7d9dd66687f68cd347a0e9e126fde2d14e68c5b5530d1a5866eafa781e88aa013fcf72b4ad56d2e484c2ac7a69bd90bb149a9b86
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1-6ubuntu1.1.debian.tar.xz' bash_5.1-6ubuntu1.1.debian.tar.xz 99944 SHA512:d7fb6110df70232bd3280c1140a812a1903968792f6608481c184bd28760d03323ada75ed3ca4da4eb6c56a84781d6e2f441e0ee83dd9364a9e37fd0fa2211e9
```

### `dpkg` source package: `boost1.74=1.74.0-14ubuntu3`

Binary Packages:

- `libboost-filesystem1.74.0:amd64=1.74.0-14ubuntu3`
- `libboost-iostreams1.74.0:amd64=1.74.0-14ubuntu3`
- `libboost-locale1.74.0:amd64=1.74.0-14ubuntu3`
- `libboost-thread1.74.0:amd64=1.74.0-14ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libboost-filesystem1.74.0/copyright`, `/usr/share/doc/libboost-iostreams1.74.0/copyright`, `/usr/share/doc/libboost-locale1.74.0/copyright`, `/usr/share/doc/libboost-thread1.74.0/copyright`)

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
$ apt-get source -qq --print-uris boost1.74=1.74.0-14ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.74/boost1.74_1.74.0-14ubuntu3.dsc' boost1.74_1.74.0-14ubuntu3.dsc 10419 SHA512:5b7ca4310a2801712ff2cbca7091d38326b47da019b1ec4e86754dff8e546f09a837948812bfa7ce06b23f9e440bf88813fee93be5deb4ccd23e6beb0a4fe434
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.74/boost1.74_1.74.0.orig.tar.xz' boost1.74_1.74.0.orig.tar.xz 60536256 SHA512:a13dde2916054f527ffd816f4d58e8c5fe8b961380ebcbaa52e861884e8264b05e3ed7a5c6b24ccc49ea15d9bcbf75bd1fdcb2534efa5813133248083392afba
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.74/boost1.74_1.74.0-14ubuntu3.debian.tar.xz' boost1.74_1.74.0-14ubuntu3.debian.tar.xz 372512 SHA512:d5f8b742fd652cd7069a8f02f4992464f01d8532d51ca3ff4369f8383eebff52eda50c489c571dab453933601c13ab266895673cd8efdfa284154fc6d01dd89f
```

### `dpkg` source package: `brotli=1.0.9-2build6`

Binary Packages:

- `libbrotli1:amd64=1.0.9-2build6`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.0.9-2build6
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.9-2build6.dsc' brotli_1.0.9-2build6.dsc 1940 SHA512:9294702945cdaadad51f8690e7454d06b3281f94429123a4353cfdcce9eac598e9ad827f97f74798a7e958147aafec059022214b3bb7fe1db6337bebec2774b4
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.9.orig.tar.gz' brotli_1.0.9.orig.tar.gz 486984 SHA512:b8e2df955e8796ac1f022eb4ebad29532cb7e3aa6a4b6aee91dbd2c7d637eee84d9a144d3e878895bb5e62800875c2c01c8f737a1261020c54feacf9f676b5f5
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.9-2build6.debian.tar.xz' brotli_1.0.9-2build6.debian.tar.xz 5812 SHA512:a50a2e8ce37aa228c3074f657d5591cd509f6b34e78b3b16b044072886c184623994a6420e5c0759a2bab1df26ba69462692c7d2c59bdc72f9683b7df884771c
```

### `dpkg` source package: `bzip2=1.0.8-5build1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5build1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5build1.dsc' bzip2_1.0.8-5build1.dsc 1860 SHA512:dfb9cd3a99f8c80a27e088b6ba7f06f50bc2bdbc61f574ed8f77d0fa58ff07fa1c34a060351fd4b601537181143dd934caadd7a00eb97aea5933febb7b61743d
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5build1.debian.tar.bz2' bzip2_1.0.8-5build1.debian.tar.bz2 26870 SHA512:e030c257c3458d780fd0ffc6f328efd69d0e875e81acd7441a7c6651194ebded61017c96aad7c99061f93d50dfc33056abe98c9a599abc900f49d51c4a1eed6f
```

### `dpkg` source package: `ca-certificates-java=20190909ubuntu1.2`

Binary Packages:

- `ca-certificates-java=20190909ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/ca-certificates-java/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates-java=20190909ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates-java/ca-certificates-java_20190909ubuntu1.2.dsc' ca-certificates-java_20190909ubuntu1.2.dsc 1903 SHA512:032b574ee3b55656a248c02c4186942e92d2e35e598481b01ab253a16f00883faad5ef1a063666c7e62f307189713e81b5c82612a02c93e24b040930f01e97be
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates-java/ca-certificates-java_20190909ubuntu1.2.tar.xz' ca-certificates-java_20190909ubuntu1.2.tar.xz 17588 SHA512:b020e1121c82bc37b916c0a6a70f5d326dbc0dbf703507ae58911841207d22a1de3fe98b7ec5595c1179bb23ccf496563570f426a730bbf378493c5bf7b2a0d2
```

### `dpkg` source package: `ca-certificates=20240203~22.04.1`

Binary Packages:

- `ca-certificates=20240203~22.04.1`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203~22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e22.04.1.dsc' ca-certificates_20240203~22.04.1.dsc 1850 SHA512:af1c4a4a202eead02abba4808ce5e7b731f7e2db6b194e74ff9f5331b515213490ba63181f7ffc59f01f5bd13b7fe80519694c7ff21502cd7e2e095075896696
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e22.04.1.tar.xz' ca-certificates_20240203~22.04.1.tar.xz 263132 SHA512:64e97c5b258dfede258dd9b447d2a1f5a43db0e70309bb4e0259b8ed9d103e1a751fb563bb4902460667385d38325945e806726aa6db8876920dff670034f3f1
```

### `dpkg` source package: `cairo=1.16.0-5ubuntu2`

Binary Packages:

- `libcairo-gobject2:amd64=1.16.0-5ubuntu2`
- `libcairo2:amd64=1.16.0-5ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.16.0-5ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.16.0-5ubuntu2.dsc' cairo_1.16.0-5ubuntu2.dsc 2880 SHA512:e9415592136e7f42794f20d8c74fed895347a95d3ffd89621440c1e12212f65083926613e87fc6ad6df8f669058dc20ad12b2e1bdee2d7a7f85ec0b7c0dd4e26
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.16.0.orig.tar.xz' cairo_1.16.0.orig.tar.xz 41997432 SHA512:9eb27c4cf01c0b8b56f2e15e651f6d4e52c99d0005875546405b64f1132aed12fbf84727273f493d84056a13105e065009d89e94a8bfaf2be2649e232b82377f
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.16.0-5ubuntu2.debian.tar.xz' cairo_1.16.0-5ubuntu2.debian.tar.xz 33368 SHA512:d51b6655b5ea60420bb80252fbcfe2e31cbef6242043457195eab60716b84dc9ae68eb4de95214b10a5ec6d5675891067a4940b58c2249602f0f355b9d31d8d4
```

### `dpkg` source package: `cdebconf=0.261ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.261ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.261ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.261ubuntu1.dsc' cdebconf_0.261ubuntu1.dsc 2941 SHA512:18554e0d66831166d01e199612aa1cd43ed56e00995d62329f2c951143860bc413870acf71f4d0e72e228ce70e6a09c97d87750e5ada1a48beaf4b39d675084c
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.261ubuntu1.tar.xz' cdebconf_0.261ubuntu1.tar.xz 297016 SHA512:6c2c8e2dccdb923ae6dc6a6b3873e6a56f6bdc4a6298c0576f60cb8d5c63bd06c4b9dac4ada4abd0d672a4e54509ad558fc9d1424a8029568d8d86cb54926390
```

### `dpkg` source package: `chromaprint=1.5.1-2`

Binary Packages:

- `libchromaprint1:amd64=1.5.1-2`

Licenses: (parsed from: `/usr/share/doc/libchromaprint1/copyright`)

- `BSD-3-clause`
- `Expat`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris chromaprint=1.5.1-2
'http://archive.ubuntu.com/ubuntu/pool/universe/c/chromaprint/chromaprint_1.5.1-2.dsc' chromaprint_1.5.1-2.dsc 2253 SHA512:1511886baea07588c73d6add9a712e4648e671cc4a591d0aca58963eeff281898fbe893d37486e865659d961ca99a66f8f186a2309073b131fc8216981771504
'http://archive.ubuntu.com/ubuntu/pool/universe/c/chromaprint/chromaprint_1.5.1.orig.tar.gz' chromaprint_1.5.1.orig.tar.gz 1581159 SHA512:ea16e4d2b879c15b1d9b9ec93878da8b893f1834c70942663e1d2d106c2e0a661094fe2dd3bae7a6c2a1f9d5d8fab5e0b0ba493561090cf57b2228606fad1e66
'http://archive.ubuntu.com/ubuntu/pool/universe/c/chromaprint/chromaprint_1.5.1-2.debian.tar.xz' chromaprint_1.5.1-2.debian.tar.xz 7388 SHA512:66fbc42eddec9b9fd7d01d91251efeee05a5a754372e56d081c318e55d3a4ce8ea2fcf995f4b3c5f408c505ad7b3c44fc8167bf3adc98f5d4b55ce66c59ca655
```

### `dpkg` source package: `clucene-core=2.3.3.4+dfsg-1ubuntu5`

Binary Packages:

- `libclucene-contribs1v5:amd64=2.3.3.4+dfsg-1ubuntu5`
- `libclucene-core1v5:amd64=2.3.3.4+dfsg-1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libclucene-contribs1v5/copyright`, `/usr/share/doc/libclucene-core1v5/copyright`)

- `Apache-2.0`
- `LGPL-2.1`
- `Reuters-21578 - Distribution 1.0`

Source:

```console
$ apt-get source -qq --print-uris clucene-core=2.3.3.4+dfsg-1ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/c/clucene-core/clucene-core_2.3.3.4%2bdfsg-1ubuntu5.dsc' clucene-core_2.3.3.4+dfsg-1ubuntu5.dsc 2354 SHA512:2b5783b3c163fcd54e5d4d681a2786696ca4b7bc1a8e6f9d7887a423cc83dbc3ab418d5e94e3789bebc33893e2472c1393e969ec3a247cabb988e41c4ed8a9ee
'http://archive.ubuntu.com/ubuntu/pool/main/c/clucene-core/clucene-core_2.3.3.4%2bdfsg.orig.tar.xz' clucene-core_2.3.3.4+dfsg.orig.tar.xz 826688 SHA512:3b9fa81eb40f8c8e14c4a1bca8e48bbc62248163f7460ddd3f5f71410958ad6248b0f20215a691f70d96536039a63b300880f1aec29d2f785d9baf5be80c2a5a
'http://archive.ubuntu.com/ubuntu/pool/main/c/clucene-core/clucene-core_2.3.3.4%2bdfsg-1ubuntu5.debian.tar.xz' clucene-core_2.3.3.4+dfsg-1ubuntu5.debian.tar.xz 9320 SHA512:2d3ead78713fee2fec8f8116325eec5f168da9b66be9ba9f880014fc44a5aeac0e9644f9702672b1765fa472bb1ae65aef5a7ae3b3a8ab25fc7228488e995723
```

### `dpkg` source package: `codec2=1.0.1-3`

Binary Packages:

- `libcodec2-1.0:amd64=1.0.1-3`

Licenses: (parsed from: `/usr/share/doc/libcodec2-1.0/copyright`)

- `JMVBSD`
- `KISSFFTBSD`
- `LGPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris codec2=1.0.1-3
'http://archive.ubuntu.com/ubuntu/pool/universe/c/codec2/codec2_1.0.1-3.dsc' codec2_1.0.1-3.dsc 2601 SHA512:cc8fc307f99db9cd903cd87d051d5c0ec14f8e017bbac0938083eb887b222329424a5ad96efbb2ccc0643ac0001a76b3454f6ba0d020db54bac3541191c95564
'http://archive.ubuntu.com/ubuntu/pool/universe/c/codec2/codec2_1.0.1.orig-lpcnet.tar.gz' codec2_1.0.1.orig-lpcnet.tar.gz 33010724 SHA512:2213835930bd59f70ad67066b3ebfbafde2b1cdee0f191b0eace900322100178dcbb3538d0bb99ea8784266fdc31a6a2638d19dd9ea74a1febacc638a5993bbe
'http://archive.ubuntu.com/ubuntu/pool/universe/c/codec2/codec2_1.0.1.orig-lpcnet191005.tar.gz' codec2_1.0.1.orig-lpcnet191005.tar.gz 18396516 SHA512:ffa52c492f2ef1ca09c34b321b36d9dd26f6d3a2e807f4601858b45a1c6159b45b846bfaf3d37c74acead955c0ad47c2d06cb08b8347d5ec441cd751f2110167
'http://archive.ubuntu.com/ubuntu/pool/universe/c/codec2/codec2_1.0.1.orig.tar.gz' codec2_1.0.1.orig.tar.gz 15062219 SHA512:e32b6ebb5480b4a6ae15e835abc0da4fac7fb46a2b14bcc2a3c52df2da6c8d3f5acbcf83d8039f1ee402b4d2e1e7445841e3c9c415bfb70af3a251e74ab3f3b6
'http://archive.ubuntu.com/ubuntu/pool/universe/c/codec2/codec2_1.0.1-3.debian.tar.xz' codec2_1.0.1-3.debian.tar.xz 135608 SHA512:9e73eec0d45176227f1dff6c6dca50cc2b14813e0840441e3416c6de015a2aff6da357b0ee8a01c52f0f185ad7faf548ddc5696f180f03cc555c401fecb0f128
```

### `dpkg` source package: `coreutils=8.32-4.1ubuntu1.2`

Binary Packages:

- `coreutils=8.32-4.1ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils=8.32-4.1ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.32-4.1ubuntu1.2.dsc' coreutils_8.32-4.1ubuntu1.2.dsc 2299 SHA512:e6de4621a13517800b91a5990f4506c9d3287ee94346694a1844c4dff113288a2f8eb1bc6531b74096a4125f8a69c76ee59fd300cfe3a44867c8307ce878187f
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.32.orig.tar.xz' coreutils_8.32.orig.tar.xz 5547836 SHA512:1c8f3584efd61b4b02e7ac5db8e103b63cfb2063432caaf1e64cb2dcc56d8c657d1133bbf10bd41468d6a1f31142e6caa81d16ae68fa3e6e84075c253613a145
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.32.orig.tar.xz.asc' coreutils_8.32.orig.tar.xz.asc 833 SHA512:9c73b35c9e8f7c2b8eff317afcb5aa3234c5f41c80d1882f3c2342906f3fdc876ae45d1256dd1b8fd3cb58c50925f3c13f93de5018626634fdca3c72c14a9acb
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.32-4.1ubuntu1.2.debian.tar.xz' coreutils_8.32-4.1ubuntu1.2.debian.tar.xz 44868 SHA512:7718e917f8f2c5c5574e73a079ea8fd3b32bc898f2e12168dc3711dfdd896e4727283011050b80f65e60994fca49da031d70901d453612132764dca7dec99543
```

### `dpkg` source package: `cups=2.4.1op1-1ubuntu4.12`

Binary Packages:

- `libcups2:amd64=2.4.1op1-1ubuntu4.12`

Licenses: (parsed from: `/usr/share/doc/libcups2/copyright`)

- `Apache-2.0`
- `Apache-2.0-with-GPL2-LGPL2-Exception`
- `BSD-2-Clause`
- `BSD-2-clause`
- `FSFUL`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris cups=2.4.1op1-1ubuntu4.12
'http://archive.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.1op1-1ubuntu4.12.dsc' cups_2.4.1op1-1ubuntu4.12.dsc 3139 SHA512:c62fd1e0aa35c23293f36d7a47ce2068017ab9e853a5d6ced627d4c5fe9caccbbd4683496f5dfc7e9d294137a7fee52cc06363179865b5035377365f53782423
'http://archive.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.1op1.orig.tar.gz' cups_2.4.1op1.orig.tar.gz 8113914 SHA512:74e83728fcc3baf709176442b26711250fd4d4ede1e81e35b02a5607711067e28cd5a05d5bc3337953f6b2236c5a429b13f3a7f1218a08a2d3c30a8c9b0d96fd
'http://archive.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.1op1-1ubuntu4.12.debian.tar.xz' cups_2.4.1op1-1ubuntu4.12.debian.tar.xz 364860 SHA512:cff62fba42ca4c796ef321b26147a86e3a877acb80026227711a7588b2152b6aa80c16a5dadc4163534b024a7fb17b9eb97a16c8d9884d44564312b64fc94d15
```

### `dpkg` source package: `curl=7.81.0-1ubuntu1.21`

Binary Packages:

- `curl=7.81.0-1ubuntu1.21`
- `libcurl3-gnutls:amd64=7.81.0-1ubuntu1.21`
- `libcurl4:amd64=7.81.0-1ubuntu1.21`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`, `/usr/share/doc/libcurl4/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris curl=7.81.0-1ubuntu1.21
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0-1ubuntu1.21.dsc' curl_7.81.0-1ubuntu1.21.dsc 3143 SHA512:b5cb5133386b1888f4cf5d1909ea39b07afad56d95d94887995d9bb80b044ffacf3cce1cf9897954814cb269cc7e4d614fd8e3cd513faa19e270ebad6fcfdf34
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0.orig.tar.gz' curl_7.81.0.orig.tar.gz 4188040 SHA512:e3084f0fa083f7f93eac923edbfdddb5fd0a372b94673ba9d4427a2b95508898c15ecdf63b99a1c1f6cf3215e27b06cbaa2b7073df038d43b362e586f92495d3
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0.orig.tar.gz.asc' curl_7.81.0.orig.tar.gz.asc 488 SHA512:92bc5ede831551285d67b03abe8400c609ad31c9d33e324ee5c41b92dd5c2a0245a09a396bd76807b3e44bcfef944b1e16ac266264f7b85d27cc1c072a6e82bd
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0-1ubuntu1.21.debian.tar.xz' curl_7.81.0-1ubuntu1.21.debian.tar.xz 82928 SHA512:121de432d377a2789734aeb30a6e32cf771cf1b33e28931fb20cd2187a7612a8f5b54a00069b379bc21187f0596164008fe41646639b2bd951e741f59d27fba2
```

### `dpkg` source package: `cyrus-sasl2=2.1.27+dfsg2-3ubuntu1.2`

Binary Packages:

- `libsasl2-2:amd64=2.1.27+dfsg2-3ubuntu1.2`
- `libsasl2-modules-db:amd64=2.1.27+dfsg2-3ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-2-clause`
- `BSD-2.2-clause`
- `BSD-3-clause`
- `BSD-3-clause-JANET`
- `BSD-3-clause-PADL`
- `BSD-4-clause`
- `BSD-4-clause-UC`
- `FSFULLR`
- `GPL-3`
- `GPL-3+`
- `IBM-as-is`
- `MIT-CMU`
- `MIT-Export`
- `MIT-OpenVision`
- `OpenLDAP`
- `OpenSSL`
- `RSA-MD`
- `SSLeay`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27+dfsg2-3ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg2-3ubuntu1.2.dsc' cyrus-sasl2_2.1.27+dfsg2-3ubuntu1.2.dsc 3626 SHA512:fc67304c71b6bf7e5097bdb080ef0973ab873ff7558d91153066820c2f7d5983260586564760d6abd04c3e3fe7b076b474ae44bc97907cc2fb2757d4ca3cfe56
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg2.orig.tar.xz' cyrus-sasl2_2.1.27+dfsg2.orig.tar.xz 829892 SHA512:13337dfcc57ea8fec471ee0f2a0f6b58fb92907ad0899a4a8afaba957c5da302924e71c9fc4a61bbc913a4ee2ea74b05772cb26ed58d5724a312bb20a8b6a4cb
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg2-3ubuntu1.2.debian.tar.xz' cyrus-sasl2_2.1.27+dfsg2-3ubuntu1.2.debian.tar.xz 98836 SHA512:91457b1c476fae1b407f82304e6f651053ceaa923059e185b59e2be680038c2a38aab7749004b640ba604f7fdf51eb87a45e91671077207b8b8b4319e1bf24fb
```

### `dpkg` source package: `dash=0.5.11+git20210903+057cd650a4ed-3build1`

Binary Packages:

- `dash=0.5.11+git20210903+057cd650a4ed-3build1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `Expat`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.11+git20210903+057cd650a4ed-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.11%2bgit20210903%2b057cd650a4ed-3build1.dsc' dash_0.5.11+git20210903+057cd650a4ed-3build1.dsc 1834 SHA512:380a677ef7fcd2060f7806e4e552891393adb43bfba82498d143cd2ed4fa0cc7681e573a27bcb0991025a8323f6eb8b113aa1519cf455645556fad968cd26232
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.11%2bgit20210903%2b057cd650a4ed.orig.tar.xz' dash_0.5.11+git20210903+057cd650a4ed.orig.tar.xz 133320 SHA512:eced6bc60ca6ba4394a2ee65d8c6b88eca729c43e47053fc01dec5500ebe002a12f536c128c3fd821a2eb61b97e92c8a0be6d4532926479ce4b7d986be109cb7
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.11%2bgit20210903%2b057cd650a4ed-3build1.debian.tar.xz' dash_0.5.11+git20210903+057cd650a4ed-3build1.debian.tar.xz 42744 SHA512:7dd5b1bcaf76d8de19ad1647862e1140de59822c25d9ab1b42423f16de1e4c606ea393adac12f16a2ce9498d8f9553b8787fc31e5f93feefe36ab84b83402e1e
```

### `dpkg` source package: `dav1d=0.9.2-1`

Binary Packages:

- `libdav1d5:amd64=0.9.2-1`

Licenses: (parsed from: `/usr/share/doc/libdav1d5/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dav1d=0.9.2-1
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_0.9.2-1.dsc' dav1d_0.9.2-1.dsc 2332 SHA512:90c914fb2e059d442b921460fe742b2050e27896be0578337becb4a8a6fc3d5c8cbe0bb40c85800b082f35eae73e2f0cd23a80546875320ee884a5f4c4b775b6
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_0.9.2.orig.tar.xz' dav1d_0.9.2.orig.tar.xz 713352 SHA512:87026f8b14e408ff50fc8f137ec2ede4b14c5f69687e615d2359d0f718ae5cb5176522490786d9ae1f7838182f82615c2674f7c2961b6dcec83f1ee587c3af7c
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_0.9.2.orig.tar.xz.asc' dav1d_0.9.2.orig.tar.xz.asc 195 SHA512:04c367dcc3f2fb2e44cfa94653c2ca86e9fd9647959bfdd62ceb0007ad968e39550a90cb8fdc4ab9d330e5ef918200f91e186f3c6263ebf8295a8b076738b7d6
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_0.9.2-1.debian.tar.xz' dav1d_0.9.2-1.debian.tar.xz 7896 SHA512:6f3d8793c945f7392ffd29f5728fdd615bb4156a72ec993c1af8f4874ab6f5c28daaff86d99d19ea3d8adc13475c2e12da528cbf8375f5b355559094d50a52a9
```

### `dpkg` source package: `db5.3=5.3.28+dfsg1-0.8ubuntu3`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg1-0.8ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg1-0.8ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg1-0.8ubuntu3.dsc' db5.3_5.3.28+dfsg1-0.8ubuntu3.dsc 2875 SHA512:8743931f44f980d7be9ae77f5ce4b14ea260b780f33c8c6da66eb2fe4dba45a9c6b93237e91e2898ae0a76754ee789d67dd4efba7111f1360cb073ba633e1389
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg1.orig.tar.xz' db5.3_5.3.28+dfsg1.orig.tar.xz 19723860 SHA512:50cb87bc3f24065839ee2932e82af032b236b290ebe89983076f503c6c62c5f36ff93d7847a3f68b2b19f35088fbab5d3ac6a34553d07e8148e68e9a3f079a12
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg1-0.8ubuntu3.debian.tar.xz' db5.3_5.3.28+dfsg1-0.8ubuntu3.debian.tar.xz 32028 SHA512:9034be98df6c753b5f3faee9cbd1886e3e3c3d15c5840bc1c269a5034f6bfe9c4926c20591150b543618816051be218e6f00c3602b8b4325b0fcb193ddba804c
```

### `dpkg` source package: `dbus=1.12.20-2ubuntu4.1`

Binary Packages:

- `libdbus-1-3:amd64=1.12.20-2ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/libdbus-1-3/copyright`)

- `AFL-2.1`
- `AFL-2.1,`
- `BSD-3-clause`
- `BSD-3-clause-generic`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `Tcl-BSDish`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris dbus=1.12.20-2ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.12.20-2ubuntu4.1.dsc' dbus_1.12.20-2ubuntu4.1.dsc 3271 SHA512:161aca34132f46355d230c9acfe4860a5a05b6c881dfedae682f6553ce6e48e9a1cffd38c2097e4e320afbc6594de3ef391caaa5e94eaec64a28cfa69c7b8798
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.12.20.orig.tar.gz' dbus_1.12.20.orig.tar.gz 2095511 SHA512:0964683bc6859374cc94e42e1ec0cdb542cca67971c205fcba4352500b6c0891665b0718e7d85eb060c81cb82e3346c313892bc02384da300ddd306c7eef0056
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.12.20-2ubuntu4.1.debian.tar.xz' dbus_1.12.20-2ubuntu4.1.debian.tar.xz 65220 SHA512:2875cc688bc37a8b5c6a4e0bbb28a0a153709d70ddf8ee264d78ba44efdd0346776df86be493e9b68526387ae97a02abc76da7672abb5ca3537891fc455d1c2f
```

### `dpkg` source package: `dconf=0.40.0-3ubuntu0.1`

Binary Packages:

- `libdconf1:amd64=0.40.0-3ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libdconf1/copyright`)

- `GPL-3`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris dconf=0.40.0-3ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dconf/dconf_0.40.0-3ubuntu0.1.dsc' dconf_0.40.0-3ubuntu0.1.dsc 2791 SHA512:f4b72126e0ed20893279ddd4a2e6ee4a01e58beba74acb156ac0f7456a1f2050f1e8f58dd5004aaf4b44755121c561ef0007ea80af604a1931d659a1d59abcb0
'http://archive.ubuntu.com/ubuntu/pool/main/d/dconf/dconf_0.40.0.orig.tar.xz' dconf_0.40.0.orig.tar.xz 117764 SHA512:71396d71f24f47653181482b052fdfc63795c50c373de34e2fb93e16101745daa7e81192b79a102d5389911cea34138eedf3ac32bc80562018e8a7f31963559a
'http://archive.ubuntu.com/ubuntu/pool/main/d/dconf/dconf_0.40.0-3ubuntu0.1.debian.tar.xz' dconf_0.40.0-3ubuntu0.1.debian.tar.xz 11972 SHA512:5aa361319aa6303b344b29eb35a508efddb730239131ef6c9769f8ac9565544fd419ef1f82e780b8ca0ca04e06225b5ba54c62f97f60ceae9ac95a5a18091310
```

### `dpkg` source package: `debconf=1.5.79ubuntu1`

Binary Packages:

- `debconf=1.5.79ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.79ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.79ubuntu1.dsc' debconf_1.5.79ubuntu1.dsc 2077 SHA512:0aac451b347a5f6758ab2e468c25ea8061840519412210861a13ced479d5e6bb2a3abd469cb0cf68d80f1f9c4debba28501141055eb2eb1ac1701f800cdd83ba
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.79ubuntu1.tar.xz' debconf_1.5.79ubuntu1.tar.xz 570660 SHA512:1bf6de4d1cec7475f64d9bdaa47ef6dcb3d1181bcb3b97076ec60213534aa344ca49d552fdcb5c6fde4d42c364b8242bb4880de0a787493868383e6db36f9e5f
```

### `dpkg` source package: `debianutils=5.5-1ubuntu2`

Binary Packages:

- `debianutils=5.5-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.5-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.5-1ubuntu2.dsc' debianutils_5.5-1ubuntu2.dsc 1667 SHA512:333b9087e56e8f9a9ab95db556783a582b2855042e3dee292767decc4e4ad366bf32b4a30e60f5000a3ccced20ec613649fcd84563dae8e552a31273b42a170b
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.5.orig.tar.xz' debianutils_5.5.orig.tar.xz 104448 SHA512:230310428ee7c145c74bb666ae729754352295230f38ef4e22f7566970c5186d607cd827a5603a678815bd48d4a1eb2716f55c32494ec75eb665651da6a56e6a
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.5-1ubuntu2.debian.tar.xz' debianutils_5.5-1ubuntu2.debian.tar.xz 68420 SHA512:62fca780251fdb3b434abe840683385d3187699cf0466333fc1894a225f256ab1f912e818bbb4b564b1083c2e05a7a199bb9cdcc56307e60ba68cacef72644cf
```

### `dpkg` source package: `diffutils=1:3.8-0ubuntu2`

Binary Packages:

- `diffutils=1:3.8-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.8-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8-0ubuntu2.dsc' diffutils_3.8-0ubuntu2.dsc 1821 SHA512:645b14680e3669261eb372ce523d8258ee65b010b4e290650f8a0a4c922a26f80ee381e3711b2bf01249d64e248c184f8898abc6e0e50cb9f64cbd647ab1f684
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8.orig.tar.xz' diffutils_3.8.orig.tar.xz 1585120 SHA512:279441270987e70d5ecfaf84b6285a4866929c43ec877e50f154a788858d548a8a316f2fc26ad62f7348c8d289cb29a09d06dfadce1806e3d8b4ea88c8b1aa7c
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8.orig.tar.xz.asc' diffutils_3.8.orig.tar.xz.asc 833 SHA512:0464ac89209411993800666b45ff90243d22fbda53bf1d71c6870d565b39cc8d9c54c141b9d297a181ce74ad8fb5313953f416bced179ff7728a52a3e9a4f5a5
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8-0ubuntu2.debian.tar.xz' diffutils_3.8-0ubuntu2.debian.tar.xz 11692 SHA512:fab99ca407c3b1bbc427ebf14595d540e6ad2957e9b43065005efd9d5b423e6a4d6d460cccd05faf5786193a5bf1cf46721743e580161d5004167eca15fc405b
```

### `dpkg` source package: `dpkg=1.21.1ubuntu2.6`

Binary Packages:

- `dpkg=1.21.1ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.21.1ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.21.1ubuntu2.6.dsc' dpkg_1.21.1ubuntu2.6.dsc 2254 SHA512:e5d28c73b84700cdbeb0f9f204e328538972dddd110fb6623eb1bdf0d85988000799408d564cb2b3c4af94b4d9bacf1a8eafb312a1e676bdd6518340082e44a4
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.21.1ubuntu2.6.tar.xz' dpkg_1.21.1ubuntu2.6.tar.xz 5017128 SHA512:2eb70e5ca3e2d0cafe460eb5236e81c3312e84426d5732cbc64952702e8e81fe9119d06a51fed1e9b72c58db8a9d4484ca6dddf5b92be351eb5a2c75ddd3c06c
```

### `dpkg` source package: `e2fsprogs=1.46.5-2ubuntu1.2`

Binary Packages:

- `e2fsprogs=1.46.5-2ubuntu1.2`
- `libcom-err2:amd64=1.46.5-2ubuntu1.2`
- `libext2fs2:amd64=1.46.5-2ubuntu1.2`
- `libss2:amd64=1.46.5-2ubuntu1.2`
- `logsave=1.46.5-2ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `GPL-2`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.46.5-2ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5-2ubuntu1.2.dsc' e2fsprogs_1.46.5-2ubuntu1.2.dsc 3190 SHA512:8bf3cf7816ff7a774b03e846fcd90083083c1cd9072635d1eb45ba76c87ea8a1d9f7c5bf99f9a80ad1fed2c294425835ff801ada260b3417258d94cee3dc3758
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5.orig.tar.gz' e2fsprogs_1.46.5.orig.tar.gz 9530158 SHA512:1a3496cb6ac575c7a5c523cc4eede39bc77c313a6d1fea2d303fc967792d75d94e42d7821e1a61b7513509320aae4a7170506decf5753ddbd1dda9d304cc392e
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5.orig.tar.gz.asc' e2fsprogs_1.46.5.orig.tar.gz.asc 488 SHA512:b288fa2418a85750673743cb58faf10537e2c79a5c2ec8b0d59435316f00006424195556ccf78fa023b67b05a29cd85bf9d96c14c166847d71a1d79b189c1d05
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5-2ubuntu1.2.debian.tar.xz' e2fsprogs_1.46.5-2ubuntu1.2.debian.tar.xz 86604 SHA512:acb7f22a63d9c0e58d626af655cdcb6e6cfcedafdd7edbc6b7b757d1b388ee04c416db98c577a8cdf2259c46ea16a679f9be770374515b21d93bd0af66bd2a1d
```

### `dpkg` source package: `elfutils=0.186-1ubuntu0.1`

Binary Packages:

- `libdw1:amd64=0.186-1ubuntu0.1`
- `libelf1:amd64=0.186-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libdw1/copyright`, `/usr/share/doc/libelf1/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris elfutils=0.186-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.186-1ubuntu0.1.dsc' elfutils_0.186-1ubuntu0.1.dsc 3349 SHA512:3c7407825a9f408f35be6d986ba60ce253e1dd652073bdb61e1fcaa619bd7f71e7aae032803c61db3ad32580dcd1c660e59fdf1c7ba2a16c3643467816deb32d
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.186.orig.tar.bz2' elfutils_0.186.orig.tar.bz2 9230491 SHA512:c9180b27ec62935f18b9431268d176f6023d1bb938731d2af6e7626ae460af6608a70ba68483aa1ec7e6cb0fa0528b661ca8b68bc4f58ea8e18af527c5950c78
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.186-1ubuntu0.1.debian.tar.xz' elfutils_0.186-1ubuntu0.1.debian.tar.xz 39200 SHA512:e19fb6558f7acd320d1498f34481b5224e610b5170656f16d5b8cd5309a758aea92fec0c5b005157164845416c16d265c923774d70c572355441bbaa81da72c4
```

### `dpkg` source package: `expat=2.4.7-1ubuntu0.6`

Binary Packages:

- `libexpat1:amd64=2.4.7-1ubuntu0.6`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.4.7-1ubuntu0.6
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7-1ubuntu0.6.dsc' expat_2.4.7-1ubuntu0.6.dsc 1491 SHA512:b127ec7ab60ea354ed05bccc38b4f022d4c62e2778e0f7b68a7da2d06910281d1833642b1cecb9a63d4a875adce31e4d992a4f894e6d8b21109f553980c3a260
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7.orig.tar.gz' expat_2.4.7.orig.tar.gz 8316374 SHA512:91bc9792c4ba1d0ad835f633d8cfa62130692f48308eea8932ec5e13a01542120561b0f255b4adc58b1adae6f83632cbabf428b5b5c0d2ac6de542478a951232
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7-1ubuntu0.6.debian.tar.xz' expat_2.4.7-1ubuntu0.6.debian.tar.xz 36504 SHA512:02f1657eb320a635fcceda6b2f7e2757df02c106da9a475e230f58c32178bc4e481162d635eb7a8b8d72644704d427fcbc04b98e94ef61fafa0cf898f651cd4b
```

### `dpkg` source package: `ffmpeg=7:4.4.2-0ubuntu0.22.04.1`

Binary Packages:

- `ffmpeg=7:4.4.2-0ubuntu0.22.04.1`
- `libavcodec58:amd64=7:4.4.2-0ubuntu0.22.04.1`
- `libavdevice58:amd64=7:4.4.2-0ubuntu0.22.04.1`
- `libavfilter7:amd64=7:4.4.2-0ubuntu0.22.04.1`
- `libavformat58:amd64=7:4.4.2-0ubuntu0.22.04.1`
- `libavutil56:amd64=7:4.4.2-0ubuntu0.22.04.1`
- `libpostproc55:amd64=7:4.4.2-0ubuntu0.22.04.1`
- `libswresample3:amd64=7:4.4.2-0ubuntu0.22.04.1`
- `libswscale5:amd64=7:4.4.2-0ubuntu0.22.04.1`

Licenses: (parsed from: `/usr/share/doc/ffmpeg/copyright`, `/usr/share/doc/libavcodec58/copyright`, `/usr/share/doc/libavdevice58/copyright`, `/usr/share/doc/libavfilter7/copyright`, `/usr/share/doc/libavformat58/copyright`, `/usr/share/doc/libavutil56/copyright`, `/usr/share/doc/libpostproc55/copyright`, `/usr/share/doc/libswresample3/copyright`, `/usr/share/doc/libswscale5/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris ffmpeg=7:4.4.2-0ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/universe/f/ffmpeg/ffmpeg_4.4.2-0ubuntu0.22.04.1.dsc' ffmpeg_4.4.2-0ubuntu0.22.04.1.dsc 5669 SHA512:9741833906d1fe8c7064917db224628376da978bfdfb4949e3299c9ddbdc8d75342c68a385118e1475fad5cfbec59c47935ebf1e7490a36e16f70ff4f317ba62
'http://archive.ubuntu.com/ubuntu/pool/universe/f/ffmpeg/ffmpeg_4.4.2.orig.tar.xz' ffmpeg_4.4.2.orig.tar.xz 9562968 SHA512:abce847c607ac6d63fe32ceff8bf8724888acf2b7db9a083cba50e3235590cdcb27feb7e0a314133d0030809fb54d474f64001fc9ab7d896a819159869c09d5a
'http://archive.ubuntu.com/ubuntu/pool/universe/f/ffmpeg/ffmpeg_4.4.2.orig.tar.xz.asc' ffmpeg_4.4.2.orig.tar.xz.asc 520 SHA512:a4df97a6328fc076b5611023bd61254f1a5043db1ec2f3426bee305206b2b0937047ede9cb51db31a3387a16218fe95a7a40296770574fa32660118938a9d301
'http://archive.ubuntu.com/ubuntu/pool/universe/f/ffmpeg/ffmpeg_4.4.2-0ubuntu0.22.04.1.debian.tar.xz' ffmpeg_4.4.2-0ubuntu0.22.04.1.debian.tar.xz 54484 SHA512:4a5ecfddfc55178ff624b8742bd2037133297f0305984d0ab3b10bc937afc050a96f9bd8452310fe61fe397eeeaddc9d0c48ee4a4e160dfe6d740a20d2994f2a
```

### `dpkg` source package: `fftw3=3.3.8-2ubuntu8`

Binary Packages:

- `libfftw3-double3:amd64=3.3.8-2ubuntu8`

Licenses: (parsed from: `/usr/share/doc/libfftw3-double3/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.8-2ubuntu8
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.8-2ubuntu8.dsc' fftw3_3.3.8-2ubuntu8.dsc 2673 SHA512:f0e7a1991fe120a3048d22a02f90adf7d934ad95a82ecc36360fa760a5125cf58d3e2dc6167dc847723af6f61720f95019895fcb8f8d0fc6902e39017aed944c
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.8.orig.tar.gz' fftw3_3.3.8.orig.tar.gz 4110137 SHA512:ab918b742a7c7dcb56390a0a0014f517a6dff9a2e4b4591060deeb2c652bf3c6868aa74559a422a276b853289b4b701bdcbd3d4d8c08943acf29167a7be81a38
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.8-2ubuntu8.debian.tar.xz' fftw3_3.3.8-2ubuntu8.debian.tar.xz 14356 SHA512:99280a373b3c5a19d472e8bd23495759aa905aec12c3c01b3f3399fd1a300b4a0cb847369efad9690ec85bf8e9206428f9bf707edc0c665485362aa6cfaf1722
```

### `dpkg` source package: `findutils=4.8.0-1ubuntu3`

Binary Packages:

- `findutils=4.8.0-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.8.0-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.8.0-1ubuntu3.dsc' findutils_4.8.0-1ubuntu3.dsc 2064 SHA512:3f0f5195138342ce515ff83f5e653457d78158c8b871ef04002adb4cc69cab6023c71f7d1032db7032d25806c22a8ad33dbf3007018d382968863521a33af2cd
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.8.0.orig.tar.xz' findutils_4.8.0.orig.tar.xz 1983096 SHA512:eaa2da304dbeb2cd659b9210ac37da1bde4cd665c12a818eca98541c5ed5cba1050641fc0c39c0a446a5a7a87a8d654df0e0e6b0cee21752ea485188c9f1071e
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.8.0.orig.tar.xz.asc' findutils_4.8.0.orig.tar.xz.asc 488 SHA512:e6ea8bd9a58ac4f787a9cc7dad9f75fab9e0623e7cda463bef60651c9319574ac7c8ba06f7d33cbead0ecb8788db71eb39f50550deb066d6d6baa625b0374a45
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.8.0-1ubuntu3.debian.tar.xz' findutils_4.8.0-1ubuntu3.debian.tar.xz 27716 SHA512:f0ce8b61f4e0beabad3178424c804468dc4c57f37794887954df28c36227ce77f00383903274a1995a104f9def44270070b9e033eb46d52f5aaaedb1f5883587
```

### `dpkg` source package: `flac=1.3.3-2ubuntu0.2`

Binary Packages:

- `libflac8:amd64=1.3.3-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libflac8/copyright`)

- `BSD-3-clause`
- `GFDL-1.1+`
- `GFDL-1.2`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Public-domain`

Source:

```console
$ apt-get source -qq --print-uris flac=1.3.3-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/f/flac/flac_1.3.3-2ubuntu0.2.dsc' flac_1.3.3-2ubuntu0.2.dsc 2356 SHA512:50a0f450ce5294b054ec31634c6e4ea8ee95a1cbe6ffa6266ec54925a51034286ccfbfcc74e6e9f9e4d248c69cad5de13cdc3b2cf50717960d6cb8cc11063d51
'http://archive.ubuntu.com/ubuntu/pool/main/f/flac/flac_1.3.3.orig.tar.xz' flac_1.3.3.orig.tar.xz 1044472 SHA512:d6417e14fab0c41b2df369e5e39ce62a5f588e491af4d465b0162f74e171e5549b2f061867f344bfbf8aaccd246bf5f2acd697e532a2c7901c920c69429b1a28
'http://archive.ubuntu.com/ubuntu/pool/main/f/flac/flac_1.3.3-2ubuntu0.2.debian.tar.xz' flac_1.3.3-2ubuntu0.2.debian.tar.xz 19988 SHA512:82d452a573989a27aae0a4abbe9d422d30ebf41d05c7456aa683b35671d424197d36f82f8658d8e11dbb3ffc142156a99809b871d287de471698f3d8afe7b7f4
```

### `dpkg` source package: `flite=2.2-3`

Binary Packages:

- `libflite1:amd64=2.2-3`

Licenses: (parsed from: `/usr/share/doc/libflite1/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris flite=2.2-3
'http://archive.ubuntu.com/ubuntu/pool/universe/f/flite/flite_2.2-3.dsc' flite_2.2-3.dsc 2197 SHA512:6b8362cbb5f5e4337a3c303530269af9fcd525fa6beff66fa5c58f56e36eb9d4de02314c96b18fdf86e73f9abd2a511003e651bc0d0c354157c9a5559cbcc0b2
'http://archive.ubuntu.com/ubuntu/pool/universe/f/flite/flite_2.2.orig.tar.gz' flite_2.2.orig.tar.gz 20233792 SHA512:1ca2f4145651490ef8405fdb830a3b42e885020a7603d965f6a5581b01bed41047d396b38c2ceab138fc0b28d28078db17acd2b5a84c6444cb99d65c581afa72
'http://archive.ubuntu.com/ubuntu/pool/universe/f/flite/flite_2.2-3.debian.tar.xz' flite_2.2-3.debian.tar.xz 48452 SHA512:660e812ca3efef386276eaccd4cd4d6012097c3c27443c9fa87cce8ccf86648543bc3c3e902557f12969b4e6fb907e62fdba81360a60f10b3457aed349dace84
```

### `dpkg` source package: `fontconfig=2.13.1-4.2ubuntu5`

Binary Packages:

- `fontconfig=2.13.1-4.2ubuntu5`
- `fontconfig-config=2.13.1-4.2ubuntu5`
- `libfontconfig1:amd64=2.13.1-4.2ubuntu5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.13.1-4.2ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.13.1-4.2ubuntu5.dsc' fontconfig_2.13.1-4.2ubuntu5.dsc 2449 SHA512:7d56f8d3b7f211ad464d20ed07b02cf38b0c10df1aa00ca8e899a734908b3342b1d67e32107231f983e473f64366444f06adb3b9c72cc2c2693aed427dda5114
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.13.1.orig.tar.bz2' fontconfig_2.13.1.orig.tar.bz2 1723639 SHA512:f97f2a9db294fd72d416a7d76dd7db5934ade2cf76903764b09e7decc33e0e2eed1a1d35c5f1c7fd9ea39e2c7653b9e65365f0c6205e047e95e38ba5000dd100
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.13.1-4.2ubuntu5.debian.tar.xz' fontconfig_2.13.1-4.2ubuntu5.debian.tar.xz 28084 SHA512:6321dd705cc0adb9330778675f4ee3545d7f22f1ec63439dab45592dda121c2c5f1b4aa8ae444db1151906c5e1f363f13f38075733649b543e4d5bf5222c0eed
```

### `dpkg` source package: `fonts-urw-base35=20200910-1`

Binary Packages:

- `fonts-urw-base35=20200910-1`

Licenses: (parsed from: `/usr/share/doc/fonts-urw-base35/copyright`)

- `AGPL-3`
- `AGPL-3 with Font exception`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fonts-urw-base35=20200910-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-urw-base35/fonts-urw-base35_20200910-1.dsc' fonts-urw-base35_20200910-1.dsc 2061 SHA512:c49491d4a4cf3ffcceab733e64de6bcd460273d884b9db9cd74bb861cec5a01981e946f05b065351c631e376239f94cb2c8927675f8d95a82efd469bb82a4794
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-urw-base35/fonts-urw-base35_20200910.orig.tar.gz' fonts-urw-base35_20200910.orig.tar.gz 11190093 SHA512:71fb27baadf5abc4ff624cdede02038681acd5fffdc728a5b2e7808713b80cb2f2174f90a1862e69d390c4434c49d5167ab095100032fa3ba80b586eb8ae51d1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-urw-base35/fonts-urw-base35_20200910-1.debian.tar.xz' fonts-urw-base35_20200910-1.debian.tar.xz 17772 SHA512:ca14ee4917425f04197c481139831dbc07e5cd0dca316b464ca6f67639077fd39d5d17dea4d00b6bce02a6338ba43b40b520cb8210cec9951255a4ab7093f7dd
```

### `dpkg` source package: `freetype=2.11.1+dfsg-1ubuntu0.3`

Binary Packages:

- `libfreetype6:amd64=2.11.1+dfsg-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `FSFAP`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `OpenGroup-BSD-like`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.11.1+dfsg-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg-1ubuntu0.3.dsc' freetype_2.11.1+dfsg-1ubuntu0.3.dsc 3791 SHA512:956ef790ec1f6cd70d35dd4b47217e9268f909478672946b85d43a5d08c368ded5524a9e71a1c2cce003b6341291b04d1cfd831fc8a6b0b70b7880caaa0a189b
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2demos.tar.xz' freetype_2.11.1+dfsg.orig-ft2demos.tar.xz 257240 SHA512:93d68daefa8a49b4fc987a7356133299fe2a8e012415ea09ad7616ececcfd978fdf9fc7a2d855f7488f51a497d019acb89ef5774484babae66357b3083a883c5
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.11.1+dfsg.orig-ft2demos.tar.xz.asc 195 SHA512:407ffade07cc62c8838d26670dffc7c26b9baf4984c42b2b2467279dabda855536b403f5a7e9dc64a787163657ca81019fef6d1879973faf180d6230ab17cd05
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2docs.tar.xz' freetype_2.11.1+dfsg.orig-ft2docs.tar.xz 2038348 SHA512:c5e19d98425491682edc58230c48390925cc4b466169f655cf3b8575ba787a70feecdeb7a16224b132dcc32f17b041483d84056cda8e3132d98b531e46a26c36
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.11.1+dfsg.orig-ft2docs.tar.xz.asc 195 SHA512:df946695a1fbaa71009f48a8f0860177984728ec1c73385d1e55c07be027dd6a5e634c9dcbb49c51f8143b0d56a6cbf06393403341fb28cea7a8a2cc9a9c5592
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig.tar.xz' freetype_2.11.1+dfsg.orig.tar.xz 1988020 SHA512:6a9a0379679abf127761cabb2da39b8faf2ca4c322075da9b86d93363ac81ce909b9544377a784118ba91ca008baa680b9da474bd2da1bfe928d5a4c9114cb08
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg-1ubuntu0.3.debian.tar.xz' freetype_2.11.1+dfsg-1ubuntu0.3.debian.tar.xz 42292 SHA512:068774dbcbd393912de1b89323f856121269e2031e662e8473372b1849e7b3d26714f2eb9d7623b49136c7b448b3267959f2c158557fbf771ef294ea799097dc
```

### `dpkg` source package: `fribidi=1.0.8-2ubuntu3.1`

Binary Packages:

- `libfribidi0:amd64=1.0.8-2ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.8-2ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.8-2ubuntu3.1.dsc' fribidi_1.0.8-2ubuntu3.1.dsc 2442 SHA512:977cb7df4e1877f0f6d5f58620cfacbb1e25090c2bfd70c71576ada3c9f11f260ed11fb0fd64a5f5bf8cfc8c419a865e0e9b9084f224deb9dfadf1b2e3bd17e9
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.8.orig.tar.bz2' fribidi_1.0.8.orig.tar.bz2 2077095 SHA512:d66b1524b26d227fd6a628f438efb875c023ae3be708acaaad11f1f62d0902de0a5f57124458291ef2b0fcd89356c52ab8ae5559b0b5a93fa435b92f1d098ba2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.8-2ubuntu3.1.debian.tar.xz' fribidi_1.0.8-2ubuntu3.1.debian.tar.xz 10888 SHA512:16e448db2038b60b3a086117774e734b1d3ed08ae09cfa1b591f5a95c6372778705ba8940dd464537d5a6e932528c1c1e01376670992580529090f20142d171a
```

### `dpkg` source package: `game-music-emu=0.6.3-2`

Binary Packages:

- `libgme0:amd64=0.6.3-2`

Licenses: (parsed from: `/usr/share/doc/libgme0/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris game-music-emu=0.6.3-2
'http://archive.ubuntu.com/ubuntu/pool/universe/g/game-music-emu/game-music-emu_0.6.3-2.dsc' game-music-emu_0.6.3-2.dsc 2030 SHA512:8f177d074077fc51d3682f7b751e79bc9295f871fceccd5490e5ef8e81a78adf4c3848c6b7715e4128b047ddf83e607b639c90e1c80b85f0e5e4f2d8a1b51410
'http://archive.ubuntu.com/ubuntu/pool/universe/g/game-music-emu/game-music-emu_0.6.3.orig.tar.xz' game-music-emu_0.6.3.orig.tar.xz 234412 SHA512:4b20c69ced696bb879c34bcb7ce0f5f276642458d4cebca8ede673eed7d50664e527626e2077f85a3411a26660f1b3f01e43cccd72945e1edb2994421efeb552
'http://archive.ubuntu.com/ubuntu/pool/universe/g/game-music-emu/game-music-emu_0.6.3-2.debian.tar.xz' game-music-emu_0.6.3-2.debian.tar.xz 4284 SHA512:3aa6b247cc2ecaa9baa9e97355c1081a024bb971f732189ef3bbcfa99fe716350e1b9854f52e7d3e279e7dbcbaef0b046fc57b9b96284b7960cb67fd854c006c
```

### `dpkg` source package: `gcc-12=12.3.0-1ubuntu1~22.04.2`

Binary Packages:

- `gcc-12-base:amd64=12.3.0-1ubuntu1~22.04.2`
- `libgcc-s1:amd64=12.3.0-1ubuntu1~22.04.2`
- `libgfortran5:amd64=12.3.0-1ubuntu1~22.04.2`
- `libgomp1:amd64=12.3.0-1ubuntu1~22.04.2`
- `libquadmath0:amd64=12.3.0-1ubuntu1~22.04.2`
- `libstdc++6:amd64=12.3.0-1ubuntu1~22.04.2`

Licenses: (parsed from: `/usr/share/doc/gcc-12-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-12=12.3.0-1ubuntu1~22.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0-1ubuntu1%7e22.04.2.dsc' gcc-12_12.3.0-1ubuntu1~22.04.2.dsc 27845 SHA512:4189e457350c0a6f43a4c9b96df4d4cea23ad97b18c7b5592b7a1e27e66cedb30c03e2d71c1496be2157e38900344bcd6171c389bd803e5d14093530528e19a8
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0.orig.tar.gz' gcc-12_12.3.0.orig.tar.gz 91555468 SHA512:a33ce506594e13cf96f0419e6d62b71f8906c87c69426218bf8679d281865f1b170bc2f7379216ae1d6ad9f6bdbf5819c34c65c7537fdb74179c27b0d4ab7b48
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0-1ubuntu1%7e22.04.2.debian.tar.xz' gcc-12_12.3.0-1ubuntu1~22.04.2.debian.tar.xz 587544 SHA512:84c4e03cba3f408e752690a34b32fa1e231b501ebd502e4cb4843d74fda287704ff60b8be1d6482297f987fa4ab651a0a605fde27dfdbd364cf7ef2c03e39847
```

### `dpkg` source package: `gdk-pixbuf=2.42.8+dfsg-1ubuntu0.4`

Binary Packages:

- `libgdk-pixbuf-2.0-0:amd64=2.42.8+dfsg-1ubuntu0.4`
- `libgdk-pixbuf2.0-common=2.42.8+dfsg-1ubuntu0.4`

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
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.8+dfsg-1ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.8%2bdfsg-1ubuntu0.4.dsc' gdk-pixbuf_2.42.8+dfsg-1ubuntu0.4.dsc 3238 SHA512:9037c66cb7fd221a38e36d36d42177c440d8ab98ad87cbeedde45ff4381156bb659fba7ec28c171b6f058625618cd490aefcfc5f42456dc6fb6054e6eae2e91c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.8%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.8+dfsg.orig.tar.xz 6439548 SHA512:d77093ac4bd5c8f9a5267e67958dd99db009e16f94c44be95a547cd291b6d03fcc35c4a02327dd9f4341af1ae2ecdaa6a1bec02dcf1116ec5a440d22b3f68924
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.8%2bdfsg-1ubuntu0.4.debian.tar.xz' gdk-pixbuf_2.42.8+dfsg-1ubuntu0.4.debian.tar.xz 29736 SHA512:5f88b7e49f1ffdb70ab6560e96f0ecacd83b7c4e7d980593e06f128c15c84139462918e65c034d231463070618fa5e38fd65e8d083d1bbfda2ae656e7592e911
```

### `dpkg` source package: `ghostscript=9.55.0~dfsg1-0ubuntu5.13`

Binary Packages:

- `ghostscript=9.55.0~dfsg1-0ubuntu5.13`
- `libgs9:amd64=9.55.0~dfsg1-0ubuntu5.13`
- `libgs9-common=9.55.0~dfsg1-0ubuntu5.13`

Licenses: (parsed from: `/usr/share/doc/ghostscript/copyright`, `/usr/share/doc/libgs9/copyright`, `/usr/share/doc/libgs9-common/copyright`)

- `AGPL-3`
- `AGPL-3+`
- `AGPL-3+ with font exception`
- `Adobe-2006`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause~Adobe`
- `Expat`
- `Expat~Ghostgum`
- `Expat~SunSoft`
- `Expat~SunSoft with SunSoft exception`
- `FTL`
- `GAP~configure`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `ISC`
- `LGPL-2.1`
- `MIT-Open-Group`
- `NTP~Lucent`
- `NTP~WSU`
- `X11`
- `ZLIB`
- `custom`
- `none`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris ghostscript=9.55.0~dfsg1-0ubuntu5.13
'http://archive.ubuntu.com/ubuntu/pool/main/g/ghostscript/ghostscript_9.55.0%7edfsg1-0ubuntu5.13.dsc' ghostscript_9.55.0~dfsg1-0ubuntu5.13.dsc 2818 SHA512:ee2688f9ba4419d022f208d81ddba065d2a1005bd1935572ef7e3fe87c7cc4e7603b66bba8da807bf6a1c4cbcca8d69018f021958418ad8b27d2fd4af6703e4e
'http://archive.ubuntu.com/ubuntu/pool/main/g/ghostscript/ghostscript_9.55.0%7edfsg1.orig.tar.xz' ghostscript_9.55.0~dfsg1.orig.tar.xz 53473556 SHA512:fb6dec73b8a1d88a6fe624d23549162f4e29059f41145aeb9bf96c09a7fb5e415fc15be5e2dbbcd21f49ecb2a91c78bc4f0d14eee8b3fe32884b405f0e709b93
'http://archive.ubuntu.com/ubuntu/pool/main/g/ghostscript/ghostscript_9.55.0%7edfsg1-0ubuntu5.13.debian.tar.xz' ghostscript_9.55.0~dfsg1-0ubuntu5.13.debian.tar.xz 189024 SHA512:0d7893184421059b103e53450bc76f619046bc9ae6c7b20b8dadcd9ce7b9d4102563e43e924fec387323532837c89bf93e4a9a26a565b93a6152c24280caa332
```

### `dpkg` source package: `giflib=5.1.9-2ubuntu0.1`

Binary Packages:

- `libgif7:amd64=5.1.9-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libgif7/copyright`)

- `ISC`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris giflib=5.1.9-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/giflib/giflib_5.1.9-2ubuntu0.1.dsc' giflib_5.1.9-2ubuntu0.1.dsc 1929 SHA512:fd432370bfb030891d61bfca3787d3671ebe42f3dba931f0fe52fbcb694ce31f3c13ad2e8eaa8a7b20de3725bdf59764ed4046a03610b32aae48c0fb8871efcd
'http://archive.ubuntu.com/ubuntu/pool/main/g/giflib/giflib_5.1.9.orig.tar.bz2' giflib_5.1.9.orig.tar.bz2 336304 SHA512:f1e0c91fb90c7bf3f2b073f79b1bd4041df5178ff2e5b93975158fc2c6dd6c8ac888f8ff95c3a1804f988ce09154539c20a3196a40704b4d42a0f5846155e0ea
'http://archive.ubuntu.com/ubuntu/pool/main/g/giflib/giflib_5.1.9-2ubuntu0.1.debian.tar.xz' giflib_5.1.9-2ubuntu0.1.debian.tar.xz 11128 SHA512:67166988b9bb5d4bc08ce41971391c24d4e5d5adce8292f2b167c55bc7c38897741e0ebf974296c22e232f93813f3137fc1ee21addb046a46c1dc89c0b14e8ee
```

### `dpkg` source package: `glib2.0=2.72.4-0ubuntu2.6`

Binary Packages:

- `libglib2.0-0:amd64=2.72.4-0ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0/copyright`)

- `Expat`
- `GPL-2+`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.72.4-0ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.72.4-0ubuntu2.6.dsc' glib2.0_2.72.4-0ubuntu2.6.dsc 3670 SHA512:63c4745c87f1e7f9d2673cf30ce10a64f7e652aacebd443030fadf5660bb92e6fff5622570ff5983b26a602252917e5810e019882d60223f5a3bc762083403ae
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.72.4.orig.tar.xz' glib2.0_2.72.4.orig.tar.xz 4884256 SHA512:b4e2e0985e2184ee9656c4f1b4e15d8d1264f3d23d31349bc43d92e8432cffa48e1685c40517efb08dc5b57b8285acf65f2747deeb50e50d9cacec7160e7edf8
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.72.4-0ubuntu2.6.debian.tar.xz' glib2.0_2.72.4-0ubuntu2.6.debian.tar.xz 150472 SHA512:191c2e94d5bbb5ab0b4bd2009fe23a43ea9248173974876a8f24e5145474b1195b284b0b37317433bd46fec7d21908b45550c67c3118019a30aace1ef98058cf
```

### `dpkg` source package: `glibc=2.35-0ubuntu3.11`

Binary Packages:

- `libc-bin=2.35-0ubuntu3.11`
- `libc6:amd64=2.35-0ubuntu3.11`
- `locales=2.35-0ubuntu3.11`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/locales/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.35-0ubuntu3.11
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35-0ubuntu3.11.dsc' glibc_2.35-0ubuntu3.11.dsc 8888 SHA512:513445f41ac47bc28f9c30bbdace95938cbd4c8af26fc192808ac2940d56503e09761b1cec6ecec6d3eebd21cca8fb34f2f57fb046d715407e9d67cd48d08f0c
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35.orig.tar.xz' glibc_2.35.orig.tar.xz 18165952 SHA512:e7336ce27561be5d7c217832a1136fb327e057bd8d3f92925b35c97e3e9f9e486948b5a1e03e5e4090772ef06437a074d10b82e68f17f1ad8f22077ee39e1b66
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35.orig.tar.xz.asc' glibc_2.35.orig.tar.xz.asc 833 SHA512:2a1c152511dac05f9b4e48f7e7a6b59dbf2d8b71fea54f128173113357be26e86216e13c9865f617049e6858396a221a5abc704f65a786b22453945fd80265e9
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35-0ubuntu3.11.debian.tar.xz' glibc_2.35-0ubuntu3.11.debian.tar.xz 940076 SHA512:3a946e60393f09557fdf8cd4f5ad0041301b07da2b11bc5307f2ec15a7926924de0a0648f78879b28a86fd1cc5d20df9963f7c164cef01ea1d5a3d03c3ab2392
```

### `dpkg` source package: `gmp=2:6.2.1+dfsg-3ubuntu1`

Binary Packages:

- `libgmp10:amd64=2:6.2.1+dfsg-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.2.1+dfsg-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.2.1%2bdfsg-3ubuntu1.dsc' gmp_6.2.1+dfsg-3ubuntu1.dsc 2355 SHA512:b41211a64cba1afee1ea7924d38581b26b36f0495ad42be6d25b7175d5fa1e000378a5d36dd80087b0e7d4495620edb1e7e1b32d6c1085a8cdf0a4cb460a0558
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.2.1%2bdfsg.orig.tar.xz' gmp_6.2.1+dfsg.orig.tar.xz 1853476 SHA512:801948b7dcf592959ea387a86bee34dfb4e02c5e93815a785fc46174899ba22129853a3e34109a6df86048a144765c5f39e65fddfcecba879cc60da62f32fea0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.2.1%2bdfsg-3ubuntu1.debian.tar.xz' gmp_6.2.1+dfsg-3ubuntu1.debian.tar.xz 40996 SHA512:d7e0a1165a42b11a26a0f9232193db41ce2e7b1f5ea50d258e156fc9d80f9a74b6739491ec73cc1e909a3d09e029f90c3be1460c993690c5081ef8c6a169a4c3
```

### `dpkg` source package: `gnupg2=2.2.27-3ubuntu2.4`

Binary Packages:

- `dirmngr=2.2.27-3ubuntu2.4`
- `gnupg=2.2.27-3ubuntu2.4`
- `gnupg-l10n=2.2.27-3ubuntu2.4`
- `gnupg-utils=2.2.27-3ubuntu2.4`
- `gpg=2.2.27-3ubuntu2.4`
- `gpg-agent=2.2.27-3ubuntu2.4`
- `gpg-wks-client=2.2.27-3ubuntu2.4`
- `gpg-wks-server=2.2.27-3ubuntu2.4`
- `gpgconf=2.2.27-3ubuntu2.4`
- `gpgsm=2.2.27-3ubuntu2.4`
- `gpgv=2.2.27-3ubuntu2.4`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpg-wks-client/copyright`, `/usr/share/doc/gpg-wks-server/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
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
$ apt-get source -qq --print-uris gnupg2=2.2.27-3ubuntu2.4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27-3ubuntu2.4.dsc' gnupg2_2.2.27-3ubuntu2.4.dsc 3381 SHA512:423656fb510c62d0452ac1963f23b3b7b073e29255be9311e9cf406b8a1463711a0bce4755be70a13c6ddabf526be5c9b8c11df38990e0ab44c9a7d84bff7f6a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27.orig.tar.bz2' gnupg2_2.2.27.orig.tar.bz2 7191555 SHA512:cf336962116c9c08ac80b1299654b94948033ef51d6d5e7f54c2f07bbf7d92c7b0bddb606ceee2cdd837063f519b8d59af5a82816b840a0fc47d90c07b0e95ab
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27-3ubuntu2.4.debian.tar.xz' gnupg2_2.2.27-3ubuntu2.4.debian.tar.xz 75972 SHA512:d0d262876a8a39f0f31f0a0a40290c8d32b3d52ae3d06180bbf3dbaf13e02a8f637ee3d0ab863cf29c12b16d3cc6399529502e302bd4bd606cb97eeb7674d2a8
```

### `dpkg` source package: `gnutls28=3.7.3-4ubuntu1.7`

Binary Packages:

- `libgnutls30:amd64=3.7.3-4ubuntu1.7`

Licenses: (parsed from: `/usr/share/doc/libgnutls30/copyright`)

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
$ apt-get source -qq --print-uris gnutls28=3.7.3-4ubuntu1.7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3-4ubuntu1.7.dsc' gnutls28_3.7.3-4ubuntu1.7.dsc 3575 SHA512:0f5007c1a2914797222013b157f5a21c9eda3d7a40284cea37a75610848558e76e354e5c383e5fcb149ff1a5be660bb231639b78b441c5ab3ab7f1f4ebcdaf3b
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3.orig.tar.xz' gnutls28_3.7.3.orig.tar.xz 6119292 SHA512:3ace744affe23e284342658d6d2d2de49dd50065489cbc8be18fc7d38187253e5268ca54027ce5cd517056c249ac039a7481e4548cec04325de37ae85617d077
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3.orig.tar.xz.asc' gnutls28_3.7.3.orig.tar.xz.asc 833 SHA512:cd0d30298377deddf20a835863b71e3f119588061f659906ad2684004758943179531508b1c77c730e930e2131148095e60ad9be365353cce772472d5f5345df
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3-4ubuntu1.7.debian.tar.xz' gnutls28_3.7.3-4ubuntu1.7.debian.tar.xz 100000 SHA512:c42143e4563ed052b24c72cb7878eaab228976ba970deb5c0a0c897e25242c66c208bcf023e4c9efcfe61b5be538454ffe8b19d5bdda5861527063de3ad51350
```

### `dpkg` source package: `gpgme1.0=1.16.0-1.2ubuntu4.2`

Binary Packages:

- `libgpgme11:amd64=1.16.0-1.2ubuntu4.2`
- `libgpgmepp6:amd64=1.16.0-1.2ubuntu4.2`

Licenses: (parsed from: `/usr/share/doc/libgpgme11/copyright`, `/usr/share/doc/libgpgmepp6/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gpgme1.0=1.16.0-1.2ubuntu4.2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpgme1.0/gpgme1.0_1.16.0-1.2ubuntu4.2.dsc' gpgme1.0_1.16.0-1.2ubuntu4.2.dsc 3057 SHA512:4359b0b51205100cc99bfa61a632a7fe8876704e6d361288f388b2421f62af69aca32b69499b994fc961fb19b01596755cc444aaf23f182e61d436a10f5080bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpgme1.0/gpgme1.0_1.16.0.orig.tar.bz2' gpgme1.0_1.16.0.orig.tar.bz2 1718913 SHA512:69487be69612e9bf0221ff56ae687248bd13635db1b7087130e93c1670e38f3c810bbca17723555c04fe207976c35871bbc3da005179ce099504321cf33636e4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpgme1.0/gpgme1.0_1.16.0.orig.tar.bz2.asc' gpgme1.0_1.16.0.orig.tar.bz2.asc 228 SHA512:fbafd1dbe1fd96ed6457ffbda6b7de603cf66b5325e233c08a33b2b5b977ec116abf938608260a85ad007e08b54a474ebbf8732c75ad682de535e5b563591f19
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpgme1.0/gpgme1.0_1.16.0-1.2ubuntu4.2.debian.tar.xz' gpgme1.0_1.16.0-1.2ubuntu4.2.debian.tar.xz 26868 SHA512:f41d8c0c51b3537953bfd38bc4e02fa063ae7f8b65b078293d6e04277ac2e90fd85621c8331938186775feff42b71cfcab31884c391aa05ad95374e34e0fb4fd
```

### `dpkg` source package: `gpm=1.20.7-10build1`

Binary Packages:

- `libgpm2:amd64=1.20.7-10build1`

Licenses: (parsed from: `/usr/share/doc/libgpm2/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0+`

Source:

```console
$ apt-get source -qq --print-uris gpm=1.20.7-10build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpm/gpm_1.20.7-10build1.dsc' gpm_1.20.7-10build1.dsc 2019 SHA512:d59551a2b4d87e6a9ebac57b7a68292234926445ef7486f1bcc0c708ab99978f7e348edf2cf8719c7f454ff9092d7545220f443caba1799b3e98e06cbcd3ff83
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpm/gpm_1.20.7.orig.tar.gz' gpm_1.20.7.orig.tar.gz 855027 SHA512:39b6ec1d78c03981a2298ce8fd92987dd7e070c767d8135bbb94d6f5fea2d1b9c75b39806c3e99618e2c40cbc29d1c1e4177714ce63ac86b8d9e7e07234feb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpm/gpm_1.20.7-10build1.debian.tar.xz' gpm_1.20.7-10build1.debian.tar.xz 84844 SHA512:0841501055de50e7549924c60d7c975e23f300eb4d192e4ee46505b3dc37ea3d74b4a5a56805dab7b478575c4775945c22450503a035a209a75d5aa1654670ab
```

### `dpkg` source package: `graphite2=1.3.14-1build2`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-1build2`

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
$ apt-get source -qq --print-uris graphite2=1.3.14-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-1build2.dsc' graphite2_1.3.14-1build2.dsc 2262 SHA512:c1c167d90602a7f072189d046304af17a2a3e61509405c3623a56231f7c8341091bb2da2c73bfc41c1a3fc60a1f1b585476aec2a932767e3c31a400d37f50966
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA512:49d127964d3f5c9403c7aecbfb5b18f32f25fe4919a81c49e0534e7123fe845423e16b0b8c8baaae21162b1150ab3e0f1c22c344e07d4364b6b8473c40a0822c
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-1build2.debian.tar.xz' graphite2_1.3.14-1build2.debian.tar.xz 12224 SHA512:7c69742dc115a123eaba93092ad67c06e43e8538c04269e05fa06cb12802b9f331f52161c3ff0ddd0520ccad6993c30102f149ac1694552594a3db5f1c07a209
```

### `dpkg` source package: `grep=3.7-1build1`

Binary Packages:

- `grep=3.7-1build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.7-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.7-1build1.dsc' grep_3.7-1build1.dsc 1900 SHA512:3345c289bc163924615d3bc9ac3138e35870715d38223ef9d38a90ab17160fc415f8c0c9a5da1939143e2701e46fc854b27b45c280c4af686db2208f2becbe4f
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.7.orig.tar.xz' grep_3.7.orig.tar.xz 1641196 SHA512:e9e45dcd40af8367f819f2b93c5e1b4e98a251a9aa251841fa67a875380fae52cfa27c68c6dbdd6a4dde1b1017ee0f6b9833ef6dd6e419d32d71b6df5e972b82
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.7.orig.tar.xz.asc' grep_3.7.orig.tar.xz.asc 833 SHA512:9db28883b696fbbb0fad32f4ecd168954dc475d5f0a8f2b4f960ff615ef7dd8348a7caaee85a96287824472a29485ff921af121c582083ca5ad5c30960f99cf4
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.7-1build1.debian.tar.xz' grep_3.7-1build1.debian.tar.xz 18184 SHA512:cbefc3635a0b0acc33d8a052d3ca7d583adbd1bcfc384559076b5e4f5508b4a8301b0dd54a029aecbab925a6f916c99a2d5bebe0a6936fe5ffeb5a07a0d9a917
```

### `dpkg` source package: `gst-plugins-base1.0=1.20.1-1ubuntu0.5`

Binary Packages:

- `libgstreamer-plugins-base1.0-0:amd64=1.20.1-1ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/libgstreamer-plugins-base1.0-0/copyright`)

- `BSD (2 clause)`
- `BSD (3 clause)`
- `GPL-2+`
- `LGPL`
- `LGPL-2+`
- `MIT/X11 (BSD like) LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris gst-plugins-base1.0=1.20.1-1ubuntu0.5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.20.1-1ubuntu0.5.dsc' gst-plugins-base1.0_1.20.1-1ubuntu0.5.dsc 3796 SHA512:54d1d6135e5701d0c10e5329ca85d351c34aa60a449e84cee50f1b2b4b3578ce405634a4dea9209023f72779d92943763cec9d2801edbb03d4d442bee11f146a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.20.1.orig.tar.xz' gst-plugins-base1.0_1.20.1.orig.tar.xz 3290068 SHA512:679a0eee1973fa9612e2e24978e2c2d9d8fdc5732e1699b4a87712881f1549d0811719a13ff4fe77b91322ca4425c39623b371703f6b3a36fb7238b977d3e541
'http://archive.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.20.1-1ubuntu0.5.debian.tar.xz' gst-plugins-base1.0_1.20.1-1ubuntu0.5.debian.tar.xz 52132 SHA512:08541478c46d6760919372ff12b6de876e222f2e13ad49549c91fc4d70ac440603e76916068329cadd4107ffa26cc5e79c3a1381fcb8e3ac27a82e08fcd3af1a
```

### `dpkg` source package: `gstreamer1.0=1.20.3-0ubuntu1.1`

Binary Packages:

- `libgstreamer1.0-0:amd64=1.20.3-0ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libgstreamer1.0-0/copyright`)

- `GPL-2+`
- `GPL-3+`
- `LGPL`
- `LGPL-2+`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris gstreamer1.0=1.20.3-0ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.20.3-0ubuntu1.1.dsc' gstreamer1.0_1.20.3-0ubuntu1.1.dsc 2968 SHA512:874b7438bd8021858a321ff07a81783541c79faf416c888f96b3368c48dc38229cc0266a1d1c2b022a499ffcfa6549420bae1bf9cb2f6747a78a44e12677053e
'http://archive.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.20.3.orig.tar.xz' gstreamer1.0_1.20.3.orig.tar.xz 2681088 SHA512:e93f9fbf2d7a839dcbe2030ed16dd53eb250741db7c2f1cea396c23e4fabf9a0caff6be4babf7c10aec4b56dc8319a970b1b0bfa6eea2e36aed3e6e1265d9278
'http://archive.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.20.3-0ubuntu1.1.debian.tar.xz' gstreamer1.0_1.20.3-0ubuntu1.1.debian.tar.xz 45248 SHA512:a77666adbad0054f9ccd118b1151dd54f7b62ce42ccf7ad9757652d125dd7040701a7fd68893ccfa4275760aa09f37e5a7f9aecbe86e19b6bf33ab464488e388
```

### `dpkg` source package: `gzip=1.10-4ubuntu4.1`

Binary Packages:

- `gzip=1.10-4ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.10-4ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10-4ubuntu4.1.dsc' gzip_1.10-4ubuntu4.1.dsc 2277 SHA512:62008eba2ed83c6b8636541acb1930a0282248c153b9f1c5dc6209673cc77bdc50af8ec028aaa82fcbbe5cb6b9c142b8026f737c1eeb3bf01e11b4a39ffa4e23
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10.orig.tar.gz' gzip_1.10.orig.tar.gz 1201421 SHA512:7939043e74554ced0c1c05d354ab4eb36cd6dce89ad79d02ccdc5ed6b7ee390759689b2d47c07227b9b44a62851afe7c76c4cae9f92527d999f3f1b4df1cccff
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10.orig.tar.gz.asc' gzip_1.10.orig.tar.gz.asc 833 SHA512:74727fb3a8b64f81b4dd2d941fa750a789c482d7ae604d0ecfbe5ec623780efc7c5f0e51d65e7b99c2f097c5cd6585cc3a0f1b31abb03306156e0d410d9f0186
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10-4ubuntu4.1.debian.tar.xz' gzip_1.10-4ubuntu4.1.debian.tar.xz 39520 SHA512:4cecf676d0c9c55b5ec266f2ffa731cf618d7f4b571768dd3ad16ac8dcf966b80dabf1cbe3939edea96ca9743d710e365c444086946c03bdc3871410e5b4da76
```

### `dpkg` source package: `harfbuzz=2.7.4-1ubuntu3.2`

Binary Packages:

- `libharfbuzz-icu0:amd64=2.7.4-1ubuntu3.2`
- `libharfbuzz0b:amd64=2.7.4-1ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz-icu0/copyright`, `/usr/share/doc/libharfbuzz0b/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=2.7.4-1ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_2.7.4-1ubuntu3.2.dsc' harfbuzz_2.7.4-1ubuntu3.2.dsc 2855 SHA512:7e79b81a2740e2a02e4f11d898b4ace6bd5201616c888e02c07665afefe402d55961f0b141310b4a97ac396498e606e313281caa27915c825a70f20ec38ca15d
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_2.7.4.orig.tar.xz' harfbuzz_2.7.4.orig.tar.xz 9532468 SHA512:d2af6a768c397c664f654cf36140e7b5696b3b983f637454604570c348247f7ffea135048d9b02cf6593cbde728567e31bf82a39df5ff38d680c78dff24d4cf0
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_2.7.4-1ubuntu3.2.debian.tar.xz' harfbuzz_2.7.4-1ubuntu3.2.debian.tar.xz 15000 SHA512:70a45981d34a9f5c085f8dea48a2ebd8c189506358e9e34bd4e9bf94f1a559001dc80915a409332a04efe01135f8aaa30f715da7efc9bd1245fa6352d6083f6d
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

### `dpkg` source package: `hostname=3.23ubuntu2`

Binary Packages:

- `hostname=3.23ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23ubuntu2.dsc' hostname_3.23ubuntu2.dsc 1085 SHA512:5e7f690bb67fcbc7521df55b69ce899ff005d24fb511c017d60ff5e4c9d9fc51271422bb81fc4998d90149cb814d2a209dc61db4d5073f72a37fb22af59827a0
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23ubuntu2.tar.gz' hostname_3.23ubuntu2.tar.gz 13854 SHA512:28b80ea23cbde63af91912aef2773ce83d7f4d1c2c82beb59a86c0e6b11e276019c610a0a60e69947af2b9bc5f86e4f8f6d13c1cb1a9ce35f1e5cfb03e0dd582
```

### `dpkg` source package: `hunspell=1.7.0-4build1`

Binary Packages:

- `libhunspell-1.7-0:amd64=1.7.0-4build1`

Licenses: (parsed from: `/usr/share/doc/libhunspell-1.7-0/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris hunspell=1.7.0-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/h/hunspell/hunspell_1.7.0-4build1.dsc' hunspell_1.7.0-4build1.dsc 1911 SHA512:2ad9656e0a4c6c4646a2751996f07b0d129468340ebc26654ce75a2ef42246820378d434912d13c189f1f44086dd123cd3b1661cdba3524feda6c079022fd444
'http://archive.ubuntu.com/ubuntu/pool/main/h/hunspell/hunspell_1.7.0.orig.tar.gz' hunspell_1.7.0.orig.tar.gz 482156 SHA512:8149b2e8b703a0610c9ca5160c2dfad3cf3b85b16b3f0f5cfcb7ebb802473b2d499e8e2d0a637a97a37a24d62424e82d3880809210d3f043fa17a4970d47c903
'http://archive.ubuntu.com/ubuntu/pool/main/h/hunspell/hunspell_1.7.0-4build1.debian.tar.xz' hunspell_1.7.0-4build1.debian.tar.xz 22056 SHA512:33b32e8474bec0ff0bf2fe049ac3d4393be6594ba8dfc50e8c6549555594317c371c740046b902b1cb5d1cc288bc09c8795074f985e38deb966e3d443c2f97e3
```

### `dpkg` source package: `hyphen=2.8.8-7build2`

Binary Packages:

- `libhyphen0:amd64=2.8.8-7build2`

Licenses: (parsed from: `/usr/share/doc/libhyphen0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1+`

Source:

```console
$ apt-get source -qq --print-uris hyphen=2.8.8-7build2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hyphen/hyphen_2.8.8-7build2.dsc' hyphen_2.8.8-7build2.dsc 1765 SHA512:7416895ec25f70b4012ffd6436d7815b8383a89c76275f8a68c9cf6fe29ba370687cc949ed56a4765a071aa5a52966df7016b37003641578d599e62846de32d1
'http://archive.ubuntu.com/ubuntu/pool/main/h/hyphen/hyphen_2.8.8.orig.tar.gz' hyphen_2.8.8.orig.tar.gz 638369 SHA512:ee514952be56869840b70fb74f60eba14dc4de246733ff8705492367e8cf00c485f8778a9d5a7ba374c988d4ac9fedbe75826dc559e1b62465dbfba21f6ce7de
'http://archive.ubuntu.com/ubuntu/pool/main/h/hyphen/hyphen_2.8.8-7build2.debian.tar.xz' hyphen_2.8.8-7build2.debian.tar.xz 12692 SHA512:988885e3b5894c0c8f274066ea5e5bb3c582dfb2249f0b660f3bfbc637450e986303f41e9b7c67f2cc7787637eb7e9a0831dfc5a9d5072f943fe7669176940ac
```

### `dpkg` source package: `icu=70.1-2`

Binary Packages:

- `libicu70:amd64=70.1-2`

Licenses: (parsed from: `/usr/share/doc/libicu70/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=70.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_70.1-2.dsc' icu_70.1-2.dsc 2252 SHA512:e1bad285bb7f66be62b8b9d595b289095621a88b0c5a2141b7317473ac25ab30a4b83de38ce215d6b7e0e135b2101ed7ab7bcf6d9b3666b4a554095b0ed6d1de
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_70.1.orig.tar.gz' icu_70.1.orig.tar.gz 25449582 SHA512:0b26ae7207155cb65a8fdb25f7b2fa4431e74b12bccbed0884a17feaae3c96833d12451064dd152197fd6ea5fd3adfd95594284a463e66c82e0d860f645880c9
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_70.1.orig.tar.gz.asc' icu_70.1.orig.tar.gz.asc 659 SHA512:17f65641de023b81f18588c5b1be6f88a8d308565343b09241ecfdc6250caeeb785e666d0772b668d5cb0fb243abc88766f02d27b273946e946e8c339cbca942
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_70.1-2.debian.tar.xz' icu_70.1-2.debian.tar.xz 62440 SHA512:ca6771b09b9f232e69b3f6fd6c3445c9b27d86c918a6b52c903a2ebe658b273ea5181fcc3030aaad90450f9d86e620fdd42e710ed81c90c29d889ecfd44c6700
```

### `dpkg` source package: `ijs=0.35-15build2`

Binary Packages:

- `libijs-0.35:amd64=0.35-15build2`

Licenses: (parsed from: `/usr/share/doc/libijs-0.35/copyright`)

- `Expat`
- `Expat~X`
- `Expat~X with X exception`
- `GAP`
- `GAP~Makefile.in`
- `GAP~configure`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`

Source:

```console
$ apt-get source -qq --print-uris ijs=0.35-15build2
'http://archive.ubuntu.com/ubuntu/pool/main/i/ijs/ijs_0.35-15build2.dsc' ijs_0.35-15build2.dsc 1752 SHA512:6f444dc3a4eb7f467380fc81bb8d91ab78b70f6ee9f4adaf5ac532030b335136dd07661069e75d081acec94b4ef10ed2275866c2718f0e88d49cf2949fda5519
'http://archive.ubuntu.com/ubuntu/pool/main/i/ijs/ijs_0.35.orig.tar.gz' ijs_0.35.orig.tar.gz 344262 SHA512:67bb9dd5106010e3a53c4a6b7f3e460c51bc841e3ce4be080f8653fe4a7623aac69db3a749fa75f0df9a48f61a94f34f383381ac2b1bc5b19c703ad6c9e9f3cf
'http://archive.ubuntu.com/ubuntu/pool/main/i/ijs/ijs_0.35-15build2.debian.tar.xz' ijs_0.35-15build2.debian.tar.xz 10488 SHA512:721e33e7175a97bb2bd7521eaf1474e56778ed490102a02d0660e208d302122f41fd32b006e13f871fc174f38dadfc136e6798cda582978f7797d2975e52f421
```

### `dpkg` source package: `imagemagick=8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5`

Binary Packages:

- `imagemagick=8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5`
- `imagemagick-6-common=8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5`
- `imagemagick-6.q16=8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5`
- `libmagickcore-6.q16-6:amd64=8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5`
- `libmagickwand-6.q16-6:amd64=8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-6-common/copyright`, `/usr/share/doc/imagemagick-6.q16/copyright`, `/usr/share/doc/libmagickcore-6.q16-6/copyright`, `/usr/share/doc/libmagickwand-6.q16-6/copyright`)

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
- `TatcherUlrichPublicDomain`
- `aclocal`

Source:

```console
$ apt-get source -qq --print-uris imagemagick=8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.11.60%2bdfsg-1.3ubuntu0.22.04.5.dsc' imagemagick_6.9.11.60+dfsg-1.3ubuntu0.22.04.5.dsc 5246 SHA512:b572b4ce398594b0bb99fe8b31547450afb136a00bd0d7af2da8c274aca693979ceb1a5718fb955f735ee905adc0b9a4dda90dfd14139ca1d29eb3f68f02cda8
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.11.60%2bdfsg.orig.tar.xz' imagemagick_6.9.11.60+dfsg.orig.tar.xz 9395144 SHA512:345a23eda96516fc7a213bd4a322bca4c8b690efe40ff7b498a448f8cedd7f0d600fae2cb6fff45bc995779a90d8c04b58288273eee97833ddebb4f9f2a3d14c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.11.60%2bdfsg-1.3ubuntu0.22.04.5.debian.tar.xz' imagemagick_6.9.11.60+dfsg-1.3ubuntu0.22.04.5.debian.tar.xz 258140 SHA512:f117a816c8578f38b2072aecb8e579103d5f91c29dfce5048947fbfb883e14342c0137135e9c20ad2f9c8f481793171da637d3ba26e656b61ec3ec5da82f0f7a
```

### `dpkg` source package: `init-system-helpers=1.62`

Binary Packages:

- `init-system-helpers=1.62`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.62
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.62.dsc' init-system-helpers_1.62.dsc 1993 SHA512:f706cf5841877ccabe6f5a8e62d44ce5b312c09776d7fb7fd841f39c2d841b3f7f19bcb63cf94073f853165ae44def8f171a0abce658d05c76a48bf1e91697eb
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.62.tar.xz' init-system-helpers_1.62.tar.xz 42144 SHA512:d90f12e642d086bd0d560ece87d119079c164b90ddbb77b2f804979540095b655715febbc2a5b0d50d7f94434d1ff7c0f4044d5d5411916fbca8300f3f88da7f
```

### `dpkg` source package: `intel-mediasdk=22.3.0-1`

Binary Packages:

- `libmfx1:amd64=22.3.0-1`

Licenses: (parsed from: `/usr/share/doc/libmfx1/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `MIT`
- `NTP`

Source:

```console
$ apt-get source -qq --print-uris intel-mediasdk=22.3.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/intel-mediasdk/intel-mediasdk_22.3.0-1.dsc' intel-mediasdk_22.3.0-1.dsc 2154 SHA512:28d569687a94efc7e32d78f0425b602b570907c9f81061a48d7f168bdb86d7f62fc361facae340d811104732eb0692636114297b425c5e51f217fcf541e3f2d8
'http://archive.ubuntu.com/ubuntu/pool/universe/i/intel-mediasdk/intel-mediasdk_22.3.0.orig.tar.gz' intel-mediasdk_22.3.0.orig.tar.gz 11657929 SHA512:cacd700a88d81e2721a3aed3d02982ab20a1d9039b008e6d84d687dcf590036287078c7dcc931e9fd345a5a22ac7ed5db6f621443cb1e1ad1390ff92e131db0f
'http://archive.ubuntu.com/ubuntu/pool/universe/i/intel-mediasdk/intel-mediasdk_22.3.0-1.debian.tar.xz' intel-mediasdk_22.3.0-1.debian.tar.xz 5124 SHA512:2db0c4c5aa9c1409f0f4840efbbdbf1189f4df408b6a0c3f4e811bdc78c2decaf5662f350e0c72bb29d8f14c8fabd0310d4d3f9b8c507d0557ff8754b7cfb485
```

### `dpkg` source package: `iputils=3:20211215-1ubuntu0.1`

Binary Packages:

- `iputils-ping=3:20211215-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/iputils-ping/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris iputils=3:20211215-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/i/iputils/iputils_20211215-1ubuntu0.1.dsc' iputils_20211215-1ubuntu0.1.dsc 2269 SHA512:3d218c702754804d2ac4a8d29b2bc7206588f8d70feb22b7f2b03ebb8f011a833c32c495230f6d2553e68e39f38b9f00824e276f053ac48a98cc4d2ec4a7c0d5
'http://archive.ubuntu.com/ubuntu/pool/main/i/iputils/iputils_20211215.orig.tar.xz' iputils_20211215.orig.tar.xz 447600 SHA512:1d2eeda7b0641d498cdfd28924d41a7f4532fb1ae54607a5c8b642e7c33097f60ee19f802d557c3058251668915d7895ed5e3b16971d9bbae4b288d92beae9d4
'http://archive.ubuntu.com/ubuntu/pool/main/i/iputils/iputils_20211215-1ubuntu0.1.debian.tar.xz' iputils_20211215-1ubuntu0.1.debian.tar.xz 13272 SHA512:54a70878bc1a40c57e32aeedf1f09d69ca45811852d39111f4368cf6c3359607d6f207b196ee08acbb39b26b4f554a7f115782b32a0de18b8d06da30f77f9387
```

### `dpkg` source package: `iso-codes=4.9.0-1`

Binary Packages:

- `iso-codes=4.9.0-1`

Licenses: (parsed from: `/usr/share/doc/iso-codes/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris iso-codes=4.9.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/i/iso-codes/iso-codes_4.9.0-1.dsc' iso-codes_4.9.0-1.dsc 1950 SHA512:5b8eeceb6616cdf557f2672bd09f575cc3cc22895129ca68acdace6baad933d2b4fca5a8e43ce4968d05063017f44bc27b42c6031ed30bfe3959e37f43375069
'http://archive.ubuntu.com/ubuntu/pool/main/i/iso-codes/iso-codes_4.9.0.orig.tar.xz' iso-codes_4.9.0.orig.tar.xz 3766648 SHA512:b31bd77409672d2c25e5e096d2bb6a3517a5afdc0c729e71b099681ddb42f17320129895c91ba1b7d584e2340decd62fdf3bea58edab10440aa2264e2f00e852
'http://archive.ubuntu.com/ubuntu/pool/main/i/iso-codes/iso-codes_4.9.0-1.debian.tar.xz' iso-codes_4.9.0-1.debian.tar.xz 24124 SHA512:4dbf10b0378545f98db24ec471ee20ef37430e197b78916d86a557d36e33a833497f26abf282f51de8fdc6ad027933cca575e9b64034f75eaa05a93089350b7e
```

### `dpkg` source package: `jackd2=1.9.20~dfsg-1`

Binary Packages:

- `libjack-jackd2-0:amd64=1.9.20~dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libjack-jackd2-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-2~either`
- `GPL-2~or`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain~Kroon`

Source:

```console
$ apt-get source -qq --print-uris jackd2=1.9.20~dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/j/jackd2/jackd2_1.9.20%7edfsg-1.dsc' jackd2_1.9.20~dfsg-1.dsc 2547 SHA512:3141385aff7b61daa57b3eeb559a18fffb441de2dfdc3abd571134d475d867f432fb465551314bced97db4209c7d067da5a367d87c491d4eaea4e54073cbf96c
'http://archive.ubuntu.com/ubuntu/pool/main/j/jackd2/jackd2_1.9.20%7edfsg.orig.tar.gz' jackd2_1.9.20~dfsg.orig.tar.gz 1027184 SHA512:ffaca238cb799f2a57882c214bcaf25e43e1e3af07ecaa42c0611e8f38519779b87bf7018efcd88f5f6f9b19f8de91db4460be690c9f3c3f111553cac2f26d79
'http://archive.ubuntu.com/ubuntu/pool/main/j/jackd2/jackd2_1.9.20%7edfsg-1.debian.tar.xz' jackd2_1.9.20~dfsg-1.debian.tar.xz 33080 SHA512:e993535a1225813110d1a7c321df7171412ce24b43ea163a4d627be2f74b646e0084e011db1bcd5d829802db4a792d52b70a42651de2a3ce9d083ba6c17eb3ce
```

### `dpkg` source package: `java-common=0.72build2`

Binary Packages:

- `java-common=0.72build2`

Licenses: (parsed from: `/usr/share/doc/java-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris java-common=0.72build2
'http://archive.ubuntu.com/ubuntu/pool/main/j/java-common/java-common_0.72build2.dsc' java-common_0.72build2.dsc 2092 SHA512:44118aab6a51939ab1b30d9a22cfba4ae31cc331b2f03070bb1485e5a54e56795e23fd652dcaaad8b40799ac00dc950c67a7c4392c38412c6e2439d1185f0437
'http://archive.ubuntu.com/ubuntu/pool/main/j/java-common/java-common_0.72build2.tar.xz' java-common_0.72build2.tar.xz 13328 SHA512:c075b3ad530cd1a84bfd212a06e50782584b9c6e1c36270dfd28d78ac9ba493f45f689adcaf4d1b007a8e6a4a32cf732868a70089681b43cadb1324928f85259
```

### `dpkg` source package: `jbig2dec=0.19-3build2`

Binary Packages:

- `libjbig2dec0:amd64=0.19-3build2`

Licenses: (parsed from: `/usr/share/doc/libjbig2dec0/copyright`)

- `AGPL-3+`
- `BSD-2-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `pubic-domain`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris jbig2dec=0.19-3build2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbig2dec/jbig2dec_0.19-3build2.dsc' jbig2dec_0.19-3build2.dsc 2171 SHA512:28ab2d2fb7b99dcfcd7ec04375cc99d7a9e02b70229fcb9cd88cd21f92e6c7cbf6aa07db0879220f39d3c99d8700d0e6d019b1e61b20f71d3d530e9ea4264a48
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbig2dec/jbig2dec_0.19.orig.tar.gz' jbig2dec_0.19.orig.tar.gz 149134 SHA512:d5a27951cc9c06c184f454e258e81b6e4d5aa2742a4da821522b9a42ecc78e7e1b78058dabc23821618e62d62d8832011f16b5ef2d66beac463da6b809fd02af
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbig2dec/jbig2dec_0.19-3build2.debian.tar.xz' jbig2dec_0.19-3build2.debian.tar.xz 23188 SHA512:b10fe086f0a757fc99ccb9b51ea593e63227351b025e47183dd7999c3e37d7dde05518c6c12c14158c631ad4f7dd994ee6ce69f7a61421ce259aa32f39887c37
```

### `dpkg` source package: `jbigkit=2.1-3.1ubuntu0.22.04.1`

Binary Packages:

- `libjbig0:amd64=2.1-3.1ubuntu0.22.04.1`

Licenses: (parsed from: `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-3.1ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-3.1ubuntu0.22.04.1.dsc' jbigkit_2.1-3.1ubuntu0.22.04.1.dsc 1796 SHA512:c7c726bcac2266327e373a30ec3d97f2197bc6f0f0859ffcc7d6930b94553f482f8693da95cb37ea2e8dc3ff4fdfd2a012e554b81afee0d336dab63d7869c570
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA512:c4127480470ef90db1ef3bd2caa444df10b50ed8df0bc9997db7612cb48b49278baf44965028f1807a21028eb965d677e015466306b44683c4ec75a23e1922cf
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-3.1ubuntu0.22.04.1.debian.tar.xz' jbigkit_2.1-3.1ubuntu0.22.04.1.debian.tar.xz 9912 SHA512:4c473125d8781d2b0192a8af40095e7c6e52225815a8dc7c87fe3bbb50aaeec4295438134be302fa57698d97fccd3f7d2240c74dbc57ef1089cab2ca3fc63475
```

### `dpkg` source package: `keyutils=1.6.1-2ubuntu3`

Binary Packages:

- `libkeyutils1:amd64=1.6.1-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.1-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.1-2ubuntu3.dsc' keyutils_1.6.1-2ubuntu3.dsc 2203 SHA512:7e9c3266bf707b3553758ab89f815542edca6d7ed0ca069986bee3dda75b534f5b275b786e246232b3234c6ccbaf4c67ff60f68bba73b0a3e2ec1bbfa00b295e
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.1.orig.tar.bz2' keyutils_1.6.1.orig.tar.bz2 97232 SHA512:ea6e20b2594234c7f51581eef2b8fd19c109fa9eacaaef8dfbb4f237bd1d6fdf071ec23b4ff334cb22a46461d09d17cf499987fd1f00e66f27506888876961e1
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.1-2ubuntu3.debian.tar.xz' keyutils_1.6.1-2ubuntu3.debian.tar.xz 18936 SHA512:16f390f0fc3154a77c8ca3666d44881a6ca2f0d11cfe0398cd82b57b6f552af85c156de358d0b87e39f301331897d72de058050e3cb53720a76b5b5ebf07aa3d
```

### `dpkg` source package: `krb5=1.19.2-2ubuntu0.7`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.19.2-2ubuntu0.7`
- `libk5crypto3:amd64=1.19.2-2ubuntu0.7`
- `libkrb5-3:amd64=1.19.2-2ubuntu0.7`
- `libkrb5support0:amd64=1.19.2-2ubuntu0.7`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.19.2-2ubuntu0.7
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2-2ubuntu0.7.dsc' krb5_1.19.2-2ubuntu0.7.dsc 3697 SHA512:e5705fc2f43b7b7fdc58c720c820f74fb1e07bcea2c5256f7013977c19bab00f4af4da92904bad3dc5e749ff4d7c480da8261d141d215e34b6f12dc9c0b50fe5
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2.orig.tar.gz' krb5_1.19.2.orig.tar.gz 8741053 SHA512:b90d6ed0e1e8a87eb5cb2c36d88b823a6a6caabf85e5d419adb8a930f7eea09a5f8491464e7e454cca7ba88be09d19415962fe0036ad2e31fc584f9fc0bbd470
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2-2ubuntu0.7.debian.tar.xz' krb5_1.19.2-2ubuntu0.7.debian.tar.xz 124844 SHA512:cc13c07edc27b07c2f4680f6edde898197e8fac06d3c55f83d5b5748c2b1813dff6add13e7d36e9c25e37c1090d90b8ed837bb6a05bf142ab062d1ef7c1148a4
```

### `dpkg` source package: `lame=3.100-3build2`

Binary Packages:

- `libmp3lame0:amd64=3.100-3build2`

Licenses: (parsed from: `/usr/share/doc/libmp3lame0/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-1+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris lame=3.100-3build2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lame/lame_3.100-3build2.dsc' lame_3.100-3build2.dsc 2275 SHA512:0aa5486cd82ea091b6105ee66f95d29d2be5f51dc56b0e042f289ed5012212c7d8ba80f45edccd6b7300126770b65ea46fe07aab8e7525c944de99812b19efc8
'http://archive.ubuntu.com/ubuntu/pool/main/l/lame/lame_3.100.orig.tar.gz' lame_3.100.orig.tar.gz 1524133 SHA512:0844b9eadb4aacf8000444621451277de365041cc1d97b7f7a589da0b7a23899310afd4e4d81114b9912aa97832621d20588034715573d417b2923948c08634b
'http://archive.ubuntu.com/ubuntu/pool/main/l/lame/lame_3.100-3build2.debian.tar.xz' lame_3.100-3build2.debian.tar.xz 12400 SHA512:4638bc184e1e5ac39db5154e72a3243e94033bf6d86b71dd05556368420e92260666177b9513cc8ae0136ec581dfc96e607c1d67d820666e504730f807689c5c
```

### `dpkg` source package: `language-pack-en-base=1:22.04+20240902`

Binary Packages:

- `language-pack-en-base=1:22.04+20240902`

Licenses: (parsed from: `/usr/share/doc/language-pack-en-base/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris language-pack-en-base=1:22.04+20240902
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-en-base/language-pack-en-base_22.04%2b20240902.dsc' language-pack-en-base_22.04+20240902.dsc 1571 SHA512:f90f5ee8b09acec98812ef51bff3eb5d9787775940f105515aa5328f18629f31de19109ddaabf20f7fad842609dd985f195d43782209b5e30217051ac44648e0
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-en-base/language-pack-en-base_22.04%2b20240902.tar.xz' language-pack-en-base_22.04+20240902.tar.xz 1680652 SHA512:0b987c2d55bf6e45d0d9b7adbc087e6d271cd3b194fc4f71e3c82f9e7a83b467926c72b1c43fd5b055ebb6b331956904ab6a082c6b0882b170e20aad248f0691
```

### `dpkg` source package: `language-pack-en=1:22.04+20240902`

Binary Packages:

- `language-pack-en=1:22.04+20240902`

Licenses: (parsed from: `/usr/share/doc/language-pack-en/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris language-pack-en=1:22.04+20240902
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-en/language-pack-en_22.04%2b20240902.dsc' language-pack-en_22.04+20240902.dsc 1532 SHA512:1c6557b4946ad69d6aa1e6c4324f6d21a29824ac60c199fa966b8d40a7ffe08f1e1eb0af2dce3cc21d35a4af3a7b46c67f0cde18fcbef79f7934c6da83416f78
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-en/language-pack-en_22.04%2b20240902.tar.xz' language-pack-en_22.04+20240902.tar.xz 8056 SHA512:b926fcf147ebff38c05598170385115ba2b940cae7026c5052962cbbe4a0d45ebae56caa9714fb2443bdf59e754fece4bfb4e23774274568d0ce6f4b1d51709f
```

### `dpkg` source package: `language-pack-fr-base=1:22.04+20240902`

Binary Packages:

- `language-pack-fr-base=1:22.04+20240902`

Licenses: (parsed from: `/usr/share/doc/language-pack-fr-base/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris language-pack-fr-base=1:22.04+20240902
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-fr-base/language-pack-fr-base_22.04%2b20240902.dsc' language-pack-fr-base_22.04+20240902.dsc 1571 SHA512:7ae88df9a0e1a1acb794ba5b8befa286914fad04bf118f7f52824a0eec51c9d0d8b831cac1b64573dd88d1c6299ada1b07ecfa52da8d48386aab79ce62662910
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-fr-base/language-pack-fr-base_22.04%2b20240902.tar.xz' language-pack-fr-base_22.04+20240902.tar.xz 3713808 SHA512:ef79ee90479b3d446ee41c781835585e1d54b87a9685810dd00ad938917dc2ffda51c7c55e01a7a84aade4ecf239a9a0f2f796c7cbfa052c6e96a43a4027174e
```

### `dpkg` source package: `language-pack-fr=1:22.04+20240902`

Binary Packages:

- `language-pack-fr=1:22.04+20240902`

Licenses: (parsed from: `/usr/share/doc/language-pack-fr/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris language-pack-fr=1:22.04+20240902
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-fr/language-pack-fr_22.04%2b20240902.dsc' language-pack-fr_22.04+20240902.dsc 1532 SHA512:a57d21633f43b6851db0d9aa3e144cb6eccdb8c5e7c298468c80393ff1922b23ef023b195cd50cb3a96a0647117e5d6faa27c0fec16e5d8039df86982f4f11bd
'http://archive.ubuntu.com/ubuntu/pool/main/l/language-pack-fr/language-pack-fr_22.04%2b20240902.tar.xz' language-pack-fr_22.04+20240902.tar.xz 8056 SHA512:23eaf2e3494c4256f5215f3ad139694471432358ee92225152f8eb1b9758091de4a44f2cd174aeba940c8c78c3baba4f990f9f8c2b71e2418bc398c7252b9e35
```

### `dpkg` source package: `lapack=3.10.0-2ubuntu1`

Binary Packages:

- `libblas3:amd64=3.10.0-2ubuntu1`
- `liblapack3:amd64=3.10.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.10.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.10.0-2ubuntu1.dsc' lapack_3.10.0-2ubuntu1.dsc 3474 SHA512:2bdbf698a2ae59dc09b752a20e7b4dfe1c25bd6dc255a36e7fa763d38cb2555eb56a51317867c3a99c09438d038822eeaa933b03b37b836c63fa602a5893b8ae
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.10.0.orig.tar.gz' lapack_3.10.0.orig.tar.gz 7630775 SHA512:56055000c241bab8f318ebd79249ea012c33be0c4c3eca6a78e247f35ad9e8088f46605a0ba52fd5ad3e7898be3b7bc6c50ceb3af327c4986a266b06fe768cbf
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.10.0-2ubuntu1.debian.tar.xz' lapack_3.10.0-2ubuntu1.debian.tar.xz 29040 SHA512:192a9ec75107c5427bd6f2d35e4785034666ba635eb6129f926aaa1663939b625f2800b6acaf686faf69cf21fb8f4201733e5515511e203895300e25675afb78
```

### `dpkg` source package: `lcms2=2.12~rc1-2build2`

Binary Packages:

- `liblcms2-2:amd64=2.12~rc1-2build2`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3 (GPL-3 for the fast_float plugin only)`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.12~rc1-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.12%7erc1-2build2.dsc' lcms2_2.12~rc1-2build2.dsc 2120 SHA512:589b8926590d9158a85ad4641920e1f9700fb864b13ec0f2e44292bd0530cc639ecbcbe216405b7a528ecc512902a79456b30985b5c5a278a5c4692f8fc4bc9f
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.12%7erc1.orig.tar.gz' lcms2_2.12~rc1.orig.tar.gz 7417767 SHA512:1d27e6f91911053b79f2a46c6c16943e25fce2f0501bb7d97f49507522a8a0f911d60f20726fc31727fee5242c6d452c86cdc28735f8f88c3aa9676fd35fdec6
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.12%7erc1-2build2.debian.tar.xz' lcms2_2.12~rc1-2build2.debian.tar.xz 10616 SHA512:250e0245e300fff7be06a43a30621bff920cbb606e51197177d3d43acc1b50ad0db8988f7c05b6b4365073bf0c952d93dcb79364228698fcd8fbc6b093d4f843
```

### `dpkg` source package: `libabw=0.1.3-1build3`

Binary Packages:

- `libabw-0.1-1:amd64=0.1.3-1build3`

Licenses: (parsed from: `/usr/share/doc/libabw-0.1-1/copyright`)

- `GPL-3`
- `LGPL-3`
- `MPL-1.1 | GPL-3 | LGPL-3`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libabw=0.1.3-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libabw/libabw_0.1.3-1build3.dsc' libabw_0.1.3-1build3.dsc 2095 SHA512:1402dca5a684d9f88f73b202a5f72f3ca987fe7433f94a636e2b021a475427906b39da0c21be95713543568c814f788e7fc2192df33605c0f09149efd1f191ec
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libabw/libabw_0.1.3.orig.tar.xz' libabw_0.1.3.orig.tar.xz 318808 SHA512:0d2646e1bad1e11b3da43714ac5931fc67ffdbc4e7a25a44ef5b6e6a41de1e0ae14596b4a87cceb07bf56dbbe9344622b3d60afcb054ee0ab8577ca8e9b5c289
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libabw/libabw_0.1.3-1build3.debian.tar.xz' libabw_0.1.3-1build3.debian.tar.xz 13212 SHA512:ff5aaab730278e87c061902a5591f4dfaf913d12b02781b039f9fc7cf0138d494b5c614c129346ed34329b753644da036bcf506ccf1b8f06b7005b040cf60c01
```

### `dpkg` source package: `libass=1:0.15.2-1`

Binary Packages:

- `libass9:amd64=1:0.15.2-1`

Licenses: (parsed from: `/usr/share/doc/libass9/copyright`)

- `GPL-2`
- `GPL-2+`
- `ISC`
- `other-1`

Source:

```console
$ apt-get source -qq --print-uris libass=1:0.15.2-1
'http://archive.ubuntu.com/ubuntu/pool/universe/liba/libass/libass_0.15.2-1.dsc' libass_0.15.2-1.dsc 2098 SHA512:fba26b2bfb85b93f0d03b9949db9b0d38c51c2a5dd730902e0f154b082f19c43622916df7e82bfba4a2666d194c4980db0aaa5d559be2fdc8335e5e7a411ee59
'http://archive.ubuntu.com/ubuntu/pool/universe/liba/libass/libass_0.15.2.orig.tar.xz' libass_0.15.2.orig.tar.xz 382036 SHA512:4a352d2d21d8a7f25d593f0456cd057912589e55c0709dbf33150d23253fa7859da41584238f03c51782e066a0f92c6849c36b6210324cdb57ed01539921a39b
'http://archive.ubuntu.com/ubuntu/pool/universe/liba/libass/libass_0.15.2-1.debian.tar.xz' libass_0.15.2-1.debian.tar.xz 6200 SHA512:ab09fdd156145adc7041f1a25c947b9f8592a9fd92093bfa75e95abc15830553a41cf800ba1f3f80a6a36f7e1d97962753d8b6aa44417269a94a9392bb147f1a
```

### `dpkg` source package: `libassuan=2.5.5-1build1`

Binary Packages:

- `libassuan0:amd64=2.5.5-1build1`

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
$ apt-get source -qq --print-uris libassuan=2.5.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.5-1build1.dsc' libassuan_2.5.5-1build1.dsc 2753 SHA512:6aa8147a85858f8e0c6ce17083c605fa92c65bcc810a0c1c5c8c5ef08332d359795ad77129bead9f7b216d7893c305e34f653ab29941b008f2bd1178e81587f5
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.5.orig.tar.bz2' libassuan_2.5.5.orig.tar.bz2 572263 SHA512:70117f77aa43bbbe0ed28da5ef23834c026780a74076a92ec775e30f851badb423e9a2cb9e8d142c94e4f6f8a794988c1b788fd4bd2271e562071adf0ab16403
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.5.orig.tar.bz2.asc' libassuan_2.5.5.orig.tar.bz2.asc 228 SHA512:343336ea5dffa113cd934167f548faf4e85d31bf64a46541ee6828b4d0995a8cc9d0668995812d9c4d3ab73347d5b1bbfff0d6ed586fbf4bbc57ac42e828e8d5
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.5-1build1.debian.tar.xz' libassuan_2.5.5-1build1.debian.tar.xz 14448 SHA512:590d52fa0d3e7fde9747cb164b08a60ae3372eff60ac80f4de809289f86a83c2b7361e65bbb20e1b68a27960e7478a78031b57d7e9784d6d2dc407f1c8530217
```

### `dpkg` source package: `libasyncns=0.8-6build2`

Binary Packages:

- `libasyncns0:amd64=0.8-6build2`

Licenses: (parsed from: `/usr/share/doc/libasyncns0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libasyncns=0.8-6build2
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libasyncns/libasyncns_0.8-6build2.dsc' libasyncns_0.8-6build2.dsc 2067 SHA512:31afe8d7efa76a2ea00f64990ab64a34d5fb8146bf0a627a37579e6eea785663877e238d52d4c56987b452eba4217a483fc6f50f9ec08e8281c43bbd8f728597
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libasyncns/libasyncns_0.8.orig.tar.gz' libasyncns_0.8.orig.tar.gz 341591 SHA512:2daad3a2d9eb875e0575843d9e9e2787be6cbba89211fd073fa8898ff80e0a891c7da1a7b0ef70f306318cb3a963ecd65d53d24d08b5f6b98e7cd2a3b3bdcda7
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libasyncns/libasyncns_0.8-6build2.debian.tar.xz' libasyncns_0.8-6build2.debian.tar.xz 4744 SHA512:27be6f29cc7b3466b1cf687cb9cef6b553730e065301644938c2c3fea6e89b0c7076253210e2d6724cc9110f4f0d0125e812c71100f62d0ab9136303d4116c4d
```

### `dpkg` source package: `libavc1394=0.5.4-5build2`

Binary Packages:

- `libavc1394-0:amd64=0.5.4-5build2`

Licenses: (parsed from: `/usr/share/doc/libavc1394-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libavc1394=0.5.4-5build2
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libavc1394/libavc1394_0.5.4-5build2.dsc' libavc1394_0.5.4-5build2.dsc 2254 SHA512:9a66070c19df7b05c572f5b174a4b71de31421cdaca7d9ad5b8ffe218638742e9b95b62bee0043f498110e1b805a9619010907a6a01eb460a62a4fca88558de5
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libavc1394/libavc1394_0.5.4.orig.tar.gz' libavc1394_0.5.4.orig.tar.gz 341679 SHA512:ef07631cd2de9b79dec9d81247d705be318101e8f8a1fe007b946ffab3dfe7b97f392144614d867ef6b2315b6c0e82d53e915f07855d4e21401645293e18842a
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libavc1394/libavc1394_0.5.4-5build2.debian.tar.xz' libavc1394_0.5.4-5build2.debian.tar.xz 6788 SHA512:1d06a6617f014dfece01bbb3d0c1bf8bd133b71a47ebbd28e36f234e3486b65fb0e35bf69a96b1606c151c9e17064f49fecd9e18903e17ef99351759c7a74ba9
```

### `dpkg` source package: `libbluray=1:1.3.1-1`

Binary Packages:

- `libbluray2:amd64=1:1.3.1-1`

Licenses: (parsed from: `/usr/share/doc/libbluray2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.0`
- `custom`

Source:

```console
$ apt-get source -qq --print-uris libbluray=1:1.3.1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/libb/libbluray/libbluray_1.3.1-1.dsc' libbluray_1.3.1-1.dsc 2425 SHA512:9e7520a992566f7e88c89b0a44ac377f99541287278a447eb8946628dcec1f19031c93ceecdf015d82746e63d5cbacba40ef652f19c60f725f178be6f8005532
'http://archive.ubuntu.com/ubuntu/pool/universe/libb/libbluray/libbluray_1.3.1.orig.tar.bz2' libbluray_1.3.1.orig.tar.bz2 754867 SHA512:f39fc8a11771e8fdd5eeebf0ab23535ffab44721f64b350e5d153eee44555b31c618b6d765da114254dc83ff0ff89e84c6b185f61cdbcfedd2d47a5f6e26b75a
'http://archive.ubuntu.com/ubuntu/pool/universe/libb/libbluray/libbluray_1.3.1-1.debian.tar.xz' libbluray_1.3.1-1.debian.tar.xz 17436 SHA512:0817f088cc8d61d8fd570846089fcf5e1ebb32f62c3237d4393193770611b1d64b1e24f16c4ee5e89ee16b29df48597320c0cc9f8ff2fdc31ad7fceead9abeac
```

### `dpkg` source package: `libbs2b=3.1.0+dfsg-2.2build1`

Binary Packages:

- `libbs2b0:amd64=3.1.0+dfsg-2.2build1`

Licenses: (parsed from: `/usr/share/doc/libbs2b0/copyright`)

- `FSF-unlimited`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `MIT+FSF-public`

Source:

```console
$ apt-get source -qq --print-uris libbs2b=3.1.0+dfsg-2.2build1
'http://archive.ubuntu.com/ubuntu/pool/universe/libb/libbs2b/libbs2b_3.1.0%2bdfsg-2.2build1.dsc' libbs2b_3.1.0+dfsg-2.2build1.dsc 2002 SHA512:eb90aa5f14483817e0b2381dec2e68745902125397b21b947440c9bb06be9c7ce0658ac32fda88004c3f808d59b006179b27f5743bf4823a10420a923fbc3864
'http://archive.ubuntu.com/ubuntu/pool/universe/libb/libbs2b/libbs2b_3.1.0%2bdfsg.orig.tar.gz' libbs2b_3.1.0+dfsg.orig.tar.gz 330675 SHA512:a3996a8709c48cbcd56fab295bc2a8113f048290180312b04f6709bfd1e7d71d32edaf72bd684e87ae0ab0804e34969deae73285284f4d3333d369c4cd362ab7
'http://archive.ubuntu.com/ubuntu/pool/universe/libb/libbs2b/libbs2b_3.1.0%2bdfsg-2.2build1.debian.tar.xz' libbs2b_3.1.0+dfsg-2.2build1.debian.tar.xz 4672 SHA512:d9d9615c916ecac200f9c89b783ae72d8a1d0fff84b89bd1416d6ac7f61e7c36285742a1cbaba3c12d151df1dad21b5f28180124a7f07ab5efc181d1cbf97679
```

### `dpkg` source package: `libbsd=0.11.5-1`

Binary Packages:

- `libbsd0:amd64=0.11.5-1`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Regents`
- `BSD-3-clause-author`
- `BSD-4-clause-Christopher-G-Demetriou`
- `BSD-4-clause-Niels-Provos`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.11.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.5-1.dsc' libbsd_0.11.5-1.dsc 2292 SHA512:635f85618e9bcf22abbe73a6864b87d34c4e9d75bc619cab4e487d0ccbb52e1c006258cb47c8b892869adb5d645303fbff3eb57618f2dc862120f741cfbe175c
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.5.orig.tar.xz' libbsd_0.11.5.orig.tar.xz 409972 SHA512:c52c19eddd53630aca14f9f6221f7b84aa9cc798b4bb91e867822b161793313aab872ac1c0350d29312a72fee6e2061f3910ff918b724ec171d8c9de5837c841
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.5.orig.tar.xz.asc' libbsd_0.11.5.orig.tar.xz.asc 833 SHA512:24a3fb414a3a354284c76724d65225619820f3f6b597ed8d163ed99f19ec433465f909fe047758f83a7cd6fc8ee2676478420c77cb2f0b8b69ffa7a690c8c17f
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.5-1.debian.tar.xz' libbsd_0.11.5-1.debian.tar.xz 17604 SHA512:438911ae479952b00aa81cdf2f12863b82a01bc2abf3acb4bf22223f4c851504a77217087b2e2edabf6cf61187314f1c3061f2794de7a38abd953451e2f0d931
```

### `dpkg` source package: `libcaca=0.99.beta19-2.2ubuntu4`

Binary Packages:

- `libcaca0:amd64=0.99.beta19-2.2ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libcaca0/copyright`)

- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libcaca=0.99.beta19-2.2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcaca/libcaca_0.99.beta19-2.2ubuntu4.dsc' libcaca_0.99.beta19-2.2ubuntu4.dsc 2360 SHA512:799cc885391a164e6ed6bda6792c5efadf20b5393daf4fc31cc4b7322cbf28fa9a6981ff97e95450b8d5f2f354d828bebd464b70f5233ea36f2f63155f545492
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcaca/libcaca_0.99.beta19.orig.tar.gz' libcaca_0.99.beta19.orig.tar.gz 1203495 SHA512:780fc7684d40207cc10df3f87d6d8f1d47ddfffa0e76e41a5ce671b82d5c7f090facb054c3d49ca7c4ea1a619625bb9085ce52f837f50792b4a2d776a4c68e15
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcaca/libcaca_0.99.beta19-2.2ubuntu4.debian.tar.xz' libcaca_0.99.beta19-2.2ubuntu4.debian.tar.xz 16460 SHA512:a7a39fc1032ec3954eedbcf258069360a6e2454faa80aa0f6d82f6884fadc81a0f137decd9de72dddbe64c68402bcea005ed59546a4b3873a7c8038eb661d586
```

### `dpkg` source package: `libcap-ng=0.7.9-2.2build3`

Binary Packages:

- `libcap-ng0:amd64=0.7.9-2.2build3`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.7.9-2.2build3
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.9-2.2build3.dsc' libcap-ng_0.7.9-2.2build3.dsc 2105 SHA512:50d7c66eea7dbadcd2314f3eb5ae9f4464e9a2a82a36004efd841bc092f6c4787dd9856aa14bef85035ae9db115b3a9aee78436b790a373e935d98f7fd761cd5
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.9.orig.tar.gz' libcap-ng_0.7.9.orig.tar.gz 449038 SHA512:095edabaf76a943aab0645b843b14e20b1733ba1d47a8e34d82f6586ca9a1512ba2677d232b13dd3900b913837401bb58bf74481970e967ba19041959dc43259
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.9-2.2build3.debian.tar.xz' libcap-ng_0.7.9-2.2build3.debian.tar.xz 6432 SHA512:9ce3f52dc0c89739f0117ba7c1b8fdfcdb51ceb7cea7c00aa55522ba733efdb7a37a7f21a9bfd106e453a8477a759af0aaf4688e4b18c3c9cc659657aeb2c0bb
```

### `dpkg` source package: `libcap2=1:2.44-1ubuntu0.22.04.2`

Binary Packages:

- `libcap2:amd64=1:2.44-1ubuntu0.22.04.2`
- `libcap2-bin=1:2.44-1ubuntu0.22.04.2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`, `/usr/share/doc/libcap2-bin/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.44-1ubuntu0.22.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.44-1ubuntu0.22.04.2.dsc' libcap2_2.44-1ubuntu0.22.04.2.dsc 2318 SHA512:7762231edf17ffd462dcc81d4ce9fed38b1eb87eed0fc15ae34f95f8464a2d1f8b22a7ca4fc32ec015d81b6cd2f8e05b7f95936e414f1f8d9f400db1d8ef71f6
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.44.orig.tar.xz' libcap2_2.44.orig.tar.xz 125568 SHA512:1bb323ca362923bd6bd0e2e4639cf8726975165a620a243b31e797056439eb7efb2bfbc8e5521636783a86c7415b2037b1638c98747b79183ca7d3d42a04ff20
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.44-1ubuntu0.22.04.2.debian.tar.xz' libcap2_2.44-1ubuntu0.22.04.2.debian.tar.xz 23308 SHA512:7a6894c76276e367e7257aa6e2a3cf96d13afe870a42d1298284b4a3ae47ae53922ca4a38466e0b5bb51b832718f8634f72a22e90f996c5b77665454d87044fe
```

### `dpkg` source package: `libcdio-paranoia=10.2+2.0.0-1build3`

Binary Packages:

- `libcdio-cdda2:amd64=10.2+2.0.0-1build3`
- `libcdio-paranoia2:amd64=10.2+2.0.0-1build3`

Licenses: (parsed from: `/usr/share/doc/libcdio-cdda2/copyright`, `/usr/share/doc/libcdio-paranoia2/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris libcdio-paranoia=10.2+2.0.0-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdio-paranoia/libcdio-paranoia_10.2%2b2.0.0-1build3.dsc' libcdio-paranoia_10.2+2.0.0-1build3.dsc 2349 SHA512:392c40bf7b91c29a0f5bbfd262e55b59ed8d107da93222415abc8e1428510545982853a60ef44b5ddea2142121e79e7619c3e67ed58151df816c3f88fa5cca47
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdio-paranoia/libcdio-paranoia_10.2%2b2.0.0.orig.tar.gz' libcdio-paranoia_10.2+2.0.0.orig.tar.gz 2095577 SHA512:66bc2a1c420a3161cf477eb368292febe5b051b1d44812e69caf65d4a88dc3839ede5163869608cbedf84bfee5ddfebb290b75a3c4c92935744abbb6b92f7022
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdio-paranoia/libcdio-paranoia_10.2%2b2.0.0-1build3.debian.tar.xz' libcdio-paranoia_10.2+2.0.0-1build3.debian.tar.xz 7856 SHA512:4ba6af9d19d4574d8a6cef89343c1bbee653f2d85a1d5c3900ab8526af3bef23f1ad1aa2f84de7a89f3eb9845ca446b058ae7d9fec9e15a9336bb75ed270828c
```

### `dpkg` source package: `libcdio=2.1.0-3ubuntu0.2`

Binary Packages:

- `libcdio19:amd64=2.1.0-3ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libcdio19/copyright`)

- `GFDL-1.2`
- `GPL-2`
- `GPL-2+ with autoconf-macro exception`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris libcdio=2.1.0-3ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdio/libcdio_2.1.0-3ubuntu0.2.dsc' libcdio_2.1.0-3ubuntu0.2.dsc 2433 SHA512:29a6a2362226de70850c1e0023b6389a0c5b6905081e4eb0cf64d2eef3550d08ef386cad0eff2ba222a9042e4c4f71c4698a1695ae496cdcd47be963f080ce7e
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdio/libcdio_2.1.0.orig.tar.bz2' libcdio_2.1.0.orig.tar.bz2 1511725 SHA512:8d61142f35a0eb27cf0c3ff33d97b2d5261a4cc37dbd9ca2b2dc2b821706b7f70572c167994d2c97b33c8f269b046dfdc55fda9dc0746e2c279f2125ffadd88f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdio/libcdio_2.1.0-3ubuntu0.2.debian.tar.xz' libcdio_2.1.0-3ubuntu0.2.debian.tar.xz 14632 SHA512:b4cfb838f036dc25fbd99b80fdc2b1b1507cb06dd580a91da6fdc09d40d455209aca85169b9bcebee194e36b8b64a6b7de1e83d3e1b59ec53a77e6c4da0f7db0
```

### `dpkg` source package: `libcdr=0.1.6-2build2`

Binary Packages:

- `libcdr-0.1-1:amd64=0.1.6-2build2`

Licenses: (parsed from: `/usr/share/doc/libcdr-0.1-1/copyright`)

- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libcdr=0.1.6-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdr/libcdr_0.1.6-2build2.dsc' libcdr_0.1.6-2build2.dsc 2167 SHA512:8b86f8c2befa8be3cd15cd3ad32878c91b60cb907a3b946b29d02da8433e9861d8a5086ba4fb80a4cfdc87cc318d94aa7c4a17eba9d0488cdb382fcc298cbd40
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdr/libcdr_0.1.6.orig.tar.xz' libcdr_0.1.6.orig.tar.xz 612068 SHA512:629d55da71c7333f41f60a32e2880deffcf80088096af1bbc8c572b80ef21d851102fdebce56f77245ed60822ca98e02c0867b192abef496a2313fde54a97bb6
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcdr/libcdr_0.1.6-2build2.debian.tar.xz' libcdr_0.1.6-2build2.debian.tar.xz 8460 SHA512:a355d2d7fb2e80fc864bec11851a719424744560388612b61922a8e78265d71bdcac92ae5424256813f09fc90e739b2d40f13502f577a2e049b02b2b8e5f0cd8
```

### `dpkg` source package: `libdatrie=0.2.13-2`

Binary Packages:

- `libdatrie1:amd64=0.2.13-2`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-2
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-2.dsc' libdatrie_0.2.13-2.dsc 2239 SHA512:86ebcb0343ca62b1e832210de6ca74e71786cf7c4c63eb5d1e944dc1bf900c986107c1120e798412fd9780902056fda1403c6124baef044778d479b53aeabb6d
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA512:db3c879d825ead5871c12ef3a06bb093cb1708a6e7e20775eaf82356af9dd6ad54c6b5cabbe1773f2494d3dfa2426528fdd49441038b6294b70ccb1a3d90099a
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-2.debian.tar.xz' libdatrie_0.2.13-2.debian.tar.xz 9604 SHA512:032040b6f9da493b7bbc4437eb16dce9dbbf10d0d9381fbc4ec6c636e5cccaf52b14e77739d227b58fc5ba54911c2cea7f679bada7ed93acb048bd996d4ce3d9
```

### `dpkg` source package: `libdc1394=2.2.6-4`

Binary Packages:

- `libdc1394-25:amd64=2.2.6-4`

Licenses: (parsed from: `/usr/share/doc/libdc1394-25/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libdc1394=2.2.6-4
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libdc1394/libdc1394_2.2.6-4.dsc' libdc1394_2.2.6-4.dsc 2283 SHA512:10c419e828e8fb86c8fb425d575cc8fd6b64040d6566f6a4f38fc40ad6f3632b093aaa35540e3898e5644ffe8b5ee7b409cc70beaa7da2004048ffa340fa2d40
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libdc1394/libdc1394_2.2.6.orig.tar.gz' libdc1394_2.2.6.orig.tar.gz 612067 SHA512:2d60ed1054da67d8518e870193b60c1d79778858f48cc6487e252de00cc57a08548515d41914a37d0227d29e158d68892c290f83930ffd95f4a483dce5aa3d25
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libdc1394/libdc1394_2.2.6-4.debian.tar.xz' libdc1394_2.2.6-4.debian.tar.xz 7832 SHA512:93a956af38d9c6b1c677bb4c7f0b847fd93d73668d789e42fbe05554be7a9d8e28c48dbf9cbcb3842227396bb255fff67f06f266d539556f5a97f382c9c91d04
```

### `dpkg` source package: `libde265=1.0.8-1ubuntu0.3`

Binary Packages:

- `libde265-0:amd64=1.0.8-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`
- `public-domain-2`

Source:

```console
$ apt-get source -qq --print-uris libde265=1.0.8-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libde265/libde265_1.0.8-1ubuntu0.3.dsc' libde265_1.0.8-1ubuntu0.3.dsc 2375 SHA512:52ec53c96c3646fa2b53fbfdf312ade25537fd0d40e5a0bdc5983ec9b3d188393a45f508e81085cc8ed5ecf927cddd40981ecec73d28a323f09568d33af57ea7
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libde265/libde265_1.0.8.orig.tar.gz' libde265_1.0.8.orig.tar.gz 837878 SHA512:bcb33493cbc337d29047c6765189aaba523b20c138aa4fd5c264b3c6aea64cd174cbe14ca2d88c76319e0a8bd5d2e6269f300f056876d2962217eea7934172da
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libde265/libde265_1.0.8-1ubuntu0.3.debian.tar.xz' libde265_1.0.8-1ubuntu0.3.debian.tar.xz 17620 SHA512:3bd585f11a185581bcae1ff4aee43728aab83c27131bf98f5724dfa16ce874f07648a5f298d3e965f02886f281942f5fe47142bed8fbf2b23f4e972e150a177b
```

### `dpkg` source package: `libdecor-0=0.1.0-3build1`

Binary Packages:

- `libdecor-0-0:amd64=0.1.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libdecor-0-0/copyright`)

- `Expat`
- `GPL-3.0`
- `GPL-3.0+`

Source:

```console
$ apt-get source -qq --print-uris libdecor-0=0.1.0-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdecor-0/libdecor-0_0.1.0-3build1.dsc' libdecor-0_0.1.0-3build1.dsc 2715 SHA512:36d2ee20599d723780091c91f524d0d031b70d609616fb447e01057c96da17d1e84432e6873112da047794313e7e174e9cc023a7e578475bafa08556d4253dda
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdecor-0/libdecor-0_0.1.0.orig.tar.gz' libdecor-0_0.1.0.orig.tar.gz 45026 SHA512:7e228b276efc98894085398ac8b4a37fb23a8ce3dfbb16c3d664d833f99e7d6365c43276880ef36d21d6471e1cdcae1925e6daaf95b4904b5701d103e023a916
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdecor-0/libdecor-0_0.1.0-3build1.debian.tar.xz' libdecor-0_0.1.0-3build1.debian.tar.xz 8540 SHA512:3a6d69608043347e452243e1e3fe823367a067d6d0822cf39a66097ab71ae4274aa432d29eb269eb0d3ee50cf7c6462ba0da62b0614e0afa83f7b1ca17c42583
```

### `dpkg` source package: `libdeflate=1.10-2`

Binary Packages:

- `libdeflate0:amd64=1.10-2`

Licenses: (parsed from: `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.10-2
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.10-2.dsc' libdeflate_1.10-2.dsc 2206 SHA512:5c2fd7116bd061a5940481924c3a35e632e178050319c5e29aab2833a2ec27378444a6db767cff1bdd7b9bada10332a975e082ce02eab1fc43f8408a54dfcf52
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.10.orig.tar.gz' libdeflate_1.10.orig.tar.gz 158379 SHA512:2b59cc170c7fb3bb13bd3c6853070ea24fb9e6844dde4d08e43a8a5f8745ecbf844952390ff758070c6fc4f17d9eec8c4d2a729922bf84e2eaa9e74f1424e241
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.10-2.debian.tar.xz' libdeflate_1.10-2.debian.tar.xz 4584 SHA512:faa6fad75528e1f7fa02dd5464bf88d7921563103aee922feade71323229e0c6758cb788545ca6b627aabae58bb7f524d775431fc821f4611713dec6069571c8
```

### `dpkg` source package: `libdrm=2.4.113-2~ubuntu0.22.04.1`

Binary Packages:

- `libdrm-amdgpu1:amd64=2.4.113-2~ubuntu0.22.04.1`
- `libdrm-common=2.4.113-2~ubuntu0.22.04.1`
- `libdrm-intel1:amd64=2.4.113-2~ubuntu0.22.04.1`
- `libdrm-nouveau2:amd64=2.4.113-2~ubuntu0.22.04.1`
- `libdrm-radeon1:amd64=2.4.113-2~ubuntu0.22.04.1`
- `libdrm2:amd64=2.4.113-2~ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libdrm=2.4.113-2~ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdrm/libdrm_2.4.113-2%7eubuntu0.22.04.1.dsc' libdrm_2.4.113-2~ubuntu0.22.04.1.dsc 3360 SHA512:85bf8290d7c3ed97803bf71c9eb640098ada36bc542849a71afca5328076c14cd6a2831b7c336c47a4433dbd256b4c3a9571dcfe5bf396d97621c2c836cf116d
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdrm/libdrm_2.4.113.orig.tar.xz' libdrm_2.4.113.orig.tar.xz 457064 SHA512:fca9834ce090f63ce6dc6d04491a2c5e86162fdddfc8ea70d55a6cdeb401be656388aae1577e58f463a78d8dc502be0a641908784819874e20bbec9a39a057e0
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdrm/libdrm_2.4.113.orig.tar.xz.asc' libdrm_2.4.113.orig.tar.xz.asc 833 SHA512:07807ad5fefd36f58400877bdb0c7cbde445888bd88e8f852b177b88f0c4c3d2bb53e334341ae5b0441c148f219cf841e45d4ae5c06415fc9044c6ff1aa9e596
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdrm/libdrm_2.4.113-2%7eubuntu0.22.04.1.debian.tar.xz' libdrm_2.4.113-2~ubuntu0.22.04.1.debian.tar.xz 60984 SHA512:ab34c74ef4cc56990c078f7d5206037516ebb364e5a0e4dc2ab67ef43452f70eb83b5d5c06e2de4d23233ef26bfefe4cb210574008f7ab7f796434d008bda931
```

### `dpkg` source package: `libe-book=0.1.3-2build2`

Binary Packages:

- `libe-book-0.1-1:amd64=0.1.3-2build2`

Licenses: (parsed from: `/usr/share/doc/libe-book-0.1-1/copyright`)

- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libe-book=0.1.3-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libe-book/libe-book_0.1.3-2build2.dsc' libe-book_0.1.3-2build2.dsc 2100 SHA512:dccc256f318f9fb78253479d141ae215fb4292a210db4349c5c44d71fb52f15c1a21d0cd2f06865e0f264762305ee3a3b5708c1ca96c7cbe93f41359bc2187c8
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libe-book/libe-book_0.1.3.orig.tar.xz' libe-book_0.1.3.orig.tar.xz 416268 SHA512:56dfa93816b8a1b7e223bda517ff81547fd7b311c3fe2bea64b12c4290642d4b9ed3778df06c4ee7a65f2b9db57702c00c32aec819efb7820115165af3d5ebdc
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libe-book/libe-book_0.1.3-2build2.debian.tar.xz' libe-book_0.1.3-2build2.debian.tar.xz 7684 SHA512:37d43a9bd149d7c7fecae1a7b37412b29925e8b8d06743bcc67887a3a980efb67575287055892c9ac0a16eabb57dfe58579b3e984c7738ec95828875013ed4c1
```

### `dpkg` source package: `libedit=3.1-20210910-1build1`

Binary Packages:

- `libedit2:amd64=3.1-20210910-1build1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20210910-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20210910-1build1.dsc' libedit_3.1-20210910-1build1.dsc 2340 SHA512:67cfd7c36cfb575a49a919968710841a19a9f523c6138c3f8bc56de3e546a90adad72f25c1bb4753d83a6d09634c873b3c636613f6d223041f00c7d18ecb7790
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20210910.orig.tar.gz' libedit_3.1-20210910.orig.tar.gz 524722 SHA512:b7361c277f971ebe87e0e539e5e1fb01a4ca1bbab61e199eb97774d8b60dddeb9e35796faf9cc68eb86d1890e8aac11db13b44b57ccc8302d559741fbe9d979e
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20210910-1build1.debian.tar.xz' libedit_3.1-20210910-1build1.debian.tar.xz 15200 SHA512:23ca0f62bf73e9fd1537c599b689807834db6b657c8f0dc448947db49fa3fe0de498ad96ea3d24515f0875fb3f50c4839f1bba25bf9bc48fe23de5fc780f3542
```

### `dpkg` source package: `libeot=0.01-5build2`

Binary Packages:

- `libeot0:amd64=0.01-5build2`

Licenses: (parsed from: `/usr/share/doc/libeot0/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`
- `other`

Source:

```console
$ apt-get source -qq --print-uris libeot=0.01-5build2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libeot/libeot_0.01-5build2.dsc' libeot_0.01-5build2.dsc 2081 SHA512:8f82dc8f9044030c85f9a54475ad22e0154baacf48b937a5264b0b0ee61f41f36556c245e81228bd0d6887ddd2b9914da0d4da962f9ce29e6d39917245cffb3f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libeot/libeot_0.01.orig.tar.bz2' libeot_0.01.orig.tar.bz2 260288 SHA512:897b3d62fdf327bcc4f3033c7b2013c1e89c7e4d98e321eee6470a9b4cf738021deea4fb3c08a7fa1bc1fb4b733ff49e822161dc68d38aef01f7eb1b2fdebc31
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libeot/libeot_0.01-5build2.debian.tar.xz' libeot_0.01-5build2.debian.tar.xz 7684 SHA512:e9a23d3dfa9330b09a7b24be9d5d2d979bb999c80c3381fa28f31003b201e7d8c985eacb92deb4661f40524a2feb5f6a1f0f355dbe9dbb408b0a8115d4d48f84
```

### `dpkg` source package: `libepoxy=1.5.10-1`

Binary Packages:

- `libepoxy0:amd64=1.5.10-1`

Licenses: (parsed from: `/usr/share/doc/libepoxy0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libepoxy=1.5.10-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libepoxy/libepoxy_1.5.10-1.dsc' libepoxy_1.5.10-1.dsc 2095 SHA512:26f4ba03a47589eae9a0413c5a24be2cb4a8e25df50839aa494c270650ecb1994a2623399ece529321736eb4d367642221044d105e2b05418e964d4023a72f27
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libepoxy/libepoxy_1.5.10.orig.tar.gz' libepoxy_1.5.10.orig.tar.gz 332078 SHA512:6786f31c6e2865e68a90eb912900a86bf56fd3df4d78a477356886ac3b6ef52ac887b9c7a77aa027525f868ae9e88b12e5927ba56069c2e115acd631fca3abee
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libepoxy/libepoxy_1.5.10-1.debian.tar.xz' libepoxy_1.5.10-1.debian.tar.xz 17484 SHA512:5c0312814d6ced38f2b3fa804776e3d94d884fcfb8c887a672aa7a51cb03066334652cf581a85e77f02576c8d2232cd7b5e98e50aaa1810d32702f6a794ff7e3
```

### `dpkg` source package: `libepubgen=0.1.1-1ubuntu5`

Binary Packages:

- `libepubgen-0.1-1:amd64=0.1.1-1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libepubgen-0.1-1/copyright`)

- `MPL-2.0`
- `other`

Source:

```console
$ apt-get source -qq --print-uris libepubgen=0.1.1-1ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libepubgen/libepubgen_0.1.1-1ubuntu5.dsc' libepubgen_0.1.1-1ubuntu5.dsc 2177 SHA512:0c96b49cc72a40925c0ffce2c479431fa4f0a925aedbd9e5094b90d3f84f5227339d422ea38c69ac439d007952a9616788917eca9415a0ce9fc36c9889229988
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libepubgen/libepubgen_0.1.1.orig.tar.xz' libepubgen_0.1.1.orig.tar.xz 324380 SHA512:9d911384672b5394ff1df3280a5c9fe12888530c41f177aa100f135954e2ec279b64193f8388f12c96f6a6e587483ce853e74fe45b29fb748a930512dd011c2b
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libepubgen/libepubgen_0.1.1-1ubuntu5.debian.tar.xz' libepubgen_0.1.1-1ubuntu5.debian.tar.xz 6356 SHA512:c71250e38401d47e31444d43fc0cff13601166e96f32d3f2fb0f5a8f571fb8fd8c80c2a5df57cd95969303697c63f82c2e803aec424c3224895e68b5dcbc6e0e
```

### `dpkg` source package: `libetonyek=0.1.10-3build1`

Binary Packages:

- `libetonyek-0.1-1:amd64=0.1.10-3build1`

Licenses: (parsed from: `/usr/share/doc/libetonyek-0.1-1/copyright`)

- `MPL 2.0`

Source:

```console
$ apt-get source -qq --print-uris libetonyek=0.1.10-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libetonyek/libetonyek_0.1.10-3build1.dsc' libetonyek_0.1.10-3build1.dsc 2316 SHA512:9a4ae57559db102d9e1be3925e2082c9c92437a0ecd10f8a7b44ba7276b19aa6ca7146502e28997f03acf808ce36e9b228e4e43ec52f3b7cfcbcc0bfba2b6e7d
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libetonyek/libetonyek_0.1.10.orig.tar.xz' libetonyek_0.1.10.orig.tar.xz 1494000 SHA512:516a14fcb7b7b5898484a4263d593a036ac728b90144da9d1c22a5d0fdffc879839e19a7b390f99d924c390d433e64433fb08939b1e04ca24359315571c5772b
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libetonyek/libetonyek_0.1.10-3build1.debian.tar.xz' libetonyek_0.1.10-3build1.debian.tar.xz 42556 SHA512:2d78a0a055910a1c36c690f9ce1b77a4cd413eaebad9605e3c7a1628cccd7b74d4021ad08bcb879c59131f07f0b7a4a44caf651574b351865936bdcb9091496a
```

### `dpkg` source package: `libexttextcat=3.4.5-1build2`

Binary Packages:

- `libexttextcat-2.0-0:amd64=3.4.5-1build2`
- `libexttextcat-data=3.4.5-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libexttextcat=3.4.5-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexttextcat/libexttextcat_3.4.5-1build2.dsc' libexttextcat_3.4.5-1build2.dsc 2231 SHA512:d111bc5beb5f769f62acd216a00694e7836dae68227eaadd2326ace9fd6dcb86e0629c419f7778d3ed5effc9d5c92aafe4cb2bf1bfc3b7c28bec2bfc426e0bd2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexttextcat/libexttextcat_3.4.5.orig.tar.xz' libexttextcat_3.4.5.orig.tar.xz 1041268 SHA512:f05a9f08c2f2f335d0e483c024321b96fee7424bc1398d4c6acbd9c501f92e22f881bc3d6ec2c0434f9bf4604f3c4b0e880e37d3d0de410eac1a20ea6669baa6
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexttextcat/libexttextcat_3.4.5-1build2.debian.tar.xz' libexttextcat_3.4.5-1build2.debian.tar.xz 7372 SHA512:6cf9289cda0495ce7851f156ef889c9ac7dfac046e1e2463471435e5b737c4f0b7684ed7abdde8970c41b6e91165fec60567c0784b955a96fdb47816b1931a9b
```

### `dpkg` source package: `libffi=3.4.2-4`

Binary Packages:

- `libffi8:amd64=3.4.2-4`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.4.2-4
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.2-4.dsc' libffi_3.4.2-4.dsc 1948 SHA512:a3a3ada71f82d244f8cb54f1cac30ae6be7c4305696700fb6ffb96783f4f9f788c943bc8ba0d7474c9fd31f04453875e1da341240707711e4eff10cd8023e8d1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.2.orig.tar.gz' libffi_3.4.2.orig.tar.gz 1351355 SHA512:31bad35251bf5c0adb998c88ff065085ca6105cf22071b9bd4b5d5d69db4fadf16cadeec9baca944c4bb97b619b035bb8279de8794b922531fddeb0779eb7fb1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.2-4.debian.tar.xz' libffi_3.4.2-4.debian.tar.xz 8164 SHA512:eecf83971847b78aae0c2cfe3b546a858c93462b7d1d2473c96f5b43de47e1d5fc4663b524e4c5792630d7a6d1796e8bdf83f55addc669d0ce3810643924a07f
```

### `dpkg` source package: `libfreehand=0.1.2-3build2`

Binary Packages:

- `libfreehand-0.1-1=0.1.2-3build2`

Licenses: (parsed from: `/usr/share/doc/libfreehand-0.1-1/copyright`)

- `GPL-3`
- `LGPL-3`
- `MPL-1.1 | GPL-3+ | LGPL-3+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libfreehand=0.1.2-3build2
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfreehand/libfreehand_0.1.2-3build2.dsc' libfreehand_0.1.2-3build2.dsc 2171 SHA512:55ec230f1b55064a3b1749ab8d624f1853de6a73ec732cf54ffb8af1349edf37f6e1efc5ba743db795a53ec90ef3271c7abf7ff8ee018d0569512216ecfeccce
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfreehand/libfreehand_0.1.2.orig.tar.xz' libfreehand_0.1.2.orig.tar.xz 516132 SHA512:4112a76ac99999801d97d1b282596d631d8496a5bf65778ab26aa06da86637b1e2b630648a67ea01bf3316ecec9f2715546baff27af090b900267c87a011b963
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfreehand/libfreehand_0.1.2-3build2.debian.tar.xz' libfreehand_0.1.2-3build2.debian.tar.xz 13672 SHA512:18cdebebb8ae61e7ed2ea1a0c3f869a91876e719ad713541fd7e9f0acd4c3d4530857b972000d1b59cf83b546d9d28074f44a116ee1e0f977fc5ce862b3a5917
```

### `dpkg` source package: `libgcrypt20=1.9.4-3ubuntu3`

Binary Packages:

- `libgcrypt20:amd64=1.9.4-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.9.4-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.9.4-3ubuntu3.dsc' libgcrypt20_1.9.4-3ubuntu3.dsc 2936 SHA512:1f68c37290d1ccdaa60cf6543c52f7dca084b49ebffd5d4fd7700304a4f8d133e694084ed69ff4b33ba2c2e25947c9ac595997a20dfb6627285d0ca2477c7809
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.9.4.orig.tar.bz2' libgcrypt20_1.9.4.orig.tar.bz2 3239704 SHA512:d0e117ac73c94d70e9521ee1e6328691498cc8328f8c4e21338096908f5c04c7b838966eb63d59494565f4e19f506c07dab4f4d922150d75610d9f7b57abbf60
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.9.4.orig.tar.bz2.asc' libgcrypt20_1.9.4.orig.tar.bz2.asc 228 SHA512:5fbc2f52ff8a9f2b254791a0d127b012a3648a03d26e043af2ab63d05f69045492581462ba485ecf005a171ea391175bdc73350aa0e76f8b5f75c64a4d685d49
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.9.4-3ubuntu3.debian.tar.xz' libgcrypt20_1.9.4-3ubuntu3.debian.tar.xz 35172 SHA512:fec6751987d91e0234a9da212456763045eabf52166fb30f4832db0460b0a250caff879ac9c80dddf5697945e3a5b1effa036206b96fbf047f2bb705d74a5245
```

### `dpkg` source package: `libglvnd=1.4.0-1`

Binary Packages:

- `libgl1:amd64=1.4.0-1`
- `libglvnd0:amd64=1.4.0-1`
- `libglx0:amd64=1.4.0-1`

Licenses: (parsed from: `/usr/share/doc/libgl1/copyright`, `/usr/share/doc/libglvnd0/copyright`, `/usr/share/doc/libglx0/copyright`)

- `Apache-2.0`
- `BSD-1-clause`
- `GPL`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libglvnd=1.4.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libglvnd/libglvnd_1.4.0-1.dsc' libglvnd_1.4.0-1.dsc 2690 SHA512:38868f25aecb76b9a42b09a994e9c1ecd1a3e8606c632da894522a4b640658280ff91988e3442d45b7f5d30fdfd5b4e9560fd3a1376e88c1a0c2f5555dc430d8
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libglvnd/libglvnd_1.4.0.orig.tar.gz' libglvnd_1.4.0.orig.tar.gz 838573 SHA512:2a1cf975a0453c4e3777e4380b1084d9d5ddfaf7fd96d97f7e503c1a3b46b2234245939626d5c816da8ad41b88dbf67ee0a8dbb7cc755852ed0b75a67caea8b0
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libglvnd/libglvnd_1.4.0-1.debian.tar.xz' libglvnd_1.4.0-1.debian.tar.xz 22264 SHA512:23cbdc9c0f9e960a5912ab4b9854da4b50f6dfdad9a233d0743bfd92f38b0d224ee02af3bfda1930e0315c912cd245acece4889d236be55e200e9346734d1aa6
```

### `dpkg` source package: `libgpg-error=1.43-3`

Binary Packages:

- `libgpg-error0:amd64=1.43-3`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.43-3
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.43-3.dsc' libgpg-error_1.43-3.dsc 2270 SHA512:c0cf8b16d720d89b69b5eb5cf22bf7bb0605892ba110100d3b30370fc93c167bda2f501e53e70a2599024bc40c1e509d06e39f68f3be63312967e4308249f0b8
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.43.orig.tar.bz2' libgpg-error_1.43.orig.tar.bz2 999006 SHA512:36769a62d0b4b219a6d58195bed692e34d3b0313f628b1036055ca34b69332edbe6bcdace9855a60d06e7be5998dc13bf1305d0b2bb211a4d8f701e85040961c
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.43.orig.tar.bz2.asc' libgpg-error_1.43.orig.tar.bz2.asc 238 SHA512:1bd12acc57bb394947dec51b70fe067f717e591484be164cafff3ac47a6bacc101f7ac64fbae350233bc76a0002981fb3fbe53db73dc914db52694b8588cecc1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.43-3.debian.tar.xz' libgpg-error_1.43-3.debian.tar.xz 19264 SHA512:bbd7615b02707405efddd4bb1dee355024bb7089770453a2addf7e722c15c2cfbebc3012c9db848f3f55eb4c66f5b9487877e8d94322d8dc1d2731876b4d8281
```

### `dpkg` source package: `libgsm=1.0.19-1`

Binary Packages:

- `libgsm1:amd64=1.0.19-1`

Licenses: (parsed from: `/usr/share/doc/libgsm1/copyright`)

- `TU-Berlin-2.0`

Source:

```console
$ apt-get source -qq --print-uris libgsm=1.0.19-1
'http://archive.ubuntu.com/ubuntu/pool/universe/libg/libgsm/libgsm_1.0.19-1.dsc' libgsm_1.0.19-1.dsc 1983 SHA512:2d8566fa0db6701dd54bc5602fed430b34cbdce43c2d02f54a51ed8f138b2f6f72650608c6b620807940d9e0008133812d4e15ed546de0d974d8ff002948c31e
'http://archive.ubuntu.com/ubuntu/pool/universe/libg/libgsm/libgsm_1.0.19.orig.tar.gz' libgsm_1.0.19.orig.tar.gz 64665 SHA512:f69b4bf2d918b118b5de90b8ab88fd026008ac7432f07b872b81fe52cdc781f605dca8eedcdaebc8beb974cef388496c618f92a41961c62057009964159f8392
'http://archive.ubuntu.com/ubuntu/pool/universe/libg/libgsm/libgsm_1.0.19-1.debian.tar.xz' libgsm_1.0.19-1.debian.tar.xz 10408 SHA512:44f1ae6954d7626d116fa4a619e2c349b6c2fa742372adc68a22cc89793ec8fc293ee5dadc8df7c6dbc44ce2d09d96abee167837b5a1c1383475ab0b9f573220
```

### `dpkg` source package: `libheif=1.12.0-2build1`

Binary Packages:

- `libheif1:amd64=1.12.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libheif1/copyright`)

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
$ apt-get source -qq --print-uris libheif=1.12.0-2build1
'http://archive.ubuntu.com/ubuntu/pool/universe/libh/libheif/libheif_1.12.0-2build1.dsc' libheif_1.12.0-2build1.dsc 2423 SHA512:62cc515cbcea9f009ebcbc65860fb6e7971d42b983fb55c716a764c57a8835706757f125eb57c2b787d9e78b216aad085d946d30f192122ec0775fa9e04e3262
'http://archive.ubuntu.com/ubuntu/pool/universe/libh/libheif/libheif_1.12.0.orig.tar.gz' libheif_1.12.0.orig.tar.gz 1684355 SHA512:9e6f74dd52841a33b6021a1581ab28c56123d927caa7972acd284444e90888bbdae983b6d847d20eac7651dacea2193d27eb8df45928cb0774229ef8eea23294
'http://archive.ubuntu.com/ubuntu/pool/universe/libh/libheif/libheif_1.12.0-2build1.debian.tar.xz' libheif_1.12.0-2build1.debian.tar.xz 7120 SHA512:0a12dea34fbbfef0d715635eac72e5fde0e6101a11d926f0aeddcc50878b3b97c74d4efb1b5c231eac7abca1fffc6ec7f7b5a544c622a9f3cd9caebee279ed1c
```

### `dpkg` source package: `libice=2:1.0.10-1build2`

Binary Packages:

- `libice6:amd64=2:1.0.10-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build2.dsc' libice_1.0.10-1build2.dsc 2181 SHA512:ab928645b15c679673d1adcc53f23b126f4ca90accbef677c15a1bb8bd428e642db5e45ef77b255d9b0351c2501dd01eafb9108875fff7c98f4543432d7e6fbf
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA512:2d4757f7325eb01180b5d7433cc350eb9606bd3afe82dabc8aa164feda75ef03a0624d74786e655c536c24a80d0ccb2f1e3ecbb04d3459b23f85455006ca8a91
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build2.diff.gz' libice_1.0.10-1build2.diff.gz 11679 SHA512:dc850d9603ac04ffee3e2de1d2f9786520f6d9829f210649756fac705b6fe2797eda307d45283533342dd425317928fbb5f61d94bfe0fcadbc8f1c0c2cb02d6c
```

### `dpkg` source package: `libidn2=2.3.2-2build1`

Binary Packages:

- `libidn2-0:amd64=2.3.2-2build1`

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
$ apt-get source -qq --print-uris libidn2=2.3.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.2-2build1.dsc' libidn2_2.3.2-2build1.dsc 2655 SHA512:bc84158420d526a0f9bca79ca2a8291c55588e2773ded66d7c4b86ad33b370f9d8723cfc3a2b278660de7060687fff5448912e802d7fb63a8ff7876b38440f32
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.2.orig.tar.gz' libidn2_2.3.2.orig.tar.gz 2169556 SHA512:958dbf49a47a84c7627ac182f4cc8ea452696cec3f0d1ff102a6c48e89893e772b2aa81f75da8223dfc6326515cca3ae085268fbf997828de9330c3a351152f1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.2.orig.tar.gz.asc' libidn2_2.3.2.orig.tar.gz.asc 488 SHA512:0559b51b37c7937f3e1f8bf9de9b193f137f16b79d6673f85691a4f4a12ec132568e913848a70136f8522118817f7ecaa8432d353a5eff6b99a7be8719421fe0
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.2-2build1.debian.tar.xz' libidn2_2.3.2-2build1.debian.tar.xz 15972 SHA512:d5af028cc405d326c31e67e577ef16d9b8b81e433171220fda2c2a6f8fc982a63b6d1d85c6595f5ce01a5005768d935aeeaa5de8a552990f4e070bc541e78570
```

### `dpkg` source package: `libidn=1.38-4ubuntu1`

Binary Packages:

- `libidn12:amd64=1.38-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libidn12/copyright`)

- `GAP`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libidn=1.38-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn/libidn_1.38-4ubuntu1.dsc' libidn_1.38-4ubuntu1.dsc 2510 SHA512:4e2d5c710390ef8780d1395bca519bc199eacd14efe081171a78b99efb2388f7a077e03762ac04b390e72319cb83fb7d0b16e57fe0e174427fbd93e150635477
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn/libidn_1.38.orig.tar.gz' libidn_1.38.orig.tar.gz 2681263 SHA512:5e59b2263fde44d1463b47b516347b17a4e3e3696ebba66ab5fe464d567e2ec81f769fa7cf72ed51cfb501e32221813bb375373713a47e2f599fc6122850e419
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn/libidn_1.38.orig.tar.gz.asc' libidn_1.38.orig.tar.gz.asc 488 SHA512:9caf0f9633f607861e94d6efe30383181db67e6fb437903b6c1ff1758363824afc1b01458f845d2bf11c8f2ec01708ba98da54a43a6e2429978caa0f41166ffe
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn/libidn_1.38-4ubuntu1.debian.tar.xz' libidn_1.38-4ubuntu1.debian.tar.xz 15336 SHA512:64e8aed314b1ff5efc6fa3fc1b9f328a2e7178e7bb2b39b15064dbdd74a39d920902a7ae0d2e6babab9b4b71e1ee6e257c994432ad0ed9bb4f19250a30b2b718
```

### `dpkg` source package: `libiec61883=1.2.0-4build3`

Binary Packages:

- `libiec61883-0:amd64=1.2.0-4build3`

Licenses: (parsed from: `/usr/share/doc/libiec61883-0/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libiec61883=1.2.0-4build3
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libiec61883/libiec61883_1.2.0-4build3.dsc' libiec61883_1.2.0-4build3.dsc 2119 SHA512:5236a59c5fe7312518936743d9635f5ce536e3513019320e7b4bb32a1c77a77f3e49bee8b1503cd3fd4b622f04ea8c2ec76e27cdf070e86fe879292c4fc84794
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libiec61883/libiec61883_1.2.0.orig.tar.gz' libiec61883_1.2.0.orig.tar.gz 339064 SHA512:7dc8a186635cba112769e36bf812221aa535641ffe5534c3b05b882fd20eab3a41cfde2fb6466490a7548e8bb45d91792f48f3190dfed671c1945281368c3762
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libiec61883/libiec61883_1.2.0-4build3.debian.tar.xz' libiec61883_1.2.0-4build3.debian.tar.xz 7828 SHA512:78bdbc065655cda2f0b2311f348d00054d8def4658da25bdfb0424e63601cf1bc46f535884e01cd70a2cb7d96aac0fe766104636b8e26850b5a6f6f9a73a5b61
```

### `dpkg` source package: `libjpeg-turbo=2.1.2-0ubuntu1`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.2-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`)

- `JPEG`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.2-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.2-0ubuntu1.dsc' libjpeg-turbo_2.1.2-0ubuntu1.dsc 1690 SHA512:401a75e62575352db079bd268f00f94c8ea1e8e6c38bda852628729e6dfd3135804e3c9ee5b18b1254fed827e6073b0078553bcbc2c1df30d628bbb717a5ed47
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.2.orig.tar.gz' libjpeg-turbo_2.1.2.orig.tar.gz 2257645 SHA512:172c3d8bdad62c32c4560754422fb36f0e80c8316e44d08708f0cba8ee9fd0830f5295d380de34d0f90ec07df6ab4dbe2f0c8451bc60553371c022c9077447c2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.2-0ubuntu1.debian.tar.xz' libjpeg-turbo_2.1.2-0ubuntu1.debian.tar.xz 17240 SHA512:5cfc1e73012f3251e385f0288dece2e3862977fb3975c61c344afc464a2fd329c3fa027fc07edc40097afaad052bdf6f0dad55c665c20ccdde9f2231ec191410
```

### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu10`

Binary Packages:

- `libjpeg8:amd64=8c-2ubuntu10`

Licenses: (parsed from: `/usr/share/doc/libjpeg8/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg8-empty=8c-2ubuntu10
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu10.dsc' libjpeg8-empty_8c-2ubuntu10.dsc 1655 SHA512:1085be8a159c716c4ca89e6bfb2b1a5ce7b66ad8bc8f4cf3796c2c4ac3dad5169ac5be045f2a9ce103858b42585b1ce52d6dc6986995d073785170d45fe4d29d
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu10.tar.gz' libjpeg8-empty_8c-2ubuntu10.tar.gz 1912 SHA512:1c21044013df62225f861ec6f88b2a43e0f6254522ed379ad081b92f4f89b64686d4e68d70e8384289cd8222df2288400c2d0e8b8ccae87dd079164bdc3f3cf3
```

### `dpkg` source package: `libksba=1.6.0-2ubuntu0.2`

Binary Packages:

- `libksba8:amd64=1.6.0-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.0-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0-2ubuntu0.2.dsc' libksba_1.6.0-2ubuntu0.2.dsc 2585 SHA512:ef96729e570627b7cf38ed0dcc3338097a81f690dde041fd9ea63b3c4b55c11ccf35ab7b2bbd196af3ca7834f8e5017cbb14436a7718034608f3276ca3db9f3f
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0.orig.tar.bz2' libksba_1.6.0.orig.tar.bz2 662120 SHA512:a7c76d41dfd8ec6383ac2de3c53848cd9f066b538f6f3cd43175e3c8095df51b96d0a24a573481c0c4856b09b7c224e2b562d88f5c0801e7acfb582ea2739c2b
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0.orig.tar.bz2.asc' libksba_1.6.0.orig.tar.bz2.asc 228 SHA512:fc381ea66eefdb431a5248fa3ac0751d7343d7f99cc7ebf7621b0763e6e31a80b45c5e17b09bbc7c1c1154e6a0152af1f13798f64959ac63f50b789ec046d7a3
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0-2ubuntu0.2.debian.tar.xz' libksba_1.6.0-2ubuntu0.2.debian.tar.xz 16004 SHA512:24a609ca522b5e3a1402ff5a97ce451869bdf0960902d171a89f2190d4de7c8442403d21f938cebeeafd0ae082bf03d76c0521b26a2c153257df784cf7894b43
```

### `dpkg` source package: `liblangtag=0.6.3-2ubuntu1`

Binary Packages:

- `liblangtag-common=0.6.3-2ubuntu1`
- `liblangtag1:amd64=0.6.3-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/liblangtag-common/copyright`, `/usr/share/doc/liblangtag1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL | MPL`

Source:

```console
$ apt-get source -qq --print-uris liblangtag=0.6.3-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libl/liblangtag/liblangtag_0.6.3-2ubuntu1.dsc' liblangtag_0.6.3-2ubuntu1.dsc 1856 SHA512:a816c47c277542acea4663d5f47d1bad955cfabdb9f23ddf9fb5d8849541f841f6ea3213990f17ae8f7dac846c85f84ea68d950e3c35d9d4ce0d9ed83e2de607
'http://archive.ubuntu.com/ubuntu/pool/main/libl/liblangtag/liblangtag_0.6.3.orig.tar.bz2' liblangtag_0.6.3.orig.tar.bz2 755492 SHA512:3dcfc20704dfaff05aeecdeef74fa81639fb70f930ebc0895fe4707ecd1d5b6221fe889449772811924d0c38329977c9d5fc751c3accbc272834b29c461f1fcf
'http://archive.ubuntu.com/ubuntu/pool/main/libl/liblangtag/liblangtag_0.6.3-2ubuntu1.debian.tar.xz' liblangtag_0.6.3-2ubuntu1.debian.tar.xz 6596 SHA512:b995d23a6d515498cfe47a05dc9e51fa96551f4f429ec647d05ffb9ff556be5a7dcdfe74c205dcd2e893bb5e96f850bb3640b1b7b94f6ee79950631d482214d7
```

### `dpkg` source package: `liblqr=0.4.2-2.1`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.1`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.1
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1.dsc' liblqr_0.4.2-2.1.dsc 2095 SHA512:ef20fa2551ce6399f0ecc42301c2d0292d624f4fd9252fd901d58d67ac7325f128cd5209661fe456dda31e4efbb6b48a80415a1b34f815dd7511eeb24e924d36
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA512:acfa5868c41ea145092711e84d6c9eb62cb725b3d7531917b0d91b7d4af2a9912b18a96edc2594a826f09dabe0a0a82936ceea7d1f31301a23d558b1450d2547
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1.debian.tar.xz' liblqr_0.4.2-2.1.debian.tar.xz 5300 SHA512:ba8ade073057be2c5b065d92c0a119049cb67b382ebbf6c2b8c59b1aec52bd60fd6c313c0a2e8d83f39e9733477b615c7a646c47ca9dbbe3c8469ff86078c027
```

### `dpkg` source package: `libmd=1.0.4-1build1`

Binary Packages:

- `libmd0:amd64=1.0.4-1build1`

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
$ apt-get source -qq --print-uris libmd=1.0.4-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.0.4-1build1.dsc' libmd_1.0.4-1build1.dsc 2380 SHA512:778b562e6b3860fe6a6d5ddf4d7cce381126be77d151ac7c2a619d57737080f2adc07ff8e01fcafd98b3ace157fc72ab77a572362b56e79e5abb79a99fdacd6c
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.0.4.orig.tar.xz' libmd_1.0.4.orig.tar.xz 264472 SHA512:731553ecc5e0e1eb228cced8fccd531fe31fb5c7627ca30013d287e1aeb8222959cf7498fbb7414bbabb967b25d4e8b0edd54fc47f6ccf55fc91087db0725ce3
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.0.4.orig.tar.xz.asc' libmd_1.0.4.orig.tar.xz.asc 833 SHA512:ec4b60a721da1f315fad73daa8ee620f44a53f17a30506c4d63b154b3abde19bb248b2ce6b83b989589e2a9184ebbe1b870e83181e18a4147d75617579d10504
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.0.4-1build1.debian.tar.xz' libmd_1.0.4-1build1.debian.tar.xz 10264 SHA512:0e287498326a5aa3bc95cb0c576df7d0bb289bfb9db3a1f812d0e202c61af9dc78ecfa4b6b26c2dee3c5ccbefad877919f44ec849b3300f0f30878080eb5cb13
```

### `dpkg` source package: `libmspub=0.1.4-3build3`

Binary Packages:

- `libmspub-0.1-1:amd64=0.1.4-3build3`

Licenses: (parsed from: `/usr/share/doc/libmspub-0.1-1/copyright`)

- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libmspub=0.1.4-3build3
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmspub/libmspub_0.1.4-3build3.dsc' libmspub_0.1.4-3build3.dsc 2233 SHA512:73f9ac740da33fc58620d3d3d654f6e8120aaeeb4e9b969bb758eb260eca0fad1381493b93210694824c8b60d4ede30eec1804dce2f24cd222289cec564d1cc0
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmspub/libmspub_0.1.4.orig.tar.xz' libmspub_0.1.4.orig.tar.xz 377472 SHA512:7275f890645961b3fd56df4584788962e8c064fe3f99f5834c6ba6177ce76d00d544fbe9a25b7ab2f4180d2f3a90c609fe0bb68d61ea24e95b086190390fff31
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmspub/libmspub_0.1.4-3build3.debian.tar.xz' libmspub_0.1.4-3build3.debian.tar.xz 7656 SHA512:1afc7af498b2ed0471ae3ca35e75841c304fef1b40d85f77938b96bfa629bd29af919bcb4de7156d5cdf0fc3bc7cdae8a5324f2d84bd365264b080fe2693986e
```

### `dpkg` source package: `libmwaw=0.3.21-1build1`

Binary Packages:

- `libmwaw-0.3-3:amd64=0.3.21-1build1`

Licenses: (parsed from: `/usr/share/doc/libmwaw-0.3-3/copyright`)

- `BSD`
- `LGPL`
- `MPL2.0 | LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libmwaw=0.3.21-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmwaw/libmwaw_0.3.21-1build1.dsc' libmwaw_0.3.21-1build1.dsc 2204 SHA512:5baa070315e3a1270be074ace75da4f789eef5c40d6f5c827c3ce37227089d41e1dece79e4e2690777ce085b027f448c6b4a5e9c75e79cf97fe3270eb753d09e
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmwaw/libmwaw_0.3.21.orig.tar.xz' libmwaw_0.3.21.orig.tar.xz 1457212 SHA512:1b6aab4f3e76d1d7a3c15cc175642c62f826172c9fdef558617b87a98d056a05d817caaccdc199197670f84ada448b65cce61f5254ed8e1d7634a637d3367384
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmwaw/libmwaw_0.3.21-1build1.debian.tar.xz' libmwaw_0.3.21-1build1.debian.tar.xz 8408 SHA512:d53692aabefb1e89149ac3d0cb16848887782de78b59f3f16675febcde17d14e66a91831e79729734beadc550523e102a039bf25b6a86e429bc7e6ba0ff9d3ee
```

### `dpkg` source package: `libmysofa=1.2.1~dfsg0-1`

Binary Packages:

- `libmysofa1:amd64=1.2.1~dfsg0-1`

Licenses: (parsed from: `/usr/share/doc/libmysofa1/copyright`)

- `BSD-3-clause`
- `CC-BY-4.0`
- `CC-BY-SA-3.0`
- `cipic`
- `listen-ircam`
- `mit-kemar`

Source:

```console
$ apt-get source -qq --print-uris libmysofa=1.2.1~dfsg0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/libm/libmysofa/libmysofa_1.2.1%7edfsg0-1.dsc' libmysofa_1.2.1~dfsg0-1.dsc 2342 SHA512:883240a9ee68513411d3ead747f2aeeb3e6984706902d0d33edb6f2d57502b0156d7e5f224593d8e0918ef3d106c07a2db9f5982a312cef3a10257b3ef1960cc
'http://archive.ubuntu.com/ubuntu/pool/universe/libm/libmysofa/libmysofa_1.2.1%7edfsg0.orig.tar.xz' libmysofa_1.2.1~dfsg0.orig.tar.xz 72713932 SHA512:d7479c46b81d27a11aae2e4a8ff7a1d6e1c74781445e74ce229c2d15caccc0afdfa2fb1dd247704c8047a60edadf82f29b36b82300924374f647745d7a4c0e9a
'http://archive.ubuntu.com/ubuntu/pool/universe/libm/libmysofa/libmysofa_1.2.1%7edfsg0-1.debian.tar.xz' libmysofa_1.2.1~dfsg0-1.debian.tar.xz 16656 SHA512:b4a4d358c861d2b79e873a2d1e0094b883b253970fca40853c3beb4acceb1fbfbe7ecdd847f40858c47bb1d9438a9bc0d0c7e131f237a20130ee3857ce1406ca
```

### `dpkg` source package: `libnsl=1.3.0-2build2`

Binary Packages:

- `libnsl2:amd64=1.3.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libnsl2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+-autoconf-exception`
- `GPL-2+-libtool-exception`
- `GPL-3`
- `GPL-3+-autoconf-exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `permissive-autoconf-m4`
- `permissive-autoconf-m4-no-warranty`
- `permissive-configure`
- `permissive-fsf`
- `permissive-makefile-in`

Source:

```console
$ apt-get source -qq --print-uris libnsl=1.3.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-2build2.dsc' libnsl_1.3.0-2build2.dsc 2087 SHA512:f13d28f34b0e71b04b5a0313b1cc79cdbe7d5e7f910d649af63b42824654e3cf01c02caa0e68309cb03350a17506e034800af1b1e3ab9af99fb64121c119215c
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0.orig.tar.xz' libnsl_1.3.0.orig.tar.xz 321488 SHA512:a5a6c3ccb2d1e724c8c1f65e55dcd09383eb1ae019c55f4c09441eadf23ffbc2196cfad259805b0ac40ddf3a10af0da453e4d739d67d46829c64d0995dab4e55
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-2build2.debian.tar.xz' libnsl_1.3.0-2build2.debian.tar.xz 4868 SHA512:367904106ba925eaa667cc273b37afd052ba795b7ed004cdb501c13dd26b469df971ac10acec2bf57d91fa4839f356c7dcbcd4969914891152588365844ced9a
```

### `dpkg` source package: `libodfgen=0.1.8-2build2`

Binary Packages:

- `libodfgen-0.1-1:amd64=0.1.8-2build2`

Licenses: (parsed from: `/usr/share/doc/libodfgen-0.1-1/copyright`)

- `LGPL`
- `MPL-2.0 | LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libodfgen=0.1.8-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libo/libodfgen/libodfgen_0.1.8-2build2.dsc' libodfgen_0.1.8-2build2.dsc 2083 SHA512:bfc55d6066452b1cc42dc61795c0b467a31b7155010e469ce4bb6b57e8d70da82010b4971d8b0263a4537abad6e439365aed0f95c1a8100b0240d62ea02b42c7
'http://archive.ubuntu.com/ubuntu/pool/main/libo/libodfgen/libodfgen_0.1.8.orig.tar.xz' libodfgen_0.1.8.orig.tar.xz 386156 SHA512:e4a15aa7f1db483cdbb9c531bfb234b4794890cc583c70e8aa3374771be8928e7917105d48dab80d1ab6d57e43fa78415097d9b897cb12fb2a609f4647ee99d6
'http://archive.ubuntu.com/ubuntu/pool/main/libo/libodfgen/libodfgen_0.1.8-2build2.debian.tar.xz' libodfgen_0.1.8-2build2.debian.tar.xz 7132 SHA512:641b31f085fc3b52b5ebfc40a1dbd414df68644264f051f8fd8e95cc1aebfb8f950b2da09a32d0db18151057aed629bd3515f81437d1fa1068ab6bef265cb719
```

### `dpkg` source package: `libogg=1.3.5-0ubuntu3`

Binary Packages:

- `libogg0:amd64=1.3.5-0ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libogg=1.3.5-0ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/libo/libogg/libogg_1.3.5-0ubuntu3.dsc' libogg_1.3.5-0ubuntu3.dsc 2007 SHA512:9ea6a9d47a9a052376686de9bfbd92dc5d81eb8c1b9ac27f4818b93ee0deef80670b9d10c3ecaff73717dfe69803766c3de1367414416cfe08e09360c7737cd8
'http://archive.ubuntu.com/ubuntu/pool/main/libo/libogg/libogg_1.3.5.orig.tar.gz' libogg_1.3.5.orig.tar.gz 593071 SHA512:e4d798621bb04a62dcb831e58a444357635ab3bcb9efbdffa009cb0be1cafb5e72bf71cbcad5305aa5268a92076a03a7e564a19c0c8d54b93a05d9b03ad2da6b
'http://archive.ubuntu.com/ubuntu/pool/main/libo/libogg/libogg_1.3.5-0ubuntu3.diff.gz' libogg_1.3.5-0ubuntu3.diff.gz 7196 SHA512:1a39af96f9b7883c962671fabfe8fc78192ae98efa548ab5097688f801382d6f8cdfcc7dbb88840d1b36b2b81f870cfb495eec27bdb5b5a76691458b5bceefeb
```

### `dpkg` source package: `libopenmpt=0.6.1-1`

Binary Packages:

- `libopenmpt0:amd64=0.6.1-1`

Licenses: (parsed from: `/usr/share/doc/libopenmpt0/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris libopenmpt=0.6.1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/libo/libopenmpt/libopenmpt_0.6.1-1.dsc' libopenmpt_0.6.1-1.dsc 2412 SHA512:783729d8e464ad572a970b0f207e7cf9f9a285332b27df6552afa4ea368beb0d10584ceb7943e11aaf9f63418fbd7c7ed10043f4e2a8abbc64f369ab41565f07
'http://archive.ubuntu.com/ubuntu/pool/universe/libo/libopenmpt/libopenmpt_0.6.1.orig.tar.gz' libopenmpt_0.6.1.orig.tar.gz 1511280 SHA512:b43124746fc7c8bdbcfcf24c5cff1cd8330cab664fd1641ac7a35416ed25bb80c74f31db74085c13f4beb9774c17c12a4486c8c5e976f3fbb70a27c236c0f4fb
'http://archive.ubuntu.com/ubuntu/pool/universe/libo/libopenmpt/libopenmpt_0.6.1-1.debian.tar.xz' libopenmpt_0.6.1-1.debian.tar.xz 11068 SHA512:13c2118a89ad6b055f1294f64519733adfd4dbec9705ec8cca4d8011a4da4d0e9c778c7d3e72ae902eb0db29e66e898cebd5e4816799366bcc6f7d1f6e0d53c0
```

### `dpkg` source package: `liborcus=0.17.2-2`

Binary Packages:

- `liborcus-0.17-0:amd64=0.17.2-2`
- `liborcus-parser-0.17-0:amd64=0.17.2-2`

Licenses: (parsed from: `/usr/share/doc/liborcus-0.17-0/copyright`, `/usr/share/doc/liborcus-parser-0.17-0/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `MPL-2.0`
- `other`

Source:

```console
$ apt-get source -qq --print-uris liborcus=0.17.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/libo/liborcus/liborcus_0.17.2-2.dsc' liborcus_0.17.2-2.dsc 2943 SHA512:4a0a58a39dbf731a91b8541c0e0aad96cf5859b58c35bd47f8db1d08bdef5f862c6f03bd4335c766d4ec027ae754c7a8c0843fa3e185e3cbb83acd5cf2ac13b8
'http://archive.ubuntu.com/ubuntu/pool/main/libo/liborcus/liborcus_0.17.2.orig.tar.xz' liborcus_0.17.2.orig.tar.xz 1839188 SHA512:8ad8db46c23673260057aff555286d95ebfeff0a027bdeae24f11f8aa12456284f7f4446edddb91936b3011eb1227cfe1618ab3c4d909f8356c8c151f5739d79
'http://archive.ubuntu.com/ubuntu/pool/main/libo/liborcus/liborcus_0.17.2-2.debian.tar.xz' liborcus_0.17.2-2.debian.tar.xz 9148 SHA512:41334dfc1c02b27b72e45cab467275e59cfbe58fab3d6de5481be84c197b459e050594408a51be89db9be7f6b89741190dfcc839fcb3ba8a4e486c3ecf9b94c9
```

### `dpkg` source package: `libpagemaker=0.0.4-1build3`

Binary Packages:

- `libpagemaker-0.0-0:amd64=0.0.4-1build3`

Licenses: (parsed from: `/usr/share/doc/libpagemaker-0.0-0/copyright`)

- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libpagemaker=0.0.4-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpagemaker/libpagemaker_0.0.4-1build3.dsc' libpagemaker_0.0.4-1build3.dsc 2140 SHA512:7145882b6759bbfb830c6fbc815344ee636a94f779c629be1d8fd2641ceb8cd62af5ddc4a85942e51eceac1c504a458730dde8752df2a281d4894aaf329f2e9e
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpagemaker/libpagemaker_0.0.4.orig.tar.xz' libpagemaker_0.0.4.orig.tar.xz 306496 SHA512:d9d9436622ae378da2a3c8e50a35b6133582a595c9ff0fe0e3b124fd0b83f1f12afdfc6a27d16b509ca9bab33067215d7300e505d4bf6b280be7e4bf46da6c64
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpagemaker/libpagemaker_0.0.4-1build3.debian.tar.xz' libpagemaker_0.0.4-1build3.debian.tar.xz 6856 SHA512:e1b7eed211d8babcf4db73f65c4c004cb70efe2dce20f18c41491ca6cfd0520e398154d30b6097e53edf263d5fcb98d602c18b9a9cc3e8e3d71ac97899e1f40e
```

### `dpkg` source package: `libpaper=1.1.28build2`

Binary Packages:

- `libpaper1:amd64=1.1.28build2`

Licenses: (parsed from: `/usr/share/doc/libpaper1/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris libpaper=1.1.28build2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpaper/libpaper_1.1.28build2.dsc' libpaper_1.1.28build2.dsc 1736 SHA512:a0d06d6a23524e976ba8943c808c65dfbb137ce9235cc66ec9a439ff7ef3215b9ca1381846e81b79fc07706db909d0d9cc599bed0ca656930cba100fc4928576
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpaper/libpaper_1.1.28build2.tar.gz' libpaper_1.1.28build2.tar.gz 43246 SHA512:e8bb01c06ec6e9da24dbf142c22c7afd87cc9746a9a63408fed11d3815a2c13912fd7633ccd4479af12a74712d2998372ad02e38964411f15b4142e907b5e455
```

### `dpkg` source package: `libpciaccess=0.16-3`

Binary Packages:

- `libpciaccess0:amd64=0.16-3`

Licenses: (parsed from: `/usr/share/doc/libpciaccess0/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libpciaccess=0.16-3
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.16-3.dsc' libpciaccess_0.16-3.dsc 2291 SHA512:02fff14cb7c21619998bc5f6a67e20866ddd7f7e06ca6e328abb224368b23bc4fc60c18a646eb4d91b70d389354d20a0ca7799cb331eb51fdb77c4d654bc772d
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.16.orig.tar.gz' libpciaccess_0.16.orig.tar.gz 470061 SHA512:ed5fe0d8bf59155f5f06ed39793179549d6f604280a93019623109c8bc0d19409e15dad51277ac7711d8e1f0aa37eee0d6a029b084160dca2e6e03874bc07590
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.16.orig.tar.gz.asc' libpciaccess_0.16.orig.tar.gz.asc 659 SHA512:2ce1e5c092e26d8d6da8f32b20e51c28f87583b2cc821248d9fd4183890b1ac5bef171dce30a5c8612dd75cf10e7070a02ed117c67bd04f9a3659a27a3774e1a
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpciaccess/libpciaccess_0.16-3.diff.gz' libpciaccess_0.16-3.diff.gz 28681 SHA512:31f4791421ef020d283c419ca5c8829250ba8d365d2176c18652495601bb87d8be7c530f72b3c7cf9527168081cb77355e6e94348e41c609ddb396f5e691af8c
```

### `dpkg` source package: `libpgm=5.3.128~dfsg-2`

Binary Packages:

- `libpgm-5.3-0:amd64=5.3.128~dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libpgm-5.3-0/copyright`)

- `BSD-3-clause`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libpgm=5.3.128~dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/universe/libp/libpgm/libpgm_5.3.128%7edfsg-2.dsc' libpgm_5.3.128~dfsg-2.dsc 1828 SHA512:fe4ea5040790ba7761639a44150dc93f149d4e91aefe0f4930e3c1393d5bfd38a51eec0f556e2d3ed829868074c91f5967d5f43abd7e7c6dd94f2facac359183
'http://archive.ubuntu.com/ubuntu/pool/universe/libp/libpgm/libpgm_5.3.128%7edfsg.orig.tar.xz' libpgm_5.3.128~dfsg.orig.tar.xz 393292 SHA512:6706b6606c0cd92f29b72e39336092d559ba68d5ff80f3e1869f653420a78b2957c9ad7f0334063cfe3a5e81fa632f27416f473ccdfe07fccd253384fbed6f9a
'http://archive.ubuntu.com/ubuntu/pool/universe/libp/libpgm/libpgm_5.3.128%7edfsg-2.debian.tar.xz' libpgm_5.3.128~dfsg-2.debian.tar.xz 6204 SHA512:72909c6418a3de568ecebce7f535aeab36a19904d169745eb0645036c4a46f254357c3f5c46bb7f5b149712474422da1c26736a4f81b1c2be85596d554e67346
```

### `dpkg` source package: `libpng1.6=1.6.37-3build5`

Binary Packages:

- `libpng16-16:amd64=1.6.37-3build5`

Licenses: (parsed from: `/usr/share/doc/libpng16-16/copyright`)

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
$ apt-get source -qq --print-uris libpng1.6=1.6.37-3build5
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-3build5.dsc' libpng1.6_1.6.37-3build5.dsc 2357 SHA512:8628c50bf667f1b7134192cbaf7b9c7fc00d6c264027092ea3aaee089497ed7e417a63c824245945a5169000dd56d0787f4538f5563ef312b1be381766cadea0
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37.orig.tar.gz' libpng1.6_1.6.37.orig.tar.gz 1508805 SHA512:ccb3705c23b2724e86d072e2ac8cfc380f41fadfd6977a248d588a8ad57b6abe0e4155e525243011f245e98d9b7afbe2e8cc7fd4ff7d82fcefb40c0f48f88918
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-3build5.debian.tar.xz' libpng1.6_1.6.37-3build5.debian.tar.xz 32492 SHA512:58be3d57602b2c6d6d2788e16de69505cf54a381b51fbd3a1338b9708ed576965975b3994c5946231fe75055a323649667edf8971b3d4d3d736457609fca0770
```

### `dpkg` source package: `libpsl=0.21.0-1.2build2`

Binary Packages:

- `libpsl5:amd64=0.21.0-1.2build2`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.0-1.2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.0-1.2build2.dsc' libpsl_0.21.0-1.2build2.dsc 2348 SHA512:28ff7399af2290fd447f781b1f799ba5cb8c0cb794833c40d8f16cc81b0abd4f77bd9dc990c7925e8be8832555f07cc6ede80f971b68ac5fc6e644d601e582b6
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.0.orig.tar.gz' libpsl_0.21.0.orig.tar.gz 8598583 SHA512:b7466edb9763f94a65330dbb3c19586f9c7b01e20ddedb38ca2fd4c9ee5764a4f9b3291dc4b76659b45425d954f15973345f917b2cd2de72ea731e8c41f2a265
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.0-1.2build2.debian.tar.xz' libpsl_0.21.0-1.2build2.debian.tar.xz 12896 SHA512:9d8c7130bee8c521e4f1ab1e13edfe2ed2fec538bda9133662d4120e8f5303595e6f27f466f30b07e61b94e138dd2787e17af91b8cc29275b5b4d2e098133eee
```

### `dpkg` source package: `librabbitmq=0.10.0-1ubuntu2`

Binary Packages:

- `librabbitmq4:amd64=0.10.0-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/librabbitmq4/copyright`)

- `BSD-Author`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris librabbitmq=0.10.0-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librabbitmq/librabbitmq_0.10.0-1ubuntu2.dsc' librabbitmq_0.10.0-1ubuntu2.dsc 2191 SHA512:8f7ee491ff5d94575858a66b987d9116213bf3d24d6b0d651c08ca1b8637d6da42b2a84fe4c6540ae2f23e9608ac6d0e4b4c690d751259b24c3ba9bb4c6643d4
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librabbitmq/librabbitmq_0.10.0.orig.tar.gz' librabbitmq_0.10.0.orig.tar.gz 145361 SHA512:52a1194fab2dc8698ed065d63898e32aa004a4d68080d4aaf5cb7148cc28ad967283f7a99910d7f054cbba92b487b3a67b839b6f0bd88486ef9be043c9517d4c
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librabbitmq/librabbitmq_0.10.0-1ubuntu2.debian.tar.xz' librabbitmq_0.10.0-1ubuntu2.debian.tar.xz 10536 SHA512:a1f13f313d807bad8d39460a17d7350d29da43742959884aae2145524ecfb30e6c2538e08b07d685cef5392c81500f01c2c5796c469533865676419da36bd54d
```

### `dpkg` source package: `libraw1394=2.1.2-2build2`

Binary Packages:

- `libraw1394-11:amd64=2.1.2-2build2`

Licenses: (parsed from: `/usr/share/doc/libraw1394-11/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libraw1394=2.1.2-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw1394/libraw1394_2.1.2-2build2.dsc' libraw1394_2.1.2-2build2.dsc 2126 SHA512:ae5b2a14ab6aa0dd973ad9f2a8dce8206586098eedc0229277b533b058ba668f01f8ed158f856145a8e85cbdbfae50634e8d29bf4692a24f3ead5f1b8ae75967
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw1394/libraw1394_2.1.2.orig.tar.gz' libraw1394_2.1.2.orig.tar.gz 458134 SHA512:f82a9fd689635773f24a074d6d61f7f70a79a9ab336a25e28975f4b795423a915a24a8355819080f2d2f399741ae042d59f8319ea3dc0e4141e8bcadfa07afd8
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw1394/libraw1394_2.1.2-2build2.debian.tar.xz' libraw1394_2.1.2-2build2.debian.tar.xz 6920 SHA512:e9bf641bbb3024d71125db073c3c5868d4b3ab4ea04e6c887db82ad44a8980a1ede7c972c762995428579314d12c256bad76ac83c87b05efaa8a8854eeb3a654
```

### `dpkg` source package: `libreoffice=1:7.3.7-0ubuntu0.22.04.10`

Binary Packages:

- `fonts-opensymbol=2:102.12+LibO7.3.7-0ubuntu0.22.04.10`
- `libreoffice=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-base=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-base-core=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-base-drivers=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-calc=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-common=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-core=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-draw=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-impress=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-math=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-report-builder-bin=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-style-colibre=1:7.3.7-0ubuntu0.22.04.10`
- `libreoffice-writer=1:7.3.7-0ubuntu0.22.04.10`
- `libuno-cppu3=1:7.3.7-0ubuntu0.22.04.10`
- `libuno-cppuhelpergcc3-3=1:7.3.7-0ubuntu0.22.04.10`
- `libuno-purpenvhelpergcc3-3=1:7.3.7-0ubuntu0.22.04.10`
- `libuno-sal3=1:7.3.7-0ubuntu0.22.04.10`
- `libuno-salhelpergcc3-3=1:7.3.7-0ubuntu0.22.04.10`
- `python3-uno=1:7.3.7-0ubuntu0.22.04.10`
- `uno-libs-private=1:7.3.7-0ubuntu0.22.04.10`
- `ure=1:7.3.7-0ubuntu0.22.04.10`

Licenses: (parsed from: `/usr/share/doc/fonts-opensymbol/copyright`, `/usr/share/doc/libreoffice/copyright`, `/usr/share/doc/libreoffice-base/copyright`, `/usr/share/doc/libreoffice-base-core/copyright`, `/usr/share/doc/libreoffice-base-drivers/copyright`, `/usr/share/doc/libreoffice-calc/copyright`, `/usr/share/doc/libreoffice-common/copyright`, `/usr/share/doc/libreoffice-core/copyright`, `/usr/share/doc/libreoffice-draw/copyright`, `/usr/share/doc/libreoffice-impress/copyright`, `/usr/share/doc/libreoffice-math/copyright`, `/usr/share/doc/libreoffice-report-builder-bin/copyright`, `/usr/share/doc/libreoffice-style-colibre/copyright`, `/usr/share/doc/libreoffice-writer/copyright`, `/usr/share/doc/libuno-cppu3/copyright`, `/usr/share/doc/libuno-cppuhelpergcc3-3/copyright`, `/usr/share/doc/libuno-purpenvhelpergcc3-3/copyright`, `/usr/share/doc/libuno-sal3/copyright`, `/usr/share/doc/libuno-salhelpergcc3-3/copyright`, `/usr/share/doc/python3-uno/copyright`, `/usr/share/doc/uno-libs-private/copyright`, `/usr/share/doc/ure/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `MPL-2.0`
- `MPL_2.0`
- `other`

Source:

```console
$ apt-get source -qq --print-uris libreoffice=1:7.3.7-0ubuntu0.22.04.10
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7-0ubuntu0.22.04.10.dsc' libreoffice_7.3.7-0ubuntu0.22.04.10.dsc 25786 SHA512:29563781edd3645e4d10edc1fc0087dcdade8b474923162525ab1540304471ed2a209c71e61aae1ef17fdacbbb0dfa164b7cf62c606090220bee909c15a9ab86
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7.orig-helpcontent2.tar.xz' libreoffice_7.3.7.orig-helpcontent2.tar.xz 112067652 SHA512:5f29783b6483824a61c700ad7516a97e69373498ca7dcbe0e24229246d2bd0fb24a2c9e555107af21b9eed35c504f0b65c4e5b5a2aadb79de1a4fa8b21e2bc98
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7.orig-tarballs.tar.xz' libreoffice_7.3.7.orig-tarballs.tar.xz 324661956 SHA512:d13cc4817a4fb298049f0306599cf25dee5906a920871c5ef58cdea9019e49580587b51c8af29946eea2d9720ca5f66ee9e2bc8a67ff7d2b1b8377bc02930521
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7.orig-translations.tar.xz' libreoffice_7.3.7.orig-translations.tar.xz 208926792 SHA512:d9895f425c7d5928915858af4d560db0b6380477b87add69c103789b4eff3b169360164609c480b9b5591a69f4130b4c77a0741b00b839126d7ce03cbcd4a6f9
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7.orig-yaru.tar.xz' libreoffice_7.3.7.orig-yaru.tar.xz 19257660 SHA512:a3bb9e04992224dba3f0a1a2edcf59a06b1c6dfaf71ef8de1fff87f7f6ade96a4557f171f374bc29e661765ef56d2f72e41c574b983d0fa9c3e3acf84439ba03
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7.orig.tar.xz' libreoffice_7.3.7.orig.tar.xz 256653492 SHA512:f7b6279f5ef9f5ad8290d2bdf4fd54f8df7775a21094ba762dbd9299effab31d4f2c6dff9f4b3d9c5673596931df1d16b195474b547007bfc9a396c47e5e181c
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7.orig.tar.xz.asc' libreoffice_7.3.7.orig.tar.xz.asc 833 SHA512:d3cf63b93c397cdf5ecee84b4e544855f5783092fc1e06e6cf798a4a2c908ae389e0111b40828adbeab3f878db1e831ebd0daa50597bc0ff4b27be7b8acdd089
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_7.3.7-0ubuntu0.22.04.10.debian.tar.xz' libreoffice_7.3.7-0ubuntu0.22.04.10.debian.tar.xz 2416028 SHA512:0c26700f6afd11c15483fcd36cced5b4a6c03dbd627339ba9af34d55c8223bf9b1053999644e36cbd3d5e93be7fc4c32b4637d05a171d67145652a5e711e7231
```

### `dpkg` source package: `librevenge=0.0.4-6ubuntu7`

Binary Packages:

- `librevenge-0.0-0:amd64=0.0.4-6ubuntu7`

Licenses: (parsed from: `/usr/share/doc/librevenge-0.0-0/copyright`)

- `LGPL-2.1`
- `MPL-1.1 | GPL-3+ | LGPL-3+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris librevenge=0.0.4-6ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librevenge/librevenge_0.0.4-6ubuntu7.dsc' librevenge_0.0.4-6ubuntu7.dsc 2151 SHA512:53d403de93eae19f8e3f2939137ade1e4c94a2d0213565ad8c820fcf3567327e7dfa6f983f4a3e65cde3bedc411cc13468c464abcf85cd88fb2375f05ea50249
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librevenge/librevenge_0.0.4.orig.tar.bz2' librevenge_0.0.4.orig.tar.bz2 529833 SHA512:9430158503a42a3b2ee2c34426e647facd773886fd256c0fc6f6d04fd58dee87745118688058bf8e2418685b49c6559fc9e6c878d6282061294fb98cb46e4c86
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librevenge/librevenge_0.0.4-6ubuntu7.debian.tar.xz' librevenge_0.0.4-6ubuntu7.debian.tar.xz 14004 SHA512:77dad5e63779e8cd604df1ef726fb11a45eb1470e501f5aebd2137cbd56b88a99c3786b353f8aa180c3da8ead460a601c20746f37f62df8f9c1f794b016acd06
```

### `dpkg` source package: `librsvg=2.52.5+dfsg-3ubuntu0.2`

Binary Packages:

- `librsvg2-2:amd64=2.52.5+dfsg-3ubuntu0.2`

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
- `CC-BY-3.0`
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
$ apt-get source -qq --print-uris librsvg=2.52.5+dfsg-3ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.52.5%2bdfsg-3ubuntu0.2.dsc' librsvg_2.52.5+dfsg-3ubuntu0.2.dsc 3126 SHA512:de08f845fd7b27d57369a01ec7a6d15063af5fbc39d35d306c40354b2254dca4e2721f98bec5ed64a1e2d1772a2df7436ef32a55cde8850b09ecfb1b637f1734
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.52.5%2bdfsg.orig.tar.xz' librsvg_2.52.5+dfsg.orig.tar.xz 20813024 SHA512:641dcd149ce0d5117947e3fcb04efd41591812953ec4b12ba350ce9950ed4bcb26726a78df9d317e6bd557e6fd463867476205b5e6720a9a15bd1bcfcb6f7ffe
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.52.5%2bdfsg-3ubuntu0.2.debian.tar.xz' librsvg_2.52.5+dfsg-3ubuntu0.2.debian.tar.xz 37684 SHA512:171868ea6d28e98afb6af4c75eb05de3b85a7adb21ae5ac36d8720fb86fa30769795a2487a2979e735662a6da9fcc4ce41a2caa128aa5044892904885e9c7e0a
```

### `dpkg` source package: `libsamplerate=0.2.2-1build1`

Binary Packages:

- `libsamplerate0:amd64=0.2.2-1build1`

Licenses: (parsed from: `/usr/share/doc/libsamplerate0/copyright`)

- `BSD-2-clause`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libsamplerate=0.2.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsamplerate/libsamplerate_0.2.2-1build1.dsc' libsamplerate_0.2.2-1build1.dsc 2302 SHA512:1f80524bc8f7c27896e98b773a63339cda7d754c4b3b0aecc5d128e9993114a9fdc222527510c77b3df29ba901efe5ad199442b0b9d0a9c59a015fc4ccec5acc
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsamplerate/libsamplerate_0.2.2.orig.tar.gz' libsamplerate_0.2.2.orig.tar.gz 3954784 SHA512:37e0fd604907caf978659466289315befd66eec16c21a94e0b6106de18ffe803fbf2e7f3a8fb0430b33c0b784ecd6d4eaf3b9a862ed2670104647decbee913d6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsamplerate/libsamplerate_0.2.2-1build1.debian.tar.xz' libsamplerate_0.2.2-1build1.debian.tar.xz 7420 SHA512:a10be5d7067edbbaedba1b12898a6b718e10e78cf59ed33352433bcd684da9bd55b44faa13047190465ea18a5bd37cf443e349bf7a7a0b355242961c222e0c42
```

### `dpkg` source package: `libsdl2=2.0.20+dfsg-2ubuntu1.22.04.1`

Binary Packages:

- `libsdl2-2.0-0:amd64=2.0.20+dfsg-2ubuntu1.22.04.1`

Licenses: (parsed from: `/usr/share/doc/libsdl2-2.0-0/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-3-clause-chromium`
- `BSD-3-clause-kitware`
- `BrownUn_UnCalifornia_ErikCorry`
- `Expat`
- `Expat-like`
- `GPL-3`
- `Gareth_McCaughan`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT-open-group`
- `Mozilla-permissive`
- `PublicDomain_David_Ludwig`
- `PublicDomain_Edgar_Simo`
- `PublicDomain_Sam_Lantinga`
- `RSA_Data_Security`
- `SGI-Free-Software-License-B`
- `SunPro`
- `hidapi-orig`
- `hidapi-orig,`
- `zlib-libpng-like-permissive`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris libsdl2=2.0.20+dfsg-2ubuntu1.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsdl2/libsdl2_2.0.20%2bdfsg-2ubuntu1.22.04.1.dsc' libsdl2_2.0.20+dfsg-2ubuntu1.22.04.1.dsc 3051 SHA512:8f2e5549eff4ee3039343ade163e3b3cf2b465d34dbd600e1cee4511dc334623c905e5cc0134226abd1f63ec8ab09d143d0fad682c6b97a965d9f84369a8519d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsdl2/libsdl2_2.0.20%2bdfsg.orig.tar.xz' libsdl2_2.0.20+dfsg.orig.tar.xz 3086284 SHA512:89f8f57cd66a7219e994f632501d86a445efdf1554454f851e4c04e2ba23715fb8299f42ad0e74416b069afb23d9fa309bc5f5992fe0fa6a8a24ce06344585e2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsdl2/libsdl2_2.0.20%2bdfsg-2ubuntu1.22.04.1.debian.tar.xz' libsdl2_2.0.20+dfsg-2ubuntu1.22.04.1.debian.tar.xz 30892 SHA512:deeb3f11ccba318d26118424012dee9cc7c5b28b2d091382091d26ad10f4940b59b3acf79c51d2bdec1afd78c02733269a66822aaf83f7ca635c3ca647bba74a
```

### `dpkg` source package: `libseccomp=2.5.3-2ubuntu3~22.04.1`

Binary Packages:

- `libseccomp2:amd64=2.5.3-2ubuntu3~22.04.1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.3-2ubuntu3~22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3-2ubuntu3%7e22.04.1.dsc' libseccomp_2.5.3-2ubuntu3~22.04.1.dsc 2860 SHA512:332a059782f315e840f19f756baebbc4f6021ee6a1c0dc53ecfc36df5385e30d6b00363a73e16978a46cd099f552f697189b1313c2ce96fa2b652eaf320eac68
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3.orig.tar.gz' libseccomp_2.5.3.orig.tar.gz 637572 SHA512:00170fe2360f0c0b33293dccfcc33e98fabb99619f34ecefbcc92bfdaa249ba91e7433226545b842b71542a3b224b6e980ea2ae656c4addf07e84a0def1870a0
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3.orig.tar.gz.asc' libseccomp_2.5.3.orig.tar.gz.asc 833 SHA512:c879872448471fb1e01617145473254a0536ade1ff1e12871793631c3c63199cd46cb48317b4d596294d5cb187ff1fe9b58dc20ce52a89bfc9234a566bf8eb85
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3-2ubuntu3%7e22.04.1.debian.tar.xz' libseccomp_2.5.3-2ubuntu3~22.04.1.debian.tar.xz 24328 SHA512:2eca56dc8497a403e87f9ff4efe4f12b37e0443de6fad5884669f156f19590572cfaeae6b3d1073bd1a64188fa563699a7454de80c1999e8240c93c6029a4e72
```

### `dpkg` source package: `libselinux=3.3-1build2`

Binary Packages:

- `libselinux1:amd64=3.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.3-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.3-1build2.dsc' libselinux_3.3-1build2.dsc 2644 SHA512:e6f6744aeef21f3acf9c36fc6251515e6be8caf1b4953ed20d2346897c72bc919ae7e26ab8dfd0c2cf24029bd39da073e57ea19df15af106ce86ab4537c691aa
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.3.orig.tar.gz' libselinux_3.3.orig.tar.gz 206826 SHA512:9a89c05ea4b17453168a985ece93ba6d6c4127916e657c46d4135eb59a1f6408faa0802cc2e49187defbde5247d659037beee089877affbab3eab6af3433696c
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.3-1build2.debian.tar.xz' libselinux_3.3-1build2.debian.tar.xz 24052 SHA512:75e344ef0d123659105774a0fe941f5821d230bd3f4db0453918407325f6c08246db2cd609ec0ba51090b2942cd1a9a1865245a18834fa1b234d730103799c0c
```

### `dpkg` source package: `libsemanage=3.3-1build2`

Binary Packages:

- `libsemanage-common=3.3-1build2`
- `libsemanage2:amd64=3.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.3-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.3-1build2.dsc' libsemanage_3.3-1build2.dsc 2690 SHA512:6337e23938be6ebe18321ce9e67802ceaa2637e37bdc0940c4a4501e73f25235c662de1ec85807062327d2d5c5e7078ad0fb20d660e075710726cd0ede51e2fc
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.3.orig.tar.gz' libsemanage_3.3.orig.tar.gz 178890 SHA512:6026d9773c0886436ad801bc0c8beac888b6fb62034edeb863192dea4b6ef34a88e080758820fe635a20e048ac666beee505a0f946258f18571709cca5228aad
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.3-1build2.debian.tar.xz' libsemanage_3.3-1build2.debian.tar.xz 17920 SHA512:b23e000956a6fc96c7609a749d1974874834b6a463b0f5b42b3e4bde75f560789f7ef7f385a3a7297e97f7c610cd0c2899986b3a228671a57e051310441b0c90
```

### `dpkg` source package: `libsepol=3.3-1build1`

Binary Packages:

- `libsepol2:amd64=3.3-1build1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.3-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.3-1build1.dsc' libsepol_3.3-1build1.dsc 2217 SHA512:91f9c8436df88aa898f2e3ea4a8bbb0cb21de84153bc88b9fff30b2aa3f0e6b11d5b9f506b81d0266e8a4881ea86d6590abe64b8eacc2d8cdeaf1a0f5f2784bf
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.3.orig.tar.gz' libsepol_3.3.orig.tar.gz 482546 SHA512:fb6bb69f8e43a911a1a9cbd791593215386e93cb9292e003f5d8efe6e86e0ce5d0287e95d52fe2fbce518a618beaf9b1135aea0d04eaebcdbd8c6d07ee67b500
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.3-1build1.debian.tar.xz' libsepol_3.3-1build1.debian.tar.xz 15068 SHA512:adb210e2dab83baa49cee624dc5ae44e9f2dff6eb4a0a7bee4b958e99871580df159d0ca339feca31d9c4cdd92d0022a841c35d615436278046379eeb766f1f2
```

### `dpkg` source package: `libsm=2:1.2.3-1build2`

Binary Packages:

- `libsm6:amd64=2:1.2.3-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build2.dsc' libsm_1.2.3-1build2.dsc 2170 SHA512:4dc5d9445614801154fb411ae2089c80c55adaea90a9d78a958724d70fc8ea8d36c9a898a478f18a9669f3448d9d9a948c632f2a4869287d1e1f88403e304096
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA512:03b77d86b33cdb3df4f9d65131a0025182f3cb0c17b33a90d236e8563b3011d225b9d006186302d07850edafa5b899aec6a086b8d437d357cd69fedd5f22d94b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build2.diff.gz' libsm_1.2.3-1build2.diff.gz 9062 SHA512:c5ddeb48fe7c846b31382a5da42a2970ae12995afb322c6291977b7ffd2251d4d9e9dc163ecb008902ae8ee3c3a44526115bddc92b402c8f4a9ea0f29f1cb037
```

### `dpkg` source package: `libsndfile=1.0.31-2ubuntu0.2`

Binary Packages:

- `libsndfile1:amd64=1.0.31-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libsndfile1/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `gsm`
- `sun`

Source:

```console
$ apt-get source -qq --print-uris libsndfile=1.0.31-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsndfile/libsndfile_1.0.31-2ubuntu0.2.dsc' libsndfile_1.0.31-2ubuntu0.2.dsc 2277 SHA512:cea2fbcad3778eabf347f0dce7fd4503970c68de5ad23a9961afeccdf39c60d31641357669ea3cd2b04e96d8c365030e7cd3d868c7a1ad3ceca882b87b0841e6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsndfile/libsndfile_1.0.31.orig.tar.gz' libsndfile_1.0.31.orig.tar.gz 662584 SHA512:5767ced306f2d300aa2014d383c22f3ee9a4fe1ffb2c463405bc26209ede09a9cfb95e1c08256db36e986d2b30151c38dbe635a3cae0b7138d7de485e2084891
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsndfile/libsndfile_1.0.31-2ubuntu0.2.debian.tar.xz' libsndfile_1.0.31-2ubuntu0.2.debian.tar.xz 25092 SHA512:64d478af31f56d4cd3d2cc091be48373ed08ff4083664a1d74833859f2c650e86deb6990b55f8e838ccf43ad230a3c54617a4afaf21d89bf20cb29165c26876f
```

### `dpkg` source package: `libsodium=1.0.18-1build2`

Binary Packages:

- `libsodium23:amd64=1.0.18-1build2`

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
$ apt-get source -qq --print-uris libsodium=1.0.18-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsodium/libsodium_1.0.18-1build2.dsc' libsodium_1.0.18-1build2.dsc 2045 SHA512:7300887b9334490ba77d766b9d6f96182c12c1afd6be7111f2fe3558b7ec38c743e63f36d0781868410cd6416b24b8d9a2187ca202a9790b6944df6b31e62aa2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsodium/libsodium_1.0.18.orig.tar.gz' libsodium_1.0.18.orig.tar.gz 1619527 SHA512:727fe50a5fb1df86ec5d807770f408a52609cbeb8510b4f4183b2a35a537905719bdb6348afcb103ff00ce946a8094ac9559b6e3e5b2ccc2a2d0c08f75577eeb
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsodium/libsodium_1.0.18-1build2.debian.tar.xz' libsodium_1.0.18-1build2.debian.tar.xz 7648 SHA512:9fd701c5437a3b41c2df0152e02d6a23b31eeaa8627de7a001abf2269f3ca869cfcdc2f9ccabf87aa7879f729ee8a1fad08dd2abdf98750d0186ec6db9141039
```

### `dpkg` source package: `libsoxr=0.1.3-4build2`

Binary Packages:

- `libsoxr0:amd64=0.1.3-4build2`

Licenses: (parsed from: `/usr/share/doc/libsoxr0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`
- `Spherepack`
- `permissive1`
- `permissive2`

Source:

```console
$ apt-get source -qq --print-uris libsoxr=0.1.3-4build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsoxr/libsoxr_0.1.3-4build2.dsc' libsoxr_0.1.3-4build2.dsc 2278 SHA512:0fc21a96842dd1f4b9cb2f46ff04f1d95d46f858bbb9139f61202ebe435e2c6747df24937fe5c55acf1d9a8ae2eb4ecd916016e2debc4301e213806d2b9e825c
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsoxr/libsoxr_0.1.3.orig.tar.xz' libsoxr_0.1.3.orig.tar.xz 94384 SHA512:f4883ed298d5650399283238aac3dbe78d605b988246bea51fa343d4a8ce5ce97c6e143f6c3f50a3ff81795d9c19e7a07217c586d4020f6ced102aceac46aaa8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsoxr/libsoxr_0.1.3-4build2.debian.tar.xz' libsoxr_0.1.3-4build2.debian.tar.xz 5204 SHA512:1d035d3401469e531eb4a1552e5cbbaece8b0c455fe75f73898b925752a42c1c8e008440f450f0d1c6d70f52735dba673f72f019ae84cd38f9052e5dc177da00
```

### `dpkg` source package: `libssh=0.9.6-2ubuntu0.22.04.5`

Binary Packages:

- `libssh-4:amd64=0.9.6-2ubuntu0.22.04.5`
- `libssh-gcrypt-4:amd64=0.9.6-2ubuntu0.22.04.5`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`, `/usr/share/doc/libssh-gcrypt-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.9.6-2ubuntu0.22.04.5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6-2ubuntu0.22.04.5.dsc' libssh_0.9.6-2ubuntu0.22.04.5.dsc 2750 SHA512:b18f8255da313d01e8883e8b29a38648bd5e40df4d37af010224aacf9cf8e2a4c1320e3d7912e969319c01efe80d97005880346cbb1975008ffa5f91c7bfc4a1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6.orig.tar.xz' libssh_0.9.6.orig.tar.xz 1053056 SHA512:4040ec4af937e95be2e41313ef6d4db60b46b8d4dea10c09402398127c1d1ca8843392d207088aeee3c7ef631c6ae7b66861327dcebf78ed3af0723777619fd1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6.orig.tar.xz.asc' libssh_0.9.6.orig.tar.xz.asc 833 SHA512:1b6223efe9e4ce864cd8d97d517f9f0d38c1cd502b5874fdc6a58731038c2830a72ce753f02fc062d9d4d5922107ec9a2e62fe24a704bb5dec0dcfecdb569fe6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6-2ubuntu0.22.04.5.debian.tar.xz' libssh_0.9.6-2ubuntu0.22.04.5.debian.tar.xz 67620 SHA512:d3b344a719d30b94916252a8c705dbc6c41bb522412c7cafb55b85d4a2cccb81ccaaf9a65a3cd6113a3093addf18a3b71e4c279069ef7d082992e2a43cc25e4f
```

### `dpkg` source package: `libtasn1-6=4.18.0-4ubuntu0.1`

Binary Packages:

- `libtasn1-6:amd64=4.18.0-4ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.18.0-4ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0-4ubuntu0.1.dsc' libtasn1-6_4.18.0-4ubuntu0.1.dsc 2822 SHA512:cc9eb79ad785b04a23f1b49a17ef513a3f54762c5c098b4b277facf606178faf1fe51c809329750c11b1250489a9c149073840905c8ce3bfbe14417707600390
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0.orig.tar.gz' libtasn1-6_4.18.0.orig.tar.gz 1724441 SHA512:4f2f4afc7561fda7a1f1c6c525c3c3b08228a1a4aa8c3d3d5e02e993d8f83ccee1dd0f1b201cec0fbfc97043d4b1d7a95ffd34d65422a38b85b931ac7a015831
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0.orig.tar.gz.asc' libtasn1-6_4.18.0.orig.tar.gz.asc 228 SHA512:8ef3918a3130f695d2d5b26dd945084b931005eff8914c50a0ac9795d4cc6ec9e9645e2941ff4235cba3b4b2987ab1c7da65225e24ce16aaab844352ecdafbf6
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0-4ubuntu0.1.debian.tar.xz' libtasn1-6_4.18.0-4ubuntu0.1.debian.tar.xz 24684 SHA512:fb1e591cb80f106438ae72fd6e11fbedc0585825e22d84313d37fe0a9f2cf03138b401ef7591afc27e719920401ee2bedd3a3aec8ef7efff21511ae072fd68d3
```

### `dpkg` source package: `libthai=0.1.29-1build1`

Binary Packages:

- `libthai-data=0.1.29-1build1`
- `libthai0:amd64=0.1.29-1build1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.29-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-1build1.dsc' libthai_0.1.29-1build1.dsc 2457 SHA512:d4181f56ccec5cddf5e65a01386d30b51a1e9cea2fd671577fa5cf14435ea3e9b0a6e6668f1f008a0d4180067d4498b163309f5a7a51b2f4ef64ab868439bb0c
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA512:0ba1261581a1705a2a2546a3071acb3c63892dbf111f0dad415667165a6b9542a5e4549061c67b11ec53de7c9e70fceb3c04d794fd12a22d991a539dbacebda1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-1build1.debian.tar.xz' libthai_0.1.29-1build1.debian.tar.xz 12676 SHA512:fd2032f66f172ee3e2646099205474c2bbe6a0dd0f0fd685b9e8add66017a160946d5708b4bac4ae9aa5da3062eafdc34c0228c99910b1c013aaee29b9ab9d07
```

### `dpkg` source package: `libtheora=1.1.1+dfsg.1-15ubuntu4`

Binary Packages:

- `libtheora0:amd64=1.1.1+dfsg.1-15ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libtheora0/copyright`)

- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libtheora=1.1.1+dfsg.1-15ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtheora/libtheora_1.1.1%2bdfsg.1-15ubuntu4.dsc' libtheora_1.1.1+dfsg.1-15ubuntu4.dsc 2739 SHA512:06085578f13ce55a7e8a3ecdaa23104349425ad3eb7d45b9f11310f8ae7f905873b9b317257c8672b025718d7da3272ae07ed89b528c6c9373295d0defba48cb
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtheora/libtheora_1.1.1%2bdfsg.1.orig.tar.gz' libtheora_1.1.1+dfsg.1.orig.tar.gz 2100495 SHA512:dca7a0504baed32a84e71e6b035946d43ac8ad3d008b3651a1e0616998bdba9c627e6d46afbe306eb9c7b044293b46b370c5b1b3a8715865cd0edf6d955bef3d
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtheora/libtheora_1.1.1%2bdfsg.1-15ubuntu4.debian.tar.xz' libtheora_1.1.1+dfsg.1-15ubuntu4.debian.tar.xz 11080 SHA512:c3aff47cbd0a569367e9be0533e70a25328ffbfd0e288eac447abcfd73b2f01b0cab5bac23c22de681ec9bbe699a815498ad9ab7df900758f0f2f88ab0f46dd3
```

### `dpkg` source package: `libtirpc=1.3.2-2ubuntu0.1`

Binary Packages:

- `libtirpc-common=1.3.2-2ubuntu0.1`
- `libtirpc3:amd64=1.3.2-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libtirpc-common/copyright`, `/usr/share/doc/libtirpc3/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-4-Clause`
- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PERMISSIVE`
- `__AUTO_PERMISSIVE__`

Source:

```console
$ apt-get source -qq --print-uris libtirpc=1.3.2-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2-2ubuntu0.1.dsc' libtirpc_1.3.2-2ubuntu0.1.dsc 2201 SHA512:da9e64904445de59217c2bfa55ca9739e0b08ac4693a45a813b7fc67273e106a11e7076d39d24e5f62d242af4e2eaac9e5503072b57f4cf7bdfa579a82920e77
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2.orig.tar.bz2' libtirpc_1.3.2.orig.tar.bz2 513151 SHA512:8664d5c4f842ee5acf83b9c1cadb7871f17b8157a7c4500e2236dcfb3a25768cab39f7c5123758dcd7381e30eb028ddfa26a28f458283f2dcea3426c9878c255
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2-2ubuntu0.1.debian.tar.xz' libtirpc_1.3.2-2ubuntu0.1.debian.tar.xz 18364 SHA512:5440c46e49837b176b8087d82762002766e48a7d487e101049079637ebb93c21fbb1dccd63a319f72ee11d7964873c00dc98a7b5b320355d640df7f9e16ab1c7
```

### `dpkg` source package: `libtool=2.4.6-15build2`

Binary Packages:

- `libltdl7:amd64=2.4.6-15build2`

Licenses: (parsed from: `/usr/share/doc/libltdl7/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.4.6-15build2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6-15build2.dsc' libtool_2.4.6-15build2.dsc 2634 SHA512:a7cdb710cae727fdb1948326fc7af9faef0634b1ebfebfcdfb94407cc2242af45e408c48bff07d075fa7f608c2f06f9257c64ec7d21341b771bf4b55f04ed5c9
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6.orig.tar.xz' libtool_2.4.6.orig.tar.xz 973080 SHA512:a6eef35f3cbccf2c9e2667f44a476ebc80ab888725eb768e91a3a6c33b8c931afc46eb23efaee76c8696d3e4eed74ab1c71157bcb924f38ee912c8a90a6521a4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6.orig.tar.xz.asc' libtool_2.4.6.orig.tar.xz.asc 380 SHA512:2f26447a837e3242b8f8f38fbab22d89df0949ee62fd966af3b5bae3aa939ba53bc4621174ee58d1c6722d569d7fe5f90097ddccffed28c3067fe5fa996fcb89
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6-15build2.debian.tar.xz' libtool_2.4.6-15build2.debian.tar.xz 54076 SHA512:324a79af930a793b3b0031a1bb727b5ed16016b8e55294f24410ee9cfe2a2db75aab2d1ace8901fdaba610069f00e246d4d552faa23d583c741da0de438377cb
```

### `dpkg` source package: `libudfread=1.1.2-1`

Binary Packages:

- `libudfread0:amd64=1.1.2-1`

Licenses: (parsed from: `/usr/share/doc/libudfread0/copyright`)

- `GPL-2`
- `GPL-2+ with autoconf-macro exception`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libudfread=1.1.2-1
'http://archive.ubuntu.com/ubuntu/pool/universe/libu/libudfread/libudfread_1.1.2-1.dsc' libudfread_1.1.2-1.dsc 2020 SHA512:56e04c16c7dad77d834897fa21ff5c220ff50f5e13750d056780e69e6d67b084619c7a17e8937d85060d34f3471d9bd06609bc5d8f122e63d1a9ee8801fbfb59
'http://archive.ubuntu.com/ubuntu/pool/universe/libu/libudfread/libudfread_1.1.2.orig.tar.gz' libudfread_1.1.2.orig.tar.gz 33744 SHA512:3069feb5db40288beb5b112b285186162a704f0fdd3cf67a17fd4eeea015f2cfcfbb455b7aa7c3d79d00fd095a3fd11cffc7b121dce94d99c3b06a509a8977d2
'http://archive.ubuntu.com/ubuntu/pool/universe/libu/libudfread/libudfread_1.1.2-1.debian.tar.xz' libudfread_1.1.2-1.debian.tar.xz 2920 SHA512:0996aa21173478bb4a34e6c863ced37639ea84bbc6d4c57c24ddc74ec355f103997e28e5ae921f0a34ac1104c467f80d520817851a500ed29e13f7c8cce078f8
```

### `dpkg` source package: `libunistring=1.0-1`

Binary Packages:

- `libunistring2:amd64=1.0-1`

Licenses: (parsed from: `/usr/share/doc/libunistring2/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.0-1.dsc' libunistring_1.0-1.dsc 1928 SHA512:630d20ef6dd19be991147131d38acae2db15d1df34403264a15a373fcd4b661efffc1ae3916c52448f05cafb93bf1266527efa6630a02def88b86495d688a0c3
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.0.orig.tar.xz' libunistring_1.0.orig.tar.xz 2367800 SHA512:70d5ad82722844dbeacdfcb4d7593358e4a00a9222a98537add4b7f0bf4a2bb503dfb3cd627e52e2a5ca1d3da9e5daf38a6bd521197f92002e11e715fb1662d1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.0-1.debian.tar.xz' libunistring_1.0-1.debian.tar.xz 42004 SHA512:f9208e7ab38cc742bb46dc1a871ddb03847b99b6169e20e8d8660dd9cdf22bffb27f9b329dcbd025ad9b26aee5a2aab01337f36d8ab3020d2e752f9c2d4368ce
```

### `dpkg` source package: `libunwind=1.3.2-2build2.1`

Binary Packages:

- `libunwind8:amd64=1.3.2-2build2.1`

Licenses: (parsed from: `/usr/share/doc/libunwind8/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libunwind=1.3.2-2build2.1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.3.2-2build2.1.dsc' libunwind_1.3.2-2build2.1.dsc 2929 SHA512:2c7543dbb427b461b2f0f106a42e97e18ad6477e7d73a4ef094e7013d450823503e2f9164477932b8d44aa727fea020968de8e09498057c04749ee8277f93d07
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.3.2.orig.tar.gz' libunwind_1.3.2.orig.tar.gz 854114 SHA512:221864eae6bf0fde281d9551662af1e539ce919fbb7050947e60dbcc09efed4f5d34574dbce11792513e63151e0af72f02801b7bcd37a6a519e6d868abb8b509
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.3.2.orig.tar.gz.asc' libunwind_1.3.2.orig.tar.gz.asc 659 SHA512:3ee5c16592a8c1c1ea62070d764ed09816e4441c724c2ea188fb368f2413e29f3a20e7cd241ab65753b28c77f589c92de4f7afbae058d4384e4dbbb441ef007d
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunwind/libunwind_1.3.2-2build2.1.debian.tar.xz' libunwind_1.3.2-2build2.1.debian.tar.xz 20156 SHA512:1296e9f4659bf9f345498f869f481b0f42c6cdf64249c4b0161b246e72994072290aada8ec9a4df86d4c9afaa61358620c6b4022585efa21d977ca09cc26de35
```

### `dpkg` source package: `libusb-1.0=2:1.0.25-1ubuntu2`

Binary Packages:

- `libusb-1.0-0:amd64=2:1.0.25-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libusb-1.0-0/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libusb-1.0=2:1.0.25-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libusb-1.0/libusb-1.0_1.0.25-1ubuntu2.dsc' libusb-1.0_1.0.25-1ubuntu2.dsc 1636 SHA512:a57172dd5247ad5a7e0492a129f27c4cdb6662c5ef6a886433c383ae95f38f2e1a85ed5f8c00f91f893118eb37e7b9a4acd6ae18367f5c9eba03743db356ee45
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libusb-1.0/libusb-1.0_1.0.25.orig.tar.bz2' libusb-1.0_1.0.25.orig.tar.bz2 609127 SHA512:f1e6e5577d4bd1ff136927dc66c615014a06ac332ddd797b1d1ad5f7b68e2405e66068dcb210e2f0ae3e31681603ef72efbd88bf7fbe0eb41ce700fdc3f92f9d
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libusb-1.0/libusb-1.0_1.0.25-1ubuntu2.debian.tar.xz' libusb-1.0_1.0.25-1ubuntu2.debian.tar.xz 15544 SHA512:ab2c50ce52dfb5bc47265506db8c7bbffe9b88bfc7cb947b195d3b46e6203cadcbab5005cc168c178c3b3c6134b71b75a600dc967a1e2392fb2e55157e91b767
```

### `dpkg` source package: `libva=2.14.0-1`

Binary Packages:

- `libva-drm2:amd64=2.14.0-1`
- `libva-x11-2:amd64=2.14.0-1`
- `libva2:amd64=2.14.0-1`

Licenses: (parsed from: `/usr/share/doc/libva-drm2/copyright`, `/usr/share/doc/libva-x11-2/copyright`, `/usr/share/doc/libva2/copyright`)

- `Expat`
- `Expat-advertising`
- `GPL-2`
- `GPL-2+`
- `other`

Source:

```console
$ apt-get source -qq --print-uris libva=2.14.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/libv/libva/libva_2.14.0-1.dsc' libva_2.14.0-1.dsc 2404 SHA512:4256d53cc650007d1b00d330a9f303d32c7e23b1b1dd0d326bdaed3d229fa4709d1161cdce0fa2b7a8dce10bc2e256addec31223b0b5b94a9ebd1558ad5891de
'http://archive.ubuntu.com/ubuntu/pool/universe/libv/libva/libva_2.14.0.orig.tar.gz' libva_2.14.0.orig.tar.gz 266254 SHA512:8d87b49c7242174d05dca709bd79e6e45cea6e6060d12f5cf7636433be587c2b3a6c3183f632fb0ff49b19f31f915a2a62818c26f57c3a8f40741aa1ab8270b4
'http://archive.ubuntu.com/ubuntu/pool/universe/libv/libva/libva_2.14.0-1.debian.tar.xz' libva_2.14.0-1.debian.tar.xz 11924 SHA512:1a4f27fa6c1d58c76446bbb7aa3a23707917e293fc272798c91424ecfae7876e5d7492dccaf7149c0bb85af4cb9908fae16769876cebcd688c3807d6270fe7e8
```

### `dpkg` source package: `libvdpau=1.4-3build2`

Binary Packages:

- `libvdpau1:amd64=1.4-3build2`

Licenses: (parsed from: `/usr/share/doc/libvdpau1/copyright`)

- `Expat`
- `other`

Source:

```console
$ apt-get source -qq --print-uris libvdpau=1.4-3build2
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvdpau/libvdpau_1.4-3build2.dsc' libvdpau_1.4-3build2.dsc 2435 SHA512:4ac03fb6b24a93da9068f6e8cbcb71070486882c3ea0277dda964133c95cd286700f54e651aabcdc2840a8e9938b874b8db0e7fc5b38953a2ed94ec56a2270d9
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvdpau/libvdpau_1.4.orig.tar.bz2' libvdpau_1.4.orig.tar.bz2 139504 SHA512:68f502f53f4a95c9af571bd5a3f5048dd1afe30d7576f7e80751c7f29450ef8cb226c1281562b616079d6c177830ec67391d0fae33348a4627ca8c113990cd01
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvdpau/libvdpau_1.4-3build2.debian.tar.xz' libvdpau_1.4-3build2.debian.tar.xz 9920 SHA512:872ae13a15f0d0578aa00da2c282bcd73e5d95c90ecb664107dc77410742b7027936a8643e7240eee8181b1eea1b9f21bf31022a9b90fd4e94b2c643a29e85f0
```

### `dpkg` source package: `libvidstab=1.1.0-2`

Binary Packages:

- `libvidstab1.1:amd64=1.1.0-2`

Licenses: (parsed from: `/usr/share/doc/libvidstab1.1/copyright`)

- `GPL-2`
- `GPL-2.0+`

Source:

```console
$ apt-get source -qq --print-uris libvidstab=1.1.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/libv/libvidstab/libvidstab_1.1.0-2.dsc' libvidstab_1.1.0-2.dsc 1826 SHA512:3298a142cf210e3590895785f9f7cab7b9f70d1c4dcccf25646386b0684fc2becd6d1b7f9e215490cd44b134e5b05962b5385a3b990bcacaa71ee21e150b69cc
'http://archive.ubuntu.com/ubuntu/pool/universe/libv/libvidstab/libvidstab_1.1.0.orig.tar.gz' libvidstab_1.1.0.orig.tar.gz 77736 SHA512:e82a4b6dd854b8415952cc0a8bdea06c01ff40a497c8e98177831e29031ec535b9f47cc30d5444c47bfd91871615a1662e3991185e9eb179acf37ea601073cdf
'http://archive.ubuntu.com/ubuntu/pool/universe/libv/libvidstab/libvidstab_1.1.0-2.debian.tar.xz' libvidstab_1.1.0-2.debian.tar.xz 3876 SHA512:ae02b39ae46d2f553d7ba62af675680580ea25a30a433675e5437c73c62a0e10f3a3b24027870b455477e16fd9747cb0a6e4da2ed12d9134cfdaa0239d901a4b
```

### `dpkg` source package: `libvisio=0.1.7-1build5`

Binary Packages:

- `libvisio-0.1-1:amd64=0.1.7-1build5`

Licenses: (parsed from: `/usr/share/doc/libvisio-0.1-1/copyright`)

- `MIT | GPL-2`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libvisio=0.1.7-1build5
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvisio/libvisio_0.1.7-1build5.dsc' libvisio_0.1.7-1build5.dsc 2316 SHA512:8d94d414144fc3542c25a1344d48d36ade5b414811fdba61b6e6fa40e8cd52c24a1db7cd097b020f5092f881fc2ae2e8a4ecacc6939a005247d48355da4c859e
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvisio/libvisio_0.1.7.orig.tar.xz' libvisio_0.1.7.orig.tar.xz 854296 SHA512:c26f67a09fa6a6d0bf6f3fff5590d5cf16983630d4f7cfcf86d9461baec58dbdf7989fd934be6db0639ca043c160aac2d008275afb9e047766bc878ac579a9ea
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvisio/libvisio_0.1.7-1build5.debian.tar.xz' libvisio_0.1.7-1build5.debian.tar.xz 8356 SHA512:90bd1f37d34ce228d80e760535cabb167bf36c6c80588d09ce004af522eb8f7e1e9760da3c40ade6c8487ffb191e4f7bade94022441b8861f205430321d20d85
```

### `dpkg` source package: `libvorbis=1.3.7-1build2`

Binary Packages:

- `libvorbis0a:amd64=1.3.7-1build2`
- `libvorbisenc2:amd64=1.3.7-1build2`
- `libvorbisfile3:amd64=1.3.7-1build2`

Licenses: (parsed from: `/usr/share/doc/libvorbis0a/copyright`, `/usr/share/doc/libvorbisenc2/copyright`, `/usr/share/doc/libvorbisfile3/copyright`)

- `BSD-3-Clause`
- `RFC-special`

Source:

```console
$ apt-get source -qq --print-uris libvorbis=1.3.7-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvorbis/libvorbis_1.3.7-1build2.dsc' libvorbis_1.3.7-1build2.dsc 2494 SHA512:4d9ded87020c23a40c26f59bad3691375e2fa6777bce2c59312f3e6367d472456ce51ef2d65a3be7a8696eba1cf6b12bff5f41811197712ca379576c1ac121c4
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvorbis/libvorbis_1.3.7.orig.tar.gz' libvorbis_1.3.7.orig.tar.gz 1658963 SHA512:8a83ac9e9197f32fad4430946dba3927921320492f9e96cda546e8eb3981e2664da97f77e43cb197577ec056437785168ca7c4138f8bf7f2ba93899846932eb2
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvorbis/libvorbis_1.3.7-1build2.debian.tar.xz' libvorbis_1.3.7-1build2.debian.tar.xz 11748 SHA512:c9fa8e209f79edd59fc38cc586a3afca7d5d98829d6546193f22e046b0d040310f7b8d110ec2e3298ac554d174d9e4d7530ebcf93da5f20b3b3c6ce9279edbab
```

### `dpkg` source package: `libvpx=1.11.0-2ubuntu2.4`

Binary Packages:

- `libvpx7:amd64=1.11.0-2ubuntu2.4`

Licenses: (parsed from: `/usr/share/doc/libvpx7/copyright`)

- `BSD-3-Clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libvpx=1.11.0-2ubuntu2.4
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvpx/libvpx_1.11.0-2ubuntu2.4.dsc' libvpx_1.11.0-2ubuntu2.4.dsc 2401 SHA512:6c3d78ffaab61c65de5d18531b7dcc85244a869009b38772887c6d36f334d9f37b6f2e40d1791c27aa71ed44f9cef61cdf32398c9e689fdff340d1a27e6e6bc5
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvpx/libvpx_1.11.0.orig.tar.gz' libvpx_1.11.0.orig.tar.gz 5347256 SHA512:7aa5d30afa956dccda60917fd82f6f9992944ca893437c8cd53a04d1b7a94e0210431954aa136594dc400340123cc166dcc855753e493c8d929667f4c42b65a5
'http://archive.ubuntu.com/ubuntu/pool/main/libv/libvpx/libvpx_1.11.0-2ubuntu2.4.debian.tar.xz' libvpx_1.11.0-2ubuntu2.4.debian.tar.xz 18972 SHA512:64b22d0487d6d07d387c8d6a8717546903e329d31f7c44b9d8be45b75d0ca77264a44dd8c5dd0e7a5fa4686bfe538ee4d82a01415d0e91d0548a07d1f7b805fb
```

### `dpkg` source package: `libwebp=1.2.2-2ubuntu0.22.04.2`

Binary Packages:

- `libwebp7:amd64=1.2.2-2ubuntu0.22.04.2`
- `libwebpdemux2:amd64=1.2.2-2ubuntu0.22.04.2`
- `libwebpmux3:amd64=1.2.2-2ubuntu0.22.04.2`

Licenses: (parsed from: `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.2.2-2ubuntu0.22.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.2.2-2ubuntu0.22.04.2.dsc' libwebp_1.2.2-2ubuntu0.22.04.2.dsc 2186 SHA512:b81aa127277d4927b79d4ea5c8b63369f0b63e4944cc70bd98b277a1ae890169d91f4a0f30502830975bd2e34faa7a861b82d61f19ef660be1b7cf1d86010668
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.2.2.orig.tar.gz' libwebp_1.2.2.orig.tar.gz 4117468 SHA512:0dd0a721352b513a218d55383bcd0cc45b786df8089f70f87257b5dcc0c4e2f1798e20f1ca98b8fe51710abb667f9c4c14f20f980a11c484c8832f0dc66e3bff
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.2.2-2ubuntu0.22.04.2.debian.tar.xz' libwebp_1.2.2-2ubuntu0.22.04.2.debian.tar.xz 10468 SHA512:3c524505239652dbd3252aaaeee9161b0bb4c2ad146849341e87370760554de17d748d9b6f03c5e35db2d3f3dfedcf5e62b165502d207d2a114bda907483a830
```

### `dpkg` source package: `libwpd=0.10.3-2build1`

Binary Packages:

- `libwpd-0.10-10:amd64=0.10.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libwpd-0.10-10/copyright`)

- `LGPL`
- `MPL-2.0 | LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libwpd=0.10.3-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwpd/libwpd_0.10.3-2build1.dsc' libwpd_0.10.3-2build1.dsc 2181 SHA512:cc748f0663fa94718afb06d8af4c89115c25ece68674ca12d10612f59091bb8e774ee5f77214132160a938d5a8d9a975a53b67f8ee0d98f43b36c9b9c224fe2f
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwpd/libwpd_0.10.3.orig.tar.xz' libwpd_0.10.3.orig.tar.xz 534712 SHA512:df14f11e885a583218afdb0aafe8a15d01890289af8b316cd1d225e4a83996c82907fbfdde83257dc71d99bfbc5b21b2c96536f5a783748388659155dbdb8949
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwpd/libwpd_0.10.3-2build1.debian.tar.xz' libwpd_0.10.3-2build1.debian.tar.xz 11948 SHA512:153f27ff230d8a21988da6c8e18cae54bd6dd4045b670b5a829e8b2143e3f539dbb7c483ad1a042d2456205db1698980277934898dbca2ab2891a48584191908
```

### `dpkg` source package: `libwpg=0.3.3-1build3`

Binary Packages:

- `libwpg-0.3-3:amd64=0.3.3-1build3`

Licenses: (parsed from: `/usr/share/doc/libwpg-0.3-3/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libwpg=0.3.3-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwpg/libwpg_0.3.3-1build3.dsc' libwpg_0.3.3-1build3.dsc 2153 SHA512:512153168588578ed388f07c46232ac92b8e00967381f05e726d03ec10afe678b0be870921e06f7dcedac47e3e80e31c03e378880ee0fee620030244da5ecfcf
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwpg/libwpg_0.3.3.orig.tar.xz' libwpg_0.3.3.orig.tar.xz 328664 SHA512:99f8346b336eb902626fe07836c73870a57e100620ddd242ce7c2866e564483ed024a3a0b2804f81a0f59a0873310c3a93c005d306437a27818a6f4374c0c491
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwpg/libwpg_0.3.3-1build3.debian.tar.xz' libwpg_0.3.3-1build3.debian.tar.xz 9444 SHA512:8f81425d9a764a119d55e1b1e757926295f32a1273fcfaa5554d3c22006fbfad7ba2f8077e7801dd1e93e81f5577c2695c47a405311a712f63722aacec6205da
```

### `dpkg` source package: `libwps=0.4.12-2build1`

Binary Packages:

- `libwps-0.4-4:amd64=0.4.12-2build1`

Licenses: (parsed from: `/usr/share/doc/libwps-0.4-4/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris libwps=0.4.12-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwps/libwps_0.4.12-2build1.dsc' libwps_0.4.12-2build1.dsc 2348 SHA512:0feea0da91901c21ede04bef379768fe92fcff57b4fc59e50b6fa1de1ce704857e0c751f7124d80068b0e7be8e8e7f7538b53dc8db027c27495ab53fa99de064
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwps/libwps_0.4.12.orig.tar.xz' libwps_0.4.12.orig.tar.xz 713008 SHA512:d23667681f443b0c718b55006bee881e8a07d6b071cda742a783a89e9ed0e4c60c66c7dc9612a3fb4a419ff6d6e572f5981cec1d9470422e10cf9837e92a4649
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwps/libwps_0.4.12-2build1.debian.tar.xz' libwps_0.4.12-2build1.debian.tar.xz 9392 SHA512:c796cbeae746f527e70b1612dc4de93e3fdf8b20f8942ae65624f314bd55b8a17ecdc4c9552facc33d2fbc323a5e59c698873e1f724251879931d3ce035f9a7c
```

### `dpkg` source package: `libx11=2:1.7.5-1ubuntu0.3`

Binary Packages:

- `libx11-6:amd64=2:1.7.5-1ubuntu0.3`
- `libx11-data=2:1.7.5-1ubuntu0.3`
- `libx11-xcb1:amd64=2:1.7.5-1ubuntu0.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.7.5-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.7.5-1ubuntu0.3.dsc' libx11_1.7.5-1ubuntu0.3.dsc 2654 SHA512:97c9c7e8096cdb264d45a08f0333025ded9b74296689809d687de62b60b5d5ef7d2dc8b592b8155dbe12aa18129f97a12b978234b52ba2ed553568d207c62fce
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.7.5.orig.tar.gz' libx11_1.7.5.orig.tar.gz 3170022 SHA512:90474f5f95c3498a02100aeeb6b5ad7ae9076bc40a70cdd828bd881adac0bf278002186142f2760e5504cf82120f4869798831e0e2332ecbc6903e8f7c9114ab
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.7.5.orig.tar.gz.asc' libx11_1.7.5.orig.tar.gz.asc 358 SHA512:75139b9f7b2f19aed3d3a66ea8b883480db2fa56d713bb0160ea8a0faba208da4c241768f9f2703f723f13906438eda3117f489d7d5d17fbe1cbb75b13c9935d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.7.5-1ubuntu0.3.diff.gz' libx11_1.7.5-1ubuntu0.3.diff.gz 98716 SHA512:54531c960c2252c99e2f32f0d051eb1e764f181aaa68fc20a053384f70b14f32872e9ca05ed45affd2e97ea2821cdd8c3e3ebacf8c81c3088386a7d95214f64b
```

### `dpkg` source package: `libxau=1:1.0.9-1build5`

Binary Packages:

- `libxau6:amd64=1:1.0.9-1build5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-1build5
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build5.dsc' libxau_1.0.9-1build5.dsc 2315 SHA512:b9a9d6888a70e8c7e8161a322a425316ed181d00ad3881caea788aeda9c4346122a70c57d30b91e7692f5c0b468da9d784c228ead5487cfb2474f4fc42b83ada
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA512:3b22f34a4e35d17421189df8ce3f858b0914aef0cea0b12689dd8576f14eb811e39d6e32384251573daa7e3daba400deea98e7c0e29b4105138cf82195d7f875
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz.asc' libxau_1.0.9.orig.tar.gz.asc 801 SHA512:e59b2944591499d0c0291a8d80ad8ee2cb13ee00c32b0d26c6af12a2bb96c947d4d15924ef15b377b8d7640b75b50f9b8127ba53c582090b3f73b7bcf9e00b01
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build5.diff.gz' libxau_1.0.9-1build5.diff.gz 10579 SHA512:9485f97bc34a7b348a7bd276001ff5e455a17c8d6b6d6e4382496c38f470f1650f7177103d2b123f25f21ce62899ceb3112909ee92e9a604d302d3c63cb59e8f
```

### `dpkg` source package: `libxcb=1.14-3ubuntu3`

Binary Packages:

- `libxcb-dri2-0:amd64=1.14-3ubuntu3`
- `libxcb-dri3-0:amd64=1.14-3ubuntu3`
- `libxcb-glx0:amd64=1.14-3ubuntu3`
- `libxcb-present0:amd64=1.14-3ubuntu3`
- `libxcb-randr0:amd64=1.14-3ubuntu3`
- `libxcb-render0:amd64=1.14-3ubuntu3`
- `libxcb-shape0:amd64=1.14-3ubuntu3`
- `libxcb-shm0:amd64=1.14-3ubuntu3`
- `libxcb-sync1:amd64=1.14-3ubuntu3`
- `libxcb-xfixes0:amd64=1.14-3ubuntu3`
- `libxcb1:amd64=1.14-3ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.14-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.14-3ubuntu3.dsc' libxcb_1.14-3ubuntu3.dsc 5480 SHA512:cc563eae53e92b3f5cf700f0a61ee036fe0df9a109453dd4cd6a8107dac4a7f6d85e28810011ef74ca69ca36853a8d20e877480b94344ad5262f8fd6da299d5c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.14.orig.tar.gz' libxcb_1.14.orig.tar.gz 640322 SHA512:6114d8c233b42b56604787a0475e924143aa13f1d382e6029b2150a4360c12ce78073409f754fbb1e5d9f99fc26900c0a4c59e9cfbd4c3d0a3af0c1306e62da1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.14-3ubuntu3.diff.gz' libxcb_1.14-3ubuntu3.diff.gz 27588 SHA512:228c6da2cf94e02b249ccb04f2668f45b2ab117a4c6670ac6f7ab449582e459df4fc7e1ce5ae5cd945acea6fd00b935ed6394c800ee3d92ce9a0fb6913460f86
```

### `dpkg` source package: `libxcrypt=1:4.4.27-1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.27-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.27-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.27-1.dsc' libxcrypt_4.4.27-1.dsc 1525 SHA512:1335a2ab3f7b519022af13c18dca9ea1c2de3007c07f120d53fbb7eb834ac7e0ece120681c1ee1dd92771469104dccedef3a7e85ec51fc1ca64b52c9447558c0
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.27.orig.tar.xz' libxcrypt_4.4.27.orig.tar.xz 391772 SHA512:9d194066ab7eefd3e568b2478d58aa378da8571abf4c37ddcde2c01114a4aa69f0edfb4e3d13d951feac5955336f9b02046d9b1fd1b9fbfbc556aad31cf64d7e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.27-1.debian.tar.xz' libxcrypt_4.4.27-1.debian.tar.xz 7764 SHA512:02e38ba06f3555dd930fc7ed44602dc816ce48f4c29fdc085249948596d5e7e96600cb81c8c9fb2e1dc33574d5136d08feeff3eb1dd3522aa8e5cdc9037c1ae0
```

### `dpkg` source package: `libxcursor=1:1.2.0-2build4`

Binary Packages:

- `libxcursor1:amd64=1:1.2.0-2build4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcursor=1:1.2.0-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcursor/libxcursor_1.2.0-2build4.dsc' libxcursor_1.2.0-2build4.dsc 2392 SHA512:83ee6e8f9cd858bd7281682250789e13c9bff3cc4409c25bbdb0d8f616c3bc78c43017986afda1ec3853721c25b19649f75344033cc26c884b18b99bee93df39
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcursor/libxcursor_1.2.0.orig.tar.gz' libxcursor_1.2.0.orig.tar.gz 408135 SHA512:7a6638cb41be2db8141845efe5e0c701e4c67004264a04d9072e2f8ae98d466de199f3565bd14f9b7e6cfda83cfc1debaa16721985f51c00ccd69904b7074c83
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcursor/libxcursor_1.2.0-2build4.debian.tar.xz' libxcursor_1.2.0-2build4.debian.tar.xz 9232 SHA512:e83598e76d9a41e02bec74fe35b96db1ba0de3a3f0fe7a3afe0343cc28149a10a9d004dfe4c9fc5f9a21ada271991723f37c6d34e14b6bab2d0c436f54fde290
```

### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu5`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.3-0ubuntu5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.3-0ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu5.dsc' libxdmcp_1.1.3-0ubuntu5.dsc 2252 SHA512:5b6df4dd48380acff08dbe1fe40258d33a2f431e27da076ce54e0a1714dacb1e031aa49e2ace3863dc2131de4df42aa76b423f44f520fd8b2dbb18c4bddcada1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3.orig.tar.gz' libxdmcp_1.1.3.orig.tar.gz 429668 SHA512:edd05654ad9ea893e9e08269e25ea050d10eaf9f997a08494e24127d1ba0c896cd5338b4595b155c8cbf576e1d910b76e6ad7820fee62d74644f1f276551e2f2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu5.diff.gz' libxdmcp_1.1.3-0ubuntu5.diff.gz 18395 SHA512:552a04477a7852b2a68ba268dcd19cee9dd89c2774b6c86ca8f11180f6b179cc7853348653cf3b7d3e89a0079bef91308e8da2dfd34d0f42104f352e47ea07bd
```

### `dpkg` source package: `libxext=2:1.3.4-1build1`

Binary Packages:

- `libxext6:amd64=2:1.3.4-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build1.dsc' libxext_1.3.4-1build1.dsc 2250 SHA512:d7a857fa82374d6b0f1435f55c697f82f5f17e9492d74eea29e04679eb6a5dd49aeb88abb048e904de207c57d16d5ad487067e6fb45696834ac5c934040d7e90
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA512:4eebd639fd57cb9b84a1e17e368f82fbf3d9f021eef5ad3fe31dd128500db57862a82c1e0d214d447cb7641b2be3fd7e949ee1196f2a482793c6628fb1e5cd70
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build1.diff.gz' libxext_1.3.4-1build1.diff.gz 12588 SHA512:bfcebe8e6e277dc1ea81063a4a4663e24b78f2b69439e3b8ed2209168016876f55e8e95c6a1828ab5bf7a1936ec795e14f4391b24ec8801e0102e00e953d46e4
```

### `dpkg` source package: `libxfixes=1:6.0.0-1`

Binary Packages:

- `libxfixes3:amd64=1:6.0.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxfixes=1:6.0.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxfixes/libxfixes_6.0.0-1.dsc' libxfixes_6.0.0-1.dsc 2264 SHA512:2fec8bc79729c9f2a58a8db7705002671e33faeaa5a2dee764c3b4fef3ad536ba555545fd9593a0362d37cf838e8f723cc5fcb84bf49feeb456ee2e814245e8c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxfixes/libxfixes_6.0.0.orig.tar.gz' libxfixes_6.0.0.orig.tar.gz 387810 SHA512:422ff6aa6dddbb5d790ddf351b12556d37312d67b3adc8c276fb507b8278703b30841f81e526f119b9ab53a3bb8c7c5a742a43826287110ef5417dd84f01348a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxfixes/libxfixes_6.0.0.orig.tar.gz.asc' libxfixes_6.0.0.orig.tar.gz.asc 195 SHA512:3f00205ee9c67956d1e06ba5f8b0271d7015b31b6b21f782fcbeac25d9494ecee5303a3900abb72e2480c5a98abf3739aa30117c8384f568e1ea05b9dd020714
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxfixes/libxfixes_6.0.0-1.diff.gz' libxfixes_6.0.0-1.diff.gz 16999 SHA512:fc7c885d20d865f9c9aff81e7a7a8cf4189b7e05c6161d120e127109f7e8def8261713564fe5fb2468f45041fef25d5d55a696bce3470f1ae8595ef5d15abb5f
```

### `dpkg` source package: `libxi=2:1.8-1build1`

Binary Packages:

- `libxi6:amd64=2:1.8-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxi=2:1.8-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxi/libxi_1.8-1build1.dsc' libxi_1.8-1build1.dsc 2242 SHA512:43c30bba60a74e48d2ab240b5982ac305a6df6e3a4ac23902616ac103b3354c9171a3561bdd85b7c66ff75ad923b8b8604e6e46e75d81bc631e87f72562a81be
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxi/libxi_1.8.orig.tar.gz' libxi_1.8.orig.tar.gz 616977 SHA512:98b65084065cb28395cbd75213d7b52ac857840237d544714cf3cbddba6f940f93dd5846546365613da02fd5b4cd8c5be01ef2ac34b2503e500ea189e3c81005
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxi/libxi_1.8-1build1.diff.gz' libxi_1.8-1build1.diff.gz 24823 SHA512:ea75bc9b8ee93f4068cad75ff6cb3f7de5592a7f151241fb32dbbffd02aed7a89887df93c862c8de901e61ec7531aeb7ad5c3ff3ffc46d487fda89f98a9fec21
```

### `dpkg` source package: `libxinerama=2:1.1.4-3`

Binary Packages:

- `libxinerama1:amd64=2:1.1.4-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxinerama=2:1.1.4-3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxinerama/libxinerama_1.1.4-3.dsc' libxinerama_1.1.4-3.dsc 2088 SHA512:2c020448cf9f882be2c282c780d636ee814954f30b3874a770c570018bc9840791194debd28ae9e27a51bcdb6c8ef7917557a2f2f4cf6125e6dc4ff9860319ba
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxinerama/libxinerama_1.1.4.orig.tar.gz' libxinerama_1.1.4.orig.tar.gz 380740 SHA512:fa2cc45214cc591da8867dcd7e332312e8d224c390912dc8580f8b15c3c9d8ffc797eee97c20263faf129fbfc6b0d931b6bf10dc04b8ec439b852451886eba75
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxinerama/libxinerama_1.1.4-3.diff.gz' libxinerama_1.1.4-3.diff.gz 8436 SHA512:614e9deb0cee3578f57315bd06d27bd6df3f5e29b4aaaeaf677b75a136f53f1598451964a59261e430f5ec2dab3177fa9b27e3055801812fce29d2e32ce7ff22
```

### `dpkg` source package: `libxkbcommon=1.4.0-1`

Binary Packages:

- `libxkbcommon0:amd64=1.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxkbcommon=1.4.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxkbcommon/libxkbcommon_1.4.0-1.dsc' libxkbcommon_1.4.0-1.dsc 2734 SHA512:1ad8ab8c6ec3a03472d6b87201af7ea0269bc59ec98cb46ec971ed6602fa34978bc4d7f1dbc95470226d0bbd4f70f1889c393706dbea48a2bc1d0e66fc0e03c7
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxkbcommon/libxkbcommon_1.4.0.orig.tar.xz' libxkbcommon_1.4.0.orig.tar.xz 471948 SHA512:7dd86952c036a6a78455b1ba05b53fcff9d6f133bb01c83fa860b4eaec3fc26bb0b5535948bcc2dafbd27204c3c91d01404ca9fc52896cc36af509384797d4f1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxkbcommon/libxkbcommon_1.4.0-1.debian.tar.xz' libxkbcommon_1.4.0-1.debian.tar.xz 8028 SHA512:d49087f93cd0cdbd56a7756a9895f97eaffdbf5aba8dfb65896337890cf732818373cb5cccee1dcbe99e119b5eff32380f3840c2f3ee2bcaec064632cd26c0a2
```

### `dpkg` source package: `libxml2=2.9.13+dfsg-1ubuntu0.10`

Binary Packages:

- `libxml2:amd64=2.9.13+dfsg-1ubuntu0.10`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.13+dfsg-1ubuntu0.10
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.13%2bdfsg-1ubuntu0.10.dsc' libxml2_2.9.13+dfsg-1ubuntu0.10.dsc 3034 SHA512:0a7b2308e1e21ce144787a2fde4f6bd2356fd433701707ed622b6dedf284a3b6ac2c9acab4f1044354100688685116cb7e6d170b18a14a59e116ab5b9d0edd81
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.13%2bdfsg.orig.tar.xz' libxml2_2.9.13+dfsg.orig.tar.xz 2351356 SHA512:6283071de4934c856c7ff5202ac1a2ed5892d7fcde82a364d40c8bc2bf3d3201fbcbb5f6983d8bf6b962026bc216b8182d71efe280f1dcef2931b277314e6e89
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.13%2bdfsg-1ubuntu0.10.debian.tar.xz' libxml2_2.9.13+dfsg-1ubuntu0.10.debian.tar.xz 49928 SHA512:25a132aaa4a0107d6f554d5882c52316d9236ea30ab1cccdfc6d7e5cbf2eacdfaafe14c46e26ef77e8274e408ff766c19041060e1ac3607b3f5c8fb771099a07
```

### `dpkg` source package: `libxrandr=2:1.5.2-1build1`

Binary Packages:

- `libxrandr2:amd64=2:1.5.2-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrandr=2:1.5.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrandr/libxrandr_1.5.2-1build1.dsc' libxrandr_1.5.2-1build1.dsc 2148 SHA512:6ff4378e649324dd71e77bcefa6943c24e00ec5338bb11d3bb1f3cb76fb19311ee66498d7a0d33855fab0f72e82fbab4a53109a0ccf246d537fa220111145d7f
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrandr/libxrandr_1.5.2.orig.tar.gz' libxrandr_1.5.2.orig.tar.gz 411714 SHA512:309df91127ae17d8bb5a4382b22d1cf788733775dfddcb7932b3edb6f4121728daa7bba1e95ee5e250b2f8b03907a2564dcb3d645d7a5ef6314d0d7b09bac75d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrandr/libxrandr_1.5.2-1build1.diff.gz' libxrandr_1.5.2-1build1.diff.gz 17189 SHA512:d832be368bd3efc077acc1353f05c2c09aa5f3df6855a49e128c9eeb4a1a3f1f88559cfa9d1add772a30975eb07339e6b3165a8bdd4998c1dbfe3202c597c2b8
```

### `dpkg` source package: `libxrender=1:0.9.10-1build4`

Binary Packages:

- `libxrender1:amd64=1:0.9.10-1build4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1build4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1build4.dsc' libxrender_0.9.10-1build4.dsc 2196 SHA512:4e5f32bd1ea1a7c78bd3f186fff28ead08e814f25029e6d955b323998c1a64ee53e6862b89aa73a9d2f84207cef9da28127bc2a40ce74f55cff37b198979b76d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA512:7768e62b500f468460f88f27bc1130170b204b478573d9e4406867e557b5638b7c1e21d88d51f9e774ce2344780a384e3c3be51421275d2ee880f9a978a3a232
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1build4.diff.gz' libxrender_0.9.10-1build4.diff.gz 15809 SHA512:8c0fe7e340497564286087bc95c6fac4ac9130723bc7389dfc88cf4172dc77ae657e8bcb8c6a99ff53ee8aca1072ad5279e4b7588499209851059948eb2869a0
```

### `dpkg` source package: `libxshmfence=1.3-1build4`

Binary Packages:

- `libxshmfence1:amd64=1.3-1build4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxshmfence=1.3-1build4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxshmfence/libxshmfence_1.3-1build4.dsc' libxshmfence_1.3-1build4.dsc 2228 SHA512:5fcc75d7ae2e9349eed698a7b1da475280edc0e5037951b67fe57f21b0373bafd036d26169158836ddd90f3d2e6afa5a7e3b4c17446acdee21a38ce23cc3591c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxshmfence/libxshmfence_1.3.orig.tar.gz' libxshmfence_1.3.orig.tar.gz 378960 SHA512:2303924c907f920462e773c82052b03e6c2cc7762b6e2ae4fa25bf9ccd7e0fd979f22f0448ba79a90d03491d311a59fa93a2b7c49590cd14b441fb4508c8e730
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxshmfence/libxshmfence_1.3-1build4.diff.gz' libxshmfence_1.3-1build4.diff.gz 17897 SHA512:a0ba8f59d00f3ecfea17bab46cffc54786c000f0561378a4028bf5d286de31867ac90c5f529306635c505b038d47d63b5d6827026a11f25a94fcb78c914f6d68
```

### `dpkg` source package: `libxslt=1.1.34-4ubuntu0.22.04.4`

Binary Packages:

- `libxslt1.1:amd64=1.1.34-4ubuntu0.22.04.4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.34-4ubuntu0.22.04.4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34-4ubuntu0.22.04.4.dsc' libxslt_1.1.34-4ubuntu0.22.04.4.dsc 2514 SHA512:5f50ed44bbffc36ce0fbc26a66312002ba9f71220efaf24d4238722447605501650b5845f5054e37779708bef66a377baaad73bb8668ae1cfedf8c835546bc41
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34.orig.tar.gz' libxslt_1.1.34.orig.tar.gz 3552258 SHA512:1516a11ad608b04740674060d2c5d733b88889de5e413b9a4e8bf8d1a90d712149df6d2b1345b615f529d7c7d3fa6dae12e544da828b39c7d415e54c0ee0776b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34.orig.tar.gz.asc' libxslt_1.1.34.orig.tar.gz.asc 488 SHA512:9b155d4571daede99cdbf2813a85fb04812737b5e23d3f7c9840225b38f3dbf171623a21645daaee190e7ff9ba38bde932922e96a2a2312c203ffa9917c3baea
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34-4ubuntu0.22.04.4.debian.tar.xz' libxslt_1.1.34-4ubuntu0.22.04.4.debian.tar.xz 31084 SHA512:97474d3f98e4158873b5c1b9bad99d85ae381d29a90bc591d1047ce7a3c62219d56a5fc09d3573c554a79c3048f26f7548bb1489d8d6c61e74d7d3bac4487983
```

### `dpkg` source package: `libxss=1:1.2.3-1build2`

Binary Packages:

- `libxss1:amd64=1:1.2.3-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxss=1:1.2.3-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxss/libxss_1.2.3-1build2.dsc' libxss_1.2.3-1build2.dsc 2335 SHA512:373a3a74c44be2758bd2c313f10e93514ac8d4a63918318073772b7b96b0c89901d06c048c9b975042971f89d95ac94abae2118efe912542800f26a5c53153f3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz' libxss_1.2.3.orig.tar.gz 385215 SHA512:8f0d1d460027acfd50a312bf3b10407959d5ccbd9e76b319563535ba9038e1195cf0493664f80fd86e61ed037593d43e7b9a4f8f5d1f0c719d42935bf74ad68f
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz.asc' libxss_1.2.3.orig.tar.gz.asc 705 SHA512:678529385a502d93119ea4b3d4a94a19b79ee1b41e54c9526277cfa20e47bef04bb007fa089edcc9722f748dd27b7f58db5c732fe94c09112cec74425dbcc5d9
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxss/libxss_1.2.3-1build2.diff.gz' libxss_1.2.3-1build2.diff.gz 7348 SHA512:88a947717b203870b8dad3751bc993fa652319181046d7d99801678c55206c384b09828bb851008fd210c3a62437209d341f57fe21174cb593e5a3584f8c21b9
```

### `dpkg` source package: `libxtst=2:1.2.3-1build4`

Binary Packages:

- `libxtst6:amd64=2:1.2.3-1build4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxtst=2:1.2.3-1build4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxtst/libxtst_1.2.3-1build4.dsc' libxtst_1.2.3-1build4.dsc 2375 SHA512:68c25cb4f05b2668bed5181b7065508fdf89e83c3f4d57cd3307c295cc301c4cd9e4787f13c97758e9bfcfeb4c30b83396c01d725fc68b917ba094f22b51bde1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxtst/libxtst_1.2.3.orig.tar.gz' libxtst_1.2.3.orig.tar.gz 400197 SHA512:a6ab344984bb24ae6a82050c3f5ae4ee3daac4f027a9564a52591b9acfe84e4d8be3dd1a8c5e5a0715bed16dc8f2ab43cf62b5a6b39407072ba18d707b680ce9
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxtst/libxtst_1.2.3-1build4.diff.gz' libxtst_1.2.3-1build4.diff.gz 10352 SHA512:58006963636cb070d80416ea2255f4cafd7f11c6577c8dc89260dbe07cacdeeacb36cfaf22a83d901752add35e1e1e4a11294b96cb476ed96692149535760bf3
```

### `dpkg` source package: `libxv=2:1.0.11-1build2`

Binary Packages:

- `libxv1:amd64=2:1.0.11-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxv=2:1.0.11-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxv/libxv_1.0.11-1build2.dsc' libxv_1.0.11-1build2.dsc 2091 SHA512:b63598e3795fcf4f644e5770d14e6c70c0f9a7ac6fb77be67aa084e59a4f56326165fdfc8c4f477f8a47816db3856d327d06b27a5645d75a0ffeb03a2091e8df
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxv/libxv_1.0.11.orig.tar.gz' libxv_1.0.11.orig.tar.gz 387057 SHA512:2e755324afd5d153aa2439b8570d4e97f11eaa75412e85b078d4c525aa73f189e0ee7ff865e1cf28de671545a72a95679e7ba09073d95d4c0792ed38f9f5375f
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxv/libxv_1.0.11-1build2.diff.gz' libxv_1.0.11-1build2.diff.gz 8537 SHA512:b7854d67a0e3f004f94bc32bcacd3ab290a512fcf1e02cc9f3b73425eed415aaeeedafd412316cdf0406160477089b8a8579748eca1bd812703b975eddcf88de
```

### `dpkg` source package: `libxxf86vm=1:1.1.4-1build3`

Binary Packages:

- `libxxf86vm1:amd64=1:1.1.4-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxxf86vm=1:1.1.4-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxxf86vm/libxxf86vm_1.1.4-1build3.dsc' libxxf86vm_1.1.4-1build3.dsc 2224 SHA512:3dbc258a766eca26c75e2aa21a7b6f66966f00b810c2a595b63413f26d52b7a862615c5cf57a52ae72476a4834106491b942b6cecb5ab15154b6c81ef6d75642
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxxf86vm/libxxf86vm_1.1.4.orig.tar.gz' libxxf86vm_1.1.4.orig.tar.gz 363146 SHA512:ba9335b45c1466508c6fc8eefaf5785d47b21e10742775c15eb5166d99350fb5827a4b7c8a2fa41248d1f71a69fc321bc3527b2c0658854e21279c7428f30611
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxxf86vm/libxxf86vm_1.1.4-1build3.diff.gz' libxxf86vm_1.1.4-1build3.diff.gz 8418 SHA512:e157bbc7975541dcd114b7af28e6674cdd63ce8f97964acdb165f447079f587fd512b3d36f0316cd072f6380200b995287b1957e8bbd2bc8a436fd52341a9ebb
```

### `dpkg` source package: `libzstd=1.4.8+dfsg-3build1`

Binary Packages:

- `libzstd1:amd64=1.4.8+dfsg-3build1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.4.8+dfsg-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.4.8%2bdfsg-3build1.dsc' libzstd_1.4.8+dfsg-3build1.dsc 2398 SHA512:cdd444b0258f1effd998781dd058c8ab37fb8aabb10b94cc5741b0fd2c4c948085cd1b919533ded2f30c5a871c68a81dacef3c3d0640b8514d5d3a9d375647f6
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.4.8%2bdfsg.orig.tar.xz' libzstd_1.4.8+dfsg.orig.tar.xz 1331996 SHA512:07fabe431367eea4badae7b1e46ac73e0b33aad5b67361bc7b67d5f9aef249c51db5b560f1cf59233255cc49db341a8d8440fed87745026fca7a7c5c14448cd8
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.4.8%2bdfsg-3build1.debian.tar.xz' libzstd_1.4.8+dfsg-3build1.debian.tar.xz 12316 SHA512:8123965a6e73c5ddd8d535e78ed1074e2eabd7f8ed090d215a89feedffae9391cf472d2395242d3cb0351cbf76603448dae93ad70d0989806b42b03c65b22db0
```

### `dpkg` source package: `lilv=0.24.12-2`

Binary Packages:

- `liblilv-0-0:amd64=0.24.12-2`

Licenses: (parsed from: `/usr/share/doc/liblilv-0-0/copyright`)

- `BSD-3-clause`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris lilv=0.24.12-2
'http://archive.ubuntu.com/ubuntu/pool/universe/l/lilv/lilv_0.24.12-2.dsc' lilv_0.24.12-2.dsc 2530 SHA512:556de44e109efc4ca00a886ec3cadab807a1c1ce60eaaed017cbab15575b014b905f5407443bcac7a67cd0408d94f1244db8ad2371c2b03f1a7d9f3ffa7d6488
'http://archive.ubuntu.com/ubuntu/pool/universe/l/lilv/lilv_0.24.12.orig.tar.bz2' lilv_0.24.12.orig.tar.bz2 427404 SHA512:ea22db4e995792b62d60d793169c792549b8fb0255c2cf7a85780dd149811921e2fae5eaea0fb83465f01b14dfa66361af3be40bf7cb3733e98655b943f4faee
'http://archive.ubuntu.com/ubuntu/pool/universe/l/lilv/lilv_0.24.12.orig.tar.bz2.asc' lilv_0.24.12.orig.tar.bz2.asc 833 SHA512:11fbd209376d772eb7ef33a6fb65b471bf428e2d5712fecd47da51f3b6736b92b62245483d6f46cf4beee86150d5b77142f600de6bf95d2fd0663f38abfcadeb
'http://archive.ubuntu.com/ubuntu/pool/universe/l/lilv/lilv_0.24.12-2.debian.tar.xz' lilv_0.24.12-2.debian.tar.xz 13128 SHA512:f1e76e512a8eb318dbfa12f18b55863b4e6c7e2e1ae03a7bf7fb7e1ba39bd01a7c18e2b87d0e9678f3af257b568d98cfe11f58b2b68b2a4fd801f4e9d9453869
```

### `dpkg` source package: `llvm-toolchain-15=1:15.0.7-0ubuntu0.22.04.3`

Binary Packages:

- `libllvm15:amd64=1:15.0.7-0ubuntu0.22.04.3`

Licenses: (parsed from: `/usr/share/doc/libllvm15/copyright`)

- `APACHE-2-LLVM-EXCEPTIONS`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-clause`
- `MIT`
- `Python`
- `solar-public-domain`

Source:

```console
$ apt-get source -qq --print-uris llvm-toolchain-15=1:15.0.7-0ubuntu0.22.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/l/llvm-toolchain-15/llvm-toolchain-15_15.0.7-0ubuntu0.22.04.3.dsc' llvm-toolchain-15_15.0.7-0ubuntu0.22.04.3.dsc 7322 SHA512:a0012dd718a164ac489dfe1d059a1cded384c0b7cc172b2f0048e38dceedbe1fd8833fc366b5cf72570a63d12d304d15117ceee4f92ade1c21d35b1ea2c75208
'http://archive.ubuntu.com/ubuntu/pool/main/l/llvm-toolchain-15/llvm-toolchain-15_15.0.7.orig.tar.xz' llvm-toolchain-15_15.0.7.orig.tar.xz 138500556 SHA512:d4e2c3be6bb5f6f780b07839c5398d0d976f392b64b18288578e77f01ec8f4f7bee28ff71250d0fe740b07bc1f47a2178f6b1371e4ba13a76cd7b3e393db9b6e
'http://archive.ubuntu.com/ubuntu/pool/main/l/llvm-toolchain-15/llvm-toolchain-15_15.0.7-0ubuntu0.22.04.3.debian.tar.xz' llvm-toolchain-15_15.0.7-0ubuntu0.22.04.3.debian.tar.xz 166524 SHA512:a13f07064b8a1d608a63b4dc5049ec8216f195273c502609d3b8c0ce3e61c3d873a84cbdcb7460661334e7d5823b614449ec9c91674a5f4c87ba114a37281146
```

### `dpkg` source package: `lm-sensors=1:3.6.0-7ubuntu1`

Binary Packages:

- `libsensors-config=1:3.6.0-7ubuntu1`
- `libsensors5:amd64=1:3.6.0-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libsensors-config/copyright`, `/usr/share/doc/libsensors5/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris lm-sensors=1:3.6.0-7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lm-sensors/lm-sensors_3.6.0-7ubuntu1.dsc' lm-sensors_3.6.0-7ubuntu1.dsc 2174 SHA512:98941ecb3fbe53980337c19da0548aebf2a1b705faa23ab7a9b3e4c2c1bcd449fbb8f4cb97fb51d67d63430a52fea78db19351ded44157680457b1b9d4793d71
'http://archive.ubuntu.com/ubuntu/pool/main/l/lm-sensors/lm-sensors_3.6.0.orig.tar.gz' lm-sensors_3.6.0.orig.tar.gz 273209 SHA512:4e80361913aff5403f1f0737fd4f42cffe43cc170ef48fff3914c9952f71990739d723f7b0b8120d9a01bcbbc829e964cfbd0a5cf18508af8f8dc825b49860bf
'http://archive.ubuntu.com/ubuntu/pool/main/l/lm-sensors/lm-sensors_3.6.0-7ubuntu1.debian.tar.xz' lm-sensors_3.6.0-7ubuntu1.debian.tar.xz 26368 SHA512:b9a64c91755dd1266fa7edb6d743987ffc2fb26f728bd90fa2934f0f8f34cdee381c0df37d6c4447169c732e33dd81ff1ab3ed37ee2971975bebfc2677853c9b
```

### `dpkg` source package: `lp-solve=5.5.2.5-2build2`

Binary Packages:

- `lp-solve=5.5.2.5-2build2`

Licenses: (parsed from: `/usr/share/doc/lp-solve/copyright`)

- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris lp-solve=5.5.2.5-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lp-solve/lp-solve_5.5.2.5-2build2.dsc' lp-solve_5.5.2.5-2build2.dsc 2375 SHA512:f3783ab13fa7daad5474eb74540593d4eea785d49634fe3a22f3c3e389be6fddaa17ab14879d9f9898f642ffe09237edb4abf56e46df210048a0ff9f39bccea5
'http://archive.ubuntu.com/ubuntu/pool/main/l/lp-solve/lp-solve_5.5.2.5.orig-doc.tar.gz' lp-solve_5.5.2.5.orig-doc.tar.gz 1448749 SHA512:69273635261cea22d8234462a30ef5b958d1464378e35d73fc8225dbc3b80140c9321f01610db5caffbc54884f9e4e33ac7be265d17f4a41a9960ed03a236140
'http://archive.ubuntu.com/ubuntu/pool/main/l/lp-solve/lp-solve_5.5.2.5.orig.tar.gz' lp-solve_5.5.2.5.orig.tar.gz 812947 SHA512:6ae78b01bf50990b8141dfe3c1994bb9e7632db6a200c7900ac44de592b3ac1e21063f7b4554d4960af01538d89e937fc25da14f67156d12464e8cfdf0f86c46
'http://archive.ubuntu.com/ubuntu/pool/main/l/lp-solve/lp-solve_5.5.2.5-2build2.debian.tar.xz' lp-solve_5.5.2.5-2build2.debian.tar.xz 16532 SHA512:08200938b9ecb3ed626005c3401186a32400c17dbb16116f032f7a00ada3ff4668887c92a67b4f7b885522360487faae3c2fda09a2d297001049612ed4483bf0
```

### `dpkg` source package: `lsb=11.1.0ubuntu4`

Binary Packages:

- `lsb-base=11.1.0ubuntu4`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`)

- `BSD-3-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris lsb=11.1.0ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lsb/lsb_11.1.0ubuntu4.dsc' lsb_11.1.0ubuntu4.dsc 2222 SHA512:2b5375ca5938f497f9211d9b85eaf60858c2d59c80ec40a3a04bec6ef47e6685661589f22514f8b2e4a325038feb0375d99e1f905aa93b4a13c3d474e3b86677
'http://archive.ubuntu.com/ubuntu/pool/main/l/lsb/lsb_11.1.0ubuntu4.tar.xz' lsb_11.1.0ubuntu4.tar.xz 46152 SHA512:03469c3b85facd88fb4c24b85eb42d6aeab171aa6e5860147ad947e2bbc2f2fe5f78ebd4a457f6af194d33173dccec4f672d1b9d460c070765377d9456bc73da
```

### `dpkg` source package: `lz4=1.9.3-2build2`

Binary Packages:

- `liblz4-1:amd64=1.9.3-2build2`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.3-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.3-2build2.dsc' lz4_1.9.3-2build2.dsc 2091 SHA512:a8f802737139536f8a9c0a3483635ff4dd8a3eba2e0d9d0d27f4f91c17592d1797929d491183dc25de4100a7aa924edefa8ca45eed4968c0e1b7e817f1ae9e1c
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.3.orig.tar.gz' lz4_1.9.3.orig.tar.gz 320958 SHA512:c246b0bda881ee9399fa1be490fa39f43b291bb1d9db72dba8a85db1a50aad416a97e9b300eee3d2a4203c2bd88bda2762e81bc229c3aa409ad217eb306a454c
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.3-2build2.debian.tar.xz' lz4_1.9.3-2build2.debian.tar.xz 14088 SHA512:9f61516a672186299a96aee5b7a71d9cb1ad3db2697fa10b802fef14a63587bb3459281f7300726711a116893c10858914f558aece1d224876e287020a23dde6
```

### `dpkg` source package: `mawk=1.3.4.20200120-3`

Binary Packages:

- `mawk=1.3.4.20200120-3`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20200120-3
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20200120-3.dsc' mawk_1.3.4.20200120-3.dsc 1915 SHA512:f51dae1f342769e4fc0b8d5faf4e988433a0e74912ba0777fbafdf058900c973087c267756f5c2b74298bfc31a36c8bbc99c6c0edcc850710b646d0d24fa1305
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20200120.orig.tar.gz' mawk_1.3.4.20200120.orig.tar.gz 468855 SHA512:14d9a6642ce931bf6457d248fc2d6da4f0ea7541976ca282ea708b26df048f86fdf92c27f72d497501ccd43a244d1d1a606f1a2f266a7558306fea35dcc3041b
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20200120-3.debian.tar.xz' mawk_1.3.4.20200120-3.debian.tar.xz 7520 SHA512:bc4f5401de313108595ba91b17f44b5c67d7650b5557eef8a6c63c75e2ccee5dfd8900576d7e81f0ab1ac2e570f64fa75f38f56f6d4535437c803029216501af
```

### `dpkg` source package: `media-types=7.0.0`

Binary Packages:

- `media-types=7.0.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=7.0.0
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_7.0.0.dsc' media-types_7.0.0.dsc 1620 SHA512:f5159688820b267f4349dce11a3427bb70d8185494386ec37076885c36c4dfda8de9daf82a92cd84442604b33dfb7835ae2121bead8151ae5e14ed375a9d9659
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_7.0.0.tar.xz' media-types_7.0.0.tar.xz 55660 SHA512:ce4b07388c490c7e3e1bdd1dcdd28c685eee81cb9d167cc903f427a28bf972210b8d5ad3d33af06530b4dba0ac7f2a2b6e914c1d88bc1e88db589de6b4490071
```

### `dpkg` source package: `mesa=23.2.1-1ubuntu3.1~22.04.3`

Binary Packages:

- `libgbm1:amd64=23.2.1-1ubuntu3.1~22.04.3`
- `libgl1-mesa-dri:amd64=23.2.1-1ubuntu3.1~22.04.3`
- `libglapi-mesa:amd64=23.2.1-1ubuntu3.1~22.04.3`
- `libglx-mesa0:amd64=23.2.1-1ubuntu3.1~22.04.3`

Licenses: (parsed from: `/usr/share/doc/libgbm1/copyright`, `/usr/share/doc/libgl1-mesa-dri/copyright`, `/usr/share/doc/libglapi-mesa/copyright`, `/usr/share/doc/libglx-mesa0/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris mesa=23.2.1-1ubuntu3.1~22.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/m/mesa/mesa_23.2.1-1ubuntu3.1%7e22.04.3.dsc' mesa_23.2.1-1ubuntu3.1~22.04.3.dsc 5839 SHA512:1f0095212bb7af4fd887815522b220719c9a2dd5c1f75fc75c9ff0e1bb3df7e77e61bb2cccd16efb75704803984434e32cbced7d32e94179567413bbf5f1c8bd
'http://archive.ubuntu.com/ubuntu/pool/main/m/mesa/mesa_23.2.1.orig.tar.gz' mesa_23.2.1.orig.tar.gz 30631591 SHA512:9836624a9731fb5046ef7a08357f8e0c342fbc88b2911e65cdb0f99064991a913c9b976325945b30169d554f9cc879e931dff34da357cd27330e4460eda58e9a
'http://archive.ubuntu.com/ubuntu/pool/main/m/mesa/mesa_23.2.1-1ubuntu3.1%7e22.04.3.diff.gz' mesa_23.2.1-1ubuntu3.1~22.04.3.diff.gz 225765 SHA512:4b89ffe84a52b3952a730ba2bbe7225cebe36d75ba08489eb4c4bb5647b432ed1d6572da1699fdc5f3a8afb5251f2cf56b1840b91973c65b65197f910a4613df
```

### `dpkg` source package: `mhash=0.9.9.9-9build2`

Binary Packages:

- `libmhash2:amd64=0.9.9.9-9build2`

Licenses: (parsed from: `/usr/share/doc/libmhash2/copyright`)

- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris mhash=0.9.9.9-9build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mhash/mhash_0.9.9.9-9build2.dsc' mhash_0.9.9.9-9build2.dsc 2015 SHA512:9076f1e0dc1624f914c19cb1bdb3939970ba71e1ce83e93019ca97441e3ac5330ad406ea86ff5e857c9dd440fcaf017e8c88b0d2aec16f276cb83029c82c1f25
'http://archive.ubuntu.com/ubuntu/pool/main/m/mhash/mhash_0.9.9.9.orig.tar.gz' mhash_0.9.9.9.orig.tar.gz 577533 SHA512:8e979568d44476801049e82f178297059bca80f89fec008217a0c50a14ec6ba64dba297c5c5956e24849a5d434d02cea5d809fc8ba02455a63c5d2905e3e5324
'http://archive.ubuntu.com/ubuntu/pool/main/m/mhash/mhash_0.9.9.9-9build2.debian.tar.xz' mhash_0.9.9.9-9build2.debian.tar.xz 13040 SHA512:17670f387a5bea655a8c1a041912d616d8387af79046da3ba98150e643072e9074c0c9ffeeddbf8ae815c1f1ae9221e2764205f6171a5549e3a5d97ddaf94c69
```

### `dpkg` source package: `mpdecimal=2.5.1-2build2`

Binary Packages:

- `libmpdec3:amd64=2.5.1-2build2`

Licenses: (parsed from: `/usr/share/doc/libmpdec3/copyright`)

- `BSD`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mpdecimal=2.5.1-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpdecimal/mpdecimal_2.5.1-2build2.dsc' mpdecimal_2.5.1-2build2.dsc 2026 SHA512:2f930154a94b9b4090f18e848ea94d115304827e351abc9141ef8646b9937a0f93eb2517790b661b0569e22bb498497c03972233e1ace6bdd85c9fc6922e7e70
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpdecimal/mpdecimal_2.5.1.orig.tar.gz' mpdecimal_2.5.1.orig.tar.gz 2584021 SHA512:710cb5cb71dbcf3e170ca15869c148df0547b848400c6b6dd70c67d9961dbe1190af8fb4d1623bfb0ca2afe44f369a42e311ab5225ed89d4031cb49a3bd70f30
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpdecimal/mpdecimal_2.5.1-2build2.debian.tar.xz' mpdecimal_2.5.1-2build2.debian.tar.xz 6860 SHA512:261ab28a609fbcff2b9561f1b1e484500c5652e48bd0abc4f8c5df73b7e00333b80f1fe416c84800690d13d52d2af72d97503dcd0afa61073ee5610d62a52a02
```

### `dpkg` source package: `mpg123=1.29.3-1ubuntu0.1`

Binary Packages:

- `libmpg123-0:amd64=1.29.3-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libmpg123-0/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris mpg123=1.29.3-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpg123/mpg123_1.29.3-1ubuntu0.1.dsc' mpg123_1.29.3-1ubuntu0.1.dsc 2717 SHA512:8b85bcdc1f97400f12501dbe6cfc105f666debcafc04b5189b51df9b4fb14acaf741d03f832681080e4670040bc3242d82d5763ff98be1ecf453d2dcf22f49a5
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpg123/mpg123_1.29.3.orig.tar.bz2' mpg123_1.29.3.orig.tar.bz2 1069979 SHA512:0d8db63f9bae1507887bc5241a56abccfeb767b7ba8362eb0fce9de2f63369e57fdd6f25a953f8ef5f9ead4f400237db51914816e278566fdf8e6f205ebca5d6
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpg123/mpg123_1.29.3.orig.tar.bz2.asc' mpg123_1.29.3.orig.tar.bz2.asc 833 SHA512:cc258dca5fac129eaf93339934118d3da7c6bfefd4637c9478cea4cd004a412848afc15f70628936ba8687df35af8c89fb87fa095164ed7d5d92ca10e04cdc28
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpg123/mpg123_1.29.3-1ubuntu0.1.debian.tar.xz' mpg123_1.29.3-1ubuntu0.1.debian.tar.xz 33676 SHA512:d0e1b68842bc44fe0ad2758289e62cbc3d5dca8eb10366bb6187141976af4d336bde003f165fa8cc46d56cbcbd4eb178c16be8e82df65c61e838893330dfca58
```

### `dpkg` source package: `mythes=2:1.2.4-4build1`

Binary Packages:

- `libmythes-1.2-0:amd64=2:1.2.4-4build1`

Licenses: (parsed from: `/usr/share/doc/libmythes-1.2-0/copyright`)

- `BSD-3-clause`
- `custom`

Source:

```console
$ apt-get source -qq --print-uris mythes=2:1.2.4-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mythes/mythes_1.2.4-4build1.dsc' mythes_1.2.4-4build1.dsc 2099 SHA512:fcbdd57abb66c19dc1e2e2a420159c0a79523408ee26e6449c0f8a15c2431ccc0049355d5847d6910d6c3a11526bf0a4991600c9235042cdde6b221f67c28733
'http://archive.ubuntu.com/ubuntu/pool/main/m/mythes/mythes_1.2.4.orig.tar.gz' mythes_1.2.4.orig.tar.gz 4910303 SHA512:a04da39812bcfb1391a2cba7de73e955eafe141679ec03ed6657d03bebf360b432480d0037dff9ed72a1dfda5a70d77d44ac2bb14cdb109fd8e2a38376feee21
'http://archive.ubuntu.com/ubuntu/pool/main/m/mythes/mythes_1.2.4-4build1.debian.tar.xz' mythes_1.2.4-4build1.debian.tar.xz 5284 SHA512:8f1d8871035ef5338fd489fdf49bad77cea70b3b8680887433c8b59867f33d6a804fc6702630d19bb741f7436751d5f7552d13eff59d8b5b68825a316ec61dd8
```

### `dpkg` source package: `ncurses=6.3-2ubuntu0.1`

Binary Packages:

- `libncurses6:amd64=6.3-2ubuntu0.1`
- `libncursesw6:amd64=6.3-2ubuntu0.1`
- `libtinfo6:amd64=6.3-2ubuntu0.1`
- `ncurses-base=6.3-2ubuntu0.1`
- `ncurses-bin=6.3-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.3-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3-2ubuntu0.1.dsc' ncurses_6.3-2ubuntu0.1.dsc 3955 SHA512:e018fe9a8a641efddfcac0e92ce46dbba3067ddc6850e7223b3abc668f1620c1ea1564d80a63b94ff1c37705630eb2116d5c4449f1115315def4d4008e5f5926
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3.orig.tar.gz' ncurses_6.3.orig.tar.gz 3583550 SHA512:5373f228cba6b7869210384a607a2d7faecfcbfef6dbfcd7c513f4e84fbd8bcad53ac7db2e7e84b95582248c1039dcfc7c4db205a618f7da22a166db482f0105
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3.orig.tar.gz.asc' ncurses_6.3.orig.tar.gz.asc 729 SHA512:5673088e7d6af580e8f1e163687146adb51261cd3c75be9ea61368c7590efc0e5e4bc1c2ae76d717f289ff6609089c5ca1f7e4a572266d7b6c5daba98eabed2e
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3-2ubuntu0.1.debian.tar.xz' ncurses_6.3-2ubuntu0.1.debian.tar.xz 56080 SHA512:d37d4fc956ad1410d0338ee4f5b465e58f35056e33d909a4871d738ef83d9002200d5c31f35ee23e6817db950fd2e227a87e5e01bde8df221dfa2650edb7583a
```

### `dpkg` source package: `net-tools=1.60+git20181103.0eebece-1ubuntu5.4`

Binary Packages:

- `net-tools=1.60+git20181103.0eebece-1ubuntu5.4`

Licenses: (parsed from: `/usr/share/doc/net-tools/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris net-tools=1.60+git20181103.0eebece-1ubuntu5.4
'http://archive.ubuntu.com/ubuntu/pool/main/n/net-tools/net-tools_1.60%2bgit20181103.0eebece-1ubuntu5.4.dsc' net-tools_1.60+git20181103.0eebece-1ubuntu5.4.dsc 2251 SHA512:75fe65606f47bfc350bfbb737826aa829191dc379ef99c637a35221fc753dc8a99fb36897e06949d15c2feabff81fcbcd9fdad7d7fa8ca1b1455f8eda312c85e
'http://archive.ubuntu.com/ubuntu/pool/main/n/net-tools/net-tools_1.60%2bgit20181103.0eebece.orig.tar.xz' net-tools_1.60+git20181103.0eebece.orig.tar.xz 197516 SHA512:2ae46a478eecbdc42b5233505329fd296137e1f7d603304f55afcc8ed1f0c89877305f2f47ff0794126e5dab063a380992fb4a57ee12f4803f26ef30ae164345
'http://archive.ubuntu.com/ubuntu/pool/main/n/net-tools/net-tools_1.60%2bgit20181103.0eebece-1ubuntu5.4.debian.tar.xz' net-tools_1.60+git20181103.0eebece-1ubuntu5.4.debian.tar.xz 61764 SHA512:7b08a3bddd9f03e32d85d92a0d3a44b848165de667120ca5684504d7f62fb08438c300ab3dae99625f8aa07596f096fde5b013e40eb5b6ffb1abb401c2de8e57
```

### `dpkg` source package: `nettle=3.7.3-1build2`

Binary Packages:

- `libhogweed6:amd64=3.7.3-1build2`
- `libnettle8:amd64=3.7.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libhogweed6/copyright`, `/usr/share/doc/libnettle8/copyright`)

- `Expat`
- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.7.3-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.7.3-1build2.dsc' nettle_3.7.3-1build2.dsc 2165 SHA512:3f774011dd48205720ac7e6aa9a44b5afa64c24fce825d6583b58c02f3c8f500ecafa265d18d5deb1ab65d6e938dd76a7917f1d5c3dab0aea28148d531fa26cd
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.7.3.orig.tar.gz' nettle_3.7.3.orig.tar.gz 2383985 SHA512:9901eba305421adff6d551ac7f478dff3f68a339d444c776724ab0b977fe6be792b1d2950c8705acbe76bd924fd6d898a65eded546777884be3b436d0e052437
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.7.3-1build2.debian.tar.xz' nettle_3.7.3-1build2.debian.tar.xz 22100 SHA512:c1935d35e9f04798273053ab92c7405ec225a5d72ba6c2869b0f2bf54b459ac428e113bc149796e91834a8b56082f8bbfbb906a6cd6787142b8932bd1dd83cec
```

### `dpkg` source package: `nghttp2=1.43.0-1ubuntu0.2`

Binary Packages:

- `libnghttp2-14:amd64=1.43.0-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `SIL-OFL-1.1`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.43.0-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0-1ubuntu0.2.dsc' nghttp2_1.43.0-1ubuntu0.2.dsc 2679 SHA512:2ad7840a04e95d55fa98b6693be289fcc86330c2b9ea06b08cdf9f1bd2c3e0bffe2f312433f243ea8b7fd8ffeeba9c840581b3eb1bef662f487d075a8428ad2a
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0.orig.tar.bz2' nghttp2_1.43.0.orig.tar.bz2 4521786 SHA512:f2e6665ad6c73f0a1a8c7b34ca821a905868d41dafca913e6a054eb5afb534a85ae91618c1a4b098e43f350ca3703fd1ece7848f0a771e8393a3eb0581ceaf59
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0-1ubuntu0.2.debian.tar.xz' nghttp2_1.43.0-1ubuntu0.2.debian.tar.xz 23788 SHA512:ebbbd0c00089e2b48feef151b00b952cfec456662f35d8dd68e886008cdb61bec788c5fa8bbd63614c18a2e06f187bf3112417e759a4f55a9c0db27511aa461a
```

### `dpkg` source package: `norm=1.5.9+dfsg-2`

Binary Packages:

- `libnorm1:amd64=1.5.9+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libnorm1/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause-UC`
- `NRL-2-clause`
- `NRL-3-clause`

Source:

```console
$ apt-get source -qq --print-uris norm=1.5.9+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/universe/n/norm/norm_1.5.9%2bdfsg-2.dsc' norm_1.5.9+dfsg-2.dsc 1683 SHA512:8dcdfe6f304401248b61b92fc860f738c8265247f64b145acbd388e216e144d239b2da50fa28227a842de8a32f69f20281249c3ec97f85aef530307ea4e03059
'http://archive.ubuntu.com/ubuntu/pool/universe/n/norm/norm_1.5.9%2bdfsg.orig.tar.xz' norm_1.5.9+dfsg.orig.tar.xz 1526456 SHA512:b25211261dff2b4a61e506d3c8d6a944c4eb1740d6c487d9e3d50e4601dfe768fb8d95d976e1ee29fbcd0e15f4ed094783496b178ca99553660980250e5814bb
'http://archive.ubuntu.com/ubuntu/pool/universe/n/norm/norm_1.5.9%2bdfsg-2.debian.tar.xz' norm_1.5.9+dfsg-2.debian.tar.xz 8776 SHA512:942e6a5728702bad73b871d596caa55a9592b46709fe881ba99c92cf15746742f5187fd7110d78644795a398855bf98100deb376261aad33561a1c335dea1ae1
```

### `dpkg` source package: `npth=1.6-3build2`

Binary Packages:

- `libnpth0:amd64=1.6-3build2`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-3build2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3build2.dsc' npth_1.6-3build2.dsc 2063 SHA512:19ea7bd0ffc2b0aff06c52298c9a25c2f30619239bea09b571feb4a3d162f461a4529136e351da42b16ab3eaef5add24234f644e822e859ccb32de5bfd658ec0
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA512:2ed1012e14a9d10665420b9a23628be7e206fd9348111ec751349b93557ee69f1176bcf7e6b195b35b1c44a5e0e81ee33b713f03d79a33d1ecd9037035afeda2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3build2.debian.tar.xz' npth_1.6-3build2.debian.tar.xz 10904 SHA512:426ab3ab9e27b3701d67cde0a4c4040aa9ccac22a0266321824487fe80a118ccd6860b6fa0fb5ca3c46dfa3c20053889fbb51a2e74618065b3aff059a0216c4c
```

### `dpkg` source package: `nspr=2:4.35-0ubuntu0.22.04.1`

Binary Packages:

- `libnspr4:amd64=2:4.35-0ubuntu0.22.04.1`

Licenses: (parsed from: `/usr/share/doc/libnspr4/copyright`)

- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris nspr=2:4.35-0ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nspr/nspr_4.35-0ubuntu0.22.04.1.dsc' nspr_4.35-0ubuntu0.22.04.1.dsc 2110 SHA512:ace773b6a831b5fc42989f5f2fe7f9facb26e4796fbdc5e28353dd3b37e72820fa0ac93b120fc277c19ca49d99db481a3dd0311f2b9b2fe6afd18864726b9380
'http://archive.ubuntu.com/ubuntu/pool/main/n/nspr/nspr_4.35.orig.tar.gz' nspr_4.35.orig.tar.gz 1096974 SHA512:502815833116e25f79ddf71d1526484908aa92fbc55f8a892729cb404a4daafcc0470a89854cd080d2d20299fdb7d9662507c5362c7ae661cbacf308ac56ef7f
'http://archive.ubuntu.com/ubuntu/pool/main/n/nspr/nspr_4.35-0ubuntu0.22.04.1.debian.tar.xz' nspr_4.35-0ubuntu0.22.04.1.debian.tar.xz 11384 SHA512:70aafc40c11aa995ce9fb3a2182f90c84011beaa3bcf8e33b19e0d1c398979833326cf891d45f27308f64f242ea3b14a2304e31fed4bdfd0f9555db754b6b6f5
```

### `dpkg` source package: `nss=2:3.98-0ubuntu0.22.04.2`

Binary Packages:

- `libnss3:amd64=2:3.98-0ubuntu0.22.04.2`

Licenses: (parsed from: `/usr/share/doc/libnss3/copyright`)

- `BSD-3`
- `MIT`
- `MPL-2.0`
- `Zlib`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nss=2:3.98-0ubuntu0.22.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nss/nss_3.98-0ubuntu0.22.04.2.dsc' nss_3.98-0ubuntu0.22.04.2.dsc 2294 SHA512:20d109133d756e1fa15ce04303443d99b6105a73595dece3b6eaad781df15dc89102ed92c4291dc1142cee27244cc3a32914af97acbd69d5904c367e5a116899
'http://archive.ubuntu.com/ubuntu/pool/main/n/nss/nss_3.98.orig.tar.gz' nss_3.98.orig.tar.gz 76685475 SHA512:4f335c5c284eff6424745cc15e32037715a915f6f61687ec36a8ffaef0e45d152602a1be275bbb2f14650c7d258d6488430cdcf512b18ba7cb73cd43ac625681
'http://archive.ubuntu.com/ubuntu/pool/main/n/nss/nss_3.98-0ubuntu0.22.04.2.debian.tar.xz' nss_3.98-0ubuntu0.22.04.2.debian.tar.xz 26096 SHA512:20bebf5fee2d03d7078a0ac7558ecd764abf6124f2259f7283db0d397322a35dd12bdb007518cc8e9b9ef5c8fec8f0466d594ffd6d1d3bc1ecc24e1aa75393e3
```

### `dpkg` source package: `numactl=2.0.14-3ubuntu2`

Binary Packages:

- `libnuma1:amd64=2.0.14-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libnuma1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris numactl=2.0.14-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.14-3ubuntu2.dsc' numactl_2.0.14-3ubuntu2.dsc 2110 SHA512:ea29c0e0746cf1b04c3295a2be4809aad18115a7dd0326f8e1bd73465bf0d1031f5853b18e755c4a5de0592e5cb18e50e76ebfbb1f4a92c9bcf13dae28165d28
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.14.orig.tar.gz' numactl_2.0.14.orig.tar.gz 107583 SHA512:adaf405f092fd9653f26d00f8c80cb83852c56ebd5d00e714e20d505008e74aa7105b0fb7aa55a605deac0d1491ceff57de931037d33e7944fca105bc6510ed4
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.14-3ubuntu2.debian.tar.xz' numactl_2.0.14-3ubuntu2.debian.tar.xz 7588 SHA512:f3e34577c93c315047be275596d59e0481f177e090cd0c7ca8ef6ac3a79eab1ee988003afd49053a0cc6a86bf3f4b0ea387f53da279f9dcbc0d9ed7ca3815fd1
```

### `dpkg` source package: `ocl-icd=2.2.14-3`

Binary Packages:

- `ocl-icd-libopencl1:amd64=2.2.14-3`

Licenses: (parsed from: `/usr/share/doc/ocl-icd-libopencl1/copyright`)

- `BSD-2-Clause`

Source:

```console
$ apt-get source -qq --print-uris ocl-icd=2.2.14-3
'http://archive.ubuntu.com/ubuntu/pool/universe/o/ocl-icd/ocl-icd_2.2.14-3.dsc' ocl-icd_2.2.14-3.dsc 2235 SHA512:b47a8dd6f8f8be40997df883dce7f544226ef5e4d1a624c9f38018252941ef82e36121a816b2896c6c73a7a39726dbf2111cb088ac1d6e27b56619472688756b
'http://archive.ubuntu.com/ubuntu/pool/universe/o/ocl-icd/ocl-icd_2.2.14.orig.tar.gz' ocl-icd_2.2.14.orig.tar.gz 100629 SHA512:78510b6fa4e2c6a52141a51ccf0d0ef3110b0b4902a43bb97f7622ff0ce470b108dc05c9619c28ce8758ccea1e1cf6b2e7f1a296f8b07f52532f23b2b036a5cf
'http://archive.ubuntu.com/ubuntu/pool/universe/o/ocl-icd/ocl-icd_2.2.14-3.debian.tar.xz' ocl-icd_2.2.14-3.debian.tar.xz 12140 SHA512:ad43b9372394c6c39392eb5501af9f54f21119c58ef143ab7286ca9b0bc9d85ae1b5af25ef06d73a5222c094dc5cc33cec026d7fb3d45e1c70612e7619b5218b
```

### `dpkg` source package: `openal-soft=1:1.19.1-2build3`

Binary Packages:

- `libopenal-data=1:1.19.1-2build3`
- `libopenal1:amd64=1:1.19.1-2build3`

Licenses: (parsed from: `/usr/share/doc/libopenal-data/copyright`, `/usr/share/doc/libopenal1/copyright`)

- `Apache`
- `BSD-3-clause-cmake`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2+`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris openal-soft=1:1.19.1-2build3
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openal-soft/openal-soft_1.19.1-2build3.dsc' openal-soft_1.19.1-2build3.dsc 2399 SHA512:52c56e729a3401bd0f072d10af0d5dc17c7f2afa515deb776f3b28686f70fdc5316c3afa611f4f97b65243c89fe12c8f85f064005ebd47b61fcb6e14e67a8a5e
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openal-soft/openal-soft_1.19.1.orig.tar.gz' openal-soft_1.19.1.orig.tar.gz 683061 SHA512:4a64cc90ddeaa3773610b0bc8023d231100f3396f3fc5bd079db81600f80a789c75e6af03391bfc78a903c96bb71f8052a9ae802ea81422028e5b12b7eb6c47b
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openal-soft/openal-soft_1.19.1-2build3.debian.tar.xz' openal-soft_1.19.1-2build3.debian.tar.xz 12932 SHA512:2353577b8a567a0d8559318f14ac4b4bb9f7f27594e255acd01abbd67669273ed1e3d087552afb876679e1ef6a76f539bd69aabcd895112f35eb4e02d21730d3
```

### `dpkg` source package: `openjdk-lts=11.0.28+6-1ubuntu1~22.04.1`

Binary Packages:

- `openjdk-11-jdk:amd64=11.0.28+6-1ubuntu1~22.04.1`
- `openjdk-11-jdk-headless:amd64=11.0.28+6-1ubuntu1~22.04.1`
- `openjdk-11-jre:amd64=11.0.28+6-1ubuntu1~22.04.1`
- `openjdk-11-jre-headless:amd64=11.0.28+6-1ubuntu1~22.04.1`

Licenses: (parsed from: `/usr/share/doc/openjdk-11-jdk/copyright`, `/usr/share/doc/openjdk-11-jdk-headless/copyright`, `/usr/share/doc/openjdk-11-jre/copyright`, `/usr/share/doc/openjdk-11-jre-headless/copyright`)

- `GPL with Classpath exception`
- `GPL-2`
- `LGPL`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openjpeg2=2.4.0-6ubuntu0.4`

Binary Packages:

- `libopenjp2-7:amd64=2.4.0-6ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`)

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
$ apt-get source -qq --print-uris openjpeg2=2.4.0-6ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.4.0-6ubuntu0.4.dsc' openjpeg2_2.4.0-6ubuntu0.4.dsc 2912 SHA512:17f0caed54afc4ab90c6ff507efc490392a3e308dbb507ff8a41522f18181b271bd1f3f059c752ec734661c6dca5a2f755835d9b3043ea1d80a07952eff153bc
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.4.0.orig.tar.xz' openjpeg2_2.4.0.orig.tar.xz 1396964 SHA512:717ead13e0805d52138bedef1a77d51b676c5a2b882ca7f2206b665b3ba5ea2b435fd81c09780e6c1f14400a49c82fcd1eb2cbea1e1d207b541e98797ecd684f
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.4.0-6ubuntu0.4.debian.tar.xz' openjpeg2_2.4.0-6ubuntu0.4.debian.tar.xz 24448 SHA512:a07855ce547e848b41c613f39bea9b8d2f27b00884f8dd14981db12a879810258bf2aef7e941529a1f0a59991396e498f93db5faa3637b068c9a17f7d449eadd
```

### `dpkg` source package: `openldap=2.5.19+dfsg-0ubuntu0.22.04.1`

Binary Packages:

- `libldap-2.5-0:amd64=2.5.19+dfsg-0ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openldap=2.5.19+dfsg-0ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.5.19%2bdfsg-0ubuntu0.22.04.1.dsc' openldap_2.5.19+dfsg-0ubuntu0.22.04.1.dsc 3319 SHA512:14cf58886e69157bc11fccc9d20c9d63e45549b530d6ed5d1c05828a753ba73cbc81a22c6d2ed770cf74bed67268ed2f4aa6e50ee540d0fa7ca90aa1d83e2986
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.5.19%2bdfsg.orig.tar.xz' openldap_2.5.19+dfsg.orig.tar.xz 3718696 SHA512:ed029c62e889db318dd09849249403e5496a41c4dd351c16e3514e5bb3f12733ab0681ab25a07cb3b4541674305f39a51ae5aac9cbbee2f126fe5c31aee0860c
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.5.19%2bdfsg-0ubuntu0.22.04.1.debian.tar.xz' openldap_2.5.19+dfsg-0ubuntu0.22.04.1.debian.tar.xz 173568 SHA512:ab691963c87b88a0d6158a69374fc7e3d46e842716cd2d8fcb939f711193d0d494e584828e0b44b45406aeeff785971e58bd12da353b2448e1ca461f3ed8e6dc
```

### `dpkg` source package: `openssl=3.0.2-0ubuntu1.20`

Binary Packages:

- `libssl3:amd64=3.0.2-0ubuntu1.20`
- `openssl=3.0.2-0ubuntu1.20`

Licenses: (parsed from: `/usr/share/doc/libssl3/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.2-0ubuntu1.20
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2-0ubuntu1.20.dsc' openssl_3.0.2-0ubuntu1.20.dsc 2730 SHA512:973fdaac3db4ee13e4fb3907cbf5f6966c816de9e7a76165769562596a1aa533e68be64678da84dd400ef2ef3a37bc0ff2598bf8314654bec894e64e115663b3
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2.orig.tar.gz' openssl_3.0.2.orig.tar.gz 15038141 SHA512:f986850d5be908b4d6b5fd7091bc4652d7378c9bccebfbc5becd7753843c04c1eb61a1749c432139d263dfac33df0b1f6c773664b485cad47542266823a4eb03
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2.orig.tar.gz.asc' openssl_3.0.2.orig.tar.gz.asc 488 SHA512:4303391a58107c76ad9b05510f5bfc95f687f4cb2f9ff5b03fb262ba99b573423ab83f0437471199954496799b343191b889ad9ef8fabdd7ee4ec3ec9b5f1d81
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2-0ubuntu1.20.debian.tar.xz' openssl_3.0.2-0ubuntu1.20.debian.tar.xz 266660 SHA512:99203365623b8360b2a9997fa7c8d3b56424518f30e20411cb7d2921041f696a7877372dfd23e58ad63af5d4159e0b66e94049fa64bbb16ba80898c680d10260
```

### `dpkg` source package: `opus=1.3.1-0.1build2`

Binary Packages:

- `libopus0:amd64=1.3.1-0.1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris opus=1.3.1-0.1build2
'http://archive.ubuntu.com/ubuntu/pool/main/o/opus/opus_1.3.1-0.1build2.dsc' opus_1.3.1-0.1build2.dsc 2076 SHA512:29a7c707385e589851d4154d1e40d9150c1da90212d096fcd3e9937295b870e6629eed77be4abbc2a4ba89a0d0408fc22f7c83eeaec141b46a6c3a9a222439a7
'http://archive.ubuntu.com/ubuntu/pool/main/o/opus/opus_1.3.1.orig.tar.gz' opus_1.3.1.orig.tar.gz 1040054 SHA512:6cd5e4d8a0551ed5fb59488c07a5cc18a241d1fde5f9eb9f16cd4e77abcdb4134dd51ad1d737be1e6039bfa56912510b8648152f2478a1f21c7c1d9ce32933cd
'http://archive.ubuntu.com/ubuntu/pool/main/o/opus/opus_1.3.1-0.1build2.diff.gz' opus_1.3.1-0.1build2.diff.gz 9154 SHA512:d85f77e7bc8055295cc1f7be10b511c862573b770624cdbcc47b7cfe278df5e60569e86f7d1bbc27428a8879b9dd00d485498699cb6eaa4a23d0aaf25f34d73e
```

### `dpkg` source package: `orc=1:0.4.32-2ubuntu0.1`

Binary Packages:

- `liborc-0.4-0:amd64=1:0.4.32-2ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris orc=1:0.4.32-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.32-2ubuntu0.1.dsc' orc_0.4.32-2ubuntu0.1.dsc 2283 SHA512:0e0311e085064849a895d300e27bc2ff478c62a093b568328fb4823ab0a7d9f6d4bf30846c4705d207429116aa5158cdfe106bb1f8a9766ef63de914b41cec9f
'http://archive.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.32.orig.tar.xz' orc_0.4.32.orig.tar.xz 180340 SHA512:63e2ab05bc23e07cd5c1ed3192515ec3b1f666abb4f9ea5de4bd72461f3a5d7066860e2ad38f35d0acd81fadfa06f2a18d61838eae89c74dec6a78099a343567
'http://archive.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.32-2ubuntu0.1.debian.tar.xz' orc_0.4.32-2ubuntu0.1.debian.tar.xz 7180 SHA512:ceb4d9c95bbb929932d69185ccef6d86dc68047b0b72615d54f13e435a309c484df91165027f2dd3be3134f8b1b3196a9de28c2c1cf0c90e2db882992e527868
```

### `dpkg` source package: `p11-kit=0.24.0-6build1`

Binary Packages:

- `libp11-kit0:amd64=0.24.0-6build1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `LGPL-2.1`
- `LGPL-2.1+`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.24.0-6build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.24.0-6build1.dsc' p11-kit_0.24.0-6build1.dsc 2633 SHA512:510edf53bc83deef34737f3607995e814695930eacb2257013262023d0c21c3180ac782595bbdc530ea89e8dba567d2f44748a9c6713befb3a3e98245896f179
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.24.0.orig.tar.xz' p11-kit_0.24.0.orig.tar.xz 834392 SHA512:48369d6fdae79b8c5a255c821fbdb982f0c649cce07c0d92f0ff0c16322fea8919faa94067cae2efede2da3646c0e69a71a3e399b769dc2327f247bcb113eb3c
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.24.0.orig.tar.xz.asc' p11-kit_0.24.0.orig.tar.xz.asc 833 SHA512:f802c6f42f437d466b008d0c62aedc2f466bcf5bec93a5fbeec183057d22eacd28184198f624972d9df684a663820e77ebdc8d8c0d14533707691b9d69cb9f69
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.24.0-6build1.debian.tar.xz' p11-kit_0.24.0-6build1.debian.tar.xz 23264 SHA512:a858251688a0655411907d5ac2d122efab057c7bc28dcb3970c68412ca699b00234b74373cbd44472e21cd3f43eab239ddd8411f188e4c214c587052bebedd4c
```

### `dpkg` source package: `pam=1.4.0-11ubuntu2.6`

Binary Packages:

- `libpam-modules:amd64=1.4.0-11ubuntu2.6`
- `libpam-modules-bin=1.4.0-11ubuntu2.6`
- `libpam-runtime=1.4.0-11ubuntu2.6`
- `libpam0g:amd64=1.4.0-11ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pam=1.4.0-11ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0-11ubuntu2.6.dsc' pam_1.4.0-11ubuntu2.6.dsc 2728 SHA512:18bfb2e4093ba1ef97a0ab9206a273c7180a607f3709567e72e5968b8d20999960869d6bbf806413066a1ba6c0dd64717015c5c20e83fb7cad31171b0e1a766e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0.orig.tar.xz' pam_1.4.0.orig.tar.xz 988908 SHA512:26eda95c45598a500bc142da4d1abf93d03b3bbb0f2390fa87c72dcbffa208dbfa115c0b411095c31ee9955e36422ccf3e2df3bd486818fafffef8c4310798c4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0-11ubuntu2.6.debian.tar.xz' pam_1.4.0-11ubuntu2.6.debian.tar.xz 187648 SHA512:5e2fe17f27a9fcc30940738efc3d8e0dc72bf2d8c9ab5bf8ecd508151ff00eb29e133d21980fe6c0acf24e201fc84af88b9134017747883c40ec78cdc7e306ae
```

### `dpkg` source package: `pango1.0=1.50.6+ds-2ubuntu1`

Binary Packages:

- `libpango-1.0-0:amd64=1.50.6+ds-2ubuntu1`
- `libpangocairo-1.0-0:amd64=1.50.6+ds-2ubuntu1`
- `libpangoft2-1.0-0:amd64=1.50.6+ds-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

- `Apache-2`
- `Apache-2.0`
- `Bitstream-Vera`
- `CC-BY-SA-3.0`
- `CC-BY-SA-3.0,`
- `CC0-1.0`
- `CC0-1.0,`
- `Chromium-BSD-style`
- `Example`
- `Expat`
- `GPL-2+`
- `GPL-2+,`
- `GPL-2.0`
- `GPL-3.0`
- `GPL-3.0+`
- `GPL-3.0+,`
- `ICU`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2+,`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1`
- `OFL-1.1`
- `TCL`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.50.6+ds-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.50.6%2bds-2ubuntu1.dsc' pango1.0_1.50.6+ds-2ubuntu1.dsc 3878 SHA512:9fc410945facf39d80ce6db1be2f34776cf0fed318fe1057eaaf23e4077458650bafd48673b4e69fdce2f37c9b53c4a7d0e1b89692c4147198071432c0b67b36
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.50.6%2bds.orig.tar.xz' pango1.0_1.50.6+ds.orig.tar.xz 2673480 SHA512:d7cca72ffe9e0d4b2e85cff5f372177444466e8b794f74bbe3dbd1a3ddce1eecfc0645dd003eb319308131266ed0e484d3212166401abe189eaa462d3f872a41
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.50.6%2bds-2ubuntu1.debian.tar.xz' pango1.0_1.50.6+ds-2ubuntu1.debian.tar.xz 51196 SHA512:6b66a168f4e922ca6dedecfb4dcb9b17fd61bfa0613f386eccbb93e0f1e6f6100711c0732fb4575cfebedfa40f8939de87aab27e3858d8efccadfd48052955fe
```

### `dpkg` source package: `pcre2=10.39-3ubuntu0.1`

Binary Packages:

- `libpcre2-8-0:amd64=10.39-3ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre2=10.39-3ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39-3ubuntu0.1.dsc' pcre2_10.39-3ubuntu0.1.dsc 2142 SHA512:8f062a4ba129491e0ec755f945b84e6e6d252e4d87b87ae0dc46156320095557093f7c3305a31cbca9252a2cbc172d701606030ebdae147eef3fbd5616b4ed99
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39.orig.tar.gz' pcre2_10.39.orig.tar.gz 2309964 SHA512:fe17ea0191a91d4e4fe88a44a07883db594941376a6e38556e03ff3b594820596fd3e43be2d73b700ca68cd0c44e38c33cc891a57b8ed65e34cd832196bc09b2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39-3ubuntu0.1.diff.gz' pcre2_10.39-3ubuntu0.1.diff.gz 11214 SHA512:7b8848adbd237351d14e68cf13d26fe0330718d2e807c69b091d2eefdd4c5f4ebde9e3b403d898b52ffcff674eb6bd0ff6995190c1fc42668e4bf8173ded7f14
```

### `dpkg` source package: `pcre3=2:8.39-13ubuntu0.22.04.1`

Binary Packages:

- `libpcre3:amd64=2:8.39-13ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-13ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-13ubuntu0.22.04.1.dsc' pcre3_8.39-13ubuntu0.22.04.1.dsc 2101 SHA512:c2b619e559192c367485fec01cf65dbc49a67ec8f2fb9d5785fdf7dba052540d70c16b4316afc83f4765ef9b57f3e2c0e6f245500866476df8a8a90310584f62
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA512:8b0f14ae5947c4b2d74876a795b04e532fd71c2479a64dbe0ed817e7c7894ea3cae533413de8c17322d305cb7f4e275d72b43e4e828eaca77dc4bcaf04529cf6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-13ubuntu0.22.04.1.debian.tar.gz' pcre3_8.39-13ubuntu0.22.04.1.debian.tar.gz 28251 SHA512:50aa437187fd45632213fe7b09a69dfbe2a58ad568a7f71c47ddab204db49850b732f17c8295788afd0c58d8134620a11aaa9fa259a980a0ab85ce043098a659
```

### `dpkg` source package: `pcsc-lite=1.9.5-3ubuntu1`

Binary Packages:

- `libpcsclite1:amd64=1.9.5-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libpcsclite1/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris pcsc-lite=1.9.5-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcsc-lite/pcsc-lite_1.9.5-3ubuntu1.dsc' pcsc-lite_1.9.5-3ubuntu1.dsc 2411 SHA512:5daefcbe6ee55deed7c44f3ad7ef7d852a23c94230be52f454388df16fd2f134498f005e4f05e6d9912b449a5aab44ff667123ff6c3e253eb6b5741b232ede4e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcsc-lite/pcsc-lite_1.9.5.orig.tar.bz2' pcsc-lite_1.9.5.orig.tar.bz2 775736 SHA512:0315c2cf97cc9da0f5faf115f24e523b5a1746cea250a4fe6c4d5d7b2fbfc7c3ea0f068611072ca84866c672eb679e8067101437573148ccd1ac5ad26b18cd78
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcsc-lite/pcsc-lite_1.9.5.orig.tar.bz2.asc' pcsc-lite_1.9.5.orig.tar.bz2.asc 833 SHA512:5e678c784dd3a860956c1e8ccc40e801a2f676faf46ca3137a309f002a44a65a87a98da0d130da57c6551a80dded9a60259b8c0fb06d3586e2020babf0de18ed
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcsc-lite/pcsc-lite_1.9.5-3ubuntu1.debian.tar.xz' pcsc-lite_1.9.5-3ubuntu1.debian.tar.xz 19320 SHA512:faa39ebcf5e06bebf76eac1a80e979f071623868a455f76b61ec56a0f10fca456d95f1d7d688cbfa8ca333d5197f865ad0b3f092e2a6c54327abc28c3b5a7a41
```

### `dpkg` source package: `perl=5.34.0-3ubuntu1.5`

Binary Packages:

- `perl-base=5.34.0-3ubuntu1.5`

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
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `HSIEH-BSD`
- `HSIEH-DERIVATIVE`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `RRA-KEEP-THIS-NOTICE`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.34.0-3ubuntu1.5
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0-3ubuntu1.5.dsc' perl_5.34.0-3ubuntu1.5.dsc 2976 SHA512:e490cfc45a24fa7538f5a92054a19a52fd9675fe7a7e6e0e20b7a6c3e6939ec0cf1b39e71f2daebb8e5ab0968d851fdf1b713166d6855968fb47e846d7350020
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0.orig-regen-configure.tar.xz' perl_5.34.0.orig-regen-configure.tar.xz 415412 SHA512:2581152e0747105314c4fa4167f1f97d286436b996341b9b75e4099ba18f15eb0d2b42888622fbe9b5499d3fe304bc8aa9ad207a945f590135beccfb68ea28b0
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0.orig.tar.xz' perl_5.34.0.orig.tar.xz 12881416 SHA512:691b4b31eacec357191fba777612b4e3eae59e946a22998a50766697c0d61db1d42a9b3bc1e41abf0d1ca1893e4a7c06d7bf3290480cf03d7f79befd7a8a3267
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0-3ubuntu1.5.debian.tar.xz' perl_5.34.0-3ubuntu1.5.debian.tar.xz 200524 SHA512:bb565b5ee511cd73dccf9b596f356fd4d4a32dcd5a584fa73e806322a541706d6940c54732d20d6eb1fcc0bac06fcef5a98f5f6a592b83b12a8ada3157dfdc6f
```

### `dpkg` source package: `pinentry=1.1.1-1build2`

Binary Packages:

- `pinentry-curses=1.1.1-1build2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.1.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.1.1-1build2.dsc' pinentry_1.1.1-1build2.dsc 2953 SHA512:d66ea2b52226887f18bab9f7ebfa65f5da95225c57362ec3be1792c261a60d7c74bb0b60d82e556f977246ef615add3d89e7137a16d73248a044e0ea752246ca
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.1.1.orig.tar.bz2' pinentry_1.1.1.orig.tar.bz2 515723 SHA512:d6ab5af8ac2f3c9c05e09703e95d8e2676f9b2b7ceb97f6a31d101d0e9da7a1e106a6d3eabe86cab1bb35a4b119a7cba1380ac64bf13c61af0b3c48803116c12
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.1.1.orig.tar.bz2.asc' pinentry_1.1.1.orig.tar.bz2.asc 390 SHA512:2b696e5a59219c6fca719d5f948d508279c483d1d2b2c99221522648fe3098da4a195aca2527fbb5b777fa2905dbda642edb5f6ac4038ed9720a5291ce282cff
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.1.1-1build2.debian.tar.xz' pinentry_1.1.1-1build2.debian.tar.xz 20060 SHA512:34adaf10856d36e7294fbc9841f6c1b2c9fc1d507fcff6d4c9c3f4e11d5aed9ce744d091f25e013084d56ce8ed3245fff67a7b5d799081def0c68345e921241e
```

### `dpkg` source package: `pixman=0.40.0-1ubuntu0.22.04.1`

Binary Packages:

- `libpixman-1-0:amd64=0.40.0-1ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.40.0-1ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.40.0-1ubuntu0.22.04.1.dsc' pixman_0.40.0-1ubuntu0.22.04.1.dsc 2160 SHA512:8065633dbf5f1d29da28dc2b97cdd6cb3f01a2904ecac623a8dc7d4fec0c1b15fe973edcc9d3ccc69362ce8da209325c6b522da021bf51b3a27fb10ce280b095
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.40.0.orig.tar.gz' pixman_0.40.0.orig.tar.gz 913976 SHA512:063776e132f5d59a6d3f94497da41d6fc1c7dca0d269149c78247f0e0d7f520a25208d908cf5e421d1564889a91da44267b12d61c0bd7934cd54261729a7de5f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.40.0-1ubuntu0.22.04.1.diff.gz' pixman_0.40.0-1ubuntu0.22.04.1.diff.gz 327740 SHA512:68949ad2589a7ae9fbe217a3d7fc58894d5a1b4bc6e219840b8620141fa2240b44e6a393bf847bfd18f5fcab2c6c6f143273936b076c29e1f979052b1275cb8e
```

### `dpkg` source package: `pocketsphinx=0.8.0+real5prealpha+1-14ubuntu1`

Binary Packages:

- `libpocketsphinx3:amd64=0.8.0+real5prealpha+1-14ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libpocketsphinx3/copyright`)

- `BSD-2`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris pocketsphinx=0.8.0+real5prealpha+1-14ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pocketsphinx/pocketsphinx_0.8.0%2breal5prealpha%2b1-14ubuntu1.dsc' pocketsphinx_0.8.0+real5prealpha+1-14ubuntu1.dsc 2714 SHA512:d7e2bc586d3d027676550efa6cc39929fe69b41119c59c212eb9b320c48518e50aeb513d3453e4b7bd2f8a8fb029da354afd223a03ac3e86520240b083c42717
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pocketsphinx/pocketsphinx_0.8.0%2breal5prealpha%2b1.orig.tar.gz' pocketsphinx_0.8.0+real5prealpha+1.orig.tar.gz 31354573 SHA512:8165ab6eb49220b0e21ca41067d91f382f9a5e09b35faf4d0c9e4b1fa75b95f4b6181fe1056dd0a85bebd23a5fb830079e443ddaaa44414da8978f8fc66a0288
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pocketsphinx/pocketsphinx_0.8.0%2breal5prealpha%2b1-14ubuntu1.debian.tar.xz' pocketsphinx_0.8.0+real5prealpha+1-14ubuntu1.debian.tar.xz 8724 SHA512:9e42834f9287445d9e640c4c4d598a406bbe951dcda57919d9bab9dc777917666413f52238e10e64055a0479f9d1ce9ca985ae91a2cfbe7d45bbeb4f62f0c5ca
```

### `dpkg` source package: `poppler-data=0.4.11-1`

Binary Packages:

- `poppler-data=0.4.11-1`

Licenses: (parsed from: `/usr/share/doc/poppler-data/copyright`)

- `AGPL-3+`
- `BSD-3-cluase`
- `GPL-2`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris poppler-data=0.4.11-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler-data/poppler-data_0.4.11-1.dsc' poppler-data_0.4.11-1.dsc 2446 SHA512:49f9dca701ff36c78bf0bb13b8ef1951a96eb83f6407c452483743f3fc8f7895e673b52c1fe94020f67b0b5d2323bc54480a602b6e98b390325c1651ff703a2e
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler-data/poppler-data_0.4.11.orig-ai0.tar.gz' poppler-data_0.4.11.orig-ai0.tar.gz 3515 SHA512:e3be22e8b32bd6e9ad71db20c1bf40bd8abd286631dd9b1ce531518df7a8f3eda4ee5a5b65a5f929505c39ca8dd2230fe4525a068c37486c5f44037631628330
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler-data/poppler-data_0.4.11.orig-from-ghostscript.tar.xz' poppler-data_0.4.11.orig-from-ghostscript.tar.xz 2320 SHA512:527359b0ba3c26b9fd0f6e61a6c82a98429a5fec57d86c495cb80585dfadcd9f21be4308331e3b911e74e9be48c0c95304d25a622f534ab367f7be852e7150ce
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler-data/poppler-data_0.4.11.orig.tar.gz' poppler-data_0.4.11.orig.tar.gz 4497282 SHA512:a5b7ace28d1677e12f7500ab6345b277dc22cd48ace8d472c083933416879edf4da4efe8217b0e11f75a3387ed98d832fe50567884095b6c0e09ebd8802b0f32
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler-data/poppler-data_0.4.11-1.debian.tar.xz' poppler-data_0.4.11-1.debian.tar.xz 19664 SHA512:3bde3ba66ec5212cae67c1fcdbebd6297b912cb0c8fc02bc0db69c1e8cb86e46631bc7cd5840c8a376585b9548ceed2f7e786b00f28d1403505900d2fb440a30
```

### `dpkg` source package: `poppler=22.02.0-2ubuntu0.12`

Binary Packages:

- `libpoppler118:amd64=22.02.0-2ubuntu0.12`

Licenses: (parsed from: `/usr/share/doc/libpoppler118/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris poppler=22.02.0-2ubuntu0.12
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_22.02.0-2ubuntu0.12.dsc' poppler_22.02.0-2ubuntu0.12.dsc 3364 SHA512:1cfc708bac0830c672567b21e742e257320ca28ead8ae5f75961d02179da85c3e7e422da5f5a1f9f15c05746a28e6ffbc6caa7dfbe45f7b56a50062d3daf8e5f
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_22.02.0.orig.tar.xz' poppler_22.02.0.orig.tar.xz 1807024 SHA512:61867241d6d076dae554d654a8ad3b1a073079bad31f45170516b886fabb4c238ff2d49705924da219e128eb4052ac6337121967347600e54f61790dd0eed487
'http://archive.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_22.02.0-2ubuntu0.12.debian.tar.xz' poppler_22.02.0-2ubuntu0.12.debian.tar.xz 46692 SHA512:7d146c1f5deb702267624b1147cbe91a03260e45ac58679afb2a1e7f4230bc167b63d8473ae608f2bd2ad02767fbe887e246cf31b897fe21c3a0c75a35c9b2d2
```

### `dpkg` source package: `procps=2:3.3.17-6ubuntu2.1`

Binary Packages:

- `libprocps8:amd64=2:3.3.17-6ubuntu2.1`
- `procps=2:3.3.17-6ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libprocps8/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:3.3.17-6ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17-6ubuntu2.1.dsc' procps_3.3.17-6ubuntu2.1.dsc 2111 SHA512:585933efef8d8e93b4187c65b678d146960480386ac3172097c790723ffadbf1d5347e05cc6de2682adcb96dd5b45ec1f98a3e00cff33ad2b30f729939896aca
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17.orig.tar.xz' procps_3.3.17.orig.tar.xz 1008428 SHA512:59e9a5013430fd9da508c4655d58375dc32e025bb502bb28fb9a92a48e4f2838b3355e92b4648f7384b2050064d17079bf4595d889822ebb5030006bc154a1a7
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17-6ubuntu2.1.debian.tar.xz' procps_3.3.17-6ubuntu2.1.debian.tar.xz 35488 SHA512:720a52d14be82aecd59e2456fbb19574c99cc5281660a36994ef4aa619c14bbec43fd30b5e949446e5db6b6bebf8003a5f173298fe8bf56ac949d61ad0225a79
```

### `dpkg` source package: `pulseaudio=1:15.99.1+dfsg1-1ubuntu2.2`

Binary Packages:

- `libpulse0:amd64=1:15.99.1+dfsg1-1ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/libpulse0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `other`

Source:

```console
$ apt-get source -qq --print-uris pulseaudio=1:15.99.1+dfsg1-1ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pulseaudio/pulseaudio_15.99.1%2bdfsg1-1ubuntu2.2.dsc' pulseaudio_15.99.1+dfsg1-1ubuntu2.2.dsc 4030 SHA512:d449de148e098cfa102e27f7c3227ade8f19bd9f814a28cbbbdfa52663e08d3b15c9cc413bd0cb26b5d827d813e8773ab3711a80b943cda2ef0497439c8c11a1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pulseaudio/pulseaudio_15.99.1%2bdfsg1.orig.tar.xz' pulseaudio_15.99.1+dfsg1.orig.tar.xz 1439224 SHA512:d6d863454f210d5105a2c2a010a20a8f47c336e1e1b87b07bb54b3ece613d38938a5557e846a9f81ed066c02f1f0b7be0c2150b6c2b02b463bd52e8b60d67a09
'http://archive.ubuntu.com/ubuntu/pool/main/p/pulseaudio/pulseaudio_15.99.1%2bdfsg1-1ubuntu2.2.debian.tar.xz' pulseaudio_15.99.1+dfsg1-1ubuntu2.2.debian.tar.xz 100192 SHA512:3f91b1cda43e59666264cee136d2224151e10c781d2925b07de068347131f8aa62dfdc9181c3abceeb6bd7cd02a6f63f4c45e67a497d7e5146eac6f14fcb19d5
```

### `dpkg` source package: `python3-defaults=3.10.6-1~22.04.1`

Binary Packages:

- `libpython3-stdlib:amd64=3.10.6-1~22.04.1`
- `python3=3.10.6-1~22.04.1`
- `python3-minimal=3.10.6-1~22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.10.6-1~22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.10.6-1%7e22.04.1.dsc' python3-defaults_3.10.6-1~22.04.1.dsc 2951 SHA512:ce4c67568f3b0fd6c8f8d2daa74351825f1595b69998dce13f82caa077729cdb83fc472a636a466e27dd1ae681035e2b11bd82f73fa33c10b400c017afd54c90
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.10.6-1%7e22.04.1.tar.gz' python3-defaults_3.10.6-1~22.04.1.tar.gz 145962 SHA512:c509a2a887e4b758fbfcb6173ff046a6f73bdfdde3bd89f77102a4d99c7219d8e1805b41541c6cf658fe9dd44da188e6af450d87236d863d29f06147fea26ea1
```

### `dpkg` source package: `python3.10=3.10.12-1~22.04.11`

Binary Packages:

- `libpython3.10:amd64=3.10.12-1~22.04.11`
- `libpython3.10-minimal:amd64=3.10.12-1~22.04.11`
- `libpython3.10-stdlib:amd64=3.10.12-1~22.04.11`
- `python3.10=3.10.12-1~22.04.11`
- `python3.10-minimal=3.10.12-1~22.04.11`

Licenses: (parsed from: `/usr/share/doc/libpython3.10/copyright`, `/usr/share/doc/libpython3.10-minimal/copyright`, `/usr/share/doc/libpython3.10-stdlib/copyright`, `/usr/share/doc/python3.10/copyright`, `/usr/share/doc/python3.10-minimal/copyright`)

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


### `dpkg` source package: `raptor2=2.0.15-0ubuntu4.1`

Binary Packages:

- `libraptor2-0:amd64=2.0.15-0ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/libraptor2-0/copyright`)

- `Apache-2.0`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris raptor2=2.0.15-0ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/r/raptor2/raptor2_2.0.15-0ubuntu4.1.dsc' raptor2_2.0.15-0ubuntu4.1.dsc 2231 SHA512:dc4ea733d495848cd0c5818c3591225509418b5fbec89762bf30df8e8ab1df3e7772876659bb694f2ca4d2c8a6891d6f55a89e36109515371b5d7bf21c851ec3
'http://archive.ubuntu.com/ubuntu/pool/main/r/raptor2/raptor2_2.0.15.orig.tar.gz' raptor2_2.0.15.orig.tar.gz 1886657 SHA512:563dd01869eb4df8524ec12e2c0a541653874dcd834bd1eb265bc2943bb616968f624121d4688579cdce11b4f00a8ab53b7099f1a0850e256bb0a2c16ba048ee
'http://archive.ubuntu.com/ubuntu/pool/main/r/raptor2/raptor2_2.0.15-0ubuntu4.1.debian.tar.xz' raptor2_2.0.15-0ubuntu4.1.debian.tar.xz 11396 SHA512:b9ba070e03c8ce40a9b92d2c96a8b1f8ce41ba9b8fd3544443ac211609483c55eb71b99906b982044f9491f06da1b640c4520b98ee1d6b16dfcb52ae9dd27501
```

### `dpkg` source package: `rasqal=0.9.33-0.2ubuntu1`

Binary Packages:

- `librasqal3:amd64=0.9.33-0.2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/librasqal3/copyright`)

- `Apache-2.0`
- `Apache-2.0+`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris rasqal=0.9.33-0.2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rasqal/rasqal_0.9.33-0.2ubuntu1.dsc' rasqal_0.9.33-0.2ubuntu1.dsc 1578 SHA512:003c9bf1ddf98e26f9b03664f847b92bdf5bb8e8b87fa70e413e8af0a77970644f8950a89617d8a48d30acb7ca648692a7bb820ab80fb7d139879457c299efa1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rasqal/rasqal_0.9.33.orig.tar.gz' rasqal_0.9.33.orig.tar.gz 1595647 SHA512:05728682797470db9e51d156012e8fde9dec1554d107372faa11cbe6cdc3356e92386f4f8de6d7c41e3100b76f9b1c6809102a913829cddbd2ff29043c04d522
'http://archive.ubuntu.com/ubuntu/pool/main/r/rasqal/rasqal_0.9.33-0.2ubuntu1.debian.tar.xz' rasqal_0.9.33-0.2ubuntu1.debian.tar.xz 6112 SHA512:bbb307c4b88df3d6b27461ae4b2b4ee9a2e4ce4e2af729ac941b8b369332e77e400895f98fa421ea8def3d8139a1bfe915629845680328f6bd04fc6479670120
```

### `dpkg` source package: `readline=8.1.2-1`

Binary Packages:

- `libreadline8:amd64=8.1.2-1`
- `readline-common=8.1.2-1`

Licenses: (parsed from: `/usr/share/doc/libreadline8/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris readline=8.1.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.1.2-1.dsc' readline_8.1.2-1.dsc 2432 SHA512:3166229d2ac183a46455c7d8cf17ef1d509ca8651ffa7887f654d87bbe1d00a08f9a9f73f14e652ac067d89e5d1128998f8f09f6a1128c56049338ace65ed773
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.1.2.orig.tar.gz' readline_8.1.2.orig.tar.gz 2993073 SHA512:b512275c8aa8b3b3178366c6d681f867676fc1c881e375134a88e9c860a448535e04ca43df727817fd0048261e48203e88bd1c086e86572022d1d65fb0350e4d
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.1.2-1.debian.tar.xz' readline_8.1.2-1.debian.tar.xz 29292 SHA512:a64621c93975bc42ba171c9298c932f9515025513911e744183092e0ef9873db474c4ec27a21f310f40e7b970ba6300edb057552f7e90fc469897ffa2eb706f0
```

### `dpkg` source package: `redland=1.0.17-1.1ubuntu3`

Binary Packages:

- `librdf0:amd64=1.0.17-1.1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/librdf0/copyright`)

- `Apache-2.0`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris redland=1.0.17-1.1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/r/redland/redland_1.0.17-1.1ubuntu3.dsc' redland_1.0.17-1.1ubuntu3.dsc 1845 SHA512:b730f0fd1913bc53f3dde9a5f655ba7c888bb4f2fad01f55341373c1553db1a06f51237ccce59b28b4d81f8c168359767ea826619ba257ebbe584c5814a3e985
'http://archive.ubuntu.com/ubuntu/pool/main/r/redland/redland_1.0.17.orig.tar.gz' redland_1.0.17.orig.tar.gz 1621566 SHA512:363323ffc9e75d4f0e3a3b40952f6241fd0d8b9f46bfd4dd86cf0a5162de35257a8b70ce408a6083c03ba7c388982231a3774e5e9024b262ebb02968f778b850
'http://archive.ubuntu.com/ubuntu/pool/main/r/redland/redland_1.0.17-1.1ubuntu3.debian.tar.xz' redland_1.0.17-1.1ubuntu3.debian.tar.xz 8808 SHA512:25af353e4393b4d35a6ebe3b828f447b15532d160f7348c4998f48c45577bec333692ad0c5d9c63cf003968803d2959306c97a1d9e40b643f9e42b470f4bb484
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build4`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build4`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build4.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build4.dsc 2431 SHA512:7536b21c9c8be02e06171db49bf0b653e4b7738e6c01f74b0b7433c2986c731eafd1743f87836e7250a744d0e34dc700685bbe7128956a274e9a9832d32c891e
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build4.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build4.debian.tar.xz 8376 SHA512:b01ac33a7251e3c0fad21897d31710766136027b656cb29903cf8f695893648631037a96fa18aa40eae7ad363394344aad4f2fae152622618b88f22133c03578
```

### `dpkg` source package: `rubberband=2.0.0-2`

Binary Packages:

- `librubberband2:amd64=2.0.0-2`

Licenses: (parsed from: `/usr/share/doc/librubberband2/copyright`)

- `BSD-3-clause`
- `BSD-4-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `Zlib`
- `other-1`

Source:

```console
$ apt-get source -qq --print-uris rubberband=2.0.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rubberband/rubberband_2.0.0-2.dsc' rubberband_2.0.0-2.dsc 2372 SHA512:a0728d0c5cc713f33081b7d6d212173ccf4cffde614e89db495cbc8de7fcbebf247eb4404a27ac8a7712ddcc1d76fae1ae664001ec1ac7d2056a99837a27a8bf
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rubberband/rubberband_2.0.0.orig.tar.bz2' rubberband_2.0.0.orig.tar.bz2 175527 SHA512:a915a3eea75f0345e83010cc3ffd3c5e0c68a0c1d88da11b11a5fd5010196167c81db611a38c2c2b8d5c5a1f828f2c74a134e6ca8bb3a543af3ef70ce8d56101
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rubberband/rubberband_2.0.0-2.debian.tar.xz' rubberband_2.0.0-2.debian.tar.xz 9308 SHA512:b29b9baae56bf3521edc4f2197a58d18c94b8fbcd624eaf315f9163636807bb159cdee21e8d53c0eba0f2e3f954aa971034033f31a68b41ddb12ae0be2338f39
```

### `dpkg` source package: `sed=4.8-1ubuntu2`

Binary Packages:

- `sed=4.8-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris sed=4.8-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.8-1ubuntu2.dsc' sed_4.8-1ubuntu2.dsc 2217 SHA512:310ccdf0bac73d16c8898fd600acbeceb534a1be53c795fc6f6059eccb431b45ef9ebcde147c150f9fd5e0d33161269f53e191bb26a095b45339a28b1c3381b2
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.8.orig.tar.xz' sed_4.8.orig.tar.xz 1348048 SHA512:7de25d9bc2981c63321c2223f3fbcab61d7b0df4fcf7d4394b72400b91993e1288d8bf53948ed5fffcf5a98c75265726a68ad4fb98e1d571bf768603a108c1c8
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.8.orig.tar.xz.asc' sed_4.8.orig.tar.xz.asc 833 SHA512:9b886bdbd18ee2d60608cee3fd2b4193a1b6c3309d887ee05828c14b89b7b515dbf042a9e0ebdd13e6ccfa42e3cd217a408c796d68c4ebedaaa64f795000f095
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.8-1ubuntu2.debian.tar.xz' sed_4.8-1ubuntu2.debian.tar.xz 60936 SHA512:c4f0c5b3f75acbcb213e78f5696129e83bc721031be3c756150e84b7aa7e725ac0d5afacbe18e91d39bc2b7892986d92e1e21db89601ccf2bccb8ac088482180
```

### `dpkg` source package: `sensible-utils=0.0.17`

Binary Packages:

- `sensible-utils=0.0.17`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.17
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.17.dsc' sensible-utils_0.0.17.dsc 1733 SHA512:33e94cbe40fbcb083564b4e4f5947f7c4dc0da0724245d19290667cf8a56eb60ba5b94c0c85e8eee2ae7c988a25a094e7edff3159bbe4339dcf9136a6336f2f7
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.17.tar.xz' sensible-utils_0.0.17.tar.xz 66648 SHA512:fb7803cacc4222f232f64850e5559aca0b56ad98b6fd31f36c89740d72f7a235e7f2934ebce1d788882bff7196d59a2ed6cc3584f31e1c1c9e3593cedca2382b
```

### `dpkg` source package: `serd=0.30.10-2`

Binary Packages:

- `libserd-0-0:amd64=0.30.10-2`

Licenses: (parsed from: `/usr/share/doc/libserd-0-0/copyright`)

- `BSD-3-clause`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris serd=0.30.10-2
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serd/serd_0.30.10-2.dsc' serd_0.30.10-2.dsc 2496 SHA512:ecc979fe339a78d3acc6ea2d9b480a72240d53f7282bccb77b75506553e30eab4cdf805fc6856f1606886b498c205d6f2a5b63ce34eb6c5813984659a1c5a102
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serd/serd_0.30.10.orig.tar.bz2' serd_0.30.10.orig.tar.bz2 586386 SHA512:ed7b49abfd3dc3a724b047f5f0cd07b811596330c96d91c0ce90540440f03260e05daee76c3ccccc3d4ca39afbbd4f3d07decbb601730e90c133a09c640c0006
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serd/serd_0.30.10.orig.tar.bz2.asc' serd_0.30.10.orig.tar.bz2.asc 833 SHA512:885ae48ff5beae40908682733a4de26ecffecc2ba10686b03a3ef0d98199b008ca95221ab59c8dbf54c0b67543572aec6038000e74a502b6a4e3e7b4760c5cc5
'http://archive.ubuntu.com/ubuntu/pool/universe/s/serd/serd_0.30.10-2.debian.tar.xz' serd_0.30.10-2.debian.tar.xz 20752 SHA512:04e2df9acf093204f2529c2eaab216720e87da8c2ba70cbc8cd8cffa6b85bfe5e81798a94bbff97726a84022bd87221046eca4ce839670b79f6e3239909810ac
```

### `dpkg` source package: `shadow=1:4.8.1-2ubuntu2.2`

Binary Packages:

- `login=1:4.8.1-2ubuntu2.2`
- `passwd=1:4.8.1-2ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.8.1-2ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-2ubuntu2.2.dsc' shadow_4.8.1-2ubuntu2.2.dsc 2060 SHA512:765de71da656f0fd36b0872e05c1f736b167faf3af9a52247e0810d260606fe440a541c5558a882f8a5d150d91f76f01303cada28ba5febe4d16042eda3da7c8
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1.orig.tar.xz' shadow_4.8.1.orig.tar.xz 1611196 SHA512:780a983483d847ed3c91c82064a0fa902b6f4185225978241bc3bc03fcc3aa143975b46aee43151c6ba43efcfdb1819516b76ba7ad3d1d3c34fcc38ea42e917b
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-2ubuntu2.2.debian.tar.xz' shadow_4.8.1-2ubuntu2.2.debian.tar.xz 98488 SHA512:dfa83a48e365f57c4881e77307bdea56db3e1b78e28ae687e5346daf1e71fe8df3388329ef6e7c90377555367267719e42e9c7f752da5b897e731bd9ca50a581
```

### `dpkg` source package: `shared-mime-info=2.1-2`

Binary Packages:

- `shared-mime-info=2.1-2`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.1-2.dsc' shared-mime-info_2.1-2.dsc 2223 SHA512:292d45d7847f5b6de7583f6c24c5ef019169e1bc6b54e5415d2dc0df203136624b7eb3e20040019608fe392468967c31e15d100f9eaa75e052d342d2aa1465c9
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.1.orig.tar.xz' shared-mime-info_2.1.orig.tar.xz 5202496 SHA512:87e308281e83c4cf889594f7c2e8dcb4d0d0d3910124c3816fdb886ba7d6113b2581711adcb17032b47f9b8d8b7001fab58daa52b7da7c0ef87915e341d6f1b0
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.1-2.debian.tar.xz' shared-mime-info_2.1-2.debian.tar.xz 11304 SHA512:833518eb333d0bb03018299db5e21b5e9f38d9c89680f86aab9e03289ef7d056ff74b3bdb5f7fb364f990b61bc8f264f2b4113edf59ecb1ef7c72f83970f1a25
```

### `dpkg` source package: `shine=3.1.1-2`

Binary Packages:

- `libshine3:amd64=3.1.1-2`

Licenses: (parsed from: `/usr/share/doc/libshine3/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris shine=3.1.1-2
'http://archive.ubuntu.com/ubuntu/pool/universe/s/shine/shine_3.1.1-2.dsc' shine_3.1.1-2.dsc 1999 SHA512:466912ba69f9dbda61310cba4cd37826b0347d4c0884e236217b8ce1af29e2ac4dffa84d2751c62c072a10e08cb55c19857a53a8476c21980c58d98bf22e8932
'http://archive.ubuntu.com/ubuntu/pool/universe/s/shine/shine_3.1.1.orig.tar.gz' shine_3.1.1.orig.tar.gz 940443 SHA512:57b017d22b373507844870ea5837962488f4a0e2238df7b79c837df0aa8f7304ba82d8d7f55d47980b854518f8e34aa55a9fa40f6260650fd7d23f5a94cd4484
'http://archive.ubuntu.com/ubuntu/pool/universe/s/shine/shine_3.1.1-2.debian.tar.xz' shine_3.1.1-2.debian.tar.xz 3624 SHA512:b9771608b85e600edf95fa680350a6634e835e85bbe55a1853a0e1481b1a0bb82a0fcd5d78ba308f6c662b04f29d1e5c156fc7d727ecc04bf92421e7593e2390
```

### `dpkg` source package: `slang2=2.3.2-5build4`

Binary Packages:

- `libslang2:amd64=2.3.2-5build4`

Licenses: (parsed from: `/usr/share/doc/libslang2/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris slang2=2.3.2-5build4
'http://archive.ubuntu.com/ubuntu/pool/main/s/slang2/slang2_2.3.2-5build4.dsc' slang2_2.3.2-5build4.dsc 2353 SHA512:91d45c66a3dad3d3de29dd13e1e81f0f99e4ab15444a4b718082113649ce3cec438903c30625f52c16b6458fc45bd116802bb5f0686bbc8d5414eacee0cf2cb5
'http://archive.ubuntu.com/ubuntu/pool/main/s/slang2/slang2_2.3.2.orig.tar.xz' slang2_2.3.2.orig.tar.xz 1309848 SHA512:e0583b159719cd5e63cc39e3a9a8781ec5f8ceba28272efd964e883a4d2f775fb4244c55e4bc32b131ea9cd4eb2447024ef3c480a14d1dcab4d248ebc8f8b7f9
'http://archive.ubuntu.com/ubuntu/pool/main/s/slang2/slang2_2.3.2-5build4.debian.tar.xz' slang2_2.3.2-5build4.debian.tar.xz 22292 SHA512:3a50252679db411264fc7340a1fbbf6e93b3860b7eee3bbc79fd9923193531c15b66e8781bffdd7b5f45d5b45c84ccc00575bab9d7409ba9287d960b2f086235
```

### `dpkg` source package: `snappy=1.1.8-1build3`

Binary Packages:

- `libsnappy1v5:amd64=1.1.8-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris snappy=1.1.8-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/s/snappy/snappy_1.1.8-1build3.dsc' snappy_1.1.8-1build3.dsc 1928 SHA512:75c713c7c54d7bea939133af5abf33549f3c21b57176040ad8c4cf4d94cd0f567020732b7dfe995bc6f1f80626a0eefb20e7410629d25c34ccd6c487435c446c
'http://archive.ubuntu.com/ubuntu/pool/main/s/snappy/snappy_1.1.8.orig.tar.gz' snappy_1.1.8.orig.tar.gz 1096137 SHA512:efe18ff1b3edda1b4b6cefcbc6da8119c05d63afdbf7a784f3490353c74dced76baed7b5f1aa34b99899729192b9d657c33c76de4b507a51553fa8001ae75c1c
'http://archive.ubuntu.com/ubuntu/pool/main/s/snappy/snappy_1.1.8-1build3.debian.tar.xz' snappy_1.1.8-1build3.debian.tar.xz 5808 SHA512:fb08004f3b67ef9a2b6e260d9db748b414b7327a42e7c659187e6bfce44196a567c6ab23531ee58a8cb79869898770c0fc8a64edb2a8cbd3fca4ccd845bb7344
```

### `dpkg` source package: `sndio=1.8.1-1.1`

Binary Packages:

- `libsndio7.0:amd64=1.8.1-1.1`

Licenses: (parsed from: `/usr/share/doc/libsndio7.0/copyright`)

- `ISC`
- `ISC-packaging`

Source:

```console
$ apt-get source -qq --print-uris sndio=1.8.1-1.1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sndio/sndio_1.8.1-1.1.dsc' sndio_1.8.1-1.1.dsc 1927 SHA512:8cc0bc506717bac415decc63ad6972fcdd3416ce1dcbb38de7048bbc88be85c2a5034b3e7dab8a65aec4c45a02e82862d19246c394b57deb8a6914e34920d5c8
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sndio/sndio_1.8.1.orig.tar.gz' sndio_1.8.1.orig.tar.gz 155821 SHA512:4affeac5758768f9ebf7d823b8d2287695ff02bb4a990474412ab96cb8eef3784c19436a130efb4f7a204193ad479c0086f9bff7b3ac69e6077692dffaa62658
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sndio/sndio_1.8.1-1.1.debian.tar.xz' sndio_1.8.1-1.1.debian.tar.xz 6572 SHA512:748fdca82ffefe9f090727303ae9160012862c16ffbf4eb6ef62285130f37818f6b817d2a880000ebeef0eee39888c0e14d06fc46cb7378708f70ab73f8cf16f
```

### `dpkg` source package: `sord=0.16.8-2`

Binary Packages:

- `libsord-0-0:amd64=0.16.8-2`

Licenses: (parsed from: `/usr/share/doc/libsord-0-0/copyright`)

- `BSD-3-clause`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris sord=0.16.8-2
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sord/sord_0.16.8-2.dsc' sord_0.16.8-2.dsc 2501 SHA512:dd05985e716536504459dfe3fa006fa1e6ae46fad540aff3dd6a4da04d8974ddcb40e4262568ec56fb4b7ff774703b383eb61c390873e29ff8842caf99637928
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sord/sord_0.16.8.orig.tar.bz2' sord_0.16.8.orig.tar.bz2 525038 SHA512:24ed50de8e5bb321e557bac6d3e441b2ed49adabf828bf0e1b33a080c89306dde80443dc8b563098fcc184c4d6e53b7e716b523ddccdf56d08301d1b0120f2b2
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sord/sord_0.16.8.orig.tar.bz2.asc' sord_0.16.8.orig.tar.bz2.asc 833 SHA512:2820018bc7c8bf80da15611b84ae6ce7779462f2fad33269df9388431f8d7ec7bbae1c939c7cf44d58271029b7a873b4d4d7757bd0e0a8e0bf1acf2e35b0b078
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sord/sord_0.16.8-2.debian.tar.xz' sord_0.16.8-2.debian.tar.xz 12036 SHA512:e0ca78cc289e6d3758d6da394954e600a2b4ab0aa2fc6a2d73a0c339444c574b769a772f2a3d0ecb47f950949af361b047e28f5e0b823f802806e4e4a15f3292
```

### `dpkg` source package: `speex=1.2~rc1.2-1.1ubuntu3`

Binary Packages:

- `libspeex1:amd64=1.2~rc1.2-1.1ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris speex=1.2~rc1.2-1.1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/s/speex/speex_1.2%7erc1.2-1.1ubuntu3.dsc' speex_1.2~rc1.2-1.1ubuntu3.dsc 2323 SHA512:a79d04da6f7214895570a993ce08a34e7cb0a1d546e7656f6ee60236b7a91b7cf9a3e509154c11e9d2fbae94a49c150d49f0caea09bf2a38ee0da1e258daea6e
'http://archive.ubuntu.com/ubuntu/pool/main/s/speex/speex_1.2%7erc1.2.orig.tar.gz' speex_1.2~rc1.2.orig.tar.gz 1069339 SHA512:b523803dd2c024c20f992e8410421719c53981df3ff1c1d96bc030baddaf4729ee6a5172b8501f4c9a3194e4dafab8b79814d90624e8226bf869605505cc0bce
'http://archive.ubuntu.com/ubuntu/pool/main/s/speex/speex_1.2%7erc1.2-1.1ubuntu3.diff.gz' speex_1.2~rc1.2-1.1ubuntu3.diff.gz 11094 SHA512:453cebbe297a84da73f22d2eba948438560d645a2fd2b311de9d6f0162954000f23edb96a70033d5c766ee777970ac8cd72852e9e32510cf43332e07a045f21b
```

### `dpkg` source package: `sphinxbase=0.8+5prealpha+1-13build1`

Binary Packages:

- `libsphinxbase3:amd64=0.8+5prealpha+1-13build1`

Licenses: (parsed from: `/usr/share/doc/libsphinxbase3/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-beyond`
- `BSD-3-clause`
- `BSD-3-clause-carnegie`
- `GPL-2`
- `GPL-2+`
- `lucent`
- `u-o-tennesee`

Source:

```console
$ apt-get source -qq --print-uris sphinxbase=0.8+5prealpha+1-13build1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sphinxbase/sphinxbase_0.8%2b5prealpha%2b1-13build1.dsc' sphinxbase_0.8+5prealpha+1-13build1.dsc 2652 SHA512:cc564f25368b63cd7f021cb87d2ff0e7f115de4c96cda7923618ad5b12b42dea2e646fcd4f1542922fb33b6358200242f385b3e5835022f4f69cf0a88478b7b8
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sphinxbase/sphinxbase_0.8%2b5prealpha%2b1.orig.tar.gz' sphinxbase_0.8+5prealpha+1.orig.tar.gz 3401241 SHA512:9d999d0b9041c0965ff679636e3c5705987b70317a353916f447809a916878d831a82a5d9c1476d304f908df1ce6b68eb07c906af4f7b86ab84b859ee1b0d20b
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sphinxbase/sphinxbase_0.8%2b5prealpha%2b1-13build1.debian.tar.xz' sphinxbase_0.8+5prealpha+1-13build1.debian.tar.xz 15508 SHA512:7ea64faf18f2e054a2d39215e0d5ae8ba5ac64677a7bbdec04c1d6a804d8c84fa77120f8cefb71a3e7d5c48199397df1ace77154c61c15948e77cbe8f525a0f6
```

### `dpkg` source package: `sqlite3=3.37.2-2ubuntu0.5`

Binary Packages:

- `libsqlite3-0:amd64=3.37.2-2ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.37.2-2ubuntu0.5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2-2ubuntu0.5.dsc' sqlite3_3.37.2-2ubuntu0.5.dsc 2602 SHA512:fb731fd5ca44dbfa72f1b685980fc3cc66379f63fe0220460897f142eb91d43f81a2c1180864695157b764c22787621c958b0c2448d7ab820c1638cc7ad5f97d
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2.orig-www.tar.xz' sqlite3_3.37.2.orig-www.tar.xz 5694016 SHA512:577e34b4ae18a3c73be6d955a2e2321e993f61decefbcca5112170072ea556eca93dcf55f3059fbcd96147124442b368150de7f68c603e84b80cbe0228ae78f8
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2.orig.tar.xz' sqlite3_3.37.2.orig.tar.xz 7623768 SHA512:dfa51b0a32ab0597cd00ae7abdb53bb255102f397ff8409f3fdbefaad17bc7d5a25f53db90bed47feb1bf4a9a1a4707bc40440c6c5303f3ef5c49ded61558fed
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2-2ubuntu0.5.debian.tar.xz' sqlite3_3.37.2-2ubuntu0.5.debian.tar.xz 33900 SHA512:47c8ee60e8f1b05eb8156a58ea6e909755895df5db9a7381fa8c9f79e7bd6b9a5e6d8f3fd39446d371485ac5feff5b4ac28ff97b4cea92de912de15b7c728e26
```

### `dpkg` source package: `sratom=0.6.8-1`

Binary Packages:

- `libsratom-0-0:amd64=0.6.8-1`

Licenses: (parsed from: `/usr/share/doc/libsratom-0-0/copyright`)

- `BSD-3-clause`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris sratom=0.6.8-1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sratom/sratom_0.6.8-1.dsc' sratom_0.6.8-1.dsc 2426 SHA512:e771c00ee9e7c1e251888c758b9eded9d39a4231adac94d0f7b81c7f3181c5fcaeb0167b0a943faf6a23ffd79cc4b982be547b41273b227365b34712c6388b1d
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sratom/sratom_0.6.8.orig.tar.bz2' sratom_0.6.8.orig.tar.bz2 327027 SHA512:49ec4b230a72005ab7a7a3de0bfa630a27a16f9f811ca8e7f6da7fcf6b34526577217075d428a993f95b813dd2a82a9b6892eeb2e36b66b122ada778fbb3fb95
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sratom/sratom_0.6.8.orig.tar.bz2.asc' sratom_0.6.8.orig.tar.bz2.asc 833 SHA512:8ef579af8bb4067f963d7c1bc87b1a579cd059dac0c5c19007b3dcf5a21d4cdb2d36d22741622b8ccdcbca94422a227e6f882d9f16f3e109e968136767394998
'http://archive.ubuntu.com/ubuntu/pool/universe/s/sratom/sratom_0.6.8-1.debian.tar.xz' sratom_0.6.8-1.debian.tar.xz 10664 SHA512:836c700526e1dc8bf217517a7fc900859c9ec7a54862f3c6f7b47afd324d669b24f3955cf437c323a4a4e3ce360799c1e4b02a10f4f6fad028f25f6acae260ef
```

### `dpkg` source package: `srt=1.4.4-4`

Binary Packages:

- `libsrt1.4-gnutls:amd64=1.4.4-4`

Licenses: (parsed from: `/usr/share/doc/libsrt1.4-gnutls/copyright`)

- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-2.0`
- `Zlib`
- `unlicense`

Source:

```console
$ apt-get source -qq --print-uris srt=1.4.4-4
'http://archive.ubuntu.com/ubuntu/pool/universe/s/srt/srt_1.4.4-4.dsc' srt_1.4.4-4.dsc 2322 SHA512:e07572dd53c7151f3a6d2d98f9893540b0a7dba36637377d1594cfd2888ed0ed66c823d020fd19140918beba26a655ced43c7133b90c937d58a64a5102680e87
'http://archive.ubuntu.com/ubuntu/pool/universe/s/srt/srt_1.4.4.orig.tar.gz' srt_1.4.4.orig.tar.gz 1649283 SHA512:0d51e0ef73f4aa7eb284288cdbbd75b1c161969c2c2fed3a6d4e13a931341ca41dfcf2d6c1b9728f72b43454a9fde3764da67a27af9f0c99a6818682e4f4d4ba
'http://archive.ubuntu.com/ubuntu/pool/universe/s/srt/srt_1.4.4-4.debian.tar.xz' srt_1.4.4-4.debian.tar.xz 14784 SHA512:73c418a33b1fe4b4808b3fefb6d364bf5c244a8070fc315219cc3be5a9e04abdf3f33f6dbc806bb8a93436febbbfc60d4b9f57caeb5b9cdde4537df27e5e3de0
```

### `dpkg` source package: `suitesparse=1:5.10.1+dfsg-4build1`

Binary Packages:

- `libcolamd2:amd64=1:5.10.1+dfsg-4build1`
- `libsuitesparseconfig5:amd64=1:5.10.1+dfsg-4build1`

Licenses: (parsed from: `/usr/share/doc/libcolamd2/copyright`, `/usr/share/doc/libsuitesparseconfig5/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-2-clause-lagraph`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `permissive`
- `permissive-2`

Source:

```console
$ apt-get source -qq --print-uris suitesparse=1:5.10.1+dfsg-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/s/suitesparse/suitesparse_5.10.1%2bdfsg-4build1.dsc' suitesparse_5.10.1+dfsg-4build1.dsc 3248 SHA512:bc57106f5fd1999143e81ed4d5380f74e2e844796b0be2a0e47b9dd542748ed2af9c0e7c7d226bb930162f413736e2963a70856feb305dad33fafbf8d4c83f4b
'http://archive.ubuntu.com/ubuntu/pool/main/s/suitesparse/suitesparse_5.10.1%2bdfsg.orig.tar.xz' suitesparse_5.10.1+dfsg.orig.tar.xz 38256808 SHA512:57e155aa58e7463206aed1846da73194842d0717c4c1c94ab33f412c4a70c262cd83ae0fed77c4d5af8f9d5825d19fe30b7374d4807715dc78605c031d2f682f
'http://archive.ubuntu.com/ubuntu/pool/main/s/suitesparse/suitesparse_5.10.1%2bdfsg-4build1.debian.tar.xz' suitesparse_5.10.1+dfsg-4build1.debian.tar.xz 23168 SHA512:56f5c555ebc8faed35998582edd66ea1068b5846cf488d0ebefd16f0b43eeeebf1878990e5000aca2635f5aca33dcda996e6b69eefe27dc5b2a92c8c8b090e72
```

### `dpkg` source package: `systemd=249.11-0ubuntu3.17`

Binary Packages:

- `libsystemd0:amd64=249.11-0ubuntu3.17`
- `libudev1:amd64=249.11-0ubuntu3.17`

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
$ apt-get source -qq --print-uris systemd=249.11-0ubuntu3.17
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_249.11-0ubuntu3.17.dsc' systemd_249.11-0ubuntu3.17.dsc 5907 SHA512:083cd0d255916c4752afc9d0ca867376727788c9acedf65f731c24a6dd5ca49f8fe6d68ea59be6f4a590d7807cfc34cb52b4a588b9cb98407f36878b32b8ec6a
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_249.11.orig.tar.gz' systemd_249.11.orig.tar.gz 10622702 SHA512:fed7f81933648945a4bfac9fb12150ecd84d32181f79be0e14e0b3a789343a87569f868670e0b8dfc2801fab39f7490f95ee8c29ba831d7611f78c14ace5ddd8
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_249.11-0ubuntu3.17.debian.tar.xz' systemd_249.11-0ubuntu3.17.debian.tar.xz 262436 SHA512:c8d14b5c6dd6396dafaaa9acfa6ce65297b8ca63869cc97cda98ff3f8e9ecf6daa2d2696e16eb7e780a3429f508457fa5dae6a34c9ba75a4f44dc3d1840cae2a
```

### `dpkg` source package: `sysvinit=3.01-1ubuntu1`

Binary Packages:

- `sysvinit-utils=3.01-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.01-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.01-1ubuntu1.dsc' sysvinit_3.01-1ubuntu1.dsc 2138 SHA512:650c939b7af5189cddf6509dd2b6a995c7b389ab4ee33bdad267d8c2b5b5506716b03e512563ed3e3265b32d2d1a9119ee0193f3dc82354896029ae124d2a276
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.01.orig.tar.xz' sysvinit_3.01.orig.tar.xz 126400 SHA512:d3b197fcfccfbc2ad95fe208fb37ed1fcc8173a7a0254528c0d8c6800b054d96e20b48274c55137f19305c105700c35974d454b4bbf5e51fbbf5c082d562167b
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.01-1ubuntu1.debian.tar.xz' sysvinit_3.01-1ubuntu1.debian.tar.xz 131304 SHA512:4c835855b58742480284b17959d54b8ac734466fc87321ddf021b61bb3e38b58aab6d07a7f27f09c0b109b4e442c0dce4d797feccce2884f5b401e13abf73554
```

### `dpkg` source package: `tar=1.34+dfsg-1ubuntu0.1.22.04.2`

Binary Packages:

- `tar=1.34+dfsg-1ubuntu0.1.22.04.2`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.34+dfsg-1ubuntu0.1.22.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1ubuntu0.1.22.04.2.dsc' tar_1.34+dfsg-1ubuntu0.1.22.04.2.dsc 1829 SHA512:e716a22f84cf0ebc0250a4ebb5d7c1fb5f055470a376c20d37a9378e85535aba8d547b6fe64df17bdedd5130d47647613dd5f2083f93cae934961b1b5ba37077
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg.orig.tar.xz' tar_1.34+dfsg.orig.tar.xz 1981736 SHA512:ec5553c53c4a5f523f872a8095f699c17bf41400fbe2f0f8b45291ccbaf9ac51dea8445c81bd95697f8853c95dcad3250071d23dbbcab857a428ee92e647bde9
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1ubuntu0.1.22.04.2.debian.tar.xz' tar_1.34+dfsg-1ubuntu0.1.22.04.2.debian.tar.xz 20544 SHA512:9840407a1364154c831665c3f1739c80a84806567fe5ad27ee3ac70f4c18e27d7f2f9e0557b6e2a634ab39449a8fc95b96f1813f5c203df8ece5226a6afe8c7c
```

### `dpkg` source package: `tiff=4.3.0-6ubuntu0.12`

Binary Packages:

- `libtiff5:amd64=4.3.0-6ubuntu0.12`

Licenses: (parsed from: `/usr/share/doc/libtiff5/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.3.0-6ubuntu0.12
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.3.0-6ubuntu0.12.dsc' tiff_4.3.0-6ubuntu0.12.dsc 2581 SHA512:60e65cbaeae1c7401506d4aa79bb2b3f870c429152cdd9337e00c1e7134759a71850c0a5af75800285ac1b2b91dda43697c79f284a6230276beb0def259ac591
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.3.0.orig.tar.gz' tiff_4.3.0.orig.tar.gz 2808254 SHA512:e04a4a6c542e58a174c1e9516af3908acf1d3d3e1096648c5514f4963f73e7af27387a76b0fbabe43cf867a18874088f963796a7cd6e45deb998692e3e235493
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.3.0.orig.tar.gz.asc' tiff_4.3.0.orig.tar.gz.asc 488 SHA512:115a4c5714b52d0fbea800c494d83c8a96b70b2c9ce84a8df03205d9afc517faa17963f5f9508c013d7d3e2be6675b84b594a771a829406473234c4bd85e469e
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.3.0-6ubuntu0.12.debian.tar.xz' tiff_4.3.0-6ubuntu0.12.debian.tar.xz 53444 SHA512:1f62ce006a8c5161b142dac9266f99de54ce9c21059a01f2c49bf7a9d7c36214bc85ab1a2a8c3355807f8c8733af89a8a2a2180dc745e1bcb7520216d137bd55
```

### `dpkg` source package: `twolame=0.4.0-2build2`

Binary Packages:

- `libtwolame0:amd64=0.4.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libtwolame0/copyright`)

- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris twolame=0.4.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/t/twolame/twolame_0.4.0-2build2.dsc' twolame_0.4.0-2build2.dsc 2180 SHA512:a44239f7e5f9ada0dc9fe0113b02739bce58a3ef110a89c3647362e2b831971a90d96a2914797c08770b8638d13f6e7007ba1d2d2ca70c3b5fe10ad5f5ec318b
'http://archive.ubuntu.com/ubuntu/pool/main/t/twolame/twolame_0.4.0.orig.tar.gz' twolame_0.4.0.orig.tar.gz 890908 SHA512:cc594bc8d2322922280f915a3c0aa52540cca0350d6498bc96f3f60fd6e53f951e775ea015a44bdb29ec883b46b31a0e5483f6a5c188b02e30008289273c7d03
'http://archive.ubuntu.com/ubuntu/pool/main/t/twolame/twolame_0.4.0-2build2.debian.tar.xz' twolame_0.4.0-2build2.debian.tar.xz 4944 SHA512:1eefc13508c60de81ac1e604ccc43f7fe92eb5b6031b65846138ae53ff31df2080ab9a47a4f1f0a24a93b5ab13256d48a1ebebf4bbd23911335d05bc5fe82a44
```

### `dpkg` source package: `tzdata=2025b-0ubuntu0.22.04.1`

Binary Packages:

- `tzdata=2025b-0ubuntu0.22.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-0ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.22.04.1.dsc' tzdata_2025b-0ubuntu0.22.04.1.dsc 2541 SHA512:7e9735cd0230941067895eb4ba5ccbe881347e1114c0dcae4def86a35e66d5bbdbc35cf2d7e26936cbbe4aec1f45d546caf4d7a16143eab6ec4c3bab0dc0d280
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA512:7d83741f3cae81fac8131994b43c55b6da7328df18b706e5ee40e9b3212bc506e6f8fc90988b18da424ed59eff69bce593f2783b7b5f18eb483a17aeb94258d6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA512:ad39fe16b32fad7eee27ff968b4e8af23267ce586629ad70e7625136d2c3cc3a42295a87b3dc770c291aa9112c56301629c1fe379735f70008e62864ce4e735a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.22.04.1.debian.tar.xz' tzdata_2025b-0ubuntu0.22.04.1.debian.tar.xz 181492 SHA512:0acbc2b6326c9b51bc10dec5cb28cfa2b66346620755388fe5ce7d87edf4e4f435804c696c7f635bea15e0d306302be789c8f8f5f65cd3b2437b3d2dd21a80c2
```

### `dpkg` source package: `ubuntu-keyring=2021.03.26`

Binary Packages:

- `ubuntu-keyring=2021.03.26`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2021.03.26
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2021.03.26.dsc' ubuntu-keyring_2021.03.26.dsc 1855 SHA512:7502f4f4d9a288fab9fb84b6ae5f8500cb3f14c68ed586b489dee95f12087b232bcecd9369e98258bb710afda50e5672dfbc6422b1436e896fb529dec8832252
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2021.03.26.tar.gz' ubuntu-keyring_2021.03.26.tar.gz 34529 SHA512:04a76e2bfa88fb428face9e01976ff98a3a26fe2b555340c14200fc6099ee3b474a6733486cedfe933933c0a6826ee3550660499d7b26bda8a27a620b1d6a35f
```

### `dpkg` source package: `ucf=3.0043`

Binary Packages:

- `ucf=3.0043`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0043
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043.dsc' ucf_3.0043.dsc 1423 SHA512:666851d1df82352f8b2be8b8760250cfa1f7635718f0f1598a3d9e9f11a9d687ec4cfb7f6bf950b194d771db039508b6d62c288f53078e2712580bda7b5befa7
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043.tar.xz' ucf_3.0043.tar.xz 70560 SHA512:693209ea06a63279278ac8f63e70fe151880f7c51d54c91ad5e846449f883d5893658d8c6932553d70da4e56ebae3ef67c0eda8593b0768f5979849c79f89f27
```

### `dpkg` source package: `unzip=6.0-26ubuntu3.2`

Binary Packages:

- `unzip=6.0-26ubuntu3.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-26ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-26ubuntu3.2.dsc' unzip_6.0-26ubuntu3.2.dsc 1811 SHA512:9339b501ce82f43a9b04655a0ee1534332972b4b42365245812aeeaf1258417695a82db6446dc5c4d630c8df7119fbc9026bd4a91dc3bd5829596075c19fdf10
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-26ubuntu3.2.debian.tar.xz' unzip_6.0-26ubuntu3.2.debian.tar.xz 28676 SHA512:996f43dcb28f8b3cd4b16ecb35d19c1bb568f249320a70c07dc1b02bad6657646904683751bfce9d4dbad89241d25924424322f95e48a345acb181fd7577bffb
```

### `dpkg` source package: `usrmerge=25ubuntu2`

Binary Packages:

- `usrmerge=25ubuntu2`

Licenses: (parsed from: `/usr/share/doc/usrmerge/copyright`)

- `GPL v2`
- `GPL-2`
- `later (please see /usr/share/common-licenses/GPL-2)`

Source:

```console
$ apt-get source -qq --print-uris usrmerge=25ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/u/usrmerge/usrmerge_25ubuntu2.dsc' usrmerge_25ubuntu2.dsc 1614 SHA512:2f0ea8dbed8277d1fef2f2c70c0075ce509579161fe2dc3a161919d3015c67caff01aa14ba3df7fa7d6b45ce63dbad48389c418781334d83e308ee16988fa9bc
'http://archive.ubuntu.com/ubuntu/pool/main/u/usrmerge/usrmerge_25ubuntu2.tar.xz' usrmerge_25ubuntu2.tar.xz 12812 SHA512:dac8ccc7e2b75c424990713869f80d62d22e1cd86cb35c1784c7e76a12096b8c3f3000cefb406456f6f5c459d14858e710d426ee11714d1a5e342e04186f8353
```

### `dpkg` source package: `util-linux=2.37.2-4ubuntu3.4`

Binary Packages:

- `bsdutils=1:2.37.2-4ubuntu3.4`
- `libblkid1:amd64=2.37.2-4ubuntu3.4`
- `libmount1:amd64=2.37.2-4ubuntu3.4`
- `libsmartcols1:amd64=2.37.2-4ubuntu3.4`
- `libuuid1:amd64=2.37.2-4ubuntu3.4`
- `mount=2.37.2-4ubuntu3.4`
- `util-linux=2.37.2-4ubuntu3.4`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
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
$ apt-get source -qq --print-uris util-linux=2.37.2-4ubuntu3.4
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2-4ubuntu3.4.dsc' util-linux_2.37.2-4ubuntu3.4.dsc 4550 SHA512:b0d37cbcd57000cf45ad6c6769e51bc0cc81a4ad9f3906e09b7f814a3638db0013c7213847c9c90f519f21896fdb5592a8ea839a1277d4e7629a01f84a535957
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2.orig.tar.xz' util-linux_2.37.2.orig.tar.xz 5621624 SHA512:38f0fe820445e3bfa79550e6581c230f98c7661566ccc4daa51c7208a5f972c61b4e57dfc86bed074fdbc7c40bc79f856be8f6a05a8860c1c0cecc4208e8b81d
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2-4ubuntu3.4.debian.tar.xz' util-linux_2.37.2-4ubuntu3.4.debian.tar.xz 114096 SHA512:8e1a3832d116062881d7823baafcf574cc252490e7e25144efa34cfd65a35b590b454298507940399568716c0ccb9533b01f2c9665f92aa2082d91e5ca8e9c9c
```

### `dpkg` source package: `vim=2:8.2.3995-1ubuntu2.24`

Binary Packages:

- `vim=2:8.2.3995-1ubuntu2.24`
- `vim-common=2:8.2.3995-1ubuntu2.24`
- `vim-runtime=2:8.2.3995-1ubuntu2.24`
- `xxd=2:8.2.3995-1ubuntu2.24`

Licenses: (parsed from: `/usr/share/doc/vim/copyright`, `/usr/share/doc/vim-common/copyright`, `/usr/share/doc/vim-runtime/copyright`, `/usr/share/doc/xxd/copyright`)

- `Apache`
- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-2-clause`
- `BSD-3-clause`
- `Compaq`
- `EDL-1`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OPL-1+`
- `SRA`
- `UC`
- `Vim`
- `Vim-Regexp`
- `X11`
- `XPM`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris vim=2:8.2.3995-1ubuntu2.24
'http://archive.ubuntu.com/ubuntu/pool/main/v/vim/vim_8.2.3995-1ubuntu2.24.dsc' vim_8.2.3995-1ubuntu2.24.dsc 3078 SHA512:336ab46d8e91c95b423623688c87b3cc8f2f77570966bd9ce49dc33d2cc5c6d7bd304cdc35d549426f4ce49605232af95f2c90b1dbfa432a970b5060531c505a
'http://archive.ubuntu.com/ubuntu/pool/main/v/vim/vim_8.2.3995.orig.tar.xz' vim_8.2.3995.orig.tar.xz 10377164 SHA512:2326b3484858c92f55076bcd2336290cc292b35c9a8963e3b14e7140dd1fe36179fe8431d71b0121f8345dac3627c80cd016899aa6120f3354fa882144a28b07
'http://archive.ubuntu.com/ubuntu/pool/main/v/vim/vim_8.2.3995-1ubuntu2.24.debian.tar.xz' vim_8.2.3995-1ubuntu2.24.debian.tar.xz 305600 SHA512:94b96dd570396ae079e0e68d7c485d58ad67c25ecc170c73390c9b10f1bcc55d4363f703d406b566be20f8c4708f290cae54159ef426f499a779b493f28350d3
```

### `dpkg` source package: `wayland=1.20.0-1ubuntu0.1`

Binary Packages:

- `libwayland-client0:amd64=1.20.0-1ubuntu0.1`
- `libwayland-cursor0:amd64=1.20.0-1ubuntu0.1`
- `libwayland-egl1:amd64=1.20.0-1ubuntu0.1`
- `libwayland-server0:amd64=1.20.0-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libwayland-client0/copyright`, `/usr/share/doc/libwayland-cursor0/copyright`, `/usr/share/doc/libwayland-egl1/copyright`, `/usr/share/doc/libwayland-server0/copyright`)

- `X11`

Source:

```console
$ apt-get source -qq --print-uris wayland=1.20.0-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/w/wayland/wayland_1.20.0-1ubuntu0.1.dsc' wayland_1.20.0-1ubuntu0.1.dsc 2687 SHA512:37074c6f0092329291687b6f8b2f63ec8330fa705a641693814b934a9fa29dab47312ca6d347d322d8d2183cc555cca74097b45b274cc4864e2beb79960fe95a
'http://archive.ubuntu.com/ubuntu/pool/main/w/wayland/wayland_1.20.0.orig.tar.gz' wayland_1.20.0.orig.tar.gz 349593 SHA512:2881fe23a80732e4b660ff6e1b01711212d3463d20e3442c381bf7ea34c866c3dbab0b39354f5fb8e29649c4530e74aedb6df668a8b54530593257b8e68be541
'http://archive.ubuntu.com/ubuntu/pool/main/w/wayland/wayland_1.20.0-1ubuntu0.1.diff.gz' wayland_1.20.0-1ubuntu0.1.diff.gz 14532 SHA512:73ecb5c916c30e61352cd6d4a3839d46003fd94c73daadd13cbe2a4f43ada37817c97a74ed73fd614cade863ee0e417d1a8cb8db7cef4a768e56f24424125bd9
```

### `dpkg` source package: `wget=1.21.2-2ubuntu1.1`

Binary Packages:

- `wget=1.21.2-2ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.21.2-2ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2-2ubuntu1.1.dsc' wget_1.21.2-2ubuntu1.1.dsc 2251 SHA512:66aa1cecef80eacb8780fdec1ba9a237e36796a22cfc3fcf4b1b095d2dbd98852c4557e3084dd45022154b4c01d8c9e980dac9239a2e27c717a75413513f8171
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2.orig.tar.gz' wget_1.21.2.orig.tar.gz 5004576 SHA512:3e35f92604486ca459f26df97d392579f1d83a9254519e8ce249b410bacf70dddf716d6caa3b29fd4865163f60410b2b8ad1ca1f7bb3dbb2456386b7647b988d
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2.orig.tar.gz.asc' wget_1.21.2.orig.tar.gz.asc 833 SHA512:c5349ed20902d4e4d76e681b9e14370d5c1f07d1ba9e600a82af67ac24fe79051b3beabbe563e6967c429cc344ee1bc46aff57c1ab0eb2db8d70e907df49c953
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2-2ubuntu1.1.debian.tar.xz' wget_1.21.2-2ubuntu1.1.debian.tar.xz 65124 SHA512:1351dc5b7271f9e5cbf85bc0bbfe36b1645b0dfa4de20940e1dc20c297b43b540c958e4908c54f6e3663fc0d1e6094c1dffb7609ca8baebb842659886f1bdf97
```

### `dpkg` source package: `x264=2:0.163.3060+git5db6aa6-2build1`

Binary Packages:

- `libx264-163:amd64=2:0.163.3060+git5db6aa6-2build1`

Licenses: (parsed from: `/usr/share/doc/libx264-163/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with other exception`
- `ISC`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris x264=2:0.163.3060+git5db6aa6-2build1
'http://archive.ubuntu.com/ubuntu/pool/universe/x/x264/x264_0.163.3060%2bgit5db6aa6-2build1.dsc' x264_0.163.3060+git5db6aa6-2build1.dsc 2402 SHA512:3e9ebb5321f4360365836bc885bf6806a6cd8d0a266a27edf1440557c2361118f81bcade54b8cd7b2f05bb240a9f1dec00c44d49cf6669112d686c3bca7f35ed
'http://archive.ubuntu.com/ubuntu/pool/universe/x/x264/x264_0.163.3060%2bgit5db6aa6.orig.tar.gz' x264_0.163.3060+git5db6aa6.orig.tar.gz 952003 SHA512:72ab03582b177455897f9ce0f9b21dfcb2397325c286a4ef1b5cbf4dedcdf3897765e3bb2ea368bfc7d1f07586b8cce4a73bc6c368919c7a3da8c29e3af5b24f
'http://archive.ubuntu.com/ubuntu/pool/universe/x/x264/x264_0.163.3060%2bgit5db6aa6-2build1.debian.tar.xz' x264_0.163.3060+git5db6aa6-2build1.debian.tar.xz 23500 SHA512:4150c68b7b27c8b9749b78205e77ff5c3521d3c96bbbd7125a0d9f4afcf8c60ea92977856490485571edb2ad65814794901cdc5aefe70909d387e5769bfcfdd4
```

### `dpkg` source package: `x265=3.5-2`

Binary Packages:

- `libx265-199:amd64=3.5-2`

Licenses: (parsed from: `/usr/share/doc/libx265-199/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris x265=3.5-2
'http://archive.ubuntu.com/ubuntu/pool/universe/x/x265/x265_3.5-2.dsc' x265_3.5-2.dsc 2234 SHA512:040a0cc2ffbdc27f45721e3c2dcd233e37e049a639ed399a337e075ce1cd0892fe2d2919e4164e0007bc01de446f05e8515403396f0c4e273f5c0e850fd30c74
'http://archive.ubuntu.com/ubuntu/pool/universe/x/x265/x265_3.5.orig.tar.gz' x265_3.5.orig.tar.gz 1537044 SHA512:230e683239c3e262096ba96246c6f67229a1625d163f86647a411733bb1cf349685858aee3017bce818bb6992448d0abaa9241615a5b620561ce47ecb164f997
'http://archive.ubuntu.com/ubuntu/pool/universe/x/x265/x265_3.5-2.debian.tar.xz' x265_3.5-2.debian.tar.xz 13536 SHA512:13da56dd92cec1f2af147049a690135d2361c12819308f87e09ce2a358e32c032eb7afa83bac6da9c4e881cdfbec970c41790b5ab027a9a5c3aee01e33f69fcc
```

### `dpkg` source package: `xkeyboard-config=2.33-1`

Binary Packages:

- `xkb-data=2.33-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xkeyboard-config=2.33-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xkeyboard-config/xkeyboard-config_2.33-1.dsc' xkeyboard-config_2.33-1.dsc 2390 SHA512:9f9fb54462501e260423c39db1c4d1a90ab307b78d71f01fefca7fb71e4e686af4f5cd043a6b9dee3cf84e31812162e2477e05743c66a65e942fd3b224049f87
'http://archive.ubuntu.com/ubuntu/pool/main/x/xkeyboard-config/xkeyboard-config_2.33.orig.tar.gz' xkeyboard-config_2.33.orig.tar.gz 2733864 SHA512:b2a7aa974cfbbdae9b0d9dce63553fcbc25327d28ac8542ffdf1bfa2dc2725f893d85c4d6868f9d45233827e01e43244c928ae9f2ace68007c8e1b54636127d6
'http://archive.ubuntu.com/ubuntu/pool/main/x/xkeyboard-config/xkeyboard-config_2.33.orig.tar.gz.asc' xkeyboard-config_2.33.orig.tar.gz.asc 488 SHA512:21274c621e1d4973b2c3dd2d42eb5b2defbfbba662089ebb7be4b5c9c1ef1db420e2e0ecafd18d139c7bf4ec8620e47793f1bb623bb8bbb46f7eea9ef6cee554
'http://archive.ubuntu.com/ubuntu/pool/main/x/xkeyboard-config/xkeyboard-config_2.33-1.diff.gz' xkeyboard-config_2.33-1.diff.gz 913399 SHA512:2bc7672993704c56db74db7d1729e003401d49aa67e13996920f12e9beaf0a3726dc831e64c28a3c885a3df6db07704b5d53f899ec625eb9a5ef063145fac597
```

### `dpkg` source package: `xmlsec1=1.2.33-1build2`

Binary Packages:

- `libxmlsec1:amd64=1.2.33-1build2`
- `libxmlsec1-nss:amd64=1.2.33-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xmlsec1=1.2.33-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xmlsec1/xmlsec1_1.2.33-1build2.dsc' xmlsec1_1.2.33-1build2.dsc 2714 SHA512:dc50a6b30e3b5584b2b2148ae7de91b60759967f5016495bc45752e57290988b1a11e335573c6ae9222faf3a7a9a52123458445ef30bd8f4f8742906e6efa6dc
'http://archive.ubuntu.com/ubuntu/pool/main/x/xmlsec1/xmlsec1_1.2.33.orig.tar.gz' xmlsec1_1.2.33.orig.tar.gz 1991955 SHA512:6354554b5cdc0a1389f6991efeac919bea912330b36d3be3d3496d61331e9edd2771786d50d2571a439f62ccfc3bd32be0a50bb5a037c4993aac076ad94b46e8
'http://archive.ubuntu.com/ubuntu/pool/main/x/xmlsec1/xmlsec1_1.2.33-1build2.debian.tar.xz' xmlsec1_1.2.33-1build2.debian.tar.xz 9056 SHA512:465308d0425458e645b6323ba67f94e8678288d9d3709e6dbaa309c47465f0692e776e61a96c11d3a89c65f9d7ce8a81bfc87f77be99377a8bb568eb2b8152ae
```

### `dpkg` source package: `xorg=1:7.7+23ubuntu2`

Binary Packages:

- `x11-common=1:7.7+23ubuntu2`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu2.dsc' xorg_7.7+23ubuntu2.dsc 2095 SHA512:f4befc0dd73c66f56856f16c4dc4051f58af50bd8819469df4bb309817952e00f2f4e29776282f85eeaef18a77fdd42cb1cfcb9a69432c4680b216039b37e480
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu2.tar.gz' xorg_7.7+23ubuntu2.tar.gz 301762 SHA512:379e60ab57cc4f9adbf1f59295fca3930bbd638f4100d08c9f1f78bd6ef063e3396385b841e66389771c4ba5825875d738b9aa4b4dc2e3f79d0537415ac0852a
```

### `dpkg` source package: `xvidcore=2:1.3.7-1`

Binary Packages:

- `libxvidcore4:amd64=2:1.3.7-1`

Licenses: (parsed from: `/usr/share/doc/libxvidcore4/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xvidcore=2:1.3.7-1
'http://archive.ubuntu.com/ubuntu/pool/universe/x/xvidcore/xvidcore_1.3.7-1.dsc' xvidcore_1.3.7-1.dsc 2129 SHA512:812fd97e65e8888956a1aa43def0fa464d0564a3e3d47278ece60a8b119ea9cf110f9deb39887fffd33443fd43fdb02af41707378a6f05432a5f449fb87917b3
'http://archive.ubuntu.com/ubuntu/pool/universe/x/xvidcore/xvidcore_1.3.7.orig.tar.bz2' xvidcore_1.3.7.orig.tar.bz2 698615 SHA512:e2b22e7a7e103af7adcc999d95484f991a0a33df02b912fe042b2e23d2af07381c737d23158dbf0fad770ee680572f86fbe04ab2ef33c81e2e0180ead2acc8ed
'http://archive.ubuntu.com/ubuntu/pool/universe/x/xvidcore/xvidcore_1.3.7-1.debian.tar.xz' xvidcore_1.3.7-1.debian.tar.xz 6464 SHA512:941e9a77a612defe2ff3eb4be39218d139b8d05fa0ee3bcaccaeb46961aee0cac4d608128c1c0348cfcf89c3124e65b7188eb862d81fb390763ce06fa3131e1c
```

### `dpkg` source package: `xxhash=0.8.1-1`

Binary Packages:

- `libxxhash0:amd64=0.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.1-1.dsc' xxhash_0.8.1-1.dsc 1966 SHA512:645799311fdf21568b23134cdf586a54bb32b58639adb8ebc1f5ad26fdfdc485506c87d763133163fde705b2f904d6f01f50e4d13ebec2b476d38e66ded2bf22
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.1.orig.tar.gz' xxhash_0.8.1.orig.tar.gz 171552 SHA512:12feedd6a1859ef55e27218dbd6dcceccbb5a4da34cd80240d2f7d44cd246c7afdeb59830c2d5b90189bb5159293532208bf5bb622250102e12d6e1bad14a193
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.1-1.debian.tar.xz' xxhash_0.8.1-1.debian.tar.xz 4572 SHA512:e59d4fc6f736d3af6f7be3ec64fc1ee4382e917a942e4000159652082e2f73f52ae0f72adb98505ac9bd8894a89800e21c0913ba4b511959f07a2bc84c341920
```

### `dpkg` source package: `xz-utils=5.2.5-2ubuntu1`

Binary Packages:

- `liblzma5:amd64=5.2.5-2ubuntu1`

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
$ apt-get source -qq --print-uris xz-utils=5.2.5-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.5-2ubuntu1.dsc' xz-utils_5.2.5-2ubuntu1.dsc 2593 SHA512:832f11d78286b4838d53b789e70b00462d255ca31c9ba059c0a018e13e546b4407889b8d1efd079bcdd8eb1e9247a970bb6811ec50a19a5af83cec3880b6c5f3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.5.orig.tar.xz' xz-utils_5.2.5.orig.tar.xz 1148824 SHA512:59266068a51cb616eb31b67cd8f07ffeb2288d1391c61665ae2ec6814465afac80fec69248f6a2f2db45b44475af001296a99af6a32287226a9c41419173ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.5.orig.tar.xz.asc' xz-utils_5.2.5.orig.tar.xz.asc 833 SHA512:582864ae306861ede34074ebfd23ab161ad3340ab4a068f727583de2bd2058da70dfe73019f4e70b8267e0e0c62f275da1e23f47d40c0b80038449b0ac335020
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.5-2ubuntu1.debian.tar.xz' xz-utils_5.2.5-2ubuntu1.debian.tar.xz 35108 SHA512:c50c36fe82204f79be5f409c633aae52ae7b5d36fc64f404308372c80c862455c26455ad0dba93877e80db576d80e672314f757a1ed080f200702d47247e9d6e
```

### `dpkg` source package: `yajl=2.1.0-3ubuntu0.22.04.1`

Binary Packages:

- `libyajl2:amd64=2.1.0-3ubuntu0.22.04.1`

Licenses: (parsed from: `/usr/share/doc/libyajl2/copyright`)

- `ISC`

Source:

```console
$ apt-get source -qq --print-uris yajl=2.1.0-3ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/y/yajl/yajl_2.1.0-3ubuntu0.22.04.1.dsc' yajl_2.1.0-3ubuntu0.22.04.1.dsc 2128 SHA512:fd9860f259863cac0a0d66a7a4e11a74903d62e92b5f5e0b41f0af85c0368a51cfdb19f081303d2f31a3476fca8230803338b5f48ca81fd9584509f463ba9ac2
'http://archive.ubuntu.com/ubuntu/pool/main/y/yajl/yajl_2.1.0.orig.tar.gz' yajl_2.1.0.orig.tar.gz 83997 SHA512:9e786d080803df80ec03a9c2f447501e6e8e433a6baf636824bc1d50ecf4f5f80d7dfb1d47958aeb0a30fe459bd0ef033d41bc6a79e1dc6e6b5eade930b19b02
'http://archive.ubuntu.com/ubuntu/pool/main/y/yajl/yajl_2.1.0-3ubuntu0.22.04.1.debian.tar.xz' yajl_2.1.0-3ubuntu0.22.04.1.debian.tar.xz 7220 SHA512:c10468ee8674988f7ce96c9ac41105c736bc6c8dcaa24262d34674077eacb20e6e6c215c27855bdf358c629c2c04db0866aca67fa7431d62f6fb32e6169f15ec
```

### `dpkg` source package: `zeromq3=4.3.4-2`

Binary Packages:

- `libzmq5:amd64=4.3.4-2`

Licenses: (parsed from: `/usr/share/doc/libzmq5/copyright`)

- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-3`
- `LGPL-3.0+ with special exception granted by copyright holders`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris zeromq3=4.3.4-2
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zeromq3/zeromq3_4.3.4-2.dsc' zeromq3_4.3.4-2.dsc 1873 SHA512:35c934b1ee0b0ddc72d76417bd91d823b10e7be8d3ea18941145ce0123de241d8bb056a3412dba06b164c5db58366ff0e195493b03a0d1efc52237e5c3062586
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zeromq3/zeromq3_4.3.4.orig.tar.gz' zeromq3_4.3.4.orig.tar.gz 918193 SHA512:ad828b1ab5a87983285a6b44b08240816ed1c4e2c73306ab1a851bf80df1892b5e2f92064a49fbadc1f4c75043625ace77dd25b64d5d1c2a7d1d61cc916fba0b
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zeromq3/zeromq3_4.3.4-2.debian.tar.xz' zeromq3_4.3.4-2.debian.tar.xz 28400 SHA512:1a4a99c59673812d98f45e275fdfd1946b8d80f666d2214eafa64afff6f7dd49566330db48feb99d21357aba7cd74330a8f7d6e8f8fe29c61f1333456f5a6809
```

### `dpkg` source package: `zimg=3.0.3+ds1-1`

Binary Packages:

- `libzimg2:amd64=3.0.3+ds1-1`

Licenses: (parsed from: `/usr/share/doc/libzimg2/copyright`)

- `GPL-3`
- `GPL-3+ with AutoConf exception`
- `WTFPL-2`

Source:

```console
$ apt-get source -qq --print-uris zimg=3.0.3+ds1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zimg/zimg_3.0.3%2bds1-1.dsc' zimg_3.0.3+ds1-1.dsc 1974 SHA512:ee4e1b84e3c834c7d14f5f9c0cfdc3737945ee7bada445cc0d71aacaaf3384b7867ec34681f62fed852f1c61d6107a18bbb7a4e9d64b004fbc652c81c73fb54d
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zimg/zimg_3.0.3%2bds1.orig.tar.xz' zimg_3.0.3+ds1.orig.tar.xz 195468 SHA512:65e60a29c647e1d24afec99b13959aac3f4eb523c47bbda1d83318bd3db88a1654ab5bf672f4918827767f20b618060ff53263ee5c379a5cf0e0fdc043e02ddd
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zimg/zimg_3.0.3%2bds1-1.debian.tar.xz' zimg_3.0.3+ds1-1.debian.tar.xz 2992 SHA512:ada234420d4957b1099c0b402070a721f8919b77461cedbbde1cf0ae3337d068b0cce458a2a1320a6f23d9640823e91b3e8c910d8c95f9394a2346a0cd8fc2fe
```

### `dpkg` source package: `zip=3.0-12build2`

Binary Packages:

- `zip=3.0-12build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zip=3.0-12build2
'http://archive.ubuntu.com/ubuntu/pool/main/z/zip/zip_3.0-12build2.dsc' zip_3.0-12build2.dsc 1805 SHA512:7823e01e09d57d53aed5b4514137ab95610c8de27c8006795a7d6368a81febd7e6b2ce00b004bce9c1ce6525a85cdea654acd489f97a98caa8eb9a4dc0297fd0
'http://archive.ubuntu.com/ubuntu/pool/main/z/zip/zip_3.0.orig.tar.gz' zip_3.0.orig.tar.gz 1118845 SHA512:c1c3d62bf1426476c0f9919b568013d6d7b03514912035f09ee283226d94c978791ad2af5310021e96c4c2bf320bfc9d0b8f4045c48e4667e034d98197e1a9b3
'http://archive.ubuntu.com/ubuntu/pool/main/z/zip/zip_3.0-12build2.debian.tar.xz' zip_3.0-12build2.debian.tar.xz 8808 SHA512:255c1e91c3c54656b42f8baa027239302de178382f7f3e6eb9d5c2ca5ffd46d35872f7d3bb6d9133c192e068338c1a7ea7f0d62de3c583a4f884cadb58a44818
```

### `dpkg` source package: `zlib=1:1.2.11.dfsg-2ubuntu9.2`

Binary Packages:

- `zlib1g:amd64=1:1.2.11.dfsg-2ubuntu9.2`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.11.dfsg-2ubuntu9.2
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu9.2.dsc' zlib_1.2.11.dfsg-2ubuntu9.2.dsc 2649 SHA512:08f3ca4c6680ddec9532de5e937c39aa891e1c2062e6da65a96aaa060c8111bbb63de6d5c36efd34f4d3892e6e334b50fa2947fde68b3ba276e6645027dd8715
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg.orig.tar.gz' zlib_1.2.11.dfsg.orig.tar.gz 370248 SHA512:92819807c0b8de655021bb2d5d182f9b6b381d3072d8c8dc1df34bbaa25d36bcba140c85f754a43cc466aac65850b7a7366aa0c93e804180e5b255e61d5748de
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu9.2.debian.tar.xz' zlib_1.2.11.dfsg-2ubuntu9.2.debian.tar.xz 60140 SHA512:5e86b01c08d5027fab6682849e6065b750d2aecafe8bd6ca85fd729c1cca88031e46f869e20d0b0483d2a6128eab9754f530d0b25f009b684b18bd6f0e8c4ae8
```

### `dpkg` source package: `zvbi=0.2.35-19`

Binary Packages:

- `libzvbi-common=0.2.35-19`
- `libzvbi0:amd64=0.2.35-19`

Licenses: (parsed from: `/usr/share/doc/libzvbi-common/copyright`, `/usr/share/doc/libzvbi0/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris zvbi=0.2.35-19
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zvbi/zvbi_0.2.35-19.dsc' zvbi_0.2.35-19.dsc 1976 SHA512:924b4f434875eb9b301fc20c48ec4721562981f2f532e706be45551d06888c72cd9c803764f3eeaabcc50c51fb62289f1d4e8e4f0a2f8da5b3984b838bc07b54
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zvbi/zvbi_0.2.35.orig.tar.bz2' zvbi_0.2.35.orig.tar.bz2 1047761 SHA512:3d73eb0a7d05fdf1e3f8a74cc9d4fcb2a0287285904d59230c832f42b91afb072e96bda7e396ef07f268348061a51242925746db124bbb713cf56bdfabdada5d
'http://archive.ubuntu.com/ubuntu/pool/universe/z/zvbi/zvbi_0.2.35-19.debian.tar.xz' zvbi_0.2.35-19.debian.tar.xz 16180 SHA512:2b5845874870be5bec22d5341bbec7d1898b4c8b5987aa26901e16141d52fcc35acee3db8f810cc6ecca03f418e77c636ff0db1aa23e93182a2ead667f58314c
```
