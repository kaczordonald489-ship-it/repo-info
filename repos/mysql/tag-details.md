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
-	[`mysql:8.0.44`](#mysql8044)
-	[`mysql:8.0.44-bookworm`](#mysql8044-bookworm)
-	[`mysql:8.0.44-debian`](#mysql8044-debian)
-	[`mysql:8.0.44-oracle`](#mysql8044-oracle)
-	[`mysql:8.0.44-oraclelinux9`](#mysql8044-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.7`](#mysql847)
-	[`mysql:8.4.7-oracle`](#mysql847-oracle)
-	[`mysql:8.4.7-oraclelinux9`](#mysql847-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.5`](#mysql95)
-	[`mysql:9.5-oracle`](#mysql95-oracle)
-	[`mysql:9.5-oraclelinux9`](#mysql95-oraclelinux9)
-	[`mysql:9.5.0`](#mysql950)
-	[`mysql:9.5.0-oracle`](#mysql950-oracle)
-	[`mysql:9.5.0-oraclelinux9`](#mysql950-oraclelinux9)
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
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f37951fc3753a6a22d6c7bf6978c5e5fefcf6f31814d98c582524f98eae52b21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:52cc603981fda056aa44422b192a0c01e1dd0331465330157abb8795484c99a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234880000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34178dbaefd067c5997133cbdef31f164aa899689394f70b065725afb7aa322a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f78e34adfadf620578919075ce76accd335e02f4c4a2494476870c948b24a6a`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed1082d9e2d4196202cfb3cdc3141a99ae7418fad3287e39685890857c7e50`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecfb07ed08c78d9ae05f96918469f3323983f8353c5f6d8bc1fe7cfe8ca307`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 6.8 MB (6819775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f94eaa123bffda76b09109dee2f66ab97edc6e02c2250630dba894bb54e9136`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2d53254403ab5a46208cbee5ce6e64030ed6af39a1e396850bd01c2b55991f`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec49971d9445b77beb107874bc797a8a8f4bfc1eb1c9713618a4a765a13908`  
		Last Modified: Wed, 22 Oct 2025 02:42:49 GMT  
		Size: 49.9 MB (49897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca9f583d44e2a026171ec7f1854acc693bbe74937321b557cc99c975a190c6`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf302dead6257c4a894029a3d8ac8b8fca1dd6fe75f58c4b17330e149ce137`  
		Last Modified: Wed, 22 Oct 2025 02:43:02 GMT  
		Size: 127.9 MB (127873232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd516ff7651d7283213508a304b0195681370b924c3f913a13126933ce14ed`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68710a4a4e9516175a58b8eed8a0068ae2d9464ab0fb6d28fc05eb827033b17`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1e7daca7e944d4c4e0a680bf33539a45964b7946908c9c25418c5413f84340f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14670414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce142dd64a0064101864190837a693bef253d897b49ec7102b20a2e4abfc317d`

```dockerfile
```

-	Layers:
	-	`sha256:dac8f6f60447d6048aa55721af2d37c7d3ce5c832a8878161f57645f55ded687`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 14.6 MB (14635460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580930fc92c5fbacfec9cfd9f59f061f0419174ca9b61d352c757d0a3a0106fd`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:f37951fc3753a6a22d6c7bf6978c5e5fefcf6f31814d98c582524f98eae52b21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:52cc603981fda056aa44422b192a0c01e1dd0331465330157abb8795484c99a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234880000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34178dbaefd067c5997133cbdef31f164aa899689394f70b065725afb7aa322a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f78e34adfadf620578919075ce76accd335e02f4c4a2494476870c948b24a6a`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed1082d9e2d4196202cfb3cdc3141a99ae7418fad3287e39685890857c7e50`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecfb07ed08c78d9ae05f96918469f3323983f8353c5f6d8bc1fe7cfe8ca307`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 6.8 MB (6819775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f94eaa123bffda76b09109dee2f66ab97edc6e02c2250630dba894bb54e9136`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2d53254403ab5a46208cbee5ce6e64030ed6af39a1e396850bd01c2b55991f`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec49971d9445b77beb107874bc797a8a8f4bfc1eb1c9713618a4a765a13908`  
		Last Modified: Wed, 22 Oct 2025 02:42:49 GMT  
		Size: 49.9 MB (49897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca9f583d44e2a026171ec7f1854acc693bbe74937321b557cc99c975a190c6`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf302dead6257c4a894029a3d8ac8b8fca1dd6fe75f58c4b17330e149ce137`  
		Last Modified: Wed, 22 Oct 2025 02:43:02 GMT  
		Size: 127.9 MB (127873232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd516ff7651d7283213508a304b0195681370b924c3f913a13126933ce14ed`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68710a4a4e9516175a58b8eed8a0068ae2d9464ab0fb6d28fc05eb827033b17`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1e7daca7e944d4c4e0a680bf33539a45964b7946908c9c25418c5413f84340f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14670414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce142dd64a0064101864190837a693bef253d897b49ec7102b20a2e4abfc317d`

```dockerfile
```

-	Layers:
	-	`sha256:dac8f6f60447d6048aa55721af2d37c7d3ce5c832a8878161f57645f55ded687`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 14.6 MB (14635460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580930fc92c5fbacfec9cfd9f59f061f0419174ca9b61d352c757d0a3a0106fd`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:f37951fc3753a6a22d6c7bf6978c5e5fefcf6f31814d98c582524f98eae52b21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:52cc603981fda056aa44422b192a0c01e1dd0331465330157abb8795484c99a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234880000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34178dbaefd067c5997133cbdef31f164aa899689394f70b065725afb7aa322a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f78e34adfadf620578919075ce76accd335e02f4c4a2494476870c948b24a6a`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed1082d9e2d4196202cfb3cdc3141a99ae7418fad3287e39685890857c7e50`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecfb07ed08c78d9ae05f96918469f3323983f8353c5f6d8bc1fe7cfe8ca307`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 6.8 MB (6819775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f94eaa123bffda76b09109dee2f66ab97edc6e02c2250630dba894bb54e9136`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2d53254403ab5a46208cbee5ce6e64030ed6af39a1e396850bd01c2b55991f`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec49971d9445b77beb107874bc797a8a8f4bfc1eb1c9713618a4a765a13908`  
		Last Modified: Wed, 22 Oct 2025 02:42:49 GMT  
		Size: 49.9 MB (49897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca9f583d44e2a026171ec7f1854acc693bbe74937321b557cc99c975a190c6`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf302dead6257c4a894029a3d8ac8b8fca1dd6fe75f58c4b17330e149ce137`  
		Last Modified: Wed, 22 Oct 2025 02:43:02 GMT  
		Size: 127.9 MB (127873232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd516ff7651d7283213508a304b0195681370b924c3f913a13126933ce14ed`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68710a4a4e9516175a58b8eed8a0068ae2d9464ab0fb6d28fc05eb827033b17`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1e7daca7e944d4c4e0a680bf33539a45964b7946908c9c25418c5413f84340f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14670414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce142dd64a0064101864190837a693bef253d897b49ec7102b20a2e4abfc317d`

```dockerfile
```

-	Layers:
	-	`sha256:dac8f6f60447d6048aa55721af2d37c7d3ce5c832a8878161f57645f55ded687`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 14.6 MB (14635460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580930fc92c5fbacfec9cfd9f59f061f0419174ca9b61d352c757d0a3a0106fd`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44`

```console
$ docker pull mysql@sha256:f37951fc3753a6a22d6c7bf6978c5e5fefcf6f31814d98c582524f98eae52b21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44` - linux; amd64

```console
$ docker pull mysql@sha256:52cc603981fda056aa44422b192a0c01e1dd0331465330157abb8795484c99a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234880000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34178dbaefd067c5997133cbdef31f164aa899689394f70b065725afb7aa322a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f78e34adfadf620578919075ce76accd335e02f4c4a2494476870c948b24a6a`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed1082d9e2d4196202cfb3cdc3141a99ae7418fad3287e39685890857c7e50`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecfb07ed08c78d9ae05f96918469f3323983f8353c5f6d8bc1fe7cfe8ca307`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 6.8 MB (6819775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f94eaa123bffda76b09109dee2f66ab97edc6e02c2250630dba894bb54e9136`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2d53254403ab5a46208cbee5ce6e64030ed6af39a1e396850bd01c2b55991f`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec49971d9445b77beb107874bc797a8a8f4bfc1eb1c9713618a4a765a13908`  
		Last Modified: Wed, 22 Oct 2025 02:42:49 GMT  
		Size: 49.9 MB (49897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca9f583d44e2a026171ec7f1854acc693bbe74937321b557cc99c975a190c6`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf302dead6257c4a894029a3d8ac8b8fca1dd6fe75f58c4b17330e149ce137`  
		Last Modified: Wed, 22 Oct 2025 02:43:02 GMT  
		Size: 127.9 MB (127873232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd516ff7651d7283213508a304b0195681370b924c3f913a13126933ce14ed`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68710a4a4e9516175a58b8eed8a0068ae2d9464ab0fb6d28fc05eb827033b17`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:1e7daca7e944d4c4e0a680bf33539a45964b7946908c9c25418c5413f84340f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14670414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce142dd64a0064101864190837a693bef253d897b49ec7102b20a2e4abfc317d`

```dockerfile
```

-	Layers:
	-	`sha256:dac8f6f60447d6048aa55721af2d37c7d3ce5c832a8878161f57645f55ded687`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 14.6 MB (14635460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580930fc92c5fbacfec9cfd9f59f061f0419174ca9b61d352c757d0a3a0106fd`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-bookworm`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-debian`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-debian` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oracle`

```console
$ docker pull mysql@sha256:f37951fc3753a6a22d6c7bf6978c5e5fefcf6f31814d98c582524f98eae52b21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:52cc603981fda056aa44422b192a0c01e1dd0331465330157abb8795484c99a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234880000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34178dbaefd067c5997133cbdef31f164aa899689394f70b065725afb7aa322a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f78e34adfadf620578919075ce76accd335e02f4c4a2494476870c948b24a6a`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed1082d9e2d4196202cfb3cdc3141a99ae7418fad3287e39685890857c7e50`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecfb07ed08c78d9ae05f96918469f3323983f8353c5f6d8bc1fe7cfe8ca307`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 6.8 MB (6819775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f94eaa123bffda76b09109dee2f66ab97edc6e02c2250630dba894bb54e9136`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2d53254403ab5a46208cbee5ce6e64030ed6af39a1e396850bd01c2b55991f`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec49971d9445b77beb107874bc797a8a8f4bfc1eb1c9713618a4a765a13908`  
		Last Modified: Wed, 22 Oct 2025 02:42:49 GMT  
		Size: 49.9 MB (49897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca9f583d44e2a026171ec7f1854acc693bbe74937321b557cc99c975a190c6`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf302dead6257c4a894029a3d8ac8b8fca1dd6fe75f58c4b17330e149ce137`  
		Last Modified: Wed, 22 Oct 2025 02:43:02 GMT  
		Size: 127.9 MB (127873232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd516ff7651d7283213508a304b0195681370b924c3f913a13126933ce14ed`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68710a4a4e9516175a58b8eed8a0068ae2d9464ab0fb6d28fc05eb827033b17`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1e7daca7e944d4c4e0a680bf33539a45964b7946908c9c25418c5413f84340f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14670414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce142dd64a0064101864190837a693bef253d897b49ec7102b20a2e4abfc317d`

```dockerfile
```

-	Layers:
	-	`sha256:dac8f6f60447d6048aa55721af2d37c7d3ce5c832a8878161f57645f55ded687`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 14.6 MB (14635460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580930fc92c5fbacfec9cfd9f59f061f0419174ca9b61d352c757d0a3a0106fd`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oraclelinux9`

```console
$ docker pull mysql@sha256:f37951fc3753a6a22d6c7bf6978c5e5fefcf6f31814d98c582524f98eae52b21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:52cc603981fda056aa44422b192a0c01e1dd0331465330157abb8795484c99a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234880000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34178dbaefd067c5997133cbdef31f164aa899689394f70b065725afb7aa322a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f78e34adfadf620578919075ce76accd335e02f4c4a2494476870c948b24a6a`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed1082d9e2d4196202cfb3cdc3141a99ae7418fad3287e39685890857c7e50`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecfb07ed08c78d9ae05f96918469f3323983f8353c5f6d8bc1fe7cfe8ca307`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 6.8 MB (6819775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f94eaa123bffda76b09109dee2f66ab97edc6e02c2250630dba894bb54e9136`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2d53254403ab5a46208cbee5ce6e64030ed6af39a1e396850bd01c2b55991f`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec49971d9445b77beb107874bc797a8a8f4bfc1eb1c9713618a4a765a13908`  
		Last Modified: Wed, 22 Oct 2025 02:42:49 GMT  
		Size: 49.9 MB (49897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca9f583d44e2a026171ec7f1854acc693bbe74937321b557cc99c975a190c6`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf302dead6257c4a894029a3d8ac8b8fca1dd6fe75f58c4b17330e149ce137`  
		Last Modified: Wed, 22 Oct 2025 02:43:02 GMT  
		Size: 127.9 MB (127873232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd516ff7651d7283213508a304b0195681370b924c3f913a13126933ce14ed`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68710a4a4e9516175a58b8eed8a0068ae2d9464ab0fb6d28fc05eb827033b17`  
		Last Modified: Wed, 22 Oct 2025 02:42:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1e7daca7e944d4c4e0a680bf33539a45964b7946908c9c25418c5413f84340f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14670414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce142dd64a0064101864190837a693bef253d897b49ec7102b20a2e4abfc317d`

```dockerfile
```

-	Layers:
	-	`sha256:dac8f6f60447d6048aa55721af2d37c7d3ce5c832a8878161f57645f55ded687`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 14.6 MB (14635460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580930fc92c5fbacfec9cfd9f59f061f0419174ca9b61d352c757d0a3a0106fd`  
		Last Modified: Wed, 22 Oct 2025 06:02:28 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oracle`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oraclelinux9`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oracle`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oraclelinux9`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oracle`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oraclelinux9`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
