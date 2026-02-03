<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.23`](#memcached1-alpine323)
-	[`memcached:1-trixie`](#memcached1-trixie)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.23`](#memcached16-alpine323)
-	[`memcached:1.6-trixie`](#memcached16-trixie)
-	[`memcached:1.6.40`](#memcached1640)
-	[`memcached:1.6.40-alpine`](#memcached1640-alpine)
-	[`memcached:1.6.40-alpine3.23`](#memcached1640-alpine323)
-	[`memcached:1.6.40-trixie`](#memcached1640-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.23`](#memcachedalpine323)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:614632cd0e4f68380f3e70c7d185bbb02064a200c58ec37d415ce851b3c6f7b5
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
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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

### `memcached:1-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:a549727caea26e26aaed638999d18e36fc3d2d10914984d0dad6044a8d0afe2d
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
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:ecb538ebf8e4fd42c99ea9085af2db2eb071e8b5c355f4d201413f251ed2038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26d0c572a242b8dc66b373b4742b72a9a7b80dffead45b7971bd3ca630c9b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:20:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:23:41 GMT
USER memcache
# Tue, 03 Feb 2026 02:23:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:23:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae20ac32290a2e03cd891e9b945d06d7024406459071085bd1448b68d658ee5`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f514c583d7e781595c671ad8a7f5df992bd28ffc8813cff3887e26986a43da0f`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 135.4 KB (135376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a85d6ff0660b7c9b74cd4b96de9c52eacd145eb3a1ee9f25424438dd1faa8a`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.2 MB (2164064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fc092ba150b1ba71f5eef8fad886bcba5bc55f1e1085165dd0b89022b56c7e`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99816ca9e16c3f3e53814030eaf19374708b033ea07fb33523400aae1464bf76`  
		Last Modified: Tue, 03 Feb 2026 02:23:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:95bce324745f1bb3aedbf8f587294282f40910f591c187728e1002b340f252f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7149d843bf5392962c85f12f82c6072f462a3542132af0b3a37d79cffcaa8c`

```dockerfile
```

-	Layers:
	-	`sha256:8ef5ccfe9e83e6980056c22ff32ee579b2d9d0fbb139a03e8a4b53eaa0e23d26`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e90de86ba479b9d32e34044c75ef7355aec8fa29ae346ad6d3b42b7c910d8c`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:614632cd0e4f68380f3e70c7d185bbb02064a200c58ec37d415ce851b3c6f7b5
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
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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

### `memcached:1.6-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:a549727caea26e26aaed638999d18e36fc3d2d10914984d0dad6044a8d0afe2d
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
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:ecb538ebf8e4fd42c99ea9085af2db2eb071e8b5c355f4d201413f251ed2038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26d0c572a242b8dc66b373b4742b72a9a7b80dffead45b7971bd3ca630c9b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:20:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:23:41 GMT
USER memcache
# Tue, 03 Feb 2026 02:23:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:23:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae20ac32290a2e03cd891e9b945d06d7024406459071085bd1448b68d658ee5`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f514c583d7e781595c671ad8a7f5df992bd28ffc8813cff3887e26986a43da0f`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 135.4 KB (135376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a85d6ff0660b7c9b74cd4b96de9c52eacd145eb3a1ee9f25424438dd1faa8a`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.2 MB (2164064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fc092ba150b1ba71f5eef8fad886bcba5bc55f1e1085165dd0b89022b56c7e`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99816ca9e16c3f3e53814030eaf19374708b033ea07fb33523400aae1464bf76`  
		Last Modified: Tue, 03 Feb 2026 02:23:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:95bce324745f1bb3aedbf8f587294282f40910f591c187728e1002b340f252f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7149d843bf5392962c85f12f82c6072f462a3542132af0b3a37d79cffcaa8c`

```dockerfile
```

-	Layers:
	-	`sha256:8ef5ccfe9e83e6980056c22ff32ee579b2d9d0fbb139a03e8a4b53eaa0e23d26`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e90de86ba479b9d32e34044c75ef7355aec8fa29ae346ad6d3b42b7c910d8c`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40`

```console
$ docker pull memcached@sha256:a549727caea26e26aaed638999d18e36fc3d2d10914984d0dad6044a8d0afe2d
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

### `memcached:1.6.40` - linux; amd64

```console
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v7

```console
$ docker pull memcached@sha256:ecb538ebf8e4fd42c99ea9085af2db2eb071e8b5c355f4d201413f251ed2038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26d0c572a242b8dc66b373b4742b72a9a7b80dffead45b7971bd3ca630c9b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:20:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:23:41 GMT
USER memcache
# Tue, 03 Feb 2026 02:23:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:23:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae20ac32290a2e03cd891e9b945d06d7024406459071085bd1448b68d658ee5`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f514c583d7e781595c671ad8a7f5df992bd28ffc8813cff3887e26986a43da0f`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 135.4 KB (135376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a85d6ff0660b7c9b74cd4b96de9c52eacd145eb3a1ee9f25424438dd1faa8a`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.2 MB (2164064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fc092ba150b1ba71f5eef8fad886bcba5bc55f1e1085165dd0b89022b56c7e`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99816ca9e16c3f3e53814030eaf19374708b033ea07fb33523400aae1464bf76`  
		Last Modified: Tue, 03 Feb 2026 02:23:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:95bce324745f1bb3aedbf8f587294282f40910f591c187728e1002b340f252f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7149d843bf5392962c85f12f82c6072f462a3542132af0b3a37d79cffcaa8c`

```dockerfile
```

-	Layers:
	-	`sha256:8ef5ccfe9e83e6980056c22ff32ee579b2d9d0fbb139a03e8a4b53eaa0e23d26`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e90de86ba479b9d32e34044c75ef7355aec8fa29ae346ad6d3b42b7c910d8c`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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

### `memcached:1.6.40-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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

### `memcached:1.6.40-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-trixie`

```console
$ docker pull memcached@sha256:a549727caea26e26aaed638999d18e36fc3d2d10914984d0dad6044a8d0afe2d
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

### `memcached:1.6.40-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:ecb538ebf8e4fd42c99ea9085af2db2eb071e8b5c355f4d201413f251ed2038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26d0c572a242b8dc66b373b4742b72a9a7b80dffead45b7971bd3ca630c9b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:20:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:23:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:23:41 GMT
USER memcache
# Tue, 03 Feb 2026 02:23:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:23:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae20ac32290a2e03cd891e9b945d06d7024406459071085bd1448b68d658ee5`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f514c583d7e781595c671ad8a7f5df992bd28ffc8813cff3887e26986a43da0f`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 135.4 KB (135376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a85d6ff0660b7c9b74cd4b96de9c52eacd145eb3a1ee9f25424438dd1faa8a`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.2 MB (2164064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fc092ba150b1ba71f5eef8fad886bcba5bc55f1e1085165dd0b89022b56c7e`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99816ca9e16c3f3e53814030eaf19374708b033ea07fb33523400aae1464bf76`  
		Last Modified: Tue, 03 Feb 2026 02:23:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:95bce324745f1bb3aedbf8f587294282f40910f591c187728e1002b340f252f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7149d843bf5392962c85f12f82c6072f462a3542132af0b3a37d79cffcaa8c`

```dockerfile
```

-	Layers:
	-	`sha256:8ef5ccfe9e83e6980056c22ff32ee579b2d9d0fbb139a03e8a4b53eaa0e23d26`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e90de86ba479b9d32e34044c75ef7355aec8fa29ae346ad6d3b42b7c910d8c`  
		Last Modified: Tue, 03 Feb 2026 02:23:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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

### `memcached:alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:614632cd0e4f68380f3e70c7d185bbb02064a200c58ec37d415ce851b3c6f7b5
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
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:614632cd0e4f68380f3e70c7d185bbb02064a200c58ec37d415ce851b3c6f7b5
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
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2b7b5039ee621410d5520d71ee3c4b421d912b8f5863c367872e545e15a885c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5488d71efb3ec1556a38e9e2996dbf727524855963a4b342be00dec5e34a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:19 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:19 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:19 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdb733d88a9038d4494fa2c86d4042cf701e7e037e1919dace5f42e1145903`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16789397ba00f5e998cd83cc368d15fde580fa5ff2b1d63823169c37a6eefd53`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 153.5 KB (153493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eeb9c937f4b000214f9d19ecd9598e8b5ed5aa014ca0c7fd828bd7195d2660`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a826201cf9db200077a8444cfa6c57bfcbf1ea6b627bd0e14f0f5f0d2b1b59c`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d59dfbd2334d5876ece943e7231e23c12f3505b5f228ad51841b6af7f6cdd`  
		Last Modified: Tue, 03 Feb 2026 02:25:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b8db6bca88120a03c511b315a5ea3c2d0c3dc058d6ad242dfac09e3cb5761187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d945651ebd3b675d8da62d9453368cde0b9971188464fa22128ed3a1f97541`

```dockerfile
```

-	Layers:
	-	`sha256:a0ff667a3c9fef8a976faf926acd08ff8b08c463b3f57bf20b6c023f0c4ff912`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fbbb74dd07ddfdd05613f82377f4cc516f3ca8a0685a9b6e72e25483b2ab75`  
		Last Modified: Tue, 03 Feb 2026 02:25:25 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:7cede414604a852698793ffc3d0e18450ffe25d21b183ab8e03fb4c3e9510bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c27a640c654e1de61c37d4f50753c446235e07c11066c38de9fdae9738da87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:18:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:51 GMT
USER memcache
# Tue, 03 Feb 2026 02:18:51 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:18:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0305606679ee5602dfe83ebed08d8a95725ae2f28239d2a3925cec06b53a08`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bcb2c024812c654ccf7f2a1fb6856e9bbe75288a013549e525c96410dd7be`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 147.5 KB (147530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c215e3c2397058a9b322ffcdc20ad77198f781e8976e7b1a04078531236d04`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.2 MB (2223637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b1c587a07abb5ae60d31224f6000a9cfc287afe2bc04f18ddab685060f433`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd47b97bf4131e574d4e5352abaeda7fafad68b021b454a19487a2cdfa2be4a`  
		Last Modified: Tue, 03 Feb 2026 02:18:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b5cbd65674c9b9f5c08723e1c34f2b954a8701c29473dbb9253f990c1494a552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de05ec6f371455ad3dcfa593db7db5830b4f27028cd5d6f283cc70db23fd97e`

```dockerfile
```

-	Layers:
	-	`sha256:1ad3c1c7030c06b1b980a395eacf38e9c41f938511607d218fe53d263819c4c3`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9678501224bae68522b858279d6e17cee23d5fa5b87d666dab7b1d8173fdfcaf`  
		Last Modified: Tue, 03 Feb 2026 02:18:58 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
