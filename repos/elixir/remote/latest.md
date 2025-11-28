## `elixir:latest`

```console
$ docker pull elixir@sha256:054df3b1e593953f5139196e3d48b57597796a237c2421ec93cd2fc673fd2517
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

### `elixir:latest` - linux; amd64

```console
$ docker pull elixir@sha256:6055852c91b8e2fdff85fb42e349c02c8d57ba869944700960da190c2755e740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.1 MB (631142867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf800565f5ad8e45bae87ef252df0579a58a5ae26678b90d31e4d25216a67e0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:21:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:25:07 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:25:07 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:25:07 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:25:07 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 00:25:07 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 27 Nov 2025 00:25:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 27 Nov 2025 00:25:20 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 27 Nov 2025 01:12:17 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:12:17 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 27 Nov 2025 01:12:17 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1208d53eb0667932469017a5ef3960e5ed2aea9143d62b983abe2f8593eeb9a`  
		Last Modified: Tue, 18 Nov 2025 11:12:42 GMT  
		Size: 211.5 MB (211460976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca5e33cc0c88344c6ef8339542351d71d35719ede6924a475422df22c0959fd`  
		Last Modified: Thu, 27 Nov 2025 01:11:53 GMT  
		Size: 274.0 MB (274005798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c6e827cf8819b4cc5e00f00bfea45b0bb308d1ac71922390f5dfcb56297f3`  
		Last Modified: Thu, 27 Nov 2025 00:26:29 GMT  
		Size: 191.4 KB (191386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc843c9b2535561222df7bd7a7dff96d874004db00930664358a5ca9fcf5ef1`  
		Last Modified: Thu, 27 Nov 2025 00:26:30 GMT  
		Size: 817.8 KB (817762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ba7f404f55a2cd563862d9d41bc6cc40a7c036c757869cf3db277fc251ecbb`  
		Last Modified: Thu, 27 Nov 2025 01:12:52 GMT  
		Size: 7.8 MB (7760574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:eabe288b1f98ea370c3e3f5532c34666324662007001d26b9c6dee32998bce0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23787236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ca77d9cb011f304971aef263849a9e3a21d54e5e33d9ef0a23db0c241f7fb6`

```dockerfile
```

-	Layers:
	-	`sha256:4692c77d99afeaa4c750862fd8f23e52a01511d321ece0811a6dc4cf50a6f88b`  
		Last Modified: Thu, 27 Nov 2025 04:52:21 GMT  
		Size: 23.8 MB (23775987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15ec1ac0cb301b3c1c57cf19ea5d9fb2e4eac3bf3bf03d95968878691646387`  
		Last Modified: Thu, 27 Nov 2025 04:52:22 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm variant v7

```console
$ docker pull elixir@sha256:69cd76fb6abd8028f420f51f197ddeaae3d0d0f690584ae5d6052c50e40677e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553701133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b9c4e96665bf40470c7f6b3432f1bf599135f8ee490a26b24349ed693c7187`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:26:02 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:02 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:26:02 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:26:02 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 00:26:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 27 Nov 2025 00:26:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 27 Nov 2025 00:26:29 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 27 Nov 2025 01:13:28 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:28 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 27 Nov 2025 01:13:28 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad0f2d457569ebe1e8bb868d038539ac612c99d1c10b8c279ff1a9fd7fa24be`  
		Last Modified: Tue, 18 Nov 2025 07:34:33 GMT  
		Size: 175.4 MB (175370481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d572a0355ddbdefcd95e8fd03cecc4d408776821eeb76defd0a6990bc94b9b`  
		Last Modified: Thu, 27 Nov 2025 00:31:41 GMT  
		Size: 243.8 MB (243778895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd363319b17e5fd8313275b8b7ada2790fdebbeb198d005142e6b7666ccf1a`  
		Last Modified: Thu, 27 Nov 2025 00:27:27 GMT  
		Size: 191.5 KB (191464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fc69f04e61f77ab4f1c51c4ce5c3b349babffa78468d5b757957fb820979fe`  
		Last Modified: Thu, 27 Nov 2025 00:27:27 GMT  
		Size: 817.8 KB (817763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff34fe901e91a70a021214e7fb8b4dcf4342017ca6b151084d74ef15c9b46c1`  
		Last Modified: Thu, 27 Nov 2025 01:14:10 GMT  
		Size: 7.8 MB (7759582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:77cbe7f89e09c2aa12442c994f900287975045326c398a963afc06c3d3510cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23600322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b819938a2dbea5b23ef93c78e9b01024241d01a267552b946bbca0312ed8cef`

```dockerfile
```

-	Layers:
	-	`sha256:dbc565831fdd69640a11a8055c3678bfb4f9bb3fba5b6e8c88bd10549cc02ac6`  
		Last Modified: Thu, 27 Nov 2025 04:52:47 GMT  
		Size: 23.6 MB (23588977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33e764478ead558f7a201ee5b71c905120ed1a6f66af557a2256ed6e95e1234`  
		Last Modified: Thu, 27 Nov 2025 04:52:48 GMT  
		Size: 11.3 KB (11345 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:a740a6df7d3c209a009bf36b85336627acc0efc428894dd3ac72bb75d2bad528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.2 MB (615205376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff229d143eb71124885ad643b4badf64ab4f1482ffc1ff589bb7a8e77a50095a`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:33:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:25:50 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:25:50 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:25:50 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:25:50 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 00:25:50 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 27 Nov 2025 00:25:52 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 27 Nov 2025 00:26:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 27 Nov 2025 01:12:12 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:12:12 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 27 Nov 2025 01:12:12 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea7607dced22dd12cfb6fe96ff19187f5ee918dd3d48379e2d2fd756af4818b`  
		Last Modified: Tue, 18 Nov 2025 07:15:14 GMT  
		Size: 203.0 MB (202980192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff29eac745c733640fb7a5b2a9aa57ae80beb3777b2c73efba5732610260b2`  
		Last Modified: Thu, 27 Nov 2025 01:10:57 GMT  
		Size: 267.1 MB (267126575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4b3eceafe408dc38efa092fd5b2bf567c2271f42287ee08389bc0169148737`  
		Last Modified: Thu, 27 Nov 2025 00:27:10 GMT  
		Size: 191.4 KB (191407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82648ce74dc782890f140fd71ed61a97503ddca56afd237aa8157a650cfcceb`  
		Last Modified: Thu, 27 Nov 2025 00:27:10 GMT  
		Size: 817.8 KB (817762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa52c58df9166ebb398f92251c2540dac3a90f7b247b2b9fad8a517543d91a3d`  
		Last Modified: Thu, 27 Nov 2025 01:12:56 GMT  
		Size: 7.8 MB (7760568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:8232f5f115b6239618079bf06c06564cf7b7f9d4656aeebc1365761407244a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23826843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342eed1ca1d0a041755d5d5cea1d643f76150568daddb7bd8dd253a5969e4302`

```dockerfile
```

-	Layers:
	-	`sha256:c6507fe8d6ebb189dc9f0639fdc557d58b5b8dfc869128e2fe72003709f78d23`  
		Last Modified: Thu, 27 Nov 2025 04:53:12 GMT  
		Size: 23.8 MB (23815468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81107d8b01a964f9b49aafd2150587d74e6110f5906581ed457b6e6aaa33671c`  
		Last Modified: Thu, 27 Nov 2025 04:53:13 GMT  
		Size: 11.4 KB (11375 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; 386

```console
$ docker pull elixir@sha256:3f4fe3ab875527ce5f99d62aa5734943eccf846b47862a98eb4dc65ef0473206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624467994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd13a76ffe9604b489d301a50177f930d768910b2543fbfcfc2e7e4fe66e0db`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:15:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:26:30 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:30 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:26:30 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:26:30 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 00:26:30 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 27 Nov 2025 00:26:33 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 27 Nov 2025 00:26:53 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 27 Nov 2025 01:13:24 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 27 Nov 2025 01:13:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c185d92b9a40ab45d15fa519a2c049e78267565301d35e186267bc212115f`  
		Last Modified: Tue, 18 Nov 2025 06:19:22 GMT  
		Size: 210.4 MB (210389386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef6c8978c88becf0ee0288159b4f28faf6d7b70e71a60c429e2afebb1473e85`  
		Last Modified: Thu, 27 Nov 2025 01:12:56 GMT  
		Size: 264.7 MB (264744589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6f2ec946978e6c03ae08f2e237f0c0d654a235a76e9ad6c6de7160ac5d964`  
		Last Modified: Thu, 27 Nov 2025 00:27:59 GMT  
		Size: 191.5 KB (191490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603921ea0c390033030091f3395dfbec811334c078b1eebccc464434de924673`  
		Last Modified: Thu, 27 Nov 2025 00:27:59 GMT  
		Size: 817.8 KB (817762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3edc2e40d7522a9d0d50e9588fbcbeb35e57faaea71d2c6236af1b7dc4c2048`  
		Last Modified: Thu, 27 Nov 2025 01:14:08 GMT  
		Size: 7.8 MB (7759616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:588348084372848fbca3fe2ceab5c2ee1110c2c50257f425789f7f0942965be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23754860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83af31ced9d33b830bdfd24d5e4e87dbbf70cd66a20050673d57291be1308633`

```dockerfile
```

-	Layers:
	-	`sha256:eb3ef0d9ef06f2c93253910b87c3d9987ba5de00a3f7f3622307e87560b9ea1a`  
		Last Modified: Thu, 27 Nov 2025 04:53:35 GMT  
		Size: 23.7 MB (23743653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728367c8f20092321f73871d3c9ba00b2bd76540a586cfcb386dd1cb460db456`  
		Last Modified: Thu, 27 Nov 2025 04:53:36 GMT  
		Size: 11.2 KB (11207 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; ppc64le

```console
$ docker pull elixir@sha256:e6ceddf7fd7018ca2076bc3a09bf29369e303b1ea4a5f530e11068ce1fe5dead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 MB (639095475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d42172a5466a3517662618445f95b194da8baa4f915f8fa95ccdfc76ae56f3`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:17:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:27:55 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:55 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:27:55 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:27:55 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 00:27:55 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 27 Nov 2025 00:28:03 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 27 Nov 2025 00:28:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 27 Nov 2025 01:13:37 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:37 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 27 Nov 2025 01:13:37 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d717b62eb888bb16cb77af768613d5d676b28f09ab1cb591a5130af4b846f`  
		Last Modified: Tue, 18 Nov 2025 06:52:50 GMT  
		Size: 69.8 MB (69845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055d1d2e62969664b2197803b2dd13eb0c52b160f256835c7b8bb1eca8dc83d`  
		Last Modified: Tue, 18 Nov 2025 11:54:22 GMT  
		Size: 214.5 MB (214498281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b3f9c46892bf5e0f71d4bc4e11b00dcb4073267c5f46288c09e799f00d18d1`  
		Last Modified: Thu, 27 Nov 2025 01:17:57 GMT  
		Size: 268.0 MB (267982771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602be03fe7b3cb45d1b9e7f34b2b471807d2ee32d927d7466fa21504c41da324`  
		Last Modified: Thu, 27 Nov 2025 00:31:44 GMT  
		Size: 191.5 KB (191491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0635feb25ca345a0afc5e2a597f7df820c3553c8011f0bef5b23178c57be6ae2`  
		Last Modified: Thu, 27 Nov 2025 00:31:45 GMT  
		Size: 817.8 KB (817763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3b1bda472a6fe1a1b356ab681d3a8e6e896d931eda2da6799ebd3c0b324956`  
		Last Modified: Thu, 27 Nov 2025 01:14:50 GMT  
		Size: 7.8 MB (7760566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:c177d76984b7d751d46faec1387e38d59adbe0a1da50e39f02249aa3278c5322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23742795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39db5b69109b718eed275d056c2fab279ec5e9d91994895ec2a3360587808cfa`

```dockerfile
```

-	Layers:
	-	`sha256:155d13b1f9ce4756cb503cb70f22e278e5490425a82f9d862de7745ab7b6f253`  
		Last Modified: Thu, 27 Nov 2025 05:26:35 GMT  
		Size: 23.7 MB (23731490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f4963c635aa7fc17eab75e6753968ecc34db20ef55291b7497b8c10fc0c0ee`  
		Last Modified: Thu, 27 Nov 2025 04:54:27 GMT  
		Size: 11.3 KB (11305 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; s390x

```console
$ docker pull elixir@sha256:e9978802d517b7626c32e94406b07a1af87c966dbf28572833aed4b5fb9fb26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.3 MB (592337543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fe99c8f12cade8699a1056d7b78916b8806e18b75860945a03bab2859938d2`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:29:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:28:31 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:28:31 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:28:31 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:28:31 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 00:28:31 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 27 Nov 2025 00:28:37 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 27 Nov 2025 00:29:11 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 27 Nov 2025 01:12:34 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:12:34 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 27 Nov 2025 01:12:34 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a3c31d224355129a49f91ee32618f26bf3cb019a25f07a3795c22816b92b87`  
		Last Modified: Tue, 18 Nov 2025 08:13:31 GMT  
		Size: 183.5 MB (183498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f696e4201ae271c7a885fae81e832102d2f0bdbdeca5f64994132a0c51b9e`  
		Last Modified: Thu, 27 Nov 2025 01:14:28 GMT  
		Size: 265.4 MB (265403656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88191398af699a109e3f33af9d4f3919fc329e4f37e7583b8e456ddcf14e7a`  
		Last Modified: Thu, 27 Nov 2025 00:31:17 GMT  
		Size: 191.5 KB (191475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acafa95b89a5e7d22b4a948136f60ebfd1bd47452e234029d18f36e7fde4572b`  
		Last Modified: Thu, 27 Nov 2025 00:31:17 GMT  
		Size: 817.8 KB (817763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf5430461e0e80ce1ca27db41156bff8e8e9a17b51f5e9262c2e28b7fd7920b`  
		Last Modified: Thu, 27 Nov 2025 01:13:46 GMT  
		Size: 7.8 MB (7760180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:c1fa6769dc256bdc89871cafd04a3b3cb1333b6a89b1822158cb28488ca1ecc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23554701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f580c551d0b4bd3131903b1942f0176a404eada75f912af8c558e830c0c70a5`

```dockerfile
```

-	Layers:
	-	`sha256:cbdeb822b528ba7563cbea6be74a09f1e675b50eb792c4e9230fbd1fc72278d8`  
		Last Modified: Thu, 27 Nov 2025 04:54:49 GMT  
		Size: 23.5 MB (23543453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0fbf9819e579144fa116e06f3307c29bdbe4e66bcfce63f3d55767414824d85`  
		Last Modified: Thu, 27 Nov 2025 04:54:50 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json
