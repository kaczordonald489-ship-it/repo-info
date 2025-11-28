## `postgres:17-trixie`

```console
$ docker pull postgres@sha256:f337b026cb1fb954a93f2e33a62bf9ea7fffc1dafc1586c53b93922a8d6ee018
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

### `postgres:17-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:43735280d1873da7ac9b6e7872b09c34f6d19283fd5f42f3fc22c982fbb0c0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161107071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a127a08802295197bb05018f8fdb08448a2e480405a81fab08d39f86fcc6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:58:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 04:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:59:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 04:59:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 04:59:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 04:59:06 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 04:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:59:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 04:59:10 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 04:59:10 GMT
ENV PG_MAJOR=17
# Tue, 18 Nov 2025 04:59:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 18 Nov 2025 04:59:10 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 18 Nov 2025 04:59:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 04:59:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 04:59:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 04:59:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 04:59:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 04:59:24 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 04:59:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:59:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 04:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:59:24 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 04:59:24 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 04:59:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c3a0b6e4a1904a49991c013dc5d9f834a6ac69310e4268a9b91e4c6a794d76`  
		Last Modified: Tue, 18 Nov 2025 04:59:58 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e478d205dee0d433928cd1665bf5f811af3019a9dd130d60b52d4bddc4cc4`  
		Last Modified: Tue, 18 Nov 2025 04:59:58 GMT  
		Size: 6.4 MB (6436615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bbd93c1b3ad800428fccbe69f050c383b08c419f23e5d5958c29cc2f920f6d`  
		Last Modified: Tue, 18 Nov 2025 05:00:00 GMT  
		Size: 1.3 MB (1256604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769571c5e085ce2b459d399df5ae7f04c43a7e18adc502c501e0f4e5d14847ab`  
		Last Modified: Tue, 18 Nov 2025 05:00:01 GMT  
		Size: 8.2 MB (8203766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbbf8d9cd9a04bc12ead3bf47713757c4ccc665a1774ca892c441df832a46de`  
		Last Modified: Tue, 18 Nov 2025 05:00:00 GMT  
		Size: 1.3 MB (1311503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07419cbc1defd2d10c8aa451a43e6658e108c602a3d12ffecf2c542a888ce408`  
		Last Modified: Tue, 18 Nov 2025 05:00:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de07d70bcb59efa26a39ec82965ba2e7a9089b48ef0bff7c5b75315f6ca7d1c2`  
		Last Modified: Tue, 18 Nov 2025 05:00:05 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc424475cfc6fb0937d40196cf715f32dbd4429c2247d2626b8bb3044c01f7b5`  
		Last Modified: Tue, 18 Nov 2025 05:00:30 GMT  
		Size: 114.1 MB (114101021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19509f484f728b932a6ceecb95dbf528597796dcd212670149265361cb1326`  
		Last Modified: Tue, 18 Nov 2025 05:00:01 GMT  
		Size: 10.3 KB (10335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a100eb7d0497f6216567bc618c4aa733112d68359f4af6da695a71555456ab`  
		Last Modified: Tue, 18 Nov 2025 05:00:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eee89b4fb96932a2a8cb2f1acf867b7a84adceb3b850d12260994505fd02c85`  
		Last Modified: Tue, 18 Nov 2025 04:59:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b78d4ef75cf5afef75b67b73ce647f74e9cfa7c087e35d2eaa9e32fe274d8f`  
		Last Modified: Tue, 18 Nov 2025 04:59:57 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c93448ed1befd257d77265af1674ecc5a166da0d623a178595ccde6b053b5`  
		Last Modified: Tue, 18 Nov 2025 04:59:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1111b3b7fc604edd195ed1e7890245333146698d7f57a895030892a5d79ce00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5780212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e675b8aacb37e6fe166fdc4672ded6af4e594ec8173bd3352d0907e52e95c3`

```dockerfile
```

-	Layers:
	-	`sha256:5e3f7bc40542cbaeb0c843f39171a60c64880c8e9bbda47a3ceb1969da3c36dd`  
		Last Modified: Tue, 18 Nov 2025 06:12:39 GMT  
		Size: 5.7 MB (5726354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:584b41c79b88a0e724b3e930cbfcde68e916705ca3850d525ba22b75dff02fa4`  
		Last Modified: Tue, 18 Nov 2025 06:12:40 GMT  
		Size: 53.9 KB (53858 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:2c20c241d334d36bacc6b66889156ee282921e3117d874b59733a187a678ed9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155161371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dcf27885ad3cbebf02d7eccbf24c1adfb669765f846ce66ed97928ad3fa8d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:03:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:03:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:03:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:04:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:04:05 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:04:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:04:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:04:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:04:13 GMT
ENV PG_MAJOR=17
# Tue, 18 Nov 2025 03:04:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 18 Nov 2025 03:04:13 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 18 Nov 2025 03:21:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:21:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:21:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:21:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:21:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:21:20 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:21:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:21:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:21:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:21:20 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:21:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:21:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0092977ce4c2116d2e8250277d05e087ff760df3fa490fea4430facac0015a`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c23053788c9800490e85687a3ad0eb175582757cc4de11a8eb2c11fe16038e`  
		Last Modified: Tue, 18 Nov 2025 03:21:50 GMT  
		Size: 5.9 MB (5929033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a038060ac06c08e969afc31cb23112080c2ddbbff422775aec56023c761faf`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 1.2 MB (1227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a256425e48d436c735143fc7ee8b8b8a54d2d1c118e40af402da0c65c4a540`  
		Last Modified: Tue, 18 Nov 2025 03:21:50 GMT  
		Size: 8.2 MB (8204179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d670e89a21c372ac6c6db957481ad8881908f5fb406c9a23146f2eb626fa79`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 1.3 MB (1317188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeee77f19c1efd1157962b1eea74f81bad88e59c4beb40c37ebc14ce09708303`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee3c983f2ceb484e024e6f032afe8204e8a91b2d639513185fff482469399e5`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4723cc7e03a1c2ce67ec1e73eb505438584577ad00b80da4b0c71a7e7eda145d`  
		Last Modified: Tue, 18 Nov 2025 03:22:02 GMT  
		Size: 110.5 MB (110518358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c6e313f78a087c9f4bfef7d067d76a0622202b5df7fdcf5aa294a4bf176768`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 10.3 KB (10322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d74bb570d8e8341b1a29640034ffb65009be33f1d8df558db94905f084337a`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7761aa54397075f0c6b70eb60588287a1a97f7f3b8b5b868b21faded66bfc`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2c55fcacdd2d8d69edb6e786246d1447f1c82c26da78c49dc43bd0e7100c92`  
		Last Modified: Tue, 18 Nov 2025 03:21:49 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75917b8f0a0fb818562b1070dc9b0c13148b6d0d344f95357501700b3ddb80`  
		Last Modified: Tue, 18 Nov 2025 03:21:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1b1deb6fa78bedb7f5e80751cb611dbc81fb28c25ee4a154accf5c592b7f9be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1230dc3f52843d4da139b8f002c420d8ae14207d7c8345e6fa7394e2332427a0`

```dockerfile
```

-	Layers:
	-	`sha256:9776b54a2bdc2a0c193bf7db864e2c7f869d9b57a868d3b92fcb00484a04de6c`  
		Last Modified: Tue, 18 Nov 2025 06:12:45 GMT  
		Size: 5.7 MB (5741272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791fc72c5522c237be67e0f6c776ede338a39ad3231fd809c9b8945149604d1f`  
		Last Modified: Tue, 18 Nov 2025 06:12:46 GMT  
		Size: 54.1 KB (54083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e56145781a67276f425fa202fc2f7dfe9ac5dd9f29885325aaeb0da0bcc7ef4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150196925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17d364d19c5465fa5afe03f68cc2c56412c10875a0d5f1b2994f4f76a197ba4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:25:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:25:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:25:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:25:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:25:40 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:25:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:25:46 GMT
ENV PG_MAJOR=17
# Tue, 18 Nov 2025 03:25:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 18 Nov 2025 03:25:46 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 18 Nov 2025 03:41:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:41:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:41:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:41:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:41:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:41:11 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:41:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:41:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:41:11 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:41:11 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:41:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d997fcf5f6e5b2da0fbd78f8e4fc913e65e3a84482341c3a8329068016757c1`  
		Last Modified: Tue, 18 Nov 2025 03:37:36 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1aadbd07854efd765a1210559a4fa35bdf71443a493ca8781ca4e16bdaa5a1`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 5.5 MB (5496787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ce3a6c5e4219a8ea14c986394173fec8ab784ec29fe8335f19788abdbf76d3`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 1.2 MB (1222268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793bacd8f8b659f965e049b0b8faf3baa11e199ab973bb9f37abe6a36a00e633`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 8.2 MB (8203920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb623fa52e6b6878559f13544e8ae4b1ecbcd17d5aa8f4076befae4de1d3e4aa`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 1.2 MB (1172443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c01433b425aa2bfff49097b67a7083b2172d46e09b94ab0d71c45c9b1256064`  
		Last Modified: Tue, 18 Nov 2025 03:41:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026778fe50851397e201591e2c490376e8243586d137873ac1d0d923575e8c43`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128da7d98a79ee5bfae779cc461c02e06d395fdc7745a15b362b3cd7d97cd530`  
		Last Modified: Tue, 18 Nov 2025 03:41:47 GMT  
		Size: 107.9 MB (107870451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e87c1f0d839c72c536bf5d95e166887fb4c017711e6f6d699e1f7dbc41aa5`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 10.3 KB (10348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d8e9e58fc92be557195fb2ce9ed0deac05292b16ab1548b609eeabc7e964d`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a73dd982a167bc55ecc00bea8aa7dab7947cc957952fe69ca9cf32a230c1294`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e615ab54f6b991c09964456589b91b553ebc1284df7983fc2a3b9b85448672bf`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665f64681d306a42ead546010d95fb5fb9b8ed73c99be2087c7747e25af7168`  
		Last Modified: Tue, 18 Nov 2025 03:41:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:14defd1b293e0a60d37020bd95a3da1818943c40fd4108afdee84a204c9e564a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a4bae6270f9ba34f0f23b8c40bf091418a197b845e0ef7c7bdb64ee526b7ca`

```dockerfile
```

-	Layers:
	-	`sha256:19d1fbd4575debf460ac0f1ab09577efb4159bc7fd5d6d00a1581d96f7f530ab`  
		Last Modified: Tue, 18 Nov 2025 06:12:51 GMT  
		Size: 5.7 MB (5740577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b5cce0bcbd30157aa243ab711123e0b89c3256c25ba4393f5ce64ae0c3ff85`  
		Last Modified: Tue, 18 Nov 2025 06:12:52 GMT  
		Size: 54.1 KB (54083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d69415e0f775efef1c3f151ed057ac26c0e795f2fac7c8088198b83d7399fc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159741248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ab9aba0ba972c3b0e10a2b65ab3b7bd7c37aac319058d0b8a615886b5da620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:00:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:00:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:00:53 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:00:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:00:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:00:59 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:01:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:03 GMT
ENV PG_MAJOR=17
# Tue, 18 Nov 2025 03:01:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 18 Nov 2025 03:01:03 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 18 Nov 2025 03:01:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:01:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:01:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:01:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:01:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:01:18 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:01:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:01:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:01:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:01:18 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:01:18 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:01:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d17fe4acec113730a92ebed00bd921c75d9aa91e0e42e8af1b4f03ca098cc9`  
		Last Modified: Tue, 18 Nov 2025 03:01:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c53429f641f803004e27bbcbc7dd81f6926c76e79d6d328dfd2ff57eac5d0b`  
		Last Modified: Tue, 18 Nov 2025 03:01:49 GMT  
		Size: 6.2 MB (6232050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f754016195edccfae6219fb8525af226f2bab07b383dd0bea731254f8f36ef0`  
		Last Modified: Tue, 18 Nov 2025 03:01:49 GMT  
		Size: 1.2 MB (1209451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcbbfe2f67063c9f17e629b23b3330cfccce0be85ead340db3e3270dfff0b0a`  
		Last Modified: Tue, 18 Nov 2025 03:01:50 GMT  
		Size: 8.2 MB (8203921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380228cbdaec1a44b4f3ca5250d757a61b6fb9e5c02649b0dfa633338fe82a84`  
		Last Modified: Tue, 18 Nov 2025 03:01:49 GMT  
		Size: 1.2 MB (1220459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60a2f9cfbea80ff093136c41adbb666b6426bd22cd5c615f8af1a256692dcbc`  
		Last Modified: Tue, 18 Nov 2025 03:01:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45294d2678249c2625e837d46a0689624dd8bddec5af2ca9423d1ee84d44eec1`  
		Last Modified: Tue, 18 Nov 2025 03:01:49 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5068eb119576af136a696a3cc2b073d616581b6669673deea47febfadade347`  
		Last Modified: Tue, 18 Nov 2025 03:02:06 GMT  
		Size: 112.7 MB (112715685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3924e7191257229f6872b0c36968708ba85deb3564768cf7c2f752be27a6f082`  
		Last Modified: Tue, 18 Nov 2025 03:01:49 GMT  
		Size: 10.3 KB (10331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd65c8eb7763ea0642ee79dcfce65019f24be9244f06fd920b7713b19e9a225`  
		Last Modified: Tue, 18 Nov 2025 03:01:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb663e24ca0372d853be787bfca5dbea05ddb94cc33a3f06f9f1801c882f496`  
		Last Modified: Tue, 18 Nov 2025 03:01:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5506ca1761fbf789140353bae08b5870dfb10fc3e34ef67dbd0a27950bb9bb`  
		Last Modified: Tue, 18 Nov 2025 03:01:48 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09971469dc6af5beaa0e61139a4a863ada813c6d8b7d135725012e337e9fa2b3`  
		Last Modified: Tue, 18 Nov 2025 03:01:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3377dba89f5d66ad4c4bed1910281f1eb2f57b1ad24b23d4c031585f544233be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5786829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68927c76530585f00b71cfb9d20f822acd8141678938514f96b1087ba73147c7`

```dockerfile
```

-	Layers:
	-	`sha256:cdbad79553c521fa8048a95c70ecf9150e4edba5e7a4312aa38ad062675386f2`  
		Last Modified: Tue, 18 Nov 2025 06:12:56 GMT  
		Size: 5.7 MB (5732700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f3ece7b9a34f4a5823ac935b43a513c0918a530dd51939d5475219b469c74`  
		Last Modified: Tue, 18 Nov 2025 06:12:57 GMT  
		Size: 54.1 KB (54129 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; 386

```console
$ docker pull postgres@sha256:c24627df11fe0b1b8e701f9ccc442615ad77b17168e55641dcd7ca36e3122d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170303287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9004ca7fc57ec19e441149a1e6340c0dfc33050056a35aaefeb2275b9fcf88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:41:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 02:41:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:41:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:41:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:41:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 02:41:35 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 02:41:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:41:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 02:41:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:41:39 GMT
ENV PG_MAJOR=17
# Tue, 18 Nov 2025 02:41:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 18 Nov 2025 02:41:39 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 18 Nov 2025 02:52:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 02:52:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 02:52:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 02:52:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 02:52:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 02:52:28 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 02:52:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:52:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 02:52:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:52:28 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 02:52:28 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 02:52:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a6ecf84e6c419a79c39c9189879679e992cf6fcf4d3b97b115817f5c7bc4c`  
		Last Modified: Tue, 18 Nov 2025 02:52:58 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1315cc1270a16f4f255b699f06a7655d678522d773f14c2ccc6620a7f3e39c0`  
		Last Modified: Tue, 18 Nov 2025 02:52:58 GMT  
		Size: 6.6 MB (6629617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f690be117991765e9a23ac75a37b195802e4125e5f0e8bb54d623b8f3a70b35`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 1.2 MB (1225690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb0b3b2bb2c75ec21f84966e4e4cb6fde92ea52129e0154e2bdf46d6f3db995`  
		Last Modified: Tue, 18 Nov 2025 02:52:58 GMT  
		Size: 8.2 MB (8203954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70e2dc2ee1a920c0c5981164fab32b97721d7e08260a9bc2a3111bc8b8f6853`  
		Last Modified: Tue, 18 Nov 2025 02:52:58 GMT  
		Size: 1.3 MB (1308154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5970904743ddd4d70b0d64e11d8dc0c74810f8af83ef54a4f3c5d93da1f98ecd`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec992c9df90d385d444c0a31460ad262ebf68e4b91d839ede4a73e78e8cd5a8`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b568426be26b0ae22f62cd7ad478a5346d305cc01afb71bde827e0a00161d5`  
		Last Modified: Tue, 18 Nov 2025 02:53:07 GMT  
		Size: 121.6 MB (121621726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc83333b503cd2d95148102fdeacfba025dc4fa65e335a64ce3a287bea54d37`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 10.3 KB (10330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d481819883a0dde151b149398c11d9b04af8ac54d44c39c1514bd49a6c3582`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aaa4d7e5090a4c6d3f3de9b7de123688d82b972a268d15bcf9e8e181978a17`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a5dd753bba34ac84b4f68415db3a63b58b606acea9c2d777c3c2f8400c6c49`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abd9f4390a3411604af93f730d8b52b88ab18741d35c35f93c9c59f31da16f8`  
		Last Modified: Tue, 18 Nov 2025 02:52:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:30a959c238446e5e89d3f9426f24381fa4d83637940424bb865ddbd61e796900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8abeabbedf3b25662e502d727bebef97af7c393259f676050c6effc1963786`

```dockerfile
```

-	Layers:
	-	`sha256:6054962d1e59d8c45661c02218ffdab9c6c7941a1bcf4a83e29dd90c6e146541`  
		Last Modified: Tue, 18 Nov 2025 06:13:01 GMT  
		Size: 5.7 MB (5740165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac1f388a106f34ca49905dc7ea3d4aae110eecc7a71013eedefbb2d46aef24e6`  
		Last Modified: Tue, 18 Nov 2025 06:13:02 GMT  
		Size: 53.8 KB (53806 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:7b210c189eccb67cdaa44645adfde95dc7583526fcea2301e91ac4aae38b22bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173449934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b745344f86d163362e454bcbcf5b15f421084d746e104eb2150a4a199d6f1e43`
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
ENV PG_MAJOR=17
# Tue, 18 Nov 2025 16:39:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 18 Nov 2025 16:39:42 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 18 Nov 2025 16:42:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 16:42:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 16:42:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 16:42:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 16:42:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 16:42:43 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 16:42:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 16:42:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 16:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 16:42:45 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 16:42:45 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 16:42:45 GMT
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
	-	`sha256:c2f6f4ac94a9224dfda5ddda920b2ca05de4c61a17a78526c20a57e6eb8a3494`  
		Last Modified: Tue, 18 Nov 2025 16:44:02 GMT  
		Size: 121.9 MB (121942617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607e5e6e16a98bc61ebc3f021ba036372298d15e870c54372b6a077d40cefce4`  
		Last Modified: Tue, 18 Nov 2025 16:43:47 GMT  
		Size: 10.3 KB (10341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a1b321b07594be2cf172b022c18a395de0e2282c31263e3c1b6aed9b95047f`  
		Last Modified: Tue, 18 Nov 2025 16:43:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d271a2ba339666c343ebd23cb53b46448a3c5633da3b31e7fdf7ec3cbc0d2d6`  
		Last Modified: Tue, 18 Nov 2025 16:43:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef312a49484b55761be3837ee13a6d2008419018a3261c2bdeb30860815853d`  
		Last Modified: Tue, 18 Nov 2025 16:43:47 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c8d5c7dbc247983d24471fc0021ae896a7cab918ee9349019f1332b9d5df3`  
		Last Modified: Tue, 18 Nov 2025 16:43:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:64eed99f5470caedabfde44142b779a95b8e293f309b95c98797ed6bee44fcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5786893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e04e0b60eeba80866a527123591c5c7dbc0e75bf4fbfea1b4d35331f33ff32`

```dockerfile
```

-	Layers:
	-	`sha256:d9576d6e28db098ee2079764bf1cdad234ee3f7cd3ca7bd7ad5ed283af3761a1`  
		Last Modified: Tue, 18 Nov 2025 18:09:32 GMT  
		Size: 5.7 MB (5732967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c19c7df5833a0d15d7b66d1d79337447dbb2bd3d7650315a1555a72339f024`  
		Last Modified: Tue, 18 Nov 2025 18:09:33 GMT  
		Size: 53.9 KB (53926 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:6c1a36469455e10a8e2442c1bb131893c347343c16c714cd1114f8e89d202329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92208865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f205d09325452e153947ec1d5d9abea6393c5136a65728976a29f7a72c3ad319`
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
ENV PG_MAJOR=17
# Wed, 19 Nov 2025 08:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 19 Nov 2025 08:57:16 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Wed, 19 Nov 2025 13:12:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 19 Nov 2025 13:12:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 19 Nov 2025 13:12:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 19 Nov 2025 13:12:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 19 Nov 2025 13:12:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 19 Nov 2025 13:12:45 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 19 Nov 2025 13:12:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 13:12:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 19 Nov 2025 13:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 13:12:45 GMT
STOPSIGNAL SIGINT
# Wed, 19 Nov 2025 13:12:45 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 19 Nov 2025 13:12:45 GMT
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
	-	`sha256:a56a260dbfe74782cb0c39b748c6811d1500803f200a07c81d37e30d1595665f`  
		Last Modified: Wed, 19 Nov 2025 13:15:30 GMT  
		Size: 46.8 MB (46815484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7f212403b3b006eabe19c9b36b92cf34cf0f1397c4b12a7d72bd5d5cd275ae`  
		Last Modified: Wed, 19 Nov 2025 13:15:26 GMT  
		Size: 10.3 KB (10344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aea4d2785a6206bbb931e41dc7c4ee1d796a6fe9f6554576f76a204eef3ff8`  
		Last Modified: Wed, 19 Nov 2025 13:15:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950b2636aa08f9f649119f0026463a08ac61032033c8ba735e7abdc17323ccf7`  
		Last Modified: Wed, 19 Nov 2025 13:15:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881c560435c8427c1d616faf6ef826019ed16b5ce6c29cf88d272a4155302ed2`  
		Last Modified: Wed, 19 Nov 2025 13:15:26 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73439dfe8f915b67ea4bb3ff57920fead713361d79d2eb61fd64d72d5697a3bd`  
		Last Modified: Wed, 19 Nov 2025 13:15:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:441236b65b55e059e4a3d41a5e5c99af373ccc63beb516ef19a9f1cfb986faf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e23dc9e4e537833fb5074fcbb8526b531412a63ce664e24f175571496257fe`

```dockerfile
```

-	Layers:
	-	`sha256:925745e36aefc162e37866ea9160ecdbae6fba52b09b69beb2e205740e07ef12`  
		Last Modified: Wed, 19 Nov 2025 15:08:30 GMT  
		Size: 5.1 MB (5083630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d6039aff07e906cdf7b04bf54c0967d8658e4e704b19fda5da1378c6042e6c`  
		Last Modified: Wed, 19 Nov 2025 15:08:31 GMT  
		Size: 53.9 KB (53920 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:8a44d634d230c61fb71602d76dfd7131e386919bcd16f4ab0860cdab18af8cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175700898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e64ad8c3618f8590e0a136421139e2cd47d7eb33439edd65470233a81f209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:27:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:27:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:27:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:27:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:27:54 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:27:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:27:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:27:58 GMT
ENV PG_MAJOR=17
# Tue, 18 Nov 2025 03:27:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 18 Nov 2025 03:27:58 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 18 Nov 2025 03:40:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:40:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:40:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:40:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:40:08 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23fc6c717395f30fd5dd5cd10b4713bccbcb613df9ccc531648b94c115e48c0`  
		Last Modified: Tue, 18 Nov 2025 03:40:49 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cca155612d52832aa5dc931cb925c1d3b451f95e79246c8b8004db36fbe50b`  
		Last Modified: Tue, 18 Nov 2025 03:40:50 GMT  
		Size: 6.4 MB (6408814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f016b19deb2a37f6144b6a442e5bb6b371178f4f7421f1cbab36554cf29cb`  
		Last Modified: Tue, 18 Nov 2025 03:40:49 GMT  
		Size: 1.2 MB (1230082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe03a4c23694b20e5b96e79121768de11ad2453eed2f0f9e933009b599a02e85`  
		Last Modified: Tue, 18 Nov 2025 03:40:50 GMT  
		Size: 8.3 MB (8258846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8c4cc6577f8a20ae09204661b60e0c0096a3e99d3753ba569993548e2edfdb`  
		Last Modified: Tue, 18 Nov 2025 03:40:49 GMT  
		Size: 1.4 MB (1398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdedda712dc521addad996e185958dc089caf7b7ab5867ef257ff2baf39660a`  
		Last Modified: Tue, 18 Nov 2025 03:40:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685932178ce2b15915eb48c4f2b7202f083595d8ab6ac22d0d6c6cdedc31892a`  
		Last Modified: Tue, 18 Nov 2025 03:40:49 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43681a6a52d199f15e3fb1328445b5bcd37c1d38fa2934123adf553947ef52`  
		Last Modified: Tue, 18 Nov 2025 06:18:15 GMT  
		Size: 128.5 MB (128549650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c755058ef7a2d6827349c6d24a73aa162fb414e6c86bbe821dfc1c6c5ea3870a`  
		Last Modified: Tue, 18 Nov 2025 03:40:49 GMT  
		Size: 10.3 KB (10326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b0b1ea048ebae01e7d3af5fbc7227d4360ed8c16ff46632a228cb6d3eb0e9`  
		Last Modified: Tue, 18 Nov 2025 03:40:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce0178d90cd6524cdffa9d14c659f3b3c605d3b9b198fb233df6f6f0cc5f017`  
		Last Modified: Tue, 18 Nov 2025 03:40:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1469b709d02f4c3a8793c98b1ac2ea30c8e40eec505e4a495114fba5152b6c9b`  
		Last Modified: Tue, 18 Nov 2025 03:40:50 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143633a282ed3767d8e4c2f3ed6f2c3617545ea491651ef7c1a31060179aaeb5`  
		Last Modified: Tue, 18 Nov 2025 03:40:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:67a1b26ac2cd38b3a28afa6cb804265214d3362be1ebf1a590af11b187a8ef09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9babcb529c8ccea23c96d1052efd95cea9723fcff443d11b2afc9a9eb5d4434c`

```dockerfile
```

-	Layers:
	-	`sha256:0e19c54ec8edaea113609d6a31b644a092eeb8690c730479a4a65fc3a744680e`  
		Last Modified: Tue, 18 Nov 2025 06:13:12 GMT  
		Size: 5.7 MB (5741303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc884e37f2c2a28767c6a3a615815bac978cc9204c6dfcad0b1e94360c7a5a7`  
		Last Modified: Tue, 18 Nov 2025 06:13:13 GMT  
		Size: 53.9 KB (53860 bytes)  
		MIME: application/vnd.in-toto+json
