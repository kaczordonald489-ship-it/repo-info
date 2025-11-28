## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:1aed029c7f1f32d20a3320d11f65b2a342a4744ef1a3defcf7c6614489afbb54
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

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:4b26f516dae03565014c4f1b748315754b1aaa7eebc2b0b70d7916d63a92e2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152900593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d371b1719f06b174abbd10951a890a5fadd0688473da0a115369d9dd914d3fe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:01:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 05:01:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:01:24 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:01:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:01:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 05:01:28 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 05:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:01:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:01:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:01:32 GMT
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 05:01:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 05:01:32 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Tue, 18 Nov 2025 05:01:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 05:01:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 05:01:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 05:01:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 05:01:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 05:01:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 05:01:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:01:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 05:01:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:01:45 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 05:01:45 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 05:01:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27fe9045e2b356e52b3d220e1325932de2ab9a56daf3630c4d5c5be84d6f347`  
		Last Modified: Tue, 18 Nov 2025 05:02:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e540bb81f070fe47ec5d56e08b745dfe849a42fad266a6d87b32611ee947e2`  
		Last Modified: Tue, 18 Nov 2025 05:02:18 GMT  
		Size: 4.5 MB (4534096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20531b75eda0c54acfb9347ee52385b7e0b0175f5279805346374c63527e3943`  
		Last Modified: Tue, 18 Nov 2025 05:02:16 GMT  
		Size: 1.2 MB (1249511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553f3a8e382684b6842bd67dfe428aa505e553b5ca91d49ed78165656a4a3b31`  
		Last Modified: Tue, 18 Nov 2025 05:02:18 GMT  
		Size: 8.1 MB (8066442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562d202602f081cfa4715b46ed21183014fc3c5805fa16c19a3e6b0a3d41138a`  
		Last Modified: Tue, 18 Nov 2025 05:02:17 GMT  
		Size: 1.2 MB (1196397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa4d1912ce69dc3ebb10644b5f75e47fdbebb7570574cfed80c67e2a8e8a476`  
		Last Modified: Tue, 18 Nov 2025 05:02:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8c11b5a242f645e7ee80b0b6c16ee9ce9425ae7d9b4890d4114b6aaa8bbc4`  
		Last Modified: Tue, 18 Nov 2025 05:02:19 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95cceb4e496666c0c0c0d64fcddd3cb90e986d648587ea7c8c4af59fe81e677`  
		Last Modified: Tue, 18 Nov 2025 05:02:37 GMT  
		Size: 109.6 MB (109605184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3582aa66cda9caa95d78cf216c7e2f787987aa529c4fc4d72451fc9c848e79b2`  
		Last Modified: Tue, 18 Nov 2025 05:02:19 GMT  
		Size: 9.8 KB (9770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cd415ea8282a41120dc6b9c25d7b084e0d5cd2b7060e97d35b07fce65df154`  
		Last Modified: Tue, 18 Nov 2025 05:02:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b536294bc385b6a4b9c07891df4bf6a494063ac50f3547e71150294fb20113`  
		Last Modified: Tue, 18 Nov 2025 05:02:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fbe811544d403440c5245f6adefd1e51c7238a609564a683d401439dcc73d1`  
		Last Modified: Tue, 18 Nov 2025 05:02:18 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6ab0a595e349f558c25057d895a6621c4d96dbeac5fde2dc92105f825411d0`  
		Last Modified: Tue, 18 Nov 2025 05:02:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6f7ac7b66889d13271d56d4e532fcfd034d12574f2ed3359e4208efd45a1efca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b817e0b7c93402a3b7bbedd3af8601bfa13c256e74c15d99e2d3bb695c73c9f`

```dockerfile
```

-	Layers:
	-	`sha256:326cf1ce13c83c8508123dc9e706f37c769953767e7f47f65f773d3bbe9a2397`  
		Last Modified: Tue, 18 Nov 2025 06:10:35 GMT  
		Size: 5.8 MB (5843338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2787cfe8fddfb0b3ab622c26664aaa7cae48714aad50d9ee8e1f8145550942f`  
		Last Modified: Tue, 18 Nov 2025 06:10:36 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:1193a818b4529e6c50a5a1ba9da5c67dfa4f431ba1c34cef60a14250340ba03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145841173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c06f76edb93febefd23cc66f2865a134ef6b67dc2a9b44accb9ac20207ae451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:08:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:08:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:08:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:08:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:08:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:08:46 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:08:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:08:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:08:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:08:53 GMT
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 03:08:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 03:08:53 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Tue, 18 Nov 2025 03:23:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:23:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:23:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:23:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:23:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:23:27 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:23:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:23:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:23:27 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:23:27 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:23:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace86575f3c58b0141fecbb81c176778457fabce3cc25630eed4ac320c8153e0`  
		Last Modified: Tue, 18 Nov 2025 03:23:57 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab64cffbdd98deafc2719190e3bb1c975bbbdde5494a9ea920e89d365a5eba8`  
		Last Modified: Tue, 18 Nov 2025 03:23:59 GMT  
		Size: 4.2 MB (4151211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbecf108aa616892f19650a0bf89a9297bac9a8e19c51f1ae7da911327f56efc`  
		Last Modified: Tue, 18 Nov 2025 03:23:58 GMT  
		Size: 1.2 MB (1220043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb3618a9619f0f78adac3fdf4abfde5f1c91b89d1d3eaf2cfa8ff8e3ffa14d`  
		Last Modified: Tue, 18 Nov 2025 03:23:58 GMT  
		Size: 8.1 MB (8066560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f366915ef4fbda133e2146af307c3f6c5861fdd43a0b645f4422dfa9578c43`  
		Last Modified: Tue, 18 Nov 2025 03:23:58 GMT  
		Size: 1.2 MB (1195048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b28f5aae9f1fe851c77236d3d6319df6c714015124e072c3773d43958de3eb`  
		Last Modified: Tue, 18 Nov 2025 03:23:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928803408a3d202f97eb93393e1fe87f8b3ddfdea44f0c971fadfe2a540c06c3`  
		Last Modified: Tue, 18 Nov 2025 03:23:58 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8beb84ed45bd70c383038281066438c440006438dd4b66bbeabee40443c90366`  
		Last Modified: Tue, 18 Nov 2025 03:24:13 GMT  
		Size: 105.4 MB (105430256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1445950acbc2b4518fc7583cd19783a8b69c8285bcc17c270ad551dae7b280ee`  
		Last Modified: Tue, 18 Nov 2025 03:23:58 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c82f62ac341f97a151a9b36e5006756abf7fd725901eb2a5aa88b119132e36`  
		Last Modified: Tue, 18 Nov 2025 03:23:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb5cba47dde6608d6e600e019708b9f59f0667defd319a4c49fac1d7a8843e8`  
		Last Modified: Tue, 18 Nov 2025 03:23:57 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df8fdf3a047f61bf0d310fdf6f1f6b173ef61ef55e36cf14c64bed7ca05840e`  
		Last Modified: Tue, 18 Nov 2025 03:23:57 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741aef8a4b350a160ad484fa96962b66c366f7e35a770a3bb8085873cba2d9dd`  
		Last Modified: Tue, 18 Nov 2025 03:23:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7788b9b9c6b4d3a50f4a8af5deb63a4f8468d7a29109d5f7c0c12b6a45d2ef18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e05ceeb6b11abe626115241495d507e144b1f9b26c96e79299bf8855b787483`

```dockerfile
```

-	Layers:
	-	`sha256:ed38f29b44c7b72211895300e3ee7096941cbaea7eb1dfaeaefef2949597cdb3`  
		Last Modified: Tue, 18 Nov 2025 06:10:42 GMT  
		Size: 5.9 MB (5857439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:493454476e33295632705ac2c71bdcdcc7853e91fd6e407251710cbaffc49148`  
		Last Modified: Tue, 18 Nov 2025 06:10:43 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:77f35096c610add0396d87422eb7acab36614a5182f4f867286ae11a254b294b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140925438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13287269bfe06e73a51d985cc3ceb3fd9f1e67b5d50bd7b1eccc131e3e0c926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:30:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:31:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:31:09 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:31:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:31:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:31:15 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:31:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:31:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:31:19 GMT
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 03:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 03:31:19 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Tue, 18 Nov 2025 03:45:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:45:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:45:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:45:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:45:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:45:04 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:45:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:45:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:45:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:45:04 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:45:04 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:45:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d500ac97fcbc2ed150e3c86372aa4fa92e58bc81f59019ec3c34da27209adcc4`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f62ad10e9639d6d96df0a9f02a425ca54d12c8dd018ffc7de2e9a3d104e0bec`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 3.7 MB (3742638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64026eb775a1f1012824c5f25c83522b182ee5406aaa3f814f9fbb126b49c952`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 1.2 MB (1215974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faa1c6ac42f9285215404f46b7b602834e168cf1ba324969f4e99db03978108`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 8.1 MB (8066463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25826a842790e062a81fdebff194e4d56fe01e67c16637267c783c35356311d4`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 1.1 MB (1067242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa0859687ed72ea7107b7b699970f239560fc9eff31a530cec56047be7b57b`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f2e531bebf2b06e9b9759541c27479e4542a0c089efb1e1b772db9bcd9509f`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0003fe19619a1c1a10102e4b6c9931a83a51c646c699bd46bd26226feddc37e`  
		Last Modified: Tue, 18 Nov 2025 03:45:40 GMT  
		Size: 102.9 MB (102878594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86faf2b02cf1fa0617e69c697aeea3f90ac94e02d867e544f4fcebdffdfbb410`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e52514016ff1f594b70f4d80512808b5fc45bfba40a8789779bdad308672d2`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41430aaf2ff0d06a7b0443524eecc9298394d791340c82c157802c435ba80043`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4cfc6844cf762331f906d0162ddbb57c05426adcb59b53157512949ed886db`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f862180d5f2398e1914300d6a815b77f59ddcb39b1b7fb70d03541f98fae79f`  
		Last Modified: Tue, 18 Nov 2025 03:45:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:819c496ef3dbc44a2f5dfde218e42480b94a468403a26c58f2941034a9bc98aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e72c258ba6a733aeecff5aff7d42a09922fec388b69e91eae49dc43883c89ec`

```dockerfile
```

-	Layers:
	-	`sha256:f6a0aa17c22cb2ee924c6eabe89058a810294103ac41bfd500b00cce8643eeb9`  
		Last Modified: Tue, 18 Nov 2025 06:10:48 GMT  
		Size: 5.9 MB (5856694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a78b0b585faece331bf2b670592e51e8800d40dea68f62689dc50ec75097ce1`  
		Last Modified: Tue, 18 Nov 2025 06:10:48 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:14809aba2989374f74d7328a52a77fb9ddd1c33f60fbb83f3f20fc037fc7ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150896681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4899ff330f80bb1b30d5985dd1415a366cec6d627e60c21e86b46b47b2d38e`
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
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 03:01:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 03:01:56 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Tue, 18 Nov 2025 03:05:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:05:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:05:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:05:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:05:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:05:45 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:05:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:05:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:05:45 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:05:45 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:05:45 GMT
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
	-	`sha256:4102688d44903167a19fd2b9ddf2921b2f61585bc653aee67494e786dc37532f`  
		Last Modified: Tue, 18 Nov 2025 03:06:20 GMT  
		Size: 107.9 MB (107875495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f3d3a0932895a981d2ebfcbc9ccb16d9dbcef81e1e9fcca23991e38f3d569f`  
		Last Modified: Tue, 18 Nov 2025 03:06:12 GMT  
		Size: 9.8 KB (9775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920389202867453633206114eb711ff6dd103de86be088da205f03316496cb3`  
		Last Modified: Tue, 18 Nov 2025 03:06:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378827b69d74b0344da8ff019d4804ee85f137ea035ed0f983a65a24296d8998`  
		Last Modified: Tue, 18 Nov 2025 03:06:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304ea7d37b43e19f6184c508d4678d7ab8a8e1633ef6a7b10be402b6d8488e4`  
		Last Modified: Tue, 18 Nov 2025 03:06:12 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f93c4a7806541f3f83f3a72af7da6c40dac8bf21c5165da6833850aa5f6efa5`  
		Last Modified: Tue, 18 Nov 2025 03:06:12 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:da10eb29a8e315d03fa99ba791af7d46be8584eda32b359ed7eb948ba91b9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd79cf663fd670c541141f0d8cc6207ff80e0738c4a1f2f307d9d5d28d9063c`

```dockerfile
```

-	Layers:
	-	`sha256:5003c3a407f2c1f315761ae82002c7b6eb887d27994ba4a4e54d9f7e8077bd58`  
		Last Modified: Tue, 18 Nov 2025 06:10:54 GMT  
		Size: 5.8 MB (5849649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e206f0244e8a06786b41030555af082e7ef3032558425939ef18e50cbd71e230`  
		Last Modified: Tue, 18 Nov 2025 06:10:55 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:f45bc180e7d4bc51038a88ef8b1e76b37a9779e4f5bb0b523c8ad99bc262088e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161593408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795c9153344e5c054c7645c37094bc91471d81cedf67bcb7fdd9dcf35ec17bf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:45:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 02:45:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:45:17 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:45:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:45:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 02:45:22 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 02:45:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:45:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 02:45:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:45:26 GMT
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 02:45:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 02:45:26 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Tue, 18 Nov 2025 02:56:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 02:56:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 02:56:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 02:56:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 02:56:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 02:56:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 02:56:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:56:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 02:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:56:51 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 02:56:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 02:56:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee757cebab5617fe390d8ba9028b3b203c5599e12f9d5a2bc1b29f977a6ea7a3`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085f0c360dad16731a83e41d53eab85713bbc5598c91bfcbc4b7c68c87457b05`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 5.0 MB (4965403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7da35000adb02717f5caa443e59ac9805fa7d45d387bbe957f25a1407f25be`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 1.2 MB (1218646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf4b503aa49205920a5849700ea19a2e2352ca6fad1eb64e661dd47671008`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 8.1 MB (8066487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4722368b8722131de75690c43ddc9440bb40fa3a6c4de1ba824ef3dc2d07d`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 1.1 MB (1137428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5d7f7983d1f1236399d1d92933179b73ebf18fc2e53445c52243ca002ed3f9`  
		Last Modified: Tue, 18 Nov 2025 02:57:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d1f4d29f08ce45681df9eedf83e5ba9c82123b1d48a567a185e6cecb3cd1fa`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e1b7717d34b9c719a74d8fa9b21cac2e79641cb81592a2ef9f39c294cf14ec`  
		Last Modified: Tue, 18 Nov 2025 02:57:32 GMT  
		Size: 117.0 MB (116975215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda2f69c4aa400a05d247312bcd648d16280123c5bd2e8db4361ec1d9b1c524f`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a235312fa5d7888707b688313f60e765f108e72ff4311cdbf5979e3dbfae546`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6adefffa839211ffcf74026920afa167c464a570dc859f6ae1f52163c54bd6a`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28717997f0e57472547a1fb937729a5c1e0c021fabe456e7d4e2e6f103ce6ae7`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400af05b9ce73e7f780cce7ad208d06d290be2cadad28237bcdde7cd3a781738`  
		Last Modified: Tue, 18 Nov 2025 02:57:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:44892d1180c4431fcb8f90d23a4958d42695f1f6460fac2943e7988324700820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ca912797befe068ae0089f8f383a32a43e77627480da23ba5c136dd43f6bac`

```dockerfile
```

-	Layers:
	-	`sha256:41aa1a430e8c2cd5b136cc7632b6e30589e8fffb7bbaabcee8af55a36eb1d826`  
		Last Modified: Tue, 18 Nov 2025 06:11:00 GMT  
		Size: 5.9 MB (5855582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a843c1d342250a64cee3d8b59132de6515148c9cde521b96d3e5ac7bbd42f702`  
		Last Modified: Tue, 18 Nov 2025 06:11:01 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:4a8dc06cc4a902d1e70ffd4089fdf7ff8ea5f7581a1cf3b6c5e0d941423b0658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151714542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f1dc8d670e53573d0f87941436f069c23d0e8f61a3a36f1ce0890178c4ee71`
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
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 11:12:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 11:12:52 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Tue, 18 Nov 2025 18:54:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 18:54:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 18:54:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 18:54:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 18:54:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 18:54:32 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 18:54:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 18:54:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 18:54:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 18:54:35 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 18:54:35 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 18:54:35 GMT
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
	-	`sha256:c51cf5cfe646d95c6587db212a0514902cc34eed0c94a54429fe7fa84a61e209`  
		Last Modified: Tue, 18 Nov 2025 18:57:01 GMT  
		Size: 108.3 MB (108295957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72db1dab3c3fbe70cd91ef07961027dd84d6a05a467e2f365f2ed1359730bb90`  
		Last Modified: Tue, 18 Nov 2025 18:56:49 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1403a3f76b75eb31381da48dfe971feafbaa588d07dfa10ac361b6c54c70a76`  
		Last Modified: Tue, 18 Nov 2025 18:56:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461a8b6b233d7848a6c65658ac628ac83b5d3d8952ad06b5500aa14b05587a6`  
		Last Modified: Tue, 18 Nov 2025 18:56:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41898f0e279ddd9860c05e30517c7321b1132c75ec20d50e004941a3cbcab5e7`  
		Last Modified: Tue, 18 Nov 2025 18:56:48 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c72af22e6c3d9d4888f152e481f79b323719dc6f93b27060c00a83b22a8550`  
		Last Modified: Tue, 18 Nov 2025 18:56:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8f52ddbdf3ccd71afd82a075cd6bdf1b08fe80bf7481514f28ce8b3436ae9de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e4bb15f01fca4138d3304f09aea9d1b858adab5b2e7d9969f00bd030e4329a`

```dockerfile
```

-	Layers:
	-	`sha256:7d50630e3c346c7cb37df7368bf89f25070d26e58c873ec92b546e032ae0f045`  
		Last Modified: Wed, 19 Nov 2025 00:08:18 GMT  
		Size: 53.2 KB (53161 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:1c33d84e18ca69cca7df8df25d75cb975424e2ce639d456e01c73d4bc426434d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165635417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fe385df93ee56e039f10e5ba9a1c1ec377ecf5d55515510bedfc2962653d35`
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
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 03:39:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 03:39:55 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
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
	-	`sha256:c4f4512bb6228dc2122e4dd8864b2522ff1a7f94b81d3dbcc410cefb4afdb5fe`  
		Last Modified: Tue, 18 Nov 2025 09:07:02 GMT  
		Size: 117.6 MB (117619184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfef78330de9b2c3aa3cd3f55e7ae53d90c1bb92c99f281487108622cf7a7a92`  
		Last Modified: Tue, 18 Nov 2025 03:51:51 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f91fc2d07d20ef60017c20ce2c356d108b920fcb9f238aad87870d5727ec8d`  
		Last Modified: Tue, 18 Nov 2025 03:51:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7e1ce5fb71f437f15bbeeb2c0270e36b269ed1aded155a6c2ee467b80f9e08`  
		Last Modified: Tue, 18 Nov 2025 03:51:52 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dc1ce00fade9f713f9ce0ceba90c8f7f92f835ccdd2831bff1770809d769be`  
		Last Modified: Tue, 18 Nov 2025 03:51:52 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d09745bf96c0b58bde508d1c7d0d24e34d15ec71ba608057d6381213a45a0ad`  
		Last Modified: Tue, 18 Nov 2025 03:51:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:857a84856e506afdff437635e5cee8ddc247d54d7f8d281588b329ad11403565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52d1da2024bc21453865fd1b328515277314ff7e7166624982ef096fd094513`

```dockerfile
```

-	Layers:
	-	`sha256:630400b2e8554bb0df21d1069d516d9264e748b44f8a791eed804f53f42eff84`  
		Last Modified: Tue, 18 Nov 2025 06:11:07 GMT  
		Size: 5.9 MB (5850699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44858cb0314f3e8cd17a12376ac714fd6a0ed27d55673398f5d6fef392fdc611`  
		Last Modified: Tue, 18 Nov 2025 06:11:08 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:a470ea54b8f7f699cef13259b485db8bcb7613b6ab3af3d8dc8dc53ff7773e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162086036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10512c603ab175337abf90d290242cf682c601cfeb586cc1d6dd48c95f50b87b`
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
ENV PG_MAJOR=15
# Tue, 18 Nov 2025 03:27:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 18 Nov 2025 03:27:56 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Tue, 18 Nov 2025 03:53:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:53:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:53:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:53:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:53:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:53:47 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:53:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:53:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:53:47 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:53:47 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:53:47 GMT
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
	-	`sha256:539f32b0d0d51a7c1de043287bb6ea858c19bb1e468cc6739efb2d3c787a25a8`  
		Last Modified: Tue, 18 Nov 2025 03:54:37 GMT  
		Size: 120.3 MB (120349319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bb2e0f959148bb15d9427fad3243a11feb7fc5e9f44f35a56390de5277c5b1`  
		Last Modified: Tue, 18 Nov 2025 03:54:24 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10cedc869c0de015f9488223a2392df9738488f0249bff3e688feb630b82f03`  
		Last Modified: Tue, 18 Nov 2025 03:54:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f42bd54c593be166795881768516155d94fb8d6620eebf03a5ebe629a6cc4c4`  
		Last Modified: Tue, 18 Nov 2025 03:54:24 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a459cfa30024315849530b83dc29b17f61b86b6cf627cf15ccc10312a9c6f9`  
		Last Modified: Tue, 18 Nov 2025 03:54:24 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f52b455dbfc672eb297df3c2064089448a63718669611a6d042038fae914d9`  
		Last Modified: Tue, 18 Nov 2025 03:54:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3977b9e818a9bc8d2488e29c4ebc342cfa884bcf18625edafc2be93f890704dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22743e02071e5de144c8b47e0fec8f5b47465ae8cff26d4efa79a6d71ff08ce6`

```dockerfile
```

-	Layers:
	-	`sha256:8545386a62601099c3477a805519c2dfb3a7b31f29f916e566ce8b865de1974a`  
		Last Modified: Tue, 18 Nov 2025 06:11:13 GMT  
		Size: 5.9 MB (5852058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdca2908f731c5af145d5af8137065b28417796f6d5ff6bb80d3a9fa044baa4`  
		Last Modified: Tue, 18 Nov 2025 06:11:14 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
