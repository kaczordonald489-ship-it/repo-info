<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.31`](#traefik21131)
-	[`traefik:2.11.31-nanoserver-ltsc2022`](#traefik21131-nanoserver-ltsc2022)
-	[`traefik:2.11.31-windowsservercore-ltsc2022`](#traefik21131-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.2`](#traefik362)
-	[`traefik:3.6.2-nanoserver-ltsc2022`](#traefik362-nanoserver-ltsc2022)
-	[`traefik:3.6.2-windowsservercore-ltsc2022`](#traefik362-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:ramequin`](#traefikramequin)
-	[`traefik:ramequin-nanoserver-ltsc2022`](#traefikramequin-nanoserver-ltsc2022)
-	[`traefik:ramequin-windowsservercore-ltsc2022`](#traefikramequin-windowsservercore-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.31`](#traefikv21131)
-	[`traefik:v2.11.31-nanoserver-ltsc2022`](#traefikv21131-nanoserver-ltsc2022)
-	[`traefik:v2.11.31-windowsservercore-ltsc2022`](#traefikv21131-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.2`](#traefikv362)
-	[`traefik:v3.6.2-nanoserver-ltsc2022`](#traefikv362-nanoserver-ltsc2022)
-	[`traefik:v3.6.2-windowsservercore-ltsc2022`](#traefikv362-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:2` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:2.11` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.31`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:2.11.31` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.31-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11.31-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.31-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11.31-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

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

### `traefik:3` - linux; amd64

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; arm variant v6

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; arm64 variant v8

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; ppc64le

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; riscv64

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; s390x

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

### `traefik:3` - unknown; unknown

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

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

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

### `traefik:3.6` - linux; amd64

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

### `traefik:3.6` - unknown; unknown

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

### `traefik:3.6` - linux; arm variant v6

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

### `traefik:3.6` - unknown; unknown

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

### `traefik:3.6` - linux; arm64 variant v8

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

### `traefik:3.6` - unknown; unknown

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

### `traefik:3.6` - linux; ppc64le

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

### `traefik:3.6` - unknown; unknown

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

### `traefik:3.6` - linux; riscv64

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

### `traefik:3.6` - unknown; unknown

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

### `traefik:3.6` - linux; s390x

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

### `traefik:3.6` - unknown; unknown

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

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.2`

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

### `traefik:3.6.2` - linux; amd64

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

### `traefik:3.6.2` - unknown; unknown

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

### `traefik:3.6.2` - linux; arm variant v6

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

### `traefik:3.6.2` - unknown; unknown

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

### `traefik:3.6.2` - linux; arm64 variant v8

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

### `traefik:3.6.2` - unknown; unknown

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

### `traefik:3.6.2` - linux; ppc64le

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

### `traefik:3.6.2` - unknown; unknown

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

### `traefik:3.6.2` - linux; riscv64

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

### `traefik:3.6.2` - unknown; unknown

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

### `traefik:3.6.2` - linux; s390x

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

### `traefik:3.6.2` - unknown; unknown

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

## `traefik:3.6.2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6.2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

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

### `traefik:latest` - linux; amd64

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; arm variant v6

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; arm64 variant v8

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; ppc64le

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; riscv64

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; s390x

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

### `traefik:latest` - unknown; unknown

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

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:v2` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:v2.11` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.31`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:v2.11.31` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.31-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11.31-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.31-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11.31-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

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

### `traefik:v3` - linux; amd64

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; arm variant v6

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; arm64 variant v8

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; ppc64le

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; riscv64

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; s390x

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

### `traefik:v3` - unknown; unknown

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

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

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

### `traefik:v3.6` - linux; amd64

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

### `traefik:v3.6` - unknown; unknown

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

### `traefik:v3.6` - linux; arm variant v6

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

### `traefik:v3.6` - unknown; unknown

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

### `traefik:v3.6` - linux; arm64 variant v8

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

### `traefik:v3.6` - unknown; unknown

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

### `traefik:v3.6` - linux; ppc64le

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

### `traefik:v3.6` - unknown; unknown

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

### `traefik:v3.6` - linux; riscv64

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

### `traefik:v3.6` - unknown; unknown

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

### `traefik:v3.6` - linux; s390x

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

### `traefik:v3.6` - unknown; unknown

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

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.2`

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

### `traefik:v3.6.2` - linux; amd64

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

### `traefik:v3.6.2` - unknown; unknown

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

### `traefik:v3.6.2` - linux; arm variant v6

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

### `traefik:v3.6.2` - unknown; unknown

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

### `traefik:v3.6.2` - linux; arm64 variant v8

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

### `traefik:v3.6.2` - unknown; unknown

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

### `traefik:v3.6.2` - linux; ppc64le

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

### `traefik:v3.6.2` - unknown; unknown

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

### `traefik:v3.6.2` - linux; riscv64

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

### `traefik:v3.6.2` - unknown; unknown

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

### `traefik:v3.6.2` - linux; s390x

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

### `traefik:v3.6.2` - unknown; unknown

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

## `traefik:v3.6.2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6.2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
