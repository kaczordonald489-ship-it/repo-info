## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:ba3a5b3b2b48154994a4f7695bc318ef6d6a9549ef04ddaa919ea05049e886f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a34bd5c63c5d4d902f50950efd6ce5dca64b1addf6060d5cb0d1249f0cbee543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308f8f8e8e8be830f406d62dc791fd094ace9d9714082e5a38b94de80c022113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7002f3da964c57bd455c7ea9aea032a614f96ad162a44a4e3be7f438517c9a`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 11.5 MB (11540369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfae06b9f53d369e6035db2bb25acc88db5141f15668b9c187df731a53d6330`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0675e38a13a9ae911bed6a859416965f3afb652c0c0bde63d3aa4b7c256fd8`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 90.4 KB (90432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a622e4dd49c0b33475fbc290bee154d0d2fa0f6b39499fc01581d935969bf0`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e40dd2e539b3db456883132b1b1edd605a481e44ded2b819881cb3566719049d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a040ca843f8191579ffafa4b24724273fd39a8d8db116dbf48cb294a674d25ac`

```dockerfile
```

-	Layers:
	-	`sha256:80d0cd2e330fc9bf7aa1ae15a2864ea8ed86232bb2bdabd6bdfc79ab09150396`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 3.6 MB (3607697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44da38342d0de406e284f67ea9541752f7cdaec248b21cc9996fbba57ab3770`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d73b7d2e2e9a0ad75e6d8f2f202ac45c5c90804f7fd491f04759f8c9ab560ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55231f6fa6a70347e96f433340baac503f1e0bc79c0414cf4e2cd569707fe81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:51:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72169edcd3114aed53fcfb33bb985a27c25f0be4ce0b90c7ee3b2602e511eb55`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 11.2 MB (11243763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa6d785888f0c8b41e2b5e14ac04e5cd32dc32e062cef01e52dd756c1b6029`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388b2d36400e3f10c42b37febaa865685b8cea7dfdad772bb4cb4648074b6df6`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c459f79798bb027f6a4cf0b4a000a6cce488b3b3163fe0705ab4981141f549`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 91.2 KB (91186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4117407e6309b71a85ba30e66e465b94f6a37a79cf55f9f2c9dce60d28096c`  
		Last Modified: Tue, 03 Feb 2026 02:52:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1130f85f99e63a69789b6108372d5894b1d29ab420ebaf59267e41ca7a6562ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2abd89ee4f4696f8234059b1d01413d7e73a51ec67b0f521b58b71cd0cab6`

```dockerfile
```

-	Layers:
	-	`sha256:fe2137c73c306d7eb945a76ae5920f36787323e1cb8075c3895577f467340eb2`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 3.6 MB (3617235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375c5dbafd2c21265776eed0de1841a836200f05b1e2f050c3ded17494a3b686`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 16.1 KB (16070 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:09d2a82a7755f31bdc924260b1004d9e18f89b53e70681bf9f52e5d7c38265b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61867112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e26265fed5bec7a6be142173b02f16f7dc8000655ce83cfeb5f076665d6436`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:50:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5e68504863f049552110bc4132aac67ebf9360a9ca0dd44ced1eb7009b5560a2`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 50.0 MB (49988982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4b67206060b17bfa3f7c139d34dc7edde12328d9c0813401b6e218eeb526c2`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 11.8 MB (11784066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12563f627f2b777c32fad8fe06dc8a81cc93f797fecbcabcdd16f1a26568ac2c`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b76f0d68fd4c718faf7b6a1dc01fe7c5addcba58f6273fab12fa8a150f330`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af106d4cc2812bb0918ebbd81516dad845621128fb2918143205c8255f2683f5`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 90.7 KB (90739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894703054bb720e327a2e8882bc8458ade09a154ae2005401bc22f71b7dbb7c`  
		Last Modified: Tue, 03 Feb 2026 02:50:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f3e41fe08d7abe4d29d2ffc0de45275ed7b5ca3b8280228247ca7c0828af736e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08921bcb04326e7d1d3cd578e21a03f61ee55fbb62ab7c207503b48aa6a75322`

```dockerfile
```

-	Layers:
	-	`sha256:7a558ce5ffa36aad5b5023dcfa30033ae66b7efd72b87f4fe8ab2ee6c15257b4`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 3.6 MB (3605637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdc2c6ad005dcf4f986126d621753f79ca7d6682cde71dab23e896c5930c544f`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json
