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
