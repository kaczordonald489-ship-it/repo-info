## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:31c6ed3b2da61645aaa3ad9217b5a52b34b6ebd555ecb71259cd7723c59ae1ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:13e9d884b7e0b9e27a5fe7e963d8831c53089a023ac529a6f08c9df5aa875d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10864983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10e008495467f740bfaa354ef3e6cee8decfe44b9546638f7511e20066d46de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:53 GMT
ENV NATS_SERVER=2.12.4
# Wed, 28 Jan 2026 02:18:53 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Wed, 28 Jan 2026 02:18:53 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='44a6ff34eff7e8d0e1409dbac0b733cff7ecbb4f19388a4d0d3d6085d899f017' ;;     armhf) natsArch='arm6'; sha256='4e59df78e00edb75544aac70e1e99008cd97a039fad6ea1942b7986ee7289245' ;;     armv7) natsArch='arm7'; sha256='67e7708005b615d1b63280c752616ff8663fa8bd3e83bb24890905b9a0a4e789' ;;     x86_64) natsArch='amd64'; sha256='92388f2e4aa1e6dea402eb173cbdb1fcb1df9a9c899cb807b91ddbb45c131b65' ;;     x86) natsArch='386'; sha256='0899515b18dcbfba3572e91ea0bf7b7577a00d102ca91be44840a8a1ad68b4d7' ;;     s390x) natsArch='s390x'; sha256='8c084d41b8ef405c31ff75f84bb03028295001f9741724a8d0fb2c28aa0f3690' ;;     ppc64le) natsArch='ppc64le'; sha256='5b073b7cdfb91b30f226a687311193ce4544700eaf69fd32df2809451e9e5fc0' ;;     loong64) natsArch='loong64'; sha256='e58995ac0402050a0bd6a9513fc144e9f8f6bb01224fdeb5476691cad187a1c7' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 28 Jan 2026 02:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 28 Jan 2026 02:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 28 Jan 2026 02:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 02:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb8431fcefde7a399842bd26161f549797c199aa2262a45ee7808b84eba89cf`  
		Last Modified: Wed, 28 Jan 2026 02:18:57 GMT  
		Size: 7.1 MB (7059142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4d9c1f61fb28d95f699fa04549100e0f1ef62e1c0fb333fa7f24086d7f4375`  
		Last Modified: Wed, 28 Jan 2026 02:18:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae302a5cfb8b576263d64661d2c293f1624a3d1fb3dd906d92480c06ceb99a3`  
		Last Modified: Wed, 28 Jan 2026 02:18:57 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:31411782d4456a1e67851d8d44e49619c3250e0b959b8faee4d259b6e74fa40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cb8700c5ec41e04688194428b2916f9c08bf0ca3702a02f626ccddc36305b9`

```dockerfile
```

-	Layers:
	-	`sha256:3e16339c187e3306a6fe547856284fccd17f2e04ada4af434e77125e501aac13`  
		Last Modified: Wed, 28 Jan 2026 02:18:57 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:7062111cfef49dd1926c37b1411c3df47d6b11b1275bd92bd56ef711759287f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10286710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e474d310c39fef94a36a643f280586cb665a278b71a5185853e0f8bac0ca3130`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:53 GMT
ENV NATS_SERVER=2.12.4
# Wed, 28 Jan 2026 02:16:53 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Wed, 28 Jan 2026 02:16:53 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='44a6ff34eff7e8d0e1409dbac0b733cff7ecbb4f19388a4d0d3d6085d899f017' ;;     armhf) natsArch='arm6'; sha256='4e59df78e00edb75544aac70e1e99008cd97a039fad6ea1942b7986ee7289245' ;;     armv7) natsArch='arm7'; sha256='67e7708005b615d1b63280c752616ff8663fa8bd3e83bb24890905b9a0a4e789' ;;     x86_64) natsArch='amd64'; sha256='92388f2e4aa1e6dea402eb173cbdb1fcb1df9a9c899cb807b91ddbb45c131b65' ;;     x86) natsArch='386'; sha256='0899515b18dcbfba3572e91ea0bf7b7577a00d102ca91be44840a8a1ad68b4d7' ;;     s390x) natsArch='s390x'; sha256='8c084d41b8ef405c31ff75f84bb03028295001f9741724a8d0fb2c28aa0f3690' ;;     ppc64le) natsArch='ppc64le'; sha256='5b073b7cdfb91b30f226a687311193ce4544700eaf69fd32df2809451e9e5fc0' ;;     loong64) natsArch='loong64'; sha256='e58995ac0402050a0bd6a9513fc144e9f8f6bb01224fdeb5476691cad187a1c7' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 28 Jan 2026 02:16:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 28 Jan 2026 02:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 28 Jan 2026 02:16:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 02:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:16:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45577f14f1b8866d12b70185685423372a30880554e8056f894a1bb2de96cad1`  
		Last Modified: Wed, 28 Jan 2026 02:16:58 GMT  
		Size: 6.8 MB (6780695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4c63a9494839d6c0706d4bcb6fb8efb9a7d8bd22698ed73e5dd39d427596dc`  
		Last Modified: Wed, 28 Jan 2026 02:16:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6e0bca84f1663f8eae918c839a07d9e3daf6a40e71d65c631e3423ed7aafa`  
		Last Modified: Wed, 28 Jan 2026 02:16:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a65aca729c97d0b50d62468520acc9f48b96000da2ef13cf34f252159bb6a82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52104c1d0b1a8b7b0eb86126dc048603a31b63aa5b2696c5cfb6d0d6bf1f7e01`

```dockerfile
```

-	Layers:
	-	`sha256:76717f8ceb3f44fbaf7a23482c4c2c293e0cd8434eee8465873df4553685462d`  
		Last Modified: Wed, 28 Jan 2026 02:16:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:a595abf585236e6414f550aba03f74b8fcce04f11aa0a449b2833cd96d0f6e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9994211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9ddd8177d3f9f2bc5f4a457f64b6f85c86b7220e3649cd196935c9baa084c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:05 GMT
ENV NATS_SERVER=2.12.4
# Wed, 28 Jan 2026 02:17:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Wed, 28 Jan 2026 02:17:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='44a6ff34eff7e8d0e1409dbac0b733cff7ecbb4f19388a4d0d3d6085d899f017' ;;     armhf) natsArch='arm6'; sha256='4e59df78e00edb75544aac70e1e99008cd97a039fad6ea1942b7986ee7289245' ;;     armv7) natsArch='arm7'; sha256='67e7708005b615d1b63280c752616ff8663fa8bd3e83bb24890905b9a0a4e789' ;;     x86_64) natsArch='amd64'; sha256='92388f2e4aa1e6dea402eb173cbdb1fcb1df9a9c899cb807b91ddbb45c131b65' ;;     x86) natsArch='386'; sha256='0899515b18dcbfba3572e91ea0bf7b7577a00d102ca91be44840a8a1ad68b4d7' ;;     s390x) natsArch='s390x'; sha256='8c084d41b8ef405c31ff75f84bb03028295001f9741724a8d0fb2c28aa0f3690' ;;     ppc64le) natsArch='ppc64le'; sha256='5b073b7cdfb91b30f226a687311193ce4544700eaf69fd32df2809451e9e5fc0' ;;     loong64) natsArch='loong64'; sha256='e58995ac0402050a0bd6a9513fc144e9f8f6bb01224fdeb5476691cad187a1c7' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 28 Jan 2026 02:17:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 28 Jan 2026 02:17:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 28 Jan 2026 02:17:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 02:17:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3268a8f501bb9f688b6872667e0bc09b09a3dd595e7235b4d3c3844cf1be877e`  
		Last Modified: Wed, 28 Jan 2026 02:17:11 GMT  
		Size: 6.8 MB (6769613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3cb5341bf8f06abd96eadee1d929f525c9eacc07ac13170f8bb88a892bb598`  
		Last Modified: Wed, 28 Jan 2026 02:17:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3505bd7156ae36744c4776c17072313eb9c2dcb6fa0b371f92b1ba02f088a`  
		Last Modified: Wed, 28 Jan 2026 02:17:10 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:01549f1d5522a0c2b97f39f4269e358e74dfece4a6977fda1d561ee2aa5ee59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19727ff872b88d2e5aea53200d5be1c9511466f8404df8a22c3cbd1168dc76a`

```dockerfile
```

-	Layers:
	-	`sha256:cdf89bce3f9376bad75a86f5159da3db0826f8471363bad6b3b5c65e9d706b24`  
		Last Modified: Wed, 28 Jan 2026 02:17:10 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb9907e62ffbbb1ad27969a6fc8fc491f35a6d7c1add7c410b152334e5478de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726b57d39eb4902f3d70abab85078460bf0e8294feeabadf84ac014ab02918d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:29 GMT
ENV NATS_SERVER=2.12.4
# Wed, 28 Jan 2026 02:18:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Wed, 28 Jan 2026 02:18:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='44a6ff34eff7e8d0e1409dbac0b733cff7ecbb4f19388a4d0d3d6085d899f017' ;;     armhf) natsArch='arm6'; sha256='4e59df78e00edb75544aac70e1e99008cd97a039fad6ea1942b7986ee7289245' ;;     armv7) natsArch='arm7'; sha256='67e7708005b615d1b63280c752616ff8663fa8bd3e83bb24890905b9a0a4e789' ;;     x86_64) natsArch='amd64'; sha256='92388f2e4aa1e6dea402eb173cbdb1fcb1df9a9c899cb807b91ddbb45c131b65' ;;     x86) natsArch='386'; sha256='0899515b18dcbfba3572e91ea0bf7b7577a00d102ca91be44840a8a1ad68b4d7' ;;     s390x) natsArch='s390x'; sha256='8c084d41b8ef405c31ff75f84bb03028295001f9741724a8d0fb2c28aa0f3690' ;;     ppc64le) natsArch='ppc64le'; sha256='5b073b7cdfb91b30f226a687311193ce4544700eaf69fd32df2809451e9e5fc0' ;;     loong64) natsArch='loong64'; sha256='e58995ac0402050a0bd6a9513fc144e9f8f6bb01224fdeb5476691cad187a1c7' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 02:18:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1822544e81552ae13f7653d74e8288b2bb4efff0a869ae0afdb9d14c624114c6`  
		Last Modified: Wed, 28 Jan 2026 02:18:33 GMT  
		Size: 6.5 MB (6469070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7096e6f0d1ac353b6a3082fade15d144a8d723625ddeadd9f8700a5df3ff79`  
		Last Modified: Wed, 28 Jan 2026 02:18:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a564e671e16521db7d3cfb70274079c8d887769598e151621d92f89057d036e5`  
		Last Modified: Wed, 28 Jan 2026 02:18:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:dd4432ebfa5c11bb579d7cc8c5617c7162aef96640ce40274da31fa03f5eff58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8e2f32c72b350cf4347b211d42816b189201c0774bb72dbdbe6f447bbd4ae6`

```dockerfile
```

-	Layers:
	-	`sha256:d59453e8dc8cfaf6e5c46143f3bbe615e0b4552eb505d3b2db3548c541c04594`  
		Last Modified: Wed, 28 Jan 2026 02:18:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:242d9dc765cb5b612c1758d0600274f601af275d3c7e593b61ac7f9296d5de33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0cd1feec1da5b6b7fa386873251c01f31ca6b27979b4fbe1a1bf7ce6755479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:35:04 GMT
ENV NATS_SERVER=2.12.4
# Wed, 28 Jan 2026 02:35:04 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Wed, 28 Jan 2026 02:35:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='44a6ff34eff7e8d0e1409dbac0b733cff7ecbb4f19388a4d0d3d6085d899f017' ;;     armhf) natsArch='arm6'; sha256='4e59df78e00edb75544aac70e1e99008cd97a039fad6ea1942b7986ee7289245' ;;     armv7) natsArch='arm7'; sha256='67e7708005b615d1b63280c752616ff8663fa8bd3e83bb24890905b9a0a4e789' ;;     x86_64) natsArch='amd64'; sha256='92388f2e4aa1e6dea402eb173cbdb1fcb1df9a9c899cb807b91ddbb45c131b65' ;;     x86) natsArch='386'; sha256='0899515b18dcbfba3572e91ea0bf7b7577a00d102ca91be44840a8a1ad68b4d7' ;;     s390x) natsArch='s390x'; sha256='8c084d41b8ef405c31ff75f84bb03028295001f9741724a8d0fb2c28aa0f3690' ;;     ppc64le) natsArch='ppc64le'; sha256='5b073b7cdfb91b30f226a687311193ce4544700eaf69fd32df2809451e9e5fc0' ;;     loong64) natsArch='loong64'; sha256='e58995ac0402050a0bd6a9513fc144e9f8f6bb01224fdeb5476691cad187a1c7' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 28 Jan 2026 02:35:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 28 Jan 2026 02:35:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 28 Jan 2026 02:35:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 02:35:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84147a59d31c7f9c2780a1992852c031b75236cb0e89f49ce197a35821de105f`  
		Last Modified: Wed, 28 Jan 2026 02:35:14 GMT  
		Size: 6.5 MB (6519029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03fac75cf7049455170e27923866db34d10a3d5c26add784969ae48cac5db20`  
		Last Modified: Wed, 28 Jan 2026 02:35:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5323a65f58a6a07cd25cdbe725d5c311647f7832b17a39964619fb826889ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:13 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:64cae85877a781a6a3715811f47721796595030701518ba5feaf6dedb9f2a343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a462304addd89cc67ed0881e5e574ccdee34a1e1cc3fdd3422cc619877067a15`

```dockerfile
```

-	Layers:
	-	`sha256:e4cb677f51ac5207db78ce533d80881f1181df93df5858c71eff05bfdc06df85`  
		Last Modified: Wed, 28 Jan 2026 02:35:14 GMT  
		Size: 15.5 KB (15471 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:8b870b281b8957474eba23de65cbd243ac4c2b29314aea33d7c521f87e9f22db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd9dde14b67dd0bcfbf82c274cafc9292733308c8be7058ddf3a18cb472a98c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
ENV NATS_SERVER=2.12.4
# Wed, 28 Jan 2026 02:21:03 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='44a6ff34eff7e8d0e1409dbac0b733cff7ecbb4f19388a4d0d3d6085d899f017' ;;     armhf) natsArch='arm6'; sha256='4e59df78e00edb75544aac70e1e99008cd97a039fad6ea1942b7986ee7289245' ;;     armv7) natsArch='arm7'; sha256='67e7708005b615d1b63280c752616ff8663fa8bd3e83bb24890905b9a0a4e789' ;;     x86_64) natsArch='amd64'; sha256='92388f2e4aa1e6dea402eb173cbdb1fcb1df9a9c899cb807b91ddbb45c131b65' ;;     x86) natsArch='386'; sha256='0899515b18dcbfba3572e91ea0bf7b7577a00d102ca91be44840a8a1ad68b4d7' ;;     s390x) natsArch='s390x'; sha256='8c084d41b8ef405c31ff75f84bb03028295001f9741724a8d0fb2c28aa0f3690' ;;     ppc64le) natsArch='ppc64le'; sha256='5b073b7cdfb91b30f226a687311193ce4544700eaf69fd32df2809451e9e5fc0' ;;     loong64) natsArch='loong64'; sha256='e58995ac0402050a0bd6a9513fc144e9f8f6bb01224fdeb5476691cad187a1c7' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9724378c32466842392e8daedbc8c36e27b6a422c6ad77018d13a3866f3d0c`  
		Last Modified: Wed, 28 Jan 2026 02:21:10 GMT  
		Size: 6.9 MB (6899881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9e5eb491008161179385869ab813d7a47155ece2715d8b1cbf3665dcb11db`  
		Last Modified: Wed, 28 Jan 2026 02:21:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed70be5c18677ddb16e3e590514ed8c2186786f4a152a4b84e85997b8ae9cea`  
		Last Modified: Wed, 28 Jan 2026 02:21:10 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:bc1aec1b954260e9f716aa99e1e9c7e4bcb3977dff08dccba6e9983c02e16f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52796605c504c4db2e2c4063d1ed9ce133fc172a72f2536e5aad87ab4d7f975e`

```dockerfile
```

-	Layers:
	-	`sha256:dd896901fa33044cad69af99c6b8babc7ba32fe143f312c3d73eae1bf110d028`  
		Last Modified: Wed, 28 Jan 2026 02:21:11 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
