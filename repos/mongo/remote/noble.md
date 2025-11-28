## `mongo:noble`

```console
$ docker pull mongo@sha256:0094e1002b7bf122754e8822f103802429b59db70bffce6e1714efa573637c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:c6b62ae11dacc284b4ac99c815b6acf36fbe2691f7e822d4964673767b4b53a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.6 MB (323614886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f862b74ef86bad4656ee847e008c3c047e8e5c702a2c638e726db57df9ccf7ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 19 Nov 2025 23:52:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 19 Nov 2025 23:52:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 23:52:27 GMT
ENV GOSU_VERSION=1.19
# Wed, 19 Nov 2025 23:52:27 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 19 Nov 2025 23:52:27 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 19 Nov 2025 23:52:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 19 Nov 2025 23:52:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 19 Nov 2025 23:52:27 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 19 Nov 2025 23:52:27 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 19 Nov 2025 23:52:27 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 19 Nov 2025 23:52:27 GMT
ENV MONGO_MAJOR=8.2
# Wed, 19 Nov 2025 23:52:27 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 19 Nov 2025 23:52:27 GMT
ENV MONGO_VERSION=8.2.2
# Wed, 19 Nov 2025 23:52:45 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 19 Nov 2025 23:52:45 GMT
VOLUME [/data/db /data/configdb]
# Wed, 19 Nov 2025 23:52:45 GMT
ENV HOME=/data/db
# Wed, 19 Nov 2025 23:52:45 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 19 Nov 2025 23:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 23:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 23:52:45 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 19 Nov 2025 23:52:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcec2d403c4e91c8b79417b4d2bc8c2d9975318766e8a75aa9f4528aee87633a`  
		Last Modified: Wed, 19 Nov 2025 23:53:34 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a63055b283755fe7606cf5705515cad883e2be97951eea54aa65111ea7c2401`  
		Last Modified: Wed, 19 Nov 2025 23:53:34 GMT  
		Size: 1.5 MB (1509253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1732f2a4d259de59025f7b24131d102baa7d5ce8bfd3f6434a02c9422bdfe3af`  
		Last Modified: Wed, 19 Nov 2025 23:53:34 GMT  
		Size: 933.7 KB (933744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc84fd2f3ac16fac9b4dc030f1ae39c85e43aebf24622b992cd2742f72d2a4f`  
		Last Modified: Wed, 19 Nov 2025 23:53:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7230971360e4fcf9598f6da2dea4a9d88677de2159250377dc546fb30054c06b`  
		Last Modified: Wed, 19 Nov 2025 23:53:34 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88373bcb58c13742837969290a751557f5c4780d0b0cef938ccb70b1f4b71273`  
		Last Modified: Wed, 19 Nov 2025 23:55:18 GMT  
		Size: 291.4 MB (291440597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89cc6fb1ead335938be1bf1d6b61a3eaf691dc07b2c03bcd5039adb039c3fa7`  
		Last Modified: Wed, 19 Nov 2025 23:53:34 GMT  
		Size: 5.0 KB (5006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:6d77eee39254e51a7bc62da2d458c79ffd1b0efa021dd559ddd75cb7aea39128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c76fb8bc695fc264713c24b2b03bf5c2ad6641ec8d7db308a0bc16da2c5dc`

```dockerfile
```

-	Layers:
	-	`sha256:41c6374abe8565133c365c230f5f678f50c10c08a78e701d3c3a4398d5d60dd4`  
		Last Modified: Thu, 20 Nov 2025 02:08:10 GMT  
		Size: 2.7 MB (2666292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f21b4c8eacfa56acebd64fb66b483a1c547fb330e6ce3293b0265b57bceb1b`  
		Last Modified: Thu, 20 Nov 2025 02:08:11 GMT  
		Size: 28.8 KB (28791 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:c5c7a4f391bfd632f73a7802a200c0c01ba5fb372c01ee2993bc02927cfa9158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309616119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e9faee9b5157cfd9e52099de5d93684cc196449556ac21a450ca1500aace7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 19 Nov 2025 23:53:14 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 19 Nov 2025 23:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 23:53:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 19 Nov 2025 23:53:37 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 19 Nov 2025 23:53:37 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 19 Nov 2025 23:53:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 19 Nov 2025 23:53:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 19 Nov 2025 23:53:37 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 19 Nov 2025 23:53:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 19 Nov 2025 23:53:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 19 Nov 2025 23:53:37 GMT
ENV MONGO_MAJOR=8.2
# Wed, 19 Nov 2025 23:53:37 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 19 Nov 2025 23:53:37 GMT
ENV MONGO_VERSION=8.2.2
# Wed, 19 Nov 2025 23:54:02 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 19 Nov 2025 23:54:02 GMT
VOLUME [/data/db /data/configdb]
# Wed, 19 Nov 2025 23:54:02 GMT
ENV HOME=/data/db
# Wed, 19 Nov 2025 23:54:02 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 19 Nov 2025 23:54:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 23:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 23:54:02 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 19 Nov 2025 23:54:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd23ef5b73dfc6f39f31ccd6224d70dae1d33424ee592fb4c5e18712046644c3`  
		Last Modified: Wed, 19 Nov 2025 23:54:57 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3cb71bd61e75ff43f1c288ef3ce67cfc098fdf6f395e486bc4ccbc1c259822`  
		Last Modified: Wed, 19 Nov 2025 23:54:56 GMT  
		Size: 1.5 MB (1494203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfda843875a5bf192b0a711ac32a20adf4556302ae088d75c477388e5a85b3`  
		Last Modified: Wed, 19 Nov 2025 23:54:56 GMT  
		Size: 886.0 KB (885968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef893190391e7b91d6c6acde99b1480e4c3fd48a7015c1699a4418d3cd8d5e`  
		Last Modified: Wed, 19 Nov 2025 23:54:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b59ce16b5f1dc32c36a63cdb5a96c348e89e1f9894c83b7c83cabaaa0cda84`  
		Last Modified: Wed, 19 Nov 2025 23:54:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22959d540d64a47dff45d8ba504546a108240abac541e19bf96c370c4f431918`  
		Last Modified: Thu, 20 Nov 2025 00:10:55 GMT  
		Size: 278.4 MB (278367388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972a29b10435a1f8e4dd0d51fb0484fc558123c33acca29c881187bd892b7ec`  
		Last Modified: Wed, 19 Nov 2025 23:54:55 GMT  
		Size: 5.0 KB (5006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:3502fc1dd125bed12b6b55e19aa5b66cdb48e1eecc389dcb94b6557cc99a7d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded9c05164cdb55d54c7d999507e75508f5e113d9b29d27f492897762c87a64f`

```dockerfile
```

-	Layers:
	-	`sha256:966fdd61e116d41604b7d8a8188d7b61bbc395af1963f0de6c7ef0d22bbc060a`  
		Last Modified: Thu, 20 Nov 2025 00:34:31 GMT  
		Size: 2.7 MB (2667428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a03ccad7ff1baa55fffe08760a402c5a73d94daad8b6d53c485f957798497c6`  
		Last Modified: Thu, 20 Nov 2025 00:34:30 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json
