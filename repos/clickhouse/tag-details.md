<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.11`](#clickhouse2511)
-	[`clickhouse:25.11-jammy`](#clickhouse2511-jammy)
-	[`clickhouse:25.11.8`](#clickhouse25118)
-	[`clickhouse:25.11.8-jammy`](#clickhouse25118-jammy)
-	[`clickhouse:25.11.8.25`](#clickhouse2511825)
-	[`clickhouse:25.11.8.25-jammy`](#clickhouse2511825-jammy)
-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.4`](#clickhouse25124)
-	[`clickhouse:25.12.4-jammy`](#clickhouse25124-jammy)
-	[`clickhouse:25.12.4.35`](#clickhouse2512435)
-	[`clickhouse:25.12.4.35-jammy`](#clickhouse2512435-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.13`](#clickhouse25313)
-	[`clickhouse:25.3.13-jammy`](#clickhouse25313-jammy)
-	[`clickhouse:25.3.13.19`](#clickhouse2531319)
-	[`clickhouse:25.3.13.19-jammy`](#clickhouse2531319-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.15`](#clickhouse25815)
-	[`clickhouse:25.8.15-jammy`](#clickhouse25815-jammy)
-	[`clickhouse:25.8.15.35`](#clickhouse2581535)
-	[`clickhouse:25.8.15.35-jammy`](#clickhouse2581535-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.1`](#clickhouse2611)
-	[`clickhouse:26.1.1-jammy`](#clickhouse2611-jammy)
-	[`clickhouse:26.1.1.912`](#clickhouse2611912)
-	[`clickhouse:26.1.1.912-jammy`](#clickhouse2611912-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.11`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
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
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
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
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
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
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
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
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
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
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
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
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8-jammy`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
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
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
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
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8.25`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8.25` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
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
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8.25` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
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
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8.25-jammy`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8.25-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
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
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8.25-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
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
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:a96fa399dc390008a0dbb98c045e54d9e0df8dc3dda876756535b581b3f2dbd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:801198b0ee4f1eda56205381b44143a744bca7dcccf2229726abe35b6db98f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246298095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60394d3a17c4bc173de2c19d4fad082c84c4bfc1876b496964d851a3c48a4138`
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
# Thu, 22 Jan 2026 19:17:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:24 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:17:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:17:52 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:17:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:17:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687afa5a8f20bd709ec4fece999bb30f131f451f07d0301ca959940a6c4a9907`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 7.6 MB (7598269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186aad36200ae63d2a501bdb3191c3de577350633455dbc60e612758c96fc95`  
		Last Modified: Thu, 22 Jan 2026 19:18:20 GMT  
		Size: 208.3 MB (208293107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93590dbacc5ee975d37b6804e1dfeea218ccf68ae4c30e75e2014f32e76da5d4`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512709b060cd5753c2b9fe9129939fff87f113831e19fe4a0b822b2fab537fb5`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61cfdf737d28c6626dacdc5de0e95eb0d3cbb4e3332e033243d3951e613c45`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94ef979c098c2429cedac3cc222dc67b932aaa1f34436218ee02adb9c041b4`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8301268ee6fd2838206e07c30940ca445da87d36645f1dba74e6333bb62dee`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50d58bb62dfd93d24f0805e03d909b695454e29b6bfe49d0548270768415efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4b0a208c4edb68fbe7d3df0f20fa17c90ad9bd314a1c0107f6bc26f9e72b19`

```dockerfile
```

-	Layers:
	-	`sha256:1bac3a4f163ee0d1b6a213b9601de42663f71bd2be0c05729a1f382133a36f35`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 26.0 KB (26046 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3b985fa1fbaa71e1bc64f0595a07dc1c99d2dd18690d91c0b8f892fd9532572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228248485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c07c7b1690572c170a0dc54a47d435d9fc6b7ab3e6993e610e6747dfb94c609`
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
# Thu, 22 Jan 2026 19:21:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:36 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:21:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:04 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8780ab146b612301ab5a1921518ab4aa45310bc49f3e8e503ac6f5f8939b9fa`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 7.6 MB (7576419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46310392d947a9c3a6a9cc45469f93b6c7fdec37d08be7eeb31b0cee84e1730e`  
		Last Modified: Thu, 22 Jan 2026 19:22:30 GMT  
		Size: 192.4 MB (192418517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273a192d26bb4bb46eab0cbbf3be6b579971b11a145903592d9739fcc73af95`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da8dae6a0fc6e7a7c65b2018f9bed5e4ffca96be98c6c3aefc8cc84ba4c1d`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1923f159bae01b625076ac367fb0f2a2bf1f127cbb58ba46b2884e3783d0cc7`  
		Last Modified: Thu, 22 Jan 2026 19:22:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42779fe1b68e7509172dcb898335cc26659c1c44521053482c5429c74a601de2`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6604d22028da5fc11b3d2488ab2938c19caa01b279945358be3accc6c2cbe`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:221af12bab0c761910e4ef5cc817d7d02618a0349790a8f13620d3cca79663f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67838c69d848e286e8296ca909dfdfba17076d92db45a029dee38ea0b54026a5`

```dockerfile
```

-	Layers:
	-	`sha256:134292be5bf7708f0d545477a562cd9a26504d710f118d7d1487ad263eddf0ac`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:a96fa399dc390008a0dbb98c045e54d9e0df8dc3dda876756535b581b3f2dbd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:801198b0ee4f1eda56205381b44143a744bca7dcccf2229726abe35b6db98f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246298095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60394d3a17c4bc173de2c19d4fad082c84c4bfc1876b496964d851a3c48a4138`
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
# Thu, 22 Jan 2026 19:17:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:24 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:17:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:17:52 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:17:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:17:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687afa5a8f20bd709ec4fece999bb30f131f451f07d0301ca959940a6c4a9907`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 7.6 MB (7598269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186aad36200ae63d2a501bdb3191c3de577350633455dbc60e612758c96fc95`  
		Last Modified: Thu, 22 Jan 2026 19:18:20 GMT  
		Size: 208.3 MB (208293107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93590dbacc5ee975d37b6804e1dfeea218ccf68ae4c30e75e2014f32e76da5d4`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512709b060cd5753c2b9fe9129939fff87f113831e19fe4a0b822b2fab537fb5`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61cfdf737d28c6626dacdc5de0e95eb0d3cbb4e3332e033243d3951e613c45`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94ef979c098c2429cedac3cc222dc67b932aaa1f34436218ee02adb9c041b4`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8301268ee6fd2838206e07c30940ca445da87d36645f1dba74e6333bb62dee`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50d58bb62dfd93d24f0805e03d909b695454e29b6bfe49d0548270768415efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4b0a208c4edb68fbe7d3df0f20fa17c90ad9bd314a1c0107f6bc26f9e72b19`

```dockerfile
```

-	Layers:
	-	`sha256:1bac3a4f163ee0d1b6a213b9601de42663f71bd2be0c05729a1f382133a36f35`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 26.0 KB (26046 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3b985fa1fbaa71e1bc64f0595a07dc1c99d2dd18690d91c0b8f892fd9532572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228248485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c07c7b1690572c170a0dc54a47d435d9fc6b7ab3e6993e610e6747dfb94c609`
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
# Thu, 22 Jan 2026 19:21:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:36 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:21:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:04 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8780ab146b612301ab5a1921518ab4aa45310bc49f3e8e503ac6f5f8939b9fa`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 7.6 MB (7576419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46310392d947a9c3a6a9cc45469f93b6c7fdec37d08be7eeb31b0cee84e1730e`  
		Last Modified: Thu, 22 Jan 2026 19:22:30 GMT  
		Size: 192.4 MB (192418517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273a192d26bb4bb46eab0cbbf3be6b579971b11a145903592d9739fcc73af95`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da8dae6a0fc6e7a7c65b2018f9bed5e4ffca96be98c6c3aefc8cc84ba4c1d`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1923f159bae01b625076ac367fb0f2a2bf1f127cbb58ba46b2884e3783d0cc7`  
		Last Modified: Thu, 22 Jan 2026 19:22:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42779fe1b68e7509172dcb898335cc26659c1c44521053482c5429c74a601de2`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6604d22028da5fc11b3d2488ab2938c19caa01b279945358be3accc6c2cbe`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:221af12bab0c761910e4ef5cc817d7d02618a0349790a8f13620d3cca79663f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67838c69d848e286e8296ca909dfdfba17076d92db45a029dee38ea0b54026a5`

```dockerfile
```

-	Layers:
	-	`sha256:134292be5bf7708f0d545477a562cd9a26504d710f118d7d1487ad263eddf0ac`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.4`

```console
$ docker pull clickhouse@sha256:a96fa399dc390008a0dbb98c045e54d9e0df8dc3dda876756535b581b3f2dbd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:801198b0ee4f1eda56205381b44143a744bca7dcccf2229726abe35b6db98f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246298095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60394d3a17c4bc173de2c19d4fad082c84c4bfc1876b496964d851a3c48a4138`
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
# Thu, 22 Jan 2026 19:17:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:24 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:17:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:17:52 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:17:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:17:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687afa5a8f20bd709ec4fece999bb30f131f451f07d0301ca959940a6c4a9907`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 7.6 MB (7598269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186aad36200ae63d2a501bdb3191c3de577350633455dbc60e612758c96fc95`  
		Last Modified: Thu, 22 Jan 2026 19:18:20 GMT  
		Size: 208.3 MB (208293107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93590dbacc5ee975d37b6804e1dfeea218ccf68ae4c30e75e2014f32e76da5d4`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512709b060cd5753c2b9fe9129939fff87f113831e19fe4a0b822b2fab537fb5`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61cfdf737d28c6626dacdc5de0e95eb0d3cbb4e3332e033243d3951e613c45`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94ef979c098c2429cedac3cc222dc67b932aaa1f34436218ee02adb9c041b4`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8301268ee6fd2838206e07c30940ca445da87d36645f1dba74e6333bb62dee`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50d58bb62dfd93d24f0805e03d909b695454e29b6bfe49d0548270768415efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4b0a208c4edb68fbe7d3df0f20fa17c90ad9bd314a1c0107f6bc26f9e72b19`

```dockerfile
```

-	Layers:
	-	`sha256:1bac3a4f163ee0d1b6a213b9601de42663f71bd2be0c05729a1f382133a36f35`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 26.0 KB (26046 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3b985fa1fbaa71e1bc64f0595a07dc1c99d2dd18690d91c0b8f892fd9532572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228248485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c07c7b1690572c170a0dc54a47d435d9fc6b7ab3e6993e610e6747dfb94c609`
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
# Thu, 22 Jan 2026 19:21:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:36 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:21:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:04 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8780ab146b612301ab5a1921518ab4aa45310bc49f3e8e503ac6f5f8939b9fa`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 7.6 MB (7576419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46310392d947a9c3a6a9cc45469f93b6c7fdec37d08be7eeb31b0cee84e1730e`  
		Last Modified: Thu, 22 Jan 2026 19:22:30 GMT  
		Size: 192.4 MB (192418517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273a192d26bb4bb46eab0cbbf3be6b579971b11a145903592d9739fcc73af95`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da8dae6a0fc6e7a7c65b2018f9bed5e4ffca96be98c6c3aefc8cc84ba4c1d`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1923f159bae01b625076ac367fb0f2a2bf1f127cbb58ba46b2884e3783d0cc7`  
		Last Modified: Thu, 22 Jan 2026 19:22:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42779fe1b68e7509172dcb898335cc26659c1c44521053482c5429c74a601de2`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6604d22028da5fc11b3d2488ab2938c19caa01b279945358be3accc6c2cbe`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:221af12bab0c761910e4ef5cc817d7d02618a0349790a8f13620d3cca79663f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67838c69d848e286e8296ca909dfdfba17076d92db45a029dee38ea0b54026a5`

```dockerfile
```

-	Layers:
	-	`sha256:134292be5bf7708f0d545477a562cd9a26504d710f118d7d1487ad263eddf0ac`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.4-jammy`

```console
$ docker pull clickhouse@sha256:a96fa399dc390008a0dbb98c045e54d9e0df8dc3dda876756535b581b3f2dbd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:801198b0ee4f1eda56205381b44143a744bca7dcccf2229726abe35b6db98f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246298095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60394d3a17c4bc173de2c19d4fad082c84c4bfc1876b496964d851a3c48a4138`
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
# Thu, 22 Jan 2026 19:17:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:24 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:17:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:17:52 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:17:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:17:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687afa5a8f20bd709ec4fece999bb30f131f451f07d0301ca959940a6c4a9907`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 7.6 MB (7598269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186aad36200ae63d2a501bdb3191c3de577350633455dbc60e612758c96fc95`  
		Last Modified: Thu, 22 Jan 2026 19:18:20 GMT  
		Size: 208.3 MB (208293107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93590dbacc5ee975d37b6804e1dfeea218ccf68ae4c30e75e2014f32e76da5d4`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512709b060cd5753c2b9fe9129939fff87f113831e19fe4a0b822b2fab537fb5`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61cfdf737d28c6626dacdc5de0e95eb0d3cbb4e3332e033243d3951e613c45`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94ef979c098c2429cedac3cc222dc67b932aaa1f34436218ee02adb9c041b4`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8301268ee6fd2838206e07c30940ca445da87d36645f1dba74e6333bb62dee`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50d58bb62dfd93d24f0805e03d909b695454e29b6bfe49d0548270768415efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4b0a208c4edb68fbe7d3df0f20fa17c90ad9bd314a1c0107f6bc26f9e72b19`

```dockerfile
```

-	Layers:
	-	`sha256:1bac3a4f163ee0d1b6a213b9601de42663f71bd2be0c05729a1f382133a36f35`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 26.0 KB (26046 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3b985fa1fbaa71e1bc64f0595a07dc1c99d2dd18690d91c0b8f892fd9532572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228248485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c07c7b1690572c170a0dc54a47d435d9fc6b7ab3e6993e610e6747dfb94c609`
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
# Thu, 22 Jan 2026 19:21:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:36 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:21:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:04 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8780ab146b612301ab5a1921518ab4aa45310bc49f3e8e503ac6f5f8939b9fa`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 7.6 MB (7576419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46310392d947a9c3a6a9cc45469f93b6c7fdec37d08be7eeb31b0cee84e1730e`  
		Last Modified: Thu, 22 Jan 2026 19:22:30 GMT  
		Size: 192.4 MB (192418517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273a192d26bb4bb46eab0cbbf3be6b579971b11a145903592d9739fcc73af95`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da8dae6a0fc6e7a7c65b2018f9bed5e4ffca96be98c6c3aefc8cc84ba4c1d`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1923f159bae01b625076ac367fb0f2a2bf1f127cbb58ba46b2884e3783d0cc7`  
		Last Modified: Thu, 22 Jan 2026 19:22:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42779fe1b68e7509172dcb898335cc26659c1c44521053482c5429c74a601de2`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6604d22028da5fc11b3d2488ab2938c19caa01b279945358be3accc6c2cbe`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:221af12bab0c761910e4ef5cc817d7d02618a0349790a8f13620d3cca79663f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67838c69d848e286e8296ca909dfdfba17076d92db45a029dee38ea0b54026a5`

```dockerfile
```

-	Layers:
	-	`sha256:134292be5bf7708f0d545477a562cd9a26504d710f118d7d1487ad263eddf0ac`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.4.35`

```console
$ docker pull clickhouse@sha256:a96fa399dc390008a0dbb98c045e54d9e0df8dc3dda876756535b581b3f2dbd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.4.35` - linux; amd64

```console
$ docker pull clickhouse@sha256:801198b0ee4f1eda56205381b44143a744bca7dcccf2229726abe35b6db98f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246298095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60394d3a17c4bc173de2c19d4fad082c84c4bfc1876b496964d851a3c48a4138`
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
# Thu, 22 Jan 2026 19:17:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:24 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:17:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:17:52 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:17:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:17:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687afa5a8f20bd709ec4fece999bb30f131f451f07d0301ca959940a6c4a9907`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 7.6 MB (7598269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186aad36200ae63d2a501bdb3191c3de577350633455dbc60e612758c96fc95`  
		Last Modified: Thu, 22 Jan 2026 19:18:20 GMT  
		Size: 208.3 MB (208293107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93590dbacc5ee975d37b6804e1dfeea218ccf68ae4c30e75e2014f32e76da5d4`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512709b060cd5753c2b9fe9129939fff87f113831e19fe4a0b822b2fab537fb5`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61cfdf737d28c6626dacdc5de0e95eb0d3cbb4e3332e033243d3951e613c45`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94ef979c098c2429cedac3cc222dc67b932aaa1f34436218ee02adb9c041b4`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8301268ee6fd2838206e07c30940ca445da87d36645f1dba74e6333bb62dee`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50d58bb62dfd93d24f0805e03d909b695454e29b6bfe49d0548270768415efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4b0a208c4edb68fbe7d3df0f20fa17c90ad9bd314a1c0107f6bc26f9e72b19`

```dockerfile
```

-	Layers:
	-	`sha256:1bac3a4f163ee0d1b6a213b9601de42663f71bd2be0c05729a1f382133a36f35`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 26.0 KB (26046 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.4.35` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3b985fa1fbaa71e1bc64f0595a07dc1c99d2dd18690d91c0b8f892fd9532572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228248485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c07c7b1690572c170a0dc54a47d435d9fc6b7ab3e6993e610e6747dfb94c609`
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
# Thu, 22 Jan 2026 19:21:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:36 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:21:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:04 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8780ab146b612301ab5a1921518ab4aa45310bc49f3e8e503ac6f5f8939b9fa`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 7.6 MB (7576419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46310392d947a9c3a6a9cc45469f93b6c7fdec37d08be7eeb31b0cee84e1730e`  
		Last Modified: Thu, 22 Jan 2026 19:22:30 GMT  
		Size: 192.4 MB (192418517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273a192d26bb4bb46eab0cbbf3be6b579971b11a145903592d9739fcc73af95`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da8dae6a0fc6e7a7c65b2018f9bed5e4ffca96be98c6c3aefc8cc84ba4c1d`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1923f159bae01b625076ac367fb0f2a2bf1f127cbb58ba46b2884e3783d0cc7`  
		Last Modified: Thu, 22 Jan 2026 19:22:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42779fe1b68e7509172dcb898335cc26659c1c44521053482c5429c74a601de2`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6604d22028da5fc11b3d2488ab2938c19caa01b279945358be3accc6c2cbe`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:221af12bab0c761910e4ef5cc817d7d02618a0349790a8f13620d3cca79663f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67838c69d848e286e8296ca909dfdfba17076d92db45a029dee38ea0b54026a5`

```dockerfile
```

-	Layers:
	-	`sha256:134292be5bf7708f0d545477a562cd9a26504d710f118d7d1487ad263eddf0ac`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.4.35-jammy`

```console
$ docker pull clickhouse@sha256:a96fa399dc390008a0dbb98c045e54d9e0df8dc3dda876756535b581b3f2dbd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.4.35-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:801198b0ee4f1eda56205381b44143a744bca7dcccf2229726abe35b6db98f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246298095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60394d3a17c4bc173de2c19d4fad082c84c4bfc1876b496964d851a3c48a4138`
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
# Thu, 22 Jan 2026 19:17:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:24 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:17:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:17:52 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:17:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:17:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:17:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:17:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687afa5a8f20bd709ec4fece999bb30f131f451f07d0301ca959940a6c4a9907`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 7.6 MB (7598269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186aad36200ae63d2a501bdb3191c3de577350633455dbc60e612758c96fc95`  
		Last Modified: Thu, 22 Jan 2026 19:18:20 GMT  
		Size: 208.3 MB (208293107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93590dbacc5ee975d37b6804e1dfeea218ccf68ae4c30e75e2014f32e76da5d4`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512709b060cd5753c2b9fe9129939fff87f113831e19fe4a0b822b2fab537fb5`  
		Last Modified: Thu, 22 Jan 2026 19:18:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61cfdf737d28c6626dacdc5de0e95eb0d3cbb4e3332e033243d3951e613c45`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94ef979c098c2429cedac3cc222dc67b932aaa1f34436218ee02adb9c041b4`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8301268ee6fd2838206e07c30940ca445da87d36645f1dba74e6333bb62dee`  
		Last Modified: Thu, 22 Jan 2026 19:18:16 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50d58bb62dfd93d24f0805e03d909b695454e29b6bfe49d0548270768415efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4b0a208c4edb68fbe7d3df0f20fa17c90ad9bd314a1c0107f6bc26f9e72b19`

```dockerfile
```

-	Layers:
	-	`sha256:1bac3a4f163ee0d1b6a213b9601de42663f71bd2be0c05729a1f382133a36f35`  
		Last Modified: Thu, 22 Jan 2026 19:18:14 GMT  
		Size: 26.0 KB (26046 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.4.35-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3b985fa1fbaa71e1bc64f0595a07dc1c99d2dd18690d91c0b8f892fd9532572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228248485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c07c7b1690572c170a0dc54a47d435d9fc6b7ab3e6993e610e6747dfb94c609`
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
# Thu, 22 Jan 2026 19:21:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:36 GMT
ARG VERSION=25.12.4.35
# Thu, 22 Jan 2026 19:21:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:04 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8780ab146b612301ab5a1921518ab4aa45310bc49f3e8e503ac6f5f8939b9fa`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 7.6 MB (7576419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46310392d947a9c3a6a9cc45469f93b6c7fdec37d08be7eeb31b0cee84e1730e`  
		Last Modified: Thu, 22 Jan 2026 19:22:30 GMT  
		Size: 192.4 MB (192418517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273a192d26bb4bb46eab0cbbf3be6b579971b11a145903592d9739fcc73af95`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da8dae6a0fc6e7a7c65b2018f9bed5e4ffca96be98c6c3aefc8cc84ba4c1d`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1923f159bae01b625076ac367fb0f2a2bf1f127cbb58ba46b2884e3783d0cc7`  
		Last Modified: Thu, 22 Jan 2026 19:22:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42779fe1b68e7509172dcb898335cc26659c1c44521053482c5429c74a601de2`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6604d22028da5fc11b3d2488ab2938c19caa01b279945358be3accc6c2cbe`  
		Last Modified: Thu, 22 Jan 2026 19:22:28 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.4.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:221af12bab0c761910e4ef5cc817d7d02618a0349790a8f13620d3cca79663f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67838c69d848e286e8296ca909dfdfba17076d92db45a029dee38ea0b54026a5`

```dockerfile
```

-	Layers:
	-	`sha256:134292be5bf7708f0d545477a562cd9a26504d710f118d7d1487ad263eddf0ac`  
		Last Modified: Thu, 22 Jan 2026 19:22:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:a60e53915564daf2d5d6fe777422f54f76cef1b595c3c6f195233c4a9f81e4d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:1981043d54b910e18f054863ff68b951431b655efd63f967e13a8e268fc70796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206327508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40d95438d3dc6c274458a0f2115075e7b615c1981c516f0d1f59192bacfc055`
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
# Thu, 22 Jan 2026 19:19:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:19:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:19:44 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:19:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:20:09 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:20:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:20:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:20:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4bb92a5a94ca6757c2da82bea4ce7bcead839fd455170531055fd96902`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 7.2 MB (7151352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06899fd4a8fd5b7b0eb7d9404bfbd651d59693dcaeadeb7caa3d94d13ad119e3`  
		Last Modified: Thu, 22 Jan 2026 19:20:32 GMT  
		Size: 168.8 MB (168769240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca408ab305496b7f1a003e523e3b50cbdbcd2bacd10ca12c920ef1bfcadc3a`  
		Last Modified: Thu, 22 Jan 2026 19:20:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a6c62a7877e796f0bdea6facc20e05dafc36076dff282d30a7413332a5704`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f249ea01bc14fe6376f0628bfe11d52074d9da1975e84b01cad4e417d3174b`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b726e025f493d5169e38289db866af96fec79f5663e883dbca9a402a7548e`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca273c02f05ca3a0c6da50d5a566cbac4343526ff4d2282915ef293eb3c41e2f`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:213913a934867686cd8672ebcbb757f5829523469a335319970d47c4f7150638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d04991a8149c6f403a3c2f9dda84887195257ebfe053f44b106c7643a7f19d4`

```dockerfile
```

-	Layers:
	-	`sha256:5fdabf5e465e1ef0ec785ce7c7d270b53668db6dbfafd1586fecfc5fb7daac47`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7d61db683bccc53989acaaeec4bd0ae332bbadf91fff2c3f5cb20f4b23fcedbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83475229ee9407e31786ad76084e8e3efa29f72bbcd6ca323c1ff2e306e2d348`
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
# Thu, 22 Jan 2026 19:22:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:22:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:22:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:22:17 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:22:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:39:58 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:39:58 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:39:58 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913952d97184f6a9730410d25d2084e15eac92b65adf5d12ba06b05698e92fd9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 7.1 MB (7126669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1052a8a252ec48476e48269fdad77443b10017d930c1b1012b8a16632e994f3`  
		Last Modified: Thu, 22 Jan 2026 19:40:17 GMT  
		Size: 158.4 MB (158419059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ee44031a93f254f5eafc816186c99897c9e95d009ecd0f9ba27312f3c6d0c`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef64c2784db8b10473505cefe99fc5c85d382a13cb92845d4cc01524c571ca9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96fba4fc15ee92ab4c3fcc45463e9a7c87ee42e5bcc3b77515fe4fa9f89b3a`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7841e46b4ba78fb89a19809574ea6bd50185e58221121fdacb339af1bc73826c`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb6a5adf593dd7b1bbeba23d8bf76309efb7423cd0735e2cb65b19bfdf2e22`  
		Last Modified: Thu, 22 Jan 2026 19:40:16 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d53b7a35f3c16d3074227875fc720d4d44dc74a68e8e81ca92ae3c71030206cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f770ed9bb32810eb455181d13d5c22a2b298cf867b83ddc7ce4f8de21dd4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:e362dea85780ffbc23c0507c0598b55b048b1344ba7c2d467a478a3841135478`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:a60e53915564daf2d5d6fe777422f54f76cef1b595c3c6f195233c4a9f81e4d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1981043d54b910e18f054863ff68b951431b655efd63f967e13a8e268fc70796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206327508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40d95438d3dc6c274458a0f2115075e7b615c1981c516f0d1f59192bacfc055`
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
# Thu, 22 Jan 2026 19:19:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:19:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:19:44 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:19:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:20:09 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:20:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:20:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:20:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4bb92a5a94ca6757c2da82bea4ce7bcead839fd455170531055fd96902`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 7.2 MB (7151352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06899fd4a8fd5b7b0eb7d9404bfbd651d59693dcaeadeb7caa3d94d13ad119e3`  
		Last Modified: Thu, 22 Jan 2026 19:20:32 GMT  
		Size: 168.8 MB (168769240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca408ab305496b7f1a003e523e3b50cbdbcd2bacd10ca12c920ef1bfcadc3a`  
		Last Modified: Thu, 22 Jan 2026 19:20:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a6c62a7877e796f0bdea6facc20e05dafc36076dff282d30a7413332a5704`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f249ea01bc14fe6376f0628bfe11d52074d9da1975e84b01cad4e417d3174b`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b726e025f493d5169e38289db866af96fec79f5663e883dbca9a402a7548e`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca273c02f05ca3a0c6da50d5a566cbac4343526ff4d2282915ef293eb3c41e2f`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:213913a934867686cd8672ebcbb757f5829523469a335319970d47c4f7150638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d04991a8149c6f403a3c2f9dda84887195257ebfe053f44b106c7643a7f19d4`

```dockerfile
```

-	Layers:
	-	`sha256:5fdabf5e465e1ef0ec785ce7c7d270b53668db6dbfafd1586fecfc5fb7daac47`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7d61db683bccc53989acaaeec4bd0ae332bbadf91fff2c3f5cb20f4b23fcedbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83475229ee9407e31786ad76084e8e3efa29f72bbcd6ca323c1ff2e306e2d348`
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
# Thu, 22 Jan 2026 19:22:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:22:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:22:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:22:17 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:22:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:39:58 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:39:58 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:39:58 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913952d97184f6a9730410d25d2084e15eac92b65adf5d12ba06b05698e92fd9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 7.1 MB (7126669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1052a8a252ec48476e48269fdad77443b10017d930c1b1012b8a16632e994f3`  
		Last Modified: Thu, 22 Jan 2026 19:40:17 GMT  
		Size: 158.4 MB (158419059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ee44031a93f254f5eafc816186c99897c9e95d009ecd0f9ba27312f3c6d0c`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef64c2784db8b10473505cefe99fc5c85d382a13cb92845d4cc01524c571ca9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96fba4fc15ee92ab4c3fcc45463e9a7c87ee42e5bcc3b77515fe4fa9f89b3a`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7841e46b4ba78fb89a19809574ea6bd50185e58221121fdacb339af1bc73826c`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb6a5adf593dd7b1bbeba23d8bf76309efb7423cd0735e2cb65b19bfdf2e22`  
		Last Modified: Thu, 22 Jan 2026 19:40:16 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d53b7a35f3c16d3074227875fc720d4d44dc74a68e8e81ca92ae3c71030206cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f770ed9bb32810eb455181d13d5c22a2b298cf867b83ddc7ce4f8de21dd4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:e362dea85780ffbc23c0507c0598b55b048b1344ba7c2d467a478a3841135478`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.13`

```console
$ docker pull clickhouse@sha256:a60e53915564daf2d5d6fe777422f54f76cef1b595c3c6f195233c4a9f81e4d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.13` - linux; amd64

```console
$ docker pull clickhouse@sha256:1981043d54b910e18f054863ff68b951431b655efd63f967e13a8e268fc70796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206327508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40d95438d3dc6c274458a0f2115075e7b615c1981c516f0d1f59192bacfc055`
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
# Thu, 22 Jan 2026 19:19:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:19:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:19:44 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:19:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:20:09 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:20:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:20:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:20:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4bb92a5a94ca6757c2da82bea4ce7bcead839fd455170531055fd96902`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 7.2 MB (7151352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06899fd4a8fd5b7b0eb7d9404bfbd651d59693dcaeadeb7caa3d94d13ad119e3`  
		Last Modified: Thu, 22 Jan 2026 19:20:32 GMT  
		Size: 168.8 MB (168769240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca408ab305496b7f1a003e523e3b50cbdbcd2bacd10ca12c920ef1bfcadc3a`  
		Last Modified: Thu, 22 Jan 2026 19:20:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a6c62a7877e796f0bdea6facc20e05dafc36076dff282d30a7413332a5704`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f249ea01bc14fe6376f0628bfe11d52074d9da1975e84b01cad4e417d3174b`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b726e025f493d5169e38289db866af96fec79f5663e883dbca9a402a7548e`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca273c02f05ca3a0c6da50d5a566cbac4343526ff4d2282915ef293eb3c41e2f`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:213913a934867686cd8672ebcbb757f5829523469a335319970d47c4f7150638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d04991a8149c6f403a3c2f9dda84887195257ebfe053f44b106c7643a7f19d4`

```dockerfile
```

-	Layers:
	-	`sha256:5fdabf5e465e1ef0ec785ce7c7d270b53668db6dbfafd1586fecfc5fb7daac47`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.13` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7d61db683bccc53989acaaeec4bd0ae332bbadf91fff2c3f5cb20f4b23fcedbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83475229ee9407e31786ad76084e8e3efa29f72bbcd6ca323c1ff2e306e2d348`
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
# Thu, 22 Jan 2026 19:22:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:22:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:22:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:22:17 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:22:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:39:58 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:39:58 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:39:58 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913952d97184f6a9730410d25d2084e15eac92b65adf5d12ba06b05698e92fd9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 7.1 MB (7126669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1052a8a252ec48476e48269fdad77443b10017d930c1b1012b8a16632e994f3`  
		Last Modified: Thu, 22 Jan 2026 19:40:17 GMT  
		Size: 158.4 MB (158419059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ee44031a93f254f5eafc816186c99897c9e95d009ecd0f9ba27312f3c6d0c`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef64c2784db8b10473505cefe99fc5c85d382a13cb92845d4cc01524c571ca9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96fba4fc15ee92ab4c3fcc45463e9a7c87ee42e5bcc3b77515fe4fa9f89b3a`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7841e46b4ba78fb89a19809574ea6bd50185e58221121fdacb339af1bc73826c`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb6a5adf593dd7b1bbeba23d8bf76309efb7423cd0735e2cb65b19bfdf2e22`  
		Last Modified: Thu, 22 Jan 2026 19:40:16 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d53b7a35f3c16d3074227875fc720d4d44dc74a68e8e81ca92ae3c71030206cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f770ed9bb32810eb455181d13d5c22a2b298cf867b83ddc7ce4f8de21dd4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:e362dea85780ffbc23c0507c0598b55b048b1344ba7c2d467a478a3841135478`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.13-jammy`

```console
$ docker pull clickhouse@sha256:a60e53915564daf2d5d6fe777422f54f76cef1b595c3c6f195233c4a9f81e4d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.13-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1981043d54b910e18f054863ff68b951431b655efd63f967e13a8e268fc70796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206327508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40d95438d3dc6c274458a0f2115075e7b615c1981c516f0d1f59192bacfc055`
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
# Thu, 22 Jan 2026 19:19:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:19:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:19:44 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:19:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:20:09 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:20:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:20:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:20:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4bb92a5a94ca6757c2da82bea4ce7bcead839fd455170531055fd96902`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 7.2 MB (7151352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06899fd4a8fd5b7b0eb7d9404bfbd651d59693dcaeadeb7caa3d94d13ad119e3`  
		Last Modified: Thu, 22 Jan 2026 19:20:32 GMT  
		Size: 168.8 MB (168769240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca408ab305496b7f1a003e523e3b50cbdbcd2bacd10ca12c920ef1bfcadc3a`  
		Last Modified: Thu, 22 Jan 2026 19:20:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a6c62a7877e796f0bdea6facc20e05dafc36076dff282d30a7413332a5704`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f249ea01bc14fe6376f0628bfe11d52074d9da1975e84b01cad4e417d3174b`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b726e025f493d5169e38289db866af96fec79f5663e883dbca9a402a7548e`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca273c02f05ca3a0c6da50d5a566cbac4343526ff4d2282915ef293eb3c41e2f`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:213913a934867686cd8672ebcbb757f5829523469a335319970d47c4f7150638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d04991a8149c6f403a3c2f9dda84887195257ebfe053f44b106c7643a7f19d4`

```dockerfile
```

-	Layers:
	-	`sha256:5fdabf5e465e1ef0ec785ce7c7d270b53668db6dbfafd1586fecfc5fb7daac47`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.13-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7d61db683bccc53989acaaeec4bd0ae332bbadf91fff2c3f5cb20f4b23fcedbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83475229ee9407e31786ad76084e8e3efa29f72bbcd6ca323c1ff2e306e2d348`
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
# Thu, 22 Jan 2026 19:22:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:22:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:22:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:22:17 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:22:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:39:58 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:39:58 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:39:58 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913952d97184f6a9730410d25d2084e15eac92b65adf5d12ba06b05698e92fd9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 7.1 MB (7126669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1052a8a252ec48476e48269fdad77443b10017d930c1b1012b8a16632e994f3`  
		Last Modified: Thu, 22 Jan 2026 19:40:17 GMT  
		Size: 158.4 MB (158419059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ee44031a93f254f5eafc816186c99897c9e95d009ecd0f9ba27312f3c6d0c`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef64c2784db8b10473505cefe99fc5c85d382a13cb92845d4cc01524c571ca9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96fba4fc15ee92ab4c3fcc45463e9a7c87ee42e5bcc3b77515fe4fa9f89b3a`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7841e46b4ba78fb89a19809574ea6bd50185e58221121fdacb339af1bc73826c`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb6a5adf593dd7b1bbeba23d8bf76309efb7423cd0735e2cb65b19bfdf2e22`  
		Last Modified: Thu, 22 Jan 2026 19:40:16 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d53b7a35f3c16d3074227875fc720d4d44dc74a68e8e81ca92ae3c71030206cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f770ed9bb32810eb455181d13d5c22a2b298cf867b83ddc7ce4f8de21dd4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:e362dea85780ffbc23c0507c0598b55b048b1344ba7c2d467a478a3841135478`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.13.19`

```console
$ docker pull clickhouse@sha256:a60e53915564daf2d5d6fe777422f54f76cef1b595c3c6f195233c4a9f81e4d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.13.19` - linux; amd64

```console
$ docker pull clickhouse@sha256:1981043d54b910e18f054863ff68b951431b655efd63f967e13a8e268fc70796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206327508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40d95438d3dc6c274458a0f2115075e7b615c1981c516f0d1f59192bacfc055`
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
# Thu, 22 Jan 2026 19:19:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:19:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:19:44 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:19:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:20:09 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:20:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:20:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:20:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4bb92a5a94ca6757c2da82bea4ce7bcead839fd455170531055fd96902`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 7.2 MB (7151352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06899fd4a8fd5b7b0eb7d9404bfbd651d59693dcaeadeb7caa3d94d13ad119e3`  
		Last Modified: Thu, 22 Jan 2026 19:20:32 GMT  
		Size: 168.8 MB (168769240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca408ab305496b7f1a003e523e3b50cbdbcd2bacd10ca12c920ef1bfcadc3a`  
		Last Modified: Thu, 22 Jan 2026 19:20:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a6c62a7877e796f0bdea6facc20e05dafc36076dff282d30a7413332a5704`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f249ea01bc14fe6376f0628bfe11d52074d9da1975e84b01cad4e417d3174b`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b726e025f493d5169e38289db866af96fec79f5663e883dbca9a402a7548e`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca273c02f05ca3a0c6da50d5a566cbac4343526ff4d2282915ef293eb3c41e2f`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13.19` - unknown; unknown

```console
$ docker pull clickhouse@sha256:213913a934867686cd8672ebcbb757f5829523469a335319970d47c4f7150638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d04991a8149c6f403a3c2f9dda84887195257ebfe053f44b106c7643a7f19d4`

```dockerfile
```

-	Layers:
	-	`sha256:5fdabf5e465e1ef0ec785ce7c7d270b53668db6dbfafd1586fecfc5fb7daac47`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.13.19` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7d61db683bccc53989acaaeec4bd0ae332bbadf91fff2c3f5cb20f4b23fcedbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83475229ee9407e31786ad76084e8e3efa29f72bbcd6ca323c1ff2e306e2d348`
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
# Thu, 22 Jan 2026 19:22:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:22:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:22:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:22:17 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:22:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:39:58 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:39:58 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:39:58 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913952d97184f6a9730410d25d2084e15eac92b65adf5d12ba06b05698e92fd9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 7.1 MB (7126669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1052a8a252ec48476e48269fdad77443b10017d930c1b1012b8a16632e994f3`  
		Last Modified: Thu, 22 Jan 2026 19:40:17 GMT  
		Size: 158.4 MB (158419059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ee44031a93f254f5eafc816186c99897c9e95d009ecd0f9ba27312f3c6d0c`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef64c2784db8b10473505cefe99fc5c85d382a13cb92845d4cc01524c571ca9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96fba4fc15ee92ab4c3fcc45463e9a7c87ee42e5bcc3b77515fe4fa9f89b3a`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7841e46b4ba78fb89a19809574ea6bd50185e58221121fdacb339af1bc73826c`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb6a5adf593dd7b1bbeba23d8bf76309efb7423cd0735e2cb65b19bfdf2e22`  
		Last Modified: Thu, 22 Jan 2026 19:40:16 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13.19` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d53b7a35f3c16d3074227875fc720d4d44dc74a68e8e81ca92ae3c71030206cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f770ed9bb32810eb455181d13d5c22a2b298cf867b83ddc7ce4f8de21dd4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:e362dea85780ffbc23c0507c0598b55b048b1344ba7c2d467a478a3841135478`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.13.19-jammy`

```console
$ docker pull clickhouse@sha256:a60e53915564daf2d5d6fe777422f54f76cef1b595c3c6f195233c4a9f81e4d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.13.19-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1981043d54b910e18f054863ff68b951431b655efd63f967e13a8e268fc70796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206327508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40d95438d3dc6c274458a0f2115075e7b615c1981c516f0d1f59192bacfc055`
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
# Thu, 22 Jan 2026 19:19:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:19:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:19:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:19:44 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:19:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:20:09 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:20:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:20:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:20:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:20:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:20:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4bb92a5a94ca6757c2da82bea4ce7bcead839fd455170531055fd96902`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 7.2 MB (7151352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06899fd4a8fd5b7b0eb7d9404bfbd651d59693dcaeadeb7caa3d94d13ad119e3`  
		Last Modified: Thu, 22 Jan 2026 19:20:32 GMT  
		Size: 168.8 MB (168769240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca408ab305496b7f1a003e523e3b50cbdbcd2bacd10ca12c920ef1bfcadc3a`  
		Last Modified: Thu, 22 Jan 2026 19:20:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a6c62a7877e796f0bdea6facc20e05dafc36076dff282d30a7413332a5704`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f249ea01bc14fe6376f0628bfe11d52074d9da1975e84b01cad4e417d3174b`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b726e025f493d5169e38289db866af96fec79f5663e883dbca9a402a7548e`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca273c02f05ca3a0c6da50d5a566cbac4343526ff4d2282915ef293eb3c41e2f`  
		Last Modified: Thu, 22 Jan 2026 19:20:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13.19-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:213913a934867686cd8672ebcbb757f5829523469a335319970d47c4f7150638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d04991a8149c6f403a3c2f9dda84887195257ebfe053f44b106c7643a7f19d4`

```dockerfile
```

-	Layers:
	-	`sha256:5fdabf5e465e1ef0ec785ce7c7d270b53668db6dbfafd1586fecfc5fb7daac47`  
		Last Modified: Thu, 22 Jan 2026 19:20:28 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.13.19-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7d61db683bccc53989acaaeec4bd0ae332bbadf91fff2c3f5cb20f4b23fcedbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83475229ee9407e31786ad76084e8e3efa29f72bbcd6ca323c1ff2e306e2d348`
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
# Thu, 22 Jan 2026 19:22:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:22:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:22:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:22:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:22:17 GMT
ARG VERSION=25.3.13.19
# Thu, 22 Jan 2026 19:22:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:39:58 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:39:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.13.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:39:58 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:39:58 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:39:58 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913952d97184f6a9730410d25d2084e15eac92b65adf5d12ba06b05698e92fd9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 7.1 MB (7126669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1052a8a252ec48476e48269fdad77443b10017d930c1b1012b8a16632e994f3`  
		Last Modified: Thu, 22 Jan 2026 19:40:17 GMT  
		Size: 158.4 MB (158419059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ee44031a93f254f5eafc816186c99897c9e95d009ecd0f9ba27312f3c6d0c`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef64c2784db8b10473505cefe99fc5c85d382a13cb92845d4cc01524c571ca9`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96fba4fc15ee92ab4c3fcc45463e9a7c87ee42e5bcc3b77515fe4fa9f89b3a`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7841e46b4ba78fb89a19809574ea6bd50185e58221121fdacb339af1bc73826c`  
		Last Modified: Thu, 22 Jan 2026 19:40:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb6a5adf593dd7b1bbeba23d8bf76309efb7423cd0735e2cb65b19bfdf2e22`  
		Last Modified: Thu, 22 Jan 2026 19:40:16 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.13.19-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d53b7a35f3c16d3074227875fc720d4d44dc74a68e8e81ca92ae3c71030206cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f770ed9bb32810eb455181d13d5c22a2b298cf867b83ddc7ce4f8de21dd4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:e362dea85780ffbc23c0507c0598b55b048b1344ba7c2d467a478a3841135478`  
		Last Modified: Thu, 22 Jan 2026 19:40:14 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.15`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.15` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.15` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.15-jammy`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.15-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.15-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.15.35`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.15.35` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.15.35` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.15.35-jammy`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.15.35-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.15.35-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.15.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

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

### `clickhouse:26.1` - unknown; unknown

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

### `clickhouse:26.1` - linux; arm64 variant v8

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

### `clickhouse:26.1` - unknown; unknown

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

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

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

### `clickhouse:26.1-jammy` - unknown; unknown

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

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

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

### `clickhouse:26.1-jammy` - unknown; unknown

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

## `clickhouse:26.1.1`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.1` - linux; amd64

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

### `clickhouse:26.1.1` - unknown; unknown

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

### `clickhouse:26.1.1` - linux; arm64 variant v8

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

### `clickhouse:26.1.1` - unknown; unknown

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

## `clickhouse:26.1.1-jammy`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.1-jammy` - linux; amd64

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

### `clickhouse:26.1.1-jammy` - unknown; unknown

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

### `clickhouse:26.1.1-jammy` - linux; arm64 variant v8

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

### `clickhouse:26.1.1-jammy` - unknown; unknown

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

## `clickhouse:26.1.1.912`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.1.912` - linux; amd64

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

### `clickhouse:26.1.1.912` - unknown; unknown

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

### `clickhouse:26.1.1.912` - linux; arm64 variant v8

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

### `clickhouse:26.1.1.912` - unknown; unknown

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

## `clickhouse:26.1.1.912-jammy`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.1.912-jammy` - linux; amd64

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

### `clickhouse:26.1.1.912-jammy` - unknown; unknown

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

### `clickhouse:26.1.1.912-jammy` - linux; arm64 variant v8

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

### `clickhouse:26.1.1.912-jammy` - unknown; unknown

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

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:f5a085dd7d06cbb15f81bdfeeb9f044b4596ce9b4612604cf152a737778f572c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

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

### `clickhouse:latest` - unknown; unknown

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

### `clickhouse:latest` - linux; arm64 variant v8

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

### `clickhouse:latest` - unknown; unknown

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

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:cddd46a555434db583d7633061fba45d3db1ac4e56f1f606b73ede531b2aa26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:18fdb9d2a3f9cf200d588299e4060900d7bcfbd5280041c029df7fe1a08d9a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53d460b357c9ed096eeb2a29bc2bc2f2764072b26aa3ed06e7a6b0986210de`
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
# Thu, 22 Jan 2026 19:17:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:17:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:17:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:17:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:17:36 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:17:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:19:07 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:19:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:19:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:19:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:19:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:19:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e90366a3a72204c616d28f81691c678a2ddcb774eb8818100c4434ded8972`  
		Last Modified: Thu, 22 Jan 2026 19:18:25 GMT  
		Size: 7.6 MB (7598265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e527cd3965498f62ca7b20df699ddd1b558427ccf0e39842c5b8205282812`  
		Last Modified: Thu, 22 Jan 2026 19:19:29 GMT  
		Size: 190.9 MB (190924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f1b1bb612f53b1ff3a60d6f2d83b7ecd218487bc7038dce4f67763fe8b9f9`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2d7d28c90b6382ad31b6995f369298e870dca4e479e4f74014eb3a0f6a1441`  
		Last Modified: Thu, 22 Jan 2026 19:19:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd743629654b484049eaf427f45d7752189516520db7dfca25df7f71aa80c2f`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbefbe2b7aa6e28fbf0427d482253e9f13376bf3a6b7408737d41963654dfe`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151572ce83eee80745028c316e7bfd7d9bbd51584071f0f9c032e973cd4c02f`  
		Last Modified: Thu, 22 Jan 2026 19:19:27 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a7ad1cbeb829571d8fd8d041a7db4ff084b5ba9dd53bbe835f019efa2b681852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad64f6669f754df4c84a0438dc444dda6d40c2e87f09526ed799cf05450e833`

```dockerfile
```

-	Layers:
	-	`sha256:68aa4e433704e3efc2e91aac00f373960aac389405575464f7cd34ef47b7710a`  
		Last Modified: Thu, 22 Jan 2026 19:19:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4fa00800c9fccc82a8c9b3128e87f0f3f2cfa4959adb3850014c4edab2586f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213834730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85bf75f877e2953b8c46aa95b4267d58ddfed384e9ec2f3d51013165c421c9d`
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
# Thu, 22 Jan 2026 19:21:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 22 Jan 2026 19:21:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 22 Jan 2026 19:21:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 22 Jan 2026 19:21:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 22 Jan 2026 19:21:44 GMT
ARG VERSION=25.8.15.35
# Thu, 22 Jan 2026 19:21:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Jan 2026 19:22:13 GMT
ENV TZ=UTC
# Thu, 22 Jan 2026 19:22:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.15.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 22 Jan 2026 19:22:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 22 Jan 2026 19:22:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 22 Jan 2026 19:22:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 22 Jan 2026 19:22:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920d072f1c3d2585f23fcbb001b61fa9bc21d5e933d91f1573edbb0f398e9e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 7.6 MB (7576398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d87f2c0f2e5d3fb2c99f91f1c3c321e6f8505d70e2330024e026f3516dc275`  
		Last Modified: Thu, 22 Jan 2026 19:22:36 GMT  
		Size: 178.0 MB (178004806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75adbc347a32c9d90ac16532400f9a30dacaf6ecaf860099fa0345c9f52a4c4`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5ae28111675c03b02b5ac4182221e9d4dea2f2971f47f3912ac265eb8da50`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b09653a96c00b88d633e53030568c5030902e8c0c4e87991b40a193bfbb4e5`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b56bb6f4d5e81933acfac98ee50b1035b7af13c4d2327e09fa5ef5278562f`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62702d63d4830b34c0df1a596e3a2da51912819216c0ae4d2044eacb2b4a9910`  
		Last Modified: Thu, 22 Jan 2026 19:22:33 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f2d2fdf753452563fcac1a8da8f812f376866cad7fd5084d099c03ebd78c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97f3d681ad8ae72dca45d2f7bf23cdb837c8e657f6301c27b97a4f430e801e`

```dockerfile
```

-	Layers:
	-	`sha256:fcca0f6e488dab24c1d9051bb4cd4f67fd9d5e0c534a435aed347895980a1579`  
		Last Modified: Thu, 22 Jan 2026 19:22:32 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
