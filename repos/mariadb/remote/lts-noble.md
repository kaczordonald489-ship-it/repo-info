## `mariadb:lts-noble`

```console
$ docker pull mariadb@sha256:345fa26d595e8c7fe298e0c4098ed400356f502458769c8902229b3437d6da2b
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

### `mariadb:lts-noble` - linux; amd64

```console
$ docker pull mariadb@sha256:3a730f41f00d261df28a0bc1bc2845f9c0901c2e2f05e5005c7713cc43ebc1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106223914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe9184ea9e5b839e6b01d279a2e508a3bb50e66c843dfd2183dd7608550ce78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 15 Jan 2026 22:32:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:32:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Jan 2026 22:32:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:32:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:32:08 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Jan 2026 22:32:08 GMT
ARG MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:32:08 GMT
ENV MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:32:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
# Thu, 15 Jan 2026 22:32:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Jan 2026 22:32:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Jan 2026 22:32:25 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Jan 2026 22:32:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Jan 2026 22:32:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:32:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:25 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Jan 2026 22:32:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65ab3e2dcc1933ea941e8f9523725895c6059c18badc1d3b9b883a0666876ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:38 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f312e18ee72622c657a79e436fbcfa3ce37d5eff08eb2dc32be7a37c0d84b436`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 5.3 MB (5288143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384e37c86ba3130a59650ee07aaf1ce489c39be5a500d5ecb655584623e0cf72`  
		Last Modified: Thu, 15 Jan 2026 22:32:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be27e7736be39e6412cd9c08c2ca81ec250b9cf0e890a56c2ce37878a19c8ddb`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b21bfaefe54d49f82c48cd6febb140b6c5269f4aa4ac55cedf0198f5a6e26a0`  
		Last Modified: Thu, 15 Jan 2026 22:32:42 GMT  
		Size: 71.2 MB (71195543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b51c2a7153a1e86fae47d2f988f74877e4044c3fa1420e6b0ea35caa986afd`  
		Last Modified: Thu, 15 Jan 2026 22:32:40 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ebe459a5d6a4cec7c90b073ab262900f8d3270c799653a5a1a2bc510ddb681`  
		Last Modified: Thu, 15 Jan 2026 22:32:40 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:da5be05183e2762363fe8a4b1ff74ca515e647064d444ba1ea0f68862091a029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe62e6f4ddb57f5810c8b5e948a37e81d7abe42a8b2c529176fde461610a88a`

```dockerfile
```

-	Layers:
	-	`sha256:83295d7ba0d2103f77a125dc265bc2d21d060730160f71598e03cb6385f1afac`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 4.3 MB (4273709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9613981426dc640f1fcbdbac99542d4ffdf9af5b1dcc22de6d160d86bfa8f4b5`  
		Last Modified: Thu, 15 Jan 2026 22:32:38 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4ab5d5e770624a5fcaa5894208576ed5088f12482c1cce9b3ab419416a4b2c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104124201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7b7bb245ed181636c97ceda8fcd8cba6c3e27776b9784c0e3141f8a4a88914`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 15 Jan 2026 22:34:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:34:38 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Jan 2026 22:34:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:34:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:34:38 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:34:38 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Jan 2026 22:34:38 GMT
ARG MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:34:38 GMT
ENV MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:34:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
# Thu, 15 Jan 2026 22:34:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Jan 2026 22:34:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Jan 2026 22:34:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Jan 2026 22:34:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Jan 2026 22:34:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:34:54 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Jan 2026 22:34:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf6635c88c956d5039bb73e0cc136997c739b73e1ab6ddcd0fafd21a246c4d`  
		Last Modified: Thu, 15 Jan 2026 22:35:08 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45e1af23cb59bbff4b2cee371a53ba426c10a5079922f5ab0117eebc6d72541`  
		Last Modified: Thu, 15 Jan 2026 22:35:08 GMT  
		Size: 5.1 MB (5098447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74fab870fd19fc26c3c9c3d32e599ecbb0bdc9702bff76f3af4777be64e6be1`  
		Last Modified: Thu, 15 Jan 2026 22:35:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e8ea3b220da87014a6c2c8c3196a9242d15cc56dc21f3820c3d7e95e8bcda5`  
		Last Modified: Thu, 15 Jan 2026 22:35:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1ca954da259477333ac2e0db431f2a8f6304e7275d4a2d95ee2059032cfc9c`  
		Last Modified: Thu, 15 Jan 2026 22:35:11 GMT  
		Size: 70.1 MB (70147710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0382d1ebe07b7088dd18fce4bb9ac63465b6cf7ea273419779adb2f4df283e`  
		Last Modified: Thu, 15 Jan 2026 22:35:09 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a16fb73c5ed9dee4ddac618ca75ea4bbfc13a2d0aaa5e1c148169c19b6bc50`  
		Last Modified: Thu, 15 Jan 2026 22:35:09 GMT  
		Size: 8.4 KB (8396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:451831d3d60ed99a898483ad1fef366985950bd3db6413879645e1f0812afdf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185aae96b6413441981013c0a52a0f12b3adfab8fab8b213ab6d908dfa93912`

```dockerfile
```

-	Layers:
	-	`sha256:7a3d87653833620e4aeb254ddee9662bf82ccd6907571e84b228ec5599ac09bb`  
		Last Modified: Thu, 15 Jan 2026 22:35:08 GMT  
		Size: 4.3 MB (4280986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01697c071ac9479b14f45a555c222d31553cb58e701382501fdf58fc7d039bf4`  
		Last Modified: Thu, 15 Jan 2026 22:35:08 GMT  
		Size: 31.7 KB (31667 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4c7bcd54df8e91281fc1ca16a81d8fc327cbcc1fdd7eb9262d9d08e9bfa41617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116406343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f7274371f424071ec6de2ffdfda1dc154c584e19941788bc4f551f26ad463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:49:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 15 Jan 2026 22:50:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:50:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Jan 2026 22:50:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:50:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:50:28 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:50:28 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Jan 2026 22:50:28 GMT
ARG MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:50:28 GMT
ENV MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:50:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
# Thu, 15 Jan 2026 22:52:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Jan 2026 22:53:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Jan 2026 22:53:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Jan 2026 22:53:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Jan 2026 22:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:53:10 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Jan 2026 22:53:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671242a7c04eafefdc4be3d392ec3dfc9fc4f4349c6b625e350257d5bf121c96`  
		Last Modified: Thu, 15 Jan 2026 22:51:59 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fcb440c1d876fbbd07566ae203e85eb55b3224e714f71ea6178051ba4e460a`  
		Last Modified: Thu, 15 Jan 2026 22:52:00 GMT  
		Size: 5.9 MB (5927566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5644ae594264dbac557062c1464031af87a4a7888132d618fecaaca3789c8e1`  
		Last Modified: Thu, 15 Jan 2026 22:52:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcfa4c3364cd38fc94e0ddcc166a768c4b0b0122fa50af8e54bc73933db41ec`  
		Last Modified: Thu, 15 Jan 2026 22:53:52 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd17926f632e6a9b0f3a24e61de76dfa1856416ba81bac8df585b5a3be8b38a`  
		Last Modified: Thu, 15 Jan 2026 22:53:55 GMT  
		Size: 76.2 MB (76158382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a65f9144938e39e5979f3297b626d66f4538f399a30f081290854a38c58341`  
		Last Modified: Thu, 15 Jan 2026 22:53:52 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed089a17cb15c70344f95827febd9b9b4e2005e4313716dbf0b433933ce1957`  
		Last Modified: Thu, 15 Jan 2026 22:53:52 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:ac06393e5d6f096fa5c92983d3b6c5bb01faac994bb3c4f94ae6f117576654af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aab69cf7234ea265d1d6d8e8862b31b6a54b0c96b2d8ff8bf8d60f4fc725d0`

```dockerfile
```

-	Layers:
	-	`sha256:ac11c0cd0500656e225498a6f1bf454628a0a3ac024d4b95369b6cf54c771dab`  
		Last Modified: Thu, 15 Jan 2026 22:53:53 GMT  
		Size: 4.3 MB (4281644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d61158419f9d9c383830c81291f2ce0423cf2ebb2932e4fd248748e6f2fba6e`  
		Last Modified: Thu, 15 Jan 2026 22:53:52 GMT  
		Size: 31.5 KB (31531 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:5962c1371daf877b4131403b9d4c27aaff52702867b0fb1f483d6be488dfd2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111612604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a1ee9035aa42a5c051e7ccd7be74b35e1f535a28db3821993eb881da690dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 15 Jan 2026 22:20:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:20:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Jan 2026 22:20:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:20:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:20:58 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:20:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Jan 2026 22:20:58 GMT
ARG MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:20:58 GMT
ENV MARIADB_VERSION=1:11.8.5+maria~ubu2404
# Thu, 15 Jan 2026 22:20:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
# Thu, 15 Jan 2026 22:20:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Jan 2026 22:21:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Jan 2026 22:21:11 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Jan 2026 22:21:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Jan 2026 22:21:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:21:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:21:12 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Jan 2026 22:21:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574d386fc69355723d0a8d614a2be6254510043f12a63f54774376bacdd3cda`  
		Last Modified: Thu, 15 Jan 2026 22:21:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9031bacb8bfd231b1b289670d2b66822f3b591b132cd3c6180b6e239b875da93`  
		Last Modified: Thu, 15 Jan 2026 22:21:35 GMT  
		Size: 5.4 MB (5443625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d33453161112250b0987aff5151793a87a77ce591bbbd11a1c5682c7ed96c0`  
		Last Modified: Thu, 15 Jan 2026 22:21:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d12ef445ef40421b8804e687b1018d2f88bba3a40a239c63aa55d29db2c02`  
		Last Modified: Thu, 15 Jan 2026 22:21:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bcb944ea1c47a037e199824bfb9dcb3dd72e6a8254c29b00ffbb8824a175e3`  
		Last Modified: Thu, 15 Jan 2026 22:21:37 GMT  
		Size: 76.2 MB (76245550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e361c82e723b1881f4943d494f3ce39183201f7d57b375ac850d8ab9d37fb1b`  
		Last Modified: Thu, 15 Jan 2026 22:21:36 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed792459c73d968b23c5df26dd928ca14f35bb37160c499bd43e3c61e76a236`  
		Last Modified: Thu, 15 Jan 2026 22:21:36 GMT  
		Size: 8.4 KB (8396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:ad3a1b5dfd464abd40feb916428ee050abb76738c94efd1faee88f2af8858b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b338542b759d59a28ed4dca2cbd4b73fbe5acacbaa3d66cfbf4ec4743253f5`

```dockerfile
```

-	Layers:
	-	`sha256:61b2aa71d93630acd1913f67ca555c2e038ba4f947528d3b1a0e8dec755ed827`  
		Last Modified: Thu, 15 Jan 2026 22:21:35 GMT  
		Size: 4.3 MB (4275428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd9d02be1f9337eda8cd36c0303205768c6661d5b8b19ad4299d40c013cf2ce`  
		Last Modified: Thu, 15 Jan 2026 22:21:35 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json
