## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:a92591a27182bb3207fc5770c5480107f13b2978ac5599248c3f228057f7e7d1
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

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:d5cdc02214a9d584142ae955cce1de4d26dd52402a1f6aea5f4417640801e597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15714071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f8ddc30bffdcd5a3b812e2314d280e3cdc2776d458680df95124fb2bb0f162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:37:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:37:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:38:22 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:38:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:38:22 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:38:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:38:22 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:38:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:38:22 GMT
USER haproxy
# Fri, 21 Nov 2025 23:38:22 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:38:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f517ed363bf570f4926b55f24538c21de3cf9abfe669c49e3425f6b5c58f28e`  
		Last Modified: Fri, 21 Nov 2025 23:38:38 GMT  
		Size: 819.7 KB (819679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fc7f162425a49c5dc05133edd8be61108dcf44b973ed304227c9ca77a630cd`  
		Last Modified: Fri, 21 Nov 2025 23:38:38 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d164b0176441bf0384f45854db4f411b8318d9d3ac8c63d0e93e86b56b7566`  
		Last Modified: Fri, 21 Nov 2025 23:38:39 GMT  
		Size: 11.1 MB (11090503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ac92c38c208e3bfa263b716e2df151abdaad8ead610c7f38c254113ed20882`  
		Last Modified: Fri, 21 Nov 2025 23:38:38 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:0d221c9907f45afde4f019f64c53930605b2fca55b19b71d1bc7ac046cc5d891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 KB (248999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5d02cd3ab8e6579a344e1ae3bc7480a1477a7c920e7897a833a4469358564c`

```dockerfile
```

-	Layers:
	-	`sha256:6147aa4d112d6a9a5d12d36a4612f20184e3c16f7777ea273d7f1b2947b8d49f`  
		Last Modified: Sat, 22 Nov 2025 01:56:47 GMT  
		Size: 227.9 KB (227943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0cf5d987d883253f9f10d2c037cdd24b9eeb8d54094bbdf9fec7bc4b64fca96`  
		Last Modified: Sat, 22 Nov 2025 01:56:47 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ca2ed1ae3f67138ee1bf1d7bce3250f6e377478a44fd4cd386b8aa685fde4035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15497515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c0fcc6191297e19f4e2657884fc12f33d14c9b6a6e5688efa419a1a07c85e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:39:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:39:15 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:39:49 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:39:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:39:49 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:39:49 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:39:49 GMT
USER haproxy
# Fri, 21 Nov 2025 23:39:49 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:39:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63401109de2a0aa84e79a8e9c305aad28d80defeee8a8885361668b9023b998b`  
		Last Modified: Fri, 21 Nov 2025 23:40:00 GMT  
		Size: 812.3 KB (812256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c30d57d1998968f13dbef071704bc357def248c4021abdad442c7bb110d57b`  
		Last Modified: Fri, 21 Nov 2025 23:40:00 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356e25cd6ac0d53f10ae7193752872f1c13ce8b3c6550492d4d5989ca43b1664`  
		Last Modified: Fri, 21 Nov 2025 23:40:01 GMT  
		Size: 11.2 MB (11179742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb9d0c8c45817b1126767b7323a6339dcee48f41935243286a2044b8e2b32ba`  
		Last Modified: Fri, 21 Nov 2025 23:40:00 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:705769677b0e54a036562ae1be7320b20bd99a864ac83a0b0d75d1cf35082347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92d8f139713e19006b3877ddd8efc37a9e0dbf8f2215ee9588632cbd13f5b75`

```dockerfile
```

-	Layers:
	-	`sha256:05d924182e4d2f35a7d96ca470f68acfb3eb73a822fa8a8e63448bd299bb507a`  
		Last Modified: Sat, 22 Nov 2025 01:56:54 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:6e3f91404279406f932e95c49734454d256a1a41cc8ff26653c0b19e0242c1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14997363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95aaade3b9d1a62d20becd25684458176315c4af480f9670d8890a66ac2d9a40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:39:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:39:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:40:10 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:40:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:40:10 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:40:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:40:10 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:40:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:40:10 GMT
USER haproxy
# Fri, 21 Nov 2025 23:40:10 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:40:10 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2e6b8463240bc1f98e0e3cedfce2d20bbb0e6e91edc23b9ffc11d218f10a9`  
		Last Modified: Fri, 21 Nov 2025 23:40:22 GMT  
		Size: 768.4 KB (768368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8008f86c97452eb0d09fd39b2c198a23725452e822498fe78c38850a3004ca`  
		Last Modified: Fri, 21 Nov 2025 23:40:21 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f685a70f67c311dcb87da27e01d22d0a5d924e10df25ee9f045e4050b57fa5d6`  
		Last Modified: Fri, 21 Nov 2025 23:40:22 GMT  
		Size: 11.0 MB (11005999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798e2e86f7c8a620a87822a5a50f4798875c702942f4eeeacb159f7c253c0eb`  
		Last Modified: Fri, 21 Nov 2025 23:40:21 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:0257a62eb97a2c8041a7974f5defe7cf15f26511b564cc5f9da1dadd5e82fad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 KB (249205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058cc8e1b7e7e06372a8b9862ea7063433d796a8061e9883be0d8ee8598c1670`

```dockerfile
```

-	Layers:
	-	`sha256:94b85ec21ef65ad17d420aeb624c7ce9ee7487838085ddfcacddf1f503b6a294`  
		Last Modified: Sat, 22 Nov 2025 01:56:53 GMT  
		Size: 228.0 KB (228011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd43b8e3d163604bd7f6794246ea0cfe9375c4b86882d3edf609b12b17fcce4a`  
		Last Modified: Sat, 22 Nov 2025 01:56:53 GMT  
		Size: 21.2 KB (21194 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:646d09aa104774e278b65314f341fd4843cd8d2f0e37c795eb958903c7310458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15996730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11744ce82057ec5a80fa69ae57de770df80528b97f010ba541455ece1c4e633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:37:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:37:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:38:17 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:38:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:38:17 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:38:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:38:17 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:38:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:38:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:38:17 GMT
USER haproxy
# Fri, 21 Nov 2025 23:38:17 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:38:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd6ca67ea027a11966e2de5e2dc3289e55ffa8f1822d068f40c88fdb601f536`  
		Last Modified: Fri, 21 Nov 2025 23:38:36 GMT  
		Size: 831.9 KB (831902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db2e69d5e36d8b3f4341a4fb54c40e4383404d09336700d2933019b1fe042e6`  
		Last Modified: Fri, 21 Nov 2025 23:38:36 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fe80c5056f34160f743a73a65debe248882be728aae6ead7be6ae1a31160b7`  
		Last Modified: Fri, 21 Nov 2025 23:38:37 GMT  
		Size: 11.0 MB (11025319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2b3fd94029e37a007298f7f8306ec6d770e2d6efe6653177e9ae9a5b6fd235`  
		Last Modified: Fri, 21 Nov 2025 23:38:36 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:9615f81c98e126154a0bd327e5c75cab943e248b99c7ea32052b98db02ad9025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 KB (249285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2daaae34b1a6e8ffd484ebf77ccfd6b393a67f389c3f26e8122b3f281587b5`

```dockerfile
```

-	Layers:
	-	`sha256:5f155e3e20bf448980e8921fac390873cef7991ef57c26bb86480c9eed49c3fa`  
		Last Modified: Sat, 22 Nov 2025 01:56:57 GMT  
		Size: 228.0 KB (228047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a70fa8dfc9a339bb56158ea79c5f6f78088d3851108b32ea175b989aaed10a`  
		Last Modified: Sat, 22 Nov 2025 01:56:57 GMT  
		Size: 21.2 KB (21238 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:824d57c52ee8216b7e5db639d9230dbecb21e8a64361ed053713b6a2cbef9ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15262559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7f62b9a9a8baddb664e6ec633e6928173b6c4db4ad1b275802966fdf2f276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:39:04 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:39:04 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:39:38 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:39:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:39:38 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:39:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:39:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:39:38 GMT
USER haproxy
# Fri, 21 Nov 2025 23:39:38 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:39:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6260fefc882a681d8ef0b47348c4a065d5791143a35688184c930978fe9547d0`  
		Last Modified: Fri, 21 Nov 2025 23:39:49 GMT  
		Size: 823.0 KB (823033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4dd22e084a0c8d5669c928e3f6993cd07f5c1939e2fbb28668896411aabef0`  
		Last Modified: Fri, 21 Nov 2025 23:39:49 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a755d153722480265e772037993de706fa9b0bff2f3e5a6591421ff61bf68`  
		Last Modified: Fri, 21 Nov 2025 23:39:50 GMT  
		Size: 10.8 MB (10819158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2664896c285114af531cdf6d44f69bdecb72796377059ed8ec35502d7b0509`  
		Last Modified: Fri, 21 Nov 2025 23:39:49 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:07b3ef34de59932092151db7b690e0f9f28a6e197770f89a96ec6a74e4fb1653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 KB (248898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f0420f5280480bb5e1d63c9c42acd1a4ed0bffcbf78ab4e5eb4285fa8f9eab`

```dockerfile
```

-	Layers:
	-	`sha256:693f1301400c263fa728b69f89eb0d42c2d6e4b3d32b7e8fa69d38bdff8ab674`  
		Last Modified: Sat, 22 Nov 2025 01:57:00 GMT  
		Size: 227.9 KB (227898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb84c44e4362439eb5e56902a1b18ebb58a4103665f44f4633a6662504f41328`  
		Last Modified: Sat, 22 Nov 2025 01:57:00 GMT  
		Size: 21.0 KB (21000 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:d238cfefd1ef235ebd8d86e43fbbd2c44159a1a1a9923f9a2168015a784b7f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16294293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd43a8d6a0bb022edd8fdb316d12d756c0ad6ffd19d16f49087ef86b95db503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:37:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:37:04 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:39:50 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:39:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:39:50 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:39:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:39:50 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:39:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:39:51 GMT
USER haproxy
# Fri, 21 Nov 2025 23:39:51 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:39:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61edcb13477f9dcbc29795388d0124105821169c006be84c553da02feddf1bd6`  
		Last Modified: Fri, 21 Nov 2025 23:38:01 GMT  
		Size: 852.3 KB (852291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75c8701f55b6ca4fe78778873120c20dabb9cfd7fdac2ddf8ff2feff41f6522`  
		Last Modified: Fri, 21 Nov 2025 23:38:00 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e3a88b571f26b768129e810bb5e4a8a20c1b7a074c4a9fe13c7990d749e63d`  
		Last Modified: Fri, 21 Nov 2025 23:40:11 GMT  
		Size: 11.7 MB (11708320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c5a14a03eaef45e03e4cda3d5cc13527011a006444fba03ac77e7b4b6bcae6`  
		Last Modified: Fri, 21 Nov 2025 23:40:10 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:833dae5fcf0e369a096cbacb8f2e2314ac0d165e712faa7053dc9edc0e9e870b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4759ca9f2dfba25498dfbcd0baf01881b297698c6d989d8e00ea7fdffb104116`

```dockerfile
```

-	Layers:
	-	`sha256:eb020e7672e3679027082218d94811a26b289e882a9cd8f6e461987efb42f2d8`  
		Last Modified: Sat, 22 Nov 2025 01:57:04 GMT  
		Size: 226.1 KB (226050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106c3d50b1202cc57c0eceb96dafa3d6ff7ec15fe33fa82b7ba496f3cdaa8a6b`  
		Last Modified: Sat, 22 Nov 2025 01:57:04 GMT  
		Size: 21.1 KB (21128 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:3cd268e050bae421dbef79b615e44f520ce82b5ba0ed2d556f5ca9f5ac35c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15130367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f82be8f183d9c0d9aa55a71f10c7877c62749167de1ed14669ff9d714e8fc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 01:50:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 18 Nov 2025 01:50:19 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sun, 23 Nov 2025 00:23:12 GMT
ENV HAPROXY_VERSION=3.2.9
# Sun, 23 Nov 2025 00:23:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Sun, 23 Nov 2025 00:23:12 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Sun, 23 Nov 2025 00:23:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sun, 23 Nov 2025 00:23:12 GMT
STOPSIGNAL SIGUSR1
# Sun, 23 Nov 2025 00:23:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 23 Nov 2025 00:23:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 23 Nov 2025 00:23:12 GMT
USER haproxy
# Sun, 23 Nov 2025 00:23:13 GMT
WORKDIR /var/lib/haproxy
# Sun, 23 Nov 2025 00:23:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9253dc76a405a85955230fc525abebff2e71a420232ccafc2b7288d35027fc70`  
		Last Modified: Tue, 18 Nov 2025 02:04:34 GMT  
		Size: 837.7 KB (837706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45136c5edba2c9203b29cad2c3b64d6efcad596e92bb5367ffcad5eac6184eae`  
		Last Modified: Tue, 18 Nov 2025 02:04:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5656217962efe4f3e9c059d7062848f1d337dd3d58cae684579eca9422c26ea2`  
		Last Modified: Sun, 23 Nov 2025 00:24:47 GMT  
		Size: 10.8 MB (10775976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151198940309f087ba038954276c58d949134943d88e88de19364f3b47cf0d3`  
		Last Modified: Sun, 23 Nov 2025 00:24:46 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:68387829420d505ed8df0f1e6f2e91209915af9b295f6c5918509d07c57d4661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d536d00516d4512de53c32291e029d4531b9333e9e6d4dc67959a77ff9548534`

```dockerfile
```

-	Layers:
	-	`sha256:23f53bf8f65fbf979cdbddb38adb84133e70c4b889ae293e85583a01f0591fe8`  
		Last Modified: Sun, 23 Nov 2025 01:56:25 GMT  
		Size: 226.0 KB (226046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f47759fb7a13190dbf6beed86ec03d211e31c96d4e7e75fb41f61b7291c12fac`  
		Last Modified: Sun, 23 Nov 2025 01:56:26 GMT  
		Size: 21.1 KB (21127 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:db452f79053477deb9739704847ba7b28953ad772555f7ba24a8e7bada72a229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f23d696310985b89fda701baf180b3c24647401548b82452ba32ba18e7854ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:37:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:37:23 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:38:32 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:38:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:38:32 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:38:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:38:32 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:38:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:38:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:38:32 GMT
USER haproxy
# Fri, 21 Nov 2025 23:38:32 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:38:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fad067889b8f9f9b71bf379bda014acdf6c3c0d9852c452a8722f1eeb988cd8`  
		Last Modified: Fri, 21 Nov 2025 23:38:41 GMT  
		Size: 879.2 KB (879227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb7c4829a9ff2d7836da0abf945674fc0f97253b6711801e42f40806cb44046`  
		Last Modified: Fri, 21 Nov 2025 23:38:41 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cf5b486182f2968d27d150d321fab530131844dbd8f36931223d4084215e6b`  
		Last Modified: Fri, 21 Nov 2025 23:38:46 GMT  
		Size: 11.5 MB (11452811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f2032e0e08f670519d17900ea571843cbbbe8b3187b63edb55df48129ab868`  
		Last Modified: Fri, 21 Nov 2025 23:38:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:a4365aa9dbdae5b9cf9f567dd7537fffd35680fc4e288484e5bd840f128c1103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 KB (247047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c920fbaf506714daf21f82483a73288c47de6eacf8112900c5645e27fd8fb`

```dockerfile
```

-	Layers:
	-	`sha256:77545cdc8731edfa0c1c55ab2ed5aaa8183c1bd4c3b8d0d3a5c56c3c645ffd7d`  
		Last Modified: Sat, 22 Nov 2025 01:57:10 GMT  
		Size: 226.0 KB (225992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055bc95902a5356d2449c6a69f7926ba7955e68c2be7f3b3279785dbed6ec598`  
		Last Modified: Sat, 22 Nov 2025 01:57:11 GMT  
		Size: 21.1 KB (21055 bytes)  
		MIME: application/vnd.in-toto+json
