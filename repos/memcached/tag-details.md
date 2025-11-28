<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.22`](#memcached1-alpine322)
-	[`memcached:1-trixie`](#memcached1-trixie)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.22`](#memcached16-alpine322)
-	[`memcached:1.6-trixie`](#memcached16-trixie)
-	[`memcached:1.6.39`](#memcached1639)
-	[`memcached:1.6.39-alpine`](#memcached1639-alpine)
-	[`memcached:1.6.39-alpine3.22`](#memcached1639-alpine322)
-	[`memcached:1.6.39-trixie`](#memcached1639-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.22`](#memcachedalpine322)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:1-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:1-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:1.6-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:1.6-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:1.6.39` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:1.6.39-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:1.6.39-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-trixie`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:1.6.39-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:4737e17016e4d65ad8007408ec1816096c4ebec04cfa89a5265a3edd3f4ca552
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

### `memcached:trixie` - linux; amd64

```console
$ docker pull memcached@sha256:3b5631af36455e8299750af72d1ee833e8d2460cf7b62a804eb5b4cab02b26da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfa206a43582385cda21c6b8922dec22741b8568cf317cf099c021b888aeca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:23:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 04:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 04:26:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 04:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 04:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:26:14 GMT
USER memcache
# Tue, 18 Nov 2025 04:26:14 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 04:26:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb6d15c038af22e52543a0e522b7a752f6cc8ec90064aedcfbcdc03e6ec391`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc826358ea7d470733a2c18ce0896d9c3a4d8b5adaa7a591b5718bcb797d2627`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b01f1d184f92d8b894802650ad4042d0893084d19f47cb0f64bd10ce46089`  
		Last Modified: Tue, 18 Nov 2025 04:26:30 GMT  
		Size: 2.3 MB (2293764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4d54e0494382ae87d8fed0ff5fe7c01d27b58ee6fcd8caa2c48f682d6fa1f`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429961289f6ce0e104759d3e41602f6f4be87b8e01c8a75a98e9e4cc51c3bc4b`  
		Last Modified: Tue, 18 Nov 2025 04:26:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7885852fdb19cb6883c6f0ebcea600b7dc88baeb84b927c65f31c9dcdcfa7e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000decf9c4792c3fb136e1cd547d08096fb11ba21563ea8887659092e8d8fc5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8355d177304230252df7db41a05396377ca83eee57481d790d863edc83c16a`  
		Last Modified: Tue, 18 Nov 2025 07:35:31 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223989c11f988c4d7bcb88b14b8a0621dbe339df3c374cf848597e08845e69d`  
		Last Modified: Tue, 18 Nov 2025 07:35:32 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:74624cdf88718ea89adb212ff7c85a1203d4f910c2a105577b593bab1cd2adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aacd5c6adc02e5e2898b5d03020085e3c0b8d2b96aa68cd3693f44b574dc992`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:26:06 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:26:06 GMT
USER memcache
# Tue, 18 Nov 2025 02:26:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:26:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b0dda729f2d014e2d3a9c0249a40505436d72ca1fa92b54dd85a38385ba8`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6f6ab2b73ee9afae6cc5b14e689ae9b7444eedc9686390a83d27fa14596c3c`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 144.2 KB (144151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0aec11ee80f5d3e9c60f38f130f8ef52d70e3881adaecbbd04a357e91d8f8c`  
		Last Modified: Tue, 18 Nov 2025 02:26:20 GMT  
		Size: 2.2 MB (2227398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f15138c562ac9e96e0c85947fdb7bf8849fb632b842f7305c9ed3b3e771f27`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b1f3ba4847f73e280fcb51ed05b9123263142abf85a6932e1583ce181b5f5`  
		Last Modified: Tue, 18 Nov 2025 02:26:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414363643bb871a32d08411ecfc86fb76da6953b92f8986cd91146dc1c0bd2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ac505ef632d88b7a7dfa719e78a6201057579aaf50439621b2916851a8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:22227a1a074a3dad86cdcbae93b96c7c3201fa8c5910f69a24c07a39436b32b7`  
		Last Modified: Tue, 18 Nov 2025 04:36:08 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7d813d3b59bb5538ab3de1a0752d915dc6c82f40c2c1b2cf932d8df9515d7`  
		Last Modified: Tue, 18 Nov 2025 04:36:09 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:60b96acc1d51c495709962faba1c3293d1ce32ef81f773a99a073a95970bc3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c5362573d54fdb4b859b5a82d16e91b3f46516f7e9908297fc2ac93e83533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:19:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:47 GMT
USER memcache
# Tue, 18 Nov 2025 02:19:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:19:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813f89cb3e639bc57bfae4fbc5934681a880766de61773781d5d8c1a9328af89`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482c804ccbec693e3f5e2f523df3274a68c6b3bad94d01af6b1a8c7993f420d`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 135.4 KB (135365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d5cdd7bcb9a401e7206ab312bc24e98c033c1f0d08356a636b8852b4e4b`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 2.2 MB (2182635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca31f7962d4314a142152e6e4632a05257cff82b6df6166856b404e4f873464`  
		Last Modified: Tue, 18 Nov 2025 02:20:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c20c45a246a82a540c758932061f1c9ecaa51b901b36059fa4f292f3de3f3`  
		Last Modified: Tue, 18 Nov 2025 02:19:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:02d49d178b92f900f98719a4d5935345a7c54633a1e0562bc7cdedcc8283296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e867e35aca069129a38dc8df404b1d2965571c2c1dd79269a18134d5cdaae1`

```dockerfile
```

-	Layers:
	-	`sha256:387ca2f046b3d7460c278fc3c277e51238bcdedfbd434866c945b02762abf9f8`  
		Last Modified: Tue, 18 Nov 2025 04:36:12 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa697bd9e15f3f5ffe33e740916fd44faa7d8cda7778c9231f812b32b276439`  
		Last Modified: Tue, 18 Nov 2025 04:36:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:915f5883fd00e5600fc669e3cb4b2b87230250b627716a575089fbc35fc32ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3c1223ede0c326de2f24464ceffba4f8081499a66e1e78528d0a3db6158694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:24:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:24:12 GMT
USER memcache
# Tue, 18 Nov 2025 02:24:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:24:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0ffd9487d55cf2751d2bae5b44240bd3587b72795c52fbfff187b1f7a0f06`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b0e405da1d276065a6a919318b81b4c50cccd39839e3e4867802e40078167`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475beb02abe44f61417f69a919f1a92a4dbea5c68f46b87365d001bb5f028108`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 2.3 MB (2275292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354cc71a19400062b8f9c95f5390f644df8e35f860aa65011dfa3543c72010a`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e398cb800ea761b4ac982cce173267e7d03a89268da329d2d7b682ebc6114`  
		Last Modified: Tue, 18 Nov 2025 02:24:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:22cb1b1380515acfb2bafaf54f8805f9aa7769a0d35dedc7a84c73726e574789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14cb78b64f2ce16b3f762982744f8a60ecebd626ee351adc81c97a236a3aea3`

```dockerfile
```

-	Layers:
	-	`sha256:e09818ab5f9a20d6ae59767d3ceb5daa4a7c10ff1baa8035f4a8640b229aae64`  
		Last Modified: Tue, 18 Nov 2025 04:36:17 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19de7f5d8c9194fd3e499a7f91266d07b4c4e93d02aff48033b9458462f206`  
		Last Modified: Tue, 18 Nov 2025 04:36:18 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:b6980ce6f21f8c78c73008ee1f8e4fb1b52ef464c3f6664f86afdd8c8e707056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9426284fe3013a3c025a1e84e72ab4e23b952305fefc3b1c03df0e8bd7812858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:20:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:20:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:18 GMT
USER memcache
# Tue, 18 Nov 2025 02:20:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:20:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a5438fe067ad735e5255bec13776b322efac8dacc5734557fcf519744ec9c`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44cbfd31ce48837c164b4fc7454710cf8e20c49e8a585c27bc06293bac83bec`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e2698eb1e4ec99376f9ed0eaef19ed9ca930b5a7d386492b107172c4481136`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 2.2 MB (2244487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44018437bffca5a62c87499f682ba96f7999019b1afc80e73c11f3136f5bbc0a`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449e3a8f8a6658ea420ae173dc5ebe092cc3e7a99093ea358b2f23beddf6460`  
		Last Modified: Tue, 18 Nov 2025 02:20:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4e045d1e422d7d521052f98c768821c97527a7883021dc972ddbcfc697a283df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a4316d28622e1af89c8aa459f49cec2f26e9f877a7a9d0b5ea6cad21917e0`

```dockerfile
```

-	Layers:
	-	`sha256:9c4de8472aa3ffc5eb31df3f23c9f640013682ab6993350c0e5517dcbd3b8444`  
		Last Modified: Tue, 18 Nov 2025 04:36:21 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3fa64b4151797703998c6b6286cb58bb8e085d604ab26942b555bbef12f65c`  
		Last Modified: Tue, 18 Nov 2025 04:36:22 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:a518bb3f855838b2b32886d334a14804222660166a1b8805966601639f93288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e916a0cab98baf1b61a08233960751c21ef4149790af3482010933400709c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:09:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 15:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 15:12:19 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 15:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 15:12:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 15:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:12:22 GMT
USER memcache
# Tue, 18 Nov 2025 15:12:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 15:12:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207739f12090f6183c3da957e4ac149a40bb1f140a1b24affb85b9f9ba9383f6`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84a2c0ced11f54044651016c3f59838fd495c5121d6cd0203781220f96bf6d`  
		Last Modified: Tue, 18 Nov 2025 15:12:48 GMT  
		Size: 170.4 KB (170374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a4a5164ada533afb736da249751a248cd8a863359b5e6385173793f74da1f`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 2.4 MB (2417058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5fa31e17fcbd86308f76dea47d69364884e98b98a31247efb5dbb252bdfb68`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddaac32ba0f3bdb45d6ae334c41d9b1832e2518377ea0efbb1d58648634f02`  
		Last Modified: Tue, 18 Nov 2025 15:12:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:64141fed6331ae24c568b626c0c2bd3dffe3258605cfd9e86432488ba121459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d114447515e28e91e9f90103727021ca4386eb18dab5057ba34e9587e6d277`

```dockerfile
```

-	Layers:
	-	`sha256:546b487f1fca08653bbe64cd8a96568fcfa31e4e79b868f60d93dca8b1c50776`  
		Last Modified: Tue, 18 Nov 2025 16:35:39 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c5c5891c11541e79f0b10a3937a4f286a3566313b2e25d3f0ec25bfc10276`  
		Last Modified: Tue, 18 Nov 2025 16:35:40 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:913554560a16e48f36f79dde1a9dcb9d5c2d6f0ff0ef7673bb58f00412e29e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa6876c5a793be59639ef725486bf6414c0384d9da655680d0f4e684178b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 02:21:00 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 02:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:00 GMT
USER memcache
# Tue, 18 Nov 2025 02:21:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 02:21:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92033d86725d50fea63c55b87da3aa1cbdfd4f2dbed19c8c7a72defb69810fb1`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4edc2d80acee7885694230d51b82e6d382715ca75282f8960b6547da407031`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 140.5 KB (140515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5265bbf38dd99f28f5a5eafd305c90277d9e451158f78a828fd404b7860e5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 2.3 MB (2313919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c8f59821004cd068efe1987d8ef9a44796820532248be68865c883fd682ae`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b8554de401e4168cb74c44ad837fe035d647f99cbee5a9dddc90f0b67f2a5`  
		Last Modified: Tue, 18 Nov 2025 02:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:710a0f236c321fd2da025ac7da7e54661d699a3efadc8ac247e5c91cc7d2fef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e078f0d6a7d898d7177cf2a568c3fd83ebac0cde831293e98d50bd8fe9bcbcc`

```dockerfile
```

-	Layers:
	-	`sha256:640a337c5f804d3955dfe34e89145207caa4965eff382da4c36bc9567a6d526a`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf09708bbedb3258107a8178d5f28743c79fd38e82c87033e2143195f5bf83`  
		Last Modified: Tue, 18 Nov 2025 04:36:31 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
