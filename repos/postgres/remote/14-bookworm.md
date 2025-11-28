## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:15ad05666ac583ff153882873d16bd098dcdfc77fefea1698afeabe37ed174ea
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:14-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:37d7244bbc4c8c0c47e4247f2e8451fef6b4936cb7d0a74d1bd5201db6aafff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151837344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ece912c55ae15eb7ca39a3dff4ea8a3fe2d939eaea9b531f39eac8a4e3f48ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:58:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 04:58:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:58:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 04:58:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 04:58:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 04:58:50 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 04:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:58:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 04:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 04:58:54 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 04:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 04:58:54 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 05:02:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 05:02:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 05:02:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 05:02:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 05:02:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 05:02:11 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 05:02:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:02:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 05:02:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:02:11 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 05:02:11 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 05:02:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7664d229e9b63965bdfe59af4b42fedcfd86a09687bb86b4e0cb8c756bb396`  
		Last Modified: Tue, 18 Nov 2025 04:59:40 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a952e506642020427cd3166a0fc3b7c945732c5208f76e77cc2fc8025c41b268`  
		Last Modified: Tue, 18 Nov 2025 04:59:41 GMT  
		Size: 4.5 MB (4534013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554dfa89b2a54ba7cc194d04c2ad1d3d551d2ea395c5fbbaaab0bd3178e2d907`  
		Last Modified: Tue, 18 Nov 2025 04:59:40 GMT  
		Size: 1.2 MB (1249468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577e841c5a4763f83204b249e612a26afecc2ff722ecc36d6f1e5be1d6a57768`  
		Last Modified: Tue, 18 Nov 2025 04:59:42 GMT  
		Size: 8.1 MB (8066426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143ba1cdf5f50319f749a71e1c7ebe05b63e7a975dc41f1fa604664217527ab8`  
		Last Modified: Tue, 18 Nov 2025 04:59:40 GMT  
		Size: 1.2 MB (1196380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c1ede25ab87b38a6784f4db109ddbc99d7a8492f6a0b0ee83fa645511be436`  
		Last Modified: Tue, 18 Nov 2025 04:59:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5727978f12d548e2b8f97caeb669aa0f8e774176735b2e62d1195d305b9506`  
		Last Modified: Tue, 18 Nov 2025 04:59:41 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fc9b6388ec31ed7ae6cee03adda72979e6d8809663e2efa6498bc685bd72f`  
		Last Modified: Tue, 18 Nov 2025 05:02:56 GMT  
		Size: 108.5 MB (108542340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c36eda311d29fededd68628c97dc58788ff23665b0240b315a24a91d8b68a6`  
		Last Modified: Tue, 18 Nov 2025 05:02:41 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539603b543c266f3c1a1a5149693db56a1bc8c93f145ad6176a921c4ffecd9c8`  
		Last Modified: Tue, 18 Nov 2025 05:02:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f750fc9b8e4b7b670078018bc65756eb52d99c58893b362c393bd587f49ebd`  
		Last Modified: Tue, 18 Nov 2025 05:02:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9c36956ab7b377e741cedcfae373f6fcedf3ccbd8f146d29e639c035c10e5a`  
		Last Modified: Tue, 18 Nov 2025 05:02:41 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343f5a11da8e93c5aa58e00bc093ed59c2fe2976ca9a2eb316f68dc78ce1f89c`  
		Last Modified: Tue, 18 Nov 2025 05:02:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b2a32f8e3d14e9c3a5395356c37c1e9f895b7241f426a8ef38d7ebf0cb50e4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5846131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc75d9acc282156ad516d3063849d39b12ba68e69995664d5b2677ce8fc0297`

```dockerfile
```

-	Layers:
	-	`sha256:e88a90dc5e11dfca17e395d26ef7009920a1eb3c8223b24bf85348c5294747ac`  
		Last Modified: Tue, 18 Nov 2025 06:09:16 GMT  
		Size: 5.8 MB (5792835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc647f639254a2d83d7b8d194533678c7ce1d0a8f99fb3cc0eef10cfdcf641c1`  
		Last Modified: Tue, 18 Nov 2025 06:09:17 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:250ddc4bdce2493b9a09449a2cb21f1dde3f866ad8b5da54d0ef35b3b971885c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144784555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1e3a9f77c28dc4858a89dceefed9daec6d267b5c1a528abef235ec86e11794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:03:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:17 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:03:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:03:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:03:24 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:30 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 03:03:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 03:03:30 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 03:30:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:30:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:30:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:30:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:30:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:30:37 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:30:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:30:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:30:37 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:30:37 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:30:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7475f86597262ecd8feea48452e415d7647386b0fbfea40510a8210913ddc`  
		Last Modified: Tue, 18 Nov 2025 03:15:42 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2390d068fcb89649c9187584e881bf8987beeb64a72dfff50f3b6e847ccb15c`  
		Last Modified: Tue, 18 Nov 2025 03:15:42 GMT  
		Size: 4.2 MB (4151198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806a6e3317f531f076fa201648b14292b01d054e67bd11a7ecdea25daf2d3c9d`  
		Last Modified: Tue, 18 Nov 2025 03:15:42 GMT  
		Size: 1.2 MB (1220051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22339039e4874b84a866592a7ccb31fdbdc88b338231865179020818ef95a7ea`  
		Last Modified: Tue, 18 Nov 2025 03:15:42 GMT  
		Size: 8.1 MB (8066538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec82ca1e597ddccc434ccd769181b49b91a8ac8090a7bf046b7b48265ffc3a9c`  
		Last Modified: Tue, 18 Nov 2025 03:15:42 GMT  
		Size: 1.2 MB (1195045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2316ba1636fba0b07a2dae347fab03e812d719efc9f549cb98b85ca21e06d7`  
		Last Modified: Tue, 18 Nov 2025 03:15:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed99c67cb200aed01db97faaba472f77cd258c0bd06bfa7cc25b0719a5f5625`  
		Last Modified: Tue, 18 Nov 2025 03:15:42 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543807e64f2125b874ff046579d56d5c71f5efdb8983b2786cf762ad2a864923`  
		Last Modified: Tue, 18 Nov 2025 03:31:14 GMT  
		Size: 104.4 MB (104373925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f43908cade3e194f88aa0e6975a2338722d079cc6612c6a9ffa3321ba9620ed`  
		Last Modified: Tue, 18 Nov 2025 03:31:05 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3055cae3548d439d4e294e8d2996fd01b5a75cd78dbc054a9b601e6429f58a05`  
		Last Modified: Tue, 18 Nov 2025 03:31:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8890d20934289369909b4623e16b0b8166f5eeb7c47d6fd46dc2219b13569fd2`  
		Last Modified: Tue, 18 Nov 2025 03:31:05 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc042e2c2e88b68a13db2791853e832d3207c298ff2ab8024504222a6b4a832`  
		Last Modified: Tue, 18 Nov 2025 03:31:05 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2d7b3f90bbf83d65c65ff6668dafa779581dea49c7341a1c1097315cd71c69`  
		Last Modified: Tue, 18 Nov 2025 03:31:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c9d09987a1185990ddb4073e733f23bad791b2418cd196ad0264b7d17aa4729f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea65e92e740ff01f7a69006ea08bff656c89d7546612b6f01428996ada32631`

```dockerfile
```

-	Layers:
	-	`sha256:d56265a353d872865fe8f9336848881c0ce1fe1aff534d154f95af2a42f72351`  
		Last Modified: Tue, 18 Nov 2025 06:09:22 GMT  
		Size: 5.8 MB (5808660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e3c7b14c7b05f6053e163ef0c63b0d07b3a42a34fd733c398ff750c48b278d`  
		Last Modified: Tue, 18 Nov 2025 06:09:23 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:2f50c1b82fda88401fa762a4db2477f1d33b20c0eab0160e12a983eaf5111ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139884647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4d35bd7197b967b0a9bfca28a35bafbac5289061478f3305c4c2a20842e4a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:38:42 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:38:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:38:56 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:38:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:39:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:39:01 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:39:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:39:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:39:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:39:06 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 03:39:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 03:39:06 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 03:52:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:52:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:52:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:52:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:52:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:52:32 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:52:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:52:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:52:33 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:52:33 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:52:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548cb2508b7f909184a0650a190382bb3595169d74e0fc61adda61a6c6fa5780`  
		Last Modified: Tue, 18 Nov 2025 03:53:01 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9a8ae397d48a9d503b1f935550125b4a009c2dcedd88ec9674b7f52095dc1e`  
		Last Modified: Tue, 18 Nov 2025 03:53:02 GMT  
		Size: 3.7 MB (3742657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0b304c34b8e7fd3d57ec1e26c48abf86f45e08ff5eb888095036b1546e465f`  
		Last Modified: Tue, 18 Nov 2025 03:53:02 GMT  
		Size: 1.2 MB (1215981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d5fe18db0afa3188f6c01a6f7e34c39100b9f0396b49e3c79bb09d30b5c8f5`  
		Last Modified: Tue, 18 Nov 2025 03:53:02 GMT  
		Size: 8.1 MB (8066417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1b7fcee5f75de0f04a9d183d89ed466bc4c21153f8c01d57038bfc97bc6c56`  
		Last Modified: Tue, 18 Nov 2025 03:53:02 GMT  
		Size: 1.1 MB (1067255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfc0bd2f7f669aaa26fc3e2301d078b29763baad99711a2c61d8817d57f4ad7`  
		Last Modified: Tue, 18 Nov 2025 03:53:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba86f1b9a3dca5c76dc91be8e1c2715c18bc60b07528b33e427ddeb8cf32bd25`  
		Last Modified: Tue, 18 Nov 2025 03:53:01 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bede7450b8d1c725bed49c441d89d84292b6a074eabb6187fa17c7e05a21e055`  
		Last Modified: Tue, 18 Nov 2025 03:53:26 GMT  
		Size: 101.8 MB (101838057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea70833e67be963f20175b54be6c8e30c0bdab39418a1af765abf25e89dea0de`  
		Last Modified: Tue, 18 Nov 2025 03:53:01 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c389c2278282f8ec3fd4403d952ba7b9bd7f011bb9f6efd11ccececd91bd44ab`  
		Last Modified: Tue, 18 Nov 2025 03:53:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aedcc691903eae893cd9818b7759f059af3100189ceaa9d7055326c677abda`  
		Last Modified: Tue, 18 Nov 2025 03:53:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76dd492ed5ef50b9da566ba3b70e01d47978178ebcfe976294b43ff152135f2`  
		Last Modified: Tue, 18 Nov 2025 03:53:03 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a4583a9e1833448329dcdaf58eeac502a25791811d0b2132a1e439634dd530`  
		Last Modified: Tue, 18 Nov 2025 03:53:02 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0473d93d8e21deb67ff1c2a28cb78163c8745a7ef310b899e5a1fcbc54952722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04082ba053c8ae782827e74d9e4ecc1ddc885fc3a4379351f499f15aaf5beb62`

```dockerfile
```

-	Layers:
	-	`sha256:69fb7e22b2ef656c07538f01d83938779c83f8f6e0aeda60af0817b284d7234b`  
		Last Modified: Tue, 18 Nov 2025 06:09:29 GMT  
		Size: 5.8 MB (5807915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b957175750b2ebbf51df438513b45d1ee677fc039efbd23311ef326e7f14a`  
		Last Modified: Tue, 18 Nov 2025 06:09:30 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e7f0d9a969716bda2d89df4c5276d94c05588589dc6d3ddd7d25dbc446f49c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149839552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdc8e4c2df01bdd37675f9b30ba313d70c3196afc244e38172816e7f4f525c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:01:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:01:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:01:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:01:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:01:52 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:01:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:56 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 03:01:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 03:01:56 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 03:07:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:07:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:07:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:07:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:07:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:07:27 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:07:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:07:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:07:27 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:07:27 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:07:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f929630baf8525405532edbf8144dcb6c700bcded6043b3df78974ac40a8059a`  
		Last Modified: Tue, 18 Nov 2025 03:02:40 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2286bbe8fb06caf5f4523d331d91a508134550e27734a95785c2e84d51cfac6f`  
		Last Modified: Tue, 18 Nov 2025 03:02:40 GMT  
		Size: 4.5 MB (4519797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9328e44d2f259aa9e586a86ef621a1d88b1031da54e718793eb4dfa47f00ae`  
		Last Modified: Tue, 18 Nov 2025 03:02:41 GMT  
		Size: 1.2 MB (1203243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b260ef9830f3786ae24cd177f488f3e640fdbe9a00ffa9dc5c14f45b582f455`  
		Last Modified: Tue, 18 Nov 2025 03:02:42 GMT  
		Size: 8.1 MB (8066466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa68f2acd6bc9265fad8f0c0fb1642a20ba5ea8433914492c290fe95a4403f0`  
		Last Modified: Tue, 18 Nov 2025 03:02:41 GMT  
		Size: 1.1 MB (1108956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3ade131247342ad9b41a10752e033b67772ded5b1fb3aae8dca0db847732a6`  
		Last Modified: Tue, 18 Nov 2025 03:02:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e482679b848359f1bc39d59a909adf1e0b1f19c442e43177858e224e1f7d37d`  
		Last Modified: Tue, 18 Nov 2025 03:02:41 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572063c0e65ef9f61782d10b22e3d7e5347582c4c88fa1ce25317bdedf09e30d`  
		Last Modified: Tue, 18 Nov 2025 03:08:02 GMT  
		Size: 106.8 MB (106818617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7eb14e676551bc9b57bcf411bba0bcfbe564ae690b95568c36dd0d50bed457`  
		Last Modified: Tue, 18 Nov 2025 03:07:53 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd6d26000b971818641abaffcc1063ad92b1e1e109083ef68ea8e328924290`  
		Last Modified: Tue, 18 Nov 2025 03:07:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28244ef28266fd63980570bd33adb7175a88f13bf9e0567d3d9c97e920dfd630`  
		Last Modified: Tue, 18 Nov 2025 03:07:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b986ef18e1bde4a640327c3b639f36e79a5bb1988d9f523dcd70a8f56d37f80c`  
		Last Modified: Tue, 18 Nov 2025 03:07:53 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e924e49f2083582cd74280fe3cbe61fc89238c0a46b814ab266088b5a62c33f5`  
		Last Modified: Tue, 18 Nov 2025 03:07:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7dc0277c17cbf54e51c9d51bcb5dad8c9eb83050e9f95481c5dbf20f0fd300b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5852687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1693c4fc4efb3d49180b4eb74f97c5a249e040a0ad91383cd31cd61b567c8a55`

```dockerfile
```

-	Layers:
	-	`sha256:211b83996da456530d30b01baced5601fde2373561d5c750be74bc368eccd60c`  
		Last Modified: Tue, 18 Nov 2025 06:09:34 GMT  
		Size: 5.8 MB (5799146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4dfe27475c4cdbb1ea24218fc20fd3907c35a6752fac675015fb9c1ce26df7`  
		Last Modified: Tue, 18 Nov 2025 06:09:35 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:f5f7d97b062f44ceab5593fb94ce199200822a07c6f72541b6910df7c0f6e0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160522154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15cb38d1aec02ce3d5b4d2b451d124acb26502d2b7a62c68c726cc44733faa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:50:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 02:50:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:50:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:50:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:50:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 02:50:46 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 02:50:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:50:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 02:50:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:50:50 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 02:50:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 02:50:50 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 03:00:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:00:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:00:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:00:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:00:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:00:19 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:00:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:00:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:00:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:00:19 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:00:19 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:00:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60518e4a4ef9ffe9630c3fe11ff95a855d3589fffc1317d905a64ce885db0bf`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e26ac169b11e3df991cd23889d3623e16f2af471564c17bc3f19ec3c472d005`  
		Last Modified: Tue, 18 Nov 2025 03:00:50 GMT  
		Size: 5.0 MB (4965384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364511113b8ed809a4460830aae0288f2aa4b7af70b7be7ae1afcc7754eaaa3d`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 1.2 MB (1218648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73be2d909e610e09823bd60d2dff83fc8ff4138ff1ad66966fd0aefbb578a88a`  
		Last Modified: Tue, 18 Nov 2025 03:00:52 GMT  
		Size: 8.1 MB (8066412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cc60c9d90d50e54f29e0469699d33f98ec5d45efa13ec3c366fdeee60a7c41`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 1.1 MB (1137439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ab6e73a35292018c779ed73021f920da70fa9a216788c55b2f511ebcbda40`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6876d4727cb1a1eb3c84a3e1b0d14413781fab1c43bf67fdc577c06179dbaf1b`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bf0a5ed9a9c955c5a61fd778950ab6f746e0dbe28a4a196399d3c10ea32d16`  
		Last Modified: Tue, 18 Nov 2025 03:00:57 GMT  
		Size: 115.9 MB (115904291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea85a0068ce9c8908c0195aedd1880d073b9a099e6addc9d1115586907691a`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233fe18da6da2374619af71c1f7a7f5d9102e6d6fe147e80c58b50f733bc9cca`  
		Last Modified: Tue, 18 Nov 2025 03:52:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce4cc745de216934fc9b442f68c249bc8e3027edcad962172581f8ac9ed8cbf`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54366574d9cdc2a8e09862a31dd897042e1b5bca44d633d610e0759a7d1e3cdd`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7881b1253a7366551e5bfda9ec293af51bde7b9f9850e8c8403bac63dbca7265`  
		Last Modified: Tue, 18 Nov 2025 03:00:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a3533a36ad3e7319ded5faffdff3ee75803469a6b92be0f7d8c4a5e472d5be95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5860055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb4fd6e1c6a07657f7ab1dae1d604da4617df0a6cb2e696ba1b6ddc90a3dc88`

```dockerfile
```

-	Layers:
	-	`sha256:5902f8fe9d16c9496807c6a9b5a6d4340cb4aeebf31881a8ac1bcafd5cf6b0b6`  
		Last Modified: Tue, 18 Nov 2025 06:09:41 GMT  
		Size: 5.8 MB (5806803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8903c97b05887e4192c0fa70f93b115dadc27d4aa47e6b7ad606bff58c161f78`  
		Last Modified: Tue, 18 Nov 2025 06:09:42 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:46b12593322b58e2ba54ec745306e5737ea4ac96decb0e393b2dd38709db08b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150634272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d743893cffb154391fbaa303c1e5ef3f7961212752997759d02205235b27e74a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 11:11:04 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 11:11:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 11:12:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 11:12:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 11:12:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 11:12:31 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 11:12:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 11:12:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 11:12:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 11:12:52 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 11:12:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 11:12:52 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 13:30:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 13:30:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 13:30:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 13:30:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 13:30:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 13:30:43 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 13:30:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 13:30:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 13:30:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 13:30:46 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 13:30:46 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 13:30:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:099882631f3c0c5583696bbb377a83dca2faf014da28b08add3482e4678d2872`  
		Last Modified: Tue, 18 Nov 2025 01:11:53 GMT  
		Size: 28.5 MB (28513764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e715074f7f33280fff2596b6f6c85030c41a75cd4ddc9ed41c75584ba523853`  
		Last Modified: Tue, 18 Nov 2025 12:26:17 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121ec9b64949cad49dcb8bc2187039620ad059b13e9fa39134559e77cef81ca9`  
		Last Modified: Tue, 18 Nov 2025 12:26:17 GMT  
		Size: 4.5 MB (4475527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c613f33280b862711cbef891ef9bc0dba543f1394559c61aff0e669c78632b`  
		Last Modified: Tue, 18 Nov 2025 12:26:16 GMT  
		Size: 1.2 MB (1159214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4786c50dab82bf8cecc92f35a4cf9e3dce4cf3e02aae33593d835020e7743b0`  
		Last Modified: Tue, 18 Nov 2025 12:26:17 GMT  
		Size: 8.1 MB (8066623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36568cc175da71190684c85089130fe08ef879760f331c7ebf5d075d3fd5f0ed`  
		Last Modified: Tue, 18 Nov 2025 12:26:16 GMT  
		Size: 1.2 MB (1182925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cbc1bccff745bc31ec75fc5896cd53cc1c19da33ae3e0ce0875e805f171fdb`  
		Last Modified: Tue, 18 Nov 2025 12:26:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e307a7d9d1e50887e6bbe63a6f8b301b1ca0f4e6e3f69dcd99bc922b9b0e80`  
		Last Modified: Tue, 18 Nov 2025 12:26:16 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff2267003315ffccd482a11ac70c0a631de19d73b67bbf240357ca5d101f84`  
		Last Modified: Tue, 18 Nov 2025 13:33:05 GMT  
		Size: 107.2 MB (107215938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8c2bbd7bbcb1c97a08f46a63759440f1271efdfb2d40c77761c911df485adc`  
		Last Modified: Tue, 18 Nov 2025 13:32:57 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0260c31bbe68294abd43cb3b9b44a38abf16e1b5858aab187b355083de11228d`  
		Last Modified: Tue, 18 Nov 2025 13:32:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950eabb6a7e3eea9238a6498b876127d320da6ee5730184a1c54f53b50fa8d4e`  
		Last Modified: Tue, 18 Nov 2025 13:32:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5888b3d156f323f6060c1a0a482d39b77d73ee16a0bd8e49f9d97bd9de9f2ab4`  
		Last Modified: Tue, 18 Nov 2025 13:32:57 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90138511f5184779a9ae7f197b572a8d324037a48e6f5baea55363afa91dca4d`  
		Last Modified: Tue, 18 Nov 2025 13:32:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7a3beb92fc2d66cf84a4f2a653a4c73d604a089bd89b0eff80193402846c8c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0461a53e62b11bc97371eb2fe0b7dd3dfed5c8478645e18bcee20b4c5de83ee9`

```dockerfile
```

-	Layers:
	-	`sha256:b897e98023071b720620db5740ee4174d9f037bf05299935087e45c902882723`  
		Last Modified: Tue, 18 Nov 2025 18:08:21 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:d3392d03dabc5e705ef321270a4e653c780141f61bbc00bae042f973f7796128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164505223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e92259ad381805c37f33879fc3e0b896b6d6743cd2708a34be4e496f4021b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:39:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:39:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:39:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:39:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:39:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:39:45 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:39:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:39:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:39:55 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 03:39:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 03:39:55 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 03:50:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:50:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:50:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:50:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:50:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:50:40 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:50:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:50:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:50:41 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:50:41 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:50:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8ea8a5e45a9f8a2e7e31a0f77d452710dadca63e6c814f5d07ae93e3b67d5`  
		Last Modified: Tue, 18 Nov 2025 03:41:52 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f2f575996d5f79ccacb98b2d4dcab20fe6dd5df6bcf230cfda5b75e16793a`  
		Last Modified: Tue, 18 Nov 2025 03:41:53 GMT  
		Size: 5.4 MB (5368530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadfd5474527e6b000820fa4e6bb91633aff5f9c0fbd36c3d0769b1e477ffc69`  
		Last Modified: Tue, 18 Nov 2025 03:41:53 GMT  
		Size: 1.2 MB (1208143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6da77ba2a3a8dd1b69ed64868243e55186732dac318046c9a3c0a2063ff25c`  
		Last Modified: Tue, 18 Nov 2025 03:41:53 GMT  
		Size: 8.1 MB (8066539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31d7688837191582e9a8e247832e843da652c91330ddd50df00bbc05cf23ea`  
		Last Modified: Tue, 18 Nov 2025 03:41:53 GMT  
		Size: 1.3 MB (1283660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0f8ff1586935e76a9b3273d42bc0a0fe1e3c97229d0cffb745ced94c725d2`  
		Last Modified: Tue, 18 Nov 2025 03:41:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c346420a081c01b7f12387afd3f16dac9d5f4d2fc3cd0d2a1f1da6452aaa45b`  
		Last Modified: Tue, 18 Nov 2025 03:41:53 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4b0cd09ad0dfa887a21867ba24a0f36a6039d3aa706e9a465625f8cbfdaf6b`  
		Last Modified: Tue, 18 Nov 2025 03:52:06 GMT  
		Size: 116.5 MB (116489238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee9716ac1fcd1f7e5312919b2419c6ef444971eeb6a898060d65fb96670b044`  
		Last Modified: Tue, 18 Nov 2025 03:51:56 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a748d390daf183c634216ed8c977e64118be9a1549a914f5386e9652d28ce`  
		Last Modified: Tue, 18 Nov 2025 03:51:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64242e7c428f3f9d94c11292ad6598c79c78a8258528620fbac25c6a108be775`  
		Last Modified: Tue, 18 Nov 2025 03:51:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bdc7a68e1a10cbcc754ddd0df5cc712e91bc7b4b98fa381dcebf705f21873c`  
		Last Modified: Tue, 18 Nov 2025 03:51:56 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d09745bf96c0b58bde508d1c7d0d24e34d15ec71ba608057d6381213a45a0ad`  
		Last Modified: Tue, 18 Nov 2025 03:51:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:594e5cc4cd9446ea89cdc953141a50dcd77f4c006a0c22dc1128a86efefbc43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5853546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28c4bd50ce4d869b61fb36c802213ce4afd77d52e6003e63bfbcb5149f6f164`

```dockerfile
```

-	Layers:
	-	`sha256:ae39edf130f7a90a7208b2382c6a4d4dba775976857ec6d006d3245941bc98fc`  
		Last Modified: Tue, 18 Nov 2025 06:09:52 GMT  
		Size: 5.8 MB (5800196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd398d79eaa795fb73df14a0d4b7692ae43cc041ceca06075ed641f3b837c56a`  
		Last Modified: Tue, 18 Nov 2025 06:09:53 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:368b721e943ea92faefdcecd3a47ffcadbe649af7ed80f1b790c10ca20c1ea64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160974157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eef5a6f8fbf3a83cd6801b6bd278781d99db8b9a122e17f9d25fcaa5081d762`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:27:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:27:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:27:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:27:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:27:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:27:52 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:27:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:27:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:27:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:27:56 GMT
ENV PG_MAJOR=14
# Tue, 18 Nov 2025 03:27:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 18 Nov 2025 03:27:56 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 18 Nov 2025 04:05:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 04:05:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 04:05:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 04:05:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 04:05:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 04:05:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 04:05:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:05:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 04:05:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:05:17 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 04:05:17 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 04:05:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23fc6c717395f30fd5dd5cd10b4713bccbcb613df9ccc531648b94c115e48c0`  
		Last Modified: Tue, 18 Nov 2025 03:40:49 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cabfabe8a19ed29c3eae5efab5b9ed715c80d51c68dc09917890c5c3fba9bd8`  
		Last Modified: Tue, 18 Nov 2025 03:41:50 GMT  
		Size: 4.4 MB (4391338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89a08c5c8c6058a168e6d22557686ecb419f476197e2722804da11207ec2560`  
		Last Modified: Tue, 18 Nov 2025 03:41:49 GMT  
		Size: 1.2 MB (1222792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a284bf76aeecdd6db3319f2eedf4cb0b39599c55a4af9e97bb42140b16757979`  
		Last Modified: Tue, 18 Nov 2025 03:41:50 GMT  
		Size: 8.1 MB (8120665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b819e69d5b1f3cdd68d019e65f2b48371b9122180bf9a7973a835016eaef57`  
		Last Modified: Tue, 18 Nov 2025 03:41:49 GMT  
		Size: 1.1 MB (1097005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255622b95937a30c5251cdcbf715af985e54ac7437642da174d9a24cba57ff6`  
		Last Modified: Tue, 18 Nov 2025 03:41:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f9a11ec36ab84a51fdad422847e273f39fedc0e780a70a9ebc8440c5ca5c5`  
		Last Modified: Tue, 18 Nov 2025 03:41:49 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67021bc3a4e69d4055aac928bb93b387f78dfc10bec167cef968f271e82f34c`  
		Last Modified: Tue, 18 Nov 2025 04:06:02 GMT  
		Size: 119.2 MB (119237693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720dc426d20f55f26b58247047563c6bc2f94ac4e9cd8065a71bd58345d61365`  
		Last Modified: Tue, 18 Nov 2025 04:05:53 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e4b89f655605b1442404fcddd6155fb2d9cee9c9734cbb758ba73a29933b5`  
		Last Modified: Tue, 18 Nov 2025 04:05:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfc22402eac874bde29ea2b0bbef847436f8459815e803e39f39c0ea83d0f21`  
		Last Modified: Tue, 18 Nov 2025 04:05:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692b6e2001362d1971f6dfbcc752436fcc82e3d4649889ff97563ca474965f43`  
		Last Modified: Tue, 18 Nov 2025 04:05:53 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24753c4844ccc7e04d2f5646d84aaa1e49d2bcb2ffffdc7c17a1632424b824`  
		Last Modified: Tue, 18 Nov 2025 04:05:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:dc07542abd10a96673f02abd39503d89b7cd5b23e86af521d8550ebe072b6942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c0eb6c009321910986e521fe1ade29870f6d7fff2278b8db228b011bad6020`

```dockerfile
```

-	Layers:
	-	`sha256:9d632fba6bd2e8fa6d7daedcd04aec7c2cedffa7a10010a070e9924e490c9de2`  
		Last Modified: Tue, 18 Nov 2025 06:09:57 GMT  
		Size: 5.8 MB (5803279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baadf7162eed9ba14e7a33476fd137980b9bd552cbff9beaf60d607f75b17348`  
		Last Modified: Tue, 18 Nov 2025 06:09:57 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json
