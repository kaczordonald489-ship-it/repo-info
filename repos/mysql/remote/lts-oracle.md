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
