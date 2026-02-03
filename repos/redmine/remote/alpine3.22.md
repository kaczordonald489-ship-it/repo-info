## `redmine:alpine3.22`

```console
$ docker pull redmine@sha256:cc0b5e6325fd1f7c07fc587ad5ef6707b24112b0c1459f5c68af7ad0a77936ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `redmine:alpine3.22` - linux; amd64

```console
$ docker pull redmine@sha256:8b6da6368863aff9ce59e8e9ba77d272052ab007b8aaf72382894fde1ce7f2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190491979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f1e3d390df36aa18708788371334e0f66bb0d75b3f1d512d66f5a3e2422408`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:45:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 28 Jan 2026 03:47:46 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:47:46 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 28 Jan 2026 03:47:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 28 Jan 2026 03:47:46 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 28 Jan 2026 03:47:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 28 Jan 2026 03:47:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 28 Jan 2026 03:47:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 28 Jan 2026 03:47:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:47:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 28 Jan 2026 03:47:46 GMT
CMD ["irb"]
# Wed, 28 Jan 2026 05:05:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 28 Jan 2026 05:05:21 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 28 Jan 2026 05:05:23 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 05:05:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 05:05:23 GMT
ENV RAILS_ENV=production
# Wed, 28 Jan 2026 05:05:23 GMT
WORKDIR /usr/src/redmine
# Wed, 28 Jan 2026 05:05:23 GMT
ENV HOME=/home/redmine
# Wed, 28 Jan 2026 05:05:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 28 Jan 2026 05:05:24 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 28 Jan 2026 05:05:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 28 Jan 2026 05:05:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 28 Jan 2026 05:05:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 28 Jan 2026 05:05:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 28 Jan 2026 05:05:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 05:05:53 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 28 Jan 2026 05:05:53 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 05:05:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 05:05:53 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 28 Jan 2026 05:05:53 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae38ecc057d040870a59407515f5cf6138ba12a507513cdae725156c52a9040b`  
		Last Modified: Wed, 28 Jan 2026 03:47:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f4a3c341f5e18b81ead5e84ff491b1cb7a79c7351a55f1f901bda7b1397203`  
		Last Modified: Wed, 28 Jan 2026 03:47:55 GMT  
		Size: 39.3 MB (39277045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798de31b32e574208bf25391b409911c5bce5abec4451f7e574d98e7004c5fcd`  
		Last Modified: Wed, 28 Jan 2026 03:47:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91a4bbd345523e6916531596c63727b393246a6baa0548606d40a729572a172`  
		Last Modified: Wed, 28 Jan 2026 05:06:03 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451ca5b835d7aad8e39fe9363b14c0503ae218528a22a5cbad1360f86bea209a`  
		Last Modified: Wed, 28 Jan 2026 05:06:05 GMT  
		Size: 75.4 MB (75408202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061fcfbf98b45eca6befd05ab9d57bae591ebe75513f74e96992748d95e77e95`  
		Last Modified: Wed, 28 Jan 2026 05:06:04 GMT  
		Size: 966.7 KB (966729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb959e1d28de31434ad7dc60c16bd73aea9f1f5698b36f75753996c48cd079d`  
		Last Modified: Wed, 28 Jan 2026 05:06:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4d619ac740e21e8c5799f8adcff2d117ee4c0370581c516dc3c59ec8053d7`  
		Last Modified: Wed, 28 Jan 2026 05:06:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6ec36d1d47638e8febd4b5a0dc2a8f382c7d8b5c694aa25d6f0014d3d18617`  
		Last Modified: Wed, 28 Jan 2026 05:06:05 GMT  
		Size: 4.1 MB (4146122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff1e4074ca63cceef5575e71c72e4336bec7e531517dca7252eeab93d79c85f`  
		Last Modified: Wed, 28 Jan 2026 05:06:07 GMT  
		Size: 66.9 MB (66885091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8603bffddc21edbf9455f3d1081531d51bef772b8cdaa223a5ad234c3e33ac9c`  
		Last Modified: Wed, 28 Jan 2026 05:06:06 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:dedab460c6bc0b8d5d43db2bb039f2a4208471662e21abbd1eafab97befc5f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74656c6ad7f4703d96af73d8d298c6761a95daf9c276e44bfc40a83a2406b13a`

```dockerfile
```

-	Layers:
	-	`sha256:0c51ca203095859f8480062e7e1ed725caac77ebccbee7fd1ff678f70873e4bd`  
		Last Modified: Wed, 28 Jan 2026 05:06:03 GMT  
		Size: 36.7 KB (36748 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; arm variant v7

```console
$ docker pull redmine@sha256:2263f012d48d9a49f9d323cc4c487a5e716e3292396303d6c62f79cc837988e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194574630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef05b1ee0cc4cef5dea9d27390486d1ace8f14edb0dbd64a4a416c76631b748`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:44:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 28 Jan 2026 03:46:53 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:46:53 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 28 Jan 2026 03:46:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 28 Jan 2026 03:46:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 28 Jan 2026 03:46:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 28 Jan 2026 03:46:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 28 Jan 2026 03:46:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 28 Jan 2026 03:46:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:46:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 28 Jan 2026 03:46:53 GMT
CMD ["irb"]
# Wed, 28 Jan 2026 04:31:27 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 28 Jan 2026 04:31:42 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 28 Jan 2026 04:31:45 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 04:31:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 04:31:45 GMT
ENV RAILS_ENV=production
# Wed, 28 Jan 2026 04:31:45 GMT
WORKDIR /usr/src/redmine
# Wed, 28 Jan 2026 04:31:45 GMT
ENV HOME=/home/redmine
# Wed, 28 Jan 2026 04:31:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 28 Jan 2026 04:31:45 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 28 Jan 2026 04:31:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 28 Jan 2026 04:31:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 28 Jan 2026 04:31:45 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 28 Jan 2026 04:31:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 28 Jan 2026 04:33:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 04:33:03 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 28 Jan 2026 04:33:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:33:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:33:03 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 28 Jan 2026 04:33:03 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419ab4e85be015ec88337bf5797d2727372868f951850d0a129587a47d9f30e`  
		Last Modified: Wed, 28 Jan 2026 03:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a65abcf2b0f53e35abf3071f3b9290588de79dbeb45cc1b457039ada6f8111`  
		Last Modified: Wed, 28 Jan 2026 03:47:01 GMT  
		Size: 34.8 MB (34769474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478c644a7d6323edb237fc9640cb88f4aa58d626e71120ca50acdb6681f533b8`  
		Last Modified: Wed, 28 Jan 2026 03:47:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9474907e924da4e709554aeb0a2252454ab85096b520bf17a7cb9195c1d35fd`  
		Last Modified: Wed, 28 Jan 2026 04:33:13 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9ddfcf8f8d212001d4ee84ef07651f1d008a4c9e3afb1bca1702b82126d386`  
		Last Modified: Wed, 28 Jan 2026 04:33:16 GMT  
		Size: 69.0 MB (68990957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ddcd28bf91e84d0902c181aca5aaaf9b7b39c5c983a0491593fca7c3ee27d9`  
		Last Modified: Wed, 28 Jan 2026 04:33:13 GMT  
		Size: 934.7 KB (934704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404ffbc18bb5c198ba3ae7ea02763165b02381609fa3cfa2a22a12686e47074`  
		Last Modified: Wed, 28 Jan 2026 04:33:13 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eaadeb42c271465e784ef8c6c6691a6bc13fbf4a43bf2e7ed3eb33c0f127532`  
		Last Modified: Wed, 28 Jan 2026 04:33:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f44f5a6617d43fe9a24884508ef37bce88eeccc69b6204e4f531b880eb773`  
		Last Modified: Wed, 28 Jan 2026 04:33:15 GMT  
		Size: 4.1 MB (4146113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32a9754b2a96ed8d4a22250636c80d79de940932b048489422cf745fcc1b40d`  
		Last Modified: Wed, 28 Jan 2026 04:33:17 GMT  
		Size: 82.5 MB (82505840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7d9c8f4901b98ad5f3ac89265bfc4b21359fd2cab4ffbd603892c19593181`  
		Last Modified: Wed, 28 Jan 2026 04:33:16 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:f9924e34414122e9aeeccedbaf32fe08571c08992271ff87760d169f8485fcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ff96ecc232687ff11771affe12ec33f48b73b400b1de2ae12f4ba642f35719`

```dockerfile
```

-	Layers:
	-	`sha256:79708fb6531d02fe8473aeecca4f53f881a24ee1012e214fbe54e5b4109430bc`  
		Last Modified: Wed, 28 Jan 2026 04:33:13 GMT  
		Size: 36.9 KB (36893 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:9945ad1b7fd728b0b469dbb07d1c868a2b5e95e703ddc8ae84dc9667a097893e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190202797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244a64c9731789f06521b3667fa56628aef2315cb623a4f590d25b8b8efb2499`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:50:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 28 Jan 2026 03:53:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:53:22 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 28 Jan 2026 03:53:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 28 Jan 2026 03:53:22 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 28 Jan 2026 03:53:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 28 Jan 2026 03:53:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 28 Jan 2026 03:53:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 28 Jan 2026 03:53:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:53:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 28 Jan 2026 03:53:23 GMT
CMD ["irb"]
# Wed, 28 Jan 2026 04:53:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 28 Jan 2026 04:53:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 28 Jan 2026 04:53:35 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 04:53:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 04:53:35 GMT
ENV RAILS_ENV=production
# Wed, 28 Jan 2026 04:53:35 GMT
WORKDIR /usr/src/redmine
# Wed, 28 Jan 2026 04:53:35 GMT
ENV HOME=/home/redmine
# Wed, 28 Jan 2026 04:53:35 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 28 Jan 2026 04:53:35 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 28 Jan 2026 04:53:35 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 28 Jan 2026 04:53:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 28 Jan 2026 04:53:35 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 28 Jan 2026 04:53:38 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 28 Jan 2026 04:54:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 04:54:06 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 28 Jan 2026 04:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:54:06 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 28 Jan 2026 04:54:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793359ea8c36a04b4d584a7bddc6dbdca13efaf38780772be4aed22b2df87e59`  
		Last Modified: Wed, 28 Jan 2026 03:53:30 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51d694c3088aead5d0b286d39ea9ddcb893331fa28e273b50b442f5f0b3741b`  
		Last Modified: Wed, 28 Jan 2026 03:53:32 GMT  
		Size: 39.2 MB (39186897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0596614852d039ae4e31b9042f8cf08918ab0cc120b7bf008dfebf4316a987`  
		Last Modified: Wed, 28 Jan 2026 03:53:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d4584f4f6d65bfbf443e03412909678a173b97fb5184e190ca49749b435941`  
		Last Modified: Wed, 28 Jan 2026 04:54:17 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e4fd0b803fcdf3a6ba38e7555cb5859ac964dd8e2c3f93c15453ca781307be`  
		Last Modified: Wed, 28 Jan 2026 04:54:19 GMT  
		Size: 75.1 MB (75058951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476c7493432c802dbd010a23c823acfcafb76b068f1a8e0230e834f5450e5875`  
		Last Modified: Wed, 28 Jan 2026 04:54:17 GMT  
		Size: 922.2 KB (922195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbb187914d66ade3c9aa3ad500dd0221833525f3fb7707fe24ba093aff59c1d`  
		Last Modified: Wed, 28 Jan 2026 04:54:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1e55d9b1002303642d1ad752121c124890f3faa0360a941b96d1ad4b871cc3`  
		Last Modified: Wed, 28 Jan 2026 04:54:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f0d9f12c7c411080d3825f9386b4ddad5443ec19d329ea10115207fd1fd87`  
		Last Modified: Wed, 28 Jan 2026 04:54:18 GMT  
		Size: 4.1 MB (4146110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941d9af6fa999b9a65abcaae95c86729f9ad55a772a00052d1d47f07605abf7`  
		Last Modified: Wed, 28 Jan 2026 04:54:21 GMT  
		Size: 66.7 MB (66745212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097ea4356884532a1a577aa751fff95d398bf6f13d0367f96ff7a7627999278`  
		Last Modified: Wed, 28 Jan 2026 04:54:20 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:c3f9a4423547ebe66347210e3dc1b97cb1e5eaa61733d0aa10501749e05afb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475d7a94c6ee523b911dec96b18175c9ad63dc5c7742b423cebb411da244ec08`

```dockerfile
```

-	Layers:
	-	`sha256:b0a3a9399508eb0ed761752bb209bac56b2ce44577a34112bfd6795c73bd52e7`  
		Last Modified: Wed, 28 Jan 2026 04:54:17 GMT  
		Size: 36.9 KB (36927 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; 386

```console
$ docker pull redmine@sha256:424e41519b0cb7fd59601820ed13a7d0a3b0173ba0a58cdb89dfe6762b018051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (208047933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374df6d45fd5e42cb9b9baf7e6d9bef557493b8dc60a6a34eaab9553cc1e39bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:45:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 28 Jan 2026 02:47:49 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:49 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 28 Jan 2026 02:47:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 28 Jan 2026 02:47:49 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 28 Jan 2026 02:47:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 28 Jan 2026 02:47:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 28 Jan 2026 02:47:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 28 Jan 2026 02:47:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:47:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 28 Jan 2026 02:47:49 GMT
CMD ["irb"]
# Wed, 28 Jan 2026 03:58:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 28 Jan 2026 03:59:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 28 Jan 2026 03:59:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 03:59:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 03:59:10 GMT
ENV RAILS_ENV=production
# Wed, 28 Jan 2026 03:59:10 GMT
WORKDIR /usr/src/redmine
# Wed, 28 Jan 2026 03:59:10 GMT
ENV HOME=/home/redmine
# Wed, 28 Jan 2026 03:59:10 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 28 Jan 2026 03:59:10 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 28 Jan 2026 03:59:10 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 28 Jan 2026 03:59:10 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 28 Jan 2026 03:59:10 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 28 Jan 2026 03:59:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 28 Jan 2026 04:01:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 04:01:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 28 Jan 2026 04:01:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:01:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:01:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 28 Jan 2026 04:01:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224d236191ae30c3faf7e946d34300725c2afc0fce4911fec5d19b0b25b9ba1d`  
		Last Modified: Wed, 28 Jan 2026 02:47:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d111f348147f8878eec7a499bfd4c71c90bf8c981fe030b78b3c594a40eb00`  
		Last Modified: Wed, 28 Jan 2026 02:47:57 GMT  
		Size: 34.8 MB (34776296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94f292753c759376f88e955b622a8370999d9230c9d519bc6464292a772382e`  
		Last Modified: Wed, 28 Jan 2026 02:47:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7891a825053a1f8b2e5a28e3ad76c32ac50462489797d6a2aca7e791b405ac2e`  
		Last Modified: Wed, 28 Jan 2026 04:01:30 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c099ddde15bb706f455e1d33af9268399271f9a57c15be419232f1e2cc7dfe79`  
		Last Modified: Wed, 28 Jan 2026 04:01:33 GMT  
		Size: 76.2 MB (76187064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9d377b3a9ff9d538cb0348a254507e3d5c2a0efbda68aa37949ae51b6c9fd2`  
		Last Modified: Wed, 28 Jan 2026 04:01:31 GMT  
		Size: 939.2 KB (939246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa50ab53a9f06fc110faf5b3165daaf005879e4c2d0ab6e4c8cd3e449c1333ae`  
		Last Modified: Wed, 28 Jan 2026 04:01:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeb075cda5fd6fd72bf316e8088e96bc8c55cee4900f3a87272609386b79467`  
		Last Modified: Wed, 28 Jan 2026 04:01:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14ca1f7ba865ec700b229f6794b4abf9fa5ec145a0b756375d38c49e07dcd3c`  
		Last Modified: Wed, 28 Jan 2026 04:01:32 GMT  
		Size: 4.1 MB (4146112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde1126c57a5feab65f8e7e8b7376f11297ab653eeac9c15144c36b7e8b12cfd`  
		Last Modified: Wed, 28 Jan 2026 04:01:35 GMT  
		Size: 88.4 MB (88374570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4d7fe1fb01338e33cf77240a52283e4feb6ee3f624ac3ff22da984ff2bd32c`  
		Last Modified: Wed, 28 Jan 2026 04:01:33 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:17d38484f90b49597107730af4f9df690301fd6ff9efa1b1c6986258a4fd813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f4ae046e6bcc21f8b1a05c0299e5a5bda5fa4edf3ca24d8295c5f1e292096d`

```dockerfile
```

-	Layers:
	-	`sha256:f4a26a8e315d692c3add533744f28c77f346a7b3635b5b90a89359f2f4c76ef2`  
		Last Modified: Wed, 28 Jan 2026 04:01:30 GMT  
		Size: 36.7 KB (36706 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; ppc64le

```console
$ docker pull redmine@sha256:83617060c62f601d37a32f8c506d9d5a99c021e5d696ca54beada137e35be050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226659052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cedcacb21a28019311dad6275d3d98a604f15bc3a1a59cbe85860bf3fbec4aab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 05:33:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 28 Jan 2026 05:40:05 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 05:40:05 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 28 Jan 2026 05:40:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 28 Jan 2026 05:40:05 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 28 Jan 2026 05:40:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 28 Jan 2026 05:40:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 28 Jan 2026 05:40:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 28 Jan 2026 05:40:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 05:40:06 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 28 Jan 2026 05:40:06 GMT
CMD ["irb"]
# Wed, 28 Jan 2026 07:11:27 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 28 Jan 2026 07:11:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 28 Jan 2026 07:11:48 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 07:11:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 07:11:48 GMT
ENV RAILS_ENV=production
# Wed, 28 Jan 2026 07:11:49 GMT
WORKDIR /usr/src/redmine
# Wed, 28 Jan 2026 07:11:49 GMT
ENV HOME=/home/redmine
# Wed, 28 Jan 2026 07:11:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 28 Jan 2026 07:11:49 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 28 Jan 2026 07:11:49 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 28 Jan 2026 07:11:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 28 Jan 2026 07:11:49 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 28 Jan 2026 07:11:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 28 Jan 2026 07:15:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 07:15:40 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 28 Jan 2026 07:15:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 07:15:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 07:15:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 28 Jan 2026 07:15:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b148065c4ae4074e205b6b7da424bacd8677efb2ac39f53691bfa1bf9340aa05`  
		Last Modified: Wed, 28 Jan 2026 05:36:49 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073f366c664c96b047a750d8a49a94a954451b78440178f8803eab06e24f091`  
		Last Modified: Wed, 28 Jan 2026 05:40:23 GMT  
		Size: 36.4 MB (36430515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f99e6ca9928e1783a0d49197fcca8188aa8969968abb0f805511ede2a0929`  
		Last Modified: Wed, 28 Jan 2026 05:40:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8cab43f445c4b55b69dc880daf0f06a7b2577e8d14054fef6201edde6030b1`  
		Last Modified: Wed, 28 Jan 2026 07:16:08 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87d1d9110ea3585a680dfee150198163d78fa05a8a9091f103a29cd6ba83d9`  
		Last Modified: Wed, 28 Jan 2026 07:16:11 GMT  
		Size: 77.5 MB (77514199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1989e8baf6509c4f11125c11a88c90d4b81f20d578daeccc50cdcd28b6af760`  
		Last Modified: Wed, 28 Jan 2026 07:16:08 GMT  
		Size: 927.8 KB (927750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843099a930158db4e4adac20840db6dd90fef737e3b7c1eda2d2f9080c5293c6`  
		Last Modified: Wed, 28 Jan 2026 07:16:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be82cc89f06b505b204c951ddd0da4c52b1c5a99393886d164206ebf8a16a214`  
		Last Modified: Wed, 28 Jan 2026 07:16:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc340161457007abd47694c66018f9c58733102bc4c14f81fabf1bf3801d8c5`  
		Last Modified: Wed, 28 Jan 2026 07:16:09 GMT  
		Size: 4.1 MB (4146117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeb60ac961d037f0d2b60d2a8e002484be0ffa18478b0d0eaf53f87499e5df8`  
		Last Modified: Wed, 28 Jan 2026 07:16:13 GMT  
		Size: 103.9 MB (103902260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d9190feabb0415ebcc8c3697ef97ad30589dd3a5e82586da5b86d1ffdc056`  
		Last Modified: Wed, 28 Jan 2026 07:16:11 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:65eed53aed2e2cf10d0db0273367e9a84647ce186c5d2399e442c0d0896b0348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669cbcdc8fbc1b1e93ad25772ed5f11ab470314c05a4f3fb9624b6bfd11a979e`

```dockerfile
```

-	Layers:
	-	`sha256:90d254aed6ff9c80ee772b5dbdee38b8cbb64ed9d9a19cf46c72b2ad64d05498`  
		Last Modified: Wed, 28 Jan 2026 07:16:08 GMT  
		Size: 36.8 KB (36804 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; riscv64

```console
$ docker pull redmine@sha256:3fc26c80509b585ae70268a58428a610a1de4cb8114722f851dfc157a8509ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220752241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3899620577f8e489ae6e2c723a570e700d9ba175ef697177bdf489ea3eff0d27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 30 Jan 2026 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 Jan 2026 12:50:21 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 12:50:21 GMT
ENV RUBY_VERSION=3.4.8
# Fri, 30 Jan 2026 12:50:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Fri, 30 Jan 2026 12:50:21 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Fri, 30 Jan 2026 12:50:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 Jan 2026 12:50:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 Jan 2026 12:50:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 Jan 2026 12:50:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 12:50:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 Jan 2026 12:50:22 GMT
CMD ["irb"]
# Sun, 01 Feb 2026 07:52:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 01 Feb 2026 07:52:50 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 01 Feb 2026 07:53:00 GMT
ENV GOSU_VERSION=1.19
# Sun, 01 Feb 2026 07:53:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 01 Feb 2026 07:53:00 GMT
ENV RAILS_ENV=production
# Sun, 01 Feb 2026 07:53:00 GMT
WORKDIR /usr/src/redmine
# Sun, 01 Feb 2026 07:53:00 GMT
ENV HOME=/home/redmine
# Sun, 01 Feb 2026 07:53:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 01 Feb 2026 07:53:01 GMT
ENV REDMINE_VERSION=6.1.1
# Sun, 01 Feb 2026 07:53:01 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Sun, 01 Feb 2026 07:53:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Sun, 01 Feb 2026 07:53:01 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 01 Feb 2026 07:53:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 01 Feb 2026 09:09:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 01 Feb 2026 09:09:29 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 01 Feb 2026 09:09:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 01 Feb 2026 09:09:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 01 Feb 2026 09:09:30 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 01 Feb 2026 09:09:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a6b93dc6eaecf04c54f0cb941600dfeb716039790fa5d5f8e2df5091842ca`  
		Last Modified: Fri, 30 Jan 2026 08:23:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f766380267d2f50db01206f94a231880e7c825cc76e8c49b40e25d5be99f4d`  
		Last Modified: Fri, 30 Jan 2026 12:51:36 GMT  
		Size: 34.9 MB (34904611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be570ed4af4daaee3c64eab2421531e1f7ff6c2235cc50ee3e5bfff55449b7`  
		Last Modified: Fri, 30 Jan 2026 12:51:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f161af336b11dfce77fb0bb9a9dcf4fd52c8207993102dd872183d8f92c47`  
		Last Modified: Sun, 01 Feb 2026 09:11:53 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d759b58b3806d737e1dd3903b6567c54100618ac0cdd2329e976540ee8b2a81d`  
		Last Modified: Sun, 01 Feb 2026 09:12:13 GMT  
		Size: 72.3 MB (72327629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85450715698df677b3a9c4853be7f810ed42b5d6ad52ac9fce8ae713a8404f7c`  
		Last Modified: Sun, 01 Feb 2026 09:11:53 GMT  
		Size: 915.2 KB (915180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b3281038551e34a5fd2e933497d3138988700a1e462ce42f9cdd0ef6462f10`  
		Last Modified: Sun, 01 Feb 2026 09:11:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3b9ae485ef4f549a07d471511f2913050e77aea0f8aec601414093f060d443`  
		Last Modified: Sun, 01 Feb 2026 09:11:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c1a3c60c7cc861ef0cbac6bdc947817d1f567ffd03d6d2e6e32b0df6cecb50`  
		Last Modified: Sun, 01 Feb 2026 09:11:56 GMT  
		Size: 4.1 MB (4146121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4906d434f639697b99c1bbb028a09181d5bae55fb2198d91c4ba5184f9e95f`  
		Last Modified: Sun, 01 Feb 2026 09:12:19 GMT  
		Size: 104.9 MB (104937366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6524ef0bb4410ece9c172bd9257f082ad446dcd1436720f8675e7cc1e192d22a`  
		Last Modified: Sun, 01 Feb 2026 09:11:56 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:bd5e2cb66a5cea23f1606b2d1b62f880d8e916490349844b15c2cfe7e332e7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5775d4572f78d1ea5429bd3fc00fc845cee3954f1a26dc36b8f70b787d402768`

```dockerfile
```

-	Layers:
	-	`sha256:42d1d1eae03d2bf74a1fd9da650c4ccf20ffba73877124bbf86a6a19fdcbf9c3`  
		Last Modified: Sun, 01 Feb 2026 09:11:53 GMT  
		Size: 36.8 KB (36804 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; s390x

```console
$ docker pull redmine@sha256:ac0976ec3322f3ae886fd6c946f48630dfc5e7a29b18fcd3ddb3ea3c4cb8fde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222123056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686939ccb9a8f03151079343224b7e2411188612b2bcf587f055d3a0caccefea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:52:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 28 Jan 2026 06:55:23 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 06:55:23 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 28 Jan 2026 06:55:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 28 Jan 2026 06:55:23 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 28 Jan 2026 06:55:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 28 Jan 2026 06:55:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 28 Jan 2026 06:55:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 28 Jan 2026 06:55:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 06:55:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 28 Jan 2026 06:55:23 GMT
CMD ["irb"]
# Wed, 28 Jan 2026 07:29:21 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 28 Jan 2026 07:29:31 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 28 Jan 2026 07:29:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 07:29:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 07:29:34 GMT
ENV RAILS_ENV=production
# Wed, 28 Jan 2026 07:29:34 GMT
WORKDIR /usr/src/redmine
# Wed, 28 Jan 2026 07:29:34 GMT
ENV HOME=/home/redmine
# Wed, 28 Jan 2026 07:29:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 28 Jan 2026 07:29:34 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 28 Jan 2026 07:29:34 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 28 Jan 2026 07:29:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 28 Jan 2026 07:29:34 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 28 Jan 2026 07:29:36 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 28 Jan 2026 07:33:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 07:33:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 28 Jan 2026 07:33:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 07:33:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 07:33:11 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 28 Jan 2026 07:33:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22640a8a680be232d92e5fd0c4c071aaea6437b7d6bc260f35a91894a4fb5ab7`  
		Last Modified: Wed, 28 Jan 2026 06:55:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f9fa3cda04abfc7edfe005df7c4340bed2a302711034ad435d86666856119e`  
		Last Modified: Wed, 28 Jan 2026 06:55:35 GMT  
		Size: 36.2 MB (36220124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d418fef72248cdba8c2faec104c1488a1eb163f2485c4a7591729e5dc66527`  
		Last Modified: Wed, 28 Jan 2026 06:55:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c7db9ba77536bbb8c1b74d79a07322c6fa5d614cbc80cc5e02e7a58888d0d`  
		Last Modified: Wed, 28 Jan 2026 07:33:28 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c24b66e17078b4749f17100675de27b83334a7478527e1a17854ccb20cddc4`  
		Last Modified: Wed, 28 Jan 2026 07:33:29 GMT  
		Size: 74.4 MB (74420392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d0d8ffeeaca9391f494a438ecaa5d6bc99b5265f7fa3f82b6671a9dc8687c8`  
		Last Modified: Wed, 28 Jan 2026 07:33:28 GMT  
		Size: 943.2 KB (943171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c328feec93d02a04230b949dcf001a5465df3bf77d3bfca0c9e5acb64d20702`  
		Last Modified: Wed, 28 Jan 2026 07:33:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1905f81a42cb8688a0f4e9a4f0451ae4a7ef6f77bf3fda3619c28968d52ab323`  
		Last Modified: Wed, 28 Jan 2026 07:33:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4934f9811710e8c576eb3de0d64bd6cba9b1d2095287c4b360664d9ee1b1d2`  
		Last Modified: Wed, 28 Jan 2026 07:33:29 GMT  
		Size: 4.1 MB (4146120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fadc2c3f65b1261ab8f84d074757e0674d02e24c0a25331c38c22c03dd659ad`  
		Last Modified: Wed, 28 Jan 2026 07:33:36 GMT  
		Size: 102.7 MB (102738902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5db6fd3eee97e3b70758d9eed03babf3d9053d41d83aad4110ac8ecbc9d9fe`  
		Last Modified: Wed, 28 Jan 2026 07:33:30 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:3245b9679a0d9bdf13482db73368450fe12544b429e6ac301c62c508a1004e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad6f31cfde58fd33878c7e93c9c2df510b39a2bde5ab8eb63965fe17e2f3934`

```dockerfile
```

-	Layers:
	-	`sha256:2064fddefbd17391f34c31bd441f854cd9d7e96aa10adee52ecbb19e38e832b7`  
		Last Modified: Wed, 28 Jan 2026 07:33:28 GMT  
		Size: 36.8 KB (36750 bytes)  
		MIME: application/vnd.in-toto+json
