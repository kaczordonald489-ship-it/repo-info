## `elixir:otp-27-alpine`

```console
$ docker pull elixir@sha256:c4b71cdd0e84eaabc5b5e20f64d6b246575008b94fbc512ed27afd429e23fb88
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

### `elixir:otp-27-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:2873887c3e5b08fc9b1f92586b6abf80ade5341c1757a1bcff03103a32ffe3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61434131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae160bce23dba2e382e5a9a86f27701075130f19f5adbdb058b1be2cd92b535`
-	Default Command: `["iex"]`

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
# Thu, 27 Nov 2025 01:13:06 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 27 Nov 2025 01:13:06 GMT
CMD ["iex"]
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
	-	`sha256:abc3d5009819199c6f77df5ef5a3dd275eaf6af93123aab382ae912aab96a33a`  
		Last Modified: Thu, 27 Nov 2025 01:13:21 GMT  
		Size: 7.8 MB (7786475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:7b620ab31f23e30a19cd33b853940e84a1476341a0bb4cbaa212dde6bdbf1da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 KB (295240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0247d3ed93d2470b39d9b1f5ce497f049fe200e6586325d7f173673b0a5d30f`

```dockerfile
```

-	Layers:
	-	`sha256:ab483bc76dffa9f35400de59cb40623fc5299c20b1664138699c8e48c2500d81`  
		Last Modified: Thu, 27 Nov 2025 04:53:54 GMT  
		Size: 285.8 KB (285755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d843f1846e0ed494392ca028a46dff006e1c611a8f8fc8f3f4d982d3f452717`  
		Last Modified: Thu, 27 Nov 2025 04:53:54 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:6b8c1230d1cc9f49389ee949e10978145203d9d5fa0152b136f25da08ed2b2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58373554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7fa0405020bb13cf71fd40c561a3d117644dee6c988298c8c3d4225c495db6`
-	Default Command: `["iex"]`

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
# Thu, 27 Nov 2025 01:13:31 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:31 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 27 Nov 2025 01:13:31 GMT
CMD ["iex"]
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
	-	`sha256:863ba1ccac431eea1f495565ced2cd0f3f2d6137bff3572a081c76ea360f036f`  
		Last Modified: Thu, 27 Nov 2025 01:13:44 GMT  
		Size: 7.8 MB (7785825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:b882d397dc9be5f2f96453776362255e6c72b269889a908c38cb21e5dafff1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482350ba81e7f0c33c1a606bc604812b2bbd00ed487d45a485dc2a70f7f03e04`

```dockerfile
```

-	Layers:
	-	`sha256:7acac3726f912b26adb1693c0ed2fccdd6f808a60a1d93903df23a6581d50bfa`  
		Last Modified: Thu, 27 Nov 2025 04:53:58 GMT  
		Size: 281.5 KB (281539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4526d1661c3f6e9d74283c867342b268f6ce4202f847780a96f5e4918046ca3`  
		Last Modified: Thu, 27 Nov 2025 04:53:59 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:5b12528b2a0a2a88fa8721109aaa308cd5dc96916a57d45bafa3a324efc4aba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61554262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f312d303cbd792110a26c1cbf9eb652f89e200fbdcfa77127d7e38d9cc525920`
-	Default Command: `["iex"]`

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
# Thu, 27 Nov 2025 01:13:27 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:27 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 27 Nov 2025 01:13:27 GMT
CMD ["iex"]
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
	-	`sha256:87aeab122c2aff25ebb83ee7ab47c8acfcf74792749287881b26bb4f2d84dd2d`  
		Last Modified: Thu, 27 Nov 2025 01:13:40 GMT  
		Size: 7.8 MB (7786438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:65f26a906f058bec5009bea8bc7a91a8145846447e6bd399350128bc758bfcac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 KB (296112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14703790ff84eea3b6dc0763edbf8395fa69f16996a0ff2e1cb8bd2d3e7bca6d`

```dockerfile
```

-	Layers:
	-	`sha256:d332e40f7e40545f3e050ebd31d366935ba8a55b4c4ccd06edd1bba582287f77`  
		Last Modified: Thu, 27 Nov 2025 04:54:02 GMT  
		Size: 286.5 KB (286535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc7b96d1d3b94bde019f6046ad510a0f924dbcdf58d41f9d810e9ea348169d3`  
		Last Modified: Thu, 27 Nov 2025 04:54:03 GMT  
		Size: 9.6 KB (9577 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; 386

```console
$ docker pull elixir@sha256:38d1e0b2bf26d0d2d333e566a356dc6cdb5f6be591e1c5d02c6b6f8c1f499dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59692087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08faa67a02f5f576eb056fee8e1c5f0c52165643d7fb42bc5fce21ab449bea92`
-	Default Command: `["iex"]`

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
# Thu, 27 Nov 2025 01:17:07 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:17:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 27 Nov 2025 01:17:07 GMT
CMD ["iex"]
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
	-	`sha256:d98575f7d18b85321f1ae6454005cfe26448c097e347763075ce60b37b77ac49`  
		Last Modified: Thu, 27 Nov 2025 01:17:22 GMT  
		Size: 7.8 MB (7785789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:21b1e106647964585cb8ffb6d966c2579ed25ad8287c26205cc47b1e79a4ceb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 KB (290213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73147f0e4e18c791d43dd13ba23301583c00e228dff705c3487b38ec05496b1a`

```dockerfile
```

-	Layers:
	-	`sha256:6fbc616b91e0202ce503153cbe178ec384c7abd52c6a7abb1b4ae8809175cde6`  
		Last Modified: Thu, 27 Nov 2025 04:54:07 GMT  
		Size: 280.8 KB (280755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d525c8483b93546f1f04a676cc41033d7a3c51bada1127ebad07a11e79619c`  
		Last Modified: Thu, 27 Nov 2025 04:54:08 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:4ce1c9af8d4944063182b2ea8038ffb8f976ce8116c6dba95399c1faf6b3dba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59912544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358590d425a1014c22261fcb90361c4628752e41a2480881c8642bfed5e2a7b7`
-	Default Command: `["iex"]`

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
# Thu, 27 Nov 2025 01:23:24 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:23:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 27 Nov 2025 01:23:24 GMT
CMD ["iex"]
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
	-	`sha256:46381954e4aa6b1f6b48623dff279fe9a01efd27c963a4ef3fec7374984dfee9`  
		Last Modified: Thu, 27 Nov 2025 01:23:48 GMT  
		Size: 7.8 MB (7785844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:f11df24e80550d9547d4589cf1ec54607dd87bf7292a0569b2e2ac7a98fc655f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 KB (289111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d44f5a47043193e2ebab46853aabe3cbee50d69ec40bc3d8eeb5a70713755f`

```dockerfile
```

-	Layers:
	-	`sha256:09dbea272756886d504d2bdbd04d49594ae64014f6413e10b25713b265f2feb0`  
		Last Modified: Thu, 27 Nov 2025 04:54:11 GMT  
		Size: 279.6 KB (279588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:871f680bcbe938c440cbe108013b33d1b40553470fa5fc3af27460dc037246b8`  
		Last Modified: Thu, 27 Nov 2025 04:54:12 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:d94401e9d9658fd924d9783747a4acac65fa75516583ad8257c98fb02c1feefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59491865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828da5cd1c9e3ebc246a895b3bf18e447fcb2f0e5d328e0e24c526c8d0214657`
-	Default Command: `["iex"]`

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
# Thu, 27 Nov 2025 01:17:14 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:17:14 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 27 Nov 2025 01:17:14 GMT
CMD ["iex"]
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
	-	`sha256:ab672d08663b0646b95e55f97d329c8b6434cb8c5fcefa08b6ba1666e38425a6`  
		Last Modified: Thu, 27 Nov 2025 01:17:34 GMT  
		Size: 7.8 MB (7785725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:bec8c1e8b63ddc5338080bbee029d2f0be76bc125d1096ab43bba3fbf8d9400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd96e50c9ef88aa4fdb958238d88af6b980d14f75c6f1dc7878222435455f56`

```dockerfile
```

-	Layers:
	-	`sha256:fb8ed2072c20ae32ff710562514c2becb088eb4995299db3e4d1f8c3520df5de`  
		Last Modified: Thu, 27 Nov 2025 04:54:15 GMT  
		Size: 279.6 KB (279560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9357bbc6d31c184d07c4df58d9c99d26effe529c887d3f508899f612bf007bd`  
		Last Modified: Thu, 27 Nov 2025 04:54:16 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.in-toto+json
