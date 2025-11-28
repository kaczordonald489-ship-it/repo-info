## `erlang:27-alpine`

```console
$ docker pull erlang@sha256:adfc5804e3f7f1bdbe5ea1671926c660f6932799564ca162b6a18c8b3d1d84d0
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

### `erlang:27-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:0418eda7935efadeeb6ec90d03307074b6931912cc9faf25c96681cf7ebba179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53647656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e36bfe5c2c26c507536d8894be8107693f6447f2a430e109253b204cead5a8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:26:38 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:38 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:26:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:26:38 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eddd6d7f0e5a761734d288ff5ef5641330f3afc88fee3ce992b8ba849ee433`  
		Last Modified: Thu, 27 Nov 2025 00:26:56 GMT  
		Size: 49.8 MB (49845204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:094a19bd644dc9337a0aac4713c38eb953130fe787fc86117b93acc7933f7f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 KB (293805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0324190a7429fea05fcdec1699c582e8f03f7dad0394d5489bd027de857437`

```dockerfile
```

-	Layers:
	-	`sha256:c369e12450052220962732cdb48d8bb67cad261a89ae0c112732ac166f7695fe`  
		Last Modified: Thu, 27 Nov 2025 02:48:43 GMT  
		Size: 278.7 KB (278729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72db1da8a8a2ee0fec9d7465ca79d7bb4ffa42d8f6c551fb5d0cdde5af92417`  
		Last Modified: Thu, 27 Nov 2025 02:48:43 GMT  
		Size: 15.1 KB (15076 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1ecb92306c73bfabcee1268f910a54df2727202f26261cee6ddde573692dd301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50587729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a85144f4d0113e4dcb35c66b57fad1f646aeeaef4d0344384989fe579d8a74b`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:28:05 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:28:05 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:28:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:28:05 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acec1230ea548ad41736effb640f46cdaf29fac22fbec419099a732855ebc605`  
		Last Modified: Thu, 27 Nov 2025 00:28:33 GMT  
		Size: 47.4 MB (47366174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:e9cf18adbc75cf9acedfbe470ddb4aeef936fbf7a77987f0266b8e1fee5b9d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 KB (289678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba4fc6f2682c44813b516bbf987f63a31f6be52239712f1da81fec4e40130c3`

```dockerfile
```

-	Layers:
	-	`sha256:1dd6350f3b6c68e2192b36d74b12fe2ec36b7ebf8ff709cedc1ea80097be5a18`  
		Last Modified: Thu, 27 Nov 2025 02:48:47 GMT  
		Size: 274.5 KB (274521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79a2897e9d795da24cba877e33320292ef37cdd3561074bdde8eda63354f9b7`  
		Last Modified: Thu, 27 Nov 2025 02:48:48 GMT  
		Size: 15.2 KB (15157 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:9bf45cb71a0237a2f96b1d27837bbb3690b0ac82d19a26932c5f450fc73d0ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53767824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d35c3c52bd737b2fdb4710f22f52407959acc97a8666863c9cadf204a34ff1e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:26:19 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:19 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:26:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:26:19 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495ae8d64fffe24632db7b687bff11f34613dca0e033488b78f01a1264ed95a9`  
		Last Modified: Thu, 27 Nov 2025 00:26:42 GMT  
		Size: 49.6 MB (49629755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:49b85fdeeecaa90a570e876514819b0acac386f940aa4b67e9b3b574bd73a89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 KB (294701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2168114177e9f31998fb243e6f1f35dfb2c09d99e3f0733ff8b119415d2d23`

```dockerfile
```

-	Layers:
	-	`sha256:be42ef76b677d6449f26b8e60ff76af79599d1a3d41eb4d3bf0c64b7695e2c45`  
		Last Modified: Thu, 27 Nov 2025 02:48:51 GMT  
		Size: 279.5 KB (279521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2820e836b945be479c50e5e4c78bbadd75dad169315b64d06bdb639437b46b8`  
		Last Modified: Thu, 27 Nov 2025 02:48:52 GMT  
		Size: 15.2 KB (15180 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; 386

```console
$ docker pull erlang@sha256:57469c773d561fe390ba11939f09535ce231d9cac4f62806538be753651a7000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd75d6391da5234f87f447318e4ca07a7609509abfb201fdacc92b43639156`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:27:21 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:21 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:27:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:27:21 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ede6b30babfb2b7d8415457bafc6436b7f24587b887ab2eeb80e0c2a0c2b2c8`  
		Last Modified: Thu, 27 Nov 2025 00:27:38 GMT  
		Size: 48.3 MB (48287367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:60feb26bcf8edf7b63e7b92f25b5d4f48eaf57427270b93a1e2c430850bdddf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 KB (288768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94045dc08a464ee0d31f01edb91c8771d2f54ad47316a88efff9f969dbc77b1`

```dockerfile
```

-	Layers:
	-	`sha256:4b539a385f05852ddf65e08b55cbbc23bd76eb08e8e55c94bb46cb8d6274735f`  
		Last Modified: Thu, 27 Nov 2025 02:48:55 GMT  
		Size: 273.7 KB (273724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbb0b4b3bf3b6a4ec977a3039ecf89ec5852af898cbfafe34f7352233829e64`  
		Last Modified: Thu, 27 Nov 2025 02:48:56 GMT  
		Size: 15.0 KB (15044 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:272308994273a1a3c862a02c9ca32909ca90d448d353e6d2b4189c375d334918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52126700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbef1534f5b98d7a955d0485454bc6d87016d3b3bb9b8558e9bd65f5f6aab02`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:38:50 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:38:50 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:38:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:38:50 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff902406bcf14ecb5d10a1caddeb2be8bbb7275f03e5e17f8c27ca6e996d5f4d`  
		Last Modified: Thu, 27 Nov 2025 00:39:22 GMT  
		Size: 48.4 MB (48394459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a1ab01e34dbd0f403f67c1e5e42345b1019613ab172da30e93045cf2f9f728fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 KB (287689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db401a7196ff2629268e2e6ec127f694b86f817afb706cb6fb52e2d5b6377463`

```dockerfile
```

-	Layers:
	-	`sha256:9fbadc1ade2b1dc31fc0510279e46ddcbd53c54b00f7e1d48924f53115aa8c4f`  
		Last Modified: Thu, 27 Nov 2025 02:48:59 GMT  
		Size: 272.6 KB (272568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007dd583059bbe6f0eaba49346fcd26ce44188e37d03c1157abc26d27002e991`  
		Last Modified: Thu, 27 Nov 2025 02:49:00 GMT  
		Size: 15.1 KB (15121 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:483547d32fbd26dd41a48b556596ceb0b50e63ec81242cd41edd52f52e01ba78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51706140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd897f88e3160491212a0bcb281a592fb6498e8ee19aebe191b522f202501a0`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 27 Nov 2025 00:32:11 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:32:11 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:32:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 27 Nov 2025 00:32:11 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bee08ca85dfe143f30037d4a1d9b86b70316c42e451b018548d461cf34dcda0`  
		Last Modified: Thu, 27 Nov 2025 00:32:39 GMT  
		Size: 48.1 MB (48056896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:bd2be55a861d1b2ff6b53d57d508c92a2640535823a4dedbcc5547a690c5d7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 KB (287610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3d73a3e69c927fc19b3dcfeee34508d7fbedaf48da7dc85deacea3d981ed4f`

```dockerfile
```

-	Layers:
	-	`sha256:7c3be212064a2c036cdcc3118fc3463df3c7417aae0722930a3ca1cd54d0c29e`  
		Last Modified: Thu, 27 Nov 2025 02:49:04 GMT  
		Size: 272.5 KB (272534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2c0e39800aa1091b2ffbbdf36ec0a384fccc23aa9faa42232503acaeb70467`  
		Last Modified: Thu, 27 Nov 2025 02:49:04 GMT  
		Size: 15.1 KB (15076 bytes)  
		MIME: application/vnd.in-toto+json
