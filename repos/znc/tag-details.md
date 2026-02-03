<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.10`](#znc110)
-	[`znc:1.10-slim`](#znc110-slim)
-	[`znc:1.10.1`](#znc1101)
-	[`znc:1.10.1-slim`](#znc1101-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.10`

```console
$ docker pull znc@sha256:62997f290c1c0f15b8a750bbf99f2b54f1cd8fb06778d3a0919d921a6770e2a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10` - linux; amd64

```console
$ docker pull znc@sha256:88b2e64fb6cb598237334b490597d3e66617cd3163977cab1a0c910a245d54bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169353457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f181e10b23a159c1263fc75c989efa6feb863c0299a663212f8f1de586b755d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:05 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:42:05 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:42:05 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:42:05 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:42:05 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:05:09 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 04:05:09 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb573624033b64c31ce0b0988dfdf9d3809781fecc6eb2d890f97c3ec0d5c48d`  
		Last Modified: Wed, 28 Jan 2026 02:42:16 GMT  
		Size: 46.0 MB (46023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9d755e36402a7458130d201cdb7310cafde20bbadcaf36b9ee03d15359dd4`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7886e99f614dac17818774c38e82652899389c6c80540e14b901962452a6393`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3dd42643aad23191e7bba9659776bd716342e4a6e8690e587203df5d08525e`  
		Last Modified: Wed, 28 Jan 2026 04:05:33 GMT  
		Size: 119.5 MB (119524282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2aa34d8b0540d44c5b6c45ebc9d65a351e483289bf6256a006dddc7f8c6b0`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:b7cd3d52a41b20d22a063849a8dee9e527a3cf74b18bc17dba3c9d68c2d5bee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6870662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00c0398071892bcf8580088bdc487cb75111e5618790000605018788a73d0ce`

```dockerfile
```

-	Layers:
	-	`sha256:0a4efbfc13e1229f0d6dd65ef0f8a6b827846388c759bb3bb241c01b4e17491b`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 6.9 MB (6861102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de638912f1a49162d380b6cd3aff7c39a98fbd99a73848c8b0422b45863548e9`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm variant v6

```console
$ docker pull znc@sha256:0d79630fa24f3e393db40c3458bbe00f42d73ccf6ad998e28e7d3b7d7c2f7a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148651940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ad51fedc2cc5de17ff6848327d5508ad3134dea322a3e74ed76259f23c09fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:19 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 03:01:19 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 03:01:19 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 03:01:19 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 03:01:19 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 03:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:54:22 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 03:54:22 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a5ce10069fc0bda0f1022fddd396e09f242597ae01c904766c5db3d9ac2675`  
		Last Modified: Wed, 28 Jan 2026 03:01:29 GMT  
		Size: 44.6 MB (44608702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa95cdc37d3c22b71ffa2e62fe167da8d27f8cac4863456b8ac87b005efc46a`  
		Last Modified: Wed, 28 Jan 2026 03:01:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a1261dfb8c36a3cb908db697a44a1d6df7c790de07f2ad174bebf62a602c82`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc42e4d82ff7185bf5dce6b1f34d38a2f4dd413d7d3b202e9c01df58649d2e57`  
		Last Modified: Wed, 28 Jan 2026 03:54:38 GMT  
		Size: 100.5 MB (100536939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff9cb955c967a34bfb0e2613967dec50029b5cee1cc4f9e4c8731439012b1fe`  
		Last Modified: Wed, 28 Jan 2026 03:54:35 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:f532a543bc4bb18ec8901e9f65cc0bf40196d5039fab9f95f14503c6184c6e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6d8e3901fdfc2f8b85fcd1157a2ce8dfc5cd802d75a81da0bca00d493092d1`

```dockerfile
```

-	Layers:
	-	`sha256:50b938328ad302c7bbd804139f5670ae551a8a78cd8da87a9584ee81a1125f36`  
		Last Modified: Wed, 28 Jan 2026 03:54:35 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9e1ed8d23dfc5886288191d77d108d4d2490eb720bda6c6b36231b04719988be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163120109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d65734d3917d9c2b324f54aeb219ddec939f4af1da2a0b839a933570173a909`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:34 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:43:34 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:43:34 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:43:34 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:43:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:43:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:25:07 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 04:25:07 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fb4c06cbae0de216b65841183a7485c5e39161ed699f8ba01c6dd1389c36de`  
		Last Modified: Wed, 28 Jan 2026 02:43:45 GMT  
		Size: 45.8 MB (45819450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a30fe37bce4d1587cc197e216ee533ec899ffc1832d348c7d50d1815192e`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78da196f5453df7f0115960345d64c78156d6778c48d0e0c3b4ca9de154e89`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c966ae1fb836a936092a368a79641536cbea77068188fd2b20818414332283`  
		Last Modified: Wed, 28 Jan 2026 04:25:28 GMT  
		Size: 113.2 MB (113159887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3753fa4a85f3738824c87e47f7ab1a81ab493724c92e41966518618469675e65`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:2cefdcb633bb73487619498b312f9b1cda1ff75915a5be4124d5a0dff0d82311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec15c1bea99d79afbcca863378a1aaf8d9d4f4906c98472ce11c2fb26f5ea5e`

```dockerfile
```

-	Layers:
	-	`sha256:81e34e546355f1c453df3cacfb1eb984b3bb1f0697ed446acb8586a6ecfa63cf`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 6.9 MB (6940526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2843c19abe39f7f5b444b4aaea24cae29c520037b84a496ae849f018bb9e0048`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10-slim`

```console
$ docker pull znc@sha256:83fc51b6b2c2667e8a088918184b8f0ee189790c41aa9a708059ee74aae68d47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10-slim` - linux; amd64

```console
$ docker pull znc@sha256:ad8e8e327b505af17e342fc577d1ac9f1c20a3f89c24dc1464ba2c34da9a6157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49828844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e012dabfe0501c513be0caf416b78fc2b04de0a2da57b66999587629fb5a06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:05 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:42:05 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:42:05 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:42:05 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:42:05 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb573624033b64c31ce0b0988dfdf9d3809781fecc6eb2d890f97c3ec0d5c48d`  
		Last Modified: Wed, 28 Jan 2026 02:42:16 GMT  
		Size: 46.0 MB (46023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9d755e36402a7458130d201cdb7310cafde20bbadcaf36b9ee03d15359dd4`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7886e99f614dac17818774c38e82652899389c6c80540e14b901962452a6393`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:9db841133b3f6208c4f4bf6269d575e6bb61891e9fc174e31c436b2371940759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d15dbc74c08e82fe6c7c81f07f0662576158b09a6e0f5d6e737801d4002f8ba`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf640ab8e140479ad814263b7eb8a593634fb817ef9aedda45a24a2682e02d`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 1.8 MB (1752770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da922eaea3a3579801d40505eb31491006da179392dcfb97ed06ca2af932dad`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:d8fb30755a1833900d80f638fee295d11ead95fadb7bbe506c4d50fb2b8dd5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48114670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a742af07f52e0257541cbdaabd2ba5390624b505f0a494d30df2ec9afac29a6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:19 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 03:01:19 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 03:01:19 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 03:01:19 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 03:01:19 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 03:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a5ce10069fc0bda0f1022fddd396e09f242597ae01c904766c5db3d9ac2675`  
		Last Modified: Wed, 28 Jan 2026 03:01:29 GMT  
		Size: 44.6 MB (44608702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa95cdc37d3c22b71ffa2e62fe167da8d27f8cac4863456b8ac87b005efc46a`  
		Last Modified: Wed, 28 Jan 2026 03:01:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a1261dfb8c36a3cb908db697a44a1d6df7c790de07f2ad174bebf62a602c82`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:f117a2bd503e53266f6c5eb06e9b7d0a890852abdfae825abd4187b2201fa3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd354a399ca5dfa10e2bcce840128924e14f7b90fba3a9b9eee2194236a8e17`

```dockerfile
```

-	Layers:
	-	`sha256:6570a77a84d68fb9174f930283eb195ac66bfc9dc5379411e4bbab29e860028d`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:d8fa210706bad66ced606cd665899bdae4c9fc429bce02af91710b64f5e0dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49959891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498d05018c4bbcbd0385187776e59b0f0fc467f2eca08ce2c274b5f53a05465d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:34 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:43:34 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:43:34 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:43:34 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:43:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:43:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fb4c06cbae0de216b65841183a7485c5e39161ed699f8ba01c6dd1389c36de`  
		Last Modified: Wed, 28 Jan 2026 02:43:45 GMT  
		Size: 45.8 MB (45819450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a30fe37bce4d1587cc197e216ee533ec899ffc1832d348c7d50d1815192e`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78da196f5453df7f0115960345d64c78156d6778c48d0e0c3b4ca9de154e89`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:1f07f787c5d807edd8208ea8bbc48e49d86b5bd27f18583d57c70dcb14fbd17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49190ad5d2830f1789d2739aa0d3bacb1a94b0478b7b042b38d5b42e8660f490`

```dockerfile
```

-	Layers:
	-	`sha256:b1584e0d7ac55f7a901e49e3d7e6fa01e611dae3214260ee0709d66d73e6005b`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 1.8 MB (1752900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc71cdf4d1aaa3453eea03b2b89eb37ec9d7b18de46618059926e2d4a754ac1`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1`

```console
$ docker pull znc@sha256:62997f290c1c0f15b8a750bbf99f2b54f1cd8fb06778d3a0919d921a6770e2a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10.1` - linux; amd64

```console
$ docker pull znc@sha256:88b2e64fb6cb598237334b490597d3e66617cd3163977cab1a0c910a245d54bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169353457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f181e10b23a159c1263fc75c989efa6feb863c0299a663212f8f1de586b755d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:05 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:42:05 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:42:05 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:42:05 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:42:05 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:05:09 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 04:05:09 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb573624033b64c31ce0b0988dfdf9d3809781fecc6eb2d890f97c3ec0d5c48d`  
		Last Modified: Wed, 28 Jan 2026 02:42:16 GMT  
		Size: 46.0 MB (46023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9d755e36402a7458130d201cdb7310cafde20bbadcaf36b9ee03d15359dd4`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7886e99f614dac17818774c38e82652899389c6c80540e14b901962452a6393`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3dd42643aad23191e7bba9659776bd716342e4a6e8690e587203df5d08525e`  
		Last Modified: Wed, 28 Jan 2026 04:05:33 GMT  
		Size: 119.5 MB (119524282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2aa34d8b0540d44c5b6c45ebc9d65a351e483289bf6256a006dddc7f8c6b0`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:b7cd3d52a41b20d22a063849a8dee9e527a3cf74b18bc17dba3c9d68c2d5bee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6870662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00c0398071892bcf8580088bdc487cb75111e5618790000605018788a73d0ce`

```dockerfile
```

-	Layers:
	-	`sha256:0a4efbfc13e1229f0d6dd65ef0f8a6b827846388c759bb3bb241c01b4e17491b`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 6.9 MB (6861102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de638912f1a49162d380b6cd3aff7c39a98fbd99a73848c8b0422b45863548e9`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1` - linux; arm variant v6

```console
$ docker pull znc@sha256:0d79630fa24f3e393db40c3458bbe00f42d73ccf6ad998e28e7d3b7d7c2f7a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148651940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ad51fedc2cc5de17ff6848327d5508ad3134dea322a3e74ed76259f23c09fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:19 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 03:01:19 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 03:01:19 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 03:01:19 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 03:01:19 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 03:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:54:22 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 03:54:22 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a5ce10069fc0bda0f1022fddd396e09f242597ae01c904766c5db3d9ac2675`  
		Last Modified: Wed, 28 Jan 2026 03:01:29 GMT  
		Size: 44.6 MB (44608702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa95cdc37d3c22b71ffa2e62fe167da8d27f8cac4863456b8ac87b005efc46a`  
		Last Modified: Wed, 28 Jan 2026 03:01:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a1261dfb8c36a3cb908db697a44a1d6df7c790de07f2ad174bebf62a602c82`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc42e4d82ff7185bf5dce6b1f34d38a2f4dd413d7d3b202e9c01df58649d2e57`  
		Last Modified: Wed, 28 Jan 2026 03:54:38 GMT  
		Size: 100.5 MB (100536939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff9cb955c967a34bfb0e2613967dec50029b5cee1cc4f9e4c8731439012b1fe`  
		Last Modified: Wed, 28 Jan 2026 03:54:35 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:f532a543bc4bb18ec8901e9f65cc0bf40196d5039fab9f95f14503c6184c6e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6d8e3901fdfc2f8b85fcd1157a2ce8dfc5cd802d75a81da0bca00d493092d1`

```dockerfile
```

-	Layers:
	-	`sha256:50b938328ad302c7bbd804139f5670ae551a8a78cd8da87a9584ee81a1125f36`  
		Last Modified: Wed, 28 Jan 2026 03:54:35 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9e1ed8d23dfc5886288191d77d108d4d2490eb720bda6c6b36231b04719988be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163120109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d65734d3917d9c2b324f54aeb219ddec939f4af1da2a0b839a933570173a909`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:34 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:43:34 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:43:34 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:43:34 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:43:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:43:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:25:07 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 04:25:07 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fb4c06cbae0de216b65841183a7485c5e39161ed699f8ba01c6dd1389c36de`  
		Last Modified: Wed, 28 Jan 2026 02:43:45 GMT  
		Size: 45.8 MB (45819450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a30fe37bce4d1587cc197e216ee533ec899ffc1832d348c7d50d1815192e`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78da196f5453df7f0115960345d64c78156d6778c48d0e0c3b4ca9de154e89`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c966ae1fb836a936092a368a79641536cbea77068188fd2b20818414332283`  
		Last Modified: Wed, 28 Jan 2026 04:25:28 GMT  
		Size: 113.2 MB (113159887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3753fa4a85f3738824c87e47f7ab1a81ab493724c92e41966518618469675e65`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:2cefdcb633bb73487619498b312f9b1cda1ff75915a5be4124d5a0dff0d82311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec15c1bea99d79afbcca863378a1aaf8d9d4f4906c98472ce11c2fb26f5ea5e`

```dockerfile
```

-	Layers:
	-	`sha256:81e34e546355f1c453df3cacfb1eb984b3bb1f0697ed446acb8586a6ecfa63cf`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 6.9 MB (6940526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2843c19abe39f7f5b444b4aaea24cae29c520037b84a496ae849f018bb9e0048`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1-slim`

```console
$ docker pull znc@sha256:83fc51b6b2c2667e8a088918184b8f0ee189790c41aa9a708059ee74aae68d47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10.1-slim` - linux; amd64

```console
$ docker pull znc@sha256:ad8e8e327b505af17e342fc577d1ac9f1c20a3f89c24dc1464ba2c34da9a6157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49828844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e012dabfe0501c513be0caf416b78fc2b04de0a2da57b66999587629fb5a06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:05 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:42:05 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:42:05 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:42:05 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:42:05 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb573624033b64c31ce0b0988dfdf9d3809781fecc6eb2d890f97c3ec0d5c48d`  
		Last Modified: Wed, 28 Jan 2026 02:42:16 GMT  
		Size: 46.0 MB (46023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9d755e36402a7458130d201cdb7310cafde20bbadcaf36b9ee03d15359dd4`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7886e99f614dac17818774c38e82652899389c6c80540e14b901962452a6393`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:9db841133b3f6208c4f4bf6269d575e6bb61891e9fc174e31c436b2371940759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d15dbc74c08e82fe6c7c81f07f0662576158b09a6e0f5d6e737801d4002f8ba`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf640ab8e140479ad814263b7eb8a593634fb817ef9aedda45a24a2682e02d`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 1.8 MB (1752770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da922eaea3a3579801d40505eb31491006da179392dcfb97ed06ca2af932dad`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:d8fb30755a1833900d80f638fee295d11ead95fadb7bbe506c4d50fb2b8dd5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48114670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a742af07f52e0257541cbdaabd2ba5390624b505f0a494d30df2ec9afac29a6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:19 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 03:01:19 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 03:01:19 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 03:01:19 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 03:01:19 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 03:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a5ce10069fc0bda0f1022fddd396e09f242597ae01c904766c5db3d9ac2675`  
		Last Modified: Wed, 28 Jan 2026 03:01:29 GMT  
		Size: 44.6 MB (44608702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa95cdc37d3c22b71ffa2e62fe167da8d27f8cac4863456b8ac87b005efc46a`  
		Last Modified: Wed, 28 Jan 2026 03:01:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a1261dfb8c36a3cb908db697a44a1d6df7c790de07f2ad174bebf62a602c82`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:f117a2bd503e53266f6c5eb06e9b7d0a890852abdfae825abd4187b2201fa3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd354a399ca5dfa10e2bcce840128924e14f7b90fba3a9b9eee2194236a8e17`

```dockerfile
```

-	Layers:
	-	`sha256:6570a77a84d68fb9174f930283eb195ac66bfc9dc5379411e4bbab29e860028d`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:d8fa210706bad66ced606cd665899bdae4c9fc429bce02af91710b64f5e0dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49959891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498d05018c4bbcbd0385187776e59b0f0fc467f2eca08ce2c274b5f53a05465d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:34 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:43:34 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:43:34 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:43:34 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:43:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:43:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fb4c06cbae0de216b65841183a7485c5e39161ed699f8ba01c6dd1389c36de`  
		Last Modified: Wed, 28 Jan 2026 02:43:45 GMT  
		Size: 45.8 MB (45819450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a30fe37bce4d1587cc197e216ee533ec899ffc1832d348c7d50d1815192e`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78da196f5453df7f0115960345d64c78156d6778c48d0e0c3b4ca9de154e89`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:1f07f787c5d807edd8208ea8bbc48e49d86b5bd27f18583d57c70dcb14fbd17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49190ad5d2830f1789d2739aa0d3bacb1a94b0478b7b042b38d5b42e8660f490`

```dockerfile
```

-	Layers:
	-	`sha256:b1584e0d7ac55f7a901e49e3d7e6fa01e611dae3214260ee0709d66d73e6005b`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 1.8 MB (1752900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc71cdf4d1aaa3453eea03b2b89eb37ec9d7b18de46618059926e2d4a754ac1`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:62997f290c1c0f15b8a750bbf99f2b54f1cd8fb06778d3a0919d921a6770e2a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:88b2e64fb6cb598237334b490597d3e66617cd3163977cab1a0c910a245d54bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169353457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f181e10b23a159c1263fc75c989efa6feb863c0299a663212f8f1de586b755d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:05 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:42:05 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:42:05 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:42:05 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:42:05 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:05:09 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 04:05:09 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb573624033b64c31ce0b0988dfdf9d3809781fecc6eb2d890f97c3ec0d5c48d`  
		Last Modified: Wed, 28 Jan 2026 02:42:16 GMT  
		Size: 46.0 MB (46023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9d755e36402a7458130d201cdb7310cafde20bbadcaf36b9ee03d15359dd4`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7886e99f614dac17818774c38e82652899389c6c80540e14b901962452a6393`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3dd42643aad23191e7bba9659776bd716342e4a6e8690e587203df5d08525e`  
		Last Modified: Wed, 28 Jan 2026 04:05:33 GMT  
		Size: 119.5 MB (119524282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2aa34d8b0540d44c5b6c45ebc9d65a351e483289bf6256a006dddc7f8c6b0`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:b7cd3d52a41b20d22a063849a8dee9e527a3cf74b18bc17dba3c9d68c2d5bee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6870662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00c0398071892bcf8580088bdc487cb75111e5618790000605018788a73d0ce`

```dockerfile
```

-	Layers:
	-	`sha256:0a4efbfc13e1229f0d6dd65ef0f8a6b827846388c759bb3bb241c01b4e17491b`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 6.9 MB (6861102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de638912f1a49162d380b6cd3aff7c39a98fbd99a73848c8b0422b45863548e9`  
		Last Modified: Wed, 28 Jan 2026 04:05:30 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:0d79630fa24f3e393db40c3458bbe00f42d73ccf6ad998e28e7d3b7d7c2f7a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148651940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ad51fedc2cc5de17ff6848327d5508ad3134dea322a3e74ed76259f23c09fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:19 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 03:01:19 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 03:01:19 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 03:01:19 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 03:01:19 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 03:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:54:22 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 03:54:22 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a5ce10069fc0bda0f1022fddd396e09f242597ae01c904766c5db3d9ac2675`  
		Last Modified: Wed, 28 Jan 2026 03:01:29 GMT  
		Size: 44.6 MB (44608702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa95cdc37d3c22b71ffa2e62fe167da8d27f8cac4863456b8ac87b005efc46a`  
		Last Modified: Wed, 28 Jan 2026 03:01:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a1261dfb8c36a3cb908db697a44a1d6df7c790de07f2ad174bebf62a602c82`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc42e4d82ff7185bf5dce6b1f34d38a2f4dd413d7d3b202e9c01df58649d2e57`  
		Last Modified: Wed, 28 Jan 2026 03:54:38 GMT  
		Size: 100.5 MB (100536939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff9cb955c967a34bfb0e2613967dec50029b5cee1cc4f9e4c8731439012b1fe`  
		Last Modified: Wed, 28 Jan 2026 03:54:35 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:f532a543bc4bb18ec8901e9f65cc0bf40196d5039fab9f95f14503c6184c6e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6d8e3901fdfc2f8b85fcd1157a2ce8dfc5cd802d75a81da0bca00d493092d1`

```dockerfile
```

-	Layers:
	-	`sha256:50b938328ad302c7bbd804139f5670ae551a8a78cd8da87a9584ee81a1125f36`  
		Last Modified: Wed, 28 Jan 2026 03:54:35 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9e1ed8d23dfc5886288191d77d108d4d2490eb720bda6c6b36231b04719988be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163120109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d65734d3917d9c2b324f54aeb219ddec939f4af1da2a0b839a933570173a909`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:34 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:43:34 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:43:34 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:43:34 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:43:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:43:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:25:07 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 28 Jan 2026 04:25:07 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fb4c06cbae0de216b65841183a7485c5e39161ed699f8ba01c6dd1389c36de`  
		Last Modified: Wed, 28 Jan 2026 02:43:45 GMT  
		Size: 45.8 MB (45819450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a30fe37bce4d1587cc197e216ee533ec899ffc1832d348c7d50d1815192e`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78da196f5453df7f0115960345d64c78156d6778c48d0e0c3b4ca9de154e89`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c966ae1fb836a936092a368a79641536cbea77068188fd2b20818414332283`  
		Last Modified: Wed, 28 Jan 2026 04:25:28 GMT  
		Size: 113.2 MB (113159887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3753fa4a85f3738824c87e47f7ab1a81ab493724c92e41966518618469675e65`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:2cefdcb633bb73487619498b312f9b1cda1ff75915a5be4124d5a0dff0d82311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec15c1bea99d79afbcca863378a1aaf8d9d4f4906c98472ce11c2fb26f5ea5e`

```dockerfile
```

-	Layers:
	-	`sha256:81e34e546355f1c453df3cacfb1eb984b3bb1f0697ed446acb8586a6ecfa63cf`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 6.9 MB (6940526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2843c19abe39f7f5b444b4aaea24cae29c520037b84a496ae849f018bb9e0048`  
		Last Modified: Wed, 28 Jan 2026 04:25:26 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:83fc51b6b2c2667e8a088918184b8f0ee189790c41aa9a708059ee74aae68d47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:ad8e8e327b505af17e342fc577d1ac9f1c20a3f89c24dc1464ba2c34da9a6157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49828844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e012dabfe0501c513be0caf416b78fc2b04de0a2da57b66999587629fb5a06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:05 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:42:05 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:42:05 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:42:05 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:42:05 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:42:05 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb573624033b64c31ce0b0988dfdf9d3809781fecc6eb2d890f97c3ec0d5c48d`  
		Last Modified: Wed, 28 Jan 2026 02:42:16 GMT  
		Size: 46.0 MB (46023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9d755e36402a7458130d201cdb7310cafde20bbadcaf36b9ee03d15359dd4`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7886e99f614dac17818774c38e82652899389c6c80540e14b901962452a6393`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:9db841133b3f6208c4f4bf6269d575e6bb61891e9fc174e31c436b2371940759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d15dbc74c08e82fe6c7c81f07f0662576158b09a6e0f5d6e737801d4002f8ba`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf640ab8e140479ad814263b7eb8a593634fb817ef9aedda45a24a2682e02d`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 1.8 MB (1752770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da922eaea3a3579801d40505eb31491006da179392dcfb97ed06ca2af932dad`  
		Last Modified: Wed, 28 Jan 2026 02:42:15 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:d8fb30755a1833900d80f638fee295d11ead95fadb7bbe506c4d50fb2b8dd5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48114670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a742af07f52e0257541cbdaabd2ba5390624b505f0a494d30df2ec9afac29a6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:19 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 03:01:19 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 03:01:19 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 03:01:19 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 03:01:19 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 03:01:19 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 03:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a5ce10069fc0bda0f1022fddd396e09f242597ae01c904766c5db3d9ac2675`  
		Last Modified: Wed, 28 Jan 2026 03:01:29 GMT  
		Size: 44.6 MB (44608702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa95cdc37d3c22b71ffa2e62fe167da8d27f8cac4863456b8ac87b005efc46a`  
		Last Modified: Wed, 28 Jan 2026 03:01:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a1261dfb8c36a3cb908db697a44a1d6df7c790de07f2ad174bebf62a602c82`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:f117a2bd503e53266f6c5eb06e9b7d0a890852abdfae825abd4187b2201fa3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd354a399ca5dfa10e2bcce840128924e14f7b90fba3a9b9eee2194236a8e17`

```dockerfile
```

-	Layers:
	-	`sha256:6570a77a84d68fb9174f930283eb195ac66bfc9dc5379411e4bbab29e860028d`  
		Last Modified: Wed, 28 Jan 2026 03:01:26 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:d8fa210706bad66ced606cd665899bdae4c9fc429bce02af91710b64f5e0dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49959891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498d05018c4bbcbd0385187776e59b0f0fc467f2eca08ce2c274b5f53a05465d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:34 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 28 Jan 2026 02:43:34 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 28 Jan 2026 02:43:34 GMT
ARG MAKEFLAGS=
# Wed, 28 Jan 2026 02:43:34 GMT
ENV ZNC_VERSION=1.10.1
# Wed, 28 Jan 2026 02:43:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 28 Jan 2026 02:43:34 GMT
VOLUME [/znc-data]
# Wed, 28 Jan 2026 02:43:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fb4c06cbae0de216b65841183a7485c5e39161ed699f8ba01c6dd1389c36de`  
		Last Modified: Wed, 28 Jan 2026 02:43:45 GMT  
		Size: 45.8 MB (45819450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977a30fe37bce4d1587cc197e216ee533ec899ffc1832d348c7d50d1815192e`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78da196f5453df7f0115960345d64c78156d6778c48d0e0c3b4ca9de154e89`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:1f07f787c5d807edd8208ea8bbc48e49d86b5bd27f18583d57c70dcb14fbd17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49190ad5d2830f1789d2739aa0d3bacb1a94b0478b7b042b38d5b42e8660f490`

```dockerfile
```

-	Layers:
	-	`sha256:b1584e0d7ac55f7a901e49e3d7e6fa01e611dae3214260ee0709d66d73e6005b`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 1.8 MB (1752900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc71cdf4d1aaa3453eea03b2b89eb37ec9d7b18de46618059926e2d4a754ac1`  
		Last Modified: Wed, 28 Jan 2026 02:43:44 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json
