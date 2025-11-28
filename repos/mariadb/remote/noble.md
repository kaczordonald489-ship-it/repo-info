## `mariadb:noble`

```console
$ docker pull mariadb@sha256:e1bcd6f85781f4a875abefb11c4166c1d79e4237c23de597bf0df81fec225b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:noble` - linux; amd64

```console
$ docker pull mariadb@sha256:a78483ea9488eefdc32af4d4dcf116748df0bc0cdea583815e51438d8fa4d9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106648020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90bc2981a9328d1cf99f733a5c355a5cc869d78f10eea1932cf99d80328ff86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

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
# Fri, 21 Nov 2025 01:11:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 21 Nov 2025 01:11:17 GMT
ENV GOSU_VERSION=1.19
# Fri, 21 Nov 2025 01:11:17 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Nov 2025 01:11:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Nov 2025 01:11:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Nov 2025 01:11:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Nov 2025 01:11:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 21 Nov 2025 01:11:17 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:11:17 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:11:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Fri, 21 Nov 2025 01:11:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 21 Nov 2025 01:11:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 21 Nov 2025 01:11:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Nov 2025 01:11:31 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 21 Nov 2025 01:11:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 01:11:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:31 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 21 Nov 2025 01:11:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e5c9f5eeb03eec310a871b4a011ab69bb5460d436f74e56a12cbf31025cb77`  
		Last Modified: Fri, 21 Nov 2025 01:11:55 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5b64c3e2f53accc17846bc88be312950a7af08c6f3f13b41e9675305336765`  
		Last Modified: Fri, 21 Nov 2025 01:11:56 GMT  
		Size: 5.3 MB (5287954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d27f4ceca7b8672c36803e4e515e04310c79494d14bc6e65e7235848f6099`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be15142d46ec89bedc51d3a565d1eeab1589a1ec22a683ad2d400be277a6da4`  
		Last Modified: Fri, 21 Nov 2025 01:11:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9047f410cb7de3e4efb461505d0fe627f99ee84efd8e97632415378d61dafab4`  
		Last Modified: Fri, 21 Nov 2025 01:12:08 GMT  
		Size: 71.6 MB (71621142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be922ac1f9ed43d64943d064c6d24b2d6b2fdfb63822a4e98591c5964cf93142`  
		Last Modified: Fri, 21 Nov 2025 01:11:55 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7ec75082e1584a18af1f5a3aed6ac4691220d469eb6eb77043032bcc09727`  
		Last Modified: Fri, 21 Nov 2025 01:11:55 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:e813ad31cc3f7111cf48d2605138ce4c8cb7d857c9495175db55d86b05c8be25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49881be0a434c358c8b04addd9361e9a8a0070a0a0a457f96647c0ea934a2416`

```dockerfile
```

-	Layers:
	-	`sha256:c2fd0cca54b4a8dc359e4e8c9b1c8f001f6101e8e59d64468b02fbdd48091ff4`  
		Last Modified: Fri, 21 Nov 2025 04:36:00 GMT  
		Size: 4.3 MB (4273707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0711efb1517f160aad72335c52d68069ef760c34c7d7e78699f89e43f3b5ab51`  
		Last Modified: Fri, 21 Nov 2025 04:36:00 GMT  
		Size: 31.4 KB (31441 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4517695230939c408f44d4cf809e588cbc16650e961103ec43f64cfebd94ed79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104565662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e31931ca21a30d0cf521f25c7c8e97698b37390b94f29fe71bb756e16b6aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

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
# Fri, 21 Nov 2025 01:12:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 21 Nov 2025 01:13:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 21 Nov 2025 01:13:05 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Nov 2025 01:13:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Nov 2025 01:13:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Nov 2025 01:13:05 GMT
ENV LANG=C.UTF-8
# Fri, 21 Nov 2025 01:13:05 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 21 Nov 2025 01:13:05 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:13:05 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:13:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Fri, 21 Nov 2025 01:13:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 21 Nov 2025 01:13:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 21 Nov 2025 01:13:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Nov 2025 01:13:23 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 21 Nov 2025 01:13:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 01:13:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 01:13:23 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 21 Nov 2025 01:13:23 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2610e955554f32d78523d27261bd4b8250216ffe316dc42e1d41e5c6ea4b349b`  
		Last Modified: Fri, 21 Nov 2025 01:13:48 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd01e102ea2f2f9dfb0f22e02a3e8aadc119f9382d51e17f247bc2b2281229f`  
		Last Modified: Fri, 21 Nov 2025 01:13:48 GMT  
		Size: 5.1 MB (5097419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09415ff6de4b8443d19fac55e1a51919eb2ac40e727d71e1dc241f5572cf3cf0`  
		Last Modified: Fri, 21 Nov 2025 01:13:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d233c2cd908cf3a05e81d0de553076ed339c3b97b0836015778576c5ec56c1b6`  
		Last Modified: Fri, 21 Nov 2025 01:13:49 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f35781d43ad85cf1757ed0261de64ea361b6d2b5103666716745f4bc605552`  
		Last Modified: Fri, 21 Nov 2025 01:14:02 GMT  
		Size: 70.6 MB (70592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b082f83a55a7022c4a013f913240518db196ab9074b8b58466b0c83787b7f90`  
		Last Modified: Fri, 21 Nov 2025 01:13:49 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75946ccbd2ca8de7821aae8bc02266c7918090e9df60aa99f0061810dad770`  
		Last Modified: Fri, 21 Nov 2025 01:13:50 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:dba36025ce4214d8af34426ce6f814ffb3a7ad36a22f042c97d3e6ef5568e8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf9fb70219de3f0ec2b6fd3517322b53835a66a2ef4a06ec7cdd26ef3364c87`

```dockerfile
```

-	Layers:
	-	`sha256:b345b46be9532c8031b31b4e862f6eda2607b287345cdc86ff514b0ca46c2369`  
		Last Modified: Fri, 21 Nov 2025 04:36:05 GMT  
		Size: 4.3 MB (4280984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f723ee14d292ecb21db0cae47ad8989a7efe7b475754d968bbd3391e0b8a7a`  
		Last Modified: Fri, 21 Nov 2025 04:36:06 GMT  
		Size: 31.7 KB (31653 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ab8b94c5e87ec2b1be693ba1d56e7747ef22da59b4c85cb4a013fa7dc738e186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116862618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba0c5d370851dd96b30dcd3d94fd371b260d1c7bc3d730a0e53b99de8e1dce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:13:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 21 Nov 2025 01:14:33 GMT
ENV GOSU_VERSION=1.19
# Fri, 21 Nov 2025 01:14:33 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Nov 2025 01:14:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Nov 2025 01:14:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Nov 2025 01:14:34 GMT
ENV LANG=C.UTF-8
# Fri, 21 Nov 2025 01:14:34 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 21 Nov 2025 01:14:34 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:14:34 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:14:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Fri, 21 Nov 2025 01:14:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 21 Nov 2025 01:15:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 21 Nov 2025 01:15:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Nov 2025 01:15:46 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 21 Nov 2025 01:15:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 01:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 01:15:47 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 21 Nov 2025 01:15:47 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfd8f64b1259195ebc7abdc03492523daa9d1c399af1ebd2476e8fece1babc4`  
		Last Modified: Fri, 21 Nov 2025 01:16:32 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2836e304b7b9afae4efc6d4f3ec295acafe8ee03f8ae0685202a32803c432db7`  
		Last Modified: Fri, 21 Nov 2025 01:16:32 GMT  
		Size: 5.9 MB (5927295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6adc928b016eaacca0b7a9f0defe5ccb5f5c245e4d8fa1872a6730d575c680`  
		Last Modified: Fri, 21 Nov 2025 01:16:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c4f0514f19c22a75610acba74063d8da266c7c91df4afb4b3a768611f87b7b`  
		Last Modified: Fri, 21 Nov 2025 01:16:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95851fcbfd0329990a22333e2be72108e60b91e4c2c5c87db43d142952c261c7`  
		Last Modified: Fri, 21 Nov 2025 01:16:39 GMT  
		Size: 76.6 MB (76616656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97235b6097a3b5f8f9801591b778ecb054d72f0e5a2068ee0b2172f734685795`  
		Last Modified: Fri, 21 Nov 2025 01:16:32 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14c707add2c28ddc29d2c60e3c55903deb7ba9045147e8d1011a839d48a7792`  
		Last Modified: Fri, 21 Nov 2025 01:16:32 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:83a8f357cc368654502d6e68c6cce2cc7587a01ac5ea0c0ecd767bcf8682689a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f456941bca37a6dcbeb03227905e967f58d9f6c710f28ec761cf9c3385dc739f`

```dockerfile
```

-	Layers:
	-	`sha256:f26074949645cc9932e15bf8cdff8ae4ab396b0902cd012ef038fd6ae7521555`  
		Last Modified: Fri, 21 Nov 2025 04:36:11 GMT  
		Size: 4.3 MB (4281642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88c9a638aa90260e5b49834ad64f3637c42aa4a4cdce86ba174013df019c485`  
		Last Modified: Fri, 21 Nov 2025 04:36:12 GMT  
		Size: 31.5 KB (31517 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:47573e985618cff1ac5f7c2d328e6e26b6dbe5199beb740590104a58529c2ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112054935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d90bfbf3c6c17022fd66a50bf4063a908f37c409fa80198b40816bf06373de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 21 Nov 2025 01:11:14 GMT
ENV GOSU_VERSION=1.19
# Fri, 21 Nov 2025 01:11:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Nov 2025 01:11:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Nov 2025 01:11:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Nov 2025 01:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Nov 2025 01:11:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 21 Nov 2025 01:11:14 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:11:14 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Fri, 21 Nov 2025 01:11:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Fri, 21 Nov 2025 01:11:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 21 Nov 2025 01:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 21 Nov 2025 01:11:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Nov 2025 01:11:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 21 Nov 2025 01:11:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 01:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:42 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 21 Nov 2025 01:11:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b58d8ccd9ab349311f8e6906c8d7ef7c476692a4f07d86f8b6d329d7f552221`  
		Last Modified: Fri, 21 Nov 2025 01:12:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecd1ff2fedb3cdf9ff9ee5a857c3c58c2b434c18c94b490a93b2a816435dca2`  
		Last Modified: Fri, 21 Nov 2025 01:12:13 GMT  
		Size: 5.4 MB (5443771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298a0500e4fcc79489ecf7170a1099375813e82d3454b5ebaf3d931227e3582b`  
		Last Modified: Fri, 21 Nov 2025 01:12:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34078458963bd3a03896b0c0c86ea843e672f6060ddcc33f1b01dc14240d9d1`  
		Last Modified: Fri, 21 Nov 2025 01:12:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae7719e2bbe9a37fc43158241e842f9cf2ad6336d8099d25e25e5b65f854777`  
		Last Modified: Fri, 21 Nov 2025 01:12:19 GMT  
		Size: 76.7 MB (76689336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dcbcee1eac544c0c5fe5a23acc60f9730da02fab753f1866edd74458915c8d`  
		Last Modified: Fri, 21 Nov 2025 01:12:12 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fbd11d1c5915068c84baee92806c5b0d32b6d421fd20ad451a0c1d993053f5`  
		Last Modified: Fri, 21 Nov 2025 01:12:12 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:752bf377fb0e6e1a9331e2a206e24604ea0d4d39fc80dd67d5018f1220b2bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce219f137710808e71909250c328f8e5bb068d1f22ea8777098b5ce05424eb7`

```dockerfile
```

-	Layers:
	-	`sha256:6d81da919569fe427f8e0172e0b1dc28b07fd688355415d1adceda0eac85a06d`  
		Last Modified: Fri, 21 Nov 2025 04:36:16 GMT  
		Size: 4.3 MB (4275426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80efb535444bfd1465beb73d25fe407d011ea576219014eba50f1fe7672f9a75`  
		Last Modified: Fri, 21 Nov 2025 04:36:16 GMT  
		Size: 31.4 KB (31441 bytes)  
		MIME: application/vnd.in-toto+json
