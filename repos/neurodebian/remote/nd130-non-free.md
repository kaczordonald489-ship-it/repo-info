## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:99e725ba2098d9f5e4ac5df767e2791f2262c541d9d3ce6882a7df90623ca8f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e3189cb38355d9a10e6ee69e26edb6de39b465cd8205913d981661a29d17dc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa59c2c3a955fb01be15b8113061546e9756a4d36c3c7470857ae9c252cc428e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16dc4dbae62748d5ea26ad4fa94cc1e428529554cea8d528dae4b9e632092a3`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 10.3 MB (10290035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f327eeba29be5557be80af3b3e54fb4b66e7f3114688f91d0d1a86e4c984e22`  
		Last Modified: Tue, 18 Nov 2025 05:25:27 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41eef2006d4e3c6079b7b7337b729efde57322b6d767c4c14d885db8d04b5b`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d9879da8be8e094ac028797b0fae41f652046596a4c4ee377662c727affdcd`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 90.2 KB (90243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266c69e3259acfd42f890841b091de6cfd0c84ac1ae6a4b555eecaf76fd850e9`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ddfdbc93c093ddbc557c782dec3add89cf90224b2a180e7e5a71db3a4f8882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e797be24246896583645947ee35f3f7738ecb63481336f5cb31d86c2f4ce8`

```dockerfile
```

-	Layers:
	-	`sha256:6108611c93b32a422b3f74aab105a2735fdd09db8ae15bbd2c08ae8a70670e13`  
		Last Modified: Tue, 18 Nov 2025 08:09:20 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36168299857e7e157d6e02f98dd16e7bb6377db14cc095d6a0b8df02014250c2`  
		Last Modified: Tue, 18 Nov 2025 08:09:21 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cbe051ff9e65e938ef970ed213bed1845e12d099468e69ee359adf3f29216d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d723f4d19be58aaf30cbc45c642741452d891db5e4ce1244af5c7ab9483bd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a505c9bb250d77e4640e96c444c4fac586fc1433c373bbef83a7256e04d6ade`  
		Last Modified: Tue, 18 Nov 2025 03:54:19 GMT  
		Size: 10.1 MB (10073459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904db87cf72b19c511cfe31ac93b95a3ed1ba1f7c9bb7582ee6eb938d2e164d4`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842dfa2696e5c96bc037b37dd0932b97434244d91043450150d9e96bdd37472b`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca400b700bdb23c02eff76b5d0d5caf6a698ebaf8497f19a82b8f417b1b01e`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 90.9 KB (90944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d36449c0d721c1d3cd641f286b2d678c32dcaa57534317626ed05a07c2d19fe`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e09f67ac5afd71c56c4130e2c079060e9181289a300b5159f7fdcc66744b050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72700cb5e900ded97e722e6c8b510c0b93dc64d74713213f9746adc344fea7d`

```dockerfile
```

-	Layers:
	-	`sha256:9c9cb02fac134943ac6de2142d5414212aaa7d7329798636b6a8f64c46838920`  
		Last Modified: Tue, 18 Nov 2025 05:10:07 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52009749de1793d97606f0008b38292d4695967e6cac6f459d6a77f967bde8c8`  
		Last Modified: Tue, 18 Nov 2025 05:10:08 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:df5a33264cb70ceafdfdded5c3985656daf4489cbef1599dc6d616fb55d10d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91d5238a64d084798a94a0f5bbcbab41284c53a2939727b9ef7d026393e446b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c0824538c3115239695f48f023fa765aa984377851b00dc5bda2cfb78f0f4`  
		Last Modified: Tue, 18 Nov 2025 03:02:54 GMT  
		Size: 10.5 MB (10462815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd84fd0f053203220666c2fc0ad3385d5508791dc63fa0de95dda5f7b47034`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43491474c911114c1ea18ff4901547554394f1757ff2be3facef60a2af71163`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5294129b5628e65891a7dd0fe5bd29ff3190e979eb91d98d77278a9614c0085`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 90.6 KB (90617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f592a181d12cc8795e06ae7cd55f2152c4e55653b5a2f8e1d71a65305a29d9`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:488f520ba92c5294e525ab10cdb9145c7b5c9dff6eedbad68ac5de96b13dbf35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b13ba51f807628099a34bcb151c6aa443a39e3bccfb5506b3456315ba489fb8`

```dockerfile
```

-	Layers:
	-	`sha256:a0f61787fb9b6f94344751cfb224a1243f2bf661be7453be08765c8f77bdc249`  
		Last Modified: Tue, 18 Nov 2025 05:10:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07484fba44c1bfedea9943a0c3add1849143bf110d7703773edeec6a8ba5769c`  
		Last Modified: Tue, 18 Nov 2025 05:10:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
