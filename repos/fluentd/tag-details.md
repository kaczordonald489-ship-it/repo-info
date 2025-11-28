<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.9-1.0`](#fluentdv1169-10)
-	[`fluentd:v1.16.9-debian-1.0`](#fluentdv1169-debian-10)
-	[`fluentd:v1.19-1`](#fluentdv119-1)
-	[`fluentd:v1.19-debian-1`](#fluentdv119-debian-1)
-	[`fluentd:v1.19.0-1.0`](#fluentdv1190-10)
-	[`fluentd:v1.19.0-debian-1.0`](#fluentdv1190-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:8680b920563192348ac191fdda16ebce739da1d9bbc6c42711ab9d04942a24ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:aabf6e4d72df07f72c6320798286e38cb4078985fba7993be976076dd19c9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a904b3458ff5a124387f32960dfa2db38c96553803b6f1ca1aa65f98cd5c1f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:11:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:11:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:11:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:11:04 GMT
USER fluent
# Tue, 18 Nov 2025 07:11:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb0562513a544d09b243cd53af17176ae058cdb46bab21dc80e6e0e176085ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 1.3 MB (1279393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2995c07ae76a079f87ad5194b6ae8ae189e2697989ee2ec3ff402c4bbdbaef98`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8b74c7e9beb752e09eab60f51bfed7d4156be9c8a4cb31e65c1c593e477ad`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 42.2 MB (42158682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50951878876ddf823dfebd9e0c1677361d53bec1ff62831466fd280b78c485e7`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d897148a18c357950ad15bea0e1575bef5fe1a2f87069f845f212cbbf20eb783`  
		Last Modified: Tue, 18 Nov 2025 07:11:19 GMT  
		Size: 6.0 MB (6044983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba720e6453fce022701e4eb9ffad635c1814d3646e93621dca69a3739535b77`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2aea49a7fcbe5821ef2d28fd99597cefbdc90bbd576c99309e18724ebaddf`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c767a526bd60d2327b413b7336b31b1a00d72bc533f3b78d5137370859a100`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:8cf6892824e97d161f124d5333687ef7b8eb6bf25f6aa2ccd03ef3a4b110b485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61709c4d165ab4eeaaedac4e4f88cd257d11b31708fbd397c45a227b866d23`

```dockerfile
```

-	Layers:
	-	`sha256:ee0b209bed1b2e569f4ce68fc851ee89e0ceb2f39e1afe579774bd04519a1711`  
		Last Modified: Tue, 18 Nov 2025 09:29:22 GMT  
		Size: 2.3 MB (2283558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2847675aad81b3637e07602402738b0ff18b4ecea6c1b1bf03ab8c53298839fc`  
		Last Modified: Tue, 18 Nov 2025 09:29:23 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8bddf98d29f007597c2419ece53918ed2a02b6807f244eba291b11a115ce2f`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 1.3 MB (1263024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce6e0d17644462250ed0239ef347ef83d3d46d91cc236e61f5d1ee58840ebe6`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dba72f3360e3a96295c7cea72647313a78f2723776a3e529d977bc6fb38431`  
		Last Modified: Tue, 18 Nov 2025 04:22:15 GMT  
		Size: 38.0 MB (37994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0930b6e7a3909c3d28136a1cc19c3a553fbbb2a2d33988cd25bd43effa0a140`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ffa87b2ef8721e0de3adac791ff08369238bf6c371e5932d6858ff86c97a8af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71020865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a309489b26daac336f6e6ea0d24e3a28b4da34d74776fc011a8ff429afb1d5c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:29:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:29:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:29:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:29:49 GMT
USER fluent
# Tue, 18 Nov 2025 07:29:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d8370801a134071a40fe32d3d2fa7e0e17d18b25e5289e7237638fa8e7778`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 1.2 MB (1236519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b3223558fcb7b7da07de149d35cb77b0270a5ab9574f7885d63190a335526`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053f0fd615ae9d3957c571c9b6d06b6a892f68a64ba86fcf53aa1540117bbac`  
		Last Modified: Tue, 18 Nov 2025 05:02:15 GMT  
		Size: 37.9 MB (37865819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f081e8cb5f13e31c833ade5ef8bd8bc86005b1083ad01fb5c19150cfe1b852`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444514b6beb7cb41d5a6d74e2f02a6bd8d9b0d67d264bddba5cf5602534aef97`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 5.7 MB (5706176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281d992d9d5bfb4e3f3533290ac4e747701b996dfaa51bf4a1887a3d63f237ff`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9cd3785a6ed6fc017c3d377c407e31815775d28357a6cdbd99ac7ef4ebe6a9`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7153e50f421f23ea30db7f22fadac8133b4cf09d65d0fd4c239fa763debfcf8`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:612ec81a16bb05c27831a6a67cf5752e4bc1c6d4fb51cf3ec02bc176489ce778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee842d899c723e51f00df47d9670b2ed70e0e106f38477cc61e408fec563880`

```dockerfile
```

-	Layers:
	-	`sha256:ac725726a20c2cfebd9dd7c4277a0d190b6fe2958362e143a17129d44928298c`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 2.3 MB (2284970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff089d2e69179495169d3e05de805a988e7d4ff76570a57563e87343611f0ea`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a222dc7e9ddd2a1a1e14eda8278bac79c4b69652f2db613d6a31ca5838ea10cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79579468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c4933f2d7aba9a6cf42193fd309996c735faf39323e3cc9ce2adf1bd5b099f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:45:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:45:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:48:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:48:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:48:39 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 06:18:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 06:18:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 06:18:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 06:18:42 GMT
USER fluent
# Tue, 18 Nov 2025 06:18:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623192602c00e918197dfe6e2a1def0175e7be0d446a268ed38b6b5a621d38e0`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 1.3 MB (1261685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5fe6e2e9edffda349665022b4300b140e6a85f15a0f7614134df0867bcd551`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c522fdb9fff298474b76a11223cdcb250793d0c701b8cf389c0375800c7d5c`  
		Last Modified: Tue, 18 Nov 2025 04:48:57 GMT  
		Size: 42.1 MB (42145706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907ba9f7c5e39a58b009710a158a43136020eb8b46dc729f4426b65e03945ab`  
		Last Modified: Tue, 18 Nov 2025 04:48:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e287744781de6ba7990849d817b7d56815ea27a555f9b632c53f48912e6a8625`  
		Last Modified: Tue, 18 Nov 2025 06:19:03 GMT  
		Size: 6.0 MB (6031074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc83efe024d58f7c0f2ae54f8d1ca24212b0426b3b9f4ed85cf9dc2d9b4f138`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987698c2ecdcb3a42d62e47e6006334377b7ac96ac221f15c83c4f57ac5e185f`  
		Last Modified: Tue, 18 Nov 2025 06:18:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7418657ce63265bb53e93a85647829e7204dc7e5e55c4d2f68d731d36c14d5d`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:63307458ba12a55d8d3c164970c0601563d734a19561d3591fbecef80b4c26f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e9a7edd5a56936df00b963c56f0cc56c6857e45e7994aff9778145c3ba6dc9`

```dockerfile
```

-	Layers:
	-	`sha256:6f06e5d3a4506938173bb5f8471b70bec3c02332e7399634d46d17a90e3cda2a`  
		Last Modified: Tue, 18 Nov 2025 09:29:36 GMT  
		Size: 2.3 MB (2283830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0189ec4797d51709921e626666d44a28d1468c0300fac9c5b0a809df6e7ca1`  
		Last Modified: Tue, 18 Nov 2025 09:29:37 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bef966be95a2220ea41b52e0e83a8a622f90c5f320368a5f0d7284a00c503`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 1.3 MB (1287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45ed37d5457ae44f5b9a372ecc7bde1dd97d5be333bac0f4030719c7f0eca`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402fa9c5b261b8af75a607827e3e965cc7ce4351d91e3eba319a98783514bc3d`  
		Last Modified: Tue, 18 Nov 2025 03:43:29 GMT  
		Size: 37.7 MB (37740240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3646abfea40cabe9f48dabaff87823bc4de7febc7191871f992e8cdd29e5cc`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7a353d0f79751c2dce8dee5b2fded32d60934117291b83ec3d732116e194ffce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81069474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c794d9c800335e31b8d79aaf1dca07460a1300dc3c2092262bbf9a3870de6a5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:28:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 00:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:42:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:42:47 GMT
CMD ["irb"]
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Wed, 19 Nov 2025 01:48:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 19 Nov 2025 01:48:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 19 Nov 2025 01:48:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 19 Nov 2025 01:48:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 19 Nov 2025 01:48:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 19 Nov 2025 01:48:21 GMT
USER fluent
# Wed, 19 Nov 2025 01:48:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 19 Nov 2025 01:48:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbe0cbe7af169b8d7859f452f051f576ef4653fffd19a193922bbf502224d54`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 1.3 MB (1309674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a0a74191697331846ecf6cc860ffede09eafae29280e1dd04f2379b2dc07`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a0cff339fe641e08a65a97169cbbb4be8d7c4819ff50a706f2ed826916747`  
		Last Modified: Wed, 19 Nov 2025 00:43:23 GMT  
		Size: 39.6 MB (39601439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923e173b58f16848269bd5ce9e04bacdfaffeebd5dac19f837456978574583d6`  
		Last Modified: Wed, 19 Nov 2025 00:43:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fcdb627de74f9b8361edff9525a0fe6a33fdd953adf0fb2c0e3b00f9613e2b`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 6.6 MB (6559103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f259062e3fb7ae4681e323cc9047c9e3d00852e2125d9e493ac1ed5b8f53e103`  
		Last Modified: Wed, 19 Nov 2025 01:49:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ddab9ad7d500134abea5277fd0c7912069edbe26baf3a161f5b021d156ec75`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f4db3acfbcf50daa96589591259155ba6cc7fca7753781f8345d4843f6f05`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:0730fbfa8014170ddc03be28fb1510037719c10514d7d5fb2f1ef694b66c9130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d1a4b27f5bebde2aadf39b7cfcbf1cbb93710322c8c18ee5f819d0ff0b4bdd`

```dockerfile
```

-	Layers:
	-	`sha256:692608745c585b5c51accdf3fb05f15ad958b401f00e1950d21c6de48529e978`  
		Last Modified: Wed, 19 Nov 2025 03:28:34 GMT  
		Size: 2.3 MB (2287093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6aad5bdc16681e7da44fc798332bef9931f9d15dd9899bd0d5f9f49af36bf2`  
		Last Modified: Wed, 19 Nov 2025 03:28:35 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:683484cc5debca5c0709f0c7d2d978e76f78712ebc852b4a4adc005d46ec25d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76835164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08e6e4b2bfe39b06d532dd33389c27a98d33b36b8e7146d75800194d194dc41`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:14:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 07:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5be0006390772cf7f9022344d107d52c9454ddfb26a9b6aa53e4f77a9bdc5e`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 1.3 MB (1294253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df3437f72c81d0de5473522e48eb46cf20ee4ae5ae981dfae54b48d71b07c5f`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67960768c1f544671789085d4901deaf00ad13d073997065fbd38e41baef3e`  
		Last Modified: Tue, 18 Nov 2025 05:17:09 GMT  
		Size: 39.3 MB (39287189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de67f11ad5b13189744a053b706d6a38590793d5b547a05561143636a6e794`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b6ba71f42284c745b166f743e6e50d1f0a6854eee654f4eb7cf742b48e808`  
		Last Modified: Tue, 18 Nov 2025 07:35:44 GMT  
		Size: 6.4 MB (6416958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d87c11925f40d6e2afa5a002fb413adc618d32a4c1f33ccd48c47e23b57b7`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082eb1114230c4c0724b38d35ab1fc4eee657526608a13dd9fd5d5e8a4a21bc9`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ab1a0cf3bc37e55bb698b7e2e76edb0e4cea56577c12907c808a17c957928`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:3f8f214fada39a1a20d17924da461fedbaf16aecfbb0fa7591a3bc3b6bb69094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9677d7cdb6034256be28e74f6dfe5c2324badba6517a6567ec886a568e1a826c`

```dockerfile
```

-	Layers:
	-	`sha256:88a33b325036b2acdcbf4c3afa0c4f5711c06a125a88b8e4dddf20ed68e32d37`  
		Last Modified: Tue, 18 Nov 2025 09:29:45 GMT  
		Size: 2.3 MB (2285003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ed799d8ee14c02a6e9a62dbc69e63a23d15a697ba91568efc436ace9eb3ba1`  
		Last Modified: Tue, 18 Nov 2025 09:29:46 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:1ad8ae3e827a63e119717cbc995ba416165edf47f802f35d9ec3a28b90874351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16-1` - linux; amd64

```console
$ docker pull fluentd@sha256:afa3a57d73c7c0768f7045af02ff38c7956371261c95b23e523e6496fbb180c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17383642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc6b44e684e6309468eb956f3d4740cf12ccb8c434b97a188b29da64c20b70e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78331f707c6d9910019296ecb4ab44f9b26a450a37e504c48be8963ce9a043`  
		Last Modified: Wed, 08 Oct 2025 23:22:10 GMT  
		Size: 14.0 MB (13961663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba1f53d18cef4c44a0dbd3daafb62cf57107f7f532fa0f57ef1b22d0af51e7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed50b040b930bc5d13e08cdd1df716af2d3ff029e5b6b134e3e2fe71fad714b7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22932eecf8769ce42b56b0bc4a4f283b4d97f1f07d7f98efacbd1a1357ee27cd`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1769926942992a983f31805ed3a13d0406f50533e68b3d4d3236fa5963c45d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.2 KB (986159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53218b2014f588519fb6edb485d5b9268070ae8f517d0500d83a0f5a95462041`

```dockerfile
```

-	Layers:
	-	`sha256:3026734faa929ea6d5e52a4a4265ccb061d0836149b6fc9ef2bb6c9c7c6865c8`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 972.5 KB (972483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3dbf40f2c01bb6ecdda2f44a969772b89c46c3166fe5663350921ae5985e8e`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 13.7 KB (13676 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:46ac9bed32c7a8ce49660a59a52f753eff30538835dd611d22bc1f7934b37c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16137396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f885d67ca4b1bd990fa3007f4cfafb8bf90d6e39ff2be76552973966350f4fef`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-armhf.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:93e88a4aad08082395ce41ebaca8e4678e1148db5e8947e4c39599181a9ee4ba`  
		Last Modified: Wed, 08 Oct 2025 21:25:16 GMT  
		Size: 3.2 MB (3176528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf77ba4c6a48f3bacaaf9db6e676cc51c8898bc17f98b43aa29c349ccd9250`  
		Last Modified: Wed, 08 Oct 2025 22:39:21 GMT  
		Size: 13.0 MB (12958702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e42f64ef5aafe9d9b3ab4319844beb84a50b007d02d84fa103521d60f2f76`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356c473ad81afc625e1af60d0c4ebf7c05152d7ea626b9f0c7875590101fae33`  
		Last Modified: Wed, 08 Oct 2025 22:39:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a4607d2da40a11eda63339c19317510928a2f1581ea6f29a6b9c0fe011d0c`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b1047a7ef72278952bd72515b06df4c47777ce18d0446c239adb2f9bdbe2e14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42935ff90a0ef9a2f68edaf9040d29def17f626d3c04096f9c92178845c3629d`

```dockerfile
```

-	Layers:
	-	`sha256:8015c3aa7387514211e92d6eee02a313c10bc707bafd172c2fd61a50d1311754`  
		Last Modified: Wed, 08 Oct 2025 23:28:29 GMT  
		Size: 13.5 KB (13539 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cef7f445d8c75f71a73b9c9ad0332a2c194fe935d3058f588c8dec4155186ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17368912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff98b6fa62f0c15cb2289ed831b50b438d943fc9324f96ee47ec3bff51bed3f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeb91e752132813c432d89f1a8dd1db5120bd0a105f5482c692c4c90eae17b3`  
		Last Modified: Wed, 08 Oct 2025 22:11:12 GMT  
		Size: 14.0 MB (14007447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df20c8f62a7ff47af002767397639763517b507053d3be2a607ad7cf039699cb`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8b09660f0729b33efa9eee73345d6e2574e683cff98f8189145136dd26dc4`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44991f0a648880052ce599ae6dc1fbcfeeea9db841398e692d720adc561c80c6`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bae4897fe1e09f33a0cb1995e2844559c6203a2de785f07457545055b868b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.4 KB (986385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93150014baf1f5b57526e2c5af7aea24f24a1f05f7958a7233428da7651d9dd`

```dockerfile
```

-	Layers:
	-	`sha256:67aba2f8a082f4bcbaa1ad6fc530073640b1b7742fa155f2fb1f96d7658cede5`  
		Last Modified: Wed, 08 Oct 2025 23:28:32 GMT  
		Size: 972.6 KB (972613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3629a5d26b2d4d23396554cd8b33525330b75f331ee1a61a6aa7b7b2bef527`  
		Last Modified: Wed, 08 Oct 2025 23:28:33 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:6a013d0b1dbe71756026d1ef1f8f07abf0ac51ead8815af66109c1a01414e18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16345474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dbc71c5e074c89edb50509532f4fb4a01d3e9ff2595e95a5533b13db016c55`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:29ed29d5a2d3bb6de33b2b4bc58a076a8bccb81beedbcc013e38338640c314cf`  
		Last Modified: Wed, 08 Oct 2025 12:04:10 GMT  
		Size: 3.3 MB (3254171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c29c80768044ac9f47738f5ba63e8f540639a570074a5dd04bc400d0468ebb8`  
		Last Modified: Wed, 08 Oct 2025 21:46:08 GMT  
		Size: 13.1 MB (13089135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e224de4549cda25d841df269ce3e9b86cd0feb6ef1703b75cb32524bedafe1`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1061097b93842eedc8d7863fc0608dbd3490771b515873cc3329b5cdc8fcbd`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba5a6e02037353ec4b014f170080310354e526bc797bfe200c2286eedaf6ae8`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:755dd01070d905860704626ff1d1155994b4bf042e5aab8aa38bca75857fc293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.9 KB (982887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc6d533e4a0d8a4e7117c42fd122fbdcec92426815b69d138847435a5f42c2d`

```dockerfile
```

-	Layers:
	-	`sha256:e17fbd8db09214885631e52c7f3ee862a494b742523bb8f6acb292439080f164`  
		Last Modified: Wed, 08 Oct 2025 23:28:36 GMT  
		Size: 969.2 KB (969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83c293b83d79cb70ba9c955cedb86fdc401f653cba99c68d22f9fa322bab621`  
		Last Modified: Wed, 08 Oct 2025 23:28:37 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:62eb94d5f8bab0352fe1bda6749f90795526e823846751875ed5078f2f8704b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16932429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b60459341330d9f4e3d27c417ba023f6fe3fb7b0846fda2d34e07b63e813c3c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-ppc64le.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8615c7c09f59391eedf1644cf56164e9680a9e5f673fc84abf83944731c13b07`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.4 MB (3364466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd729167cc2a515dbbde613e7ae787652d091f0141bb5881d946a962a54a4b4`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 13.6 MB (13565797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae39192a12d7e6272184f7dcbe45d1241c964aafe748d27068d19340c408c9`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58128b57f286f34d4522f0e60a4be46c9fad0ee0dcf950dc879b1dcf511804ff`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63d13a8c0219e4550fb93a4d23eb5ecebf4f0cb4dbf998c38c7538a6243f718`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:23f4110435b3c619f0c6dfd9bc4b503e4d1f29f43cc89d63a31362be157e36aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.7 KB (981716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e38f607b22ca7f6244be9c7241bb070aeec1e5087b0cf13bf0ac887e0dde105`

```dockerfile
```

-	Layers:
	-	`sha256:ab9c1e7d5cf37454b207e160b91793faa0c78f73788b2c5eb29bd4c53c8b6970`  
		Last Modified: Thu, 09 Oct 2025 08:28:29 GMT  
		Size: 968.0 KB (968006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ccd55a5597ae933a84d99a7a7f1903f8379b62a381c32ab960f5b9cd3b64b58`  
		Last Modified: Thu, 09 Oct 2025 08:28:30 GMT  
		Size: 13.7 KB (13710 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:0b41672737621c0b4d9636f2680dc26702a455105378c6fddfde27ccd0dc7754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16767969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55cf05ab6ec22da0c19bd4f8545dddd8e4be8caddc43341112665a1915a7201`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-s390x.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:913efc36ec133ccc056e722147d93d8138aa999785d2ce858104b0c2d0e78fd6`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.3 MB (3253007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd32227ea6240b7d955081f56cf0e5cc573c44dd77407da8bb53c063ab87b71`  
		Last Modified: Thu, 09 Oct 2025 14:10:11 GMT  
		Size: 13.5 MB (13512798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fab613ee49849eb1192e5b5aca71cbeabae4d8c9ed4297bbc7070c859d579b3`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1655c318dd63d9aadb21ad09dc3762229e1cecd22e44d14c481db0c808efcc1`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed09bc671cc79a80b0e31f178bdf4318f525b2880e56c471dffebf3a859f886`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:48b41953e35001058187fa9db056f5f99dd35a109572db363ed221550ec063b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.1 KB (981071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab11aac5ad8d7f16b2e926d62908dbe2278ca45cffe6b3527a559b15741ff15`

```dockerfile
```

-	Layers:
	-	`sha256:370521b0c1295049f7e15fcdc00056580fd5959e7fb0423f9759e0b2cd663222`  
		Last Modified: Thu, 09 Oct 2025 14:28:31 GMT  
		Size: 967.4 KB (967396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129be691f47d14c09692973c170d7b9564fd1a2535581688d141759c73b4a009`  
		Last Modified: Thu, 09 Oct 2025 14:28:32 GMT  
		Size: 13.7 KB (13675 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:0092223659683b5aa193a2bb2439b156b3d91e0017941ec2541a9ce0246ed6b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:adc32d59b13596bea4e0c47cda19e01de34a450fa3131e5eba9752b6d7f0cc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81975913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a1f69a1e4a41ac657f4a49b214232a65121e6640eedb25d175a88d5437116`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:01:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:36 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 06:03:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 06:03:36 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 06:03:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:36 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:10:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:10:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:10:22 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:10:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:10:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:10:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:10:23 GMT
USER fluent
# Tue, 18 Nov 2025 07:10:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e866b3193d2e6441b53636d4e28f58cf0d3bddf19ddcb1d61e0699552ab9892`  
		Last Modified: Tue, 18 Nov 2025 06:03:53 GMT  
		Size: 3.5 MB (3509694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660fd9d37538af993f94c911cf40fdd3f65887f00bdd3b02d5f6beb5575f110`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdf0cffb9c947b88141a6cba3cd7d029546ad9e7fc7738ed734520b77518834`  
		Last Modified: Tue, 18 Nov 2025 06:03:58 GMT  
		Size: 36.0 MB (35963790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb63ff945397c57afdf5357fc26230f517e828b379cdf66f18775e111560dc31`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468107321d5436a93897728b385869239ee0171197567d4c9bf4a7dc9bdd1bc`  
		Last Modified: Tue, 18 Nov 2025 07:10:41 GMT  
		Size: 14.3 MB (14271585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c9825ed723b1fd916d8601339d6b14ae9cbae397538a507ce9ad877d758727`  
		Last Modified: Tue, 18 Nov 2025 07:10:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf7111818affb5fcd616da180926cb9857a507cac1cd3e77be9ee669ac9a62`  
		Last Modified: Tue, 18 Nov 2025 07:10:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48db7a3726ac5725adb9de367b5037b8cf7aa782f1089c49a6a909282154891`  
		Last Modified: Tue, 18 Nov 2025 07:10:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c8916a8d7c83e36810ad724c22c5b003e00a59eb417685fd7e4614355adff2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af096d5aa78541edcbf14961dd92a8aad9460b4160f6e4d5a9dbb314bbe814f`

```dockerfile
```

-	Layers:
	-	`sha256:d334dd7417fb839e1656a8f2c7f7104476699fb6abc97ea2b859656c49853659`  
		Last Modified: Tue, 18 Nov 2025 09:29:37 GMT  
		Size: 2.7 MB (2668452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623ec4a7af11708575a06aee0539e27d050a33469d4aae769dfc51d944138074`  
		Last Modified: Tue, 18 Nov 2025 09:29:38 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:15b64e0fd4162ae5d056943a22573ca147389050286521bbe2f4d760d17567e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cbac93bc99cc5fdfab88c444893f98ff5d71a0fb527121625c23a624161031`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:34:04 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:34:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:34:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:34:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:34:04 GMT
USER fluent
# Tue, 18 Nov 2025 05:34:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:34:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76389c7791ac539e08f00ada6c0d8e63fb2875388ac5be539590ff77fa593d6`  
		Last Modified: Tue, 18 Nov 2025 04:21:40 GMT  
		Size: 3.1 MB (3079850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58dfc7ad8f3d981491eff3548b814629f9594b76173cfba1b38d23839061a86`  
		Last Modified: Tue, 18 Nov 2025 04:21:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a479b7ac057a0f4485088567a448a9324d019e266525d79d0b4dd8b9968fa8`  
		Last Modified: Tue, 18 Nov 2025 04:24:45 GMT  
		Size: 32.3 MB (32327214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450839ed4674e7308e9f7f985d309da887b11fd14e92704dab4f77a6ebc15e9e`  
		Last Modified: Tue, 18 Nov 2025 04:24:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0fd05fee9eeae456f90dbd571124d2ad5a2240e039f2dc9f6b4ebc2140d9c5`  
		Last Modified: Tue, 18 Nov 2025 05:34:20 GMT  
		Size: 14.3 MB (14252439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3beb25103dd976dfe482fdb173eb9929e23f669a1812b8fc47bb715ecd459cf`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ac208bcd85cb9a2d2e3dcc6d4329be633f2d58ff9524ae4a6a531e7a5c8cea`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa35afe7bbfb4076da474085792f28f9581cd063df1c5d35686fc9e874fb75d`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:463d6110b7a9c0727e420b063e6ad8bc7225cd82894c89c1edacca6e6aab85a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d823bc78b2159cc078821e7fba871cfad90af83c4d41aa1457662f6606abc4d`

```dockerfile
```

-	Layers:
	-	`sha256:6957e480a4692006176772042905e24d6bb195f08da82aaf9b707fee590dfd51`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 2.7 MB (2672247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bbc786027331eb6d2974efb5ebeb9a98b3f82c15369e282681c82a4298a93db`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:c62b98b516bd0cf1237055213f6a579ce09c97a6e2e329585f2f3736012d30bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73190289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a771229e4142fd0b51497ec50a2648bb7736ab1c7a2e392953820a55f7f56f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:01:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:04:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:04:12 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 05:04:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 05:04:12 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 05:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:04:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:04:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:04:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:04:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:04:12 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:28:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:28:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:28:28 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:28:28 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:28:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:28:28 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:28:28 GMT
USER fluent
# Tue, 18 Nov 2025 07:28:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:28:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9c0766613dc586001c46dae6e50a767011e7d1b04c8fb27148520aba2da1a8`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 2.9 MB (2912826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b207a185365783ce19f3e94783c81921c29d626773a40b9d5fb3a7d3b5bdba`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312cd8dbd34cd26bbcf8bca420953962f7f16bbb1a87c6c0a6ef1e9875d22922`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 32.2 MB (32161820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbdead32f83c943b0c1c05aad20ac65d39453f37714cffded8bc274cd4f015d`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87db319712a669b3dec8afa0fa6785c5f7a90020537102571a8e40a12b72ed95`  
		Last Modified: Tue, 18 Nov 2025 07:28:44 GMT  
		Size: 14.2 MB (14179242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d361a53696f68d6c389c54ce81fddbb4522599efc6497d689513c3208fa432`  
		Last Modified: Tue, 18 Nov 2025 07:28:43 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693a6ddf3e2773fd349931971e333d0cf0ae4f5d712080885353fbd4f00a4006`  
		Last Modified: Tue, 18 Nov 2025 07:28:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3897e10a4bca61a4d06b148626272d5c9eaf60dd626d7cb160612795811e1c61`  
		Last Modified: Tue, 18 Nov 2025 07:28:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:97ed9bffb33f12fc62046b50803c52a1582a9ae3b84a6683593f3d2caa091c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6cb67741d7ef4658281db6d5e5318d0e2dd6f6cf112f14dd796e284af4de7a`

```dockerfile
```

-	Layers:
	-	`sha256:5bb380245e438d04ee92d968686f91c1ee4fe496250ca4aa240b512e2a9e8a34`  
		Last Modified: Tue, 18 Nov 2025 09:29:45 GMT  
		Size: 2.7 MB (2670678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168cdede318dc6601583a2ec7cff5ee932fd81b3c9a172e20d835b8c0ff8b321`  
		Last Modified: Tue, 18 Nov 2025 09:29:46 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a74a854734c759084ea1309b166e9715c0111e870c0aa20ccb9ef220b798c2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81625828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c2a0808d03714b1ef462b82a89fa56387ae2f6a7a4a4dc580b5e67b905a6f0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:47:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:47:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:49:20 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:49:20 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:49:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:49:20 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:49:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:49:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:49:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:49:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:49:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:49:20 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 06:17:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 06:17:39 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 06:17:39 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 06:17:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 06:17:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 06:17:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 06:17:39 GMT
USER fluent
# Tue, 18 Nov 2025 06:17:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447d15816b20de873f108e14be26d90895500245066c7397e903586b095268a9`  
		Last Modified: Tue, 18 Nov 2025 04:49:37 GMT  
		Size: 3.3 MB (3340700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50837de87579b732cdad8b680bd50678beebb0cec017ce254837430cf811810`  
		Last Modified: Tue, 18 Nov 2025 04:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7a72e04d5ec1976629669c94d9c534ffbf63371ad40d3d8be38d58fc585ed1`  
		Last Modified: Tue, 18 Nov 2025 04:49:41 GMT  
		Size: 35.9 MB (35900784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e4a0ffc3a4b590761b2aca3f8b729de43ede03f31063296c234525e772eab`  
		Last Modified: Tue, 18 Nov 2025 04:49:36 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e45e62fd06b6b0f94ba92afe0cd26471007fdfbb89e07c7421d6e2da5c4eba5`  
		Last Modified: Tue, 18 Nov 2025 06:17:55 GMT  
		Size: 14.3 MB (14279747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717cafd37babad20847fb123db81f2db7bc7589562250ddf1b17467b7aa44ad5`  
		Last Modified: Tue, 18 Nov 2025 06:17:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ae39c11987a18f98bab176cce3747f0c6633253568faf6b482713937033921`  
		Last Modified: Tue, 18 Nov 2025 06:17:54 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3cae4e20bba4d629b36999405c42e6e7f7ec8fc2a341c7b2c54ee868f18286`  
		Last Modified: Tue, 18 Nov 2025 06:17:54 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c307505bb074738befbf88da23559f5cbdeebc38da8f3c36b2e6075847f31ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb612b0e20c513b7ceebbc2b10eaf33d5cfaefd70f4c8988ad21f6bc67640d3`

```dockerfile
```

-	Layers:
	-	`sha256:fa11a376c73a89598cd4134b8fdcdb946f4c220f64fe5c544b48e2108865941a`  
		Last Modified: Tue, 18 Nov 2025 09:29:49 GMT  
		Size: 2.7 MB (2668692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ac9a753cb51c54a975f782a1edd0209246aca3e59ba22fcc3607d7b4eb83eb`  
		Last Modified: Tue, 18 Nov 2025 09:29:50 GMT  
		Size: 21.2 KB (21156 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:5df4e8b2e830a5003333e290ce271796fdfc7bf162a3fa4a7128ed51cfef0686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23bc26f4db07b606df02f14ce3b529bd3b232e9d0dc8e86d66bebd934352301`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:22:34 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:22:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:22:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:22:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:22:34 GMT
USER fluent
# Tue, 18 Nov 2025 05:22:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:22:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ae260a61c110779bd438deac4d1cd76065ff2394ea83afc9ff5529ea91071`  
		Last Modified: Tue, 18 Nov 2025 03:42:47 GMT  
		Size: 3.5 MB (3510984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356fe9a31a02a164458a68e3f079e86eabe6530bc2f61ae1772c93ea96dfa2a`  
		Last Modified: Tue, 18 Nov 2025 03:42:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0b280db48ee6f86ec56584743697a062ecc6953d4df02a3fe330846b9913a`  
		Last Modified: Tue, 18 Nov 2025 03:46:03 GMT  
		Size: 32.2 MB (32160063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23894894335470a52957a4ef6504faf802a94d333679fd77a4c50a500ae296d0`  
		Last Modified: Tue, 18 Nov 2025 03:46:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979287a7b7479f4b091297b8dde77dd57c16255c1122c316d64dc56986cbe84a`  
		Last Modified: Tue, 18 Nov 2025 05:22:51 GMT  
		Size: 14.1 MB (14066199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daafd6d338e29911ba2ed0bb0dc4f03149fa5d57f96910e6062ca814f1d2cb`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a19ba85eb93000ad493ae17988dc6f1cebc1b849fe17484acbca51ea4e25ea`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757e96ba36c6bae804639ca2dadf2349a78d93393529d6377d411a1e46eb13e2`  
		Last Modified: Tue, 18 Nov 2025 05:22:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3e0f8b5b437688f58383aa7bbf12ccce82a250f7adc1aaea24df67d02376cd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97badbe75c72a0883ff7fa244c548058584d26342bdbe2a1a40dd9da77026744`

```dockerfile
```

-	Layers:
	-	`sha256:9c8cce8e3dfe4cce97ae219a474956647bbc2d50d4f9c0348172ec67f4c23f8b`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 2.7 MB (2665631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcee889ac2455f6b2a0a490ac2e27e5e15a2c2abafd1f3913fbfb7a83acea5f`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:c3dd205475aab6893fda4c4802be16d38d94a9d19c56fce0e0cbd4b9beef5b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84284788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5ad0f7cae4a769dea962c57c97fcc28442eb83ce4ca7f5636c44a986718af`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:10:52 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 06:10:52 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 06:10:52 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 06:10:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:10:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:10:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:10:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:10:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:10:53 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:54:24 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:54:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:54:24 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:54:24 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:54:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:54:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:54:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:54:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:54:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:54:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:54:47 GMT
USER fluent
# Tue, 18 Nov 2025 07:54:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:54:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7c3256cf347ab6b6a418c4e50ff4e79b212be8ebcba139b73b0d7a77d8a838`  
		Last Modified: Tue, 18 Nov 2025 06:01:10 GMT  
		Size: 3.7 MB (3709070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f335ae6f41ee5bac5c8c7103ef44dad3d973bccfddc68ea5180a3c3df5134479`  
		Last Modified: Tue, 18 Nov 2025 06:01:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ae5750a058d28b188bfebfb64590023c1ae76a06a38cfb615b3c04590ed6f8`  
		Last Modified: Tue, 18 Nov 2025 06:11:24 GMT  
		Size: 33.8 MB (33832721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a28a6be34cea10ec6c8e39c6c559216f250208d1ecaae8b534f595f5a2ebfee`  
		Last Modified: Tue, 18 Nov 2025 06:11:21 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a654a7e0ee1888427feed02385b1150972a0a1382dd53a9e1f327803dba8d9`  
		Last Modified: Tue, 18 Nov 2025 07:55:44 GMT  
		Size: 14.7 MB (14671768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a5ee07211a55484c951f64594f3bb028bedf0df4a871d1650b8ae30fa372d`  
		Last Modified: Tue, 18 Nov 2025 07:55:43 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fbfa1e7e07c3f565ed6198b18555f8b1c92f22da1223de02583000d397b71`  
		Last Modified: Tue, 18 Nov 2025 07:55:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e8486975df22c10d7469c04194d0e4418656ee02045cfa1f74c396b813820d`  
		Last Modified: Tue, 18 Nov 2025 07:55:43 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cfaaf6773ac9301ca6ae489b41795bd781a6538d137497f1ad0943c51ed3e8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf195803d6591f23154ad250aa9efe8c4bec8beb1c3780093fb12735859f474`

```dockerfile
```

-	Layers:
	-	`sha256:a3dfd935c905deccc47982f58f00926d94a14c7e9fe9a0b44e3cd22a0f62c8f9`  
		Last Modified: Tue, 18 Nov 2025 09:29:57 GMT  
		Size: 2.7 MB (2672869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56c2f575fde1951d949035c8d9828c8d71e7915e93f7d49034cf6be698fd3b0`  
		Last Modified: Tue, 18 Nov 2025 09:29:58 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:7b591458e33d653dbcb4598b59495bc46e31c4047a0c5afcd14933181b2c0ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8eee832a3af52775f4fa5471d06654bf279b4654dd3de596f6a505c0369a323`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:13:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:20:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:20:34 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 05:20:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 05:20:34 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 05:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:20:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:20:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:20:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:20:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:20:35 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:34:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:34:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:34:28 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:34:28 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:34:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:34:28 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:34:28 GMT
USER fluent
# Tue, 18 Nov 2025 07:34:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:34:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7196bcb3e6bc745b16dc7a6e7435e03f41c2430ffd8c34ac4f2bf12a675f3f`  
		Last Modified: Tue, 18 Nov 2025 05:16:34 GMT  
		Size: 3.2 MB (3170278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b108059018115f7f88520870ada2c23aea918378f4c030a9d69dd2718b920e8`  
		Last Modified: Tue, 18 Nov 2025 05:16:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c181644556269bfc25c91fddc70dc96c3037ebde78ae77c288ab61f0e6e884`  
		Last Modified: Tue, 18 Nov 2025 05:20:56 GMT  
		Size: 33.1 MB (33098859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721217bef3eacac627789c34868d8b3ff6d7a61ba3b996aaf5c6c870c8476926`  
		Last Modified: Tue, 18 Nov 2025 05:20:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4604a2ae868194199882dcbae1eb59161843cd60b1618015c43c2838a31cffa3`  
		Last Modified: Tue, 18 Nov 2025 07:34:49 GMT  
		Size: 14.4 MB (14408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f6d9f66541f127e1c1213a9d0a44000dfcdaeff27d8abcff326e40ef75a8f3`  
		Last Modified: Tue, 18 Nov 2025 07:34:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0b59420960976eba026636fd2340c4be7b7ea79c5d1b8becbec4b1f4dd8e76`  
		Last Modified: Tue, 18 Nov 2025 07:34:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17d7fa2ea048ae6cfc3eda74cdb7a311406f0bec78ecffa19b7fed75e660423`  
		Last Modified: Tue, 18 Nov 2025 07:34:48 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2605158bd61d1e404dbce925caa624601dc85c7962c82aaae653d4a9924d6c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daea78483b2618cf1f03b0d417f6174039d09034d7d4b2675dd64382deb435fb`

```dockerfile
```

-	Layers:
	-	`sha256:1775e819948141f9eb7fd9c7cb4a420f199f0e0f3f6ecdc8ba7de1c334b45d4a`  
		Last Modified: Tue, 18 Nov 2025 09:30:04 GMT  
		Size: 2.7 MB (2665277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c375b01fff7a47d05524a9ced0d3e950cafcc0571abebf6efe42d44117e46e5`  
		Last Modified: Tue, 18 Nov 2025 09:30:05 GMT  
		Size: 21.1 KB (21060 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.9-1.0`

```console
$ docker pull fluentd@sha256:1ad8ae3e827a63e119717cbc995ba416165edf47f802f35d9ec3a28b90874351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16.9-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:afa3a57d73c7c0768f7045af02ff38c7956371261c95b23e523e6496fbb180c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17383642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc6b44e684e6309468eb956f3d4740cf12ccb8c434b97a188b29da64c20b70e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78331f707c6d9910019296ecb4ab44f9b26a450a37e504c48be8963ce9a043`  
		Last Modified: Wed, 08 Oct 2025 23:22:10 GMT  
		Size: 14.0 MB (13961663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba1f53d18cef4c44a0dbd3daafb62cf57107f7f532fa0f57ef1b22d0af51e7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed50b040b930bc5d13e08cdd1df716af2d3ff029e5b6b134e3e2fe71fad714b7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22932eecf8769ce42b56b0bc4a4f283b4d97f1f07d7f98efacbd1a1357ee27cd`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1769926942992a983f31805ed3a13d0406f50533e68b3d4d3236fa5963c45d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.2 KB (986159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53218b2014f588519fb6edb485d5b9268070ae8f517d0500d83a0f5a95462041`

```dockerfile
```

-	Layers:
	-	`sha256:3026734faa929ea6d5e52a4a4265ccb061d0836149b6fc9ef2bb6c9c7c6865c8`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 972.5 KB (972483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3dbf40f2c01bb6ecdda2f44a969772b89c46c3166fe5663350921ae5985e8e`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 13.7 KB (13676 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:46ac9bed32c7a8ce49660a59a52f753eff30538835dd611d22bc1f7934b37c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16137396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f885d67ca4b1bd990fa3007f4cfafb8bf90d6e39ff2be76552973966350f4fef`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-armhf.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:93e88a4aad08082395ce41ebaca8e4678e1148db5e8947e4c39599181a9ee4ba`  
		Last Modified: Wed, 08 Oct 2025 21:25:16 GMT  
		Size: 3.2 MB (3176528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf77ba4c6a48f3bacaaf9db6e676cc51c8898bc17f98b43aa29c349ccd9250`  
		Last Modified: Wed, 08 Oct 2025 22:39:21 GMT  
		Size: 13.0 MB (12958702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e42f64ef5aafe9d9b3ab4319844beb84a50b007d02d84fa103521d60f2f76`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356c473ad81afc625e1af60d0c4ebf7c05152d7ea626b9f0c7875590101fae33`  
		Last Modified: Wed, 08 Oct 2025 22:39:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a4607d2da40a11eda63339c19317510928a2f1581ea6f29a6b9c0fe011d0c`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b1047a7ef72278952bd72515b06df4c47777ce18d0446c239adb2f9bdbe2e14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42935ff90a0ef9a2f68edaf9040d29def17f626d3c04096f9c92178845c3629d`

```dockerfile
```

-	Layers:
	-	`sha256:8015c3aa7387514211e92d6eee02a313c10bc707bafd172c2fd61a50d1311754`  
		Last Modified: Wed, 08 Oct 2025 23:28:29 GMT  
		Size: 13.5 KB (13539 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cef7f445d8c75f71a73b9c9ad0332a2c194fe935d3058f588c8dec4155186ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17368912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff98b6fa62f0c15cb2289ed831b50b438d943fc9324f96ee47ec3bff51bed3f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeb91e752132813c432d89f1a8dd1db5120bd0a105f5482c692c4c90eae17b3`  
		Last Modified: Wed, 08 Oct 2025 22:11:12 GMT  
		Size: 14.0 MB (14007447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df20c8f62a7ff47af002767397639763517b507053d3be2a607ad7cf039699cb`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8b09660f0729b33efa9eee73345d6e2574e683cff98f8189145136dd26dc4`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44991f0a648880052ce599ae6dc1fbcfeeea9db841398e692d720adc561c80c6`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bae4897fe1e09f33a0cb1995e2844559c6203a2de785f07457545055b868b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.4 KB (986385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93150014baf1f5b57526e2c5af7aea24f24a1f05f7958a7233428da7651d9dd`

```dockerfile
```

-	Layers:
	-	`sha256:67aba2f8a082f4bcbaa1ad6fc530073640b1b7742fa155f2fb1f96d7658cede5`  
		Last Modified: Wed, 08 Oct 2025 23:28:32 GMT  
		Size: 972.6 KB (972613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3629a5d26b2d4d23396554cd8b33525330b75f331ee1a61a6aa7b7b2bef527`  
		Last Modified: Wed, 08 Oct 2025 23:28:33 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:6a013d0b1dbe71756026d1ef1f8f07abf0ac51ead8815af66109c1a01414e18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16345474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dbc71c5e074c89edb50509532f4fb4a01d3e9ff2595e95a5533b13db016c55`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:29ed29d5a2d3bb6de33b2b4bc58a076a8bccb81beedbcc013e38338640c314cf`  
		Last Modified: Wed, 08 Oct 2025 12:04:10 GMT  
		Size: 3.3 MB (3254171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c29c80768044ac9f47738f5ba63e8f540639a570074a5dd04bc400d0468ebb8`  
		Last Modified: Wed, 08 Oct 2025 21:46:08 GMT  
		Size: 13.1 MB (13089135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e224de4549cda25d841df269ce3e9b86cd0feb6ef1703b75cb32524bedafe1`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1061097b93842eedc8d7863fc0608dbd3490771b515873cc3329b5cdc8fcbd`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba5a6e02037353ec4b014f170080310354e526bc797bfe200c2286eedaf6ae8`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:755dd01070d905860704626ff1d1155994b4bf042e5aab8aa38bca75857fc293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.9 KB (982887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc6d533e4a0d8a4e7117c42fd122fbdcec92426815b69d138847435a5f42c2d`

```dockerfile
```

-	Layers:
	-	`sha256:e17fbd8db09214885631e52c7f3ee862a494b742523bb8f6acb292439080f164`  
		Last Modified: Wed, 08 Oct 2025 23:28:36 GMT  
		Size: 969.2 KB (969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83c293b83d79cb70ba9c955cedb86fdc401f653cba99c68d22f9fa322bab621`  
		Last Modified: Wed, 08 Oct 2025 23:28:37 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:62eb94d5f8bab0352fe1bda6749f90795526e823846751875ed5078f2f8704b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16932429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b60459341330d9f4e3d27c417ba023f6fe3fb7b0846fda2d34e07b63e813c3c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-ppc64le.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8615c7c09f59391eedf1644cf56164e9680a9e5f673fc84abf83944731c13b07`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.4 MB (3364466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd729167cc2a515dbbde613e7ae787652d091f0141bb5881d946a962a54a4b4`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 13.6 MB (13565797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae39192a12d7e6272184f7dcbe45d1241c964aafe748d27068d19340c408c9`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58128b57f286f34d4522f0e60a4be46c9fad0ee0dcf950dc879b1dcf511804ff`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63d13a8c0219e4550fb93a4d23eb5ecebf4f0cb4dbf998c38c7538a6243f718`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:23f4110435b3c619f0c6dfd9bc4b503e4d1f29f43cc89d63a31362be157e36aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.7 KB (981716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e38f607b22ca7f6244be9c7241bb070aeec1e5087b0cf13bf0ac887e0dde105`

```dockerfile
```

-	Layers:
	-	`sha256:ab9c1e7d5cf37454b207e160b91793faa0c78f73788b2c5eb29bd4c53c8b6970`  
		Last Modified: Thu, 09 Oct 2025 08:28:29 GMT  
		Size: 968.0 KB (968006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ccd55a5597ae933a84d99a7a7f1903f8379b62a381c32ab960f5b9cd3b64b58`  
		Last Modified: Thu, 09 Oct 2025 08:28:30 GMT  
		Size: 13.7 KB (13710 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:0b41672737621c0b4d9636f2680dc26702a455105378c6fddfde27ccd0dc7754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16767969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55cf05ab6ec22da0c19bd4f8545dddd8e4be8caddc43341112665a1915a7201`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-s390x.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:913efc36ec133ccc056e722147d93d8138aa999785d2ce858104b0c2d0e78fd6`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.3 MB (3253007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd32227ea6240b7d955081f56cf0e5cc573c44dd77407da8bb53c063ab87b71`  
		Last Modified: Thu, 09 Oct 2025 14:10:11 GMT  
		Size: 13.5 MB (13512798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fab613ee49849eb1192e5b5aca71cbeabae4d8c9ed4297bbc7070c859d579b3`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1655c318dd63d9aadb21ad09dc3762229e1cecd22e44d14c481db0c808efcc1`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed09bc671cc79a80b0e31f178bdf4318f525b2880e56c471dffebf3a859f886`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:48b41953e35001058187fa9db056f5f99dd35a109572db363ed221550ec063b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.1 KB (981071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab11aac5ad8d7f16b2e926d62908dbe2278ca45cffe6b3527a559b15741ff15`

```dockerfile
```

-	Layers:
	-	`sha256:370521b0c1295049f7e15fcdc00056580fd5959e7fb0423f9759e0b2cd663222`  
		Last Modified: Thu, 09 Oct 2025 14:28:31 GMT  
		Size: 967.4 KB (967396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129be691f47d14c09692973c170d7b9564fd1a2535581688d141759c73b4a009`  
		Last Modified: Thu, 09 Oct 2025 14:28:32 GMT  
		Size: 13.7 KB (13675 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.9-debian-1.0`

```console
$ docker pull fluentd@sha256:0092223659683b5aa193a2bb2439b156b3d91e0017941ec2541a9ce0246ed6b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16.9-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:adc32d59b13596bea4e0c47cda19e01de34a450fa3131e5eba9752b6d7f0cc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81975913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a1f69a1e4a41ac657f4a49b214232a65121e6640eedb25d175a88d5437116`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:01:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:36 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 06:03:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 06:03:36 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 06:03:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:36 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:10:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:10:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:10:22 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:10:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:10:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:10:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:10:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:10:23 GMT
USER fluent
# Tue, 18 Nov 2025 07:10:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:10:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e866b3193d2e6441b53636d4e28f58cf0d3bddf19ddcb1d61e0699552ab9892`  
		Last Modified: Tue, 18 Nov 2025 06:03:53 GMT  
		Size: 3.5 MB (3509694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660fd9d37538af993f94c911cf40fdd3f65887f00bdd3b02d5f6beb5575f110`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdf0cffb9c947b88141a6cba3cd7d029546ad9e7fc7738ed734520b77518834`  
		Last Modified: Tue, 18 Nov 2025 06:03:58 GMT  
		Size: 36.0 MB (35963790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb63ff945397c57afdf5357fc26230f517e828b379cdf66f18775e111560dc31`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468107321d5436a93897728b385869239ee0171197567d4c9bf4a7dc9bdd1bc`  
		Last Modified: Tue, 18 Nov 2025 07:10:41 GMT  
		Size: 14.3 MB (14271585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c9825ed723b1fd916d8601339d6b14ae9cbae397538a507ce9ad877d758727`  
		Last Modified: Tue, 18 Nov 2025 07:10:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf7111818affb5fcd616da180926cb9857a507cac1cd3e77be9ee669ac9a62`  
		Last Modified: Tue, 18 Nov 2025 07:10:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48db7a3726ac5725adb9de367b5037b8cf7aa782f1089c49a6a909282154891`  
		Last Modified: Tue, 18 Nov 2025 07:10:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c8916a8d7c83e36810ad724c22c5b003e00a59eb417685fd7e4614355adff2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af096d5aa78541edcbf14961dd92a8aad9460b4160f6e4d5a9dbb314bbe814f`

```dockerfile
```

-	Layers:
	-	`sha256:d334dd7417fb839e1656a8f2c7f7104476699fb6abc97ea2b859656c49853659`  
		Last Modified: Tue, 18 Nov 2025 09:29:37 GMT  
		Size: 2.7 MB (2668452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623ec4a7af11708575a06aee0539e27d050a33469d4aae769dfc51d944138074`  
		Last Modified: Tue, 18 Nov 2025 09:29:38 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:15b64e0fd4162ae5d056943a22573ca147389050286521bbe2f4d760d17567e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cbac93bc99cc5fdfab88c444893f98ff5d71a0fb527121625c23a624161031`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:34:04 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:34:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:34:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:34:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:34:04 GMT
USER fluent
# Tue, 18 Nov 2025 05:34:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:34:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76389c7791ac539e08f00ada6c0d8e63fb2875388ac5be539590ff77fa593d6`  
		Last Modified: Tue, 18 Nov 2025 04:21:40 GMT  
		Size: 3.1 MB (3079850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58dfc7ad8f3d981491eff3548b814629f9594b76173cfba1b38d23839061a86`  
		Last Modified: Tue, 18 Nov 2025 04:21:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a479b7ac057a0f4485088567a448a9324d019e266525d79d0b4dd8b9968fa8`  
		Last Modified: Tue, 18 Nov 2025 04:24:45 GMT  
		Size: 32.3 MB (32327214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450839ed4674e7308e9f7f985d309da887b11fd14e92704dab4f77a6ebc15e9e`  
		Last Modified: Tue, 18 Nov 2025 04:24:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0fd05fee9eeae456f90dbd571124d2ad5a2240e039f2dc9f6b4ebc2140d9c5`  
		Last Modified: Tue, 18 Nov 2025 05:34:20 GMT  
		Size: 14.3 MB (14252439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3beb25103dd976dfe482fdb173eb9929e23f669a1812b8fc47bb715ecd459cf`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ac208bcd85cb9a2d2e3dcc6d4329be633f2d58ff9524ae4a6a531e7a5c8cea`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa35afe7bbfb4076da474085792f28f9581cd063df1c5d35686fc9e874fb75d`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:463d6110b7a9c0727e420b063e6ad8bc7225cd82894c89c1edacca6e6aab85a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d823bc78b2159cc078821e7fba871cfad90af83c4d41aa1457662f6606abc4d`

```dockerfile
```

-	Layers:
	-	`sha256:6957e480a4692006176772042905e24d6bb195f08da82aaf9b707fee590dfd51`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 2.7 MB (2672247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bbc786027331eb6d2974efb5ebeb9a98b3f82c15369e282681c82a4298a93db`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:c62b98b516bd0cf1237055213f6a579ce09c97a6e2e329585f2f3736012d30bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73190289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a771229e4142fd0b51497ec50a2648bb7736ab1c7a2e392953820a55f7f56f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:01:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:04:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:04:12 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 05:04:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 05:04:12 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 05:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:04:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:04:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:04:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:04:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:04:12 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:28:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:28:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:28:28 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:28:28 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:28:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:28:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:28:28 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:28:28 GMT
USER fluent
# Tue, 18 Nov 2025 07:28:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:28:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9c0766613dc586001c46dae6e50a767011e7d1b04c8fb27148520aba2da1a8`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 2.9 MB (2912826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b207a185365783ce19f3e94783c81921c29d626773a40b9d5fb3a7d3b5bdba`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312cd8dbd34cd26bbcf8bca420953962f7f16bbb1a87c6c0a6ef1e9875d22922`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 32.2 MB (32161820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbdead32f83c943b0c1c05aad20ac65d39453f37714cffded8bc274cd4f015d`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87db319712a669b3dec8afa0fa6785c5f7a90020537102571a8e40a12b72ed95`  
		Last Modified: Tue, 18 Nov 2025 07:28:44 GMT  
		Size: 14.2 MB (14179242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d361a53696f68d6c389c54ce81fddbb4522599efc6497d689513c3208fa432`  
		Last Modified: Tue, 18 Nov 2025 07:28:43 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693a6ddf3e2773fd349931971e333d0cf0ae4f5d712080885353fbd4f00a4006`  
		Last Modified: Tue, 18 Nov 2025 07:28:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3897e10a4bca61a4d06b148626272d5c9eaf60dd626d7cb160612795811e1c61`  
		Last Modified: Tue, 18 Nov 2025 07:28:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:97ed9bffb33f12fc62046b50803c52a1582a9ae3b84a6683593f3d2caa091c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6cb67741d7ef4658281db6d5e5318d0e2dd6f6cf112f14dd796e284af4de7a`

```dockerfile
```

-	Layers:
	-	`sha256:5bb380245e438d04ee92d968686f91c1ee4fe496250ca4aa240b512e2a9e8a34`  
		Last Modified: Tue, 18 Nov 2025 09:29:45 GMT  
		Size: 2.7 MB (2670678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168cdede318dc6601583a2ec7cff5ee932fd81b3c9a172e20d835b8c0ff8b321`  
		Last Modified: Tue, 18 Nov 2025 09:29:46 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a74a854734c759084ea1309b166e9715c0111e870c0aa20ccb9ef220b798c2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81625828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c2a0808d03714b1ef462b82a89fa56387ae2f6a7a4a4dc580b5e67b905a6f0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:47:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:47:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:49:20 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:49:20 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:49:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:49:20 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:49:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:49:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:49:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:49:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:49:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:49:20 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 06:17:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 06:17:39 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 06:17:39 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 06:17:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 06:17:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 06:17:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 06:17:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 06:17:39 GMT
USER fluent
# Tue, 18 Nov 2025 06:17:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 06:17:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447d15816b20de873f108e14be26d90895500245066c7397e903586b095268a9`  
		Last Modified: Tue, 18 Nov 2025 04:49:37 GMT  
		Size: 3.3 MB (3340700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50837de87579b732cdad8b680bd50678beebb0cec017ce254837430cf811810`  
		Last Modified: Tue, 18 Nov 2025 04:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7a72e04d5ec1976629669c94d9c534ffbf63371ad40d3d8be38d58fc585ed1`  
		Last Modified: Tue, 18 Nov 2025 04:49:41 GMT  
		Size: 35.9 MB (35900784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e4a0ffc3a4b590761b2aca3f8b729de43ede03f31063296c234525e772eab`  
		Last Modified: Tue, 18 Nov 2025 04:49:36 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e45e62fd06b6b0f94ba92afe0cd26471007fdfbb89e07c7421d6e2da5c4eba5`  
		Last Modified: Tue, 18 Nov 2025 06:17:55 GMT  
		Size: 14.3 MB (14279747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717cafd37babad20847fb123db81f2db7bc7589562250ddf1b17467b7aa44ad5`  
		Last Modified: Tue, 18 Nov 2025 06:17:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ae39c11987a18f98bab176cce3747f0c6633253568faf6b482713937033921`  
		Last Modified: Tue, 18 Nov 2025 06:17:54 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3cae4e20bba4d629b36999405c42e6e7f7ec8fc2a341c7b2c54ee868f18286`  
		Last Modified: Tue, 18 Nov 2025 06:17:54 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c307505bb074738befbf88da23559f5cbdeebc38da8f3c36b2e6075847f31ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb612b0e20c513b7ceebbc2b10eaf33d5cfaefd70f4c8988ad21f6bc67640d3`

```dockerfile
```

-	Layers:
	-	`sha256:fa11a376c73a89598cd4134b8fdcdb946f4c220f64fe5c544b48e2108865941a`  
		Last Modified: Tue, 18 Nov 2025 09:29:49 GMT  
		Size: 2.7 MB (2668692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ac9a753cb51c54a975f782a1edd0209246aca3e59ba22fcc3607d7b4eb83eb`  
		Last Modified: Tue, 18 Nov 2025 09:29:50 GMT  
		Size: 21.2 KB (21156 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5df4e8b2e830a5003333e290ce271796fdfc7bf162a3fa4a7128ed51cfef0686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23bc26f4db07b606df02f14ce3b529bd3b232e9d0dc8e86d66bebd934352301`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:22:34 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:22:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:22:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:22:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:22:34 GMT
USER fluent
# Tue, 18 Nov 2025 05:22:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:22:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ae260a61c110779bd438deac4d1cd76065ff2394ea83afc9ff5529ea91071`  
		Last Modified: Tue, 18 Nov 2025 03:42:47 GMT  
		Size: 3.5 MB (3510984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356fe9a31a02a164458a68e3f079e86eabe6530bc2f61ae1772c93ea96dfa2a`  
		Last Modified: Tue, 18 Nov 2025 03:42:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0b280db48ee6f86ec56584743697a062ecc6953d4df02a3fe330846b9913a`  
		Last Modified: Tue, 18 Nov 2025 03:46:03 GMT  
		Size: 32.2 MB (32160063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23894894335470a52957a4ef6504faf802a94d333679fd77a4c50a500ae296d0`  
		Last Modified: Tue, 18 Nov 2025 03:46:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979287a7b7479f4b091297b8dde77dd57c16255c1122c316d64dc56986cbe84a`  
		Last Modified: Tue, 18 Nov 2025 05:22:51 GMT  
		Size: 14.1 MB (14066199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daafd6d338e29911ba2ed0bb0dc4f03149fa5d57f96910e6062ca814f1d2cb`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a19ba85eb93000ad493ae17988dc6f1cebc1b849fe17484acbca51ea4e25ea`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757e96ba36c6bae804639ca2dadf2349a78d93393529d6377d411a1e46eb13e2`  
		Last Modified: Tue, 18 Nov 2025 05:22:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3e0f8b5b437688f58383aa7bbf12ccce82a250f7adc1aaea24df67d02376cd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97badbe75c72a0883ff7fa244c548058584d26342bdbe2a1a40dd9da77026744`

```dockerfile
```

-	Layers:
	-	`sha256:9c8cce8e3dfe4cce97ae219a474956647bbc2d50d4f9c0348172ec67f4c23f8b`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 2.7 MB (2665631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcee889ac2455f6b2a0a490ac2e27e5e15a2c2abafd1f3913fbfb7a83acea5f`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:c3dd205475aab6893fda4c4802be16d38d94a9d19c56fce0e0cbd4b9beef5b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84284788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5ad0f7cae4a769dea962c57c97fcc28442eb83ce4ca7f5636c44a986718af`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:10:52 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 06:10:52 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 06:10:52 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 06:10:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:10:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:10:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:10:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:10:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:10:53 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:54:24 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:54:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:54:24 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:54:24 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:54:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:54:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:54:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:54:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:54:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:54:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:54:47 GMT
USER fluent
# Tue, 18 Nov 2025 07:54:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:54:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7c3256cf347ab6b6a418c4e50ff4e79b212be8ebcba139b73b0d7a77d8a838`  
		Last Modified: Tue, 18 Nov 2025 06:01:10 GMT  
		Size: 3.7 MB (3709070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f335ae6f41ee5bac5c8c7103ef44dad3d973bccfddc68ea5180a3c3df5134479`  
		Last Modified: Tue, 18 Nov 2025 06:01:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ae5750a058d28b188bfebfb64590023c1ae76a06a38cfb615b3c04590ed6f8`  
		Last Modified: Tue, 18 Nov 2025 06:11:24 GMT  
		Size: 33.8 MB (33832721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a28a6be34cea10ec6c8e39c6c559216f250208d1ecaae8b534f595f5a2ebfee`  
		Last Modified: Tue, 18 Nov 2025 06:11:21 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a654a7e0ee1888427feed02385b1150972a0a1382dd53a9e1f327803dba8d9`  
		Last Modified: Tue, 18 Nov 2025 07:55:44 GMT  
		Size: 14.7 MB (14671768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a5ee07211a55484c951f64594f3bb028bedf0df4a871d1650b8ae30fa372d`  
		Last Modified: Tue, 18 Nov 2025 07:55:43 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fbfa1e7e07c3f565ed6198b18555f8b1c92f22da1223de02583000d397b71`  
		Last Modified: Tue, 18 Nov 2025 07:55:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e8486975df22c10d7469c04194d0e4418656ee02045cfa1f74c396b813820d`  
		Last Modified: Tue, 18 Nov 2025 07:55:43 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cfaaf6773ac9301ca6ae489b41795bd781a6538d137497f1ad0943c51ed3e8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf195803d6591f23154ad250aa9efe8c4bec8beb1c3780093fb12735859f474`

```dockerfile
```

-	Layers:
	-	`sha256:a3dfd935c905deccc47982f58f00926d94a14c7e9fe9a0b44e3cd22a0f62c8f9`  
		Last Modified: Tue, 18 Nov 2025 09:29:57 GMT  
		Size: 2.7 MB (2672869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56c2f575fde1951d949035c8d9828c8d71e7915e93f7d49034cf6be698fd3b0`  
		Last Modified: Tue, 18 Nov 2025 09:29:58 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:7b591458e33d653dbcb4598b59495bc46e31c4047a0c5afcd14933181b2c0ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8eee832a3af52775f4fa5471d06654bf279b4654dd3de596f6a505c0369a323`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:13:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:20:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:20:34 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 05:20:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 05:20:34 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 05:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:20:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:20:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:20:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:20:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:20:35 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:34:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:34:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 07:34:28 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 07:34:28 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:34:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:34:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:34:28 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:34:28 GMT
USER fluent
# Tue, 18 Nov 2025 07:34:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:34:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7196bcb3e6bc745b16dc7a6e7435e03f41c2430ffd8c34ac4f2bf12a675f3f`  
		Last Modified: Tue, 18 Nov 2025 05:16:34 GMT  
		Size: 3.2 MB (3170278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b108059018115f7f88520870ada2c23aea918378f4c030a9d69dd2718b920e8`  
		Last Modified: Tue, 18 Nov 2025 05:16:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c181644556269bfc25c91fddc70dc96c3037ebde78ae77c288ab61f0e6e884`  
		Last Modified: Tue, 18 Nov 2025 05:20:56 GMT  
		Size: 33.1 MB (33098859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721217bef3eacac627789c34868d8b3ff6d7a61ba3b996aaf5c6c870c8476926`  
		Last Modified: Tue, 18 Nov 2025 05:20:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4604a2ae868194199882dcbae1eb59161843cd60b1618015c43c2838a31cffa3`  
		Last Modified: Tue, 18 Nov 2025 07:34:49 GMT  
		Size: 14.4 MB (14408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f6d9f66541f127e1c1213a9d0a44000dfcdaeff27d8abcff326e40ef75a8f3`  
		Last Modified: Tue, 18 Nov 2025 07:34:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0b59420960976eba026636fd2340c4be7b7ea79c5d1b8becbec4b1f4dd8e76`  
		Last Modified: Tue, 18 Nov 2025 07:34:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17d7fa2ea048ae6cfc3eda74cdb7a311406f0bec78ecffa19b7fed75e660423`  
		Last Modified: Tue, 18 Nov 2025 07:34:48 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2605158bd61d1e404dbce925caa624601dc85c7962c82aaae653d4a9924d6c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daea78483b2618cf1f03b0d417f6174039d09034d7d4b2675dd64382deb435fb`

```dockerfile
```

-	Layers:
	-	`sha256:1775e819948141f9eb7fd9c7cb4a420f199f0e0f3f6ecdc8ba7de1c334b45d4a`  
		Last Modified: Tue, 18 Nov 2025 09:30:04 GMT  
		Size: 2.7 MB (2665277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c375b01fff7a47d05524a9ced0d3e950cafcc0571abebf6efe42d44117e46e5`  
		Last Modified: Tue, 18 Nov 2025 09:30:05 GMT  
		Size: 21.1 KB (21060 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:8680b920563192348ac191fdda16ebce739da1d9bbc6c42711ab9d04942a24ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.19-1` - linux; amd64

```console
$ docker pull fluentd@sha256:aabf6e4d72df07f72c6320798286e38cb4078985fba7993be976076dd19c9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a904b3458ff5a124387f32960dfa2db38c96553803b6f1ca1aa65f98cd5c1f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:11:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:11:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:11:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:11:04 GMT
USER fluent
# Tue, 18 Nov 2025 07:11:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb0562513a544d09b243cd53af17176ae058cdb46bab21dc80e6e0e176085ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 1.3 MB (1279393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2995c07ae76a079f87ad5194b6ae8ae189e2697989ee2ec3ff402c4bbdbaef98`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8b74c7e9beb752e09eab60f51bfed7d4156be9c8a4cb31e65c1c593e477ad`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 42.2 MB (42158682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50951878876ddf823dfebd9e0c1677361d53bec1ff62831466fd280b78c485e7`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d897148a18c357950ad15bea0e1575bef5fe1a2f87069f845f212cbbf20eb783`  
		Last Modified: Tue, 18 Nov 2025 07:11:19 GMT  
		Size: 6.0 MB (6044983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba720e6453fce022701e4eb9ffad635c1814d3646e93621dca69a3739535b77`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2aea49a7fcbe5821ef2d28fd99597cefbdc90bbd576c99309e18724ebaddf`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c767a526bd60d2327b413b7336b31b1a00d72bc533f3b78d5137370859a100`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8cf6892824e97d161f124d5333687ef7b8eb6bf25f6aa2ccd03ef3a4b110b485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61709c4d165ab4eeaaedac4e4f88cd257d11b31708fbd397c45a227b866d23`

```dockerfile
```

-	Layers:
	-	`sha256:ee0b209bed1b2e569f4ce68fc851ee89e0ceb2f39e1afe579774bd04519a1711`  
		Last Modified: Tue, 18 Nov 2025 09:29:22 GMT  
		Size: 2.3 MB (2283558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2847675aad81b3637e07602402738b0ff18b4ecea6c1b1bf03ab8c53298839fc`  
		Last Modified: Tue, 18 Nov 2025 09:29:23 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8bddf98d29f007597c2419ece53918ed2a02b6807f244eba291b11a115ce2f`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 1.3 MB (1263024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce6e0d17644462250ed0239ef347ef83d3d46d91cc236e61f5d1ee58840ebe6`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dba72f3360e3a96295c7cea72647313a78f2723776a3e529d977bc6fb38431`  
		Last Modified: Tue, 18 Nov 2025 04:22:15 GMT  
		Size: 38.0 MB (37994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0930b6e7a3909c3d28136a1cc19c3a553fbbb2a2d33988cd25bd43effa0a140`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ffa87b2ef8721e0de3adac791ff08369238bf6c371e5932d6858ff86c97a8af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71020865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a309489b26daac336f6e6ea0d24e3a28b4da34d74776fc011a8ff429afb1d5c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:29:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:29:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:29:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:29:49 GMT
USER fluent
# Tue, 18 Nov 2025 07:29:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d8370801a134071a40fe32d3d2fa7e0e17d18b25e5289e7237638fa8e7778`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 1.2 MB (1236519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b3223558fcb7b7da07de149d35cb77b0270a5ab9574f7885d63190a335526`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053f0fd615ae9d3957c571c9b6d06b6a892f68a64ba86fcf53aa1540117bbac`  
		Last Modified: Tue, 18 Nov 2025 05:02:15 GMT  
		Size: 37.9 MB (37865819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f081e8cb5f13e31c833ade5ef8bd8bc86005b1083ad01fb5c19150cfe1b852`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444514b6beb7cb41d5a6d74e2f02a6bd8d9b0d67d264bddba5cf5602534aef97`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 5.7 MB (5706176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281d992d9d5bfb4e3f3533290ac4e747701b996dfaa51bf4a1887a3d63f237ff`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9cd3785a6ed6fc017c3d377c407e31815775d28357a6cdbd99ac7ef4ebe6a9`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7153e50f421f23ea30db7f22fadac8133b4cf09d65d0fd4c239fa763debfcf8`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:612ec81a16bb05c27831a6a67cf5752e4bc1c6d4fb51cf3ec02bc176489ce778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee842d899c723e51f00df47d9670b2ed70e0e106f38477cc61e408fec563880`

```dockerfile
```

-	Layers:
	-	`sha256:ac725726a20c2cfebd9dd7c4277a0d190b6fe2958362e143a17129d44928298c`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 2.3 MB (2284970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff089d2e69179495169d3e05de805a988e7d4ff76570a57563e87343611f0ea`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a222dc7e9ddd2a1a1e14eda8278bac79c4b69652f2db613d6a31ca5838ea10cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79579468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c4933f2d7aba9a6cf42193fd309996c735faf39323e3cc9ce2adf1bd5b099f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:45:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:45:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:48:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:48:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:48:39 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 06:18:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 06:18:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 06:18:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 06:18:42 GMT
USER fluent
# Tue, 18 Nov 2025 06:18:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623192602c00e918197dfe6e2a1def0175e7be0d446a268ed38b6b5a621d38e0`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 1.3 MB (1261685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5fe6e2e9edffda349665022b4300b140e6a85f15a0f7614134df0867bcd551`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c522fdb9fff298474b76a11223cdcb250793d0c701b8cf389c0375800c7d5c`  
		Last Modified: Tue, 18 Nov 2025 04:48:57 GMT  
		Size: 42.1 MB (42145706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907ba9f7c5e39a58b009710a158a43136020eb8b46dc729f4426b65e03945ab`  
		Last Modified: Tue, 18 Nov 2025 04:48:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e287744781de6ba7990849d817b7d56815ea27a555f9b632c53f48912e6a8625`  
		Last Modified: Tue, 18 Nov 2025 06:19:03 GMT  
		Size: 6.0 MB (6031074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc83efe024d58f7c0f2ae54f8d1ca24212b0426b3b9f4ed85cf9dc2d9b4f138`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987698c2ecdcb3a42d62e47e6006334377b7ac96ac221f15c83c4f57ac5e185f`  
		Last Modified: Tue, 18 Nov 2025 06:18:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7418657ce63265bb53e93a85647829e7204dc7e5e55c4d2f68d731d36c14d5d`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:63307458ba12a55d8d3c164970c0601563d734a19561d3591fbecef80b4c26f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e9a7edd5a56936df00b963c56f0cc56c6857e45e7994aff9778145c3ba6dc9`

```dockerfile
```

-	Layers:
	-	`sha256:6f06e5d3a4506938173bb5f8471b70bec3c02332e7399634d46d17a90e3cda2a`  
		Last Modified: Tue, 18 Nov 2025 09:29:36 GMT  
		Size: 2.3 MB (2283830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0189ec4797d51709921e626666d44a28d1468c0300fac9c5b0a809df6e7ca1`  
		Last Modified: Tue, 18 Nov 2025 09:29:37 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bef966be95a2220ea41b52e0e83a8a622f90c5f320368a5f0d7284a00c503`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 1.3 MB (1287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45ed37d5457ae44f5b9a372ecc7bde1dd97d5be333bac0f4030719c7f0eca`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402fa9c5b261b8af75a607827e3e965cc7ce4351d91e3eba319a98783514bc3d`  
		Last Modified: Tue, 18 Nov 2025 03:43:29 GMT  
		Size: 37.7 MB (37740240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3646abfea40cabe9f48dabaff87823bc4de7febc7191871f992e8cdd29e5cc`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7a353d0f79751c2dce8dee5b2fded32d60934117291b83ec3d732116e194ffce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81069474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c794d9c800335e31b8d79aaf1dca07460a1300dc3c2092262bbf9a3870de6a5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:28:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 00:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:42:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:42:47 GMT
CMD ["irb"]
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Wed, 19 Nov 2025 01:48:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 19 Nov 2025 01:48:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 19 Nov 2025 01:48:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 19 Nov 2025 01:48:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 19 Nov 2025 01:48:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 19 Nov 2025 01:48:21 GMT
USER fluent
# Wed, 19 Nov 2025 01:48:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 19 Nov 2025 01:48:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbe0cbe7af169b8d7859f452f051f576ef4653fffd19a193922bbf502224d54`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 1.3 MB (1309674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a0a74191697331846ecf6cc860ffede09eafae29280e1dd04f2379b2dc07`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a0cff339fe641e08a65a97169cbbb4be8d7c4819ff50a706f2ed826916747`  
		Last Modified: Wed, 19 Nov 2025 00:43:23 GMT  
		Size: 39.6 MB (39601439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923e173b58f16848269bd5ce9e04bacdfaffeebd5dac19f837456978574583d6`  
		Last Modified: Wed, 19 Nov 2025 00:43:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fcdb627de74f9b8361edff9525a0fe6a33fdd953adf0fb2c0e3b00f9613e2b`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 6.6 MB (6559103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f259062e3fb7ae4681e323cc9047c9e3d00852e2125d9e493ac1ed5b8f53e103`  
		Last Modified: Wed, 19 Nov 2025 01:49:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ddab9ad7d500134abea5277fd0c7912069edbe26baf3a161f5b021d156ec75`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f4db3acfbcf50daa96589591259155ba6cc7fca7753781f8345d4843f6f05`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0730fbfa8014170ddc03be28fb1510037719c10514d7d5fb2f1ef694b66c9130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d1a4b27f5bebde2aadf39b7cfcbf1cbb93710322c8c18ee5f819d0ff0b4bdd`

```dockerfile
```

-	Layers:
	-	`sha256:692608745c585b5c51accdf3fb05f15ad958b401f00e1950d21c6de48529e978`  
		Last Modified: Wed, 19 Nov 2025 03:28:34 GMT  
		Size: 2.3 MB (2287093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6aad5bdc16681e7da44fc798332bef9931f9d15dd9899bd0d5f9f49af36bf2`  
		Last Modified: Wed, 19 Nov 2025 03:28:35 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:683484cc5debca5c0709f0c7d2d978e76f78712ebc852b4a4adc005d46ec25d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76835164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08e6e4b2bfe39b06d532dd33389c27a98d33b36b8e7146d75800194d194dc41`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:14:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 07:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5be0006390772cf7f9022344d107d52c9454ddfb26a9b6aa53e4f77a9bdc5e`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 1.3 MB (1294253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df3437f72c81d0de5473522e48eb46cf20ee4ae5ae981dfae54b48d71b07c5f`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67960768c1f544671789085d4901deaf00ad13d073997065fbd38e41baef3e`  
		Last Modified: Tue, 18 Nov 2025 05:17:09 GMT  
		Size: 39.3 MB (39287189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de67f11ad5b13189744a053b706d6a38590793d5b547a05561143636a6e794`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b6ba71f42284c745b166f743e6e50d1f0a6854eee654f4eb7cf742b48e808`  
		Last Modified: Tue, 18 Nov 2025 07:35:44 GMT  
		Size: 6.4 MB (6416958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d87c11925f40d6e2afa5a002fb413adc618d32a4c1f33ccd48c47e23b57b7`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082eb1114230c4c0724b38d35ab1fc4eee657526608a13dd9fd5d5e8a4a21bc9`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ab1a0cf3bc37e55bb698b7e2e76edb0e4cea56577c12907c808a17c957928`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3f8f214fada39a1a20d17924da461fedbaf16aecfbb0fa7591a3bc3b6bb69094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9677d7cdb6034256be28e74f6dfe5c2324badba6517a6567ec886a568e1a826c`

```dockerfile
```

-	Layers:
	-	`sha256:88a33b325036b2acdcbf4c3afa0c4f5711c06a125a88b8e4dddf20ed68e32d37`  
		Last Modified: Tue, 18 Nov 2025 09:29:45 GMT  
		Size: 2.3 MB (2285003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ed799d8ee14c02a6e9a62dbc69e63a23d15a697ba91568efc436ace9eb3ba1`  
		Last Modified: Tue, 18 Nov 2025 09:29:46 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:8680b920563192348ac191fdda16ebce739da1d9bbc6c42711ab9d04942a24ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.19-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:aabf6e4d72df07f72c6320798286e38cb4078985fba7993be976076dd19c9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a904b3458ff5a124387f32960dfa2db38c96553803b6f1ca1aa65f98cd5c1f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:11:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:11:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:11:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:11:04 GMT
USER fluent
# Tue, 18 Nov 2025 07:11:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb0562513a544d09b243cd53af17176ae058cdb46bab21dc80e6e0e176085ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 1.3 MB (1279393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2995c07ae76a079f87ad5194b6ae8ae189e2697989ee2ec3ff402c4bbdbaef98`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8b74c7e9beb752e09eab60f51bfed7d4156be9c8a4cb31e65c1c593e477ad`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 42.2 MB (42158682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50951878876ddf823dfebd9e0c1677361d53bec1ff62831466fd280b78c485e7`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d897148a18c357950ad15bea0e1575bef5fe1a2f87069f845f212cbbf20eb783`  
		Last Modified: Tue, 18 Nov 2025 07:11:19 GMT  
		Size: 6.0 MB (6044983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba720e6453fce022701e4eb9ffad635c1814d3646e93621dca69a3739535b77`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2aea49a7fcbe5821ef2d28fd99597cefbdc90bbd576c99309e18724ebaddf`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c767a526bd60d2327b413b7336b31b1a00d72bc533f3b78d5137370859a100`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8cf6892824e97d161f124d5333687ef7b8eb6bf25f6aa2ccd03ef3a4b110b485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61709c4d165ab4eeaaedac4e4f88cd257d11b31708fbd397c45a227b866d23`

```dockerfile
```

-	Layers:
	-	`sha256:ee0b209bed1b2e569f4ce68fc851ee89e0ceb2f39e1afe579774bd04519a1711`  
		Last Modified: Tue, 18 Nov 2025 09:29:22 GMT  
		Size: 2.3 MB (2283558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2847675aad81b3637e07602402738b0ff18b4ecea6c1b1bf03ab8c53298839fc`  
		Last Modified: Tue, 18 Nov 2025 09:29:23 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8bddf98d29f007597c2419ece53918ed2a02b6807f244eba291b11a115ce2f`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 1.3 MB (1263024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce6e0d17644462250ed0239ef347ef83d3d46d91cc236e61f5d1ee58840ebe6`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dba72f3360e3a96295c7cea72647313a78f2723776a3e529d977bc6fb38431`  
		Last Modified: Tue, 18 Nov 2025 04:22:15 GMT  
		Size: 38.0 MB (37994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0930b6e7a3909c3d28136a1cc19c3a553fbbb2a2d33988cd25bd43effa0a140`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ffa87b2ef8721e0de3adac791ff08369238bf6c371e5932d6858ff86c97a8af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71020865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a309489b26daac336f6e6ea0d24e3a28b4da34d74776fc011a8ff429afb1d5c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:29:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:29:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:29:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:29:49 GMT
USER fluent
# Tue, 18 Nov 2025 07:29:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d8370801a134071a40fe32d3d2fa7e0e17d18b25e5289e7237638fa8e7778`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 1.2 MB (1236519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b3223558fcb7b7da07de149d35cb77b0270a5ab9574f7885d63190a335526`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053f0fd615ae9d3957c571c9b6d06b6a892f68a64ba86fcf53aa1540117bbac`  
		Last Modified: Tue, 18 Nov 2025 05:02:15 GMT  
		Size: 37.9 MB (37865819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f081e8cb5f13e31c833ade5ef8bd8bc86005b1083ad01fb5c19150cfe1b852`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444514b6beb7cb41d5a6d74e2f02a6bd8d9b0d67d264bddba5cf5602534aef97`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 5.7 MB (5706176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281d992d9d5bfb4e3f3533290ac4e747701b996dfaa51bf4a1887a3d63f237ff`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9cd3785a6ed6fc017c3d377c407e31815775d28357a6cdbd99ac7ef4ebe6a9`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7153e50f421f23ea30db7f22fadac8133b4cf09d65d0fd4c239fa763debfcf8`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:612ec81a16bb05c27831a6a67cf5752e4bc1c6d4fb51cf3ec02bc176489ce778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee842d899c723e51f00df47d9670b2ed70e0e106f38477cc61e408fec563880`

```dockerfile
```

-	Layers:
	-	`sha256:ac725726a20c2cfebd9dd7c4277a0d190b6fe2958362e143a17129d44928298c`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 2.3 MB (2284970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff089d2e69179495169d3e05de805a988e7d4ff76570a57563e87343611f0ea`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a222dc7e9ddd2a1a1e14eda8278bac79c4b69652f2db613d6a31ca5838ea10cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79579468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c4933f2d7aba9a6cf42193fd309996c735faf39323e3cc9ce2adf1bd5b099f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:45:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:45:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:48:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:48:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:48:39 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 06:18:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 06:18:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 06:18:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 06:18:42 GMT
USER fluent
# Tue, 18 Nov 2025 06:18:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623192602c00e918197dfe6e2a1def0175e7be0d446a268ed38b6b5a621d38e0`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 1.3 MB (1261685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5fe6e2e9edffda349665022b4300b140e6a85f15a0f7614134df0867bcd551`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c522fdb9fff298474b76a11223cdcb250793d0c701b8cf389c0375800c7d5c`  
		Last Modified: Tue, 18 Nov 2025 04:48:57 GMT  
		Size: 42.1 MB (42145706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907ba9f7c5e39a58b009710a158a43136020eb8b46dc729f4426b65e03945ab`  
		Last Modified: Tue, 18 Nov 2025 04:48:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e287744781de6ba7990849d817b7d56815ea27a555f9b632c53f48912e6a8625`  
		Last Modified: Tue, 18 Nov 2025 06:19:03 GMT  
		Size: 6.0 MB (6031074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc83efe024d58f7c0f2ae54f8d1ca24212b0426b3b9f4ed85cf9dc2d9b4f138`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987698c2ecdcb3a42d62e47e6006334377b7ac96ac221f15c83c4f57ac5e185f`  
		Last Modified: Tue, 18 Nov 2025 06:18:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7418657ce63265bb53e93a85647829e7204dc7e5e55c4d2f68d731d36c14d5d`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:63307458ba12a55d8d3c164970c0601563d734a19561d3591fbecef80b4c26f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e9a7edd5a56936df00b963c56f0cc56c6857e45e7994aff9778145c3ba6dc9`

```dockerfile
```

-	Layers:
	-	`sha256:6f06e5d3a4506938173bb5f8471b70bec3c02332e7399634d46d17a90e3cda2a`  
		Last Modified: Tue, 18 Nov 2025 09:29:36 GMT  
		Size: 2.3 MB (2283830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0189ec4797d51709921e626666d44a28d1468c0300fac9c5b0a809df6e7ca1`  
		Last Modified: Tue, 18 Nov 2025 09:29:37 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bef966be95a2220ea41b52e0e83a8a622f90c5f320368a5f0d7284a00c503`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 1.3 MB (1287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45ed37d5457ae44f5b9a372ecc7bde1dd97d5be333bac0f4030719c7f0eca`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402fa9c5b261b8af75a607827e3e965cc7ce4351d91e3eba319a98783514bc3d`  
		Last Modified: Tue, 18 Nov 2025 03:43:29 GMT  
		Size: 37.7 MB (37740240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3646abfea40cabe9f48dabaff87823bc4de7febc7191871f992e8cdd29e5cc`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7a353d0f79751c2dce8dee5b2fded32d60934117291b83ec3d732116e194ffce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81069474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c794d9c800335e31b8d79aaf1dca07460a1300dc3c2092262bbf9a3870de6a5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:28:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 00:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:42:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:42:47 GMT
CMD ["irb"]
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Wed, 19 Nov 2025 01:48:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 19 Nov 2025 01:48:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 19 Nov 2025 01:48:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 19 Nov 2025 01:48:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 19 Nov 2025 01:48:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 19 Nov 2025 01:48:21 GMT
USER fluent
# Wed, 19 Nov 2025 01:48:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 19 Nov 2025 01:48:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbe0cbe7af169b8d7859f452f051f576ef4653fffd19a193922bbf502224d54`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 1.3 MB (1309674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a0a74191697331846ecf6cc860ffede09eafae29280e1dd04f2379b2dc07`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a0cff339fe641e08a65a97169cbbb4be8d7c4819ff50a706f2ed826916747`  
		Last Modified: Wed, 19 Nov 2025 00:43:23 GMT  
		Size: 39.6 MB (39601439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923e173b58f16848269bd5ce9e04bacdfaffeebd5dac19f837456978574583d6`  
		Last Modified: Wed, 19 Nov 2025 00:43:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fcdb627de74f9b8361edff9525a0fe6a33fdd953adf0fb2c0e3b00f9613e2b`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 6.6 MB (6559103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f259062e3fb7ae4681e323cc9047c9e3d00852e2125d9e493ac1ed5b8f53e103`  
		Last Modified: Wed, 19 Nov 2025 01:49:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ddab9ad7d500134abea5277fd0c7912069edbe26baf3a161f5b021d156ec75`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f4db3acfbcf50daa96589591259155ba6cc7fca7753781f8345d4843f6f05`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0730fbfa8014170ddc03be28fb1510037719c10514d7d5fb2f1ef694b66c9130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d1a4b27f5bebde2aadf39b7cfcbf1cbb93710322c8c18ee5f819d0ff0b4bdd`

```dockerfile
```

-	Layers:
	-	`sha256:692608745c585b5c51accdf3fb05f15ad958b401f00e1950d21c6de48529e978`  
		Last Modified: Wed, 19 Nov 2025 03:28:34 GMT  
		Size: 2.3 MB (2287093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6aad5bdc16681e7da44fc798332bef9931f9d15dd9899bd0d5f9f49af36bf2`  
		Last Modified: Wed, 19 Nov 2025 03:28:35 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:683484cc5debca5c0709f0c7d2d978e76f78712ebc852b4a4adc005d46ec25d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76835164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08e6e4b2bfe39b06d532dd33389c27a98d33b36b8e7146d75800194d194dc41`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:14:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 07:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5be0006390772cf7f9022344d107d52c9454ddfb26a9b6aa53e4f77a9bdc5e`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 1.3 MB (1294253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df3437f72c81d0de5473522e48eb46cf20ee4ae5ae981dfae54b48d71b07c5f`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67960768c1f544671789085d4901deaf00ad13d073997065fbd38e41baef3e`  
		Last Modified: Tue, 18 Nov 2025 05:17:09 GMT  
		Size: 39.3 MB (39287189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de67f11ad5b13189744a053b706d6a38590793d5b547a05561143636a6e794`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b6ba71f42284c745b166f743e6e50d1f0a6854eee654f4eb7cf742b48e808`  
		Last Modified: Tue, 18 Nov 2025 07:35:44 GMT  
		Size: 6.4 MB (6416958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d87c11925f40d6e2afa5a002fb413adc618d32a4c1f33ccd48c47e23b57b7`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082eb1114230c4c0724b38d35ab1fc4eee657526608a13dd9fd5d5e8a4a21bc9`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ab1a0cf3bc37e55bb698b7e2e76edb0e4cea56577c12907c808a17c957928`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3f8f214fada39a1a20d17924da461fedbaf16aecfbb0fa7591a3bc3b6bb69094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9677d7cdb6034256be28e74f6dfe5c2324badba6517a6567ec886a568e1a826c`

```dockerfile
```

-	Layers:
	-	`sha256:88a33b325036b2acdcbf4c3afa0c4f5711c06a125a88b8e4dddf20ed68e32d37`  
		Last Modified: Tue, 18 Nov 2025 09:29:45 GMT  
		Size: 2.3 MB (2285003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ed799d8ee14c02a6e9a62dbc69e63a23d15a697ba91568efc436ace9eb3ba1`  
		Last Modified: Tue, 18 Nov 2025 09:29:46 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-1.0`

```console
$ docker pull fluentd@sha256:8680b920563192348ac191fdda16ebce739da1d9bbc6c42711ab9d04942a24ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.19.0-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:aabf6e4d72df07f72c6320798286e38cb4078985fba7993be976076dd19c9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a904b3458ff5a124387f32960dfa2db38c96553803b6f1ca1aa65f98cd5c1f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:11:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:11:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:11:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:11:04 GMT
USER fluent
# Tue, 18 Nov 2025 07:11:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb0562513a544d09b243cd53af17176ae058cdb46bab21dc80e6e0e176085ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 1.3 MB (1279393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2995c07ae76a079f87ad5194b6ae8ae189e2697989ee2ec3ff402c4bbdbaef98`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8b74c7e9beb752e09eab60f51bfed7d4156be9c8a4cb31e65c1c593e477ad`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 42.2 MB (42158682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50951878876ddf823dfebd9e0c1677361d53bec1ff62831466fd280b78c485e7`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d897148a18c357950ad15bea0e1575bef5fe1a2f87069f845f212cbbf20eb783`  
		Last Modified: Tue, 18 Nov 2025 07:11:19 GMT  
		Size: 6.0 MB (6044983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba720e6453fce022701e4eb9ffad635c1814d3646e93621dca69a3739535b77`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2aea49a7fcbe5821ef2d28fd99597cefbdc90bbd576c99309e18724ebaddf`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c767a526bd60d2327b413b7336b31b1a00d72bc533f3b78d5137370859a100`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8cf6892824e97d161f124d5333687ef7b8eb6bf25f6aa2ccd03ef3a4b110b485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61709c4d165ab4eeaaedac4e4f88cd257d11b31708fbd397c45a227b866d23`

```dockerfile
```

-	Layers:
	-	`sha256:ee0b209bed1b2e569f4ce68fc851ee89e0ceb2f39e1afe579774bd04519a1711`  
		Last Modified: Tue, 18 Nov 2025 09:29:22 GMT  
		Size: 2.3 MB (2283558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2847675aad81b3637e07602402738b0ff18b4ecea6c1b1bf03ab8c53298839fc`  
		Last Modified: Tue, 18 Nov 2025 09:29:23 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8bddf98d29f007597c2419ece53918ed2a02b6807f244eba291b11a115ce2f`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 1.3 MB (1263024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce6e0d17644462250ed0239ef347ef83d3d46d91cc236e61f5d1ee58840ebe6`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dba72f3360e3a96295c7cea72647313a78f2723776a3e529d977bc6fb38431`  
		Last Modified: Tue, 18 Nov 2025 04:22:15 GMT  
		Size: 38.0 MB (37994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0930b6e7a3909c3d28136a1cc19c3a553fbbb2a2d33988cd25bd43effa0a140`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ffa87b2ef8721e0de3adac791ff08369238bf6c371e5932d6858ff86c97a8af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71020865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a309489b26daac336f6e6ea0d24e3a28b4da34d74776fc011a8ff429afb1d5c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:29:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:29:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:29:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:29:49 GMT
USER fluent
# Tue, 18 Nov 2025 07:29:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d8370801a134071a40fe32d3d2fa7e0e17d18b25e5289e7237638fa8e7778`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 1.2 MB (1236519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b3223558fcb7b7da07de149d35cb77b0270a5ab9574f7885d63190a335526`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053f0fd615ae9d3957c571c9b6d06b6a892f68a64ba86fcf53aa1540117bbac`  
		Last Modified: Tue, 18 Nov 2025 05:02:15 GMT  
		Size: 37.9 MB (37865819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f081e8cb5f13e31c833ade5ef8bd8bc86005b1083ad01fb5c19150cfe1b852`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444514b6beb7cb41d5a6d74e2f02a6bd8d9b0d67d264bddba5cf5602534aef97`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 5.7 MB (5706176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281d992d9d5bfb4e3f3533290ac4e747701b996dfaa51bf4a1887a3d63f237ff`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9cd3785a6ed6fc017c3d377c407e31815775d28357a6cdbd99ac7ef4ebe6a9`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7153e50f421f23ea30db7f22fadac8133b4cf09d65d0fd4c239fa763debfcf8`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:612ec81a16bb05c27831a6a67cf5752e4bc1c6d4fb51cf3ec02bc176489ce778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee842d899c723e51f00df47d9670b2ed70e0e106f38477cc61e408fec563880`

```dockerfile
```

-	Layers:
	-	`sha256:ac725726a20c2cfebd9dd7c4277a0d190b6fe2958362e143a17129d44928298c`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 2.3 MB (2284970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff089d2e69179495169d3e05de805a988e7d4ff76570a57563e87343611f0ea`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a222dc7e9ddd2a1a1e14eda8278bac79c4b69652f2db613d6a31ca5838ea10cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79579468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c4933f2d7aba9a6cf42193fd309996c735faf39323e3cc9ce2adf1bd5b099f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:45:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:45:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:48:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:48:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:48:39 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 06:18:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 06:18:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 06:18:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 06:18:42 GMT
USER fluent
# Tue, 18 Nov 2025 06:18:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623192602c00e918197dfe6e2a1def0175e7be0d446a268ed38b6b5a621d38e0`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 1.3 MB (1261685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5fe6e2e9edffda349665022b4300b140e6a85f15a0f7614134df0867bcd551`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c522fdb9fff298474b76a11223cdcb250793d0c701b8cf389c0375800c7d5c`  
		Last Modified: Tue, 18 Nov 2025 04:48:57 GMT  
		Size: 42.1 MB (42145706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907ba9f7c5e39a58b009710a158a43136020eb8b46dc729f4426b65e03945ab`  
		Last Modified: Tue, 18 Nov 2025 04:48:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e287744781de6ba7990849d817b7d56815ea27a555f9b632c53f48912e6a8625`  
		Last Modified: Tue, 18 Nov 2025 06:19:03 GMT  
		Size: 6.0 MB (6031074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc83efe024d58f7c0f2ae54f8d1ca24212b0426b3b9f4ed85cf9dc2d9b4f138`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987698c2ecdcb3a42d62e47e6006334377b7ac96ac221f15c83c4f57ac5e185f`  
		Last Modified: Tue, 18 Nov 2025 06:18:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7418657ce63265bb53e93a85647829e7204dc7e5e55c4d2f68d731d36c14d5d`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:63307458ba12a55d8d3c164970c0601563d734a19561d3591fbecef80b4c26f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e9a7edd5a56936df00b963c56f0cc56c6857e45e7994aff9778145c3ba6dc9`

```dockerfile
```

-	Layers:
	-	`sha256:6f06e5d3a4506938173bb5f8471b70bec3c02332e7399634d46d17a90e3cda2a`  
		Last Modified: Tue, 18 Nov 2025 09:29:36 GMT  
		Size: 2.3 MB (2283830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0189ec4797d51709921e626666d44a28d1468c0300fac9c5b0a809df6e7ca1`  
		Last Modified: Tue, 18 Nov 2025 09:29:37 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bef966be95a2220ea41b52e0e83a8a622f90c5f320368a5f0d7284a00c503`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 1.3 MB (1287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45ed37d5457ae44f5b9a372ecc7bde1dd97d5be333bac0f4030719c7f0eca`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402fa9c5b261b8af75a607827e3e965cc7ce4351d91e3eba319a98783514bc3d`  
		Last Modified: Tue, 18 Nov 2025 03:43:29 GMT  
		Size: 37.7 MB (37740240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3646abfea40cabe9f48dabaff87823bc4de7febc7191871f992e8cdd29e5cc`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7a353d0f79751c2dce8dee5b2fded32d60934117291b83ec3d732116e194ffce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81069474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c794d9c800335e31b8d79aaf1dca07460a1300dc3c2092262bbf9a3870de6a5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:28:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 00:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:42:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:42:47 GMT
CMD ["irb"]
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Wed, 19 Nov 2025 01:48:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 19 Nov 2025 01:48:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 19 Nov 2025 01:48:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 19 Nov 2025 01:48:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 19 Nov 2025 01:48:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 19 Nov 2025 01:48:21 GMT
USER fluent
# Wed, 19 Nov 2025 01:48:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 19 Nov 2025 01:48:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbe0cbe7af169b8d7859f452f051f576ef4653fffd19a193922bbf502224d54`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 1.3 MB (1309674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a0a74191697331846ecf6cc860ffede09eafae29280e1dd04f2379b2dc07`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a0cff339fe641e08a65a97169cbbb4be8d7c4819ff50a706f2ed826916747`  
		Last Modified: Wed, 19 Nov 2025 00:43:23 GMT  
		Size: 39.6 MB (39601439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923e173b58f16848269bd5ce9e04bacdfaffeebd5dac19f837456978574583d6`  
		Last Modified: Wed, 19 Nov 2025 00:43:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fcdb627de74f9b8361edff9525a0fe6a33fdd953adf0fb2c0e3b00f9613e2b`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 6.6 MB (6559103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f259062e3fb7ae4681e323cc9047c9e3d00852e2125d9e493ac1ed5b8f53e103`  
		Last Modified: Wed, 19 Nov 2025 01:49:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ddab9ad7d500134abea5277fd0c7912069edbe26baf3a161f5b021d156ec75`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f4db3acfbcf50daa96589591259155ba6cc7fca7753781f8345d4843f6f05`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0730fbfa8014170ddc03be28fb1510037719c10514d7d5fb2f1ef694b66c9130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d1a4b27f5bebde2aadf39b7cfcbf1cbb93710322c8c18ee5f819d0ff0b4bdd`

```dockerfile
```

-	Layers:
	-	`sha256:692608745c585b5c51accdf3fb05f15ad958b401f00e1950d21c6de48529e978`  
		Last Modified: Wed, 19 Nov 2025 03:28:34 GMT  
		Size: 2.3 MB (2287093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6aad5bdc16681e7da44fc798332bef9931f9d15dd9899bd0d5f9f49af36bf2`  
		Last Modified: Wed, 19 Nov 2025 03:28:35 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:683484cc5debca5c0709f0c7d2d978e76f78712ebc852b4a4adc005d46ec25d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76835164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08e6e4b2bfe39b06d532dd33389c27a98d33b36b8e7146d75800194d194dc41`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:14:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 07:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5be0006390772cf7f9022344d107d52c9454ddfb26a9b6aa53e4f77a9bdc5e`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 1.3 MB (1294253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df3437f72c81d0de5473522e48eb46cf20ee4ae5ae981dfae54b48d71b07c5f`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67960768c1f544671789085d4901deaf00ad13d073997065fbd38e41baef3e`  
		Last Modified: Tue, 18 Nov 2025 05:17:09 GMT  
		Size: 39.3 MB (39287189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de67f11ad5b13189744a053b706d6a38590793d5b547a05561143636a6e794`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b6ba71f42284c745b166f743e6e50d1f0a6854eee654f4eb7cf742b48e808`  
		Last Modified: Tue, 18 Nov 2025 07:35:44 GMT  
		Size: 6.4 MB (6416958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d87c11925f40d6e2afa5a002fb413adc618d32a4c1f33ccd48c47e23b57b7`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082eb1114230c4c0724b38d35ab1fc4eee657526608a13dd9fd5d5e8a4a21bc9`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ab1a0cf3bc37e55bb698b7e2e76edb0e4cea56577c12907c808a17c957928`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3f8f214fada39a1a20d17924da461fedbaf16aecfbb0fa7591a3bc3b6bb69094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9677d7cdb6034256be28e74f6dfe5c2324badba6517a6567ec886a568e1a826c`

```dockerfile
```

-	Layers:
	-	`sha256:88a33b325036b2acdcbf4c3afa0c4f5711c06a125a88b8e4dddf20ed68e32d37`  
		Last Modified: Tue, 18 Nov 2025 09:29:45 GMT  
		Size: 2.3 MB (2285003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ed799d8ee14c02a6e9a62dbc69e63a23d15a697ba91568efc436ace9eb3ba1`  
		Last Modified: Tue, 18 Nov 2025 09:29:46 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-debian-1.0`

```console
$ docker pull fluentd@sha256:8680b920563192348ac191fdda16ebce739da1d9bbc6c42711ab9d04942a24ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.19.0-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:aabf6e4d72df07f72c6320798286e38cb4078985fba7993be976076dd19c9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a904b3458ff5a124387f32960dfa2db38c96553803b6f1ca1aa65f98cd5c1f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:11:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:11:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:11:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:11:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:11:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:11:04 GMT
USER fluent
# Tue, 18 Nov 2025 07:11:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:11:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb0562513a544d09b243cd53af17176ae058cdb46bab21dc80e6e0e176085ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 1.3 MB (1279393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2995c07ae76a079f87ad5194b6ae8ae189e2697989ee2ec3ff402c4bbdbaef98`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8b74c7e9beb752e09eab60f51bfed7d4156be9c8a4cb31e65c1c593e477ad`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 42.2 MB (42158682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50951878876ddf823dfebd9e0c1677361d53bec1ff62831466fd280b78c485e7`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d897148a18c357950ad15bea0e1575bef5fe1a2f87069f845f212cbbf20eb783`  
		Last Modified: Tue, 18 Nov 2025 07:11:19 GMT  
		Size: 6.0 MB (6044983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba720e6453fce022701e4eb9ffad635c1814d3646e93621dca69a3739535b77`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2aea49a7fcbe5821ef2d28fd99597cefbdc90bbd576c99309e18724ebaddf`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c767a526bd60d2327b413b7336b31b1a00d72bc533f3b78d5137370859a100`  
		Last Modified: Tue, 18 Nov 2025 07:11:18 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8cf6892824e97d161f124d5333687ef7b8eb6bf25f6aa2ccd03ef3a4b110b485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61709c4d165ab4eeaaedac4e4f88cd257d11b31708fbd397c45a227b866d23`

```dockerfile
```

-	Layers:
	-	`sha256:ee0b209bed1b2e569f4ce68fc851ee89e0ceb2f39e1afe579774bd04519a1711`  
		Last Modified: Tue, 18 Nov 2025 09:29:22 GMT  
		Size: 2.3 MB (2283558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2847675aad81b3637e07602402738b0ff18b4ecea6c1b1bf03ab8c53298839fc`  
		Last Modified: Tue, 18 Nov 2025 09:29:23 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8bddf98d29f007597c2419ece53918ed2a02b6807f244eba291b11a115ce2f`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 1.3 MB (1263024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce6e0d17644462250ed0239ef347ef83d3d46d91cc236e61f5d1ee58840ebe6`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dba72f3360e3a96295c7cea72647313a78f2723776a3e529d977bc6fb38431`  
		Last Modified: Tue, 18 Nov 2025 04:22:15 GMT  
		Size: 38.0 MB (37994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0930b6e7a3909c3d28136a1cc19c3a553fbbb2a2d33988cd25bd43effa0a140`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ffa87b2ef8721e0de3adac791ff08369238bf6c371e5932d6858ff86c97a8af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71020865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a309489b26daac336f6e6ea0d24e3a28b4da34d74776fc011a8ff429afb1d5c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:29:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:29:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:29:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:29:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:29:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:29:49 GMT
USER fluent
# Tue, 18 Nov 2025 07:29:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:29:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d8370801a134071a40fe32d3d2fa7e0e17d18b25e5289e7237638fa8e7778`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 1.2 MB (1236519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b3223558fcb7b7da07de149d35cb77b0270a5ab9574f7885d63190a335526`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053f0fd615ae9d3957c571c9b6d06b6a892f68a64ba86fcf53aa1540117bbac`  
		Last Modified: Tue, 18 Nov 2025 05:02:15 GMT  
		Size: 37.9 MB (37865819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f081e8cb5f13e31c833ade5ef8bd8bc86005b1083ad01fb5c19150cfe1b852`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444514b6beb7cb41d5a6d74e2f02a6bd8d9b0d67d264bddba5cf5602534aef97`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 5.7 MB (5706176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281d992d9d5bfb4e3f3533290ac4e747701b996dfaa51bf4a1887a3d63f237ff`  
		Last Modified: Tue, 18 Nov 2025 07:30:06 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9cd3785a6ed6fc017c3d377c407e31815775d28357a6cdbd99ac7ef4ebe6a9`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7153e50f421f23ea30db7f22fadac8133b4cf09d65d0fd4c239fa763debfcf8`  
		Last Modified: Tue, 18 Nov 2025 07:30:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:612ec81a16bb05c27831a6a67cf5752e4bc1c6d4fb51cf3ec02bc176489ce778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee842d899c723e51f00df47d9670b2ed70e0e106f38477cc61e408fec563880`

```dockerfile
```

-	Layers:
	-	`sha256:ac725726a20c2cfebd9dd7c4277a0d190b6fe2958362e143a17129d44928298c`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 2.3 MB (2284970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff089d2e69179495169d3e05de805a988e7d4ff76570a57563e87343611f0ea`  
		Last Modified: Tue, 18 Nov 2025 09:29:32 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a222dc7e9ddd2a1a1e14eda8278bac79c4b69652f2db613d6a31ca5838ea10cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79579468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c4933f2d7aba9a6cf42193fd309996c735faf39323e3cc9ce2adf1bd5b099f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:45:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:45:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:48:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:48:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:48:39 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 06:18:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 06:18:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 06:18:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 06:18:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 06:18:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 06:18:42 GMT
USER fluent
# Tue, 18 Nov 2025 06:18:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 06:18:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623192602c00e918197dfe6e2a1def0175e7be0d446a268ed38b6b5a621d38e0`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 1.3 MB (1261685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5fe6e2e9edffda349665022b4300b140e6a85f15a0f7614134df0867bcd551`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c522fdb9fff298474b76a11223cdcb250793d0c701b8cf389c0375800c7d5c`  
		Last Modified: Tue, 18 Nov 2025 04:48:57 GMT  
		Size: 42.1 MB (42145706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907ba9f7c5e39a58b009710a158a43136020eb8b46dc729f4426b65e03945ab`  
		Last Modified: Tue, 18 Nov 2025 04:48:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e287744781de6ba7990849d817b7d56815ea27a555f9b632c53f48912e6a8625`  
		Last Modified: Tue, 18 Nov 2025 06:19:03 GMT  
		Size: 6.0 MB (6031074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc83efe024d58f7c0f2ae54f8d1ca24212b0426b3b9f4ed85cf9dc2d9b4f138`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987698c2ecdcb3a42d62e47e6006334377b7ac96ac221f15c83c4f57ac5e185f`  
		Last Modified: Tue, 18 Nov 2025 06:18:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7418657ce63265bb53e93a85647829e7204dc7e5e55c4d2f68d731d36c14d5d`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:63307458ba12a55d8d3c164970c0601563d734a19561d3591fbecef80b4c26f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e9a7edd5a56936df00b963c56f0cc56c6857e45e7994aff9778145c3ba6dc9`

```dockerfile
```

-	Layers:
	-	`sha256:6f06e5d3a4506938173bb5f8471b70bec3c02332e7399634d46d17a90e3cda2a`  
		Last Modified: Tue, 18 Nov 2025 09:29:36 GMT  
		Size: 2.3 MB (2283830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0189ec4797d51709921e626666d44a28d1468c0300fac9c5b0a809df6e7ca1`  
		Last Modified: Tue, 18 Nov 2025 09:29:37 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bef966be95a2220ea41b52e0e83a8a622f90c5f320368a5f0d7284a00c503`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 1.3 MB (1287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45ed37d5457ae44f5b9a372ecc7bde1dd97d5be333bac0f4030719c7f0eca`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402fa9c5b261b8af75a607827e3e965cc7ce4351d91e3eba319a98783514bc3d`  
		Last Modified: Tue, 18 Nov 2025 03:43:29 GMT  
		Size: 37.7 MB (37740240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3646abfea40cabe9f48dabaff87823bc4de7febc7191871f992e8cdd29e5cc`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7a353d0f79751c2dce8dee5b2fded32d60934117291b83ec3d732116e194ffce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81069474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c794d9c800335e31b8d79aaf1dca07460a1300dc3c2092262bbf9a3870de6a5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:28:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 00:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:42:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:42:47 GMT
CMD ["irb"]
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 19 Nov 2025 01:48:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Wed, 19 Nov 2025 01:48:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 19 Nov 2025 01:48:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 19 Nov 2025 01:48:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 19 Nov 2025 01:48:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 19 Nov 2025 01:48:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 19 Nov 2025 01:48:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 19 Nov 2025 01:48:21 GMT
USER fluent
# Wed, 19 Nov 2025 01:48:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 19 Nov 2025 01:48:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbe0cbe7af169b8d7859f452f051f576ef4653fffd19a193922bbf502224d54`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 1.3 MB (1309674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a0a74191697331846ecf6cc860ffede09eafae29280e1dd04f2379b2dc07`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a0cff339fe641e08a65a97169cbbb4be8d7c4819ff50a706f2ed826916747`  
		Last Modified: Wed, 19 Nov 2025 00:43:23 GMT  
		Size: 39.6 MB (39601439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923e173b58f16848269bd5ce9e04bacdfaffeebd5dac19f837456978574583d6`  
		Last Modified: Wed, 19 Nov 2025 00:43:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fcdb627de74f9b8361edff9525a0fe6a33fdd953adf0fb2c0e3b00f9613e2b`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 6.6 MB (6559103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f259062e3fb7ae4681e323cc9047c9e3d00852e2125d9e493ac1ed5b8f53e103`  
		Last Modified: Wed, 19 Nov 2025 01:49:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ddab9ad7d500134abea5277fd0c7912069edbe26baf3a161f5b021d156ec75`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f4db3acfbcf50daa96589591259155ba6cc7fca7753781f8345d4843f6f05`  
		Last Modified: Wed, 19 Nov 2025 01:49:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0730fbfa8014170ddc03be28fb1510037719c10514d7d5fb2f1ef694b66c9130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d1a4b27f5bebde2aadf39b7cfcbf1cbb93710322c8c18ee5f819d0ff0b4bdd`

```dockerfile
```

-	Layers:
	-	`sha256:692608745c585b5c51accdf3fb05f15ad958b401f00e1950d21c6de48529e978`  
		Last Modified: Wed, 19 Nov 2025 03:28:34 GMT  
		Size: 2.3 MB (2287093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6aad5bdc16681e7da44fc798332bef9931f9d15dd9899bd0d5f9f49af36bf2`  
		Last Modified: Wed, 19 Nov 2025 03:28:35 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:683484cc5debca5c0709f0c7d2d978e76f78712ebc852b4a4adc005d46ec25d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76835164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08e6e4b2bfe39b06d532dd33389c27a98d33b36b8e7146d75800194d194dc41`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:14:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 07:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 07:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 07:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 07:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 07:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 07:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 07:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 07:35:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5be0006390772cf7f9022344d107d52c9454ddfb26a9b6aa53e4f77a9bdc5e`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 1.3 MB (1294253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df3437f72c81d0de5473522e48eb46cf20ee4ae5ae981dfae54b48d71b07c5f`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67960768c1f544671789085d4901deaf00ad13d073997065fbd38e41baef3e`  
		Last Modified: Tue, 18 Nov 2025 05:17:09 GMT  
		Size: 39.3 MB (39287189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de67f11ad5b13189744a053b706d6a38590793d5b547a05561143636a6e794`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b6ba71f42284c745b166f743e6e50d1f0a6854eee654f4eb7cf742b48e808`  
		Last Modified: Tue, 18 Nov 2025 07:35:44 GMT  
		Size: 6.4 MB (6416958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d87c11925f40d6e2afa5a002fb413adc618d32a4c1f33ccd48c47e23b57b7`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082eb1114230c4c0724b38d35ab1fc4eee657526608a13dd9fd5d5e8a4a21bc9`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ab1a0cf3bc37e55bb698b7e2e76edb0e4cea56577c12907c808a17c957928`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3f8f214fada39a1a20d17924da461fedbaf16aecfbb0fa7591a3bc3b6bb69094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9677d7cdb6034256be28e74f6dfe5c2324badba6517a6567ec886a568e1a826c`

```dockerfile
```

-	Layers:
	-	`sha256:88a33b325036b2acdcbf4c3afa0c4f5711c06a125a88b8e4dddf20ed68e32d37`  
		Last Modified: Tue, 18 Nov 2025 09:29:45 GMT  
		Size: 2.3 MB (2285003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ed799d8ee14c02a6e9a62dbc69e63a23d15a697ba91568efc436ace9eb3ba1`  
		Last Modified: Tue, 18 Nov 2025 09:29:46 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json
