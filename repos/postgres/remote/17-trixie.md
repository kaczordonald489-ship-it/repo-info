## `postgres:17-trixie`

```console
$ docker pull postgres@sha256:4493696c5ba6a9cd4a3303411d5dd6af52cf5e34cdd87ba8ebf26a19735f84d1
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
$ docker pull postgres@sha256:030da09481c3876b71a7e49738a932e1c18c398201a1e4ccfdbff1e5a541215b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161112580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2f8e0ad2949b4e100456f138b1184fe58cb2010cd7a9721008abb87f501458`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:38:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:38:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:38:27 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:38:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:38:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:38:32 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:38:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:38:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:38:36 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 02:38:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 02:38:36 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 03 Feb 2026 02:38:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:38:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:38:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:38:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 02:38:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 02:38:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 02:38:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:38:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:38:51 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:38:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:38:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6d6da846e903fc71efdb4cd9c96f0d2946722b005069581b56c571ec1bd06`  
		Last Modified: Tue, 03 Feb 2026 02:39:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e73123a8202ebe9f84d6bb9efbed16eaf36cf5f020537098b8d0bb60c05d496`  
		Last Modified: Tue, 03 Feb 2026 02:39:12 GMT  
		Size: 6.4 MB (6437948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb6e6454401c12b9b8870a9f4d949ac3a35862e44553558c249ca718cc351c6`  
		Last Modified: Tue, 03 Feb 2026 02:39:12 GMT  
		Size: 1.3 MB (1256753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be8671e729e914b34117ff76d53bc34672b8c39204a0a839249e8509b42e739`  
		Last Modified: Tue, 03 Feb 2026 02:39:12 GMT  
		Size: 8.2 MB (8203844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9211fd3e1a60143bf6212257934c1536acb77a3343a0a1e3a63c7bb40acf9b`  
		Last Modified: Tue, 03 Feb 2026 02:39:13 GMT  
		Size: 1.3 MB (1311636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8cfcf27c7a0ff63739bbdd9b52ca7ee7e607746b7491432595053b297803f5`  
		Last Modified: Tue, 03 Feb 2026 02:39:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18c8e97cb312d32a926435b7aba106d7d90c0a9b302c068aaab07d033b869c`  
		Last Modified: Tue, 03 Feb 2026 02:39:14 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65758d82f26b00660531a6809d4317bce136ff999b867e600be05b271facb3e`  
		Last Modified: Tue, 03 Feb 2026 02:39:17 GMT  
		Size: 114.1 MB (114102712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3e8313a980332463f35daa2f356f2cde8197014d047a486c238f657c0e8187`  
		Last Modified: Tue, 03 Feb 2026 02:39:14 GMT  
		Size: 10.3 KB (10344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9be5b309347560dfbe42a02f83c0ced92a447cdfe7e33e140dbe50b819da22`  
		Last Modified: Tue, 03 Feb 2026 02:39:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63efc7efa2e5a39d4207cc7a7deac39040f915d6d1bbfaa4641c5361f9d12f9`  
		Last Modified: Tue, 03 Feb 2026 02:39:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1dbc12fcae5e31daa82a88e66169aa84cb36756f10292c1cf0a122470e3547`  
		Last Modified: Tue, 03 Feb 2026 02:39:15 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff421dac2937fea159366226b8d6cd89fb8b4bf82ef3d31b7a08c0a930ea411`  
		Last Modified: Tue, 03 Feb 2026 02:39:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:10c6339a1fa38e1cb8fdb5ce50cf4ec1e3f4606fa811562288d2923ac43275d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5780492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6298506909b9228fa226ca7d7421c61e61600640bb8ad7b18544aa15e4d869`

```dockerfile
```

-	Layers:
	-	`sha256:73566c509014e13ec252ef8980574915386a0a556269468f9dcba88a54adc4ef`  
		Last Modified: Tue, 03 Feb 2026 02:39:12 GMT  
		Size: 5.7 MB (5726632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42c89b521da6668f89b09c10b51c2bd260f204620f4f6c8d1b303594866f424`  
		Last Modified: Tue, 03 Feb 2026 02:39:12 GMT  
		Size: 53.9 KB (53860 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8536eae1102a2d22ae3479cbec1ba1bab6dd18945844dad5d81181be67b6934d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155156123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c96aa37db4235d252bc42175d9ea059bc6ca1fcfa73883b8f225ed314001a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:53:58 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:54:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:54:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:54:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:54:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:54:27 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:54:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:54:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:54:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:54:34 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 02:54:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 02:54:34 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 03 Feb 2026 03:11:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:11:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:11:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:11:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:11:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:11:25 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:11:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:11:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:11:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:11:25 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:11:25 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:11:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061dad571a7d4290fa1bd136d7c84674effbfbbec6f621b9d61e90458ecbce53`  
		Last Modified: Tue, 03 Feb 2026 03:11:43 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e20c6446abcc8778b808c3dd9c730f4cd577f7375a3eae9eec5d54a2a91763`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 5.9 MB (5930431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fdf9420bc3325594f936fdad1f18e41ef2a0fa39ff54053d3b045b596eb5c9`  
		Last Modified: Tue, 03 Feb 2026 03:11:43 GMT  
		Size: 1.2 MB (1227500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bb55acc69c919ff8c0b21aaf661246a8a477404b6860ea64edefa60e56d658`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 8.2 MB (8204185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41aa9e1995e37e5c77d914d6e5367af72071c7bd164367d59f6c3e843aea5b6e`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 1.3 MB (1317302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d49be92060fe7a82200dc78e90d0bda20ad7f1ebdb988c1075d50bd9e78deec`  
		Last Modified: Tue, 03 Feb 2026 03:11:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6debd3987dba917b313fda646a8dd7f148b00a84420214ed1a69bcc863bcda64`  
		Last Modified: Tue, 03 Feb 2026 03:11:45 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b500212066bb0019b12c8ee788570425cb7fbba96e8984009180d818e0535`  
		Last Modified: Tue, 03 Feb 2026 03:11:48 GMT  
		Size: 110.5 MB (110508066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd75e20684c57969f8ef3632d8afdbd85e7dac80df27fd7b0af5c7cccef82383`  
		Last Modified: Tue, 03 Feb 2026 03:11:45 GMT  
		Size: 10.3 KB (10332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a11dba53ef40096110e1f875f2fffe66836ed1a7dcb36b9f6f3da2eef9599ae`  
		Last Modified: Tue, 03 Feb 2026 03:11:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7458441670901bd0dd1c50368739838daf4933039716ff500e613a9e98efa`  
		Last Modified: Tue, 03 Feb 2026 03:11:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cea84ba8b87cc1771a72d9603e348eebe35012675d6a7d60119c3e697aac4a9`  
		Last Modified: Tue, 03 Feb 2026 03:11:47 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963b18d65b0e74c26d9c36d1d78a65326625e95654180af4a340fe658acaec58`  
		Last Modified: Tue, 03 Feb 2026 03:11:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e6604fcc14302154f1fdf89ad822b8950900b4595a63de88daa06527de2a4939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf01e39051941093a39934a5cb16de7fa94cbf159048695575c03b742caaad0`

```dockerfile
```

-	Layers:
	-	`sha256:340bc60ae3dfdd7fbe84046841970c602f4a1747a09ee5d495c6ad4fda1240c6`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 5.7 MB (5741550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae623535af3ad877bc9c4c7c84c808aea70235b04969d0df0e6559fe2243d55d`  
		Last Modified: Tue, 03 Feb 2026 03:11:43 GMT  
		Size: 54.1 KB (54083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ccf5ba4d7154d417e50ab3657a33982dfec850c7b1f0d673814507a085b4bb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150198471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20130631402dd6a7686c9dc2faa9d05b25ecb606e9b60aeff83b2fc754ad06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:07:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:07:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:08:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:08:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:08:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:08:12 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:08:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:08:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:08:18 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 03:08:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 03:08:18 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 03 Feb 2026 03:24:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:24:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:24:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:24:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:24:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:24:20 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:24:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:24:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:24:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:24:20 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:24:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:24:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75395a7d483d190238ae1601a661d87a6bfe4eb7e00dd86229037bc72ab10f`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85597644e4a69e5065fc0c6d5ebd0515757f69a15aff6c9788e0a82d0164ff1b`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 5.5 MB (5496523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa851e95ba8e838a4e95b42e82a526e3975888da1d5a9a0a7ce915b2fcb8baed`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 1.2 MB (1222420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efa8dac1c715a3bf9d20ff8b002f6f8d4eb56118ebfde8a5209cf13eb8d251d`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 8.2 MB (8204020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3ec30476ec60cabacdeeea7c20da9127ea24dd452f475215ffd933c4ba0911`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 1.2 MB (1172587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e0d67bb16b0837212551cffdf42a057e1fc90107f89f02ada8b230e1339c7`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3df4a35f85d98470ac7ecf2d59ddd8d4ef0729436b7e621728abf2f187d62f`  
		Last Modified: Tue, 03 Feb 2026 03:24:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c68016624e4e62f0e17b336a6e79e5c7acd6558d67ec798c928b2a3cbe19db`  
		Last Modified: Tue, 03 Feb 2026 03:24:42 GMT  
		Size: 107.9 MB (107868076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b61262cbf6ac1e539929bc3d367f5b9778e26023660473c741853998b9a4cb`  
		Last Modified: Tue, 03 Feb 2026 03:24:40 GMT  
		Size: 10.3 KB (10347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6938027220b5166cdd40a11f72ddf0d99e708b4ca06292a1224a63ccdf3ae`  
		Last Modified: Tue, 03 Feb 2026 03:24:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a85843fe103305e4a58f6cb661ade08fc939c82bf5298e7f25779af15343e2`  
		Last Modified: Tue, 03 Feb 2026 03:24:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8498397c4163dc0a464cdeddf9fe349d0b8e4c260a9effadbd9b1c83e0880d`  
		Last Modified: Tue, 03 Feb 2026 03:24:41 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0a1b6c2095a80a901597bf566c3b99e3f4c79e1cd8255ec61dc818bebfd959`  
		Last Modified: Tue, 03 Feb 2026 03:24:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ea7b77d7f48850689d1465956b83f57ed9cfce86de4e76e0c2d5c2d2cac11b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f576ba67b4212a936ae05611691cd74523352dfe6ae90c69085be6edd21c43`

```dockerfile
```

-	Layers:
	-	`sha256:64cb66a2e4a6d48f42fc1212a8384d8ae9a32de5949ee043077d516fa8edcf29`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 5.7 MB (5740855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b38329e21ad1ccb6fe66747492f26393c9eaee84c389769bc9616b37ece42cb`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 54.1 KB (54083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b74f62dc826a1aefbc7fc65269b1bf8724a20cd9207c3ce7a10307084734c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159739930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1457834f8237bff51c16705bc39c98280d971defa1adc59d2a3b39b517c27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:40:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:40:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:41:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:41:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:41:11 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:41:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:41:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:41:16 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 02:41:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 02:41:16 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 03 Feb 2026 02:41:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:41:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:41:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:41:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 02:41:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 02:41:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 02:41:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:30 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:41:30 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:41:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0bff38570cb8f95db65a884c7312006f3132f49d8414fa430963e8b896e8a`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2b0d649becc305e3d3eae07719f69ad916dc39e6d8afba0f5dc7d457bff9e7`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 6.2 MB (6231050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b4287a888ce4a7e25c5744b883f3f7a191454d6e173204f76b092d7db3661`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 1.2 MB (1209553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b91010dfdeb3c23189c2e2b09fbca4e0cbcb94928fda53da5fd181cb4468a`  
		Last Modified: Tue, 03 Feb 2026 02:41:50 GMT  
		Size: 8.2 MB (8203971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7c45fcb13dc3aff543d73e46457a56021cc698ffdf981558f79730fe8bafc3`  
		Last Modified: Tue, 03 Feb 2026 02:41:50 GMT  
		Size: 1.2 MB (1220588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea116cb65b1126361172e89347bbef5c89366e3bea8e018a4f0c6a3d8b0d6e09`  
		Last Modified: Tue, 03 Feb 2026 02:41:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704d93261535820f4a6e4cb1b0fa66ee1ba979864160126ce31d473483de94f6`  
		Last Modified: Tue, 03 Feb 2026 02:41:50 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2064727f0e72b933bb9807feb05da6cb92a20bb7797ce6a939ef5307c4243ec8`  
		Last Modified: Tue, 03 Feb 2026 02:41:53 GMT  
		Size: 112.7 MB (112713617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604bdd30258ad2655a8db65b498523f930af398f676d65fc1fa420b738a23048`  
		Last Modified: Tue, 03 Feb 2026 02:41:51 GMT  
		Size: 10.3 KB (10337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbf6304eb847d7d37a1bb545a129b2e303710512a075cfccfd358629188857`  
		Last Modified: Tue, 03 Feb 2026 02:41:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5913c507892baa83c0f8da297d9feb6394874dd053c90fabd5cf3dbd2de7b02`  
		Last Modified: Tue, 03 Feb 2026 02:41:52 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420babce711d19cb53a3c20d590b2d2e76adfcc37bcba67c58a9853fe7ad735b`  
		Last Modified: Tue, 03 Feb 2026 02:41:53 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184329343878e0175724bb09895fc061bee52824ac866e7feda2a7a9a310aef3`  
		Last Modified: Tue, 03 Feb 2026 02:41:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e545ba8a317cb8f805a9aefc37c1b4d90977692c7ec2e274bac63e18574dddcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5787107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35563f5f13912f272386987e0c8da394a55f7ed3e2e49d18070e17c9aeaa47d`

```dockerfile
```

-	Layers:
	-	`sha256:468bfee897941ab4fc584c899d00c1ad2f3e7d1f348a081cc5b4d8e423672df4`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 5.7 MB (5732978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e1ab9ee869f36dec6f6e2d70b20041edbd926eeae122e69a91327da8b5d328`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 54.1 KB (54129 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; 386

```console
$ docker pull postgres@sha256:9100c0079d09b827d12c2b45b00b6541a9129f95b3a3ca415e93b250fabe1d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170314044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972ba6565146e504c8199ed8de8c5c6fd6cc40c1ed702fe7463d6344e8f7f3a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:37:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:37:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:27 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:37:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:37:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:37:32 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:37:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:37:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:37:36 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 02:37:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 02:37:36 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 03 Feb 2026 02:49:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:49:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:49:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:49:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 02:49:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 02:49:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 02:49:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:02 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:49:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:49:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9063ce28338b950bf879d2ce1aa5b76b0131748813f9dda099ceb215aa17e9ae`  
		Last Modified: Tue, 03 Feb 2026 02:49:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfbe2399d504925152b49dcf863839ffab572b8e2cddd98b32958d9f47fff96`  
		Last Modified: Tue, 03 Feb 2026 02:49:22 GMT  
		Size: 6.6 MB (6630503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f677663ff01acb38c09257bcb82a4df7e36af291aaefc0f7f5040efdd3fa3014`  
		Last Modified: Tue, 03 Feb 2026 02:49:22 GMT  
		Size: 1.2 MB (1225795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973428e890bdfca29ce51b690b689dfe6ce39358dc87389b1fd6eafc2a26e608`  
		Last Modified: Tue, 03 Feb 2026 02:49:22 GMT  
		Size: 8.2 MB (8204000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40a750d28d95e3f5393311a993932063b6c4a254eff7cf9bc75f089f325c536`  
		Last Modified: Tue, 03 Feb 2026 02:49:23 GMT  
		Size: 1.3 MB (1308226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad05103646f37991f52a40cee17bc137a4d64df7688283ba63f82c080742893f`  
		Last Modified: Tue, 03 Feb 2026 02:49:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca8a6eab3ea5b7c06fd772f567f334e4d8e97a8e22cf174cb4b063c33ce0745`  
		Last Modified: Tue, 03 Feb 2026 02:49:23 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b1730914cde66e4281290d493fbf9a337a7e60249c0dc4d14d85f677e5c537`  
		Last Modified: Tue, 03 Feb 2026 02:49:26 GMT  
		Size: 121.6 MB (121630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213f3beee8a2ac6bf5ee0527e8ef314a81f1fae82bbc6c34313356a295d741b9`  
		Last Modified: Tue, 03 Feb 2026 02:49:24 GMT  
		Size: 10.3 KB (10336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f0a84f2e74ddd5da9f203b577bd969cbfe4acf606d827c6726e92ee10e899e`  
		Last Modified: Tue, 03 Feb 2026 02:49:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb24e98b2f7cd1448c223ede8892631223a32c3ab300d15aad67463e04b658d2`  
		Last Modified: Tue, 03 Feb 2026 02:49:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2644477d36bed7fe8413a39d39749135496a15795bbc20a6698db5cde2097`  
		Last Modified: Tue, 03 Feb 2026 02:49:26 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f63b39df3dc0bd1cec15e1b47413c4cbcf00e963dfd34c3ff8f2d1913e0d81c`  
		Last Modified: Tue, 03 Feb 2026 02:49:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b7bb28efd208d49637a8618de72fdcae9038f23ad3a208aac47b36957ecfe7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2589b1f5fc042fec9510e21757744b89ea13908bbb1a4bb4072639b57593d64a`

```dockerfile
```

-	Layers:
	-	`sha256:63e35220f7861769b81440c2bf2b32e36915317d0b70446ccb0eee5c55668d16`  
		Last Modified: Tue, 03 Feb 2026 02:49:22 GMT  
		Size: 5.7 MB (5740443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20964a912f587f331d492568b5ce08515a122352010c2b7060f26ebfffe9366d`  
		Last Modified: Tue, 03 Feb 2026 02:49:22 GMT  
		Size: 53.8 KB (53806 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:34723ff5ce6375f43d02dbb7180d6c72cb7abbcb2d3616a582b4e5b76aacad65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173453782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1bbabf576b14408d4ab61cc86cf500315264f491b838eea9536159fb288694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:59:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 04:59:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:00:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:00:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:00:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 05:00:24 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 05:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:00:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 05:00:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 05:00:35 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 05:00:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 05:00:35 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 03 Feb 2026 05:04:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 05:04:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 05:04:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 05:04:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 05:04:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 05:04:50 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 05:04:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:04:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 05:04:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:04:51 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 05:04:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 05:04:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2067247c50ee586cbb200d8226f05fcdcd2f42e6334ae4c7a1237e4974f27da8`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ddbdeb362dc9b15e871349cea403b2d5b0c947796b89ef6c02f249af0304b`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 7.1 MB (7076665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df226ec6ab28e05688aa44ea38117e503dfb939c29a93e4feb3cf3c6fb6bba0`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 1.2 MB (1214788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f5a8b4cbb1a257798fe9778fb752789b44196d95d970fda697a9912746221`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 8.2 MB (8203993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0a009047e8b1d6fea0f3cb745c3d08e69cc73279dfb9977fddb9ba8c1f7fdf`  
		Last Modified: Tue, 03 Feb 2026 05:02:12 GMT  
		Size: 1.4 MB (1394928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bb216edc5ca1912e97faf441f5114c5659586b5b912b049ce97837c3e05d2a`  
		Last Modified: Tue, 03 Feb 2026 05:02:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f9f462009a8a9f8be02cbb3eca10364467ff555fa297b06b769cc2f087a66e`  
		Last Modified: Tue, 03 Feb 2026 05:02:12 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90e584917c83ee52c27624c3fc167fd3d50d6d53684367d50667053cd6ecf8c`  
		Last Modified: Tue, 03 Feb 2026 05:05:38 GMT  
		Size: 121.9 MB (121942137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb17ed291fbea0495c54caddd76af96ba5824e5795f8ec0afb4570ce2154a5e`  
		Last Modified: Tue, 03 Feb 2026 05:05:35 GMT  
		Size: 10.3 KB (10339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a02a3655fc803734e870df922a9df38781e23f56a13158ff7f07fa9ed077c1a`  
		Last Modified: Tue, 03 Feb 2026 05:05:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa01fbb8e7da0f13125248e32f41c6af7ba1c39b01bdb4a2ab6864f2265eed35`  
		Last Modified: Tue, 03 Feb 2026 05:05:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f299ec5528eb0146cbaa9bbed9278b4c025c0397f18b71c95d0996a73e686`  
		Last Modified: Tue, 03 Feb 2026 05:05:37 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596b782a61c49cca4728144ef820af6574953b98ab5ec0e678655a7718739ba5`  
		Last Modified: Tue, 03 Feb 2026 05:05:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:7cd427e3389cc88578e2b2037e361cf4a91f0c00ec105c349db6eddaf79b91eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5787170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e857f3a5102965d6e32e2abeea0a32508768d06543f895dde3a4821971a5163`

```dockerfile
```

-	Layers:
	-	`sha256:d93db1113163962b76655135e8ab0e102aac511082b2c8f043a3e848538b97c4`  
		Last Modified: Tue, 03 Feb 2026 05:05:35 GMT  
		Size: 5.7 MB (5733245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635a747cf3e1e8dd2273eb772e0f277d45b72a029d27fe0489631e6e1441f235`  
		Last Modified: Tue, 03 Feb 2026 05:05:35 GMT  
		Size: 53.9 KB (53925 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:8c0228f33b015e5d304dd2a238323bf7d7f26d581112f6f83ccb488f5c09729a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92208424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326d4ce35edc236a4663852e6cca04b12079e6e1265a286c6b69e4f64725bd63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 19:09:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 15 Jan 2026 19:10:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:11:20 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 19:11:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 19:12:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 15 Jan 2026 19:12:19 GMT
ENV LANG=en_US.utf8
# Thu, 15 Jan 2026 19:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:12:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 19:13:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 19:13:00 GMT
ENV PG_MAJOR=17
# Thu, 15 Jan 2026 19:13:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 15 Jan 2026 19:13:00 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Thu, 15 Jan 2026 23:23:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 15 Jan 2026 23:23:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 15 Jan 2026 23:23:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 15 Jan 2026 23:23:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Jan 2026 23:23:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 15 Jan 2026 23:23:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Jan 2026 23:23:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:23:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 15 Jan 2026 23:23:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:23:54 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jan 2026 23:23:54 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 15 Jan 2026 23:23:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d835f0a154b0ccafb9fc80b01e712667413c253da9a0442a5b7ddf530d997cc3`  
		Last Modified: Thu, 15 Jan 2026 21:17:02 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c0224995e218b2b34c947965de64395face3e23a2621d509fca4c66ace184`  
		Last Modified: Thu, 15 Jan 2026 21:17:04 GMT  
		Size: 6.3 MB (6292271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedfe84a36c48759909cc48f6a5ba014d4b6cdeb6b907b4f88e51f07241aeeb8`  
		Last Modified: Thu, 15 Jan 2026 21:17:02 GMT  
		Size: 1.2 MB (1202032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8a5a1e179e9ada920ac0fe35266eb99dee60127368949cdc4a214c41766ea3`  
		Last Modified: Thu, 15 Jan 2026 21:17:05 GMT  
		Size: 8.2 MB (8203641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ea341f388801705ab59087d8b80970494dbb1a10513796d29ab0244c52b345`  
		Last Modified: Thu, 15 Jan 2026 21:17:04 GMT  
		Size: 1.4 MB (1402343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888775f106c69c858e84bb13bc4ddd467514ccc2f42dc3e260dc52ce58415948`  
		Last Modified: Thu, 15 Jan 2026 21:17:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f0ef0c3ef53020327fe79220e01362f5a7dce715ae367d41c111e5f75f3dda`  
		Last Modified: Thu, 15 Jan 2026 21:17:06 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f3f4035912bfcfa93e03142425d493f36a6679eb29ce36fb9327fffbc1922e`  
		Last Modified: Thu, 15 Jan 2026 23:26:27 GMT  
		Size: 46.8 MB (46815359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2ba5d41d9c03eaf3eccf4c38a3b3cdfb0761def00decdef8a9846980f2e7b3`  
		Last Modified: Thu, 15 Jan 2026 23:26:19 GMT  
		Size: 10.3 KB (10343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88085e237a50a4ead9b19ab209d2187b930a94f14bfe0c005cad27bc66df5334`  
		Last Modified: Thu, 15 Jan 2026 23:26:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43259fd3936f05c6b9bc607206ef56ba41b8ea7406f51e9ea450da95e96155f6`  
		Last Modified: Thu, 15 Jan 2026 23:26:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61604e2dab07b85299b210a58e76bbbbf4a6fdf33bfb898eeafca6e8ffa3025`  
		Last Modified: Thu, 15 Jan 2026 23:26:20 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77253eb0fa38acef0575811f691812ab2ce6f9c31571fbaa92d5a4920de3612d`  
		Last Modified: Thu, 15 Jan 2026 23:26:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e9a7d52c65c4f2651f26e10feaf260476f94a46cd52dcf4d70a1afd8acae1606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4cde3fc72fc10a33427926960bede6e61b7abc467c17ed39834aba7f4e9d55`

```dockerfile
```

-	Layers:
	-	`sha256:050f42673435446259b709854d3e32c7d17ccbc773f3af54ebf66a07642b40ea`  
		Last Modified: Thu, 15 Jan 2026 23:26:20 GMT  
		Size: 5.1 MB (5083908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c850bba97fc981ecd9822ac5654996e51ecb082bb1f3327d98e63391cde29cb`  
		Last Modified: Thu, 15 Jan 2026 23:26:19 GMT  
		Size: 53.9 KB (53920 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:0b47ad43c57d2a1c1d9bd33b288431075f4b2e049ab7dc9d6852dc886c66e7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175696063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a63967121450ce2a92ea9eda847b9255db4b5ca5f6c45ddaa2f929c9ba2f74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:10:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:10:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:10:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:10:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:11:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:11:04 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PG_VERSION=17.7-3.pgdg13+1
# Tue, 03 Feb 2026 03:23:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:23:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:23:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:23:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:23:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:23:56 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:23:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:23:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:23:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:23:56 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:23:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:23:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8077f2bbcfce1aaedf1a064a0e8fd51aebe94ad0ef24c0ff2ddca619fbd173fa`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79287514408b6ef0a85b7d3a863a699fc7122c0b12b45844a562c3208221510`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 6.4 MB (6408759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5e8fb73d9a4ab10b09d8fd286ff36deb8d8ae34e6f2013352136f379a40f4`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 1.2 MB (1230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c866b9c8124101d8c7209f17cfd7d182230fddc5fb91850fe69a2dd12caee377`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 8.3 MB (8258952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b55952f5e10fc188cd69ff85002b0f1dbd437076f36a273875c03c1562589f`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 1.4 MB (1398202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a2d60021e150d93707586195a33ecb491529c20516756048816be04ff66b72`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42b977764bd402a1c842afa683e87e58284f47b463bdba118c8bd7fa04f0cc`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbe8a9b9eb9c17e2478cead91c854454e41034569ffd6d4d29d9116e8baf261`  
		Last Modified: Tue, 03 Feb 2026 03:24:27 GMT  
		Size: 128.5 MB (128540707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dec91d1ad506e669652ac02d5595bd0373f0e62a0d4b330f5775bc2e909941e`  
		Last Modified: Tue, 03 Feb 2026 03:24:25 GMT  
		Size: 10.3 KB (10342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad176f281bf721ffdffaf16418ca4a569cf949803bc4a5fd8f81b3822f46fbe`  
		Last Modified: Tue, 03 Feb 2026 03:24:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adc4824b5e79bca3e0d62b9a0ff8b7dfebd917857cdacc47989ca7179c4c58b`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e80408244350c07bf658342b2a04f7726831092436e68ed45e81477f781ec1`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febacae3970db0b4c852c9dcb8c1cf44a0ad2723c9f6ff796b1b4c18eed8536c`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ca08f9d6047a2b294c76e8ca29c19c5f8409bb7deefde4f1d6e7e156bf251a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9c548cc7e7649dbb9917494b471d19de5a8966ccb63d877ef3f9f9d9eb70b6`

```dockerfile
```

-	Layers:
	-	`sha256:b8591b432ca9c044b8a32a129b96e42e8ae8f86c42e92654f0b448f37ad9893e`  
		Last Modified: Tue, 03 Feb 2026 03:24:25 GMT  
		Size: 5.7 MB (5741581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6cb040c1eef0b94d353bbf0a8fa96d234e6322a50a52a9feb611ae6af26d691`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 53.9 KB (53860 bytes)  
		MIME: application/vnd.in-toto+json
