<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.34`](#telegraf134)
-	[`telegraf:1.34-alpine`](#telegraf134-alpine)
-	[`telegraf:1.34.4`](#telegraf1344)
-	[`telegraf:1.34.4-alpine`](#telegraf1344-alpine)
-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:2173764352db5591bebe02d3f965cc64cdd357ff8439f57e45b6a1885eb50333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34` - linux; amd64

```console
$ docker pull telegraf@sha256:3754bcaa1b1859a8dfa6860ea4b6c88ab8978a46b4d36c34f7089801c1ab9333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168903414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49d4995e32102dcb59b9d85e38f4d3d6ef3135b3b240dc9f7a8fd63ca515e45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 18 Nov 2025 07:03:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba07203c635300950eb8131b4b46779d4f3489ba20bfa5b643f945506d990a2`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 18.9 MB (18943039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada49748821f7b83d4d2c200073a23181ec7dd8a9000c41a468fd2f18eeb0dec`  
		Last Modified: Tue, 18 Nov 2025 07:03:54 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf07cd071e1684f29df006ab60a55aaf0d27f9dab92cd61d1420788c15ac205`  
		Last Modified: Tue, 18 Nov 2025 07:04:09 GMT  
		Size: 77.4 MB (77446202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ba1a840ba15691e766823f63b325d8755a1b9dcb4b4a10516fffa951e6f676`  
		Last Modified: Tue, 18 Nov 2025 07:03:54 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:b0c6027feafc31e0afa1005b7376001a504b25aff339f6c2c00bffecc8ec4f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c22e1d57fe2631c6f6047f9bf05bdc13c06ffc1f310bc5b8fbc27822b6661fb`

```dockerfile
```

-	Layers:
	-	`sha256:fd0b1e307aaac7d7e424cbcf5c238844afab86ce632fc45a6c60f35dc992a2d9`  
		Last Modified: Tue, 18 Nov 2025 10:11:37 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f42b79c9a8d6a23dc70907bcadf862ff1da96b35db88a144d8252ae5181c47e`  
		Last Modified: Tue, 18 Nov 2025 10:11:38 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c123f48a244f6b723ee96fc27387201f31840474d726f2bae0c10b468cec0079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155384518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8cf53e9fdbde446d7779d2f4fe53edc2f7d0a9f500fed1707d6bdf65ab2f98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:50:19 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 18 Nov 2025 05:50:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:50:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:50:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:50:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:50:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0d98d8baac58b69cf6bbbebe00a6a4be720a9a2f53a2ae0ff0383da69055b8`  
		Last Modified: Tue, 18 Nov 2025 05:50:43 GMT  
		Size: 17.7 MB (17722489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761e4687bc7deac4b90a11f11da1680b802cb56900de39b189c46adf63e34586`  
		Last Modified: Tue, 18 Nov 2025 05:50:42 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6354b029a3e82634694031e0d0952e1092bea595b8decf75c1e91ebd20127a33`  
		Last Modified: Tue, 18 Nov 2025 05:50:47 GMT  
		Size: 71.5 MB (71527153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddaff953ad4451ad5ea9a28aa58bd70a9dc3e30a7ccfafac726e5552319b053`  
		Last Modified: Tue, 18 Nov 2025 05:50:42 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:3acdec9675cc0ab227702ee63f198b95eeb46c897eeb6983851245c79788144c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c04d115ff34e16f8fa71f40b346ffbd89438e77313f1b4dee698691eb9200f4`

```dockerfile
```

-	Layers:
	-	`sha256:40919a6c6817f52eee2ef61a93c9b3b0ce72e5fa47418240b975b069d05e02b7`  
		Last Modified: Tue, 18 Nov 2025 07:11:21 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80fea505fd013913a27dc8cedc6f87966fbb03438e3df2b24fe4a354102e1054`  
		Last Modified: Tue, 18 Nov 2025 07:11:21 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4274e8b45fca9bc2279aeb5e2c9b8f936f73b4114d3f307508da15d5b35b35ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161047240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e5f7048e8156c889eec31254e792884ec3073e0f6a3e9cfb087aa10c2a7a32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:10:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:10:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:10:42 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 18 Nov 2025 06:10:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:10:42 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:10:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:10:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea752a0c161fc9d1cc8be8814712cbb61987ecd1bb74409d7d780babd4ce7da`  
		Last Modified: Tue, 18 Nov 2025 06:11:08 GMT  
		Size: 18.9 MB (18884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df93e335448cf6243073d6a4d709eb16e77698138390adb4c0a73678e4f4e79`  
		Last Modified: Tue, 18 Nov 2025 06:11:06 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caeaf807ec8cb8af3679c2021199be968ec688c6084e19fa5a6601fb66e7691`  
		Last Modified: Tue, 18 Nov 2025 06:11:13 GMT  
		Size: 70.2 MB (70201193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e16a3a77236f129121d8bbc9d0a35208f18ef878083198164ec44112c9931b`  
		Last Modified: Tue, 18 Nov 2025 06:11:06 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:4998a2e209a7b032fa619eb13e30a7453d26d5ffbbc37ca636ff2199edbb16cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8e26a287710baded54a5d7362a0b73d45f7aeae0072dc4866c14400a30dd53`

```dockerfile
```

-	Layers:
	-	`sha256:c3a2b9fb030e150af1e2da25ddbfffad5a69cb1b378ac5b9ad29d3688e5c0f9a`  
		Last Modified: Tue, 18 Nov 2025 07:11:26 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922e0cdbed6677239844923decfd3a3827e1e707ef4802e747768f08ea4a8b84`  
		Last Modified: Tue, 18 Nov 2025 07:11:27 GMT  
		Size: 14.5 KB (14536 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:a3b7b41d457aaba6bbf693ac582488cb0eef9189e0123228d6d73b5ddbecf3d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:af13b793aa1dce69208718cd1a5e52ee46c4fbbc66dd3482802244da07004de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83310068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c734f900c2cc54d55ee1c3608e192247e73d9d77db94c72301e8af7b0cf4cc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac3b64855296be028704ca1d2bdbcaae40b9d4c034875c7d2e1d19a637cb9ba`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 2.4 MB (2446002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c0ccc8f4b7cdee3ffc55785877dd2d581e631f44db1c9273a55f4b1a3ca54`  
		Last Modified: Wed, 08 Oct 2025 23:21:34 GMT  
		Size: 77.2 MB (77236402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a75aa1ed1e0e691f32d3b2541b96ee1c6992482ea6123523007989090e2eee`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f71f1cf17498be8fd0065e60ded60735877224cb9e944bcdc6cdb93d2989504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4ae4f8be5c6ec51fb0b53e97e765bf86a5b5bb24f54af62f06331612ddc487`

```dockerfile
```

-	Layers:
	-	`sha256:6c5d8506040a5778f7f878513986c23cc8a163a4350c0a06768c33507d6878f1`  
		Last Modified: Thu, 09 Oct 2025 00:10:21 GMT  
		Size: 1.1 MB (1102789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba82ca0ac2c265c7cc6c07a2b174b33a447c7789031192fe81b028bd4cb3ee5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:22 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6aa7aa23f4efce9034251674a6146bec7ba0afed83de490ae1fcc009bbfd927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76618603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94050c98410bd57b667d3082abc1644fef314f392475a2a56e455c7c71bfee19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141f6585ef76c126161606642d71be3a680014fb406af77ccd75e5b599e1bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912684419f3dc0457cd6ad63dccc9aa5136f2a64160a2644f8870b703024c81`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 2.5 MB (2531896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a09e09af7872ce5a0604c4669bb70f24e21906b015babebfb76e540fda9fd87`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 70.0 MB (69996727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd0f429f0ae9c0dfcbe4e4a0a000c40c0f51c66b3f27ca3a24e49d773e2af3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f569a6c02470d9b48f6a9719b16f8a2ef536cbe1211ecc12f936487aba61c777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1113486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4b3e083f9b4fa0c40a8082ad1ce012ab2c1b9e22fa7beb132420241f4ba444`

```dockerfile
```

-	Layers:
	-	`sha256:3fdf8a231bfa0803332f5275e62890777cf63dc47fcb8d137a896246cbd0affe`  
		Last Modified: Thu, 09 Oct 2025 00:10:25 GMT  
		Size: 1.1 MB (1098416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5a824629380351fa0100a1f00c0e438e44a10630ca74c4090aed4df9cec1b8`  
		Last Modified: Thu, 09 Oct 2025 00:10:26 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4`

```console
$ docker pull telegraf@sha256:2173764352db5591bebe02d3f965cc64cdd357ff8439f57e45b6a1885eb50333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4` - linux; amd64

```console
$ docker pull telegraf@sha256:3754bcaa1b1859a8dfa6860ea4b6c88ab8978a46b4d36c34f7089801c1ab9333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168903414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49d4995e32102dcb59b9d85e38f4d3d6ef3135b3b240dc9f7a8fd63ca515e45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 18 Nov 2025 07:03:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba07203c635300950eb8131b4b46779d4f3489ba20bfa5b643f945506d990a2`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 18.9 MB (18943039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada49748821f7b83d4d2c200073a23181ec7dd8a9000c41a468fd2f18eeb0dec`  
		Last Modified: Tue, 18 Nov 2025 07:03:54 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf07cd071e1684f29df006ab60a55aaf0d27f9dab92cd61d1420788c15ac205`  
		Last Modified: Tue, 18 Nov 2025 07:04:09 GMT  
		Size: 77.4 MB (77446202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ba1a840ba15691e766823f63b325d8755a1b9dcb4b4a10516fffa951e6f676`  
		Last Modified: Tue, 18 Nov 2025 07:03:54 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:b0c6027feafc31e0afa1005b7376001a504b25aff339f6c2c00bffecc8ec4f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c22e1d57fe2631c6f6047f9bf05bdc13c06ffc1f310bc5b8fbc27822b6661fb`

```dockerfile
```

-	Layers:
	-	`sha256:fd0b1e307aaac7d7e424cbcf5c238844afab86ce632fc45a6c60f35dc992a2d9`  
		Last Modified: Tue, 18 Nov 2025 10:11:37 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f42b79c9a8d6a23dc70907bcadf862ff1da96b35db88a144d8252ae5181c47e`  
		Last Modified: Tue, 18 Nov 2025 10:11:38 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c123f48a244f6b723ee96fc27387201f31840474d726f2bae0c10b468cec0079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155384518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8cf53e9fdbde446d7779d2f4fe53edc2f7d0a9f500fed1707d6bdf65ab2f98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:50:19 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 18 Nov 2025 05:50:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:50:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:50:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:50:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:50:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0d98d8baac58b69cf6bbbebe00a6a4be720a9a2f53a2ae0ff0383da69055b8`  
		Last Modified: Tue, 18 Nov 2025 05:50:43 GMT  
		Size: 17.7 MB (17722489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761e4687bc7deac4b90a11f11da1680b802cb56900de39b189c46adf63e34586`  
		Last Modified: Tue, 18 Nov 2025 05:50:42 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6354b029a3e82634694031e0d0952e1092bea595b8decf75c1e91ebd20127a33`  
		Last Modified: Tue, 18 Nov 2025 05:50:47 GMT  
		Size: 71.5 MB (71527153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddaff953ad4451ad5ea9a28aa58bd70a9dc3e30a7ccfafac726e5552319b053`  
		Last Modified: Tue, 18 Nov 2025 05:50:42 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:3acdec9675cc0ab227702ee63f198b95eeb46c897eeb6983851245c79788144c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c04d115ff34e16f8fa71f40b346ffbd89438e77313f1b4dee698691eb9200f4`

```dockerfile
```

-	Layers:
	-	`sha256:40919a6c6817f52eee2ef61a93c9b3b0ce72e5fa47418240b975b069d05e02b7`  
		Last Modified: Tue, 18 Nov 2025 07:11:21 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80fea505fd013913a27dc8cedc6f87966fbb03438e3df2b24fe4a354102e1054`  
		Last Modified: Tue, 18 Nov 2025 07:11:21 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4274e8b45fca9bc2279aeb5e2c9b8f936f73b4114d3f307508da15d5b35b35ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161047240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e5f7048e8156c889eec31254e792884ec3073e0f6a3e9cfb087aa10c2a7a32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:10:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:10:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:10:42 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 18 Nov 2025 06:10:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:10:42 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:10:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:10:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea752a0c161fc9d1cc8be8814712cbb61987ecd1bb74409d7d780babd4ce7da`  
		Last Modified: Tue, 18 Nov 2025 06:11:08 GMT  
		Size: 18.9 MB (18884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df93e335448cf6243073d6a4d709eb16e77698138390adb4c0a73678e4f4e79`  
		Last Modified: Tue, 18 Nov 2025 06:11:06 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caeaf807ec8cb8af3679c2021199be968ec688c6084e19fa5a6601fb66e7691`  
		Last Modified: Tue, 18 Nov 2025 06:11:13 GMT  
		Size: 70.2 MB (70201193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e16a3a77236f129121d8bbc9d0a35208f18ef878083198164ec44112c9931b`  
		Last Modified: Tue, 18 Nov 2025 06:11:06 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:4998a2e209a7b032fa619eb13e30a7453d26d5ffbbc37ca636ff2199edbb16cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8e26a287710baded54a5d7362a0b73d45f7aeae0072dc4866c14400a30dd53`

```dockerfile
```

-	Layers:
	-	`sha256:c3a2b9fb030e150af1e2da25ddbfffad5a69cb1b378ac5b9ad29d3688e5c0f9a`  
		Last Modified: Tue, 18 Nov 2025 07:11:26 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922e0cdbed6677239844923decfd3a3827e1e707ef4802e747768f08ea4a8b84`  
		Last Modified: Tue, 18 Nov 2025 07:11:27 GMT  
		Size: 14.5 KB (14536 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4-alpine`

```console
$ docker pull telegraf@sha256:a3b7b41d457aaba6bbf693ac582488cb0eef9189e0123228d6d73b5ddbecf3d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:af13b793aa1dce69208718cd1a5e52ee46c4fbbc66dd3482802244da07004de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83310068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c734f900c2cc54d55ee1c3608e192247e73d9d77db94c72301e8af7b0cf4cc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac3b64855296be028704ca1d2bdbcaae40b9d4c034875c7d2e1d19a637cb9ba`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 2.4 MB (2446002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c0ccc8f4b7cdee3ffc55785877dd2d581e631f44db1c9273a55f4b1a3ca54`  
		Last Modified: Wed, 08 Oct 2025 23:21:34 GMT  
		Size: 77.2 MB (77236402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a75aa1ed1e0e691f32d3b2541b96ee1c6992482ea6123523007989090e2eee`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f71f1cf17498be8fd0065e60ded60735877224cb9e944bcdc6cdb93d2989504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4ae4f8be5c6ec51fb0b53e97e765bf86a5b5bb24f54af62f06331612ddc487`

```dockerfile
```

-	Layers:
	-	`sha256:6c5d8506040a5778f7f878513986c23cc8a163a4350c0a06768c33507d6878f1`  
		Last Modified: Thu, 09 Oct 2025 00:10:21 GMT  
		Size: 1.1 MB (1102789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba82ca0ac2c265c7cc6c07a2b174b33a447c7789031192fe81b028bd4cb3ee5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:22 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6aa7aa23f4efce9034251674a6146bec7ba0afed83de490ae1fcc009bbfd927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76618603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94050c98410bd57b667d3082abc1644fef314f392475a2a56e455c7c71bfee19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141f6585ef76c126161606642d71be3a680014fb406af77ccd75e5b599e1bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912684419f3dc0457cd6ad63dccc9aa5136f2a64160a2644f8870b703024c81`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 2.5 MB (2531896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a09e09af7872ce5a0604c4669bb70f24e21906b015babebfb76e540fda9fd87`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 70.0 MB (69996727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd0f429f0ae9c0dfcbe4e4a0a000c40c0f51c66b3f27ca3a24e49d773e2af3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f569a6c02470d9b48f6a9719b16f8a2ef536cbe1211ecc12f936487aba61c777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1113486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4b3e083f9b4fa0c40a8082ad1ce012ab2c1b9e22fa7beb132420241f4ba444`

```dockerfile
```

-	Layers:
	-	`sha256:3fdf8a231bfa0803332f5275e62890777cf63dc47fcb8d137a896246cbd0affe`  
		Last Modified: Thu, 09 Oct 2025 00:10:25 GMT  
		Size: 1.1 MB (1098416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5a824629380351fa0100a1f00c0e438e44a10630ca74c4090aed4df9cec1b8`  
		Last Modified: Thu, 09 Oct 2025 00:10:26 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:8d2193e9ffb654e19abf2cfcd7fba1697bef812a775455142aedc1bf2c3844e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35` - linux; amd64

```console
$ docker pull telegraf@sha256:50d80d075e876d4029cbeb15dd9400cdcd623a551eb4c0af409ee49e41512568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269d0176b0dcbe5112803f8fb2cfa4fc1a2779f75c6e98b5491ba845f4beef79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 07:03:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f053ec8926ee0eac7cd01f85cba4936db5cd004807d520797258a293de2f2`  
		Last Modified: Tue, 18 Nov 2025 07:03:58 GMT  
		Size: 18.9 MB (18942918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff3b5a7e3a3189d28a02bb5802edb06a68bdac6958aeb327cfc4effb36ef3a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b4568a334886380c1ddbd41e3887ea7712558d19dbb287eea69a5f4365c3d`  
		Last Modified: Tue, 18 Nov 2025 07:04:10 GMT  
		Size: 79.6 MB (79570680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2257ba4d71f440352eb07b501c4a467afa432a68db3be6645e936e89c774c86a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:f04995bce32c7a9e3ce63a62cf9d78782b454d9d4434349a2d7a6125d0234c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7723b8e0c4f8908d64b757e580e2751a5bb3a752d899dcafcea1bbdca98bf3`

```dockerfile
```

-	Layers:
	-	`sha256:83c52b6bdfc78cd3f0899c7dae78bdce7b69082a8c964b3cfe507aad63bb4e77`  
		Last Modified: Tue, 18 Nov 2025 10:11:48 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076b5f3088b7bf663c9684ffa83eca3bce17623e586c2d25f01ad3c992461a60`  
		Last Modified: Tue, 18 Nov 2025 10:11:49 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:085c84f62156cb279c05694ab3fff24b0b96e867bb0bccf168b5df902fca48cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba8fb66d8290d9df131d773ae56b0501594cf65c3b99ee84da29aabba70f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 05:50:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:50:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:50:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de283c9f1014e51262a382731c3a4d3224f79d2e1126367dc0e017820fffaf2e`  
		Last Modified: Tue, 18 Nov 2025 05:51:41 GMT  
		Size: 17.7 MB (17722470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d468a03d1b31f40e39d9a9e76bb739e0d6324bbcd67bf402772634bc52cf6`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce9268d0540926055eaad7328348ac9eb9a4654604d3fc39e18a52fba8efa7f`  
		Last Modified: Tue, 18 Nov 2025 05:51:44 GMT  
		Size: 73.3 MB (73290755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3643944f07ce119cabd447b7de7e0d3ae7c66a6037416cc78d81600e7451b4d2`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:59d0ea717bd2e426860e10efd2aed8913fcf01fe8d0b187ec5effbb938a1e0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031a0d2e2aead9d0e7578dd55e2835c67aff52bf96f18c39b0699d881808f48c`

```dockerfile
```

-	Layers:
	-	`sha256:65cf11ea9b8b0e52ce561982f3da8f2e05588e198dc9c9199314005242d00415`  
		Last Modified: Tue, 18 Nov 2025 07:11:29 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cbcf987f70cc3bf95749837eb6ba218afc958afec6d13cc1635b4c9e5354076`  
		Last Modified: Tue, 18 Nov 2025 07:11:30 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d49e01013420e1cbf4604bdc135eae846aeeb4877608b1fc706c9006704abb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaea9b88101ace62d615d5484fe1167abf09e31fc3430aee424eba12b2bf0a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 06:11:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb45c5599c9c6c086d5acafe91bc81ccd2c81008c1431729fe3d7c4c2c396a`  
		Last Modified: Tue, 18 Nov 2025 06:11:42 GMT  
		Size: 18.9 MB (18884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e7d413ad7172c971c72728951997295238b5fd79fe9aac465d1ebfa4685864`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaed55b3c4269b53c03d0d9eb44a1794778c3939aabee1a482fad11b1868cfa`  
		Last Modified: Tue, 18 Nov 2025 06:11:44 GMT  
		Size: 72.1 MB (72079330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ca2b75a13023f96ad260241723dfb32f25d44a5eaa96b4a8a4fa5275b5c5a`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:95d17338946d671cc48b3151c4c7c52cb48a25733feac71f0c1521ddb2c5486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa75bc84ec0235e4602f212226c6727855805215aff014548ea81eedc4b63d76`

```dockerfile
```

-	Layers:
	-	`sha256:2efd56c35f67dcb6dda051c71f4a3686a2219c1783ccb721f783e661655d0dba`  
		Last Modified: Tue, 18 Nov 2025 10:11:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdc0095e31df8d53bf59c363739d44995c8058df0ffb8a0386b385f287bf3ca`  
		Last Modified: Tue, 18 Nov 2025 10:11:59 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Wed, 08 Oct 2025 23:21:36 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Thu, 09 Oct 2025 00:11:14 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Wed, 08 Oct 2025 23:21:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Thu, 09 Oct 2025 00:10:32 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Thu, 09 Oct 2025 00:10:33 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:15 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Wed, 08 Oct 2025 22:10:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Thu, 09 Oct 2025 00:10:36 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:37 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:8d2193e9ffb654e19abf2cfcd7fba1697bef812a775455142aedc1bf2c3844e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4` - linux; amd64

```console
$ docker pull telegraf@sha256:50d80d075e876d4029cbeb15dd9400cdcd623a551eb4c0af409ee49e41512568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269d0176b0dcbe5112803f8fb2cfa4fc1a2779f75c6e98b5491ba845f4beef79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 07:03:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f053ec8926ee0eac7cd01f85cba4936db5cd004807d520797258a293de2f2`  
		Last Modified: Tue, 18 Nov 2025 07:03:58 GMT  
		Size: 18.9 MB (18942918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff3b5a7e3a3189d28a02bb5802edb06a68bdac6958aeb327cfc4effb36ef3a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b4568a334886380c1ddbd41e3887ea7712558d19dbb287eea69a5f4365c3d`  
		Last Modified: Tue, 18 Nov 2025 07:04:10 GMT  
		Size: 79.6 MB (79570680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2257ba4d71f440352eb07b501c4a467afa432a68db3be6645e936e89c774c86a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:f04995bce32c7a9e3ce63a62cf9d78782b454d9d4434349a2d7a6125d0234c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7723b8e0c4f8908d64b757e580e2751a5bb3a752d899dcafcea1bbdca98bf3`

```dockerfile
```

-	Layers:
	-	`sha256:83c52b6bdfc78cd3f0899c7dae78bdce7b69082a8c964b3cfe507aad63bb4e77`  
		Last Modified: Tue, 18 Nov 2025 10:11:48 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076b5f3088b7bf663c9684ffa83eca3bce17623e586c2d25f01ad3c992461a60`  
		Last Modified: Tue, 18 Nov 2025 10:11:49 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:085c84f62156cb279c05694ab3fff24b0b96e867bb0bccf168b5df902fca48cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba8fb66d8290d9df131d773ae56b0501594cf65c3b99ee84da29aabba70f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 05:50:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:50:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:50:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de283c9f1014e51262a382731c3a4d3224f79d2e1126367dc0e017820fffaf2e`  
		Last Modified: Tue, 18 Nov 2025 05:51:41 GMT  
		Size: 17.7 MB (17722470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d468a03d1b31f40e39d9a9e76bb739e0d6324bbcd67bf402772634bc52cf6`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce9268d0540926055eaad7328348ac9eb9a4654604d3fc39e18a52fba8efa7f`  
		Last Modified: Tue, 18 Nov 2025 05:51:44 GMT  
		Size: 73.3 MB (73290755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3643944f07ce119cabd447b7de7e0d3ae7c66a6037416cc78d81600e7451b4d2`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:59d0ea717bd2e426860e10efd2aed8913fcf01fe8d0b187ec5effbb938a1e0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031a0d2e2aead9d0e7578dd55e2835c67aff52bf96f18c39b0699d881808f48c`

```dockerfile
```

-	Layers:
	-	`sha256:65cf11ea9b8b0e52ce561982f3da8f2e05588e198dc9c9199314005242d00415`  
		Last Modified: Tue, 18 Nov 2025 07:11:29 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cbcf987f70cc3bf95749837eb6ba218afc958afec6d13cc1635b4c9e5354076`  
		Last Modified: Tue, 18 Nov 2025 07:11:30 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d49e01013420e1cbf4604bdc135eae846aeeb4877608b1fc706c9006704abb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaea9b88101ace62d615d5484fe1167abf09e31fc3430aee424eba12b2bf0a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 06:11:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb45c5599c9c6c086d5acafe91bc81ccd2c81008c1431729fe3d7c4c2c396a`  
		Last Modified: Tue, 18 Nov 2025 06:11:42 GMT  
		Size: 18.9 MB (18884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e7d413ad7172c971c72728951997295238b5fd79fe9aac465d1ebfa4685864`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaed55b3c4269b53c03d0d9eb44a1794778c3939aabee1a482fad11b1868cfa`  
		Last Modified: Tue, 18 Nov 2025 06:11:44 GMT  
		Size: 72.1 MB (72079330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ca2b75a13023f96ad260241723dfb32f25d44a5eaa96b4a8a4fa5275b5c5a`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:95d17338946d671cc48b3151c4c7c52cb48a25733feac71f0c1521ddb2c5486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa75bc84ec0235e4602f212226c6727855805215aff014548ea81eedc4b63d76`

```dockerfile
```

-	Layers:
	-	`sha256:2efd56c35f67dcb6dda051c71f4a3686a2219c1783ccb721f783e661655d0dba`  
		Last Modified: Tue, 18 Nov 2025 10:11:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdc0095e31df8d53bf59c363739d44995c8058df0ffb8a0386b385f287bf3ca`  
		Last Modified: Tue, 18 Nov 2025 10:11:59 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Wed, 08 Oct 2025 23:21:36 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Thu, 09 Oct 2025 00:11:14 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Wed, 08 Oct 2025 23:21:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Thu, 09 Oct 2025 00:10:32 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Thu, 09 Oct 2025 00:10:33 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:15 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Wed, 08 Oct 2025 22:10:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Thu, 09 Oct 2025 00:10:36 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:37 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:5f5a18511b2f75c2773394bdeb70e8df735e788d834280842c72a3afbd2ea033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36` - linux; amd64

```console
$ docker pull telegraf@sha256:44d0c1e880333cbca36d5b04a4265d9c25439e803c2923a717bded1458e19f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307a413c6ef9a168da7c4f02d3f56425b7fd46b5145c996d0031e38265629aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 07:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b9d0400de861bd9fd471e8915c53d25ae95fa8c9b6faada96c93bab8b33eed`  
		Last Modified: Tue, 18 Nov 2025 07:04:09 GMT  
		Size: 18.9 MB (18942686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33929b66e536ddcd331e714db06615e3bf1fe0594621b9374104e65ead7a73`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbc395ec01246ec776b36853ed74cc7d2dd1834ea59a5068252608594b3d9d1`  
		Last Modified: Tue, 18 Nov 2025 07:04:20 GMT  
		Size: 80.5 MB (80473522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8190af7a955eec0bae4f8ce8953bec2ff6a32ec8c7ed0c8b48052e3a76e00f49`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:ddcad4cd4a6a685b92715342d7ac637974a093d277294b771f8ee9c8a430b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707c51fd65ac0bbfad0eb314e65218461c473227a398cd1889ba5a280fa66d3f`

```dockerfile
```

-	Layers:
	-	`sha256:3b071af06ce227d07aa190f6ba4c86e0fc3c38a6675e09e4eca6c95610757f4a`  
		Last Modified: Tue, 18 Nov 2025 10:12:03 GMT  
		Size: 6.7 MB (6653548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5b21e929a204e5831fffeb8099afef4de813a34f4ce9b4384b56106cdb01f8`  
		Last Modified: Tue, 18 Nov 2025 10:12:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9e27fd79374ef186b5d218b2212ec8dd5a5bf2f35c0e230050ae58d39001d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571a4938a7b9caba0eb38582091907a2decabe3a31f8521e304f22cd94c33381`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 05:51:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:51:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:51:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7105ead932b30517c12cb3bb6c17914e08db14c4798aa43c1aabb7010f5b45`  
		Last Modified: Tue, 18 Nov 2025 05:51:34 GMT  
		Size: 17.7 MB (17722488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dad9c2caee4b2dfe72a6a3ee58e157e80aa18ffca53632e15785e1953b9820`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1136d33da7add9039d86ae1587988fa40135f4f5f757372d3d2a520807c59c32`  
		Last Modified: Tue, 18 Nov 2025 05:51:38 GMT  
		Size: 74.0 MB (73963585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae494612a17424b8bd1b0160c8fd5b5a1872657894a7818a842ffb572ae117bd`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:e821deda4c002d2fd49eea100765b9b6d299c29542e13500d933d740c4a09129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44916c788a82e02df905fbb56a10119301ff779a62445d3ed4b42cbb0856590c`

```dockerfile
```

-	Layers:
	-	`sha256:573ae69a018ad83aa850ca735d385a4afb4fb6d6a759b0dbb4a3274fece4504e`  
		Last Modified: Tue, 18 Nov 2025 07:11:37 GMT  
		Size: 6.6 MB (6648153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5434d141d8bb9751ddda08d6f97f2a72be54fbd6157fce1cc08774b249bf72c`  
		Last Modified: Tue, 18 Nov 2025 07:11:38 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6ebda6a65fc5573ee696a0481c69dea9fc68c5d44366c080c956d5f8d76dac33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162645599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2bc6ef617e6cb4888c328d42a5b672a883bb04a0b45f52c49e4ab141e20b89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:16 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 06:11:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8759b8978ec0d34561d784757fa6476dd7b42d741d4ffb7e39e1daee465b081`  
		Last Modified: Tue, 18 Nov 2025 06:11:48 GMT  
		Size: 18.9 MB (18883787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe79faffe81a3dbc810b07a1ada318d395cd3fcaebe00c730fd4a21d186023`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf27dce91cceef13a63c40febe7e615e985dca81383f71c4fd78b072a624d2`  
		Last Modified: Tue, 18 Nov 2025 06:11:52 GMT  
		Size: 71.8 MB (71800292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fa4e01808b562f04159fa0c2c7b0698fda75af81de83e130cde4c067acf1d6`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:77b326c80f4525a0546588711843437362ba80969941a6e7bae25cd2bf8052c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6669087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6375a82c70a4059eea635d4a2cf4735e30ac32695885063af0269ff03b67a7`

```dockerfile
```

-	Layers:
	-	`sha256:649f319c614cbafcd450d7b6dd2b09969455c7794bbd7bae9ef2921e053f5cb0`  
		Last Modified: Tue, 18 Nov 2025 10:12:13 GMT  
		Size: 6.7 MB (6654236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d6fb8cc8da981ec451c3345291491d558fa3707cb025e7272cd4ac5242892f`  
		Last Modified: Tue, 18 Nov 2025 10:12:14 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:5f5a18511b2f75c2773394bdeb70e8df735e788d834280842c72a3afbd2ea033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4` - linux; amd64

```console
$ docker pull telegraf@sha256:44d0c1e880333cbca36d5b04a4265d9c25439e803c2923a717bded1458e19f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307a413c6ef9a168da7c4f02d3f56425b7fd46b5145c996d0031e38265629aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 07:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b9d0400de861bd9fd471e8915c53d25ae95fa8c9b6faada96c93bab8b33eed`  
		Last Modified: Tue, 18 Nov 2025 07:04:09 GMT  
		Size: 18.9 MB (18942686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33929b66e536ddcd331e714db06615e3bf1fe0594621b9374104e65ead7a73`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbc395ec01246ec776b36853ed74cc7d2dd1834ea59a5068252608594b3d9d1`  
		Last Modified: Tue, 18 Nov 2025 07:04:20 GMT  
		Size: 80.5 MB (80473522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8190af7a955eec0bae4f8ce8953bec2ff6a32ec8c7ed0c8b48052e3a76e00f49`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:ddcad4cd4a6a685b92715342d7ac637974a093d277294b771f8ee9c8a430b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707c51fd65ac0bbfad0eb314e65218461c473227a398cd1889ba5a280fa66d3f`

```dockerfile
```

-	Layers:
	-	`sha256:3b071af06ce227d07aa190f6ba4c86e0fc3c38a6675e09e4eca6c95610757f4a`  
		Last Modified: Tue, 18 Nov 2025 10:12:03 GMT  
		Size: 6.7 MB (6653548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5b21e929a204e5831fffeb8099afef4de813a34f4ce9b4384b56106cdb01f8`  
		Last Modified: Tue, 18 Nov 2025 10:12:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9e27fd79374ef186b5d218b2212ec8dd5a5bf2f35c0e230050ae58d39001d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571a4938a7b9caba0eb38582091907a2decabe3a31f8521e304f22cd94c33381`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 05:51:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:51:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:51:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7105ead932b30517c12cb3bb6c17914e08db14c4798aa43c1aabb7010f5b45`  
		Last Modified: Tue, 18 Nov 2025 05:51:34 GMT  
		Size: 17.7 MB (17722488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dad9c2caee4b2dfe72a6a3ee58e157e80aa18ffca53632e15785e1953b9820`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1136d33da7add9039d86ae1587988fa40135f4f5f757372d3d2a520807c59c32`  
		Last Modified: Tue, 18 Nov 2025 05:51:38 GMT  
		Size: 74.0 MB (73963585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae494612a17424b8bd1b0160c8fd5b5a1872657894a7818a842ffb572ae117bd`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:e821deda4c002d2fd49eea100765b9b6d299c29542e13500d933d740c4a09129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44916c788a82e02df905fbb56a10119301ff779a62445d3ed4b42cbb0856590c`

```dockerfile
```

-	Layers:
	-	`sha256:573ae69a018ad83aa850ca735d385a4afb4fb6d6a759b0dbb4a3274fece4504e`  
		Last Modified: Tue, 18 Nov 2025 07:11:37 GMT  
		Size: 6.6 MB (6648153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5434d141d8bb9751ddda08d6f97f2a72be54fbd6157fce1cc08774b249bf72c`  
		Last Modified: Tue, 18 Nov 2025 07:11:38 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6ebda6a65fc5573ee696a0481c69dea9fc68c5d44366c080c956d5f8d76dac33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162645599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2bc6ef617e6cb4888c328d42a5b672a883bb04a0b45f52c49e4ab141e20b89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:16 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 06:11:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8759b8978ec0d34561d784757fa6476dd7b42d741d4ffb7e39e1daee465b081`  
		Last Modified: Tue, 18 Nov 2025 06:11:48 GMT  
		Size: 18.9 MB (18883787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe79faffe81a3dbc810b07a1ada318d395cd3fcaebe00c730fd4a21d186023`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf27dce91cceef13a63c40febe7e615e985dca81383f71c4fd78b072a624d2`  
		Last Modified: Tue, 18 Nov 2025 06:11:52 GMT  
		Size: 71.8 MB (71800292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fa4e01808b562f04159fa0c2c7b0698fda75af81de83e130cde4c067acf1d6`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:77b326c80f4525a0546588711843437362ba80969941a6e7bae25cd2bf8052c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6669087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6375a82c70a4059eea635d4a2cf4735e30ac32695885063af0269ff03b67a7`

```dockerfile
```

-	Layers:
	-	`sha256:649f319c614cbafcd450d7b6dd2b09969455c7794bbd7bae9ef2921e053f5cb0`  
		Last Modified: Tue, 18 Nov 2025 10:12:13 GMT  
		Size: 6.7 MB (6654236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d6fb8cc8da981ec451c3345291491d558fa3707cb025e7272cd4ac5242892f`  
		Last Modified: Tue, 18 Nov 2025 10:12:14 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:5f5a18511b2f75c2773394bdeb70e8df735e788d834280842c72a3afbd2ea033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:44d0c1e880333cbca36d5b04a4265d9c25439e803c2923a717bded1458e19f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307a413c6ef9a168da7c4f02d3f56425b7fd46b5145c996d0031e38265629aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 07:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b9d0400de861bd9fd471e8915c53d25ae95fa8c9b6faada96c93bab8b33eed`  
		Last Modified: Tue, 18 Nov 2025 07:04:09 GMT  
		Size: 18.9 MB (18942686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33929b66e536ddcd331e714db06615e3bf1fe0594621b9374104e65ead7a73`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbc395ec01246ec776b36853ed74cc7d2dd1834ea59a5068252608594b3d9d1`  
		Last Modified: Tue, 18 Nov 2025 07:04:20 GMT  
		Size: 80.5 MB (80473522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8190af7a955eec0bae4f8ce8953bec2ff6a32ec8c7ed0c8b48052e3a76e00f49`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ddcad4cd4a6a685b92715342d7ac637974a093d277294b771f8ee9c8a430b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707c51fd65ac0bbfad0eb314e65218461c473227a398cd1889ba5a280fa66d3f`

```dockerfile
```

-	Layers:
	-	`sha256:3b071af06ce227d07aa190f6ba4c86e0fc3c38a6675e09e4eca6c95610757f4a`  
		Last Modified: Tue, 18 Nov 2025 10:12:03 GMT  
		Size: 6.7 MB (6653548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5b21e929a204e5831fffeb8099afef4de813a34f4ce9b4384b56106cdb01f8`  
		Last Modified: Tue, 18 Nov 2025 10:12:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9e27fd79374ef186b5d218b2212ec8dd5a5bf2f35c0e230050ae58d39001d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571a4938a7b9caba0eb38582091907a2decabe3a31f8521e304f22cd94c33381`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 05:51:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:51:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:51:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7105ead932b30517c12cb3bb6c17914e08db14c4798aa43c1aabb7010f5b45`  
		Last Modified: Tue, 18 Nov 2025 05:51:34 GMT  
		Size: 17.7 MB (17722488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dad9c2caee4b2dfe72a6a3ee58e157e80aa18ffca53632e15785e1953b9820`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1136d33da7add9039d86ae1587988fa40135f4f5f757372d3d2a520807c59c32`  
		Last Modified: Tue, 18 Nov 2025 05:51:38 GMT  
		Size: 74.0 MB (73963585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae494612a17424b8bd1b0160c8fd5b5a1872657894a7818a842ffb572ae117bd`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:e821deda4c002d2fd49eea100765b9b6d299c29542e13500d933d740c4a09129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44916c788a82e02df905fbb56a10119301ff779a62445d3ed4b42cbb0856590c`

```dockerfile
```

-	Layers:
	-	`sha256:573ae69a018ad83aa850ca735d385a4afb4fb6d6a759b0dbb4a3274fece4504e`  
		Last Modified: Tue, 18 Nov 2025 07:11:37 GMT  
		Size: 6.6 MB (6648153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5434d141d8bb9751ddda08d6f97f2a72be54fbd6157fce1cc08774b249bf72c`  
		Last Modified: Tue, 18 Nov 2025 07:11:38 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6ebda6a65fc5573ee696a0481c69dea9fc68c5d44366c080c956d5f8d76dac33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162645599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2bc6ef617e6cb4888c328d42a5b672a883bb04a0b45f52c49e4ab141e20b89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:16 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 06:11:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8759b8978ec0d34561d784757fa6476dd7b42d741d4ffb7e39e1daee465b081`  
		Last Modified: Tue, 18 Nov 2025 06:11:48 GMT  
		Size: 18.9 MB (18883787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe79faffe81a3dbc810b07a1ada318d395cd3fcaebe00c730fd4a21d186023`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf27dce91cceef13a63c40febe7e615e985dca81383f71c4fd78b072a624d2`  
		Last Modified: Tue, 18 Nov 2025 06:11:52 GMT  
		Size: 71.8 MB (71800292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fa4e01808b562f04159fa0c2c7b0698fda75af81de83e130cde4c067acf1d6`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:77b326c80f4525a0546588711843437362ba80969941a6e7bae25cd2bf8052c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6669087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6375a82c70a4059eea635d4a2cf4735e30ac32695885063af0269ff03b67a7`

```dockerfile
```

-	Layers:
	-	`sha256:649f319c614cbafcd450d7b6dd2b09969455c7794bbd7bae9ef2921e053f5cb0`  
		Last Modified: Tue, 18 Nov 2025 10:12:13 GMT  
		Size: 6.7 MB (6654236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d6fb8cc8da981ec451c3345291491d558fa3707cb025e7272cd4ac5242892f`  
		Last Modified: Tue, 18 Nov 2025 10:12:14 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
