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
