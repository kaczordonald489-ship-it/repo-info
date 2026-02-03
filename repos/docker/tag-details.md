<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.2`](#docker292)
-	[`docker:29.2-cli`](#docker292-cli)
-	[`docker:29.2-dind`](#docker292-dind)
-	[`docker:29.2-dind-rootless`](#docker292-dind-rootless)
-	[`docker:29.2-windowsservercore`](#docker292-windowsservercore)
-	[`docker:29.2-windowsservercore-ltsc2022`](#docker292-windowsservercore-ltsc2022)
-	[`docker:29.2-windowsservercore-ltsc2025`](#docker292-windowsservercore-ltsc2025)
-	[`docker:29.2.0`](#docker2920)
-	[`docker:29.2.0-alpine3.23`](#docker2920-alpine323)
-	[`docker:29.2.0-cli`](#docker2920-cli)
-	[`docker:29.2.0-cli-alpine3.23`](#docker2920-cli-alpine323)
-	[`docker:29.2.0-dind`](#docker2920-dind)
-	[`docker:29.2.0-dind-alpine3.23`](#docker2920-dind-alpine323)
-	[`docker:29.2.0-dind-rootless`](#docker2920-dind-rootless)
-	[`docker:29.2.0-windowsservercore`](#docker2920-windowsservercore)
-	[`docker:29.2.0-windowsservercore-ltsc2022`](#docker2920-windowsservercore-ltsc2022)
-	[`docker:29.2.0-windowsservercore-ltsc2025`](#docker2920-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:ae2609c051339b48c157d97edc4f1171026251607b29a2b0f25f990898586334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:f7da93bb3a6c57789eec1180058c44127f70548977cc18e602d52082506de826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7456360d729184ce664287a28910e7d0954dc4cb47af5f368836ebca6c968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3aca729d148603e7359809f3dd91bca4e2caf81b10795045854a954ee35c5474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece80dd2cdf869afe1e8f247c3a89871d95f4571f4db4501ed2f356521aad2da`

```dockerfile
```

-	Layers:
	-	`sha256:afbbd960a4dc2b95eb5ce34efe5f925861c5d4f7c7053610c318b26cb8adbd82`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d1daa846e67962482579359f8f9eb214ddf7d429eb0344df8a96dc091621ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66233037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4832bcda60ebc58c73495ff6fca84735d315de14546234deed4b47cfd7418197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:deeab2b34164fec351034fe69f2c19b7a892aeb681d0cc81f52a6bf6587482c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b56e28e9e8737e0b519a92914f19168ea72c229b5f2b5356344b8a7e500278`

```dockerfile
```

-	Layers:
	-	`sha256:cee7fb4beb798e4490ff9df87ee037c582391eb7be41938033f8b3b00c468725`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3d5e24bc578c3c405ee75a3b3e84f22401d8011a7cf734a1c57b08157dc3df74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65191411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3129e4614b8a4c307d4bcc11891481cf8ad58aa25066b0e8a95edf427673ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0f34ce8cba350174784966cc122a11880969e2ccbeaf707481cfb5d31635e058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e8e62373cdb656671bac3362081150948a8bd52d6377dd5fc560d9796a14a`

```dockerfile
```

-	Layers:
	-	`sha256:db482dc560884045eef339dcac5ae861c5919cbe94f76c9d69fc83e8c1146362`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:647687c6c262cf27eddc075fcb7f38045f5d1cb01dc8338d580f7911f87346f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65496936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5082de71f8c0906e532d06374cb3bc4615c46ddeffae2c47992b4599911bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8431c41f4bed45f8a05f23efa126b99996e542633171e6c9190c5caf41e60f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed9b9f1dcb4e6a17e5c72a1b717d5af38e9d75ce22f692ecd09ac9a2e74922`

```dockerfile
```

-	Layers:
	-	`sha256:e873aca13e5836fbdfb1649455476882c8a1600ea227ea88b19db24b0ec52207`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 38.3 KB (38257 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:e2256cccf0a81babdf6b0715edc84299976eea749dc373de1d4c4b98f38be576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e740431e7ec02952bcba763683de89ae7c38ed168d0cfc4b875ffc2cc94eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164596244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893377b7f16e5efd1e758a1c978a11516ff914ffd6896497463fae305e6732d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
# Wed, 28 Jan 2026 04:49:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 04:49:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f26c740596bada2273b63c30df575d6fe75108c34ae59cf6cce23eb6fde38`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 3.4 MB (3419936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b0d647df5d90a456bfb18e7fe3512570e5501e17a96c28d0673f36c7de2ab`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266ba1a98fbf4bf56e7477a64291015ffc22febbdef7b5c52756c0bccea91bc`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7bef04bfc2f8ecbd179e44e594aea6870289cac0095619a71f9ae48c070b2`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 17.4 MB (17375872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de36060bb1e57bb0070a546b5af68c0c667dfc7c88ad9c5e0b4b58cd903fdd5f`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:304a9bab4d48983bd4f25caa7723d4ff17feec1769ef4b9d815a85818b33f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a9fa96564b6f3cbe5f035361ffe48a58c26e0d28c673a4517c0afb4d19bd17`

```dockerfile
```

-	Layers:
	-	`sha256:f20e17ed780eccbdcae7df7f23b087c7750a8fca8f1ef231ace886ff1ec41145`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:10185cf7e9ecf2d725eabaed0f994c40d28c4ca77f04234d07c2bb0efcd4c588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a4777f73ae85118338e6c79bca8a28937df9dc8a5f912a5066951db75e2a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
# Wed, 28 Jan 2026 05:26:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 05:26:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2ca6f15a1175824a8ac624e8e96c03e577d7045335b3b8da66fa925ac730e`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 3.4 MB (3394379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae4fb46b816b0c2dabc0ce7fb6de979a1297033cfc1d63f2330898b865858f`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee34b605800e64fa4c7d8ae1e8b3a28b7a99fb9273d49a13ddc555bda1daa5`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850780d6ebb6a4c34ff107ae6908c6afecf589851309b1c501eea08aadde6b2`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 17.7 MB (17710501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19d5a6a20d8289c916e7596e72a2d20595e4e8c11ae662f0ce57a9c05814f1`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c4559aefd8beb1182fc0607820b2e0c38fe82f9a6af4f47c78173a966859ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50641e7994aded7de3b8033e71f36c7fa1b0b852dc54cb3365dbfd3de2e376b6`

```dockerfile
```

-	Layers:
	-	`sha256:2e936dbc59719f822df84bc05b46cb1f559506d9e7912ed2c9c670c5b0a6d64c`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-cli`

```console
$ docker pull docker@sha256:ae2609c051339b48c157d97edc4f1171026251607b29a2b0f25f990898586334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:f7da93bb3a6c57789eec1180058c44127f70548977cc18e602d52082506de826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7456360d729184ce664287a28910e7d0954dc4cb47af5f368836ebca6c968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3aca729d148603e7359809f3dd91bca4e2caf81b10795045854a954ee35c5474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece80dd2cdf869afe1e8f247c3a89871d95f4571f4db4501ed2f356521aad2da`

```dockerfile
```

-	Layers:
	-	`sha256:afbbd960a4dc2b95eb5ce34efe5f925861c5d4f7c7053610c318b26cb8adbd82`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d1daa846e67962482579359f8f9eb214ddf7d429eb0344df8a96dc091621ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66233037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4832bcda60ebc58c73495ff6fca84735d315de14546234deed4b47cfd7418197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:deeab2b34164fec351034fe69f2c19b7a892aeb681d0cc81f52a6bf6587482c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b56e28e9e8737e0b519a92914f19168ea72c229b5f2b5356344b8a7e500278`

```dockerfile
```

-	Layers:
	-	`sha256:cee7fb4beb798e4490ff9df87ee037c582391eb7be41938033f8b3b00c468725`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3d5e24bc578c3c405ee75a3b3e84f22401d8011a7cf734a1c57b08157dc3df74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65191411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3129e4614b8a4c307d4bcc11891481cf8ad58aa25066b0e8a95edf427673ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0f34ce8cba350174784966cc122a11880969e2ccbeaf707481cfb5d31635e058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e8e62373cdb656671bac3362081150948a8bd52d6377dd5fc560d9796a14a`

```dockerfile
```

-	Layers:
	-	`sha256:db482dc560884045eef339dcac5ae861c5919cbe94f76c9d69fc83e8c1146362`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:647687c6c262cf27eddc075fcb7f38045f5d1cb01dc8338d580f7911f87346f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65496936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5082de71f8c0906e532d06374cb3bc4615c46ddeffae2c47992b4599911bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8431c41f4bed45f8a05f23efa126b99996e542633171e6c9190c5caf41e60f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed9b9f1dcb4e6a17e5c72a1b717d5af38e9d75ce22f692ecd09ac9a2e74922`

```dockerfile
```

-	Layers:
	-	`sha256:e873aca13e5836fbdfb1649455476882c8a1600ea227ea88b19db24b0ec52207`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 38.3 KB (38257 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind-rootless`

```console
$ docker pull docker@sha256:e2256cccf0a81babdf6b0715edc84299976eea749dc373de1d4c4b98f38be576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e740431e7ec02952bcba763683de89ae7c38ed168d0cfc4b875ffc2cc94eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164596244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893377b7f16e5efd1e758a1c978a11516ff914ffd6896497463fae305e6732d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
# Wed, 28 Jan 2026 04:49:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 04:49:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f26c740596bada2273b63c30df575d6fe75108c34ae59cf6cce23eb6fde38`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 3.4 MB (3419936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b0d647df5d90a456bfb18e7fe3512570e5501e17a96c28d0673f36c7de2ab`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266ba1a98fbf4bf56e7477a64291015ffc22febbdef7b5c52756c0bccea91bc`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7bef04bfc2f8ecbd179e44e594aea6870289cac0095619a71f9ae48c070b2`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 17.4 MB (17375872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de36060bb1e57bb0070a546b5af68c0c667dfc7c88ad9c5e0b4b58cd903fdd5f`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:304a9bab4d48983bd4f25caa7723d4ff17feec1769ef4b9d815a85818b33f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a9fa96564b6f3cbe5f035361ffe48a58c26e0d28c673a4517c0afb4d19bd17`

```dockerfile
```

-	Layers:
	-	`sha256:f20e17ed780eccbdcae7df7f23b087c7750a8fca8f1ef231ace886ff1ec41145`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:10185cf7e9ecf2d725eabaed0f994c40d28c4ca77f04234d07c2bb0efcd4c588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a4777f73ae85118338e6c79bca8a28937df9dc8a5f912a5066951db75e2a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
# Wed, 28 Jan 2026 05:26:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 05:26:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2ca6f15a1175824a8ac624e8e96c03e577d7045335b3b8da66fa925ac730e`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 3.4 MB (3394379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae4fb46b816b0c2dabc0ce7fb6de979a1297033cfc1d63f2330898b865858f`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee34b605800e64fa4c7d8ae1e8b3a28b7a99fb9273d49a13ddc555bda1daa5`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850780d6ebb6a4c34ff107ae6908c6afecf589851309b1c501eea08aadde6b2`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 17.7 MB (17710501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19d5a6a20d8289c916e7596e72a2d20595e4e8c11ae662f0ce57a9c05814f1`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c4559aefd8beb1182fc0607820b2e0c38fe82f9a6af4f47c78173a966859ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50641e7994aded7de3b8033e71f36c7fa1b0b852dc54cb3365dbfd3de2e376b6`

```dockerfile
```

-	Layers:
	-	`sha256:2e936dbc59719f822df84bc05b46cb1f559506d9e7912ed2c9c670c5b0a6d64c`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-alpine3.23`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-cli`

```console
$ docker pull docker@sha256:ae2609c051339b48c157d97edc4f1171026251607b29a2b0f25f990898586334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:f7da93bb3a6c57789eec1180058c44127f70548977cc18e602d52082506de826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7456360d729184ce664287a28910e7d0954dc4cb47af5f368836ebca6c968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3aca729d148603e7359809f3dd91bca4e2caf81b10795045854a954ee35c5474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece80dd2cdf869afe1e8f247c3a89871d95f4571f4db4501ed2f356521aad2da`

```dockerfile
```

-	Layers:
	-	`sha256:afbbd960a4dc2b95eb5ce34efe5f925861c5d4f7c7053610c318b26cb8adbd82`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d1daa846e67962482579359f8f9eb214ddf7d429eb0344df8a96dc091621ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66233037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4832bcda60ebc58c73495ff6fca84735d315de14546234deed4b47cfd7418197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:deeab2b34164fec351034fe69f2c19b7a892aeb681d0cc81f52a6bf6587482c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b56e28e9e8737e0b519a92914f19168ea72c229b5f2b5356344b8a7e500278`

```dockerfile
```

-	Layers:
	-	`sha256:cee7fb4beb798e4490ff9df87ee037c582391eb7be41938033f8b3b00c468725`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3d5e24bc578c3c405ee75a3b3e84f22401d8011a7cf734a1c57b08157dc3df74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65191411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3129e4614b8a4c307d4bcc11891481cf8ad58aa25066b0e8a95edf427673ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0f34ce8cba350174784966cc122a11880969e2ccbeaf707481cfb5d31635e058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e8e62373cdb656671bac3362081150948a8bd52d6377dd5fc560d9796a14a`

```dockerfile
```

-	Layers:
	-	`sha256:db482dc560884045eef339dcac5ae861c5919cbe94f76c9d69fc83e8c1146362`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:647687c6c262cf27eddc075fcb7f38045f5d1cb01dc8338d580f7911f87346f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65496936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5082de71f8c0906e532d06374cb3bc4615c46ddeffae2c47992b4599911bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8431c41f4bed45f8a05f23efa126b99996e542633171e6c9190c5caf41e60f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed9b9f1dcb4e6a17e5c72a1b717d5af38e9d75ce22f692ecd09ac9a2e74922`

```dockerfile
```

-	Layers:
	-	`sha256:e873aca13e5836fbdfb1649455476882c8a1600ea227ea88b19db24b0ec52207`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 38.3 KB (38257 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-cli-alpine3.23`

```console
$ docker pull docker@sha256:ae2609c051339b48c157d97edc4f1171026251607b29a2b0f25f990898586334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:f7da93bb3a6c57789eec1180058c44127f70548977cc18e602d52082506de826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7456360d729184ce664287a28910e7d0954dc4cb47af5f368836ebca6c968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:3aca729d148603e7359809f3dd91bca4e2caf81b10795045854a954ee35c5474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece80dd2cdf869afe1e8f247c3a89871d95f4571f4db4501ed2f356521aad2da`

```dockerfile
```

-	Layers:
	-	`sha256:afbbd960a4dc2b95eb5ce34efe5f925861c5d4f7c7053610c318b26cb8adbd82`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:d1daa846e67962482579359f8f9eb214ddf7d429eb0344df8a96dc091621ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66233037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4832bcda60ebc58c73495ff6fca84735d315de14546234deed4b47cfd7418197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:deeab2b34164fec351034fe69f2c19b7a892aeb681d0cc81f52a6bf6587482c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b56e28e9e8737e0b519a92914f19168ea72c229b5f2b5356344b8a7e500278`

```dockerfile
```

-	Layers:
	-	`sha256:cee7fb4beb798e4490ff9df87ee037c582391eb7be41938033f8b3b00c468725`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:3d5e24bc578c3c405ee75a3b3e84f22401d8011a7cf734a1c57b08157dc3df74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65191411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3129e4614b8a4c307d4bcc11891481cf8ad58aa25066b0e8a95edf427673ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:0f34ce8cba350174784966cc122a11880969e2ccbeaf707481cfb5d31635e058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e8e62373cdb656671bac3362081150948a8bd52d6377dd5fc560d9796a14a`

```dockerfile
```

-	Layers:
	-	`sha256:db482dc560884045eef339dcac5ae861c5919cbe94f76c9d69fc83e8c1146362`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:647687c6c262cf27eddc075fcb7f38045f5d1cb01dc8338d580f7911f87346f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65496936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5082de71f8c0906e532d06374cb3bc4615c46ddeffae2c47992b4599911bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a8431c41f4bed45f8a05f23efa126b99996e542633171e6c9190c5caf41e60f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed9b9f1dcb4e6a17e5c72a1b717d5af38e9d75ce22f692ecd09ac9a2e74922`

```dockerfile
```

-	Layers:
	-	`sha256:e873aca13e5836fbdfb1649455476882c8a1600ea227ea88b19db24b0ec52207`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 38.3 KB (38257 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-dind`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-dind-alpine3.23`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0-dind-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-dind-rootless`

```console
$ docker pull docker@sha256:e2256cccf0a81babdf6b0715edc84299976eea749dc373de1d4c4b98f38be576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e740431e7ec02952bcba763683de89ae7c38ed168d0cfc4b875ffc2cc94eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164596244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893377b7f16e5efd1e758a1c978a11516ff914ffd6896497463fae305e6732d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
# Wed, 28 Jan 2026 04:49:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 04:49:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f26c740596bada2273b63c30df575d6fe75108c34ae59cf6cce23eb6fde38`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 3.4 MB (3419936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b0d647df5d90a456bfb18e7fe3512570e5501e17a96c28d0673f36c7de2ab`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266ba1a98fbf4bf56e7477a64291015ffc22febbdef7b5c52756c0bccea91bc`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7bef04bfc2f8ecbd179e44e594aea6870289cac0095619a71f9ae48c070b2`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 17.4 MB (17375872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de36060bb1e57bb0070a546b5af68c0c667dfc7c88ad9c5e0b4b58cd903fdd5f`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:304a9bab4d48983bd4f25caa7723d4ff17feec1769ef4b9d815a85818b33f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a9fa96564b6f3cbe5f035361ffe48a58c26e0d28c673a4517c0afb4d19bd17`

```dockerfile
```

-	Layers:
	-	`sha256:f20e17ed780eccbdcae7df7f23b087c7750a8fca8f1ef231ace886ff1ec41145`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:10185cf7e9ecf2d725eabaed0f994c40d28c4ca77f04234d07c2bb0efcd4c588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a4777f73ae85118338e6c79bca8a28937df9dc8a5f912a5066951db75e2a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
# Wed, 28 Jan 2026 05:26:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 05:26:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2ca6f15a1175824a8ac624e8e96c03e577d7045335b3b8da66fa925ac730e`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 3.4 MB (3394379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae4fb46b816b0c2dabc0ce7fb6de979a1297033cfc1d63f2330898b865858f`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee34b605800e64fa4c7d8ae1e8b3a28b7a99fb9273d49a13ddc555bda1daa5`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850780d6ebb6a4c34ff107ae6908c6afecf589851309b1c501eea08aadde6b2`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 17.7 MB (17710501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19d5a6a20d8289c916e7596e72a2d20595e4e8c11ae662f0ce57a9c05814f1`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c4559aefd8beb1182fc0607820b2e0c38fe82f9a6af4f47c78173a966859ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50641e7994aded7de3b8033e71f36c7fa1b0b852dc54cb3365dbfd3de2e376b6`

```dockerfile
```

-	Layers:
	-	`sha256:2e936dbc59719f822df84bc05b46cb1f559506d9e7912ed2c9c670c5b0a6d64c`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.0-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2.0-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2.0-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:ae2609c051339b48c157d97edc4f1171026251607b29a2b0f25f990898586334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:f7da93bb3a6c57789eec1180058c44127f70548977cc18e602d52082506de826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7456360d729184ce664287a28910e7d0954dc4cb47af5f368836ebca6c968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:3aca729d148603e7359809f3dd91bca4e2caf81b10795045854a954ee35c5474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece80dd2cdf869afe1e8f247c3a89871d95f4571f4db4501ed2f356521aad2da`

```dockerfile
```

-	Layers:
	-	`sha256:afbbd960a4dc2b95eb5ce34efe5f925861c5d4f7c7053610c318b26cb8adbd82`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d1daa846e67962482579359f8f9eb214ddf7d429eb0344df8a96dc091621ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66233037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4832bcda60ebc58c73495ff6fca84735d315de14546234deed4b47cfd7418197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:deeab2b34164fec351034fe69f2c19b7a892aeb681d0cc81f52a6bf6587482c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b56e28e9e8737e0b519a92914f19168ea72c229b5f2b5356344b8a7e500278`

```dockerfile
```

-	Layers:
	-	`sha256:cee7fb4beb798e4490ff9df87ee037c582391eb7be41938033f8b3b00c468725`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3d5e24bc578c3c405ee75a3b3e84f22401d8011a7cf734a1c57b08157dc3df74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65191411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3129e4614b8a4c307d4bcc11891481cf8ad58aa25066b0e8a95edf427673ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0f34ce8cba350174784966cc122a11880969e2ccbeaf707481cfb5d31635e058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e8e62373cdb656671bac3362081150948a8bd52d6377dd5fc560d9796a14a`

```dockerfile
```

-	Layers:
	-	`sha256:db482dc560884045eef339dcac5ae861c5919cbe94f76c9d69fc83e8c1146362`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:647687c6c262cf27eddc075fcb7f38045f5d1cb01dc8338d580f7911f87346f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65496936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5082de71f8c0906e532d06374cb3bc4615c46ddeffae2c47992b4599911bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8431c41f4bed45f8a05f23efa126b99996e542633171e6c9190c5caf41e60f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed9b9f1dcb4e6a17e5c72a1b717d5af38e9d75ce22f692ecd09ac9a2e74922`

```dockerfile
```

-	Layers:
	-	`sha256:e873aca13e5836fbdfb1649455476882c8a1600ea227ea88b19db24b0ec52207`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 38.3 KB (38257 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:e2256cccf0a81babdf6b0715edc84299976eea749dc373de1d4c4b98f38be576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e740431e7ec02952bcba763683de89ae7c38ed168d0cfc4b875ffc2cc94eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164596244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893377b7f16e5efd1e758a1c978a11516ff914ffd6896497463fae305e6732d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
# Wed, 28 Jan 2026 04:49:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 04:49:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f26c740596bada2273b63c30df575d6fe75108c34ae59cf6cce23eb6fde38`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 3.4 MB (3419936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b0d647df5d90a456bfb18e7fe3512570e5501e17a96c28d0673f36c7de2ab`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266ba1a98fbf4bf56e7477a64291015ffc22febbdef7b5c52756c0bccea91bc`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7bef04bfc2f8ecbd179e44e594aea6870289cac0095619a71f9ae48c070b2`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 17.4 MB (17375872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de36060bb1e57bb0070a546b5af68c0c667dfc7c88ad9c5e0b4b58cd903fdd5f`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:304a9bab4d48983bd4f25caa7723d4ff17feec1769ef4b9d815a85818b33f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a9fa96564b6f3cbe5f035361ffe48a58c26e0d28c673a4517c0afb4d19bd17`

```dockerfile
```

-	Layers:
	-	`sha256:f20e17ed780eccbdcae7df7f23b087c7750a8fca8f1ef231ace886ff1ec41145`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:10185cf7e9ecf2d725eabaed0f994c40d28c4ca77f04234d07c2bb0efcd4c588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a4777f73ae85118338e6c79bca8a28937df9dc8a5f912a5066951db75e2a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
# Wed, 28 Jan 2026 05:26:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 05:26:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2ca6f15a1175824a8ac624e8e96c03e577d7045335b3b8da66fa925ac730e`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 3.4 MB (3394379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae4fb46b816b0c2dabc0ce7fb6de979a1297033cfc1d63f2330898b865858f`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee34b605800e64fa4c7d8ae1e8b3a28b7a99fb9273d49a13ddc555bda1daa5`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850780d6ebb6a4c34ff107ae6908c6afecf589851309b1c501eea08aadde6b2`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 17.7 MB (17710501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19d5a6a20d8289c916e7596e72a2d20595e4e8c11ae662f0ce57a9c05814f1`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c4559aefd8beb1182fc0607820b2e0c38fe82f9a6af4f47c78173a966859ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50641e7994aded7de3b8033e71f36c7fa1b0b852dc54cb3365dbfd3de2e376b6`

```dockerfile
```

-	Layers:
	-	`sha256:2e936dbc59719f822df84bc05b46cb1f559506d9e7912ed2c9c670c5b0a6d64c`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
