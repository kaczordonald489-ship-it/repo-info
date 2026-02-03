## `haproxy:lts-alpine3.23`

```console
$ docker pull haproxy@sha256:17cd651239b99d2481580814103d56f55307ddc1170300702efa0c1baf106fa4
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

### `haproxy:lts-alpine3.23` - linux; amd64

```console
$ docker pull haproxy@sha256:706bf381c8b61328a15aa1240afe5a5fe2697b764770baeddc3d16ad5b2e8d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17902871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9987bef7f7cb78cf277ae2438c61c8d45ef217f46d39cf5d8a38fe517e70711a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:38:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 29 Jan 2026 19:38:36 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:39:20 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:39:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:39:20 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:39:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:39:20 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:39:20 GMT
USER haproxy
# Thu, 29 Jan 2026 19:39:20 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:39:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b60c03198c0a879a0eda9077f6b4a684ff1b53307e1e7420b3e06596671e4c`  
		Last Modified: Thu, 29 Jan 2026 19:39:27 GMT  
		Size: 829.6 KB (829629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d8c61dbdd66979e21f5e7ce1b3ffd3d4d2d6ffb5fb5b7347cc92749c54de7b`  
		Last Modified: Thu, 29 Jan 2026 19:39:27 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e836c629eea60692d7d264d874db3abef6a40b002b7e3138a6636c872e685`  
		Last Modified: Thu, 29 Jan 2026 19:39:27 GMT  
		Size: 13.2 MB (13209982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b9234f68ee9e285e3db989f9138f9416c2db02a03f8cd6e756a30d1e82ada6`  
		Last Modified: Thu, 29 Jan 2026 19:39:27 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:9d8010d2b8484f9b4441a7d7cffdac3e7e7f36d45d5da3bf6105324318611997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 KB (248523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caad7e37d5d8b3a87a9e2893d5c30ebd1123b5a8083d74ed60976b93440bbf0a`

```dockerfile
```

-	Layers:
	-	`sha256:4725e88499b83e525434041bc09b3d5af7e95c657a5419a3bb67ef2766d4f838`  
		Last Modified: Thu, 29 Jan 2026 19:39:27 GMT  
		Size: 227.3 KB (227328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f432a2d0140aac8a7e07405d6372271c9fd949cac867a1539359e65e5aec86`  
		Last Modified: Thu, 29 Jan 2026 19:39:27 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.23` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:d63627b98e399380d5d0467ee09daf0e03eb3460978463d2ac8f746ff0439af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17773386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6252c5b37162e1fcc250b6dbdd808788a106547ec49c16885485f98f99e1f2e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:37:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 29 Jan 2026 19:37:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:38:27 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:38:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:38:27 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:38:27 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:38:27 GMT
USER haproxy
# Thu, 29 Jan 2026 19:38:27 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:38:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8307b3a73806b63abe51ceeb4c7016de8b92e7f944f55f8ace9a8078326c05a1`  
		Last Modified: Thu, 29 Jan 2026 19:38:33 GMT  
		Size: 821.8 KB (821837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10495c62a17347c05308faf088966541305b1df7165f58e32bf8ebbefa51f7bd`  
		Last Modified: Thu, 29 Jan 2026 19:38:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fbbb7aee8fbe118ba8bb613d8e128aeb47bab7443573ba6be3e2ac317e07b3`  
		Last Modified: Thu, 29 Jan 2026 19:38:33 GMT  
		Size: 13.4 MB (13380293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1afff57f233368106c940fb85572a7dbfd736545f4e3293ae95a0ed8491c5`  
		Last Modified: Thu, 29 Jan 2026 19:38:33 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:f47214c0f11829a9233ea338c8e1e64124dfb19e3f9f99dc7030bf08b3593ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3914c44707313a86d388a7507853a2921f6b551c63d034715ae48b97311fde`

```dockerfile
```

-	Layers:
	-	`sha256:386fbbb0018d9b4510f1a6694c950330370e1c6008d9f7322c877aefb2d1601a`  
		Last Modified: Thu, 29 Jan 2026 19:38:33 GMT  
		Size: 21.1 KB (21100 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.23` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:65e417858e8e1585afc5bc031951ff41ff6aebf56931e58b10191913320c576e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17254585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c04891fd876e245bd1759709e8fd2e855cfc3f37b72494377d42d45de656141`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:39:49 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 29 Jan 2026 19:39:49 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:40:31 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:40:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:40:31 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:40:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:40:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:40:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:40:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:40:31 GMT
USER haproxy
# Thu, 29 Jan 2026 19:40:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:40:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4638e5470233a9590ebb84069d1edf479db10077dac885c33eec1081b244a5`  
		Last Modified: Thu, 29 Jan 2026 19:40:37 GMT  
		Size: 777.7 KB (777718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9b8a1c62440f33a85618844283e8b2ba9761d9403aedae31390f1fe68c1182`  
		Last Modified: Thu, 29 Jan 2026 19:40:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb50e89e8f58ef0245c0960f8b1037b91ae5162df919edb14fa1cdd418c2fb9c`  
		Last Modified: Thu, 29 Jan 2026 19:40:37 GMT  
		Size: 13.2 MB (13193702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c12baf20cce147553bcd1664f064f730acacb269672652d6cd24bd8e61d857a`  
		Last Modified: Thu, 29 Jan 2026 19:40:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:95691883a8084d3a16adfc5aab62c55928d654b4f377225117a1aec8edf42617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (248047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf31071b2e8dc4b0bbb15c80775a7bc63079fe6ea347dc17480717dc229de9c`

```dockerfile
```

-	Layers:
	-	`sha256:abde070138f0bc7414535b680bd20afaa315b29cc3cce16e5083c51d1037daa4`  
		Last Modified: Thu, 29 Jan 2026 19:40:37 GMT  
		Size: 226.7 KB (226730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9103a5730c4fa87abf867fe7b768817379d671d142382211b937526e8736dda`  
		Last Modified: Thu, 29 Jan 2026 19:40:37 GMT  
		Size: 21.3 KB (21317 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:04f348907928cb1b01a131b48721018a231c034cf60a21328bab303987994375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18062989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f634273ed27180fa1cd702d35d3eadd7865ebfc423ab20b75dbd6fdac7fc83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:38:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 29 Jan 2026 19:38:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:39:07 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:39:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:39:07 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:39:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:39:07 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:39:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:39:07 GMT
USER haproxy
# Thu, 29 Jan 2026 19:39:07 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:39:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7124f63f179c0ef22759eff4310e956d08babc2f4d77f9ab3a0dd603de55b64`  
		Last Modified: Thu, 29 Jan 2026 19:39:13 GMT  
		Size: 842.4 KB (842397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e1ce92e54a6e27bc9e60c11d5d9f6970959d929238c6a58cb15de8df74078`  
		Last Modified: Thu, 29 Jan 2026 19:39:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f4ddb2144e806969d50f3bd1e2aa984add7f3f167e85290f491973fc7098ec`  
		Last Modified: Thu, 29 Jan 2026 19:39:14 GMT  
		Size: 13.0 MB (13022059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbf5d0bc7e3911f439591f674fe163707601fe845ff071a1ef8906e32ea0ccc`  
		Last Modified: Thu, 29 Jan 2026 19:39:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:b0a339d513f5f06cfecb98931b77045617166ff00785dc821366629f9d6bcc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 KB (248110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0129479c0e7b65e726509aeb8579b81665559dc15475fb30d703d7d41d077fba`

```dockerfile
```

-	Layers:
	-	`sha256:d4dfc59d41db07c01bc51af7db31ac30863eed129ded90f8c062a7593d143db0`  
		Last Modified: Thu, 29 Jan 2026 19:39:13 GMT  
		Size: 226.8 KB (226758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e4322a2cc4963d5dea4c36c7926d5f7c7e6e8bddf62e30d7aadc33585956ff`  
		Last Modified: Thu, 29 Jan 2026 19:39:13 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.23` - linux; 386

```console
$ docker pull haproxy@sha256:10339d03f732e29391323b315d93732761e891279d97376bc3cf2acd0af41049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17439991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a240a6bb49800b4c68041d5270aa21455202e0003853455be80deda502b02c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:38:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 29 Jan 2026 19:38:54 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:39:40 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:39:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:39:40 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:39:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:39:40 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:39:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:39:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:39:40 GMT
USER haproxy
# Thu, 29 Jan 2026 19:39:40 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:39:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f91d55821f6cef79bb99a398123c37e0538e550ac2dce425a697413920ef22`  
		Last Modified: Thu, 29 Jan 2026 19:39:46 GMT  
		Size: 835.9 KB (835921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e245b717ee9cfc0eff417e495344c73424c4852dbebc87528b34dfd71c9cce1d`  
		Last Modified: Thu, 29 Jan 2026 19:39:46 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c348c214d0b06c75eb6f5ed11fa220a0e7eaaf9e0e8d0a8a869f59bd2eb18a`  
		Last Modified: Thu, 29 Jan 2026 19:39:47 GMT  
		Size: 12.9 MB (12915639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9914a81d3177c86a7bfba0ac68373b9e8995fe54b540e72c1307273bd2dd137c`  
		Last Modified: Thu, 29 Jan 2026 19:39:46 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:bf1c01ac6d51482946bc5f4f6d9d17e5b22f19e654705f91c25971767bfed8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 KB (248440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c20645809c8fba143ea538508ca74674983e6fbd37958a19a4a5f8954ad84`

```dockerfile
```

-	Layers:
	-	`sha256:d8229662e5afb7f1ae95fe9ac12ed99cc1ec727d55b0bd7a3a921d858607a83c`  
		Last Modified: Thu, 29 Jan 2026 19:39:47 GMT  
		Size: 227.3 KB (227293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b601db76f0c9fb06ba952a66ad2e2780037dc0e79b9e7779b909abc8579b545`  
		Last Modified: Thu, 29 Jan 2026 19:39:46 GMT  
		Size: 21.1 KB (21147 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.23` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e10ec9d1ee45d7565ac997248a4fb11c21357077950c52130a820d0fc226778c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18652461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cb1e79b1172e7a5c8b26897c7a8db74599d552e6d5654041cb92f2bf81b7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:24:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 02:24:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:50:29 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:50:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:50:29 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:50:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:50:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:50:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:50:29 GMT
USER haproxy
# Thu, 29 Jan 2026 19:50:30 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:50:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d27b1e97f0948cf3686ea8cb6cc1957831c0a3170485b92dbc2786826d1165`  
		Last Modified: Wed, 28 Jan 2026 02:26:04 GMT  
		Size: 865.8 KB (865808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849dd5f71397d6ac7827ddcbf8b793602ef28580985776a08c455ab03f357cdb`  
		Last Modified: Wed, 28 Jan 2026 02:26:04 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b940288b64047383750531c4e5365c38c9d285d6a104099b8c1c123093cc8`  
		Last Modified: Thu, 29 Jan 2026 19:50:42 GMT  
		Size: 14.0 MB (13955568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35717e203551bf26bb516b2167d82ae6c7bb8ece77f3e8c3bdd54182a2072b`  
		Last Modified: Thu, 29 Jan 2026 19:50:42 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:60b294d634177e97f41b7a20e75315293d86845b73711a1bcd45f88664e37580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fbde46ec974d6b3cc4e197e4ca498f3ca9277c56313c8dcc5f2ebe444d31bf`

```dockerfile
```

-	Layers:
	-	`sha256:8c37793bd8601f51721afc050367e1dca293702260a07359e3b5fc8907a15e93`  
		Last Modified: Thu, 29 Jan 2026 19:50:41 GMT  
		Size: 226.7 KB (226723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2479a1ef2f6d0457c871b20d87ae918176090c099710c33cdbb5780a0e43fb`  
		Last Modified: Thu, 29 Jan 2026 19:50:41 GMT  
		Size: 21.3 KB (21254 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.23` - linux; riscv64

```console
$ docker pull haproxy@sha256:1c3c8a04f8756989368ab309ee1e1e7a8e112fa4ba911546084aa1382c3a6e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18651635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041011aa39daa5000827e226fdeb66f2e4d81932008cbbddbb7c206f257cdf83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:30:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 06:30:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 30 Jan 2026 19:23:11 GMT
ENV HAPROXY_VERSION=3.2.11
# Fri, 30 Jan 2026 19:23:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Fri, 30 Jan 2026 19:23:11 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Fri, 30 Jan 2026 19:23:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 30 Jan 2026 19:23:11 GMT
STOPSIGNAL SIGUSR1
# Fri, 30 Jan 2026 19:23:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 19:23:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jan 2026 19:23:11 GMT
USER haproxy
# Fri, 30 Jan 2026 19:23:11 GMT
WORKDIR /var/lib/haproxy
# Fri, 30 Jan 2026 19:23:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c9470919a79f39f2a2a1db9bf476647c20b35b6e97f36111db731eafdd6c58`  
		Last Modified: Wed, 28 Jan 2026 06:46:56 GMT  
		Size: 849.9 KB (849900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495b0565d23aaed2a0be6162e94f23c2de4ca298bc65512773f4fba68e98bf5d`  
		Last Modified: Wed, 28 Jan 2026 06:46:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8b83ca11b5c24919ca449944fd43a19ab4bde564053965370678fa36249f1d`  
		Last Modified: Fri, 30 Jan 2026 19:23:59 GMT  
		Size: 14.2 MB (14215006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafedf8b8560c17ed7e7de90e0fb8cf2fe782d0cfbc3f7cb180618da5d3456c0`  
		Last Modified: Fri, 30 Jan 2026 19:23:57 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:155b97f87a3f379c8f2ba6142f766126f40ce044f0a815623611cdd04c647dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb45a80f2febbbf2231a262e038ba9ce91e4a1ead1a524bc94b6cbe2002fb5b`

```dockerfile
```

-	Layers:
	-	`sha256:3f201c99e9a0a20d1aeb43f411c7d1c5adb7d51c9ef23db5ae0ed3be138d7fd8`  
		Last Modified: Fri, 30 Jan 2026 19:23:57 GMT  
		Size: 226.7 KB (226719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e89e4fd92406b98710be31189c87f068b27d825c35bc4561dfb9826eafcc68ff`  
		Last Modified: Fri, 30 Jan 2026 19:23:57 GMT  
		Size: 21.3 KB (21255 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.23` - linux; s390x

```console
$ docker pull haproxy@sha256:6bca637f7ee03f82f1072b726ba154e875215f767053f4f512f2e1772691da26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18154097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a58e46cc0c1fda2db79f4424ce2a8bc0bff4c85657bdd82e71d41501185fa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 02:16:23 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:38:16 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:38:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:38:16 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:38:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:38:16 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:38:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:38:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:38:16 GMT
USER haproxy
# Thu, 29 Jan 2026 19:38:16 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:38:16 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29bd43b91a413d34ea4bc82575783c555fca01eece6a8f965d200501492554`  
		Last Modified: Wed, 28 Jan 2026 02:17:25 GMT  
		Size: 891.5 KB (891540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2c82b5b859949825f0ffea88a725e08f8b3477411b2ef102d2fe8bb3a105fa`  
		Last Modified: Wed, 28 Jan 2026 02:17:25 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64d6b4e882140e96616cd593cd36fcc3a20d693aa70de38896490d5ea88786`  
		Last Modified: Thu, 29 Jan 2026 19:38:27 GMT  
		Size: 13.5 MB (13535788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247dad3b4f88d5411c1a746b6ba3fc8aeaa6ad1071537d534d066023b3be5a5`  
		Last Modified: Thu, 29 Jan 2026 19:38:27 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:fdd649e56d3540d4c71eaacbecac6066f43566c7de51cafcd1338b10518f955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e4a448e16dc70d8a83c9a238fbe1a2567234943731a09057061e9f3eb57ba2`

```dockerfile
```

-	Layers:
	-	`sha256:ebd7c5e3165c3c9c4c4ee7bd3a1356bb849cf89540f7531e373c86f5aafb5c27`  
		Last Modified: Thu, 29 Jan 2026 19:38:27 GMT  
		Size: 226.7 KB (226677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b20e9b2b1dd173aa46e2dcab060d44254630d247e349dd880675ed445de2c2`  
		Last Modified: Thu, 29 Jan 2026 19:38:27 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json
