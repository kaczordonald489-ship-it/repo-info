## `postgres:18-trixie`

```console
$ docker pull postgres@sha256:5ec39c188013123927f30a006987c6b0e20f3ef2b54b140dfa96dac6844d883f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:18-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:babcdb287bd9087f2fa7e6d59b26f90922e3fd6a9d5d944b6a737eb360ad97b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162205420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c0891f5de95d70f2fd664165fa6b8aa246b805a5c13c97824c4bd0970f4c8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:58:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 04:58:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:58:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 04:58:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 04:58:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 04:58:20 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 04:58:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:58:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 04:58:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 04:58:25 GMT
ENV PG_MAJOR=18
# Tue, 18 Nov 2025 04:58:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 18 Nov 2025 04:58:25 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 18 Nov 2025 04:58:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 04:58:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 04:58:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 04:58:44 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 18 Nov 2025 04:58:44 GMT
VOLUME [/var/lib/postgresql]
# Tue, 18 Nov 2025 04:58:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:58:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 04:58:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:58:44 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 04:58:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 04:58:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a50b0db5bdeef4b15e43ca52140bc406c820eed808fa25e44ae9a6ac588de25`  
		Last Modified: Tue, 18 Nov 2025 04:59:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02119e61144b9bb81fff1d3181043912248c3f2102df55c6e3ed332a852ff4fb`  
		Last Modified: Tue, 18 Nov 2025 04:59:17 GMT  
		Size: 6.4 MB (6436654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221278be71481cdc8fc0e56906a47bc9af2b763914d6da7e45b475661c43d82`  
		Last Modified: Tue, 18 Nov 2025 04:59:17 GMT  
		Size: 1.3 MB (1256619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed2b3560f55a09239f055d7eef76c2db1e41efff531f26b58bc9c67f23b8dfe`  
		Last Modified: Tue, 18 Nov 2025 04:59:17 GMT  
		Size: 8.2 MB (8203764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6aa08a3c71177d6ae18f2f8415ac03b1d5054b4adfcfcfef37347fa5efe66aa`  
		Last Modified: Tue, 18 Nov 2025 04:59:16 GMT  
		Size: 1.3 MB (1311474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fdbfae116dd73bd63985221759ae79114b2889986d55fe04fef97df2ec5533`  
		Last Modified: Tue, 18 Nov 2025 04:59:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81fb737f8b5a29cc62203bd68951d61836cdcf8e9a7224ef7774b2ad3a3a97`  
		Last Modified: Tue, 18 Nov 2025 04:59:17 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889840ade1ab91a4eec30cb71343bc203cd2341caa89923cee1b46e7602dfb49`  
		Last Modified: Tue, 18 Nov 2025 04:59:29 GMT  
		Size: 115.2 MB (115190658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75755489c862d3e22e55e07f2ae732e8211d6ac3afaa88f1b720f8c442a7813`  
		Last Modified: Tue, 18 Nov 2025 04:59:17 GMT  
		Size: 19.2 KB (19191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf222e9e3b90f5b91c1fd5327e14f63be6222530920e4a7985850f338b174c1`  
		Last Modified: Tue, 18 Nov 2025 04:59:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a19de04632f423cf8fb29ee843b2bc617cdf3cfa8a4f22b4dfaaa9afa8ee520`  
		Last Modified: Tue, 18 Nov 2025 04:59:16 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57871086ddd6a38d91b827e0dc0df69eaf820139b5a20f386464e885d22f531a`  
		Last Modified: Tue, 18 Nov 2025 04:59:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:bd8e6d179efb4f4a21bcd326827e0b425a9c9167be40a88b0b97f2a90e36e731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6008931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e52af1bf7d81ed780737ac7c52733194b4e83beacee73a36d37f2427e43b23`

```dockerfile
```

-	Layers:
	-	`sha256:8c481e98c21356c1f998ae66bd0888c0659dbddc25088a9345a9f3cb1383cd95`  
		Last Modified: Tue, 18 Nov 2025 06:13:55 GMT  
		Size: 6.0 MB (5956473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070d54116084e948a18dead50b4b1a97d099103ba31bca5a56bb05175fb7506`  
		Last Modified: Tue, 18 Nov 2025 06:13:55 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:a6580c4135ee56a7421e1ceae575ae0b1c15d3316d08aae35ff0edbe2d073d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91397186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5baffb8737c095e89ec5411444402dc2e37dac1fde9a817742ff53202051ee5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:02:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:02:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:27 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:02:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:02:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:02:36 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:02:43 GMT
ENV PG_MAJOR=18
# Tue, 18 Nov 2025 03:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 18 Nov 2025 03:02:43 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 18 Nov 2025 03:16:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:16:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:16:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:16:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 18 Nov 2025 03:16:09 GMT
VOLUME [/var/lib/postgresql]
# Tue, 18 Nov 2025 03:16:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:16:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:16:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:16:10 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:16:10 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:16:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f4c28bb4c6e7f01843c17e277a6a0048ed2e6b77dba8603a96e90ec3c1827c`  
		Last Modified: Tue, 18 Nov 2025 03:16:32 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb1f1406b51814a3ff092bffc8d4296d465474d8f1bb6105bc89e4c32a85fe`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 5.9 MB (5929053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35aba9d288fffa5e162483c6377c78f8a360b856d6947b27e41c3f89360fa7a7`  
		Last Modified: Tue, 18 Nov 2025 03:16:32 GMT  
		Size: 1.2 MB (1227413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c100f4ae6ac4c48fc55ff23876f41bad3520da72062ba96af52a0a9fe352ed32`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 8.2 MB (8204161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b6f13bea0cbe162b0d15f5c59aaabfc8a7d7eec8ea1e785a5190eea778e506`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 1.3 MB (1317195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c0154b0dbd84f0fea790fad000a129f50d399f00a3af0e6dbbcc42db8aa78`  
		Last Modified: Tue, 18 Nov 2025 03:16:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8f61bcca2798395f238b4e3c412cb0e8c71e1855a80ddafca4ce0eaa852c`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fae0b03b791a0b1d298196858e6b633d6fbca3be82c0336e79ada9b0c85159`  
		Last Modified: Tue, 18 Nov 2025 03:16:38 GMT  
		Size: 46.7 MB (46745463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d18c50742ca4b2c7fbf793b6c3f1faf7751d898f0b6f15fe25b81341161b9e3`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9c6b278bbaec546a139e948d215c473c1369d0bf9427926d953f52a51392f`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043ee1300d91c4015ca18470cb0d3519bda4b9d9cb323f51345ab4eca678adb8`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9c93daa794e858c4b11a0e360470ad10f26aefa959104def35c39316da8eb3`  
		Last Modified: Tue, 18 Nov 2025 03:16:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:6c725fe06ca45209046017722547b18e87767cd475b069c29909585956096e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f73889d48cf54452ee5c3d277e9de212246c43ecb653094956dfd4a16be2d8`

```dockerfile
```

-	Layers:
	-	`sha256:183cc6a0dcdde24f9116da6387e1b2a82488438c57c2a7337bae0a4b6c65843e`  
		Last Modified: Tue, 18 Nov 2025 06:13:59 GMT  
		Size: 5.1 MB (5119616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:defa41498ca97864c756b6f7d239189ee4407860aa39f06125f1223af23b8062`  
		Last Modified: Tue, 18 Nov 2025 06:14:00 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:61b98373a66c1bc5ef3e893c9dd632ef070c55a7ad6a458d36784bab0343a03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87718187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9368d26084ffbb1304266fa3d42456fec8b66ad8b9a9d8d0b4351aad5b25efe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:24:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:24:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:24:26 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:24:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:24:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:24:33 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:24:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:24:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:24:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:24:39 GMT
ENV PG_MAJOR=18
# Tue, 18 Nov 2025 03:24:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 18 Nov 2025 03:24:39 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 18 Nov 2025 03:36:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:36:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:36:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:36:44 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 18 Nov 2025 03:36:44 GMT
VOLUME [/var/lib/postgresql]
# Tue, 18 Nov 2025 03:36:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:36:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:36:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:36:44 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:36:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:36:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702fab0dc8e86a9c2cce8b0140b7a2539c05bea33cdf8298c34dd5e8283a7124`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c751ee5f4ca0de6b4c89847b8888ab3ee5fc02a7b53270b4b9a62e6098f3b160`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 5.5 MB (5496874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04d0fcf1f959e675d6a79d85839ff4ebd52514de52727bb3574c1bf1f610bff`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 1.2 MB (1222289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81079a43a2eea35c5f005cdac70bdb58cf10013a6daf1536924e2c49ca38d0dc`  
		Last Modified: Tue, 18 Nov 2025 03:37:11 GMT  
		Size: 8.2 MB (8203956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c841c463ffd7dbd8931a63f0aa01e135957908a0376a388508c460635aeac832`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 1.2 MB (1172458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913fa600a0e5d7d8c8914645401b4c06582fe3ef1792ce698b995cb32831e494`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcb057a4ae8b0a7d5d965577f13f25aeb5ec5c25ad1900a4d755f1d69856d37`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b1e7c48ca6fc9633b4fecc8c5d64bb73a0a6b867865354bbf695d71b0eb16`  
		Last Modified: Tue, 18 Nov 2025 03:37:12 GMT  
		Size: 45.4 MB (45382880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a71e61526536432e5d3cbf4a59509acca6ec52b2a578755156b1a78a7e7a8c`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 19.2 KB (19195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4735cea0813c3dd7fb2981a128704db631fb1583a4afc5b021a45ab647ffb022`  
		Last Modified: Tue, 18 Nov 2025 03:37:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc3b6e435a8e941c03a4701feb3f466d580029f43f67842df69acdedeb357e6`  
		Last Modified: Tue, 18 Nov 2025 03:37:10 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0c06e8cdccba208dbb27ed38cc6c7249b76b9aa42edab83279bba75048b518`  
		Last Modified: Tue, 18 Nov 2025 03:37:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3645e2e8ffbb01bcf61adc1d9e715996a739a6a1d97cda627595d39c9ad0b3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc634a1563bcb02aedd354c6491b29b0af78bc73d7b353fc1bf7eaf1f95ce35`

```dockerfile
```

-	Layers:
	-	`sha256:48e7f8c5cfc9b2f4c28cd6b83ba6049d7637799da7d6eaefb2022155ffa8937e`  
		Last Modified: Tue, 18 Nov 2025 06:14:05 GMT  
		Size: 5.1 MB (5118921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ff175f5ce4132a27fd22b180a001f492eeea4f6c92b978a77cdb5c5487be78`  
		Last Modified: Tue, 18 Nov 2025 06:14:05 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c80f4d2a7a0576ce63056429ab9f45a8cf38f5d0a7eb1a89e70fbefbc5bba212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160813239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246b1ef15b7401309051f932247e794ada9a0120d5b422db4eb67843410a2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:59:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 02:59:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:59:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:59:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 02:59:20 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 02:59:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 02:59:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:24 GMT
ENV PG_MAJOR=18
# Tue, 18 Nov 2025 02:59:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 18 Nov 2025 02:59:24 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 18 Nov 2025 02:59:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 02:59:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 02:59:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 02:59:43 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 18 Nov 2025 02:59:43 GMT
VOLUME [/var/lib/postgresql]
# Tue, 18 Nov 2025 02:59:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:59:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 02:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:59:43 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 02:59:43 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 02:59:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d40ad1ee5171160eaf0d19b0ec102b2c2c0645dce2188f81110f82028bf7df2`  
		Last Modified: Tue, 18 Nov 2025 03:00:22 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e86690e08b45bca61f6eb9f8deb5a16e09fc41c9ed729c80b27a791686a2013`  
		Last Modified: Tue, 18 Nov 2025 03:00:22 GMT  
		Size: 6.2 MB (6232037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aea44977d6932b440d1770057091be206805be43009d1c86379b8717a08386`  
		Last Modified: Tue, 18 Nov 2025 03:00:23 GMT  
		Size: 1.2 MB (1209442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5b2941599bf3cccde7b513bff09a2d4380a123d3b9bcae7180fd10c5492786`  
		Last Modified: Tue, 18 Nov 2025 03:00:23 GMT  
		Size: 8.2 MB (8203923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e808f1e529cfffd5b98ae366039d64483386db124d3d0b5acdbee822078b843e`  
		Last Modified: Tue, 18 Nov 2025 03:00:22 GMT  
		Size: 1.2 MB (1220452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c5a27f41447a62fcc3c8c7a30136feae957b9f91e4ab39e09b13aa5847a8d7`  
		Last Modified: Tue, 18 Nov 2025 03:00:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84932fbe51de4cea1b224160f4a54e0a691db87d0d52c56f6c1b1dd6f1102cf`  
		Last Modified: Tue, 18 Nov 2025 03:00:22 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e5f1d7b9946750d327f4701410fa824d9c02e78710adc9761456f41e0b4a09`  
		Last Modified: Tue, 18 Nov 2025 03:00:38 GMT  
		Size: 113.8 MB (113779017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477d35ab7c57b7378187d7f584eeab4666aeb6e73149dc5a74a54da27ff4c5f8`  
		Last Modified: Tue, 18 Nov 2025 03:00:23 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c598951473cfb9d044e64c358d69b3d12e0548a814ee65729ee5f77fefa68093`  
		Last Modified: Tue, 18 Nov 2025 03:00:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bb4e0a9b608e6fae3c2a6d36cd51737468c2f95716a63f1a9a801a17294234`  
		Last Modified: Tue, 18 Nov 2025 03:00:21 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aee7b1337ee457514ae5f090b829546a4fa84c965d61e7c2a5df455e290e93e`  
		Last Modified: Tue, 18 Nov 2025 03:00:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:d024e7a9ace7a349e108bfed89c7021c63a8fd4d12fc46cedfffbaebd607a91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5560ccb9c9c052271456caa8d7a8ba073e8641b59fd7fff93445b86f3aa198e`

```dockerfile
```

-	Layers:
	-	`sha256:faaea12705a6391adcbf543e90d84f57a4432885c1a46a9113ba3b11ede2a9a6`  
		Last Modified: Tue, 18 Nov 2025 06:14:10 GMT  
		Size: 6.0 MB (5962846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170b1c71f0ec5a997e30221caae195e293e22530bdc74e7eb2bce349125c1fb5`  
		Last Modified: Tue, 18 Nov 2025 06:14:11 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; 386

```console
$ docker pull postgres@sha256:3590fc4e930914490b6e6f16d035395980ecc114254fc3a1ad53d6f72db487c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a06a4e6ecdd78a440e6c1ee5e475678c12ef6f9ac51c805a12f79cb8b3761b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:40:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 02:40:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:40:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:40:51 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 02:40:51 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 02:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:40:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 02:40:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:40:55 GMT
ENV PG_MAJOR=18
# Tue, 18 Nov 2025 02:40:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 18 Nov 2025 02:40:55 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 18 Nov 2025 02:49:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 02:49:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 02:49:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 02:49:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 18 Nov 2025 02:49:22 GMT
VOLUME [/var/lib/postgresql]
# Tue, 18 Nov 2025 02:49:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:49:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 02:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:49:23 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 02:49:23 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 02:49:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c97731956a1c9cfccde84ed817c1343644bb0d238e2dfb2717fb40fc07f571f`  
		Last Modified: Tue, 18 Nov 2025 02:49:43 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06133043fae6f724fb67c0646592e1fb799fc5529c1753d70d6e6bc1df10900d`  
		Last Modified: Tue, 18 Nov 2025 02:49:44 GMT  
		Size: 6.6 MB (6629550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937bf414beed57f4b428a98a9a53e833cc8a49f353c20f3c5b30665a72d60134`  
		Last Modified: Tue, 18 Nov 2025 02:49:44 GMT  
		Size: 1.2 MB (1225684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5db87a2ca8400f726469f64b04514c37f22c0da38ec6c41c6faa8e5b71d7c15`  
		Last Modified: Tue, 18 Nov 2025 02:49:44 GMT  
		Size: 8.2 MB (8203926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835e98260e9e5549479ea5e7c74a4367ef889754271be0603d0ed627ec089cc8`  
		Last Modified: Tue, 18 Nov 2025 02:49:44 GMT  
		Size: 1.3 MB (1308147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f649c13b93adb7fa423118a662404ad3431f896140fe8f145f54f11c1a0919`  
		Last Modified: Tue, 18 Nov 2025 02:49:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f857dbb1bcf170b687d2474cec3102574f6920042179b9c438eeaa91ae18b1b`  
		Last Modified: Tue, 18 Nov 2025 02:49:43 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61e369aedb9624e0d05ea7c3fcbb981a12d5817fa17a5e47e77e2feded6a8c4`  
		Last Modified: Tue, 18 Nov 2025 02:49:47 GMT  
		Size: 48.8 MB (48821712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da87ce765215a47a37a3d27eba37d2ff3a1f27833e17b5ee42078bbfbdea588d`  
		Last Modified: Tue, 18 Nov 2025 02:49:43 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c284d3f84c987a1e9ddafdbbe066f05d887c97dd5cc134952df99687ee009e`  
		Last Modified: Tue, 18 Nov 2025 02:49:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0264bfaab6408f7ebfc007cc2e4422a4a90b5e8470917f9e4d7e5bedf6dfc4`  
		Last Modified: Tue, 18 Nov 2025 02:49:43 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a98635328aa5fec22c92ed1cfe8d49ae91a17adc8a004064704fcbe5a4c797b`  
		Last Modified: Tue, 18 Nov 2025 02:49:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b5c70a1f32641a863f1a53eafa99cba99f81d0819cc37ff05bf9171be2df9233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dacd23f4e5c8818a1ef4a4cf58e0c12060ae0d8296ff44f10f3813f6b08256`

```dockerfile
```

-	Layers:
	-	`sha256:0d57b1a50291d4a8ab646fcf6472657917f104d8d1e08bc219ce416a370edf85`  
		Last Modified: Tue, 18 Nov 2025 06:14:15 GMT  
		Size: 5.1 MB (5114949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c831c5c1988e10d62605541e559028e341e2402498ee14e5c93ec5c94a5ab376`  
		Last Modified: Tue, 18 Nov 2025 06:14:16 GMT  
		Size: 52.4 KB (52391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:f0248126832abd191da83441477fab0c2c0db9203848abf5bee54b665e3c83a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a161955fcd05194b1cc30b63e3e643ac10e904a22412ee4b99b73e77ef49877`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 16:38:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 16:39:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 16:39:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 16:39:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 16:39:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 16:39:29 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 16:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 16:39:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 16:39:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 16:39:42 GMT
ENV PG_MAJOR=18
# Tue, 18 Nov 2025 16:39:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 18 Nov 2025 16:39:42 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 18 Nov 2025 16:40:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 16:40:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 16:40:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 16:40:31 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 18 Nov 2025 16:40:31 GMT
VOLUME [/var/lib/postgresql]
# Tue, 18 Nov 2025 16:40:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 16:40:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 16:40:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 16:40:31 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 16:40:31 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 16:40:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef330636987142aff961cd20308e2d82b874643a96889acb8fb5ad5c7a25e927`  
		Last Modified: Tue, 18 Nov 2025 16:41:38 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979b3b20969aef2bd2d3d113d2d54c6b72a50e9917bc30998fa04ddff1af142`  
		Last Modified: Tue, 18 Nov 2025 16:41:39 GMT  
		Size: 7.1 MB (7075905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2dabf421e89d0214fb76bdca5ee3a5e4ad834c1d991236a94a650d828922b5`  
		Last Modified: Tue, 18 Nov 2025 16:41:38 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702b1fbe0a6729e22c9ff3496e25114396d5d9ec0784e8a745e27a1462081dc`  
		Last Modified: Tue, 18 Nov 2025 16:41:41 GMT  
		Size: 8.2 MB (8203955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ea89aab51df4b5db18410b192769b21399ad5df25230a99f4148f4b781703e`  
		Last Modified: Tue, 18 Nov 2025 16:41:39 GMT  
		Size: 1.4 MB (1394824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4244c6e87c8c4ed297a8bb3685915ef419ccf53b91455ae728d917eb076990ea`  
		Last Modified: Tue, 18 Nov 2025 16:41:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c57bc51378b73451358792b681dd396c8a362dc67fad5ea9d6e56c2d4a1fe1`  
		Last Modified: Tue, 18 Nov 2025 16:41:39 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d94f0bfc80f1fd4b9dbe1ffb53016a93b6b02818b58a950b020f2cd88e92426`  
		Last Modified: Tue, 18 Nov 2025 18:12:04 GMT  
		Size: 123.1 MB (123110340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdef0645fa73ba83ad1477c4793bd41b57a7037790afed20c8b99832ed124a5`  
		Last Modified: Tue, 18 Nov 2025 16:41:38 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8a5d934ff3389b9526e7433664fc33e9601471b0643c7798da0ecc1d869048`  
		Last Modified: Tue, 18 Nov 2025 16:41:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78327baedc278b6fb8ce8d724a396529e211b12d582edfdea98fbaee22336c34`  
		Last Modified: Tue, 18 Nov 2025 16:41:38 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ef43da994ae2730f17295dd5fab3665aa1e136d18575d41bfc5ebc3076387`  
		Last Modified: Tue, 18 Nov 2025 16:41:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:822c29c5e368787727dca76775f9a38e97671fb979117f6a7ad3f98ed7ae2b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d71dfc210753469e2f638ee2ca5ee938946d5632c1b5c8bfd80718e2a21cf52`

```dockerfile
```

-	Layers:
	-	`sha256:2dec497445984d4bda90309f1f45ac1d29998b206e7bb6a63bcf16015e2abad5`  
		Last Modified: Tue, 18 Nov 2025 18:10:04 GMT  
		Size: 6.0 MB (5963121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0002577536d06960c6d2b0325b06b9f2fd40e91df9e8ab3bac116e390dfeb0d2`  
		Last Modified: Tue, 18 Nov 2025 18:10:05 GMT  
		Size: 52.5 KB (52533 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:6074d7509d78ab7beb660571b7a5ee2d4bbfdb4b9c7829c7c777c670aa7ea9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92795852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49693ba6f8915f0fa339a7300d560a4fb3c4d885dfa67cf8c598d6185fe4013b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 08:53:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 19 Nov 2025 08:54:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:55:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 19 Nov 2025 08:55:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 19 Nov 2025 08:56:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 19 Nov 2025 08:56:36 GMT
ENV LANG=en_US.utf8
# Wed, 19 Nov 2025 08:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:57:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 19 Nov 2025 08:57:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 19 Nov 2025 08:57:16 GMT
ENV PG_MAJOR=18
# Wed, 19 Nov 2025 08:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 19 Nov 2025 08:57:16 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Wed, 19 Nov 2025 11:00:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 19 Nov 2025 11:00:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 19 Nov 2025 11:00:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 19 Nov 2025 11:00:50 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 19 Nov 2025 11:00:50 GMT
VOLUME [/var/lib/postgresql]
# Wed, 19 Nov 2025 11:00:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 11:00:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 19 Nov 2025 11:00:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 11:00:51 GMT
STOPSIGNAL SIGINT
# Wed, 19 Nov 2025 11:00:51 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 19 Nov 2025 11:00:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead35b712ff5d9d8ca52f6d8dc388c182090aeef7230f12c0e05eb3edb485fd1`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805cd2ec0bf25032c615ebe04d2bb38652c5b53a48b1cfed2f4c1fe462fd4b10`  
		Last Modified: Wed, 19 Nov 2025 11:03:44 GMT  
		Size: 6.3 MB (6291335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd9c82f78034dd1233158b2ceed5652e2801f225b1942083ef6387cd103c8c`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 1.2 MB (1201936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331c3a8365f0dfb78f990cc2d93424fd734fd6db628189e19912c9cda7b9b27`  
		Last Modified: Wed, 19 Nov 2025 11:03:43 GMT  
		Size: 8.2 MB (8203629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f1254c0a6888a8b60202100653213d8bfbe16398f19e33ed95324a1058b34`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 1.4 MB (1402267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d3b88ef3c7c5d24295612d9ca59e0997343d09a8c0f13f340dd004f2eccda1`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d88dfc5525c07d975efeddcc1f8cb228ecaa45372166be21dfec30503cf46`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cd9d37cfdda48747727516dc68fa4e51d6429efd63d19fd7fa6ea0041437e8`  
		Last Modified: Wed, 19 Nov 2025 11:03:45 GMT  
		Size: 47.4 MB (47393791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df63348000b699642d5edebbe3e191cb55db46b03d919b6f8938df45865cdd98`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 19.2 KB (19191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e5c1322746fed0e50ba2fa2c031f4fcc238552d8a01eb91ac6e9cdedb19392`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd245c2acac1b93c8bf0f8135347419a2bf66036208da490a4af2cb6aebaeb7`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd98e60c343a91c21d389fb11255d3bd455eced7e4b7ecb2228d5681fc0e04d8`  
		Last Modified: Wed, 19 Nov 2025 11:03:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:d09c3674172f557e57cab13802d49434c9463dc89fb72b74c4057f2d42a614c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fd522c38cc9f33ad041f37e59ede7a255a9366b7003e562800a4ff41c86a6a`

```dockerfile
```

-	Layers:
	-	`sha256:46243f8428b3cd43232001fc1c4990bd512ced40a21dfd4c5ebfba45960d9054`  
		Last Modified: Wed, 19 Nov 2025 12:08:44 GMT  
		Size: 5.1 MB (5109889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82232272833af70934051b7c2c69acbed7300f6108cc1bc88626528bee159cb`  
		Last Modified: Wed, 19 Nov 2025 12:08:45 GMT  
		Size: 52.5 KB (52527 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:163a0c6eee5155af262b63c2f78a43023254791cb2b7fbccff3b54334332aa7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176851574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a53f523e06a163674821d2439474e61b8c519412120ccab93e7a419118a0fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:24:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:24:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:25:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:25:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:25:12 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:25:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:25:17 GMT
ENV PG_MAJOR=18
# Tue, 18 Nov 2025 03:25:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 18 Nov 2025 03:25:17 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 18 Nov 2025 03:37:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:37:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:37:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:37:44 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 18 Nov 2025 03:37:44 GMT
VOLUME [/var/lib/postgresql]
# Tue, 18 Nov 2025 03:37:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:37:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:37:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:37:44 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:37:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:37:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1da7a00bc065972ff7a0cc172ae5aeffd57460e2d8201e7ca7f11c9f3d91f81`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640b0fe0d4888a2c7a19f141461a945d052f3d4237638800abe357409191335`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 6.4 MB (6408826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934d38de3ba60840502809b113b390285df853744e380bac937d7872e57ea94`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 1.2 MB (1230102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548d3e72f4a5f82cb7897c75bf9446844f4c0ed467f8c875294c35e3bb31376`  
		Last Modified: Tue, 18 Nov 2025 03:38:30 GMT  
		Size: 8.3 MB (8258828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896924454e3ca726939ac8bcf6bb15537624f9271e53887928e29f4e4b812e6`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 1.4 MB (1398066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2d8b2fe721daccd41d2fc57054b8090f304d9d4f5e26f0432cc917aa23ffd`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5b90033baa0840a68a94663b272baee694f3df08e730e0dc5b0c3f76be23d3`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f8bb68f5c688dd15faca5a67c9d0265253a01ca4206288a61ba25106e50c5a`  
		Last Modified: Tue, 18 Nov 2025 06:16:14 GMT  
		Size: 129.7 MB (129691613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6810118b55b18e7e56c2166f90e6b7aaafa66371fa4c33d98e8be7a37faf2427`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 19.2 KB (19187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11152393322b95e3059a2eda81a0e0eb4a1e44888df145c83802e6817bd8c71e`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8487d71f785ff34c2c9e0fbcee50b881efeecb6294b024f9708ecbd8d0054d5`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb824386348553f45261d14a475608f591d431206bec4aefaacb0895c7e13fa`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:34baa710f123ade0061ffe317f04c66476067c2a6f693ab83932ed0c6c105fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2496806957616563e181936c4cb9de78f880fbabada99efa40d935fa7064c9`

```dockerfile
```

-	Layers:
	-	`sha256:8b9ae575c591f2df544edeb804fdbd4f2755bb112a86738c5eea763a9f2a29bf`  
		Last Modified: Tue, 18 Nov 2025 06:14:27 GMT  
		Size: 6.0 MB (5973143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb805e414c97811b4997ebeaeb3e947bd07448e2ed93affed716b891ca2ddb81`  
		Last Modified: Tue, 18 Nov 2025 06:14:28 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json
