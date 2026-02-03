## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:e60e70dd2ecc36918ee4ef7a12501e9a8c5aa4238ec448c3ab89f0565356a8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:62557098c459de418b2e59e2e0374ded8453839c8dc8a8a635e934e25b272fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60289672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e09429446df5077bffdd30968e77332ee3dbad06f3b3bea0d5d4e95d262872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2730c822ebcac3a15d3d766e879e3429b4f9adf6fe76271ccfc76c249537f502`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc7445e516a5d581aed9ea2f12b0eaeed7fb0988a1b7763124e12ff75af87a`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.6 KB (90648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6aed34d51bd5ea07823221ec742d4e2d9232789220b79efe8f13368675e3040f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3787c78d5c00b60dd7bf2b7563d0ab9a1f311b1efe8e20720192ef75f7123075`

```dockerfile
```

-	Layers:
	-	`sha256:5b86a2fd5679538630a28183b3b3ba91097d7d8705bb17616d47cf9348996af0`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d480378322cf7188821388658920d0bdc152a426690dd4aca8e70b9eb5cd12aa`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c3c2279dfef5b1dc5801320cca47e07527c809bfd5b8501e47a54886d752e589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60016699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5303416cf8c75cf18340519a6abdb2c2603976b0e99f7947a44a4386905605d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:51:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe9791138d0a57aaca050f57b565887e667f14821c8231f93c2d0c305c7e471`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 11.2 MB (11243891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c0a9f59ed57dde67760c8b95b1ac9a6e2b6a87a29f3ffe1bb31f968cf15933`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e2416924c6e88fd98b2ecc7ba1069de6c6c9b1579c057f3ace4d1ce181bb26`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4e195e6cd71c46f9c6a5642063ca9d7395067cbc82cec1f6c0c133adfd0a4`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 91.4 KB (91373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e16860a4e030141224640806bb45d2e39341e64caea29bc7a7b88081583ec337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bfffc9dcc54d9ba58efca740fba1097bfef5a19b1896c56713736816def4dd`

```dockerfile
```

-	Layers:
	-	`sha256:172889f9237c9e8233f219895f1fe9b57a489f5bd8800559fb0fa2feda3cf7ab`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 3.6 MB (3618081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cc10f725eb0b8fd8134c1c72a383f9d97018377dc013bed07e8ea5d26e62ec`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:372715dd9d593229a9937c8e98543f99da9162df29c92ca6eac1f1fc5ab78228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61860090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670a3c8d8684fcd47ddc6995df4f4337300ec88be2777020a509d2a71a2a36fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:50:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0e91a2c7873b83c48aa15d9575016025f65009bb2a2697185fc7c1cb3258a`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 11.8 MB (11784286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778f855abd2e9eba1fb32ff318ee9e04561d33943ad5ee010c23514f44c7f9b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b124115f9efbbfa225774d314331b6efc9cb5a56f0297c3b8a3a232389266b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b21d5c5dbc2b33cca4880d981b958ba838908e34a46b81d62441314a5465015`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 91.0 KB (90964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:adb60bd7608494b5e43c5616cf74a0c141d1c97857da108077e02b9a48877c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62470d32ade636f2b7255e3643887b7193c4ef781667ece2d405e4c84592332b`

```dockerfile
```

-	Layers:
	-	`sha256:5d9a2f5cdcd0a0287877961e006e91a56b955f9e17dcbfc60d768d2544743d64`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3606482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f6368f043ceb8e4c5ed5e1a65f2c65f04f6fe87b106c5b112dc5c93161a9a7`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json
