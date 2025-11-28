## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:d346efc1653ce69298b0583c215759f69e4c520b1687b306ae31ee696ee1ca62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c8ead1f42c634e681b9cdac2bf63ba48bc04ef8800d888bbab9ac6bc443233b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9ceed3d827ee121c147b39aee58e02ca8f8f14e9be70c9899aa69c0e4db108`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:24:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f85a9e90a8b30122ba1fd3c2518caa5dfa52bad3467bf81a8895b3ef33d4a`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 11.3 MB (11269784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c5250e45b37b7a4ff8c28cceb975c813e947b0cecc421a569c75cf55bb3c60`  
		Last Modified: Tue, 18 Nov 2025 05:24:34 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193261405425b3c59f2c41fb87d2b4d31680bf8592a977be1caf0a5113b36ae1`  
		Last Modified: Tue, 18 Nov 2025 05:24:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13be725ce53a3aa8771c7b171f351ebd4ed147048d82dc5056b9c1f81e85ac4`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 93.4 KB (93374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0f9162a0042d874a36b09ff302bd44f0f89155feccf6d3f925f58ec54e728`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed9d4c3f6b45fcc01320121fddd661becdf4e23be51c8630c3bccdcb27c45d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ada510161ccd0cbdb6e2b1d71f378cbfe93e95b0896c977ac560e969d2f1c0`

```dockerfile
```

-	Layers:
	-	`sha256:abdc6af02c68406dc3e31ead91fc836045df6d11811540bdc969c352335f9a0c`  
		Last Modified: Tue, 18 Nov 2025 08:08:17 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9eb26d88e694e6a18b0aa1414822b139d8020bb0108bdeb82201e5a65f8b6`  
		Last Modified: Tue, 18 Nov 2025 08:08:18 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:799a9fdaeac12508072ad286af1e4e7af48fdb6b90fa105569d75c585522decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9196b72b4cef17624139168cb8a29ac1a83af665a592f750bb3c2721486de148`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807214d6bb58ce93643f23da0d4f513c5ad5c1d7afbca79b7efed5365942ca8`  
		Last Modified: Tue, 18 Nov 2025 03:52:35 GMT  
		Size: 11.3 MB (11253434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6e4641d306f35a7865dc55f0617616dc6b1fdffcb7dc3efedf0737835a76`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba37d77eb8f27c5b50207c5ded85c692607c6c8731c3646f7aa887fb707d9b4`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f35d356531128f85210ebbce70caffc3b026330c2f6cf599438d5cc6fd6ca6`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 93.5 KB (93515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a21ba5c85c56614c9af83a1aedff34ebaa1eb2f907abf5f9e128f2413b19b7`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed1488b88f01f98361118e77ce3f25f9d4948315e0be7528e934b3f88bfb8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4703273c9e0ef5f78614bb8691d50f70c13a6b84a97abe62174461caddfb7da`

```dockerfile
```

-	Layers:
	-	`sha256:ff89c214db7039e198f750d1504e92a410cfd11dc52faaab1c904d28bfb17e10`  
		Last Modified: Tue, 18 Nov 2025 05:08:52 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb4ebb333c44656c1f30b692d638ce65ab8a9add9573811002d77ae7ef10360`  
		Last Modified: Tue, 18 Nov 2025 05:08:53 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2b8d3d240bdf2e13a28c55a3342b49ba13fc0ceb8366f34fa9cc11f991fb02a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f231018d42fd321a780aaa8de73caa2d59d077695636f36a0cee80ee8f81bd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:01:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:01:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a93d0237e128ad08fcddfd034244077cd71dc323e8c25586ee8ee24728ec4d6`  
		Last Modified: Tue, 18 Nov 2025 03:01:29 GMT  
		Size: 11.7 MB (11690161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff35b78322711c76b309f998cde01420d157ca97747d0dca1c2f1303f2e4c85b`  
		Last Modified: Tue, 18 Nov 2025 03:01:27 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fce1d0ab5d7eed1f6fb618d4f905b41413bb9793db1989d6d8a7329d274744`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe045baa9269b254e517da9ffee8d4ba6c88e789fb777f5c77bc4120b4f6a1`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 93.4 KB (93412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd1f28a6350b9b83efd2d573a2963eda9ec1c308dba86dd4c23ade9b1ee1518`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52ca226625f2cc7d0ec9f3f7a67f8c1a133b4d6d44935fa551176ef9f7c9e27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d398885232ce92f7fdad4175c8954f4a3fafcbfb91f3380e2bcc238b0788425d`

```dockerfile
```

-	Layers:
	-	`sha256:9eae406c595dd9fb241902d88fff47118b84928d56f49314f5e086ef1b4626a5`  
		Last Modified: Tue, 18 Nov 2025 05:08:57 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb0e974253a831d2dc5b7732b8c9a0ea76c6d4ce502ff780e687782910c8a5b`  
		Last Modified: Tue, 18 Nov 2025 05:08:58 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
