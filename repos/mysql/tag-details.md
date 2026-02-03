<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bookworm`](#mysql80-bookworm)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux9`](#mysql80-oraclelinux9)
-	[`mysql:8.0.45`](#mysql8045)
-	[`mysql:8.0.45-bookworm`](#mysql8045-bookworm)
-	[`mysql:8.0.45-debian`](#mysql8045-debian)
-	[`mysql:8.0.45-oracle`](#mysql8045-oracle)
-	[`mysql:8.0.45-oraclelinux9`](#mysql8045-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.8`](#mysql848)
-	[`mysql:8.4.8-oracle`](#mysql848-oracle)
-	[`mysql:8.4.8-oraclelinux9`](#mysql848-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.6`](#mysql96)
-	[`mysql:9.6-oracle`](#mysql96-oracle)
-	[`mysql:9.6-oraclelinux9`](#mysql96-oraclelinux9)
-	[`mysql:9.6.0`](#mysql960)
-	[`mysql:9.6.0-oracle`](#mysql960-oracle)
-	[`mysql:9.6.0-oraclelinux9`](#mysql960-oraclelinux9)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux9`](#mysqlinnovation-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:9c7897818a32cb639b0404fadd828c7cbc522da90398107fbae55682aee577c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:8fd817c666f6913194a2c24946e2a525ab514fd47036532b10e3ae62fdccf7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232311053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fcbe35dfe84111133d8ba560a86aec393db4353b85217bccdbdbe3b328ad6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:45 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:12:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:13:07 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:13:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:13:07 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:13:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bba75f9c491c56e71e9cabdf6b194c7006c9d07385e525909c43563aedd021`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7842cc7478272f46c7b84fc61ee1d74e97132522fc6954e05b6b3b3e09e922a`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1944d72bca6dde4d32cc82b406d5dfd1d8e80d54fb65aef206f039abaf1d0e`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 6.2 MB (6175266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ebd7bbdedabb4111bd5bf3030c9d3044f6987ebda89fcf261364f3f49b605`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142c5fc9ea8a2d7156d977b33918b7b695a363201df60b979f8dcf80c95bedb3`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526dbe6f3591e92ef805b1b368f3ded7965b3c9ad699dd234814bc49e66e88aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:39 GMT  
		Size: 49.9 MB (49925465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b17de9630a006e5f9b21d95b0ba31a12dafe3510181c5fc326d91bcd69ddc`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145e04eb4706e5de6fdd3e0f3c9e546ef09acc3c50c6555f6631ae12c571d96`  
		Last Modified: Sat, 31 Jan 2026 00:13:40 GMT  
		Size: 128.1 MB (128103362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b7cf07833ee8819b666ebeb43b60b17f803c6d68a8f8a2ae49b0757473f46`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9f94601d6afe3d556624c05ea55b67ecc816be8728fa89634a2cadbba6218`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f9f73d16d4ba6a3449bd80183248de57fa72a95a292c86278d0b38d1c4e264db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be41fd1b58eb3064579cd4a08590f7732299ea4dcf11f3c130aae54ca42fcb49`

```dockerfile
```

-	Layers:
	-	`sha256:16a042b28046084f3dbe4ed69e68d5de675b9354491c6d81ac724cd764f6db0c`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d6a1e96dc0d07de9205c61cb37b077766078c798eaccadd69487112a2462f`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5ba616da907066423733e48e6334614d763267d5550cfcd081719e5cf82423df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fbc459d67ca93ec8867b9e6893ad776e178b57a6b0e6f2de1b24c1dedd54e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:10 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b89f520a88cf19dae316a4923b664b7e6bf95c3315e6d141fb757349d3e8a`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803e42c69cf3e606e27ca4a06da2435d4ea059a03cc5856cd6f50b37c3382595`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c14e296756ac06a1560de0a58b510f0b080c8cb05113b2aa3d2eaa03c83fc`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 5.8 MB (5791496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70cc2884f7e43f795b60e342e686802e72d0a5f8586bbec349943626ae98e39`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4609b660cfe4aef6e68410e3b40ab7efe4f35560ad7c855ec911a9e5fe28d5d`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ba81b42a2aa9e7a7a44386fefea991308a713531590f8dbf54305dca317874`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 48.8 MB (48777660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ee5a103ec0a7d4c8c41713b03fe52b67fd6265fa77e023c7b54ade27f6111`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457891cd44ec3897c6bddbd3934cc988aa57b4d42ec8990f1cac5c8dd98ffa4`  
		Last Modified: Sat, 31 Jan 2026 00:13:23 GMT  
		Size: 126.7 MB (126681626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7015cb85f5f43fe858846b8f8e8359c24c3827d30f9da438dbfee91cafd71`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19c4a82a368d5fd463df226d9961021f91237e84f338104e050377e2eb45b17`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d22c90075d7dae6d423e1e9f4e916c29a8ab682d7b88d81b12c5b4d7c3d8187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45439e0f5020f7dbe2617512deb8c471592a4128ddcce5ef3beb1f3003d7d603`

```dockerfile
```

-	Layers:
	-	`sha256:451653891a1ef001567b90b98ad6dc519aedc1d1480b274d56bf4901d08fe095`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a3c6ac4004261be493ee6b3e7a3871a796b4a8f4fa91b7b90e95796f99e5cf`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:9c7897818a32cb639b0404fadd828c7cbc522da90398107fbae55682aee577c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8fd817c666f6913194a2c24946e2a525ab514fd47036532b10e3ae62fdccf7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232311053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fcbe35dfe84111133d8ba560a86aec393db4353b85217bccdbdbe3b328ad6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:45 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:12:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:13:07 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:13:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:13:07 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:13:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bba75f9c491c56e71e9cabdf6b194c7006c9d07385e525909c43563aedd021`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7842cc7478272f46c7b84fc61ee1d74e97132522fc6954e05b6b3b3e09e922a`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1944d72bca6dde4d32cc82b406d5dfd1d8e80d54fb65aef206f039abaf1d0e`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 6.2 MB (6175266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ebd7bbdedabb4111bd5bf3030c9d3044f6987ebda89fcf261364f3f49b605`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142c5fc9ea8a2d7156d977b33918b7b695a363201df60b979f8dcf80c95bedb3`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526dbe6f3591e92ef805b1b368f3ded7965b3c9ad699dd234814bc49e66e88aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:39 GMT  
		Size: 49.9 MB (49925465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b17de9630a006e5f9b21d95b0ba31a12dafe3510181c5fc326d91bcd69ddc`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145e04eb4706e5de6fdd3e0f3c9e546ef09acc3c50c6555f6631ae12c571d96`  
		Last Modified: Sat, 31 Jan 2026 00:13:40 GMT  
		Size: 128.1 MB (128103362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b7cf07833ee8819b666ebeb43b60b17f803c6d68a8f8a2ae49b0757473f46`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9f94601d6afe3d556624c05ea55b67ecc816be8728fa89634a2cadbba6218`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f9f73d16d4ba6a3449bd80183248de57fa72a95a292c86278d0b38d1c4e264db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be41fd1b58eb3064579cd4a08590f7732299ea4dcf11f3c130aae54ca42fcb49`

```dockerfile
```

-	Layers:
	-	`sha256:16a042b28046084f3dbe4ed69e68d5de675b9354491c6d81ac724cd764f6db0c`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d6a1e96dc0d07de9205c61cb37b077766078c798eaccadd69487112a2462f`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5ba616da907066423733e48e6334614d763267d5550cfcd081719e5cf82423df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fbc459d67ca93ec8867b9e6893ad776e178b57a6b0e6f2de1b24c1dedd54e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:10 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b89f520a88cf19dae316a4923b664b7e6bf95c3315e6d141fb757349d3e8a`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803e42c69cf3e606e27ca4a06da2435d4ea059a03cc5856cd6f50b37c3382595`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c14e296756ac06a1560de0a58b510f0b080c8cb05113b2aa3d2eaa03c83fc`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 5.8 MB (5791496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70cc2884f7e43f795b60e342e686802e72d0a5f8586bbec349943626ae98e39`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4609b660cfe4aef6e68410e3b40ab7efe4f35560ad7c855ec911a9e5fe28d5d`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ba81b42a2aa9e7a7a44386fefea991308a713531590f8dbf54305dca317874`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 48.8 MB (48777660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ee5a103ec0a7d4c8c41713b03fe52b67fd6265fa77e023c7b54ade27f6111`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457891cd44ec3897c6bddbd3934cc988aa57b4d42ec8990f1cac5c8dd98ffa4`  
		Last Modified: Sat, 31 Jan 2026 00:13:23 GMT  
		Size: 126.7 MB (126681626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7015cb85f5f43fe858846b8f8e8359c24c3827d30f9da438dbfee91cafd71`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19c4a82a368d5fd463df226d9961021f91237e84f338104e050377e2eb45b17`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d22c90075d7dae6d423e1e9f4e916c29a8ab682d7b88d81b12c5b4d7c3d8187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45439e0f5020f7dbe2617512deb8c471592a4128ddcce5ef3beb1f3003d7d603`

```dockerfile
```

-	Layers:
	-	`sha256:451653891a1ef001567b90b98ad6dc519aedc1d1480b274d56bf4901d08fe095`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a3c6ac4004261be493ee6b3e7a3871a796b4a8f4fa91b7b90e95796f99e5cf`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9c7897818a32cb639b0404fadd828c7cbc522da90398107fbae55682aee577c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8fd817c666f6913194a2c24946e2a525ab514fd47036532b10e3ae62fdccf7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232311053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fcbe35dfe84111133d8ba560a86aec393db4353b85217bccdbdbe3b328ad6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:45 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:12:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:13:07 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:13:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:13:07 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:13:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bba75f9c491c56e71e9cabdf6b194c7006c9d07385e525909c43563aedd021`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7842cc7478272f46c7b84fc61ee1d74e97132522fc6954e05b6b3b3e09e922a`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1944d72bca6dde4d32cc82b406d5dfd1d8e80d54fb65aef206f039abaf1d0e`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 6.2 MB (6175266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ebd7bbdedabb4111bd5bf3030c9d3044f6987ebda89fcf261364f3f49b605`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142c5fc9ea8a2d7156d977b33918b7b695a363201df60b979f8dcf80c95bedb3`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526dbe6f3591e92ef805b1b368f3ded7965b3c9ad699dd234814bc49e66e88aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:39 GMT  
		Size: 49.9 MB (49925465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b17de9630a006e5f9b21d95b0ba31a12dafe3510181c5fc326d91bcd69ddc`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145e04eb4706e5de6fdd3e0f3c9e546ef09acc3c50c6555f6631ae12c571d96`  
		Last Modified: Sat, 31 Jan 2026 00:13:40 GMT  
		Size: 128.1 MB (128103362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b7cf07833ee8819b666ebeb43b60b17f803c6d68a8f8a2ae49b0757473f46`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9f94601d6afe3d556624c05ea55b67ecc816be8728fa89634a2cadbba6218`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f9f73d16d4ba6a3449bd80183248de57fa72a95a292c86278d0b38d1c4e264db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be41fd1b58eb3064579cd4a08590f7732299ea4dcf11f3c130aae54ca42fcb49`

```dockerfile
```

-	Layers:
	-	`sha256:16a042b28046084f3dbe4ed69e68d5de675b9354491c6d81ac724cd764f6db0c`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d6a1e96dc0d07de9205c61cb37b077766078c798eaccadd69487112a2462f`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5ba616da907066423733e48e6334614d763267d5550cfcd081719e5cf82423df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fbc459d67ca93ec8867b9e6893ad776e178b57a6b0e6f2de1b24c1dedd54e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:10 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b89f520a88cf19dae316a4923b664b7e6bf95c3315e6d141fb757349d3e8a`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803e42c69cf3e606e27ca4a06da2435d4ea059a03cc5856cd6f50b37c3382595`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c14e296756ac06a1560de0a58b510f0b080c8cb05113b2aa3d2eaa03c83fc`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 5.8 MB (5791496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70cc2884f7e43f795b60e342e686802e72d0a5f8586bbec349943626ae98e39`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4609b660cfe4aef6e68410e3b40ab7efe4f35560ad7c855ec911a9e5fe28d5d`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ba81b42a2aa9e7a7a44386fefea991308a713531590f8dbf54305dca317874`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 48.8 MB (48777660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ee5a103ec0a7d4c8c41713b03fe52b67fd6265fa77e023c7b54ade27f6111`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457891cd44ec3897c6bddbd3934cc988aa57b4d42ec8990f1cac5c8dd98ffa4`  
		Last Modified: Sat, 31 Jan 2026 00:13:23 GMT  
		Size: 126.7 MB (126681626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7015cb85f5f43fe858846b8f8e8359c24c3827d30f9da438dbfee91cafd71`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19c4a82a368d5fd463df226d9961021f91237e84f338104e050377e2eb45b17`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d22c90075d7dae6d423e1e9f4e916c29a8ab682d7b88d81b12c5b4d7c3d8187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45439e0f5020f7dbe2617512deb8c471592a4128ddcce5ef3beb1f3003d7d603`

```dockerfile
```

-	Layers:
	-	`sha256:451653891a1ef001567b90b98ad6dc519aedc1d1480b274d56bf4901d08fe095`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a3c6ac4004261be493ee6b3e7a3871a796b4a8f4fa91b7b90e95796f99e5cf`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:9c7897818a32cb639b0404fadd828c7cbc522da90398107fbae55682aee577c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:8fd817c666f6913194a2c24946e2a525ab514fd47036532b10e3ae62fdccf7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232311053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fcbe35dfe84111133d8ba560a86aec393db4353b85217bccdbdbe3b328ad6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:45 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:12:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:13:07 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:13:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:13:07 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:13:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bba75f9c491c56e71e9cabdf6b194c7006c9d07385e525909c43563aedd021`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7842cc7478272f46c7b84fc61ee1d74e97132522fc6954e05b6b3b3e09e922a`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1944d72bca6dde4d32cc82b406d5dfd1d8e80d54fb65aef206f039abaf1d0e`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 6.2 MB (6175266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ebd7bbdedabb4111bd5bf3030c9d3044f6987ebda89fcf261364f3f49b605`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142c5fc9ea8a2d7156d977b33918b7b695a363201df60b979f8dcf80c95bedb3`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526dbe6f3591e92ef805b1b368f3ded7965b3c9ad699dd234814bc49e66e88aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:39 GMT  
		Size: 49.9 MB (49925465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b17de9630a006e5f9b21d95b0ba31a12dafe3510181c5fc326d91bcd69ddc`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145e04eb4706e5de6fdd3e0f3c9e546ef09acc3c50c6555f6631ae12c571d96`  
		Last Modified: Sat, 31 Jan 2026 00:13:40 GMT  
		Size: 128.1 MB (128103362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b7cf07833ee8819b666ebeb43b60b17f803c6d68a8f8a2ae49b0757473f46`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9f94601d6afe3d556624c05ea55b67ecc816be8728fa89634a2cadbba6218`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:f9f73d16d4ba6a3449bd80183248de57fa72a95a292c86278d0b38d1c4e264db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be41fd1b58eb3064579cd4a08590f7732299ea4dcf11f3c130aae54ca42fcb49`

```dockerfile
```

-	Layers:
	-	`sha256:16a042b28046084f3dbe4ed69e68d5de675b9354491c6d81ac724cd764f6db0c`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d6a1e96dc0d07de9205c61cb37b077766078c798eaccadd69487112a2462f`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5ba616da907066423733e48e6334614d763267d5550cfcd081719e5cf82423df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fbc459d67ca93ec8867b9e6893ad776e178b57a6b0e6f2de1b24c1dedd54e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:10 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b89f520a88cf19dae316a4923b664b7e6bf95c3315e6d141fb757349d3e8a`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803e42c69cf3e606e27ca4a06da2435d4ea059a03cc5856cd6f50b37c3382595`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c14e296756ac06a1560de0a58b510f0b080c8cb05113b2aa3d2eaa03c83fc`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 5.8 MB (5791496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70cc2884f7e43f795b60e342e686802e72d0a5f8586bbec349943626ae98e39`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4609b660cfe4aef6e68410e3b40ab7efe4f35560ad7c855ec911a9e5fe28d5d`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ba81b42a2aa9e7a7a44386fefea991308a713531590f8dbf54305dca317874`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 48.8 MB (48777660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ee5a103ec0a7d4c8c41713b03fe52b67fd6265fa77e023c7b54ade27f6111`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457891cd44ec3897c6bddbd3934cc988aa57b4d42ec8990f1cac5c8dd98ffa4`  
		Last Modified: Sat, 31 Jan 2026 00:13:23 GMT  
		Size: 126.7 MB (126681626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7015cb85f5f43fe858846b8f8e8359c24c3827d30f9da438dbfee91cafd71`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19c4a82a368d5fd463df226d9961021f91237e84f338104e050377e2eb45b17`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:d22c90075d7dae6d423e1e9f4e916c29a8ab682d7b88d81b12c5b4d7c3d8187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45439e0f5020f7dbe2617512deb8c471592a4128ddcce5ef3beb1f3003d7d603`

```dockerfile
```

-	Layers:
	-	`sha256:451653891a1ef001567b90b98ad6dc519aedc1d1480b274d56bf4901d08fe095`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a3c6ac4004261be493ee6b3e7a3871a796b4a8f4fa91b7b90e95796f99e5cf`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:9c7897818a32cb639b0404fadd828c7cbc522da90398107fbae55682aee577c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8fd817c666f6913194a2c24946e2a525ab514fd47036532b10e3ae62fdccf7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232311053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fcbe35dfe84111133d8ba560a86aec393db4353b85217bccdbdbe3b328ad6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:45 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:12:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:13:07 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:13:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:13:07 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:13:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bba75f9c491c56e71e9cabdf6b194c7006c9d07385e525909c43563aedd021`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7842cc7478272f46c7b84fc61ee1d74e97132522fc6954e05b6b3b3e09e922a`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1944d72bca6dde4d32cc82b406d5dfd1d8e80d54fb65aef206f039abaf1d0e`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 6.2 MB (6175266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ebd7bbdedabb4111bd5bf3030c9d3044f6987ebda89fcf261364f3f49b605`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142c5fc9ea8a2d7156d977b33918b7b695a363201df60b979f8dcf80c95bedb3`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526dbe6f3591e92ef805b1b368f3ded7965b3c9ad699dd234814bc49e66e88aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:39 GMT  
		Size: 49.9 MB (49925465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b17de9630a006e5f9b21d95b0ba31a12dafe3510181c5fc326d91bcd69ddc`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145e04eb4706e5de6fdd3e0f3c9e546ef09acc3c50c6555f6631ae12c571d96`  
		Last Modified: Sat, 31 Jan 2026 00:13:40 GMT  
		Size: 128.1 MB (128103362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b7cf07833ee8819b666ebeb43b60b17f803c6d68a8f8a2ae49b0757473f46`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9f94601d6afe3d556624c05ea55b67ecc816be8728fa89634a2cadbba6218`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f9f73d16d4ba6a3449bd80183248de57fa72a95a292c86278d0b38d1c4e264db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be41fd1b58eb3064579cd4a08590f7732299ea4dcf11f3c130aae54ca42fcb49`

```dockerfile
```

-	Layers:
	-	`sha256:16a042b28046084f3dbe4ed69e68d5de675b9354491c6d81ac724cd764f6db0c`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d6a1e96dc0d07de9205c61cb37b077766078c798eaccadd69487112a2462f`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5ba616da907066423733e48e6334614d763267d5550cfcd081719e5cf82423df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fbc459d67ca93ec8867b9e6893ad776e178b57a6b0e6f2de1b24c1dedd54e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:10 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b89f520a88cf19dae316a4923b664b7e6bf95c3315e6d141fb757349d3e8a`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803e42c69cf3e606e27ca4a06da2435d4ea059a03cc5856cd6f50b37c3382595`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c14e296756ac06a1560de0a58b510f0b080c8cb05113b2aa3d2eaa03c83fc`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 5.8 MB (5791496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70cc2884f7e43f795b60e342e686802e72d0a5f8586bbec349943626ae98e39`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4609b660cfe4aef6e68410e3b40ab7efe4f35560ad7c855ec911a9e5fe28d5d`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ba81b42a2aa9e7a7a44386fefea991308a713531590f8dbf54305dca317874`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 48.8 MB (48777660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ee5a103ec0a7d4c8c41713b03fe52b67fd6265fa77e023c7b54ade27f6111`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457891cd44ec3897c6bddbd3934cc988aa57b4d42ec8990f1cac5c8dd98ffa4`  
		Last Modified: Sat, 31 Jan 2026 00:13:23 GMT  
		Size: 126.7 MB (126681626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7015cb85f5f43fe858846b8f8e8359c24c3827d30f9da438dbfee91cafd71`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19c4a82a368d5fd463df226d9961021f91237e84f338104e050377e2eb45b17`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d22c90075d7dae6d423e1e9f4e916c29a8ab682d7b88d81b12c5b4d7c3d8187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45439e0f5020f7dbe2617512deb8c471592a4128ddcce5ef3beb1f3003d7d603`

```dockerfile
```

-	Layers:
	-	`sha256:451653891a1ef001567b90b98ad6dc519aedc1d1480b274d56bf4901d08fe095`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a3c6ac4004261be493ee6b3e7a3871a796b4a8f4fa91b7b90e95796f99e5cf`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:9c7897818a32cb639b0404fadd828c7cbc522da90398107fbae55682aee577c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8fd817c666f6913194a2c24946e2a525ab514fd47036532b10e3ae62fdccf7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232311053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fcbe35dfe84111133d8ba560a86aec393db4353b85217bccdbdbe3b328ad6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:45 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:12:07 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:12:08 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:13:07 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:13:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:13:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:13:07 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:13:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bba75f9c491c56e71e9cabdf6b194c7006c9d07385e525909c43563aedd021`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7842cc7478272f46c7b84fc61ee1d74e97132522fc6954e05b6b3b3e09e922a`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1944d72bca6dde4d32cc82b406d5dfd1d8e80d54fb65aef206f039abaf1d0e`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 6.2 MB (6175266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ebd7bbdedabb4111bd5bf3030c9d3044f6987ebda89fcf261364f3f49b605`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142c5fc9ea8a2d7156d977b33918b7b695a363201df60b979f8dcf80c95bedb3`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526dbe6f3591e92ef805b1b368f3ded7965b3c9ad699dd234814bc49e66e88aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:39 GMT  
		Size: 49.9 MB (49925465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b17de9630a006e5f9b21d95b0ba31a12dafe3510181c5fc326d91bcd69ddc`  
		Last Modified: Sat, 31 Jan 2026 00:13:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145e04eb4706e5de6fdd3e0f3c9e546ef09acc3c50c6555f6631ae12c571d96`  
		Last Modified: Sat, 31 Jan 2026 00:13:40 GMT  
		Size: 128.1 MB (128103362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b7cf07833ee8819b666ebeb43b60b17f803c6d68a8f8a2ae49b0757473f46`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9f94601d6afe3d556624c05ea55b67ecc816be8728fa89634a2cadbba6218`  
		Last Modified: Sat, 31 Jan 2026 00:13:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f9f73d16d4ba6a3449bd80183248de57fa72a95a292c86278d0b38d1c4e264db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be41fd1b58eb3064579cd4a08590f7732299ea4dcf11f3c130aae54ca42fcb49`

```dockerfile
```

-	Layers:
	-	`sha256:16a042b28046084f3dbe4ed69e68d5de675b9354491c6d81ac724cd764f6db0c`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d6a1e96dc0d07de9205c61cb37b077766078c798eaccadd69487112a2462f`  
		Last Modified: Sat, 31 Jan 2026 00:13:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5ba616da907066423733e48e6334614d763267d5550cfcd081719e5cf82423df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fbc459d67ca93ec8867b9e6893ad776e178b57a6b0e6f2de1b24c1dedd54e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:10 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 31 Jan 2026 00:11:37 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:11:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 31 Jan 2026 00:12:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 31 Jan 2026 00:12:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b89f520a88cf19dae316a4923b664b7e6bf95c3315e6d141fb757349d3e8a`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803e42c69cf3e606e27ca4a06da2435d4ea059a03cc5856cd6f50b37c3382595`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c14e296756ac06a1560de0a58b510f0b080c8cb05113b2aa3d2eaa03c83fc`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 5.8 MB (5791496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70cc2884f7e43f795b60e342e686802e72d0a5f8586bbec349943626ae98e39`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4609b660cfe4aef6e68410e3b40ab7efe4f35560ad7c855ec911a9e5fe28d5d`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ba81b42a2aa9e7a7a44386fefea991308a713531590f8dbf54305dca317874`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 48.8 MB (48777660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ee5a103ec0a7d4c8c41713b03fe52b67fd6265fa77e023c7b54ade27f6111`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457891cd44ec3897c6bddbd3934cc988aa57b4d42ec8990f1cac5c8dd98ffa4`  
		Last Modified: Sat, 31 Jan 2026 00:13:23 GMT  
		Size: 126.7 MB (126681626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7015cb85f5f43fe858846b8f8e8359c24c3827d30f9da438dbfee91cafd71`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19c4a82a368d5fd463df226d9961021f91237e84f338104e050377e2eb45b17`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d22c90075d7dae6d423e1e9f4e916c29a8ab682d7b88d81b12c5b4d7c3d8187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45439e0f5020f7dbe2617512deb8c471592a4128ddcce5ef3beb1f3003d7d603`

```dockerfile
```

-	Layers:
	-	`sha256:451653891a1ef001567b90b98ad6dc519aedc1d1480b274d56bf4901d08fe095`  
		Last Modified: Sat, 31 Jan 2026 00:13:19 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a3c6ac4004261be493ee6b3e7a3871a796b4a8f4fa91b7b90e95796f99e5cf`  
		Last Modified: Sat, 31 Jan 2026 00:13:18 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:c4678fed620278d29a6ef031b6aba9a31b1bc8f48e46bd56e9706943db2bc0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:7b67e5d38694e2a7d452fe58b8f0a9dd7133c5a5ec15511bf707344522e52cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233235378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffec24914d0400302b39b2d89b48ed334fed1719080cb577f4bc28bceba283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:53 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:18 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:18 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:21 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b10d19996b9826c15f8957f58ce8f4a5b4439ea6004de90d98341359ea5454`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3da22b30fe536b79b810e7fadf82442a3abd4277791c53a9e328bc4297735`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179870ed4f67cf550985d567df6cc6ecf71d64c5bd52613b6691a389d7ad88`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 6.2 MB (6175260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a30003c2eb7544d75acf2e4357256b4cedf6638cc91e979e914b16010f6c2`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54eefb1b1ac9740bcc324b8fe2f1a3a172ed385a8c943207397fd6e725bfa05`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f157e82a70ad96b2d80dd4ebd02529b18e12d1cbef57a49a5bbc7e0675d337`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 47.8 MB (47811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aee23ed85355d1abfbf446f8c80044446e9098fdec57192df115491edab314`  
		Last Modified: Sat, 31 Jan 2026 00:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1cd90e6407c1d9b6c16bee686b58b08b0823bfbe7c4d446b6dfd9ef37d0ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:57 GMT  
		Size: 131.1 MB (131141800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb6d2428e1cbdeb8791b0b0a898deeeec5b631d615fb1867a1b0a02f949eef`  
		Last Modified: Sat, 31 Jan 2026 00:12:55 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:45aa99642c453c67b16aaf9828c7907ed9c62ed03b068449b45ad24960d8d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9eb37bf857384a44b3af3960b6405ab5632552b029d18e43e90f8b4319e734`

```dockerfile
```

-	Layers:
	-	`sha256:f3b798bd6d0bab7c91484b35eb7ff420a5cb149c62924c1c9876f9d1451079ea`  
		Last Modified: Sat, 31 Jan 2026 00:12:53 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b38b225a111740f39bd7089dde003c6cd905b7933cf51414a7ca9b29e9b2af`  
		Last Modified: Sat, 31 Jan 2026 00:12:52 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6f5b5d699ad48d28761e01d41ed27c2493c923d38ced9b12e358f420ad1167ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd3b9259f63fea0773fb30b7c238fcbbc647ffd4d9701dff290aa46b9462cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:11:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:11:12 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:11:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 31 Jan 2026 00:11:38 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:11:39 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:12:12 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 31 Jan 2026 00:12:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0003bb3c02cdcb5ebab93d4f6cf61f9430469ae240325117ec7333e86a78c7d`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77229059e2e027e5478dd88383133984f8898e498161e212a0a5099cd70403a`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d641b0963a3a4c5e4605c5f14ced70c6e102003ef5e2760e336853d1fa4cd685`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 5.8 MB (5791502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f813722a19ab9b7a62acc973a2edda5524bad4d0e882e0e3facb9f9bbb16fa`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45674ea9cb43dc51c2ff05b786b943b586995338b3953e3d1c709429fa513f76`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45595a46988036c44666bc8ebc0026ea4faa2962991b4fb8700492e72dc8ae7c`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 46.7 MB (46701239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62b58b512c9926eae2900ad35feecc067286ebe828060d8c0544f8ca38c76c`  
		Last Modified: Sat, 31 Jan 2026 00:13:21 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a038ee0e6440c91e0bf0f98d340066adf89fa7845faf1e8c5462bd45bc53521`  
		Last Modified: Sat, 31 Jan 2026 00:13:25 GMT  
		Size: 129.5 MB (129549299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a88e06251fa53736bc95713326dc55f691d70cf10269daa77a589ffca8ceea`  
		Last Modified: Sat, 31 Jan 2026 00:13:22 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bf0ecdab283298c57c06ebe1498d3ee794aa0a4227e7db1a002bcfdf42dd2c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c78f86eb927da799000416112b10f93a294cde3e416f2e2b45028ac9e11f68`

```dockerfile
```

-	Layers:
	-	`sha256:29b4a898aeb5b486bb803d8d3b67b966d2ed3a34cd8c04396f457ea36aa7eb4e`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b052f49896cb25d5ef367bc3bac1ba8988d51792de0bc01d0b693c0b4d87701`  
		Last Modified: Sat, 31 Jan 2026 00:13:20 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:932fe8fbc04c1488a38f8cab0f30cdac8d7753bded3df1762475a8001a323bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0eab641543f55f4698934b0de264c88c1a8bc0137b77260123507620c8ab507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0648a94df9f763bcb89445f29de8f7398a03f50a7bc6e9f1da18f1d3812d1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:31 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:58 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:58 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:11:28 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf746d6e600363233ab0496607c5d2449bb495e761ee541d3fe92a0dc18130e`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3afd2b6b7544686823d45f4f4e0d8eb1be6b541eba32f4c587b4d9cd3b7a97`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc017098aeb30fd29a2250a2061052768b87a3ae4d8ef81dd18ad4dad9c2ba`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 6.2 MB (6175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d4e0fa09108753a1aadd8822101b7121feca36e14b0fd10ff386bc84dde03`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d294926a196e9697e774edbaa0efc7e74265cac9bb3871d140b9cfade1dbb`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c26b04681bd48af6d96160e7e4323482e90cb76c6eb8eaeea58d044391df11`  
		Last Modified: Sat, 31 Jan 2026 00:12:47 GMT  
		Size: 51.5 MB (51455329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d138a56c48507b2b56f29029b04a3ff34113ef45b172de9f770473771d4da`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863342a2e0657e04e8ea01cb628aa564931b12542d0c2d46ee88a24dcf87d7e8`  
		Last Modified: Sat, 31 Jan 2026 00:12:51 GMT  
		Size: 160.6 MB (160632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92d9f2f65a6cb35f8260356c7aff44d821d83886d968ccb778b7f38fa057f5`  
		Last Modified: Sat, 31 Jan 2026 00:12:45 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca63fc64668d3d4ed7ec2f54636550a51e19af3c70a6df41639cbf7fee630f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5756884e05bc2bfc30cc33b17a0520e06194f75c28932b038494eb874d389a82`

```dockerfile
```

-	Layers:
	-	`sha256:6f35804f94b3aa652eca8c7d96c35aca0bb0077953ea182e7139c40481b44780`  
		Last Modified: Sat, 31 Jan 2026 00:12:44 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec207a705e69a7dc83d80c7bdc6486f4757ac090dd29ed05e2a1c84beef780f`  
		Last Modified: Sat, 31 Jan 2026 00:12:43 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1cf714550d102b117cdfd117ca6df50042d52e38b720c026fba9d16fa68c9bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261470904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3988c5d3ed950b6877ff60412605cb20bf7a6e09a66023f00e8c79881b82d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:10:00 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 31 Jan 2026 00:10:02 GMT
ENV GOSU_VERSION=1.19
# Sat, 31 Jan 2026 00:10:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 31 Jan 2026 00:10:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 31 Jan 2026 00:10:28 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:10:28 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 31 Jan 2026 00:10:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 31 Jan 2026 00:11:42 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 31 Jan 2026 00:11:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 31 Jan 2026 00:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 31 Jan 2026 00:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jan 2026 00:11:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 31 Jan 2026 00:11:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957f2e7085cf5d88ab7a79175c35a8455ff80afdccf2bb81305572215105ac`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0c5c262d5e7280eac9de7653f6c3ce77411fe7efb3032073368154195d56d`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59ba4d7fa272c541ed71988897b99f42c2b15f8c8a75d6bf10c858599259cf9`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 5.8 MB (5791488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6c63ed289e9e9390180b066aaf2544a0d72082106a1040e3ba1e7bfdd71a3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f10befa1067630c472630d78efa8f3860cfd5692e59473f0f057697d19fad`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377787c0d940d400171fb05c3b150b20b2aa8b80ad6ec8e30651fafc4d89dd4`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 50.1 MB (50089165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7384d8630fb11d299016902c627a01111e74cbf0b124085bd468e51d4fc729d`  
		Last Modified: Sat, 31 Jan 2026 00:12:19 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e5ea9eb583e16b3b55896d2c5856e764888b0bd32a360a01f27a2d788913c`  
		Last Modified: Sat, 31 Jan 2026 00:12:23 GMT  
		Size: 158.9 MB (158941599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff3675e9cf9568ebb047670a30a9b26d1a229d8b0dc8b839d22af9d03251fe`  
		Last Modified: Sat, 31 Jan 2026 00:12:20 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3b8450269a2928ce12ad5444446c3b811bc8d3adc4092c6f557d48c4ee8cb8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5d057fced1845a0bb9c66b99dba29803ef97dbc633328a386417cb4727a5a`

```dockerfile
```

-	Layers:
	-	`sha256:290b3bb5ad670daf8c0eb54d019973b86eb7d0c198768d2699da19706cd32140`  
		Last Modified: Sat, 31 Jan 2026 00:12:18 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb42dc96b13b5f8981e8f190ad105589c46e2ba97e7abd3f03fe6054be8be3`  
		Last Modified: Sat, 31 Jan 2026 00:12:17 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
