## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:0f18bc1f784f10280a845619e4cb21c545b4bedff88df1e685f5404a23735f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a163bb449af86570efbb2c848f4a56b0a9f75e2c9bab460fac75b282e0ee9659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60290217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ebf1e005f416f00f58c9265e914c41d744ca6aa1cfbeee885ba91c67104b69`
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
# Tue, 03 Feb 2026 02:49:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbb37aa9daedccd57c940309ed43a39d7248abc940a23204d466caa4499871f`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035ddd951380f76413ebc0059b6934df85dc73f566840fbe23db460cfcd656e9`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.7 KB (90675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef19c1eb6c1cbf32f075f42496b94816b18968b15c0f0b69876955199b6719`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14a013c4124a4a318ef9462fba9ce8e7d4f7ade0f5398b9583274cdf91689f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f2134a5a1a99b81c7e83acec3a0283963987a07471c68c3cdf183c9f72d260`

```dockerfile
```

-	Layers:
	-	`sha256:2164015860c8679b1861e5dd23a57a9c9cf4dfe0487d529174fcf93b3b40604d`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cff4e739dd29e441abfa38f38ab0d7eff091449c92875d8627eed5ac223629`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8782f0cbd867e5cbf0a00809d2009fc7d99b9dac92bc8d074fbb25ad4928217b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92256154c8d58a75a4a78ba1066be026d1a4d93461b9883112013f1f315b31d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f011967afc3b9472b0c743cd8832587b7373c1a9e793ef57c52f8e1c2061c`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 11.2 MB (11243869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c36ebd2a34f62d27f0d7cef3ead3d16165f9623f928d1bfe2b41b30f74c828`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac5250fe806def3c12f50acd0b6fe7d6851fec3d0a5e991b2638d7543c0dca3`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d313056e5d16e90d2205cc6d85f4999bb2e91762bf29d6f405fe2a6bec2fe67f`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 91.4 KB (91372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5cbbb997fec7584e04e4b04ed9e8fdbdf6ca498e81490eaa86e4db34a6c603`  
		Last Modified: Tue, 03 Feb 2026 02:51:54 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:94e7098c49dd9439a3e0b5fd3a09d5ec77087becdfd9c3a9a528a18285e3ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4e5d034a0bd7358ad9328e4e08533bdf5014b7277fa2e24279b515eb53b93`

```dockerfile
```

-	Layers:
	-	`sha256:556e59f143cdbd0a487dbeb922c3d70dae2429bed531b17f3c08f7d816f3ad23`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 3.6 MB (3618117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bdedb5ebac73f1c7c14c80ceacc95ed4c954edb869cd21a8abb346bdf0a2d0`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:76db44b9c094c727694409a86d9d46053c182d88334960270e0c32f0cc439d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61860509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfdd9ac4c6dff21718140687ea8b4349667ed4e76bda91b250de02cd621303e`
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
# Tue, 03 Feb 2026 02:50:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c435bc3bbcc2b13bab5e538cf235a937f4a4af7f766c52a475efea971328f83f`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 11.8 MB (11784268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de453593ab8b3ceefaf8d95e35ed8836a37f66dbace8e41451254c44d8f0c8d`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b124115f9efbbfa225774d314331b6efc9cb5a56f0297c3b8a3a232389266b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1864f2cc4b84a441ce01b9bc21922485dea409990a9b34103b645bd80a06f53`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 90.9 KB (90948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcecd183b72d5159137f34d97a72e00182f405589c991bd975f0f5f998d8f0a0`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:35d6816101ce8f76f0bb8cdfcd919c4655940a119331a86e7031cc025cd18677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e1cc49c57572daa393062465301f86970c1cec84f1d7fbd9df4d0baa233c5c`

```dockerfile
```

-	Layers:
	-	`sha256:c78197de2901716faabbc631b5648a6ca556f3490d2677f1df58ce0ad3ffa0eb`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3606518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842ed29984a6b5bb38a099c5776fce07d0557ca96adf412a06ad3ad9508c1747`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
