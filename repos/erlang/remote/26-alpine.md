## `erlang:26-alpine`

```console
$ docker pull erlang@sha256:3aa46eee6749cf1d549bfd652585871932ac072118f864f359da203c5942c3b2
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

### `erlang:26-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:9f7f0d373879dd09eb141c5e1a16e18cf9ce4cfc9f1cc6df25b25cedebcd7611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49720506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03454713ea2b50d9678a18ea9228a5a80ca9981fc1ca5cf3171549b320df8c1f`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8f169f33f2973abf731cf2ba2ea73440d7063c26bc1dbdf9c37b49cf04f33a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a6b58c200bca9f95a7cb4b6fcfc0494ac7aca7c4c9379d25869c5234b131cf`

```dockerfile
```

-	Layers:
	-	`sha256:2731b46fbf3f6deed6819bc2279967b80043a1debd9cdebd952bb62450079dfb`  
		Last Modified: Wed, 28 Jan 2026 03:19:59 GMT  
		Size: 273.4 KB (273365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41390f6112b5881a56e5a44bda948da060e69c8740847169ddbca11ff99f9a5`  
		Last Modified: Wed, 28 Jan 2026 03:19:59 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:948ee844dcdc966f53266ea180ab819c9c5938fead08bf607cc0f5f74f1b9c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46850504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b2c815e31a0a9e6da07aa7a7d38a7272534b916a3aed2abf363fee62ecb4ff`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:4a4e1177c1d1c09e5640c79b4571a908d91dbfd3c96ac6e2520a5efa9af3110e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 KB (284169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825bc07708a2a143696388fa251fb9a2ef8aa67ea53cd09a8ddfd5571971abae`

```dockerfile
```

-	Layers:
	-	`sha256:0e4fd6833acfeff056043161b2841d25f654d121ec902f030d4b59a4367edee7`  
		Last Modified: Wed, 28 Jan 2026 03:00:44 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2350c7b18d2af69aa5765eac7b256a5aaae7e4cb18c553e90080dddc96c4dd5`  
		Last Modified: Wed, 28 Jan 2026 03:00:55 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:9b6acf257d6e36630367b28e0ce13d9f64e670f3f1a6807e41e2c3c078f70889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49969366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927906ba128de8ab10678ce40b2e977f62f79e7d371635ee8fa2a143088fb4be`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:bbe5be0b7390e49f4da390fb246560986bb71c810a4e5ea1ade7335782d66094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 KB (289265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422b83ae8e14f2aa412d5afb3370d27cf7ba89b8cff845df813103d8a28132a7`

```dockerfile
```

-	Layers:
	-	`sha256:e4a5daa1ae2dff60fb081818a5b256697e37d35f2db2b4a12768e120c095c0e7`  
		Last Modified: Wed, 28 Jan 2026 03:07:48 GMT  
		Size: 274.2 KB (274158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f11de2180c877c163fa1af40120bc4e75477c6271cb8fbfe291da5acc1e72b`  
		Last Modified: Wed, 28 Jan 2026 03:07:48 GMT  
		Size: 15.1 KB (15107 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; 386

```console
$ docker pull erlang@sha256:d85f44b5416b8f8b692a48916b3d0959a7576934892c19a65469833e6296d7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48157036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7e91f913c1b6db30eab1c86d43cbb057167dcc63018969344ef5199855cf49`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1bd17b261e7c55f06ecb15f0d0fc68b0f2fabb6fc4359c83caca1a382a7df9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 KB (283259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4839eef418dae585ef44d42a741d27bb8408ad3c7b5eec256562205d7914a545`

```dockerfile
```

-	Layers:
	-	`sha256:2362b9b90d76b113304e56322bda15269d327303e862c8fd69e7930add714cd4`  
		Last Modified: Wed, 28 Jan 2026 02:36:17 GMT  
		Size: 268.3 KB (268288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe83500ff871f340fa877aec5891571bb98469e1c9bebc504fa466e526bcb31`  
		Last Modified: Wed, 28 Jan 2026 02:36:17 GMT  
		Size: 15.0 KB (14971 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:e95c92c6f925524c58d620d6bc73b25e46d3e497a02ad29a32e1ffa1c54ec731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48317495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c108d9ee06e129ab438569c8d2ae9460ad311b54482e28ffd101062e487f43`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:115215887b6fec92743e7b48031a5a404f8bd1e9d3cd67a0226d3cb738a54d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6f3b7d0d000bd46973a1ff215ac2ad7be53a2abaf1d0410bd4e0b8aa2260d5`

```dockerfile
```

-	Layers:
	-	`sha256:470f2207687d248f631bdd165ed7fdd7114869d8fa02a6dc717b60799b402bb6`  
		Last Modified: Wed, 28 Jan 2026 04:11:07 GMT  
		Size: 267.1 KB (267133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30a90fb6184a7b2b1071f47d40d65a5eea735c0a097b48c7740a760f50d1662`  
		Last Modified: Wed, 28 Jan 2026 04:11:07 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:bf583fe1e074acb73d90a59470a55bcbfebd91a01521f29765098cabb20cbd7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47860928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b8ce2637a2c26073c141930178b1f6f20b2add7403b206b723a20ad8f93ce2`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:e51dafdb04da3a5bb258adf5b7d1c64df8d828b9b12351d001d7059db46fd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77714a572f7ab8feb5844ed6afa88248e3f42b64e2683a10364f4fbbff7780bf`

```dockerfile
```

-	Layers:
	-	`sha256:70c91668c4ddacefd6e447f77281684817e0441faee513ec231eabc7a250fc6c`  
		Last Modified: Wed, 28 Jan 2026 03:12:21 GMT  
		Size: 267.1 KB (267099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a53464ff439354934620c626afd92ee864f3f9375e7e9d7cf6103bd281e6b42`  
		Last Modified: Wed, 28 Jan 2026 03:12:21 GMT  
		Size: 15.0 KB (15002 bytes)  
		MIME: application/vnd.in-toto+json
