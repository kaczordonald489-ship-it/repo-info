## `traefik:ramequin`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:ramequin` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json
