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
