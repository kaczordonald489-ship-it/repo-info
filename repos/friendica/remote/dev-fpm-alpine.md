## `friendica:dev-fpm-alpine`

```console
$ docker pull friendica@sha256:de86e51d44d29538bd8ec1eb6ca786c97a5e1d95b065a3d5691b176303653a87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `friendica:dev-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:95f6e8956e3d49e07d1cab835ca4d1c97ae8c4906a8b8341644a5b50d29a7750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57234727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07dc16989475b7aa5c4820bd6a416c40c71d68ac9cf0118def88d1bbe2a60361`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:03:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:03:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:03:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:03:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:04:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:04:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:07:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:07:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:07:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:07:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:07:06 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:07:06 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 20:45:09 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 20 Nov 2025 20:45:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Nov 2025 20:45:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Nov 2025 20:47:18 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 20 Nov 2025 20:47:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 20 Nov 2025 20:47:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 20 Nov 2025 20:47:18 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 20 Nov 2025 20:47:18 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 20 Nov 2025 20:47:18 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 20 Nov 2025 20:47:18 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 20:47:18 GMT
VOLUME [/var/www/data]
# Thu, 20 Nov 2025 20:47:18 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 20 Nov 2025 20:47:18 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 20 Nov 2025 20:47:18 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 20 Nov 2025 20:47:19 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 20 Nov 2025 20:47:19 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 20 Nov 2025 20:47:19 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 20 Nov 2025 20:47:19 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 20 Nov 2025 20:47:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581d36e768dbacf5bdd194bbf9fe2fa06835e31f9daf22b51a674081d71bdbb7`  
		Last Modified: Thu, 20 Nov 2025 20:07:27 GMT  
		Size: 3.5 MB (3463770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5a3fcc2dd6a8286922bfaeb41e4f6c3e903acbb27688538cc48d05ce1b8ed`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6fa6edd4f26b32894cdaf1d71232133c5544f3071fae5df8ea7229d35630ea`  
		Last Modified: Thu, 20 Nov 2025 20:07:26 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6421ac3f83f664829c691279f8ee8a38a08a6b57633bf3322e0e06cfbb53ad6d`  
		Last Modified: Thu, 20 Nov 2025 20:07:28 GMT  
		Size: 12.6 MB (12625125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8994e0a506927e4635bd453fd1807827d89aed4075e656c4dd05c2a3d026c5d9`  
		Last Modified: Thu, 20 Nov 2025 20:07:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46564e0a987d7ad2cf420f22c1ebaeaa705ed03d3611efe60d1aea7040709b12`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 13.3 MB (13273057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5c27422ace307c473400f5e670e512119f50c8c7ea3abe0e073a1daf3e0481`  
		Last Modified: Thu, 20 Nov 2025 20:07:28 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90831669701bd29cf5ba9bd319e9c47ae19be5ed86fa0b99c7218630b2c343de`  
		Last Modified: Thu, 20 Nov 2025 20:07:28 GMT  
		Size: 20.1 KB (20081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0758fb508b003ef455a3cd0b29fb2e33b314b4b646e3949a249e1a02376ed6a`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcccce939e3c6ca05cdbdaafc21e2e4ee2923a75242bc8c5b289ca40a93955cc`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bb8231743bba91fd1a41ec90c0ee5f0b2203c94e466bc059c5cab554d08d5e`  
		Last Modified: Thu, 20 Nov 2025 21:31:23 GMT  
		Size: 8.8 MB (8763578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa70431b909337a825ff0f74a2decfcbe8f9eefb3436e3460f812bdfeda51658`  
		Last Modified: Thu, 20 Nov 2025 21:31:21 GMT  
		Size: 1.0 MB (1031309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da79eba0a7a6e16af9ab6740c84884b9c85e3c1a60feba98b19b3334e5c27aa`  
		Last Modified: Thu, 20 Nov 2025 21:31:25 GMT  
		Size: 9.8 MB (9829300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a66aa745864d69e7b6635e6e768e607e8b8b05aa6512f27512356a0f52df857`  
		Last Modified: Thu, 20 Nov 2025 21:31:21 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332586bd63164736e4caba22d358ee9153490476927848d9ba6488d6aeadda2e`  
		Last Modified: Thu, 20 Nov 2025 21:31:21 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf9def75dc8596e639c3657c1d5409ef4586ba014d9735173f34749ea18250`  
		Last Modified: Thu, 20 Nov 2025 21:31:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69d94fbbf0a4e925de9276ce885c329dc59d7450ba565667e0db96be0634233`  
		Last Modified: Thu, 20 Nov 2025 21:31:22 GMT  
		Size: 4.4 MB (4386670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355947c65a0034a9a09d7748da364a889333f47bc0ce147e8f48cdde096c900b`  
		Last Modified: Thu, 20 Nov 2025 21:31:22 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9136eb77e5148a40aa1608572964c830f32246fddc4df4f15c02dd2b993aff8`  
		Last Modified: Thu, 20 Nov 2025 21:31:22 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:70c61d3f0bc74063f5152fa5e85f1a8ea700c647fed2df4f461f888f4c19e9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba67ec5f1bf721d84d09bfcf7d202ab0f74d3f0f3f9717fbf76b119750bdb5c`

```dockerfile
```

-	Layers:
	-	`sha256:7d918e1619da408830d75aafbe60f4c20868a984542b5fcfadcba9daf156630a`  
		Last Modified: Thu, 20 Nov 2025 21:29:48 GMT  
		Size: 55.5 KB (55524 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:866b2e9880a0962c09e4b5058e5f1cbe4459892c2cc9ed3d1c8a691c33cafe7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54217741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c267574dd340493e95e3f213487dfa2b89e65eab3eef5b3b2569d8f64b547c4b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:58:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:58:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:58:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:58:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:58:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:58:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 19:58:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:58:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:01:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:01:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:01:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:01:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:01:06 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:01:06 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 20:26:06 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 20 Nov 2025 20:26:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Nov 2025 20:26:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Nov 2025 20:28:33 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 20 Nov 2025 20:28:33 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 20 Nov 2025 20:28:33 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 20 Nov 2025 20:28:33 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 20 Nov 2025 20:28:33 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 20 Nov 2025 20:28:33 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 20 Nov 2025 20:28:33 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 20:28:33 GMT
VOLUME [/var/www/data]
# Thu, 20 Nov 2025 20:28:33 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 20 Nov 2025 20:28:33 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 20 Nov 2025 20:28:33 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 20 Nov 2025 20:28:34 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 20 Nov 2025 20:28:34 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 20 Nov 2025 20:28:34 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 20 Nov 2025 20:28:34 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 20 Nov 2025 20:28:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc37df1221ed237d17e665fdd71dad79d915044e97eb493b116f73f9d73ac987`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 3.4 MB (3428341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db45bdb2468e503765c9317a985379e7dff83ad0c811221c15db1bbf8e018cf`  
		Last Modified: Thu, 20 Nov 2025 20:01:40 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc60ea8fc0e4b64ead950b75712383229d8fe7e62194157598a5a62b1edf736`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e2ac2e870149c9aa7689a095a9afe28608aefa5adf7dc4549e133b7bea3f0b`  
		Last Modified: Thu, 20 Nov 2025 20:01:44 GMT  
		Size: 12.6 MB (12625122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9290b68559d797a7a15ef80386abd14df48533137849e3540c0463ebb60600d9`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788110136de653a7035c8d38ccf47351a212fcaf96ad048ca936870c2e6ba284`  
		Last Modified: Thu, 20 Nov 2025 20:01:44 GMT  
		Size: 12.0 MB (11986225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e817bb5d5aa1d8c1a6e709834ea5d640ee9b80c74991f3e2a375ab63b620d7a2`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ed9ba8eaf79cc949ba58cd00db64c604868388cb83eeeccbef5095e1c3dab`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d59c6a492ca9530b3b1c03faca08b2c4b3c84e7d98ca25ba9e20e13140a8a5c`  
		Last Modified: Thu, 20 Nov 2025 20:01:42 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cabc0a8d2fc2e5fa2dc11f76250be56ae288e30ae342d64e79d4ca993ca6979`  
		Last Modified: Thu, 20 Nov 2025 20:01:42 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f4b19f21c55c87ec4e3918d36c9e5323b8d6318485b0de4ea9189b1903be0c`  
		Last Modified: Thu, 20 Nov 2025 21:29:50 GMT  
		Size: 8.3 MB (8250650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27362fa7229c6e4d18393403c22c689a27855ff0c3129778e302308ecd2abeb`  
		Last Modified: Thu, 20 Nov 2025 21:16:54 GMT  
		Size: 997.6 KB (997617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa2c580f82693bc1689f8ca5658161e3a459b484b04df7aa098ca5657749028`  
		Last Modified: Thu, 20 Nov 2025 21:29:55 GMT  
		Size: 9.0 MB (9024105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bccc211f1e80b0c90af2ccf624e3ba460c245681d5d29457228150133a90230`  
		Last Modified: Thu, 20 Nov 2025 21:16:53 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abb318d8769d196e496fc384a881f545c94c4ecc97e091e6caddc8d2a38324a`  
		Last Modified: Thu, 20 Nov 2025 21:16:53 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac5dcf0bd7805b6a288bf7c827c8618940ccd578f20f353ba7701f702a728d`  
		Last Modified: Thu, 20 Nov 2025 21:16:55 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db94f63766e64bdda71dd65a48b34cdee9667aa68a9588c929a11962a466d04`  
		Last Modified: Thu, 20 Nov 2025 21:29:48 GMT  
		Size: 4.3 MB (4342548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5d43728a08638503f86db345ecc6dcc900fd6eada111a185feb62c778d59e`  
		Last Modified: Thu, 20 Nov 2025 21:16:56 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bbe95252292d65fa1be535476854419da7c1452507f6ce75bf2b401adc24e0`  
		Last Modified: Thu, 20 Nov 2025 21:16:53 GMT  
		Size: 917.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:e4fb5a1811b38023147aefc48c896e1a5024082eccf0317e0b8d22b0fc409536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dca7009634823011a06aad25b2b203d1dcddb42ef47adc4b16ba80bf0299a3b`

```dockerfile
```

-	Layers:
	-	`sha256:1ca6b062c73ba38aa07c67ad32635a9c55d2a3dc84a68a9880326775b3c2193b`  
		Last Modified: Thu, 20 Nov 2025 21:29:52 GMT  
		Size: 55.7 KB (55658 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:da15d375b58da12a3c58d44c2b350a7840055e6900124471898ee339ab8631d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51934057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dbe179f4c93c7a4e045338acc3cf12d545e158aeae0294019da4015f2cde90`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:16:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:16:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:16:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:16:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:16:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:16:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:16:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:19:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:19:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:19:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:19:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:19:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:19:23 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:19:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:19:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:19:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:19:23 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 21:47:34 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 20 Nov 2025 21:47:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Nov 2025 21:47:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Nov 2025 21:50:05 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 20 Nov 2025 21:50:05 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 20 Nov 2025 21:50:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 20 Nov 2025 21:50:05 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 20 Nov 2025 21:50:05 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 20 Nov 2025 21:50:05 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 20 Nov 2025 21:50:05 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 21:50:05 GMT
VOLUME [/var/www/data]
# Thu, 20 Nov 2025 21:50:05 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 20 Nov 2025 21:50:05 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 20 Nov 2025 21:50:05 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 20 Nov 2025 21:50:06 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 20 Nov 2025 21:50:06 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 20 Nov 2025 21:50:06 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 20 Nov 2025 21:50:06 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 20 Nov 2025 21:50:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24006ca79b19813864910cc813946667a37fa2dcb1c183d771668a38685e9d79`  
		Last Modified: Thu, 20 Nov 2025 21:05:22 GMT  
		Size: 3.2 MB (3244419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492c64266c1e3e312d13a40ecbcfafa94e2856d0cfbe2789657eb0421c9dbd12`  
		Last Modified: Thu, 20 Nov 2025 21:05:01 GMT  
		Size: 938.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31c8a839b8e35d22d94761b3db7bf49c0d267e62f5c28d5acb586fa0e964518`  
		Last Modified: Thu, 20 Nov 2025 21:05:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f36284021159973665a155a90723b258caa120bb0f52604c8abf0157506c5c`  
		Last Modified: Thu, 20 Nov 2025 21:17:52 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524751bc1919023503d64e914b985b2ea6bed64c7b0690639a64b30324044ea0`  
		Last Modified: Thu, 20 Nov 2025 21:05:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e716dbcfaf71c1469c2a91f9b7873c7e22062af70a0fad98bedb6f88d383b56d`  
		Last Modified: Thu, 20 Nov 2025 21:17:51 GMT  
		Size: 11.3 MB (11293429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c518c819621305d7106c117fc83d873fcc37ac427a439a57f01fe102eff1ea`  
		Last Modified: Thu, 20 Nov 2025 21:05:00 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25612b4c22efa0e60f64fc7ed4064474319a43d6b8d1a82ba8a25d14211d62a6`  
		Last Modified: Thu, 20 Nov 2025 21:05:01 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d2d41bad136320446b1215475da892aa80d9f080685949d870d7d15031e4b`  
		Last Modified: Thu, 20 Nov 2025 21:05:21 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd8f42946365810d9e87af4f15833e2dce6cd5b847610ebd6819a5399d564f4`  
		Last Modified: Thu, 20 Nov 2025 21:05:00 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b9f3306ed1b7ee8a0cdce35c03194b247b488fd8f6521a3234c4f2b4876ffc`  
		Last Modified: Thu, 20 Nov 2025 21:50:25 GMT  
		Size: 7.6 MB (7628511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d298599322bcfb207459a1c62310d805ac71d291b8dd177433d2b9bdf937953`  
		Last Modified: Thu, 20 Nov 2025 21:50:25 GMT  
		Size: 997.6 KB (997598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71204f4102b561e8a2a84976f1b03ee4458b602a1b104f0376e245977d86f2e5`  
		Last Modified: Thu, 20 Nov 2025 21:50:26 GMT  
		Size: 8.9 MB (8916151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc48d66209f077415aa001a6cc08bce7b6fb46156361036a04850af39288110`  
		Last Modified: Thu, 20 Nov 2025 21:50:25 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83281493c23792d852c24ee22ca98f28e93ea5d96f1604e494ca726d888a1ef4`  
		Last Modified: Thu, 20 Nov 2025 21:50:26 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2fc309864976e73bb91e7ff941e39b930b40dfde96800a6d8280ad3e621d69`  
		Last Modified: Thu, 20 Nov 2025 21:50:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d28c176c3c74818ac717a42d049cd367b87b8de0d3dfb0d5df0a7e6a3204872`  
		Last Modified: Thu, 20 Nov 2025 21:50:27 GMT  
		Size: 3.9 MB (3948245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3065e7c723e36d51f8ab434af428faef2adedc549f1ee79b6a74a84cedbb003`  
		Last Modified: Thu, 20 Nov 2025 21:50:26 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311d1428d6ff409531a4bdf1557b0eee1d9cd63c296765a7510d01ea89dd72cf`  
		Last Modified: Thu, 20 Nov 2025 21:50:27 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:254bd9314f59edd18b84eb4c5c1ac0014b60d574f5bfc867919385c35c0902e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d183314771afdcc23333b0f6cf135c655de93d87cc4a760c908c46dcf6b62b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8ac41ab370057b1f51b68f5ff1951d5e82afd870728bdb3845b9d96b7f6b7`  
		Last Modified: Fri, 21 Nov 2025 00:29:56 GMT  
		Size: 55.7 KB (55657 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:0a9549e54725d8da0605bf0e3ea1c8d821e7f5a02e92a46e0690e7a333cb5c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57501609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3507c3bf2be3217c568a6367a26000fc95d3e543672aea34235e7e7c254f596e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:51:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:51:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:51:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:51:51 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:07:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:07:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:12:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:12:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:12:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:12:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:12:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:12:25 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:12:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:12:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:12:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:12:25 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 21:37:35 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 20 Nov 2025 21:37:38 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Nov 2025 21:37:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Nov 2025 21:41:17 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 20 Nov 2025 21:41:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 20 Nov 2025 21:41:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 20 Nov 2025 21:41:17 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 20 Nov 2025 21:41:17 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 20 Nov 2025 21:41:17 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 20 Nov 2025 21:41:17 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 21:41:17 GMT
VOLUME [/var/www/data]
# Thu, 20 Nov 2025 21:41:17 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 20 Nov 2025 21:41:17 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 20 Nov 2025 21:41:17 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 20 Nov 2025 21:41:18 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 20 Nov 2025 21:41:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 20 Nov 2025 21:41:18 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 20 Nov 2025 21:41:18 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 20 Nov 2025 21:41:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec9d497168c549f2247fd034c53ae139ca2119ecd169d3a5077266764ebcf`  
		Last Modified: Thu, 20 Nov 2025 19:56:09 GMT  
		Size: 3.5 MB (3466799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde06d6c5e70a5cd4927c1f451661d460ce59d50f974cfd99a3519403c77059b`  
		Last Modified: Thu, 20 Nov 2025 19:56:05 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c198bfe2eba5c7b8b21f18d0c4fdd9cad93e4814a31f7100bc8afb71b2465b`  
		Last Modified: Thu, 20 Nov 2025 19:56:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524019b6333c4e36a1499d6131d3324651f4924a560c3b305865bb94dcd94e`  
		Last Modified: Thu, 20 Nov 2025 21:12:48 GMT  
		Size: 12.6 MB (12625108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdbef2d2bb560ad1d6c0839bf15838b36b8c60fda6529f5df5db5a706dae8df`  
		Last Modified: Thu, 20 Nov 2025 20:59:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc2dd1281e4af866e33344fde1ab06f6772dd60a339f4143ef2793b835253e`  
		Last Modified: Thu, 20 Nov 2025 21:12:48 GMT  
		Size: 13.3 MB (13253989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e908f43d29d26402f2fcfdd92afe250a07c73344b45ae245383fb7d4d8cd61c0`  
		Last Modified: Thu, 20 Nov 2025 20:59:00 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c65f1e13f98b02c115418626c8ddb2104d45bf46522975ff99b42f7abc4e9`  
		Last Modified: Thu, 20 Nov 2025 20:59:00 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e716b32e913ac69abdfb20074604fe686a1079d6e0eac41cc23c1910504812e`  
		Last Modified: Thu, 20 Nov 2025 20:59:02 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53799599c74521714ef292d858efb3f79d299482722509361fb06f58a57f24e2`  
		Last Modified: Thu, 20 Nov 2025 20:58:59 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221504a068ef35b0c5c081151065b5cff567be0e8f19462dd96a630b5da1a127`  
		Last Modified: Thu, 20 Nov 2025 21:41:33 GMT  
		Size: 8.6 MB (8639456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a97e78d90bc80797c14736222b467bae4ea76b58e38b0ce311f147ddcc50628`  
		Last Modified: Thu, 20 Nov 2025 21:41:31 GMT  
		Size: 961.0 KB (960975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec8be0d774b139d1fc4cbdbff39551d27d999206e2a14a98caf3dea2fdf514e`  
		Last Modified: Thu, 20 Nov 2025 21:41:33 GMT  
		Size: 10.0 MB (10027223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c7ed0274962248e3997f560058946a1b49a87b13044b8618b9d99736cd97`  
		Last Modified: Thu, 20 Nov 2025 21:41:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e808e68b8da72d874e4187b7cd163f4c7019fe5750b9a24fd748296fc8dc6dd`  
		Last Modified: Thu, 20 Nov 2025 21:41:31 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a2ebb5947e9de862c60355c5228fb576f5ed64a081d65bd00a9b0687da6ffb`  
		Last Modified: Thu, 20 Nov 2025 21:41:31 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44b868aae4ddf329f086b8ae244be044b2abffed3d42d5139a33e193cd31db`  
		Last Modified: Thu, 20 Nov 2025 21:41:32 GMT  
		Size: 4.3 MB (4330950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e4f17d65dce86d40f4da3b13cf805136f5911dc0c7e857d2050c9f85d22051`  
		Last Modified: Thu, 20 Nov 2025 21:41:32 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ebe4a1b65b82a4ca42044cddc65900944e9f299044d8a07ec539b6f8f241be`  
		Last Modified: Thu, 20 Nov 2025 21:41:32 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:fa2ea1d9898e6377a0d40e24af98a66a853aeebd468d015f1f64344e0534d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ca3fedaec3127af56b54167178c8937a621201038622594deed3b8c53b6d79`

```dockerfile
```

-	Layers:
	-	`sha256:d4679a9dc957a2b32cf642b7829c165905c011ccdf830c34e402947786ff5c2f`  
		Last Modified: Fri, 21 Nov 2025 00:29:59 GMT  
		Size: 55.7 KB (55693 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:7788a758b1cc8e936eddaa65dab63c6400a3bbc9442c8d8bbe109d5bc25388a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57622549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb007573ea737d91131dcd671652a0c83b3715a4a09aa92a4042bfa42e921db`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:59:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:59:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:59:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:03:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:03:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:06:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:06:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:06:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:06:39 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:06:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:06:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:06:39 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:06:39 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 20:35:45 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 20 Nov 2025 20:35:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Nov 2025 20:35:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Nov 2025 20:37:59 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 20 Nov 2025 20:37:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 20 Nov 2025 20:37:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 20 Nov 2025 20:37:59 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 20 Nov 2025 20:37:59 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 20 Nov 2025 20:37:59 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 20 Nov 2025 20:37:59 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 20:37:59 GMT
VOLUME [/var/www/data]
# Thu, 20 Nov 2025 20:37:59 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 20 Nov 2025 20:37:59 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 20 Nov 2025 20:37:59 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 20 Nov 2025 20:38:00 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 20 Nov 2025 20:38:00 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 20 Nov 2025 20:38:00 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 20 Nov 2025 20:38:00 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 20 Nov 2025 20:38:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6509e3b357df36f52696dfbe328393531f7e3356e402d07e199f3d973331203f`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 3.5 MB (3522951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e039386f4b37dbfcbea789b4f5f316f5d4dd9d0e451b31a1f50c6386261e42`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39301bd5b5ff1a20465358c20a4027ac1a97efc27ed5ae1eac1a398cd9fbfbd3`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9b8b22c3cc05570c3e5f1b2db3e48b23575af4641a32dafe5be18ab76f2293`  
		Last Modified: Thu, 20 Nov 2025 20:07:06 GMT  
		Size: 12.6 MB (12625079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c291b968b60244e3558f345bfa1bc727d6f2d5da4a5c027a4aea79dfa32eb`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96cab2c2542154024f59b595ed51c6b720c5bbae58d98cf3c8a27f18cf71d0a`  
		Last Modified: Thu, 20 Nov 2025 20:07:04 GMT  
		Size: 13.6 MB (13583064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159b936d878ae45e15824dbc02adcd3e400e8c701b2188391638a842dc807f0`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c789ef3d045e4f68762afb1fb5f7381d73738745e97ac4379b88c6ca4da8f4e`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4cc9837f008b85ef99be633e259a312c1a3f68e82a88cd81bc14372daa7a2a`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df52ce8f9e5e399e732090e679cbd16c8b262bf513c841543acb861d3e3052bd`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78144ea5a2d23fb5fa5d12cb1217f816abe770fab5609c478db4d0297591c9f6`  
		Last Modified: Thu, 20 Nov 2025 20:38:35 GMT  
		Size: 8.8 MB (8847783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974f3880b677dcfeb57856a0d5a42e990af785acaace3028e9ab829f17b5efa5`  
		Last Modified: Thu, 20 Nov 2025 20:38:34 GMT  
		Size: 1.0 MB (1006322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0cea1cd39c2b1e6048584ded000db0f28e3cfc7d9257c091e6638f67a25767`  
		Last Modified: Thu, 20 Nov 2025 20:38:35 GMT  
		Size: 10.0 MB (10012508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b510eba44e91b239ade4ce11168eeae6cdd5a5fd49940c82939cb41f234c9f6`  
		Last Modified: Thu, 20 Nov 2025 20:38:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1536270e8621b337384608356c9440ced7a16e3f83443863ba12c128db059a`  
		Last Modified: Thu, 20 Nov 2025 20:38:35 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1845a6671c619a36f873ecdd9670ccb801c8d712634cf853009cf65bea15417e`  
		Last Modified: Thu, 20 Nov 2025 20:38:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d9a81d0fc5b5120226780581462a09a95f55aa4f3d667f0b622088c188f8af`  
		Last Modified: Thu, 20 Nov 2025 20:38:36 GMT  
		Size: 4.3 MB (4346490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7b1041048bdddab6fd26092c66b1ccf41150542fe1506af6e478408b44f661`  
		Last Modified: Thu, 20 Nov 2025 20:38:36 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6b0d9597465c739fed5a056240d4c8f4b22ce5e174ebd6afdb011eec0a2f2`  
		Last Modified: Thu, 20 Nov 2025 20:38:36 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:45e1ff206ace21d2a06a10916006d8a46c3fca6609cd1dfce0e3e5fd6971b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3667b630a8e124aa12a77d973a0b7533e4acb6ebcd68bf712ebf75b214cf8e9`

```dockerfile
```

-	Layers:
	-	`sha256:c4b2cabc8a74cbbfb3f7c4732a3cb9a9de2e85e487a450627f4f29a5fb2d34ba`  
		Last Modified: Thu, 20 Nov 2025 21:30:00 GMT  
		Size: 55.5 KB (55497 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:8a95367bbfd2513e989926d5bc4d2937e901a66d5cc195d61f4d8b0de63cd7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58188323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbe5dc46b450d99a4d4e83d4286b7e8526aec7c3d3ef3a8abd969325e23283c`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 00:51:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 00:51:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 00:51:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_VERSION=8.3.28
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 21:20:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 21:20:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:29:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 21:29:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:29:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 21:29:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 21:29:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 21:29:54 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 21:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 21:29:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 21:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 21:29:55 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 23:31:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 20 Nov 2025 23:31:54 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Nov 2025 23:31:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Nov 2025 23:35:03 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 20 Nov 2025 23:35:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 20 Nov 2025 23:35:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 20 Nov 2025 23:35:04 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 20 Nov 2025 23:35:05 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 20 Nov 2025 23:35:07 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 20 Nov 2025 23:35:07 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 23:35:07 GMT
VOLUME [/var/www/data]
# Thu, 20 Nov 2025 23:35:07 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 20 Nov 2025 23:35:07 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 20 Nov 2025 23:35:07 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 20 Nov 2025 23:35:10 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 20 Nov 2025 23:35:12 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 20 Nov 2025 23:35:14 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 20 Nov 2025 23:35:14 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 20 Nov 2025 23:35:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53971e004648f8982fc3b37775bc935a3e17a526dffea78cab354e2849bfd0d`  
		Last Modified: Thu, 20 Nov 2025 21:25:17 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd2a999bdbd1916d536ced797c2f38b0416bdf9b4e4d63ebb04063c3aefe64`  
		Last Modified: Thu, 20 Nov 2025 21:25:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ebd17c49beb1ea4ab18f7e8e27dcc03d329a184e14b1e7777d271f3777db7`  
		Last Modified: Thu, 20 Nov 2025 21:30:16 GMT  
		Size: 13.7 MB (13737190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8faaf33b461bd94b5b6b94ae859b9d46ed4b89bf9fedd33d4eba5039c7037af`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00983a40cc1e11404d5947d0d2295acd834ead990652b9e4560c1d79132f6997`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df143cd827d82f9423db96861cf0cd96f0c06bbffabc927d66ef1fc7096df2ff`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda55e1c6e511a0ecf8615a6eaf4bef9c53f19936f40e103ecc82630277c17de`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b95561fb0b374c5fcae5c92638b96886ab547908cab578c2527ed93d9811075`  
		Last Modified: Thu, 20 Nov 2025 23:35:43 GMT  
		Size: 9.2 MB (9196457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc9ded08bae9de81fabe2ff2864b660c4be38ad1fb7a9a3158375412c6c4d5e`  
		Last Modified: Thu, 20 Nov 2025 23:35:42 GMT  
		Size: 951.3 KB (951283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93135ae4173f83dd531dc3717b50bca2b7c0a6e345591ec341cd74302bee691`  
		Last Modified: Thu, 20 Nov 2025 23:35:43 GMT  
		Size: 9.8 MB (9833532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac52d316349580840ac064ea6a96dd6ce5c55662030fd822df940ef3139706`  
		Last Modified: Thu, 20 Nov 2025 23:35:42 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a6084245704e962683bd89bbb3c9d55ee5c3be5e08758580bd2a33577b0a5b`  
		Last Modified: Thu, 20 Nov 2025 23:35:42 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78547c52984427b1ec6e143bd9a2a3be4ddb191f295cc13ce169f4f9ff9d6d9d`  
		Last Modified: Thu, 20 Nov 2025 23:35:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b278b1101fec2fe8af0cabac2a6f9dbbb3546ed06f79efaf38078920618758eb`  
		Last Modified: Thu, 20 Nov 2025 23:35:43 GMT  
		Size: 4.4 MB (4438750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960b169ab9ea8628d1d94de06bc7e1624a27ab2699182f9f296d316adf99d259`  
		Last Modified: Thu, 20 Nov 2025 23:35:42 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d973930acceef0e2215b41a9499c8a20b3c90521d698ba16fa0099d82a166e9a`  
		Last Modified: Thu, 20 Nov 2025 23:35:42 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:a56d924d799c3ba971117678544a5bb81d76226e3dca80151ee5cdbcab4e619b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1d5f391fcabe02e0ca31f1b4a1e6958395ddd163e591a51d3a708a8cdc12ba`

```dockerfile
```

-	Layers:
	-	`sha256:1f76b8dc3bb2c38bd7118e1505b3eb1f7a2c45ea46c7e1fa4edc5badf1422238`  
		Last Modified: Fri, 21 Nov 2025 00:30:05 GMT  
		Size: 55.6 KB (55560 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:9b913efe12d90371c4d6254dd596ac635acea5e203c591839b5fd2e2cb7bd327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55775732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f3fb340feea14998da0927c9ede603d043d7076c0913468867ad50e0f07a0b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 05:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 05:22:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 05:22:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.3.28
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Sat, 22 Nov 2025 15:38:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 22 Nov 2025 15:38:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 17:26:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 22 Nov 2025 17:26:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 17:26:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 22 Nov 2025 17:26:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 22 Nov 2025 17:26:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 22 Nov 2025 17:26:20 GMT
WORKDIR /var/www/html
# Sat, 22 Nov 2025 17:26:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 22 Nov 2025 17:26:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 22 Nov 2025 17:26:21 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 22 Nov 2025 17:26:21 GMT
CMD ["php-fpm"]
# Sun, 23 Nov 2025 04:39:37 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sun, 23 Nov 2025 04:39:47 GMT
ENV GOSU_VERSION=1.17
# Sun, 23 Nov 2025 04:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 23 Nov 2025 05:02:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sun, 23 Nov 2025 05:02:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sun, 23 Nov 2025 05:02:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sun, 23 Nov 2025 05:02:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sun, 23 Nov 2025 05:02:37 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sun, 23 Nov 2025 05:02:37 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sun, 23 Nov 2025 05:02:37 GMT
VOLUME [/var/www/html]
# Sun, 23 Nov 2025 05:02:37 GMT
VOLUME [/var/www/data]
# Sun, 23 Nov 2025 05:02:37 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sun, 23 Nov 2025 05:02:37 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Sun, 23 Nov 2025 05:02:37 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Sun, 23 Nov 2025 05:05:27 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sun, 23 Nov 2025 05:05:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sun, 23 Nov 2025 05:05:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sun, 23 Nov 2025 05:05:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sun, 23 Nov 2025 05:05:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991964637c5dacf87db7d4b063b50de6a499256ab7e57a034d7fbb66130c70c`  
		Last Modified: Sat, 22 Nov 2025 16:32:54 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851189fe88fff06f1beb5b7e6faad5356c44b7bfc59f4b4a31ba142d162b867c`  
		Last Modified: Sat, 22 Nov 2025 16:32:51 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9230cf5bb38689b2e24c8ec7c384acac8d82dcf8fe8783c2a17b6def8faeb7`  
		Last Modified: Sat, 22 Nov 2025 17:27:18 GMT  
		Size: 12.8 MB (12767137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d22ed6dbe6db669cc5e7492eb5b8504eac7ea145fb4ded5496e5b991b0d558d`  
		Last Modified: Sat, 22 Nov 2025 17:27:17 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfee7bad0ca5b74fd533bae9e647537f5f3848f06d09746efcbd20c1f68e1f65`  
		Last Modified: Sat, 22 Nov 2025 17:27:17 GMT  
		Size: 19.9 KB (19865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42accf1cd02375116cc9944eb69398111c800df4f77ea8d93b74f90f1569757`  
		Last Modified: Sat, 22 Nov 2025 17:27:17 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8919d6a24c13538f8d3ff9294701857f1fcb2d186ae35b16e03b6ce255ab0751`  
		Last Modified: Sat, 22 Nov 2025 17:27:17 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be3eaa0deea5c226f452ef4bdda2b6d80db110b01ca296e8e3315ff925206ee`  
		Last Modified: Sun, 23 Nov 2025 05:04:59 GMT  
		Size: 8.5 MB (8547915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2752986f3b03aa0ba72d8e902aa412e1ee8c8b7c4cf048adfc04021ffe22984`  
		Last Modified: Sun, 23 Nov 2025 05:04:58 GMT  
		Size: 1000.8 KB (1000760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e726f79732c8e703241c8469e1b90af7af1a4e166f12b1fc4071c98890d4b`  
		Last Modified: Sun, 23 Nov 2025 05:04:59 GMT  
		Size: 9.3 MB (9258314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6087f2d044c1ddd276e2c2872108e4ca518c2ba0e8c6f47835a616dc309ed7d`  
		Last Modified: Sun, 23 Nov 2025 05:04:58 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa9d92dcb9273973b58d7ac3d35e18d88a165d81825da9deea2c96234c2698`  
		Last Modified: Sun, 23 Nov 2025 05:04:58 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54ce8f3b8b1d4f9ed019c1d616553e320d44d181a2cdc9ba85c1dab6716f2de`  
		Last Modified: Sun, 23 Nov 2025 05:04:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f645e9f2a53e5d6780f7b84cc6a4729cdccbb408642b795d9d6c32233068b16e`  
		Last Modified: Sun, 23 Nov 2025 05:05:53 GMT  
		Size: 4.4 MB (4401918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017c4693abbb620a6440c555a03a83731e6f15bc61a2111bcb440e2bc6da70b8`  
		Last Modified: Sun, 23 Nov 2025 05:05:53 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419b418a3926e7c4f152079bc0732753832334af5a200e987c201f878e3a95a4`  
		Last Modified: Sun, 23 Nov 2025 05:05:53 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:fc92dadbdce8ae709144ca3bbe0b95a059ef751a3d9ce8c6054b71bf73a1454b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c76b1af56dc93254418fb7886b9a23fc6839e1554759b6f0255119ecbf9647f`

```dockerfile
```

-	Layers:
	-	`sha256:043a8d1b4ad5529d089545120f0428f96a25c2f0217b1cba002526a258d51485`  
		Last Modified: Sun, 23 Nov 2025 06:27:54 GMT  
		Size: 55.6 KB (55568 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:719b3c846b1142e3a183a972ee9f5ce23f3a19c6888bd08bb5331e02d362058e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57516043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3a0b9f6917978d20bf8c7d5a7007745b1ff8e3e4d4177b7fc8d7e555863fd8`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:48:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 14 Nov 2025 17:48:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 14 Nov 2025 17:48:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 14 Nov 2025 17:48:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:11:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:11:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:47:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:52:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:52:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:52:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:52:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:52:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:52:41 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:52:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:52:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:52:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:52:41 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 21:38:52 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 20 Nov 2025 21:38:56 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Nov 2025 21:38:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Nov 2025 21:41:28 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 20 Nov 2025 21:41:28 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 20 Nov 2025 21:41:28 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 20 Nov 2025 21:41:28 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 20 Nov 2025 21:41:29 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 20 Nov 2025 21:41:29 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 20 Nov 2025 21:41:29 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 21:41:29 GMT
VOLUME [/var/www/data]
# Thu, 20 Nov 2025 21:41:29 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 20 Nov 2025 21:41:29 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 20 Nov 2025 21:41:29 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 20 Nov 2025 21:42:33 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 20 Nov 2025 21:42:33 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 20 Nov 2025 21:42:33 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 20 Nov 2025 21:42:33 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 20 Nov 2025 21:42:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf21615e7c59e15e1f62a5a7808d0f5410d99d33eb1fa9e2321034798c88c649`  
		Last Modified: Fri, 14 Nov 2025 17:53:52 GMT  
		Size: 3.7 MB (3692784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4246c35005445d4bbee50c8ecfabf7bfff37a35458ccab55f059ef588e7d1b15`  
		Last Modified: Fri, 14 Nov 2025 17:53:51 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cbf8f8851344a16a8334b41749b8f5de7602e34ddb78157ce3902c37e8a59a`  
		Last Modified: Thu, 20 Nov 2025 20:43:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c247a5593e1221a6d015cb4f96ffae67e1d2dc99228574ed713bc504ad1292b`  
		Last Modified: Thu, 20 Nov 2025 21:15:33 GMT  
		Size: 12.6 MB (12625128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484fcf9bd55b21ece798cfb747a1954931fcddd9f84d8768994b4f622dd43456`  
		Last Modified: Thu, 20 Nov 2025 21:15:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c336bf7c35208c2f44ddea792a1e9375bb16ba33e6192986091634fac4da295`  
		Last Modified: Thu, 20 Nov 2025 21:15:32 GMT  
		Size: 13.2 MB (13214353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9db0c567cb04d71830fb67e4ee1e1fb6dc37ab2b776f9cf91878fa4f1d3328`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032bf3f23f3f8b52b6bb6b36ec5126ea583f47dac060e0acf8b9435c14bec4ac`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 19.9 KB (19878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e312fe8b12a5384db61e662e16d3872e08e339d82b7ea9d89cf24e85b180dc2`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 19.9 KB (19875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce95a1304df61591b93a604356999c24f3ed863b111b0d5429baec808f4d79c0`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acaea0f50ccff460ee7aca8db57efeb0c186cdfa03275718eed0767ae43178`  
		Last Modified: Thu, 20 Nov 2025 21:42:06 GMT  
		Size: 8.9 MB (8913369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962c3d73088088734ac62ff348eaa9c3e0ccee9b87852d77ec26a8bc9db1121c`  
		Last Modified: Thu, 20 Nov 2025 21:42:05 GMT  
		Size: 995.5 KB (995494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f4a24cfe233cf4fe1f62baa2f7ee5f7b925fb11595ea774413fd2665f2c4b`  
		Last Modified: Thu, 20 Nov 2025 21:42:06 GMT  
		Size: 9.8 MB (9767786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103ec9cc87c6efc73dfc58ea6ced6b434208c1e42d2795edb06ff21f2350de9c`  
		Last Modified: Thu, 20 Nov 2025 21:42:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b71dc4f61efb1c9f0522dd1145329a4ec38a14a5557a4747498883fe2236b0`  
		Last Modified: Thu, 20 Nov 2025 21:42:05 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ad74215394521ceb4fd4d4b8ada9a8794ecc12bd07eedc6b6fcc6720b60cfd`  
		Last Modified: Thu, 20 Nov 2025 21:42:05 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713f72e79cbe220c6e7cd2c22786c59525c9a2a87312be614278ee0cbef24090`  
		Last Modified: Thu, 20 Nov 2025 21:42:46 GMT  
		Size: 4.6 MB (4598798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387b72f2aa3c8673dbb8653753e4f6fe053904762ef996944916de704f883541`  
		Last Modified: Thu, 20 Nov 2025 21:42:45 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694df817d4cb891f9b5dc233021bec775145fa090db78caa3dc521ab0ad4a33b`  
		Last Modified: Thu, 20 Nov 2025 21:42:45 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:15df515a58d1cd03434e3d69990c4aead4086067a37547abe935b4fb7faeee36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792754b1488451854f7a47309143a225040ff20991393ad9528991925ed949`

```dockerfile
```

-	Layers:
	-	`sha256:d945db3e0746e1decfdb4942f4fed15a5479ce24c0875b4fe8ce905eab6a3920`  
		Last Modified: Fri, 21 Nov 2025 00:30:10 GMT  
		Size: 55.5 KB (55516 bytes)  
		MIME: application/vnd.in-toto+json
