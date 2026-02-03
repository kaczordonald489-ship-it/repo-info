## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:9e594df6bac4c9c0c4daa53c980bb4b3a83e3fa0d293167d551e63d718150e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e3fad9231ad143b2ff8fd64aa94fc567d24640473609aa9e53813ba25514dd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59819618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bb57dc02b437ffa494706757c4e8012b3ca9dc37c95e0eb0a621d87abe9dcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da6bb4121ff52ec24b7b3ca19672a3a6dd5bd671413dade3605ce5d9db5212`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff00c0307437e770f79d7730e90f4fe49614963cc352021322f601722e96861`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8be89556aee6cfbc97cba23e7039718bbfb9e26c495ebeecc6b35befaaca0f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e2e18971c937c3084a9bc87a08e8529f6a4134d0df2863e3a7122cc88202f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 91.0 KB (91017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:77bdc7555a73675a432f3ed42bdd322df51878adcfd7f5430a8078b80b1dff39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee510c4dd9d6ee4305db104fdbbaaaa61cda87948394e49326c32b36e0dda2`

```dockerfile
```

-	Layers:
	-	`sha256:3e9450b0d7b05d40b743a7a02ed1088df21be4b25b167218b0ed71e322282c79`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aaf88d71cb5e6047430224faeccaa93971261590bea6c175d6ab5d6990d57c`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:0c07f5e657cc09b86e2e9d42cfe321237c14a5e56f50e8ddfbd4e883d1df05f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd0e10b4f3310ce286b4442d36b326afc8ee52d43f2fe723ebb88a02ac4ff15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8584529105db32472d0fb905ba0ffd3f044b43449f19a931af68cbff933e6f0`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 10.5 MB (10466733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5467fcd76c4951d6cee5b8fea463953e06cbf6b3499279c34eb9e44fe4a41b`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468da32b58b2c95585f26b570d4c00790c123586d464617db5182bb2a4f019bc`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639673e23612c864203b2e3ffc9651b21dbf4b2aa62f36a7a66ecdf0a75bb6a2`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 90.8 KB (90764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a8babc935e1f8f1e38243dbb223658ef808b3e8c0a544f215cff45d7986f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8d14de849f297db4adf9be12411a7e0ca06be0469961ec5dea52a603352dcc`

```dockerfile
```

-	Layers:
	-	`sha256:1cff4584330b4a198de56e38439573dd2692d53421016a7605697ac702459b73`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c846b8599cc185520df1fabe5df76ae8f9e4cd8995574b29094363d2157ba84`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
