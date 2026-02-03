## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b74502b5b2fc1acc9d732c8b70acf7234468a0d6cb55813814d7220103b05930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245990939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bb4d4f2b725d8becc8b20182ffea9bdc909dec3e2de1de09f624207141101a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 02 Feb 2026 19:20:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 02 Feb 2026 19:20:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 02 Feb 2026 19:20:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 02 Feb 2026 19:20:17 GMT
ARG REPO_CHANNEL=stable
# Mon, 02 Feb 2026 19:20:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 02 Feb 2026 19:20:17 GMT
ARG VERSION=26.1.1.912
# Mon, 02 Feb 2026 19:20:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 02 Feb 2026 19:20:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 02 Feb 2026 19:20:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 02 Feb 2026 19:20:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 02 Feb 2026 19:20:46 GMT
ENV LANG=en_US.UTF-8
# Mon, 02 Feb 2026 19:20:46 GMT
ENV TZ=UTC
# Mon, 02 Feb 2026 19:20:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 02 Feb 2026 19:20:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 02 Feb 2026 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Feb 2026 19:20:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 02 Feb 2026 19:20:46 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 02 Feb 2026 19:20:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 02 Feb 2026 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c17ec233300a53c134a09d6a8e50bee26ddf34a1606785fab1885be201c97`  
		Last Modified: Mon, 02 Feb 2026 19:21:12 GMT  
		Size: 7.6 MB (7598255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6572ed2a104bf44313a897521a01d0812f25dc75caefba43ec91afdd88ee8276`  
		Last Modified: Mon, 02 Feb 2026 19:21:16 GMT  
		Size: 208.0 MB (207985970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f63a1ddd47459858f93abe3f365a47fdc30daea9790063ae363e133ff44c49`  
		Last Modified: Mon, 02 Feb 2026 19:21:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aef332b97189862327571455d5f1b519ca5d77bc37f8054e62fc758c2f7ba53`  
		Last Modified: Mon, 02 Feb 2026 19:21:11 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d26f5e9fdad98ad6b5d6e85fb31a6d429acef0956c519cc01a52f943adcea4`  
		Last Modified: Mon, 02 Feb 2026 19:21:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49ea65459e03a20b0051c064c3979311e12b907d3ce0f0562c63aeaf2b75c80`  
		Last Modified: Mon, 02 Feb 2026 19:21:13 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30227b7ec7d1283808ae55b89603dd0c63a0271fb27a8bb1fc738680753af41`  
		Last Modified: Mon, 02 Feb 2026 19:21:13 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c63e23b5a0a78a144828afb7debf09c35073fc754c8bf126bff21d012ef8d689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92f5b5688a07cf827007181e4a136806883beb7673cf4a66e952619319f8e0a`

```dockerfile
```

-	Layers:
	-	`sha256:75b0fcf2593073eb5cd1a3ecd5d5aa00356b5d4f3f8f5afd8bd9b6c1de537420`  
		Last Modified: Mon, 02 Feb 2026 19:21:11 GMT  
		Size: 26.0 KB (26039 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1869dc50345f9da8cb4251798192e63949814344f30b1009673d7f802f32c3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228182232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90a72eeae66b56b14961176b32740b07c9c8bc58d7a86b356ca7b07287a0fa4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Feb 2026 19:24:20 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 02 Feb 2026 19:24:20 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 02 Feb 2026 19:24:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 02 Feb 2026 19:24:20 GMT
ARG REPO_CHANNEL=stable
# Mon, 02 Feb 2026 19:24:20 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 02 Feb 2026 19:24:20 GMT
ARG VERSION=26.1.1.912
# Mon, 02 Feb 2026 19:24:20 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 02 Feb 2026 19:24:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 02 Feb 2026 19:24:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 02 Feb 2026 19:24:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 02 Feb 2026 19:24:51 GMT
ENV LANG=en_US.UTF-8
# Mon, 02 Feb 2026 19:24:51 GMT
ENV TZ=UTC
# Mon, 02 Feb 2026 19:24:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.1.912 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 02 Feb 2026 19:24:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 02 Feb 2026 19:24:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Feb 2026 19:24:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 02 Feb 2026 19:24:51 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 02 Feb 2026 19:24:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 02 Feb 2026 19:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede8ae520eb5d513e8aade6069115c9224f3dd84229d164b62ca625704b1a2d2`  
		Last Modified: Mon, 02 Feb 2026 19:25:13 GMT  
		Size: 7.6 MB (7577372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da55dd13937fcd97e3ff62896fa738b20873e1381a07bb4d2a519773115de2f7`  
		Last Modified: Mon, 02 Feb 2026 19:25:17 GMT  
		Size: 192.4 MB (192351310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38858aae40685b96ded2fa806238b68b6b8d8aa71929f0adcf3b8716ccf14303`  
		Last Modified: Mon, 02 Feb 2026 19:25:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c930032b73430a6adb438ccaa808208db640c79e86f89fd14abc1566c47ecb81`  
		Last Modified: Mon, 02 Feb 2026 19:25:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4bae9574079d57d3194867e6f2ebe31719d3660602c9e15c476c29ffad5249`  
		Last Modified: Mon, 02 Feb 2026 19:25:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1f46de6818b1ab215d854174f20952300b10be264bf36903ac562032e0ed11`  
		Last Modified: Mon, 02 Feb 2026 19:25:14 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb47a4e4de3ef2c87f23e11ebe414f46ce93948c7f1bc8cee5090338a43e3b`  
		Last Modified: Mon, 02 Feb 2026 19:25:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4dbc952fc945b6d5ba771fb02ed25571635573cf2104e18305b33b55a5e31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393b9d46266ea622bfa70aac38a48100e1aa16129cd59d2a0cae998f8fae90cf`

```dockerfile
```

-	Layers:
	-	`sha256:57292d24058ad36343b4f8e206d849ac168a79ad2aef37348d1939b0b8e39454`  
		Last Modified: Mon, 02 Feb 2026 19:25:13 GMT  
		Size: 26.3 KB (26251 bytes)  
		MIME: application/vnd.in-toto+json
