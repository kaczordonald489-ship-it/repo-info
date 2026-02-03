## `elixir:otp-26-alpine`

```console
$ docker pull elixir@sha256:8871fc0b5ba7fc5f12e83753a33c02f615b2ef6361059760a3d584fc64e623f1
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

### `elixir:otp-26-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:8cb55d6bb4891a472489b44a1f89cda5293550c9f0c4ab78963543890686550c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57512821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5d307140eaf007718e8ead13ebe56d1ec5fe33fe855b9b2a6c249cb371299`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:19:52 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Wed, 28 Jan 2026 03:19:52 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Wed, 28 Jan 2026 03:19:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 28 Jan 2026 03:19:52 GMT
CMD ["erl"]
# Wed, 28 Jan 2026 04:59:43 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 28 Jan 2026 04:59:43 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 28 Jan 2026 04:59:43 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a6505de5601eea7315b0ed2bacd13bfd7cc2be23fe26834aaa58787ba7b605`  
		Last Modified: Wed, 28 Jan 2026 03:20:00 GMT  
		Size: 46.1 MB (46092642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91749f4b6c7b46840419ba3471b4e72021ce2c0b565182681b58e1462a255f1`  
		Last Modified: Wed, 28 Jan 2026 04:59:49 GMT  
		Size: 7.8 MB (7792315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:9350dc554de46ef4580c77f5e4bd2f2a6c9c1faffc1def9e3cd43a3a01b4b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 KB (289875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644e1dd3e36027d04e7e33fe832595e9039722cc7a36f8de3b90e0b1d232d2d5`

```dockerfile
```

-	Layers:
	-	`sha256:5bcf4945993da6eadb6dafb741e9a7bd38793195e29aa912d91c1686d96f4958`  
		Last Modified: Wed, 28 Jan 2026 04:59:49 GMT  
		Size: 280.4 KB (280389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5843f002952e42f626e05763d5eda5c3fe3ed121b8eb5cbc70e9df6a33a29f72`  
		Last Modified: Wed, 28 Jan 2026 04:59:49 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:6e3d6536fd5bf0cd1615359fd208e58aa0a8e42fe1f62389b5a013effbb541f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54642444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be0d9209a3fef4a18b3f405cd7656aa1b313429f9eb684c9ad5a07b33531410`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:51 GMT
ADD alpine-minirootfs-3.20.9-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:51 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:00:37 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Wed, 28 Jan 2026 03:00:37 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Wed, 28 Jan 2026 03:00:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 28 Jan 2026 03:00:37 GMT
CMD ["erl"]
# Wed, 28 Jan 2026 04:10:18 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 28 Jan 2026 04:10:18 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 28 Jan 2026 04:10:18 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0eecdfceac50ced18bf01b02cc208cce22bcbd8e601e53bca3de98531db8946b`  
		Last Modified: Wed, 28 Jan 2026 01:18:57 GMT  
		Size: 3.1 MB (3097225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fda5faa977347c9037735b83487045ee04349250ac01520b551f0d80fd45477`  
		Last Modified: Wed, 28 Jan 2026 03:00:56 GMT  
		Size: 43.8 MB (43753279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8380ccc994b7b3e1873f96df4b6e794cbdc71d9dff3a88d841a73e7d2dab25b8`  
		Last Modified: Wed, 28 Jan 2026 04:10:24 GMT  
		Size: 7.8 MB (7791940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:df62e4e7b47ada78f57e2b9903c140c0f994ce917478c1dce7ae73fc483f55b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 KB (285659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c68d935abaecc1a6f1c8e62492ada24d578f73932f4059192fc8c82ed1c92e`

```dockerfile
```

-	Layers:
	-	`sha256:8415594f1a53722d59113edda0c0a547295bde1384d95c702a83d4dc6c9057e4`  
		Last Modified: Wed, 28 Jan 2026 04:10:24 GMT  
		Size: 276.1 KB (276102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d2b07052679b42e04957a924fa7a9e15b5939e7c23357ac8bfe6be620141d9`  
		Last Modified: Wed, 28 Jan 2026 04:10:24 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:3ff150068f58c921b6f436b1190eb07ccc2302bb02c6d2fa7a84b41065d32abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57761687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f914e41d87d8723898a0bd0857fbe395dd429a14b59d5fefea79e79f3f02dbb0`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:07:40 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Wed, 28 Jan 2026 03:07:40 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Wed, 28 Jan 2026 03:07:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 28 Jan 2026 03:07:40 GMT
CMD ["erl"]
# Wed, 28 Jan 2026 04:47:35 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 28 Jan 2026 04:47:35 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 28 Jan 2026 04:47:35 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0665a99642f968aab934bb96e39b6c0c21c44b5c9309fb7358d95758463058`  
		Last Modified: Wed, 28 Jan 2026 03:07:49 GMT  
		Size: 45.9 MB (45879408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8315acda8c0292d2dee2a5c417f2d6c577142f4ceef00932cbdd038d104679`  
		Last Modified: Wed, 28 Jan 2026 04:47:41 GMT  
		Size: 7.8 MB (7792321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:a6428c59889910581adc168163f3d79f0b79a38269206b663d316151953b4d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 KB (290747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5a881d446dd12fb5c0dbbb342acba28598ade6e1857f23c47ea2c882c7f`

```dockerfile
```

-	Layers:
	-	`sha256:75352a4f074b849c093a043c5b35e933b9fb357ac0984bca688bd5c9805e8bad`  
		Last Modified: Wed, 28 Jan 2026 04:47:41 GMT  
		Size: 281.2 KB (281170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7579d183997764f8334d3c67961a153e645a175b5ca1f39237f2df420345ad68`  
		Last Modified: Wed, 28 Jan 2026 04:47:41 GMT  
		Size: 9.6 KB (9577 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; 386

```console
$ docker pull elixir@sha256:3f08c82740e613e296abd973a3ea166dd26e699175e8c2dedc0dbf8d70ebbe55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55948940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201ccfe10377cf1c14a60450616b00d54e26eb3ed60d93d09edcf028a52c899c`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:19:04 GMT
ADD alpine-minirootfs-3.20.9-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:19:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:09 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Wed, 28 Jan 2026 02:36:09 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Wed, 28 Jan 2026 02:36:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:09 GMT
CMD ["erl"]
# Wed, 28 Jan 2026 03:54:00 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 28 Jan 2026 03:54:00 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:54:00 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:deafad5a9be5989c4df2fba946fa81d5f8f786fc89fbc6a1f294ce7e14e8aea3`  
		Last Modified: Wed, 28 Jan 2026 01:19:10 GMT  
		Size: 3.5 MB (3471744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695dffe7e5eb542fdd30869d0c7ec08478070cb1dbeed211aaeaf78d2ce35e81`  
		Last Modified: Wed, 28 Jan 2026 02:36:18 GMT  
		Size: 44.7 MB (44685292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4115ded1f80d6e55b7a02d299301796d21c6e860ac807977be55fdf196d45a`  
		Last Modified: Wed, 28 Jan 2026 03:54:06 GMT  
		Size: 7.8 MB (7791904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:905f6928bed87368be3e577da71d968d654c2a1ac6ccfd6070adf569984845c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 KB (284776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b565a167e0e74300fb087db1e23b9aa98feec68a190df4b76aef6117ed15c0bd`

```dockerfile
```

-	Layers:
	-	`sha256:ebeb502a44837d9cb484ffb3a8541375e1dd4ee5f814b71f03277237a17afb9f`  
		Last Modified: Wed, 28 Jan 2026 03:54:05 GMT  
		Size: 275.3 KB (275317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d663285563eec65e93f554e589544e8f76a362f22ff4d8d590a1c06f6b095245`  
		Last Modified: Wed, 28 Jan 2026 03:54:05 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:5811d01fa3b4b465af6ef1f64c03c8a6a87fa5cd7bf91fb0ca0bbdd59cc220e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56109375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5095d17c53be7e7bf7a52ddbc1cf2f43b2f9cf85066c6ddbed33f303641b563`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.20.9-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:10:53 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Wed, 28 Jan 2026 04:10:53 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Wed, 28 Jan 2026 04:10:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 28 Jan 2026 04:10:53 GMT
CMD ["erl"]
# Wed, 28 Jan 2026 06:49:06 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 28 Jan 2026 06:49:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 28 Jan 2026 06:49:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3990151ce2a342ec7b501891daf9b442e02873f6a48f096b1bb8bfb26bea6ff2`  
		Last Modified: Wed, 28 Jan 2026 01:18:27 GMT  
		Size: 3.6 MB (3577510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174489ec34a5ef07093e331a70af433621b5c6611a3ea516671d4050916b1aff`  
		Last Modified: Wed, 28 Jan 2026 04:11:09 GMT  
		Size: 44.7 MB (44739985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035418132414f21ddf643bb97c569c1cbf74df495021e38898a10ed5161007d1`  
		Last Modified: Wed, 28 Jan 2026 06:49:26 GMT  
		Size: 7.8 MB (7791880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ff30f17630996d95ee29de3ad58c52ed57708a7484c936e60fdaf599c228eed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 KB (283675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c025be489544a0f726fd9e3a8d0291a14d620576fcfc78369e605ddf500c8d7f`

```dockerfile
```

-	Layers:
	-	`sha256:f07cdc77889ea7f0d200bc35c4b0d1ba30fb6c3691329b85bbb8ceb974752f81`  
		Last Modified: Wed, 28 Jan 2026 06:49:25 GMT  
		Size: 274.2 KB (274151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6b128b209d808ba561352e64525a30f083fb63d6145a230d804221907ade8e`  
		Last Modified: Wed, 28 Jan 2026 06:49:25 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:4ecde98ea78c2e2b253adaa8967a74cb042530f20dae3f1c4f1542e6fd679a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55652725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54668a5c453e9f0ee3a75f1c777db2e5a9548617c5a69c895e4932b29a38adeb`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:34 GMT
ADD alpine-minirootfs-3.20.9-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:34 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:12:09 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Wed, 28 Jan 2026 03:12:09 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Wed, 28 Jan 2026 03:12:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 28 Jan 2026 03:12:09 GMT
CMD ["erl"]
# Wed, 28 Jan 2026 07:19:44 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 28 Jan 2026 07:19:44 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 28 Jan 2026 07:19:44 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:30120c90dcd290753d8c17676e1f51febd0a7eaee3d15ff1094eb027081d9dc0`  
		Last Modified: Wed, 28 Jan 2026 01:17:42 GMT  
		Size: 3.5 MB (3463654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ca1d03720d21cc2a32881936786704d3b6dcc89bd0c065f1ac2d0f20410549`  
		Last Modified: Wed, 28 Jan 2026 03:12:22 GMT  
		Size: 44.4 MB (44397274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23da2e639056d8e6329f15ce488c9eeb7722cc48035cb55cfb1322832c0ce5e`  
		Last Modified: Wed, 28 Jan 2026 07:19:53 GMT  
		Size: 7.8 MB (7791797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:6bdbb69fd075d574df260ab847e2ef0b2cbedf69eea2366904d40863feed0d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 KB (283608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cc8c37c517eee9e4710e591103de6b49079cb833f9ceb3d332475b62540652`

```dockerfile
```

-	Layers:
	-	`sha256:8b02155c9c14b872bfe7d1733aae80d7e27db1f933e1340291f48c4552969cdf`  
		Last Modified: Wed, 28 Jan 2026 07:19:53 GMT  
		Size: 274.1 KB (274123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:230b14b41f2bfea490940c72ec77d639dafdc2958145d4d0d9e70a58ee871475`  
		Last Modified: Wed, 28 Jan 2026 07:19:53 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.in-toto+json
