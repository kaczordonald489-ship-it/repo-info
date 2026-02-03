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
