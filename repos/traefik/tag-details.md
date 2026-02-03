<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.36`](#traefik21136)
-	[`traefik:2.11.36-nanoserver-ltsc2022`](#traefik21136-nanoserver-ltsc2022)
-	[`traefik:2.11.36-windowsservercore-ltsc2022`](#traefik21136-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.7`](#traefik367)
-	[`traefik:3.6.7-nanoserver-ltsc2022`](#traefik367-nanoserver-ltsc2022)
-	[`traefik:3.6.7-windowsservercore-ltsc2022`](#traefik367-windowsservercore-ltsc2022)
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
-	[`traefik:v2.11.36`](#traefikv21136)
-	[`traefik:v2.11.36-nanoserver-ltsc2022`](#traefikv21136-nanoserver-ltsc2022)
-	[`traefik:v2.11.36-windowsservercore-ltsc2022`](#traefikv21136-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.7`](#traefikv367)
-	[`traefik:v3.6.7-nanoserver-ltsc2022`](#traefikv367-nanoserver-ltsc2022)
-	[`traefik:v3.6.7-windowsservercore-ltsc2022`](#traefikv367-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:6ca360db0fbc2f150415b1155d99213ee56d4f1a73d90474301d944943e1a850
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
$ docker pull traefik@sha256:32a30df3a661d213b3283d194aa3893cae9caf73fce2232e9874272e5d29efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340548c740e253c703c6b801d23a1f6a49a8a9929e520185a40695cd5f9e1de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:20:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:20:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f2786675ef53faf7d7614172f9443975122a1b1ae64cd2569afaf96c41c7f2`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 461.0 KB (460951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc916c0d969ec35d695c846b073b1b1b91bf77b063a67ec11c18ad0e9a80c3`  
		Last Modified: Mon, 02 Feb 2026 19:20:33 GMT  
		Size: 46.8 MB (46824091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2013761267b39711282c021b9c5777e0ed3dcd4935afd5eb907b99f812ddf`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c0773956eacc3d9010e58a06a7ad2fd854ba3f499bd65987c6715f017a14b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b11a49a8583fa61436b5f9788bb7b9000636544d1bfd81a9bc7af002c21044`

```dockerfile
```

-	Layers:
	-	`sha256:ef3309bd98bbe3cff86b4c3fe9fe64d9e0317ad73e14e87a584968588d9cb6ac`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51b5719639e240ee9da354d652b0548f752a9fadbfe98a1d586ae8be2fde209`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d4574561869dbcba3ceaff23fc0788a14e6c6312ace734594b7dd0258a47b1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d9a56e76f976f87aea78762fb21a347964d8af628083946540a3bf7a753671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:19:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:32 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a4a9b6b9676c19d79002ed3e7d9e3aa82e0d76fe0d8864c957f1e9d55168ed`  
		Last Modified: Mon, 02 Feb 2026 19:19:40 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb176de5ae6175882b58168e955d155949a2387ad424ef44dedc3cb97308c4`  
		Last Modified: Mon, 02 Feb 2026 19:19:41 GMT  
		Size: 42.9 MB (42851387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6e178dc0f68f29f2e284e3dc88b79a46bab88ed786dab5da0eb7e0eac58a2`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:cfbeea50418380014cb82f0ab50e081489a69c9f13c64917cc4d60b18d70b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67671f8be07fe685feed12b91f122c7c05cea55d9cb74f8520da1cb71ff04540`

```dockerfile
```

-	Layers:
	-	`sha256:27bf125363d18322cdb1a86703b4db6e0b22adbd5dab554dacac5946eaa3e983`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19b85f525731d2e3dae5ea04044c2d4a7dadd9654ae5cccc8376e8d52238efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feada2dc396baa2615171b3d750ba5f367ad9cf371f6ab6aa0a80053d989305`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:24:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:24:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760a4e7f97791609aa051682708c95b35de5fe9cc6f296231465d8d08cd812d`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 463.0 KB (463011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e88306c87b340425aa60ae18cff826197a37d08e6f28bcb8041b13cd4512`  
		Last Modified: Mon, 02 Feb 2026 19:24:37 GMT  
		Size: 42.1 MB (42109642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a64a2e8c4ae63bd423fc78f6da3de120d6cb7afb00e2fb811d90a06d4ad222`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a2f4ea11ef5a33c4d78d6eb96f7b98cdfc73c94355397341e1304a69e70f0d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17237fa8264f3b3ccbd7d1a803277a7389abb3377f433424894cad517eaf49ec`

```dockerfile
```

-	Layers:
	-	`sha256:92669e16a7fca33855e7b84fc0d85d499bae208e891d503dee468959b8b64be3`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540e481eee38c62376d8b04e565c69ea3e3acad3df55ddd48bbda0e127ca33c`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a4c0d555390f89f254be8955dcb866664401c9b02f02277821c3abf135015c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dfa5fd5676302535f3ee212252e73de7678216963cb905c4405a7d52443ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:18:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:00 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa218b5bedd12623a723833cd6946e5b5d62f5ecc64582746b3e1d80740135f`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 463.5 KB (463527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efd8826a5ff2fa3dc5f24dcc15c3db4cc519fd089f8c57bd7ae973e2edeba5`  
		Last Modified: Mon, 02 Feb 2026 19:19:54 GMT  
		Size: 41.1 MB (41058027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216f00a2112efdba5a3f6a030ce039e30f5e1c0191e8fc23f5e96a7e216ceb8`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:525a1bac2c221c0c843fb1d225bd15d1741a3e49896795136b4e283acf355c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cea6d71b657acbabfd505c8a223eab8b8e20f6190dc48cb9f23da89ace1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ce1efd0e4598b024a13ee8350c8b23381bd5e1f4a39576f421927ecfc9d92`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45ccf22c5bb5800544b273cd9dec64a78d473a288af8961d138407b4ff36a0`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:74ebe09868f81a2e9e0444d0a1de76aba73a45df6d8513285890f27023bb4fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a72913bdaaed333ef8ad012d63dc268f23081f78ef2c8c3ac8c1d3df3205d49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 19:06:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 19:06:31 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 19:06:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec037c2d893d7d29b7afede297802111719ead4b63664808242a3630fb16b91a`  
		Last Modified: Thu, 29 Jan 2026 19:11:27 GMT  
		Size: 45.3 MB (45325193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63acc32e46aa68086758b34a77f1e96b4d4d6e7808474c578ab6d07791bda83`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:574c6c8cc03fe79bf98cf9b54cd3ad40b5ce4d0ae959a228982998fd2dccb746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c66325e70ceb1c7e41957f16488f268f9ab12fcc781cda3ae1dd6304c74193a`

```dockerfile
```

-	Layers:
	-	`sha256:59dcd5eedbfd366ebe44be1ae13702861d40f3e00c4234cf6aa4616f2bde44dd`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfd7f8f4b46f541575dc51c3c2c718782b260d479bf557c37eafdf78b0aee03`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:3a5b28df2712e797c55b80b393d4f3081be5499046bd322368b2c88eacbb82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b43eb5dec4846e5afbd335d9d236b549f598da9c1bd21087d157721443d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:08 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c59e88b8945e71acb4f8f932a7c082a2d71ee4e61e549a4014e08a3e0cb653`  
		Last Modified: Mon, 02 Feb 2026 19:19:57 GMT  
		Size: 45.3 MB (45289326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc755ae19df08a4aba8c642cb3a4e7da4289d2fe21c4ad2450c30f2ed53699d1`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:f473f7ef16753708c841171ee8fcb75da0ed1b1c94c9b742c0ef4d5d9a358436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72053089031553af326e08d00875b5f2e05442f5c4ec8d343b3bc0772c7dd578`

```dockerfile
```

-	Layers:
	-	`sha256:43e3b17de8448cc504dc90998d5b30a1c3b893dc1fbbd1a1eabeb47342beedf7`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94706cb0698d6979497f3ade2388839d15910ec569a123c79f9949b59e15f95e`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d92a7468aee7f1df38369e9d817d13956c51a070458e3d8473ca20ee1b162917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:fa8dcc7dc8a27e8fac41bb0c3fda6200e33143bc5d05ad7687be7867230f87f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56f2ce9a331443214d5aa465eee78d3cbed6cb18fe51a8af9e5eda228f5059`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 02 Feb 2026 20:44:57 GMT
RUN cmd /S /C #(nop) COPY file:0b0150726a403f05ecd4788bbb4d84dbd236c80829e39a8e79edf4cc9e33137f in \ 
# Mon, 02 Feb 2026 20:44:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e487e7b658ecea2210e57410d93f8908fce2fa3e646f4e7da7012cfd8d242`  
		Last Modified: Mon, 02 Feb 2026 20:45:19 GMT  
		Size: 47.6 MB (47632503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a0aade23718702fc88e49f20a7b71d2277787261a242bf328d92a8eb7519a3`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd04af343a3432e3644907bdbbbf5ed02691378a5069713ac5065afac6433c`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13ca5eabe4abc4fd35a9b6c4485e3c397db223c65b1e3d910adfa5c43f7fb9`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:6ca360db0fbc2f150415b1155d99213ee56d4f1a73d90474301d944943e1a850
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
$ docker pull traefik@sha256:32a30df3a661d213b3283d194aa3893cae9caf73fce2232e9874272e5d29efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340548c740e253c703c6b801d23a1f6a49a8a9929e520185a40695cd5f9e1de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:20:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:20:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f2786675ef53faf7d7614172f9443975122a1b1ae64cd2569afaf96c41c7f2`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 461.0 KB (460951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc916c0d969ec35d695c846b073b1b1b91bf77b063a67ec11c18ad0e9a80c3`  
		Last Modified: Mon, 02 Feb 2026 19:20:33 GMT  
		Size: 46.8 MB (46824091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2013761267b39711282c021b9c5777e0ed3dcd4935afd5eb907b99f812ddf`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c0773956eacc3d9010e58a06a7ad2fd854ba3f499bd65987c6715f017a14b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b11a49a8583fa61436b5f9788bb7b9000636544d1bfd81a9bc7af002c21044`

```dockerfile
```

-	Layers:
	-	`sha256:ef3309bd98bbe3cff86b4c3fe9fe64d9e0317ad73e14e87a584968588d9cb6ac`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51b5719639e240ee9da354d652b0548f752a9fadbfe98a1d586ae8be2fde209`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d4574561869dbcba3ceaff23fc0788a14e6c6312ace734594b7dd0258a47b1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d9a56e76f976f87aea78762fb21a347964d8af628083946540a3bf7a753671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:19:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:32 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a4a9b6b9676c19d79002ed3e7d9e3aa82e0d76fe0d8864c957f1e9d55168ed`  
		Last Modified: Mon, 02 Feb 2026 19:19:40 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb176de5ae6175882b58168e955d155949a2387ad424ef44dedc3cb97308c4`  
		Last Modified: Mon, 02 Feb 2026 19:19:41 GMT  
		Size: 42.9 MB (42851387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6e178dc0f68f29f2e284e3dc88b79a46bab88ed786dab5da0eb7e0eac58a2`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cfbeea50418380014cb82f0ab50e081489a69c9f13c64917cc4d60b18d70b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67671f8be07fe685feed12b91f122c7c05cea55d9cb74f8520da1cb71ff04540`

```dockerfile
```

-	Layers:
	-	`sha256:27bf125363d18322cdb1a86703b4db6e0b22adbd5dab554dacac5946eaa3e983`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19b85f525731d2e3dae5ea04044c2d4a7dadd9654ae5cccc8376e8d52238efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feada2dc396baa2615171b3d750ba5f367ad9cf371f6ab6aa0a80053d989305`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:24:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:24:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760a4e7f97791609aa051682708c95b35de5fe9cc6f296231465d8d08cd812d`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 463.0 KB (463011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e88306c87b340425aa60ae18cff826197a37d08e6f28bcb8041b13cd4512`  
		Last Modified: Mon, 02 Feb 2026 19:24:37 GMT  
		Size: 42.1 MB (42109642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a64a2e8c4ae63bd423fc78f6da3de120d6cb7afb00e2fb811d90a06d4ad222`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a2f4ea11ef5a33c4d78d6eb96f7b98cdfc73c94355397341e1304a69e70f0d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17237fa8264f3b3ccbd7d1a803277a7389abb3377f433424894cad517eaf49ec`

```dockerfile
```

-	Layers:
	-	`sha256:92669e16a7fca33855e7b84fc0d85d499bae208e891d503dee468959b8b64be3`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540e481eee38c62376d8b04e565c69ea3e3acad3df55ddd48bbda0e127ca33c`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a4c0d555390f89f254be8955dcb866664401c9b02f02277821c3abf135015c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dfa5fd5676302535f3ee212252e73de7678216963cb905c4405a7d52443ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:18:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:00 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa218b5bedd12623a723833cd6946e5b5d62f5ecc64582746b3e1d80740135f`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 463.5 KB (463527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efd8826a5ff2fa3dc5f24dcc15c3db4cc519fd089f8c57bd7ae973e2edeba5`  
		Last Modified: Mon, 02 Feb 2026 19:19:54 GMT  
		Size: 41.1 MB (41058027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216f00a2112efdba5a3f6a030ce039e30f5e1c0191e8fc23f5e96a7e216ceb8`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:525a1bac2c221c0c843fb1d225bd15d1741a3e49896795136b4e283acf355c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cea6d71b657acbabfd505c8a223eab8b8e20f6190dc48cb9f23da89ace1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ce1efd0e4598b024a13ee8350c8b23381bd5e1f4a39576f421927ecfc9d92`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45ccf22c5bb5800544b273cd9dec64a78d473a288af8961d138407b4ff36a0`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:74ebe09868f81a2e9e0444d0a1de76aba73a45df6d8513285890f27023bb4fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a72913bdaaed333ef8ad012d63dc268f23081f78ef2c8c3ac8c1d3df3205d49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 19:06:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 19:06:31 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 19:06:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec037c2d893d7d29b7afede297802111719ead4b63664808242a3630fb16b91a`  
		Last Modified: Thu, 29 Jan 2026 19:11:27 GMT  
		Size: 45.3 MB (45325193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63acc32e46aa68086758b34a77f1e96b4d4d6e7808474c578ab6d07791bda83`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:574c6c8cc03fe79bf98cf9b54cd3ad40b5ce4d0ae959a228982998fd2dccb746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c66325e70ceb1c7e41957f16488f268f9ab12fcc781cda3ae1dd6304c74193a`

```dockerfile
```

-	Layers:
	-	`sha256:59dcd5eedbfd366ebe44be1ae13702861d40f3e00c4234cf6aa4616f2bde44dd`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfd7f8f4b46f541575dc51c3c2c718782b260d479bf557c37eafdf78b0aee03`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:3a5b28df2712e797c55b80b393d4f3081be5499046bd322368b2c88eacbb82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b43eb5dec4846e5afbd335d9d236b549f598da9c1bd21087d157721443d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:08 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c59e88b8945e71acb4f8f932a7c082a2d71ee4e61e549a4014e08a3e0cb653`  
		Last Modified: Mon, 02 Feb 2026 19:19:57 GMT  
		Size: 45.3 MB (45289326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc755ae19df08a4aba8c642cb3a4e7da4289d2fe21c4ad2450c30f2ed53699d1`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f473f7ef16753708c841171ee8fcb75da0ed1b1c94c9b742c0ef4d5d9a358436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72053089031553af326e08d00875b5f2e05442f5c4ec8d343b3bc0772c7dd578`

```dockerfile
```

-	Layers:
	-	`sha256:43e3b17de8448cc504dc90998d5b30a1c3b893dc1fbbd1a1eabeb47342beedf7`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94706cb0698d6979497f3ade2388839d15910ec569a123c79f9949b59e15f95e`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d92a7468aee7f1df38369e9d817d13956c51a070458e3d8473ca20ee1b162917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:fa8dcc7dc8a27e8fac41bb0c3fda6200e33143bc5d05ad7687be7867230f87f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56f2ce9a331443214d5aa465eee78d3cbed6cb18fe51a8af9e5eda228f5059`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 02 Feb 2026 20:44:57 GMT
RUN cmd /S /C #(nop) COPY file:0b0150726a403f05ecd4788bbb4d84dbd236c80829e39a8e79edf4cc9e33137f in \ 
# Mon, 02 Feb 2026 20:44:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e487e7b658ecea2210e57410d93f8908fce2fa3e646f4e7da7012cfd8d242`  
		Last Modified: Mon, 02 Feb 2026 20:45:19 GMT  
		Size: 47.6 MB (47632503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a0aade23718702fc88e49f20a7b71d2277787261a242bf328d92a8eb7519a3`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd04af343a3432e3644907bdbbbf5ed02691378a5069713ac5065afac6433c`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13ca5eabe4abc4fd35a9b6c4485e3c397db223c65b1e3d910adfa5c43f7fb9`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.36`

```console
$ docker pull traefik@sha256:ea36eb2360592c76d8eb925accbfae8ad6b4586ecbb90b3d81c438d70ff63ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11.36` - linux; amd64

```console
$ docker pull traefik@sha256:32a30df3a661d213b3283d194aa3893cae9caf73fce2232e9874272e5d29efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340548c740e253c703c6b801d23a1f6a49a8a9929e520185a40695cd5f9e1de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:20:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:20:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f2786675ef53faf7d7614172f9443975122a1b1ae64cd2569afaf96c41c7f2`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 461.0 KB (460951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc916c0d969ec35d695c846b073b1b1b91bf77b063a67ec11c18ad0e9a80c3`  
		Last Modified: Mon, 02 Feb 2026 19:20:33 GMT  
		Size: 46.8 MB (46824091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2013761267b39711282c021b9c5777e0ed3dcd4935afd5eb907b99f812ddf`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:c0773956eacc3d9010e58a06a7ad2fd854ba3f499bd65987c6715f017a14b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b11a49a8583fa61436b5f9788bb7b9000636544d1bfd81a9bc7af002c21044`

```dockerfile
```

-	Layers:
	-	`sha256:ef3309bd98bbe3cff86b4c3fe9fe64d9e0317ad73e14e87a584968588d9cb6ac`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51b5719639e240ee9da354d652b0548f752a9fadbfe98a1d586ae8be2fde209`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.36` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d4574561869dbcba3ceaff23fc0788a14e6c6312ace734594b7dd0258a47b1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d9a56e76f976f87aea78762fb21a347964d8af628083946540a3bf7a753671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:19:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:32 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a4a9b6b9676c19d79002ed3e7d9e3aa82e0d76fe0d8864c957f1e9d55168ed`  
		Last Modified: Mon, 02 Feb 2026 19:19:40 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb176de5ae6175882b58168e955d155949a2387ad424ef44dedc3cb97308c4`  
		Last Modified: Mon, 02 Feb 2026 19:19:41 GMT  
		Size: 42.9 MB (42851387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6e178dc0f68f29f2e284e3dc88b79a46bab88ed786dab5da0eb7e0eac58a2`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:cfbeea50418380014cb82f0ab50e081489a69c9f13c64917cc4d60b18d70b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67671f8be07fe685feed12b91f122c7c05cea55d9cb74f8520da1cb71ff04540`

```dockerfile
```

-	Layers:
	-	`sha256:27bf125363d18322cdb1a86703b4db6e0b22adbd5dab554dacac5946eaa3e983`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.36` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19b85f525731d2e3dae5ea04044c2d4a7dadd9654ae5cccc8376e8d52238efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feada2dc396baa2615171b3d750ba5f367ad9cf371f6ab6aa0a80053d989305`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:24:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:24:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760a4e7f97791609aa051682708c95b35de5fe9cc6f296231465d8d08cd812d`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 463.0 KB (463011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e88306c87b340425aa60ae18cff826197a37d08e6f28bcb8041b13cd4512`  
		Last Modified: Mon, 02 Feb 2026 19:24:37 GMT  
		Size: 42.1 MB (42109642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a64a2e8c4ae63bd423fc78f6da3de120d6cb7afb00e2fb811d90a06d4ad222`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:a2f4ea11ef5a33c4d78d6eb96f7b98cdfc73c94355397341e1304a69e70f0d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17237fa8264f3b3ccbd7d1a803277a7389abb3377f433424894cad517eaf49ec`

```dockerfile
```

-	Layers:
	-	`sha256:92669e16a7fca33855e7b84fc0d85d499bae208e891d503dee468959b8b64be3`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540e481eee38c62376d8b04e565c69ea3e3acad3df55ddd48bbda0e127ca33c`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.36` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a4c0d555390f89f254be8955dcb866664401c9b02f02277821c3abf135015c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dfa5fd5676302535f3ee212252e73de7678216963cb905c4405a7d52443ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:18:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:00 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa218b5bedd12623a723833cd6946e5b5d62f5ecc64582746b3e1d80740135f`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 463.5 KB (463527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efd8826a5ff2fa3dc5f24dcc15c3db4cc519fd089f8c57bd7ae973e2edeba5`  
		Last Modified: Mon, 02 Feb 2026 19:19:54 GMT  
		Size: 41.1 MB (41058027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216f00a2112efdba5a3f6a030ce039e30f5e1c0191e8fc23f5e96a7e216ceb8`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:525a1bac2c221c0c843fb1d225bd15d1741a3e49896795136b4e283acf355c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cea6d71b657acbabfd505c8a223eab8b8e20f6190dc48cb9f23da89ace1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ce1efd0e4598b024a13ee8350c8b23381bd5e1f4a39576f421927ecfc9d92`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45ccf22c5bb5800544b273cd9dec64a78d473a288af8961d138407b4ff36a0`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.36` - linux; s390x

```console
$ docker pull traefik@sha256:3a5b28df2712e797c55b80b393d4f3081be5499046bd322368b2c88eacbb82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b43eb5dec4846e5afbd335d9d236b549f598da9c1bd21087d157721443d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:08 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c59e88b8945e71acb4f8f932a7c082a2d71ee4e61e549a4014e08a3e0cb653`  
		Last Modified: Mon, 02 Feb 2026 19:19:57 GMT  
		Size: 45.3 MB (45289326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc755ae19df08a4aba8c642cb3a4e7da4289d2fe21c4ad2450c30f2ed53699d1`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:f473f7ef16753708c841171ee8fcb75da0ed1b1c94c9b742c0ef4d5d9a358436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72053089031553af326e08d00875b5f2e05442f5c4ec8d343b3bc0772c7dd578`

```dockerfile
```

-	Layers:
	-	`sha256:43e3b17de8448cc504dc90998d5b30a1c3b893dc1fbbd1a1eabeb47342beedf7`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94706cb0698d6979497f3ade2388839d15910ec569a123c79f9949b59e15f95e`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.36-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d92a7468aee7f1df38369e9d817d13956c51a070458e3d8473ca20ee1b162917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11.36-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:fa8dcc7dc8a27e8fac41bb0c3fda6200e33143bc5d05ad7687be7867230f87f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56f2ce9a331443214d5aa465eee78d3cbed6cb18fe51a8af9e5eda228f5059`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 02 Feb 2026 20:44:57 GMT
RUN cmd /S /C #(nop) COPY file:0b0150726a403f05ecd4788bbb4d84dbd236c80829e39a8e79edf4cc9e33137f in \ 
# Mon, 02 Feb 2026 20:44:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e487e7b658ecea2210e57410d93f8908fce2fa3e646f4e7da7012cfd8d242`  
		Last Modified: Mon, 02 Feb 2026 20:45:19 GMT  
		Size: 47.6 MB (47632503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a0aade23718702fc88e49f20a7b71d2277787261a242bf328d92a8eb7519a3`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd04af343a3432e3644907bdbbbf5ed02691378a5069713ac5065afac6433c`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13ca5eabe4abc4fd35a9b6c4485e3c397db223c65b1e3d910adfa5c43f7fb9`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.36-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11.36-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.7`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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

### `traefik:3.6.7` - linux; amd64

```console
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.7-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6.7-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.7-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:6ca360db0fbc2f150415b1155d99213ee56d4f1a73d90474301d944943e1a850
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
$ docker pull traefik@sha256:32a30df3a661d213b3283d194aa3893cae9caf73fce2232e9874272e5d29efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340548c740e253c703c6b801d23a1f6a49a8a9929e520185a40695cd5f9e1de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:20:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:20:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f2786675ef53faf7d7614172f9443975122a1b1ae64cd2569afaf96c41c7f2`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 461.0 KB (460951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc916c0d969ec35d695c846b073b1b1b91bf77b063a67ec11c18ad0e9a80c3`  
		Last Modified: Mon, 02 Feb 2026 19:20:33 GMT  
		Size: 46.8 MB (46824091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2013761267b39711282c021b9c5777e0ed3dcd4935afd5eb907b99f812ddf`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c0773956eacc3d9010e58a06a7ad2fd854ba3f499bd65987c6715f017a14b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b11a49a8583fa61436b5f9788bb7b9000636544d1bfd81a9bc7af002c21044`

```dockerfile
```

-	Layers:
	-	`sha256:ef3309bd98bbe3cff86b4c3fe9fe64d9e0317ad73e14e87a584968588d9cb6ac`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51b5719639e240ee9da354d652b0548f752a9fadbfe98a1d586ae8be2fde209`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d4574561869dbcba3ceaff23fc0788a14e6c6312ace734594b7dd0258a47b1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d9a56e76f976f87aea78762fb21a347964d8af628083946540a3bf7a753671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:19:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:32 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a4a9b6b9676c19d79002ed3e7d9e3aa82e0d76fe0d8864c957f1e9d55168ed`  
		Last Modified: Mon, 02 Feb 2026 19:19:40 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb176de5ae6175882b58168e955d155949a2387ad424ef44dedc3cb97308c4`  
		Last Modified: Mon, 02 Feb 2026 19:19:41 GMT  
		Size: 42.9 MB (42851387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6e178dc0f68f29f2e284e3dc88b79a46bab88ed786dab5da0eb7e0eac58a2`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:cfbeea50418380014cb82f0ab50e081489a69c9f13c64917cc4d60b18d70b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67671f8be07fe685feed12b91f122c7c05cea55d9cb74f8520da1cb71ff04540`

```dockerfile
```

-	Layers:
	-	`sha256:27bf125363d18322cdb1a86703b4db6e0b22adbd5dab554dacac5946eaa3e983`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19b85f525731d2e3dae5ea04044c2d4a7dadd9654ae5cccc8376e8d52238efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feada2dc396baa2615171b3d750ba5f367ad9cf371f6ab6aa0a80053d989305`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:24:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:24:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760a4e7f97791609aa051682708c95b35de5fe9cc6f296231465d8d08cd812d`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 463.0 KB (463011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e88306c87b340425aa60ae18cff826197a37d08e6f28bcb8041b13cd4512`  
		Last Modified: Mon, 02 Feb 2026 19:24:37 GMT  
		Size: 42.1 MB (42109642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a64a2e8c4ae63bd423fc78f6da3de120d6cb7afb00e2fb811d90a06d4ad222`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a2f4ea11ef5a33c4d78d6eb96f7b98cdfc73c94355397341e1304a69e70f0d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17237fa8264f3b3ccbd7d1a803277a7389abb3377f433424894cad517eaf49ec`

```dockerfile
```

-	Layers:
	-	`sha256:92669e16a7fca33855e7b84fc0d85d499bae208e891d503dee468959b8b64be3`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540e481eee38c62376d8b04e565c69ea3e3acad3df55ddd48bbda0e127ca33c`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a4c0d555390f89f254be8955dcb866664401c9b02f02277821c3abf135015c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dfa5fd5676302535f3ee212252e73de7678216963cb905c4405a7d52443ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:18:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:00 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa218b5bedd12623a723833cd6946e5b5d62f5ecc64582746b3e1d80740135f`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 463.5 KB (463527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efd8826a5ff2fa3dc5f24dcc15c3db4cc519fd089f8c57bd7ae973e2edeba5`  
		Last Modified: Mon, 02 Feb 2026 19:19:54 GMT  
		Size: 41.1 MB (41058027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216f00a2112efdba5a3f6a030ce039e30f5e1c0191e8fc23f5e96a7e216ceb8`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:525a1bac2c221c0c843fb1d225bd15d1741a3e49896795136b4e283acf355c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cea6d71b657acbabfd505c8a223eab8b8e20f6190dc48cb9f23da89ace1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ce1efd0e4598b024a13ee8350c8b23381bd5e1f4a39576f421927ecfc9d92`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45ccf22c5bb5800544b273cd9dec64a78d473a288af8961d138407b4ff36a0`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:74ebe09868f81a2e9e0444d0a1de76aba73a45df6d8513285890f27023bb4fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a72913bdaaed333ef8ad012d63dc268f23081f78ef2c8c3ac8c1d3df3205d49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 19:06:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 19:06:31 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 19:06:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec037c2d893d7d29b7afede297802111719ead4b63664808242a3630fb16b91a`  
		Last Modified: Thu, 29 Jan 2026 19:11:27 GMT  
		Size: 45.3 MB (45325193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63acc32e46aa68086758b34a77f1e96b4d4d6e7808474c578ab6d07791bda83`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:574c6c8cc03fe79bf98cf9b54cd3ad40b5ce4d0ae959a228982998fd2dccb746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c66325e70ceb1c7e41957f16488f268f9ab12fcc781cda3ae1dd6304c74193a`

```dockerfile
```

-	Layers:
	-	`sha256:59dcd5eedbfd366ebe44be1ae13702861d40f3e00c4234cf6aa4616f2bde44dd`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfd7f8f4b46f541575dc51c3c2c718782b260d479bf557c37eafdf78b0aee03`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:3a5b28df2712e797c55b80b393d4f3081be5499046bd322368b2c88eacbb82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b43eb5dec4846e5afbd335d9d236b549f598da9c1bd21087d157721443d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:08 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c59e88b8945e71acb4f8f932a7c082a2d71ee4e61e549a4014e08a3e0cb653`  
		Last Modified: Mon, 02 Feb 2026 19:19:57 GMT  
		Size: 45.3 MB (45289326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc755ae19df08a4aba8c642cb3a4e7da4289d2fe21c4ad2450c30f2ed53699d1`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:f473f7ef16753708c841171ee8fcb75da0ed1b1c94c9b742c0ef4d5d9a358436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72053089031553af326e08d00875b5f2e05442f5c4ec8d343b3bc0772c7dd578`

```dockerfile
```

-	Layers:
	-	`sha256:43e3b17de8448cc504dc90998d5b30a1c3b893dc1fbbd1a1eabeb47342beedf7`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94706cb0698d6979497f3ade2388839d15910ec569a123c79f9949b59e15f95e`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d92a7468aee7f1df38369e9d817d13956c51a070458e3d8473ca20ee1b162917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:fa8dcc7dc8a27e8fac41bb0c3fda6200e33143bc5d05ad7687be7867230f87f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56f2ce9a331443214d5aa465eee78d3cbed6cb18fe51a8af9e5eda228f5059`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 02 Feb 2026 20:44:57 GMT
RUN cmd /S /C #(nop) COPY file:0b0150726a403f05ecd4788bbb4d84dbd236c80829e39a8e79edf4cc9e33137f in \ 
# Mon, 02 Feb 2026 20:44:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e487e7b658ecea2210e57410d93f8908fce2fa3e646f4e7da7012cfd8d242`  
		Last Modified: Mon, 02 Feb 2026 20:45:19 GMT  
		Size: 47.6 MB (47632503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a0aade23718702fc88e49f20a7b71d2277787261a242bf328d92a8eb7519a3`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd04af343a3432e3644907bdbbbf5ed02691378a5069713ac5065afac6433c`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13ca5eabe4abc4fd35a9b6c4485e3c397db223c65b1e3d910adfa5c43f7fb9`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:6ca360db0fbc2f150415b1155d99213ee56d4f1a73d90474301d944943e1a850
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
$ docker pull traefik@sha256:32a30df3a661d213b3283d194aa3893cae9caf73fce2232e9874272e5d29efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340548c740e253c703c6b801d23a1f6a49a8a9929e520185a40695cd5f9e1de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:20:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:20:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f2786675ef53faf7d7614172f9443975122a1b1ae64cd2569afaf96c41c7f2`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 461.0 KB (460951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc916c0d969ec35d695c846b073b1b1b91bf77b063a67ec11c18ad0e9a80c3`  
		Last Modified: Mon, 02 Feb 2026 19:20:33 GMT  
		Size: 46.8 MB (46824091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2013761267b39711282c021b9c5777e0ed3dcd4935afd5eb907b99f812ddf`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c0773956eacc3d9010e58a06a7ad2fd854ba3f499bd65987c6715f017a14b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b11a49a8583fa61436b5f9788bb7b9000636544d1bfd81a9bc7af002c21044`

```dockerfile
```

-	Layers:
	-	`sha256:ef3309bd98bbe3cff86b4c3fe9fe64d9e0317ad73e14e87a584968588d9cb6ac`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51b5719639e240ee9da354d652b0548f752a9fadbfe98a1d586ae8be2fde209`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d4574561869dbcba3ceaff23fc0788a14e6c6312ace734594b7dd0258a47b1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d9a56e76f976f87aea78762fb21a347964d8af628083946540a3bf7a753671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:19:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:32 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a4a9b6b9676c19d79002ed3e7d9e3aa82e0d76fe0d8864c957f1e9d55168ed`  
		Last Modified: Mon, 02 Feb 2026 19:19:40 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb176de5ae6175882b58168e955d155949a2387ad424ef44dedc3cb97308c4`  
		Last Modified: Mon, 02 Feb 2026 19:19:41 GMT  
		Size: 42.9 MB (42851387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6e178dc0f68f29f2e284e3dc88b79a46bab88ed786dab5da0eb7e0eac58a2`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:cfbeea50418380014cb82f0ab50e081489a69c9f13c64917cc4d60b18d70b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67671f8be07fe685feed12b91f122c7c05cea55d9cb74f8520da1cb71ff04540`

```dockerfile
```

-	Layers:
	-	`sha256:27bf125363d18322cdb1a86703b4db6e0b22adbd5dab554dacac5946eaa3e983`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19b85f525731d2e3dae5ea04044c2d4a7dadd9654ae5cccc8376e8d52238efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feada2dc396baa2615171b3d750ba5f367ad9cf371f6ab6aa0a80053d989305`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:24:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:24:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760a4e7f97791609aa051682708c95b35de5fe9cc6f296231465d8d08cd812d`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 463.0 KB (463011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e88306c87b340425aa60ae18cff826197a37d08e6f28bcb8041b13cd4512`  
		Last Modified: Mon, 02 Feb 2026 19:24:37 GMT  
		Size: 42.1 MB (42109642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a64a2e8c4ae63bd423fc78f6da3de120d6cb7afb00e2fb811d90a06d4ad222`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a2f4ea11ef5a33c4d78d6eb96f7b98cdfc73c94355397341e1304a69e70f0d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17237fa8264f3b3ccbd7d1a803277a7389abb3377f433424894cad517eaf49ec`

```dockerfile
```

-	Layers:
	-	`sha256:92669e16a7fca33855e7b84fc0d85d499bae208e891d503dee468959b8b64be3`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540e481eee38c62376d8b04e565c69ea3e3acad3df55ddd48bbda0e127ca33c`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a4c0d555390f89f254be8955dcb866664401c9b02f02277821c3abf135015c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dfa5fd5676302535f3ee212252e73de7678216963cb905c4405a7d52443ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:18:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:00 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa218b5bedd12623a723833cd6946e5b5d62f5ecc64582746b3e1d80740135f`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 463.5 KB (463527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efd8826a5ff2fa3dc5f24dcc15c3db4cc519fd089f8c57bd7ae973e2edeba5`  
		Last Modified: Mon, 02 Feb 2026 19:19:54 GMT  
		Size: 41.1 MB (41058027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216f00a2112efdba5a3f6a030ce039e30f5e1c0191e8fc23f5e96a7e216ceb8`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:525a1bac2c221c0c843fb1d225bd15d1741a3e49896795136b4e283acf355c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cea6d71b657acbabfd505c8a223eab8b8e20f6190dc48cb9f23da89ace1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ce1efd0e4598b024a13ee8350c8b23381bd5e1f4a39576f421927ecfc9d92`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45ccf22c5bb5800544b273cd9dec64a78d473a288af8961d138407b4ff36a0`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:74ebe09868f81a2e9e0444d0a1de76aba73a45df6d8513285890f27023bb4fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a72913bdaaed333ef8ad012d63dc268f23081f78ef2c8c3ac8c1d3df3205d49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 19:06:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 19:06:31 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 19:06:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec037c2d893d7d29b7afede297802111719ead4b63664808242a3630fb16b91a`  
		Last Modified: Thu, 29 Jan 2026 19:11:27 GMT  
		Size: 45.3 MB (45325193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63acc32e46aa68086758b34a77f1e96b4d4d6e7808474c578ab6d07791bda83`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:574c6c8cc03fe79bf98cf9b54cd3ad40b5ce4d0ae959a228982998fd2dccb746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c66325e70ceb1c7e41957f16488f268f9ab12fcc781cda3ae1dd6304c74193a`

```dockerfile
```

-	Layers:
	-	`sha256:59dcd5eedbfd366ebe44be1ae13702861d40f3e00c4234cf6aa4616f2bde44dd`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfd7f8f4b46f541575dc51c3c2c718782b260d479bf557c37eafdf78b0aee03`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:3a5b28df2712e797c55b80b393d4f3081be5499046bd322368b2c88eacbb82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b43eb5dec4846e5afbd335d9d236b549f598da9c1bd21087d157721443d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:08 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c59e88b8945e71acb4f8f932a7c082a2d71ee4e61e549a4014e08a3e0cb653`  
		Last Modified: Mon, 02 Feb 2026 19:19:57 GMT  
		Size: 45.3 MB (45289326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc755ae19df08a4aba8c642cb3a4e7da4289d2fe21c4ad2450c30f2ed53699d1`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:f473f7ef16753708c841171ee8fcb75da0ed1b1c94c9b742c0ef4d5d9a358436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72053089031553af326e08d00875b5f2e05442f5c4ec8d343b3bc0772c7dd578`

```dockerfile
```

-	Layers:
	-	`sha256:43e3b17de8448cc504dc90998d5b30a1c3b893dc1fbbd1a1eabeb47342beedf7`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94706cb0698d6979497f3ade2388839d15910ec569a123c79f9949b59e15f95e`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d92a7468aee7f1df38369e9d817d13956c51a070458e3d8473ca20ee1b162917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:fa8dcc7dc8a27e8fac41bb0c3fda6200e33143bc5d05ad7687be7867230f87f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56f2ce9a331443214d5aa465eee78d3cbed6cb18fe51a8af9e5eda228f5059`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 02 Feb 2026 20:44:57 GMT
RUN cmd /S /C #(nop) COPY file:0b0150726a403f05ecd4788bbb4d84dbd236c80829e39a8e79edf4cc9e33137f in \ 
# Mon, 02 Feb 2026 20:44:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e487e7b658ecea2210e57410d93f8908fce2fa3e646f4e7da7012cfd8d242`  
		Last Modified: Mon, 02 Feb 2026 20:45:19 GMT  
		Size: 47.6 MB (47632503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a0aade23718702fc88e49f20a7b71d2277787261a242bf328d92a8eb7519a3`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd04af343a3432e3644907bdbbbf5ed02691378a5069713ac5065afac6433c`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13ca5eabe4abc4fd35a9b6c4485e3c397db223c65b1e3d910adfa5c43f7fb9`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:6ca360db0fbc2f150415b1155d99213ee56d4f1a73d90474301d944943e1a850
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
$ docker pull traefik@sha256:32a30df3a661d213b3283d194aa3893cae9caf73fce2232e9874272e5d29efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340548c740e253c703c6b801d23a1f6a49a8a9929e520185a40695cd5f9e1de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:20:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:20:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f2786675ef53faf7d7614172f9443975122a1b1ae64cd2569afaf96c41c7f2`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 461.0 KB (460951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc916c0d969ec35d695c846b073b1b1b91bf77b063a67ec11c18ad0e9a80c3`  
		Last Modified: Mon, 02 Feb 2026 19:20:33 GMT  
		Size: 46.8 MB (46824091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2013761267b39711282c021b9c5777e0ed3dcd4935afd5eb907b99f812ddf`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c0773956eacc3d9010e58a06a7ad2fd854ba3f499bd65987c6715f017a14b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b11a49a8583fa61436b5f9788bb7b9000636544d1bfd81a9bc7af002c21044`

```dockerfile
```

-	Layers:
	-	`sha256:ef3309bd98bbe3cff86b4c3fe9fe64d9e0317ad73e14e87a584968588d9cb6ac`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51b5719639e240ee9da354d652b0548f752a9fadbfe98a1d586ae8be2fde209`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d4574561869dbcba3ceaff23fc0788a14e6c6312ace734594b7dd0258a47b1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d9a56e76f976f87aea78762fb21a347964d8af628083946540a3bf7a753671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:19:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:32 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a4a9b6b9676c19d79002ed3e7d9e3aa82e0d76fe0d8864c957f1e9d55168ed`  
		Last Modified: Mon, 02 Feb 2026 19:19:40 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb176de5ae6175882b58168e955d155949a2387ad424ef44dedc3cb97308c4`  
		Last Modified: Mon, 02 Feb 2026 19:19:41 GMT  
		Size: 42.9 MB (42851387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6e178dc0f68f29f2e284e3dc88b79a46bab88ed786dab5da0eb7e0eac58a2`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cfbeea50418380014cb82f0ab50e081489a69c9f13c64917cc4d60b18d70b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67671f8be07fe685feed12b91f122c7c05cea55d9cb74f8520da1cb71ff04540`

```dockerfile
```

-	Layers:
	-	`sha256:27bf125363d18322cdb1a86703b4db6e0b22adbd5dab554dacac5946eaa3e983`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19b85f525731d2e3dae5ea04044c2d4a7dadd9654ae5cccc8376e8d52238efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feada2dc396baa2615171b3d750ba5f367ad9cf371f6ab6aa0a80053d989305`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:24:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:24:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760a4e7f97791609aa051682708c95b35de5fe9cc6f296231465d8d08cd812d`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 463.0 KB (463011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e88306c87b340425aa60ae18cff826197a37d08e6f28bcb8041b13cd4512`  
		Last Modified: Mon, 02 Feb 2026 19:24:37 GMT  
		Size: 42.1 MB (42109642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a64a2e8c4ae63bd423fc78f6da3de120d6cb7afb00e2fb811d90a06d4ad222`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a2f4ea11ef5a33c4d78d6eb96f7b98cdfc73c94355397341e1304a69e70f0d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17237fa8264f3b3ccbd7d1a803277a7389abb3377f433424894cad517eaf49ec`

```dockerfile
```

-	Layers:
	-	`sha256:92669e16a7fca33855e7b84fc0d85d499bae208e891d503dee468959b8b64be3`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540e481eee38c62376d8b04e565c69ea3e3acad3df55ddd48bbda0e127ca33c`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a4c0d555390f89f254be8955dcb866664401c9b02f02277821c3abf135015c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dfa5fd5676302535f3ee212252e73de7678216963cb905c4405a7d52443ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:18:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:00 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa218b5bedd12623a723833cd6946e5b5d62f5ecc64582746b3e1d80740135f`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 463.5 KB (463527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efd8826a5ff2fa3dc5f24dcc15c3db4cc519fd089f8c57bd7ae973e2edeba5`  
		Last Modified: Mon, 02 Feb 2026 19:19:54 GMT  
		Size: 41.1 MB (41058027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216f00a2112efdba5a3f6a030ce039e30f5e1c0191e8fc23f5e96a7e216ceb8`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:525a1bac2c221c0c843fb1d225bd15d1741a3e49896795136b4e283acf355c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cea6d71b657acbabfd505c8a223eab8b8e20f6190dc48cb9f23da89ace1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ce1efd0e4598b024a13ee8350c8b23381bd5e1f4a39576f421927ecfc9d92`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45ccf22c5bb5800544b273cd9dec64a78d473a288af8961d138407b4ff36a0`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:74ebe09868f81a2e9e0444d0a1de76aba73a45df6d8513285890f27023bb4fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a72913bdaaed333ef8ad012d63dc268f23081f78ef2c8c3ac8c1d3df3205d49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 19:06:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 19:06:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 19:06:31 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 19:06:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec037c2d893d7d29b7afede297802111719ead4b63664808242a3630fb16b91a`  
		Last Modified: Thu, 29 Jan 2026 19:11:27 GMT  
		Size: 45.3 MB (45325193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63acc32e46aa68086758b34a77f1e96b4d4d6e7808474c578ab6d07791bda83`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:574c6c8cc03fe79bf98cf9b54cd3ad40b5ce4d0ae959a228982998fd2dccb746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c66325e70ceb1c7e41957f16488f268f9ab12fcc781cda3ae1dd6304c74193a`

```dockerfile
```

-	Layers:
	-	`sha256:59dcd5eedbfd366ebe44be1ae13702861d40f3e00c4234cf6aa4616f2bde44dd`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfd7f8f4b46f541575dc51c3c2c718782b260d479bf557c37eafdf78b0aee03`  
		Last Modified: Thu, 29 Jan 2026 19:11:21 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:3a5b28df2712e797c55b80b393d4f3081be5499046bd322368b2c88eacbb82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b43eb5dec4846e5afbd335d9d236b549f598da9c1bd21087d157721443d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:08 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c59e88b8945e71acb4f8f932a7c082a2d71ee4e61e549a4014e08a3e0cb653`  
		Last Modified: Mon, 02 Feb 2026 19:19:57 GMT  
		Size: 45.3 MB (45289326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc755ae19df08a4aba8c642cb3a4e7da4289d2fe21c4ad2450c30f2ed53699d1`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f473f7ef16753708c841171ee8fcb75da0ed1b1c94c9b742c0ef4d5d9a358436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72053089031553af326e08d00875b5f2e05442f5c4ec8d343b3bc0772c7dd578`

```dockerfile
```

-	Layers:
	-	`sha256:43e3b17de8448cc504dc90998d5b30a1c3b893dc1fbbd1a1eabeb47342beedf7`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94706cb0698d6979497f3ade2388839d15910ec569a123c79f9949b59e15f95e`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d92a7468aee7f1df38369e9d817d13956c51a070458e3d8473ca20ee1b162917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:fa8dcc7dc8a27e8fac41bb0c3fda6200e33143bc5d05ad7687be7867230f87f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56f2ce9a331443214d5aa465eee78d3cbed6cb18fe51a8af9e5eda228f5059`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 02 Feb 2026 20:44:57 GMT
RUN cmd /S /C #(nop) COPY file:0b0150726a403f05ecd4788bbb4d84dbd236c80829e39a8e79edf4cc9e33137f in \ 
# Mon, 02 Feb 2026 20:44:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e487e7b658ecea2210e57410d93f8908fce2fa3e646f4e7da7012cfd8d242`  
		Last Modified: Mon, 02 Feb 2026 20:45:19 GMT  
		Size: 47.6 MB (47632503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a0aade23718702fc88e49f20a7b71d2277787261a242bf328d92a8eb7519a3`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd04af343a3432e3644907bdbbbf5ed02691378a5069713ac5065afac6433c`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13ca5eabe4abc4fd35a9b6c4485e3c397db223c65b1e3d910adfa5c43f7fb9`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.36`

```console
$ docker pull traefik@sha256:ea36eb2360592c76d8eb925accbfae8ad6b4586ecbb90b3d81c438d70ff63ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11.36` - linux; amd64

```console
$ docker pull traefik@sha256:32a30df3a661d213b3283d194aa3893cae9caf73fce2232e9874272e5d29efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340548c740e253c703c6b801d23a1f6a49a8a9929e520185a40695cd5f9e1de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:20:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:20:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:20:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f2786675ef53faf7d7614172f9443975122a1b1ae64cd2569afaf96c41c7f2`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 461.0 KB (460951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc916c0d969ec35d695c846b073b1b1b91bf77b063a67ec11c18ad0e9a80c3`  
		Last Modified: Mon, 02 Feb 2026 19:20:33 GMT  
		Size: 46.8 MB (46824091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2013761267b39711282c021b9c5777e0ed3dcd4935afd5eb907b99f812ddf`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:c0773956eacc3d9010e58a06a7ad2fd854ba3f499bd65987c6715f017a14b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b11a49a8583fa61436b5f9788bb7b9000636544d1bfd81a9bc7af002c21044`

```dockerfile
```

-	Layers:
	-	`sha256:ef3309bd98bbe3cff86b4c3fe9fe64d9e0317ad73e14e87a584968588d9cb6ac`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51b5719639e240ee9da354d652b0548f752a9fadbfe98a1d586ae8be2fde209`  
		Last Modified: Mon, 02 Feb 2026 19:20:32 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.36` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d4574561869dbcba3ceaff23fc0788a14e6c6312ace734594b7dd0258a47b1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d9a56e76f976f87aea78762fb21a347964d8af628083946540a3bf7a753671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:19:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:32 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a4a9b6b9676c19d79002ed3e7d9e3aa82e0d76fe0d8864c957f1e9d55168ed`  
		Last Modified: Mon, 02 Feb 2026 19:19:40 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb176de5ae6175882b58168e955d155949a2387ad424ef44dedc3cb97308c4`  
		Last Modified: Mon, 02 Feb 2026 19:19:41 GMT  
		Size: 42.9 MB (42851387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6e178dc0f68f29f2e284e3dc88b79a46bab88ed786dab5da0eb7e0eac58a2`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:cfbeea50418380014cb82f0ab50e081489a69c9f13c64917cc4d60b18d70b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67671f8be07fe685feed12b91f122c7c05cea55d9cb74f8520da1cb71ff04540`

```dockerfile
```

-	Layers:
	-	`sha256:27bf125363d18322cdb1a86703b4db6e0b22adbd5dab554dacac5946eaa3e983`  
		Last Modified: Mon, 02 Feb 2026 19:19:39 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.36` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19b85f525731d2e3dae5ea04044c2d4a7dadd9654ae5cccc8376e8d52238efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feada2dc396baa2615171b3d750ba5f367ad9cf371f6ab6aa0a80053d989305`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:24:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:24:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760a4e7f97791609aa051682708c95b35de5fe9cc6f296231465d8d08cd812d`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 463.0 KB (463011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e88306c87b340425aa60ae18cff826197a37d08e6f28bcb8041b13cd4512`  
		Last Modified: Mon, 02 Feb 2026 19:24:37 GMT  
		Size: 42.1 MB (42109642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a64a2e8c4ae63bd423fc78f6da3de120d6cb7afb00e2fb811d90a06d4ad222`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:a2f4ea11ef5a33c4d78d6eb96f7b98cdfc73c94355397341e1304a69e70f0d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17237fa8264f3b3ccbd7d1a803277a7389abb3377f433424894cad517eaf49ec`

```dockerfile
```

-	Layers:
	-	`sha256:92669e16a7fca33855e7b84fc0d85d499bae208e891d503dee468959b8b64be3`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540e481eee38c62376d8b04e565c69ea3e3acad3df55ddd48bbda0e127ca33c`  
		Last Modified: Mon, 02 Feb 2026 19:24:35 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.36` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a4c0d555390f89f254be8955dcb866664401c9b02f02277821c3abf135015c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45351566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dfa5fd5676302535f3ee212252e73de7678216963cb905c4405a7d52443ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:18:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:00 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa218b5bedd12623a723833cd6946e5b5d62f5ecc64582746b3e1d80740135f`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 463.5 KB (463527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efd8826a5ff2fa3dc5f24dcc15c3db4cc519fd089f8c57bd7ae973e2edeba5`  
		Last Modified: Mon, 02 Feb 2026 19:19:54 GMT  
		Size: 41.1 MB (41058027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216f00a2112efdba5a3f6a030ce039e30f5e1c0191e8fc23f5e96a7e216ceb8`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:525a1bac2c221c0c843fb1d225bd15d1741a3e49896795136b4e283acf355c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cea6d71b657acbabfd505c8a223eab8b8e20f6190dc48cb9f23da89ace1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ce1efd0e4598b024a13ee8350c8b23381bd5e1f4a39576f421927ecfc9d92`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45ccf22c5bb5800544b273cd9dec64a78d473a288af8961d138407b4ff36a0`  
		Last Modified: Mon, 02 Feb 2026 19:19:52 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.36` - linux; s390x

```console
$ docker pull traefik@sha256:3a5b28df2712e797c55b80b393d4f3081be5499046bd322368b2c88eacbb82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b43eb5dec4846e5afbd335d9d236b549f598da9c1bd21087d157721443d9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
COPY entrypoint.sh / # buildkit
# Mon, 02 Feb 2026 19:19:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 02 Feb 2026 19:19:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Feb 2026 19:19:08 GMT
CMD ["traefik"]
# Mon, 02 Feb 2026 19:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c59e88b8945e71acb4f8f932a7c082a2d71ee4e61e549a4014e08a3e0cb653`  
		Last Modified: Mon, 02 Feb 2026 19:19:57 GMT  
		Size: 45.3 MB (45289326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc755ae19df08a4aba8c642cb3a4e7da4289d2fe21c4ad2450c30f2ed53699d1`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.36` - unknown; unknown

```console
$ docker pull traefik@sha256:f473f7ef16753708c841171ee8fcb75da0ed1b1c94c9b742c0ef4d5d9a358436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72053089031553af326e08d00875b5f2e05442f5c4ec8d343b3bc0772c7dd578`

```dockerfile
```

-	Layers:
	-	`sha256:43e3b17de8448cc504dc90998d5b30a1c3b893dc1fbbd1a1eabeb47342beedf7`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94706cb0698d6979497f3ade2388839d15910ec569a123c79f9949b59e15f95e`  
		Last Modified: Mon, 02 Feb 2026 19:19:56 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.36-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d92a7468aee7f1df38369e9d817d13956c51a070458e3d8473ca20ee1b162917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11.36-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:fa8dcc7dc8a27e8fac41bb0c3fda6200e33143bc5d05ad7687be7867230f87f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56f2ce9a331443214d5aa465eee78d3cbed6cb18fe51a8af9e5eda228f5059`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 02 Feb 2026 20:44:57 GMT
RUN cmd /S /C #(nop) COPY file:0b0150726a403f05ecd4788bbb4d84dbd236c80829e39a8e79edf4cc9e33137f in \ 
# Mon, 02 Feb 2026 20:44:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 20:45:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e487e7b658ecea2210e57410d93f8908fce2fa3e646f4e7da7012cfd8d242`  
		Last Modified: Mon, 02 Feb 2026 20:45:19 GMT  
		Size: 47.6 MB (47632503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a0aade23718702fc88e49f20a7b71d2277787261a242bf328d92a8eb7519a3`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd04af343a3432e3644907bdbbbf5ed02691378a5069713ac5065afac6433c`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13ca5eabe4abc4fd35a9b6c4485e3c397db223c65b1e3d910adfa5c43f7fb9`  
		Last Modified: Mon, 02 Feb 2026 20:45:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.36-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11.36-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.7`

```console
$ docker pull traefik@sha256:a9890c898f379c1905ee5b28342f6b408dc863f08db2dab20e46c267d1ff463a
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

### `traefik:v3.6.7` - linux; amd64

```console
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; riscv64

```console
$ docker pull traefik@sha256:eb407c9a0df154290ec008e1c69ddd16329f9244d13360b64e94a3953244d79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50334895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a515c8f861992c7fedeb3f2a5798cbfa0a98289deaad94459b4e063273bfba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:59:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
COPY entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:59:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 29 Jan 2026 18:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:59:55 GMT
CMD ["traefik"]
# Thu, 29 Jan 2026 18:59:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1b25cf06842e0b0dcc119934ca6989dad15a41bc8c8574921d34cc831ce01`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 461.2 KB (461183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab70e725b25e5aa68e7fd5bb0ad33b4e274ddf64c37e722dd1b72e52cadfa2`  
		Last Modified: Thu, 29 Jan 2026 19:05:44 GMT  
		Size: 46.3 MB (46288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc7eb596b3f7953901bd11bda95f5849ac6bda3ea0ecc8000274ee844220a4`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:69e36d5064d83e525d98798c12c2570fb97f4733b497e98538322c64cfb53c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dbf8eca6efd80bff4ec0935565b3f7b298c0e7682fe6f4e69c7e4dc4e8ab8a`

```dockerfile
```

-	Layers:
	-	`sha256:de7144bf2bcc4ced3991cc0194fa0a1044435c45cce7a5b00bf3bde45d54a426`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2b4cf3970059cad1f73e18b75b4d1bf3b17420442ae135c6cc9c39bc96270`  
		Last Modified: Thu, 29 Jan 2026 19:05:37 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.7-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6.7-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.7-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
