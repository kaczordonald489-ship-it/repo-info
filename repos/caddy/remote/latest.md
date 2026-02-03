## `caddy:latest`

```console
$ docker pull caddy@sha256:f20f80e1fb627294fb84b8515b7593aff8018c840f1396dc942a50ed0c2db648
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:b0780a47e6f7502610d16fa177a8bfe8e3229fe3f1e5b8dd1b040f2f917af7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22502235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aed261b9d04b08cca89b6076e336af590dbedcd5178dfd6d490cf26da61debf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:54 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:49:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:49:56 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:49:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:49:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:49:56 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:49:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233224cdc908851482adf1d142dd77f697a4f320d7457a26f80b3bf886ac7fe`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.8 MB (2765883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241bbfa4875f6e97ad2966d2bd1439109ea867cbf0f8fa492e8009727c8fa24f`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099e4eae307f3fc3ce28f54f0db4e8b41dc7318ca249bb01d6582ffd10553ac`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 15.9 MB (15923954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9785eb8268d98a9552e6819607bf1f6eea78128ca7462857af529637b9eb78ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 KB (338111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4df38ee34b1810d3aa6fdf9b998b95c534c1a7c917cd79469c6197df576b11c`

```dockerfile
```

-	Layers:
	-	`sha256:33d6adb97eb48edcc7c7f797ff67ad2623a563a4d5bcb2cf9d70c96ef83b4e7a`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 319.8 KB (319817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada840fbfb4c1f7df3285d88f6cceb573c1d019c2ab5b155d2457b7c7f9138ba`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 18.3 KB (18294 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3419b51f2f4bec4bbe037d4b791e372ff2b097e3b52ed0525be98e700cc2db22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21262107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2432c4b853c3b89fc0bf1ebe0da7ca65af4ab689000e914d736e3e4e0ab409fd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:47:11 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:47:13 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:47:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:47:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:47:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:47:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8969decbc3ab02b36d50abd17e14a3ec76d9d0875f458282904dbc4d433620`  
		Last Modified: Wed, 28 Jan 2026 03:47:18 GMT  
		Size: 2.7 MB (2701019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d2210b20920ce47f06b5b9224c5ac24a919b97dfa2a7c33e358c796161ef6f`  
		Last Modified: Wed, 28 Jan 2026 03:47:18 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ce2074fc6d422debb8e9dc0252c4351f76bfc53d6046bb62f5f6fbf0c4fb54`  
		Last Modified: Wed, 28 Jan 2026 03:47:19 GMT  
		Size: 15.0 MB (15048515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:05353075c91eaba3720ad6ede7dee390b43cbd3d6a4a60ebfd3b2c58ec3f9e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7631f81fdf869e51a88d9588466aa7e9715aeafff7267b0edb6a44816f5c30e`

```dockerfile
```

-	Layers:
	-	`sha256:c271ce95b8e40d3e390f1d17f5a16676f1a3e7007c72350eec7fc6a64937fa67`  
		Last Modified: Wed, 28 Jan 2026 03:47:18 GMT  
		Size: 18.2 KB (18217 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d7a1b9d635ed7d40e18f9ee9a568c934561c7f9902eb0e9518e8e92c36b84522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20846091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771cfd473aae0e709970ec8b291a37c66196741dba8c8c59c582c6780e557282`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:47:16 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:47:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:47:19 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:47:19 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:47:19 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:47:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d66e158a340bf7d4b009a721892d22cc3cc5cc845422607af9493396d7c2c72`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 2.6 MB (2582948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a03a4daa4c354fc55dc9c81a61b67eea5edf8fa9a73ba3f0e44d90f2660767`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e328cf0b856f1ba40061d5cf56f24ec2aa0d25139cc1194105429e044f1fb15`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 15.0 MB (15031991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:b8b93790f88082ce3ccde72eb3384be67aec300dd12a54c033fd4b46765b4b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 KB (338317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36607589a513a3c6dc5b10983d83716ea59be30c7fa8e41263c8c3507da4ffa4`

```dockerfile
```

-	Layers:
	-	`sha256:ac333ae5fa9c8b09feb252e4dee352c2f18c56cddb7dde60679a574eb14b5c62`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 319.9 KB (319885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b25c2b9628d351706780289b7ecf7d51a5284bd7af2eb448f363e1db913fd5`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:41a99e75650213d76ff63fd49ab58a02a9ce4f1129a6985661659993c91a5bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21437628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209ef7854fc1f0fa74146feafca79a016a61f4f6b20f4457e5f0ad3b228d9c7e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:38 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:56:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:56:40 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:56:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:56:40 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:56:40 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:56:40 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4faa3274f6632949d447e44d107d209b567d1828ad37406becdeb78faf2a292`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 2.8 MB (2773038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5082e1f85493f22e64b9374824aa63a8038a94a642fa4e7cc905e7cdeb68146d`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb0c9b27be6cd7db5b535fc1ad267ab4bdcac9fdca2fb884e4934e2f2ac6197`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 14.5 MB (14517544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:52b102a611855f2fe509a00f862e994e6e9a4d0590e0e391c7bf3a1bac048439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 KB (338397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dd8d17c272b00c9b2e7251aaf4b9de16b50176dfa477aafb62d2b7cd36e14b`

```dockerfile
```

-	Layers:
	-	`sha256:4fc8976f2cb69754ae5dbe18a0d3a1d4ed5e705b410c8a24e70658ecd1579a7e`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 319.9 KB (319921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546f85385a3d95ce6ea0511f6ca5ac562c9160782c0c2a94faeef33ffc6e89e5`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:7945eecf0567a8d377392a010929755ac9edc7983a719595b0abcaad99a4f958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21118744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029c041718cba83f3f73c7a03b122bf79ca74256ef4cf6aef5eb8501ec80cf89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 05:49:42 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 05:49:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 05:49:46 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 05:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 05:49:46 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 05:49:46 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 05:49:47 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 05:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d27a1cebfcd5c7d19f815a118a939680dd7f17dbe0fc6708fdf8e18b4e08e7`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 2.9 MB (2881009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f8f91b00c9d5bdabdab56b6356d32076ea61820c67088dfcd4f4c82365b386`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 7.5 KB (7490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580f1b75e743904245a014c656f0ceb2811c2afdf316017a02d11c36cc218310`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 14.5 MB (14495916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:0bd47765d347cae743b21d5ed9be391f310153dde547e1f2bbaff1cf00ea134e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 KB (336290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debc9b84c0deb0ebe3efa50b31be33c0777f74907e84ff1039fe412913794c3e`

```dockerfile
```

-	Layers:
	-	`sha256:49e53b3c2722757ce8c4b2dd55a232215d5d433643ae22f1f0abb6b235d7d624`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 317.9 KB (317924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed2654dd3697cf27c7a6fd105274d11114c040a4b4defe2ea7bab4f331b3b97`  
		Last Modified: Wed, 28 Jan 2026 05:49:59 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:1fda1ea60041573a7343d9ac09c2a671487373eb2a0d4ac02cc97547b12b2a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21544363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62c731a67a2fa983f6002abe485198b41b427d959dc968ed8de8cea26f525d3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Sun, 01 Feb 2026 05:41:40 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Sun, 01 Feb 2026 05:41:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sun, 01 Feb 2026 05:41:48 GMT
ENV CADDY_VERSION=v2.10.2
# Sun, 01 Feb 2026 05:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sun, 01 Feb 2026 05:41:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sun, 01 Feb 2026 05:41:48 GMT
ENV XDG_DATA_HOME=/data
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[80/tcp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[443/tcp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[443/udp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[2019/tcp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
WORKDIR /srv
# Sun, 01 Feb 2026 05:41:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef112d08d3a9af3893edd8085873b635eee17016e49d660415dc2cfeebc479f`  
		Last Modified: Sun, 01 Feb 2026 05:42:36 GMT  
		Size: 2.9 MB (2889122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca694903ff86ed9e688cb7279ee66be7051ee75d68985f3e91357c272429930`  
		Last Modified: Sun, 01 Feb 2026 05:42:35 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcddfcab535731a9ccef4307b226a59163e16bfe92a64e874e915c3eec6e7d`  
		Last Modified: Sun, 01 Feb 2026 05:42:38 GMT  
		Size: 15.1 MB (15130288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9f9cbee6a0b56e542b332fbc0e236e739648db71f558354d8296faea82884caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 KB (336285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844bfad8fd9f088a8dc30158b09e2c9848ef781d54245826d1f6adad34ee9790`

```dockerfile
```

-	Layers:
	-	`sha256:16d5726973f883ab398894a3869d4a5248698374baa15d7982703c4d163ec0ac`  
		Last Modified: Sun, 01 Feb 2026 05:42:35 GMT  
		Size: 317.9 KB (317920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765de01d9208844588ac004d7160d42c5563721efc204013dbe00b2d04ad4773`  
		Last Modified: Sun, 01 Feb 2026 05:42:35 GMT  
		Size: 18.4 KB (18365 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:6f5897a40ba331b6168ead40cc1af5e38d20ff4f363a5ea3672f58da1a39e857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21926347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07127a3343ffee00e7caa9b9ea8e566a208a7195571afd0c3984d8519c94fd4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:57:07 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 06:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 06:57:09 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 06:57:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 06:57:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 06:57:09 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 06:57:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7491ee627d96375c3d815309c875024be98d4a23e338476433fbc9f131035055`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 2.9 MB (2911727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4823f0238a3307d087b783a0492fa37ed26d107fb428f910c8771cbef1344c`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de39d52dda6fcb149d5fe9c9951b9fc4c5c79f388084ec63dd96ee2882e58fa`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:db77930a68a31e89d2f36104e852747509c1f6b1082face89d2b33fbf3f614e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 KB (336159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090c6a9bd1993a4fbd1e66e29403c3e7237a50bec7bad331499fb801bc7da44`

```dockerfile
```

-	Layers:
	-	`sha256:434937b4ed21587a7eda92958eefa3639edbcf2f48ad5f213902681f388f2997`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 317.9 KB (317866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9e0fdbcd0818a0e579184915c7ad2a64145583ea09f562a0fdf920d923d86f`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 18.3 KB (18293 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:de3d1803d449ab02b73296f3ed11e210b30b0e3f7b83665bd85cae0ec1049175
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1513252253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24887a74e96798d4529e46beae49f382b1a10d043a14d7bca49b4cecbdca5dbd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 21:47:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 21:47:44 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 16 Jan 2026 21:47:45 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:48:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 16 Jan 2026 21:48:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 16 Jan 2026 21:48:11 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 16 Jan 2026 21:48:11 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:48:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:48:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:48:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:48:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:48:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:48:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:48:16 GMT
EXPOSE 80
# Fri, 16 Jan 2026 21:48:17 GMT
EXPOSE 443
# Fri, 16 Jan 2026 21:48:18 GMT
EXPOSE 443/udp
# Fri, 16 Jan 2026 21:48:19 GMT
EXPOSE 2019
# Fri, 16 Jan 2026 21:48:26 GMT
RUN caddy version
# Fri, 16 Jan 2026 21:48:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b7436bdde4954ab997653ca362b6410146a18fcf3b8b83a54c551cf59c9c73`  
		Last Modified: Fri, 16 Jan 2026 21:48:36 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8984e104b3c0ff05fa60406f16ff2c4a2f58af5476a4da8460d993e5b15c54`  
		Last Modified: Fri, 16 Jan 2026 21:48:36 GMT  
		Size: 400.1 KB (400124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d50d69015e54959d508b06414479a76601f3f1c0c143302fa9815426f0ecdb`  
		Last Modified: Fri, 16 Jan 2026 21:48:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dd758177c1c66b62710c9ed34334f9a3b5978222bc6019718dfae6fd235898`  
		Last Modified: Fri, 16 Jan 2026 21:48:38 GMT  
		Size: 16.7 MB (16685267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6469db906ffeec163dc378daa88374a7395d787fbd64478d4a423691f7aa1c6`  
		Last Modified: Fri, 16 Jan 2026 21:48:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460c8b42281a2a84615f002cbb6533907bb7414d370ba83f99b09259c4b8577`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6125a52e3a7563428016564d117f80bd877e38a7a37181bab82f031fc024b8`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f6273de3485d3093bea4161194792b0a4895d56b17d19ea0ae955de131723`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb815f2b06c4f07495bb86c150cb225f1e14a30832c182218467729a2c22cd`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3bb0e23239e46f5ac1baf3505b72062c5c1b0a2b56accf494255279b81dc6c`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a0214cac497353d4d26a9e5729390a85a2cb4422324ad1a8dc9b7cbc10c883`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a97fe8c2c247a6fcaf584e485cc9b3d5bc584d4f0b7e97ca098fd712ffcc10e`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe22cb691633447fd4bb8f450aa6f4382ed47bc70c2f393e6eec96f267f6872`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3985fbe8b539cb8a152f3c35d7e7df4d60e2640770f2aa39f00fe07553a32e4`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e323161037befd8a9185eb6af7db6e238ccb4451b0f64284a255f3062f58ac`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852fd37e891f32ad639c4d4d7f6645b31ca2efe1e9bc6b7b588d6046bce65ab`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1abadcb16f8b7383029dbb8f7528efb9cddedd7ff75d0847ef53f11e744b75c`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e8ff0c84b5e9acf20fae62134d7bb0807d09f14fe921287c0ca135f987422`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa1ae318ebbfdc86e2311719b9629cade532ac567939ea85a8dd9fd1f236062`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 384.3 KB (384316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3e746bfff6a737ce01c0ec0226a66bf3b12acfd3f6c44c2fd4fc4809d15811`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.4648; amd64

```console
$ docker pull caddy@sha256:c10a12076add43fa2fcacfce590ac2f6a9e0d01cd2e1354b67e470bf0d06bd56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1853115354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f606fbff6b8d9ec8bbb5c43b8421f44d197c4f55842e54a82c05797112718a32`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Fri, 16 Jan 2026 21:47:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 21:47:39 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 16 Jan 2026 21:47:40 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:47:50 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 16 Jan 2026 21:47:50 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 16 Jan 2026 21:47:51 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 16 Jan 2026 21:47:52 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:47:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:47:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:47:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:47:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:47:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:47:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:47:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:48:00 GMT
EXPOSE 80
# Fri, 16 Jan 2026 21:48:00 GMT
EXPOSE 443
# Fri, 16 Jan 2026 21:48:01 GMT
EXPOSE 443/udp
# Fri, 16 Jan 2026 21:48:02 GMT
EXPOSE 2019
# Fri, 16 Jan 2026 21:48:11 GMT
RUN caddy version
# Fri, 16 Jan 2026 21:48:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
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
	-	`sha256:da84340b07e1cad15dbe51c11c05f559aa95ab7eed9c6e68dc4a812c0906345b`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4160a6438b1a19d88835ec1728c72ae59f039f5784b9526691a7eeb82534b`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 501.7 KB (501660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79009ba30b634a5be800711a4826a3472717eebab51a739db447021acd08cf23`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9b614b74a27be3bfbabfae99d05eee3a8c9519f9f22b63874fd166b1478dd5`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 16.6 MB (16574503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7410e33005a69fb0873209de68263e1b4f2915be399c4f43aa318a5fcb9fd1`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929bb4e999d90782a313f7c9b9b7c0435cb0745857211642bb657132e716240`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538a350f92fb6ac1f4078601f7b59d9fd2f687f613930258988a571d227ddf45`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2770b5e6afd5fc8d518455cb07fe2fa7bbfc026746e7d85fa24b9c3e0eaa24b8`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4940ace21147a2455987b5d6fb5173346a78c22c1f7b6a67aa49a65e3d6b217f`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa00dab456cb8086de15acacb6e660122a0aaf402479cdb95e473c6721052456`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc014ece1282be27edce301ee3c6569096f34dbea5174b32918638fd985d9d2`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9925c02e110fb56805cb659030ffd87a3a4035f403366d9489efdd0fff509fe6`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc38634bbbc8d62ac19edafe1c5c534965984ef837f6921a41227105f80c98c`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa2f1c08e7e6bffba7e2aafe2cae668cdbae2d991f19beda42da8df5df3b57a`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a925076807ae691e68aab5bdcd04ad643544b23148d12a721bf71f657fc9c0`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7733bea24770f80b76f2796916cd7abe848203317f7a263a87e0d9738944fec1`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ac31721ac6a9a67ce9b5f1586d31f549412d51993ac1cb6432bd891cd5d263`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e09078b5a083a4a9e63b2fcc5bac2ca609b27d3aad7d7680f8f3855a00e74ce`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc66546b510325c0a603db853cfaae858d0aea3e3f9b244947cd5d1b91934c6a`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 357.8 KB (357768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12efdcf8eadcbf183e0c9807135be6f68bb4557242cdf88beea64f37bf7cc32`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
