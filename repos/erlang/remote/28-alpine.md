## `erlang:28-alpine`

```console
$ docker pull erlang@sha256:889026431ec9cd41dbe2012ec58ea2d6d76bc00c7fb659067c43b9ffbfb6ec77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `erlang:28-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:20b0a2e2ef9a729e433f95a8b5d7c9463ae7b3ed89b5c17c1b8706a715ff1e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55676287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b219b9f174aff8feef6c96d1e338c8b5c7a2a8d848815c1a29a21e6e8fa5464`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:25:30 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:25:30 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:25:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:25:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2a71b1ed640a3d68d11f025b353d2f7dc7523d758bfc60e4583812878faab8`  
		Last Modified: Thu, 27 Nov 2025 00:25:56 GMT  
		Size: 51.9 MB (51873835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:31c110600fda7687b2ffd1ab0414d722830cd27b783f09275d2b483b8000272f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 KB (294264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1baf927c754765a07524c8228f8c1584488cac2d5bafd66097cefa1cf249ca3`

```dockerfile
```

-	Layers:
	-	`sha256:55a5a2d1d933ec32bacb9eef32ec48a60fd4eca60e6bafb6294422f6432f3ed5`  
		Last Modified: Thu, 27 Nov 2025 02:50:13 GMT  
		Size: 278.9 KB (278897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833b5cf1b5004a4661e69aeb8c6e4523cb5b4a01256f29a68e645a1ff40912e1`  
		Last Modified: Thu, 27 Nov 2025 02:50:14 GMT  
		Size: 15.4 KB (15367 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:61e59a0549872a82f7aae5391e598fdba5ae09c9d162b0a125caa43f8f91347f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52632359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc918a1c380a0a3500300a5a2b0c74ee299c89fed5e42e34e9035c97e97c239`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:28:29 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:28:29 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:28:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:28:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b9715f9f6d9db74ab5b3866d1f367123417a172fc60112cb41f0495e74bae9`  
		Last Modified: Thu, 27 Nov 2025 00:29:05 GMT  
		Size: 49.4 MB (49410804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:48401719d9eed60c16238d3443e838a0dd9e62ef247d77bedb5a3f3d755dcb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 KB (293140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e0a0f2dfd1b4ab4655dc6323404e4b4a78d08b2245a9c35d6a621d07349474`

```dockerfile
```

-	Layers:
	-	`sha256:c9228eeaf362e3c2f68b3fb99718076d10e18c8bb7c23e2c30eead984132e491`  
		Last Modified: Thu, 27 Nov 2025 02:50:17 GMT  
		Size: 277.7 KB (277685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f48f5a366f2cd474f6a5f1bf2fc004b1c1d3c92d19bd1e1d4d36d73e929c16d`  
		Last Modified: Thu, 27 Nov 2025 02:50:18 GMT  
		Size: 15.5 KB (15455 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:9c20a122ae0c21b41a7f08c771a52c7c28783c770219a66d06f61136978ec178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55774407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0b6e0588bfb3595a4d95c344c3cadfcdc9d4e763837e9878fd1bec067852b1`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:26:02 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:02 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:26:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:26:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fad7d01c12e42294b40d686ce38a81e83f0e4d4c83e03745731d7d84b6e7364`  
		Last Modified: Thu, 27 Nov 2025 00:26:23 GMT  
		Size: 51.6 MB (51636338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:37113b521bb9a135be98f4a67d2fa17d67dbff35b032b4c75a1d5a168453aee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 KB (295182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d700297c2dae8bc7c13b525db2128c1bec623e96e8ee04406b759ecea43e84`

```dockerfile
```

-	Layers:
	-	`sha256:2e3dd8e832d911fb79abe126183dac72738f5bab294afb58fb3d192a9cbf07b4`  
		Last Modified: Thu, 27 Nov 2025 02:50:21 GMT  
		Size: 279.7 KB (279699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09e70be90df464ad37ef42d6ccb434ec46e4e0e590cf2a917af505f6e732aec`  
		Last Modified: Thu, 27 Nov 2025 02:50:22 GMT  
		Size: 15.5 KB (15483 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; 386

```console
$ docker pull erlang@sha256:c3e262164531a799edea82c33f386b465c130f0ff5c80de15ff037f7fac5508e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53962581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af05d3effa8bd711faa47fed2a07ecab0a4961909dfa2f63b294363d2275990`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:27:15 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:15 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:27:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:27:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42996bdd7041ec9780c322fa4fb94d57a4c48f7e893f97913fcd004554802cc9`  
		Last Modified: Thu, 27 Nov 2025 00:27:36 GMT  
		Size: 50.3 MB (50343650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:94acc5cefb0934226dcb61a56b733117ebe725e92f586d1e9c9c1aade2a90146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 KB (289217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1eb27dd9f4ddc4fd5be06c6506d5b47464dbaabce239225930deb86f930aed`

```dockerfile
```

-	Layers:
	-	`sha256:0d3c80fadc06f3264e7dbd6487e45d37b67853ce0dc9388bc7df0630650733ff`  
		Last Modified: Thu, 27 Nov 2025 02:50:26 GMT  
		Size: 273.9 KB (273887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac61b95a7ae198feaac763590f940f772a7ba43c85b46393059f3a2043d40a6`  
		Last Modified: Thu, 27 Nov 2025 02:50:27 GMT  
		Size: 15.3 KB (15330 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:533d6fec7d1b4a48c65bb6c3accff08274ae998711b19c7928ce4f1cefc63e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54165229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9fd2fbed11158f63980b53a4025c33bf6aaad84c6bde772327bf83b0adadc5`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:31:05 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:31:05 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:31:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:31:05 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de2f0a0a0949a134b5a8ea28a75ffe47b0b02d7a6d11084c1b5c53e90df3b99`  
		Last Modified: Thu, 27 Nov 2025 00:31:53 GMT  
		Size: 50.4 MB (50432988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:ba8abf9805e20af7fda5b51735bba4811d9857a31f0be4fa7b69a82b4474b185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 KB (288157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e63cb11b66f891ed090bd07365a8d7b4495bbe9e99bf5447e449719bd560487`

```dockerfile
```

-	Layers:
	-	`sha256:446df8ffaa65142031dc8e57cf1cc7138609f5045c8f945a219d38bd2bfbf373`  
		Last Modified: Thu, 27 Nov 2025 02:50:30 GMT  
		Size: 272.7 KB (272740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5509f365b9db90d472bd53eaa03eaeda02f730f16a9c65b94ff42223f8a978af`  
		Last Modified: Thu, 27 Nov 2025 02:50:31 GMT  
		Size: 15.4 KB (15417 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:0a1be327e45eb592163c999b170cc1bcd1dba4d80874d874f77e9cdb3ea75d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53812185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b8fe6cb754ff6cc5bb0f47842bd3d2c41359d5aa6c75bca15097515fda5ee3`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:27:08 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:08 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:27:08 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:27:08 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a044533f24735f0e407c63061b042ac1dc713e461dc8ccb0dd478b542d0bda9`  
		Last Modified: Thu, 27 Nov 2025 00:28:08 GMT  
		Size: 50.2 MB (50162941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b96694092f9cc6308febb234a5d847ca74a40041c3d03ea2565dcb14e1b6aabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47e594ede8737c81ffb2945017ec3fbabd2922534ed081d49ddfe940b51594a`

```dockerfile
```

-	Layers:
	-	`sha256:6e5236db7b5306955f6a0c9e5ec384314290fef127baf3bc189dd567ce937be8`  
		Last Modified: Thu, 27 Nov 2025 02:50:34 GMT  
		Size: 272.7 KB (272700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59859bc8fba468fc16354bf7c972b7c1bdbfb3d84302eac6a871eb8cfdcf4144`  
		Last Modified: Thu, 27 Nov 2025 02:50:35 GMT  
		Size: 15.4 KB (15367 bytes)  
		MIME: application/vnd.in-toto+json
