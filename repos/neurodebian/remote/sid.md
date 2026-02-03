## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5736c97073ee74f8f16e62030c34d68ea731f86e107e74b0c781593277e9dbb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:742f81326d6458fc4835788d8fe3317f77b687290629fc738389f12c4814df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9d256c1ca3e4c144c863cc2281316c3cc3eb45088369a88aea3a40a0914ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911d1558a1b3010131d47ee741db0963c889273e31e2a95035fd6cfb9f17c1`  
		Last Modified: Tue, 03 Feb 2026 02:49:21 GMT  
		Size: 11.5 MB (11540410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6309d0a7b6729391c7f1314a74b6b06b07c4646ed52a3d9e7ce4cb11daa5bc`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740384dd13f89422fe1f4638c08fb758dc33e4f5c9810aa0b1d0a69d7fae0bb`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 90.5 KB (90457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e1ba3408ddc3dfef56dc25b1915ff61fc917b613ede0a431592467c4b4864a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba3eb40824aca52a92259785bc8cb173186a6bb1ccb406742f34f2f6ebfec74`

```dockerfile
```

-	Layers:
	-	`sha256:7d69e622a5bfed66bf691b20cdf1aa82f53f6f580b821ab40aec94be47d4d4b1`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 3.6 MB (3607661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7e7edca04a0e1aa36eebfdd3e3f3946a1ce7603207a77681ec83592f931e12`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9f8d97f995caee3f00eabda2e5b2e80dda71f89f30a2aa9880a5822d60e61fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed43c76e582a60593bacd55fe4dcd315ba8213831d318c188385c0990e8cbcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:51:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd35008056e1180ece221c285a1c86c1769a7176cb5d2e594f69e6d206f64ae`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 11.2 MB (11243894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92aab31c07432757e3c05a48406dacbb80522a11812614df8c6a1d9a79a3154`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f8a8c48aa5f798b4c9dd2715c2e97c069e5446870e61c7604c9e8621078cf`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689f86ee7d710aaf5e5f25e6ab2160a673cbeba10275adc492d11b0573243f78`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 91.2 KB (91207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a6e4e155a78bd1cf49dbc0345cedd63cd782f42ca24d03ebbc9eec6770f30589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8d05e0e918a47d8eba4c94f215675f9e099ec13d995e05081385ee0a01f8d`

```dockerfile
```

-	Layers:
	-	`sha256:995820befc47d1c55c6cc54493b19e2c17b2821c3c7a7aecd5c807d813f05460`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 3.6 MB (3617199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93978bff663ff63536a1550e800673779f73f1aa275a88ecc1f1ad05e58bf8c`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:6a90c95db1a2638b60aa36691d3a536024d2108a161f2c5fe47c17d301bb22c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61867005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6f605f6913d479e305f041c7a9b47ccb2ebb97207c2fbb42fd8a3f7c4c3f17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e68504863f049552110bc4132aac67ebf9360a9ca0dd44ced1eb7009b5560a2`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 50.0 MB (49988982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e9787e5aeae5594380d4cbb775abd6fa3ec27c76a2ec4cca5e9405d5336bbb`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 11.8 MB (11784382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778f855abd2e9eba1fb32ff318ee9e04561d33943ad5ee010c23514f44c7f9b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b76d608765aa6285fce58e5f3f7c2d318b20960b933cd4f0f96f93b8350f7e`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4740d9cbf74ca39636ca18c075358ca3fc32195250247fc9c8a961bfbd5437c7`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 90.7 KB (90737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d1e658726c43eec3951bcb02149b6f9ed20f79e8668fbe71937320ed8f4814a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66420441c356368d62eef101d1964d2aa0a638f7076eb7e63133073408c60356`

```dockerfile
```

-	Layers:
	-	`sha256:960074c60cda9620fb77ba8ba0212d8d0ae309978f421b6147062e8f62cfe20e`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3605601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9187b2aaf43c788908a856edf1454a2ea59994c22e7278cf0676b60711104265`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 13.9 KB (13875 bytes)  
		MIME: application/vnd.in-toto+json
