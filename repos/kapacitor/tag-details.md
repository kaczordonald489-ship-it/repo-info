<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.2`](#kapacitor182)
-	[`kapacitor:1.8.2-alpine`](#kapacitor182-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:8b02d8e0ba02cde56d1a104ba227c578e0e52eec6d37b8206c8d4aaf3ed9ae1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:c88aecc684c4dd1da6d9fd8286d8d59f51baf5dd5ca079553333147e94469fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157663032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af03cbfd87de1e81c7b11fb06a7e902b70e00bff2efe10ac359994f9230b16a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:16:16 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:16 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:42 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f64ee49ae86a8609207d68c3ddf6230af2d9e770ca3b155cda2b45dd97629`  
		Last Modified: Thu, 15 Jan 2026 23:16:31 GMT  
		Size: 49.0 MB (48970801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16704bd5bb7d865c187ac1f527d937e86ffec3c50ee4cc3beaef6cf70f91e52f`  
		Last Modified: Thu, 15 Jan 2026 23:16:32 GMT  
		Size: 72.1 MB (72051145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af534873430c73d8e79450df6e2df84135fec105f9c1ef8c2f96d38d4ed5ee1`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf625e605f4adfd7fc6753244529c55dff81825ff50ae5e7aa5405103e1548d`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:12e42e0a59763ced958976290230f0b2e6416505b48a563a27323ddc99dcf912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ffd2f2d16c7286307ce0545156b0d98a7e16108b5841231feca322f92c567`

```dockerfile
```

-	Layers:
	-	`sha256:53909e7d18b2311a090eb0c22ebd28650e2d7dda19c31d07a1e3daca12ba70c3`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2754e29c97a8a8dee81e854e16b250e547f911edf2709269bf86fd3d25331839`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:e2070fa539333d6e2318c8e992fdd0364dc51bcaf6ad02b046d1612534fad6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149466694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d17dfa9099d2055320ea8cc71dcf1fc4cf6b0087c7a6f847d0502a6ea4add60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:21:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:41 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:29 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce866c5b77da86a9383d2583a9a42c1b21e86f746ee7c6ac2c3308553a422b`  
		Last Modified: Thu, 15 Jan 2026 23:21:57 GMT  
		Size: 47.2 MB (47213869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd89a8870a2fd246249c5fa0017b4693e0a678bcedfec979a85760f2d20f8f5`  
		Last Modified: Thu, 15 Jan 2026 23:21:57 GMT  
		Size: 67.8 MB (67813752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec193a4f26362c7e7cfb88e3943f5b44b0668a7e2ee8fbe016b431f2874db8f5`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301854c7bb29b4e6b1603b318fb0dc116fbb002c4d2870ff7fd9a1579a1b960`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:822d37928e086cb62f6ff29080642ff866595cd457e31ed59f886be551039994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41ea2f90cdfec6b65ece9935a0c16d03faa0b5bc3ca39a27712a15d159c0f43`

```dockerfile
```

-	Layers:
	-	`sha256:32ed23bfe28b986ebda85169020cef5fbc227f7c73cbc9c2c62428a9cb0ffa5d`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a48b7287700452437811e491f43e4d7f2f8dc3e36d84051cafcef4604e3ffcd`  
		Last Modified: Thu, 15 Jan 2026 23:21:54 GMT  
		Size: 14.8 KB (14809 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:8b02d8e0ba02cde56d1a104ba227c578e0e52eec6d37b8206c8d4aaf3ed9ae1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:c88aecc684c4dd1da6d9fd8286d8d59f51baf5dd5ca079553333147e94469fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157663032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af03cbfd87de1e81c7b11fb06a7e902b70e00bff2efe10ac359994f9230b16a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:16:16 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:16 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:42 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f64ee49ae86a8609207d68c3ddf6230af2d9e770ca3b155cda2b45dd97629`  
		Last Modified: Thu, 15 Jan 2026 23:16:31 GMT  
		Size: 49.0 MB (48970801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16704bd5bb7d865c187ac1f527d937e86ffec3c50ee4cc3beaef6cf70f91e52f`  
		Last Modified: Thu, 15 Jan 2026 23:16:32 GMT  
		Size: 72.1 MB (72051145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af534873430c73d8e79450df6e2df84135fec105f9c1ef8c2f96d38d4ed5ee1`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf625e605f4adfd7fc6753244529c55dff81825ff50ae5e7aa5405103e1548d`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:12e42e0a59763ced958976290230f0b2e6416505b48a563a27323ddc99dcf912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982ffd2f2d16c7286307ce0545156b0d98a7e16108b5841231feca322f92c567`

```dockerfile
```

-	Layers:
	-	`sha256:53909e7d18b2311a090eb0c22ebd28650e2d7dda19c31d07a1e3daca12ba70c3`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2754e29c97a8a8dee81e854e16b250e547f911edf2709269bf86fd3d25331839`  
		Last Modified: Thu, 15 Jan 2026 23:16:29 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:e2070fa539333d6e2318c8e992fdd0364dc51bcaf6ad02b046d1612534fad6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149466694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d17dfa9099d2055320ea8cc71dcf1fc4cf6b0087c7a6f847d0502a6ea4add60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENV KAPACITOR_VERSION=1.7.7
# Thu, 15 Jan 2026 23:21:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:41 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:29 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce866c5b77da86a9383d2583a9a42c1b21e86f746ee7c6ac2c3308553a422b`  
		Last Modified: Thu, 15 Jan 2026 23:21:57 GMT  
		Size: 47.2 MB (47213869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd89a8870a2fd246249c5fa0017b4693e0a678bcedfec979a85760f2d20f8f5`  
		Last Modified: Thu, 15 Jan 2026 23:21:57 GMT  
		Size: 67.8 MB (67813752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec193a4f26362c7e7cfb88e3943f5b44b0668a7e2ee8fbe016b431f2874db8f5`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301854c7bb29b4e6b1603b318fb0dc116fbb002c4d2870ff7fd9a1579a1b960`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:822d37928e086cb62f6ff29080642ff866595cd457e31ed59f886be551039994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41ea2f90cdfec6b65ece9935a0c16d03faa0b5bc3ca39a27712a15d159c0f43`

```dockerfile
```

-	Layers:
	-	`sha256:32ed23bfe28b986ebda85169020cef5fbc227f7c73cbc9c2c62428a9cb0ffa5d`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a48b7287700452437811e491f43e4d7f2f8dc3e36d84051cafcef4604e3ffcd`  
		Last Modified: Thu, 15 Jan 2026 23:21:54 GMT  
		Size: 14.8 KB (14809 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:0b91b3acf44d3d578b205bd6e48c083a2a2cf0c81073e7108447f1c6d388dba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:316e124fcc0d4c8e8c51924d9a552fa576d6e92a567681e728c665516fd6d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173824651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa34749cbffd8b4405edd652f3f54dbbdd69b39746aea1ee1f483f6c6e5eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:25 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:42 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c57012893e9c14b4ed9be8ff981779047a0270882fdc44dcbc62633cc7e32`  
		Last Modified: Thu, 15 Jan 2026 23:16:43 GMT  
		Size: 49.0 MB (48970775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001b6dd15f097a48f388ebd7ac53b24426780188e0003d01a3035e9949815cc`  
		Last Modified: Thu, 15 Jan 2026 23:16:44 GMT  
		Size: 88.2 MB (88212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28eefc9be64c03f4386625be3e9e84b5e37b59f8707428be0e80b0ec1055e`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee239ae6aabfbd9dee2a137982ec91d496c77e9ce6911952947b5dc0b89fc328`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:da49a5d03519c9afb5a37fd68c601ad03da5677f937d098e972898b7823a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ee7c403e95a982b588095e396d65a9b77a92e00903498a70cbd69f4adee1c`

```dockerfile
```

-	Layers:
	-	`sha256:74b897cbd09ebfb85d02ae725b41a3a704f39493ae150df51c5b919bdf62e0ed`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81142b9e66372f3ee8c660975c4219a8830dd755a3164ae0925aa438a22389b`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1eff3236806e63039ce16d5ec6b729e874f734640ef191027b81fe4c9330a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9c742c5c037ee1e884b24763997b778ee49fb4afea00038401930332285a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:21:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:57 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:29 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b066ac69fa615a156bc4b2cf1298e60a75122022abe5360dac459bcfdd4b7b`  
		Last Modified: Thu, 15 Jan 2026 23:22:13 GMT  
		Size: 47.2 MB (47213852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f523369fde43a4ea8bd398add7b37d189dc3d4d25f1bc37226edc54d76719`  
		Last Modified: Thu, 15 Jan 2026 23:22:14 GMT  
		Size: 82.0 MB (82009641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f9c520e751598daf66788cb9d9281379b9665fae8a19cb89b3823f4d1d07f`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd761fdd2bb99f3381484f0aee3ff1a23ba5989db64cdcc9d04980bd2e16d73`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:74947cdf7e133ce11495ec5896ab81f4fb893ec50cb7a27a9cc7c036f67d0607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f0a0901976304e95e4a6cf6fd576e90be6cace4b3f6ccd8e7346f36a21c39f`

```dockerfile
```

-	Layers:
	-	`sha256:f263e41f29ec2a97e31bc94888ca0b548221e2fa232e18d75c8744d4f7ce97b9`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe0a8ddc2a028f140c1a139ae06031fa36e9c2b0ec6949a12cb5a601f607fc0`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:855acafe575119c61b8aa3a1590267081f83e69225cea4b61661f69232337447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:f44bdf538a1c3cf60f32d663c0e866748755d4026c276c049b480d71920e34d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92252975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b17d24377e2e9f0b8631f3b5edce6c623c5e60dcc6d9dd7fe1e044609d70a42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENV KAPACITOR_VERSION=1.8.2
# Wed, 28 Jan 2026 03:27:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:53 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085801fe0b551c017ec55b67fc2b9da5116738b713cc527919618ca9ad3e9ae5`  
		Last Modified: Wed, 28 Jan 2026 03:28:08 GMT  
		Size: 88.1 MB (88132674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5a77b32109f5a2d8065e3d27ef96c972cedf4a96e4307d30e02dfcbc5f0b6`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb46f8cc26b337892b51bf260762b87f3db82fb83dc10fd3078b73098b15ef86`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7e60dfaa73c57ad9a325d266f4401f9f3c543fa60ea523eb41bb075948d5827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844842b357864934f15da3f35fa8436b4778711a876fc35142b9f827b160d69e`

```dockerfile
```

-	Layers:
	-	`sha256:c32909963dbc4228a173f333911bebca859c26aa22437d118adef1acdfa78164`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6cf9fdc2130489dfc2d84bc7a13d0be7faab5932e0670eba58ed233371fb0c`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2`

```console
$ docker pull kapacitor@sha256:0b91b3acf44d3d578b205bd6e48c083a2a2cf0c81073e7108447f1c6d388dba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.2` - linux; amd64

```console
$ docker pull kapacitor@sha256:316e124fcc0d4c8e8c51924d9a552fa576d6e92a567681e728c665516fd6d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173824651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa34749cbffd8b4405edd652f3f54dbbdd69b39746aea1ee1f483f6c6e5eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:25 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:42 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c57012893e9c14b4ed9be8ff981779047a0270882fdc44dcbc62633cc7e32`  
		Last Modified: Thu, 15 Jan 2026 23:16:43 GMT  
		Size: 49.0 MB (48970775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001b6dd15f097a48f388ebd7ac53b24426780188e0003d01a3035e9949815cc`  
		Last Modified: Thu, 15 Jan 2026 23:16:44 GMT  
		Size: 88.2 MB (88212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28eefc9be64c03f4386625be3e9e84b5e37b59f8707428be0e80b0ec1055e`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee239ae6aabfbd9dee2a137982ec91d496c77e9ce6911952947b5dc0b89fc328`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:da49a5d03519c9afb5a37fd68c601ad03da5677f937d098e972898b7823a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ee7c403e95a982b588095e396d65a9b77a92e00903498a70cbd69f4adee1c`

```dockerfile
```

-	Layers:
	-	`sha256:74b897cbd09ebfb85d02ae725b41a3a704f39493ae150df51c5b919bdf62e0ed`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81142b9e66372f3ee8c660975c4219a8830dd755a3164ae0925aa438a22389b`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.2` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1eff3236806e63039ce16d5ec6b729e874f734640ef191027b81fe4c9330a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9c742c5c037ee1e884b24763997b778ee49fb4afea00038401930332285a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:21:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:57 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:29 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b066ac69fa615a156bc4b2cf1298e60a75122022abe5360dac459bcfdd4b7b`  
		Last Modified: Thu, 15 Jan 2026 23:22:13 GMT  
		Size: 47.2 MB (47213852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f523369fde43a4ea8bd398add7b37d189dc3d4d25f1bc37226edc54d76719`  
		Last Modified: Thu, 15 Jan 2026 23:22:14 GMT  
		Size: 82.0 MB (82009641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f9c520e751598daf66788cb9d9281379b9665fae8a19cb89b3823f4d1d07f`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd761fdd2bb99f3381484f0aee3ff1a23ba5989db64cdcc9d04980bd2e16d73`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:74947cdf7e133ce11495ec5896ab81f4fb893ec50cb7a27a9cc7c036f67d0607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f0a0901976304e95e4a6cf6fd576e90be6cace4b3f6ccd8e7346f36a21c39f`

```dockerfile
```

-	Layers:
	-	`sha256:f263e41f29ec2a97e31bc94888ca0b548221e2fa232e18d75c8744d4f7ce97b9`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe0a8ddc2a028f140c1a139ae06031fa36e9c2b0ec6949a12cb5a601f607fc0`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2-alpine`

```console
$ docker pull kapacitor@sha256:855acafe575119c61b8aa3a1590267081f83e69225cea4b61661f69232337447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.2-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:f44bdf538a1c3cf60f32d663c0e866748755d4026c276c049b480d71920e34d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92252975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b17d24377e2e9f0b8631f3b5edce6c623c5e60dcc6d9dd7fe1e044609d70a42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENV KAPACITOR_VERSION=1.8.2
# Wed, 28 Jan 2026 03:27:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:53 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085801fe0b551c017ec55b67fc2b9da5116738b713cc527919618ca9ad3e9ae5`  
		Last Modified: Wed, 28 Jan 2026 03:28:08 GMT  
		Size: 88.1 MB (88132674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5a77b32109f5a2d8065e3d27ef96c972cedf4a96e4307d30e02dfcbc5f0b6`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb46f8cc26b337892b51bf260762b87f3db82fb83dc10fd3078b73098b15ef86`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7e60dfaa73c57ad9a325d266f4401f9f3c543fa60ea523eb41bb075948d5827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844842b357864934f15da3f35fa8436b4778711a876fc35142b9f827b160d69e`

```dockerfile
```

-	Layers:
	-	`sha256:c32909963dbc4228a173f333911bebca859c26aa22437d118adef1acdfa78164`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6cf9fdc2130489dfc2d84bc7a13d0be7faab5932e0670eba58ed233371fb0c`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:0b91b3acf44d3d578b205bd6e48c083a2a2cf0c81073e7108447f1c6d388dba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:316e124fcc0d4c8e8c51924d9a552fa576d6e92a567681e728c665516fd6d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173824651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa34749cbffd8b4405edd652f3f54dbbdd69b39746aea1ee1f483f6c6e5eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:25 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:42 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c57012893e9c14b4ed9be8ff981779047a0270882fdc44dcbc62633cc7e32`  
		Last Modified: Thu, 15 Jan 2026 23:16:43 GMT  
		Size: 49.0 MB (48970775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001b6dd15f097a48f388ebd7ac53b24426780188e0003d01a3035e9949815cc`  
		Last Modified: Thu, 15 Jan 2026 23:16:44 GMT  
		Size: 88.2 MB (88212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28eefc9be64c03f4386625be3e9e84b5e37b59f8707428be0e80b0ec1055e`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee239ae6aabfbd9dee2a137982ec91d496c77e9ce6911952947b5dc0b89fc328`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:da49a5d03519c9afb5a37fd68c601ad03da5677f937d098e972898b7823a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ee7c403e95a982b588095e396d65a9b77a92e00903498a70cbd69f4adee1c`

```dockerfile
```

-	Layers:
	-	`sha256:74b897cbd09ebfb85d02ae725b41a3a704f39493ae150df51c5b919bdf62e0ed`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81142b9e66372f3ee8c660975c4219a8830dd755a3164ae0925aa438a22389b`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1eff3236806e63039ce16d5ec6b729e874f734640ef191027b81fe4c9330a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9c742c5c037ee1e884b24763997b778ee49fb4afea00038401930332285a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:21:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:57 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:29 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b066ac69fa615a156bc4b2cf1298e60a75122022abe5360dac459bcfdd4b7b`  
		Last Modified: Thu, 15 Jan 2026 23:22:13 GMT  
		Size: 47.2 MB (47213852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f523369fde43a4ea8bd398add7b37d189dc3d4d25f1bc37226edc54d76719`  
		Last Modified: Thu, 15 Jan 2026 23:22:14 GMT  
		Size: 82.0 MB (82009641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f9c520e751598daf66788cb9d9281379b9665fae8a19cb89b3823f4d1d07f`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd761fdd2bb99f3381484f0aee3ff1a23ba5989db64cdcc9d04980bd2e16d73`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:74947cdf7e133ce11495ec5896ab81f4fb893ec50cb7a27a9cc7c036f67d0607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f0a0901976304e95e4a6cf6fd576e90be6cace4b3f6ccd8e7346f36a21c39f`

```dockerfile
```

-	Layers:
	-	`sha256:f263e41f29ec2a97e31bc94888ca0b548221e2fa232e18d75c8744d4f7ce97b9`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe0a8ddc2a028f140c1a139ae06031fa36e9c2b0ec6949a12cb5a601f607fc0`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
