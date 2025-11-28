## `elixir:slim`

```console
$ docker pull elixir@sha256:5298fc65ca1c478f98ad347b18949f3a73c6ea548b6e848917fce71838bc5fa0
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

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:4184041634d75259b0691e3ffc58bceb863de1da3a57ee743953afb08ab92a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137394171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016fd5e75340025190b8d0dbed55c08655035ded82d45cd2db59fe14b96bb71f`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:25:40 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:25:40 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:25:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:25:40 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:12:23 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:12:23 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:12:23 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4a2c4a896258c14b1cce58c9ebec503d7c4fb1bed3a109268bf414682319da`  
		Last Modified: Thu, 27 Nov 2025 00:26:09 GMT  
		Size: 80.7 MB (80686476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34de315c47793f68868ee2a20812394152abaf55773011b4a393947489ae412`  
		Last Modified: Thu, 27 Nov 2025 01:12:39 GMT  
		Size: 8.2 MB (8226934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:155de9480e00646aa4af05044cd8b0543175175c49f9aa9ba3c4608b140baab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea57fa4bd079a50e74e33b2b3400fa1acb1e59027938b0ee807727f6059ecc61`

```dockerfile
```

-	Layers:
	-	`sha256:fda8743a3f249f94025fcd3570d9800731c4c436231f5166b8829b4ad9bb9165`  
		Last Modified: Thu, 27 Nov 2025 04:54:39 GMT  
		Size: 3.8 MB (3831912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70aed2b50303e7122d7ee666b19077f9e0b00b329b567769ca55278190d59a78`  
		Last Modified: Thu, 27 Nov 2025 04:54:33 GMT  
		Size: 10.6 KB (10633 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:b415b64e334b80c6a745366153492c08b2f6e3b1a30574c854fee386d123745d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122184688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6662cae93e3c04a09a81d7379abcfe4b7218accd3cdb1b29c9df4563b9b09318`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:25:48 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:25:48 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:25:48 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:25:48 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:13:35 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:35 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:13:35 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e20b947e1c47bdfb508ad26cc674010df46c40860326cc9e0e8912bfa825f`  
		Last Modified: Thu, 27 Nov 2025 01:12:20 GMT  
		Size: 69.8 MB (69763264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b53b5583e09c073550c157761e6dbf8a76d60e82df18538ed62bcd1e04c60c`  
		Last Modified: Thu, 27 Nov 2025 01:13:52 GMT  
		Size: 8.2 MB (8225300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:214c9f140b1b9446495ed2e20a865fc78336c2e63eeca6a3240b5194bda55a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c43f8e4581c59a0fa90d88a1c7b99f3173ed6eb69ab56eb836c6ade8da809f5`

```dockerfile
```

-	Layers:
	-	`sha256:c96e35161170af125328c6a97daf0b622ff9509a3df7f9f9099d55b21d6f2654`  
		Last Modified: Thu, 27 Nov 2025 04:54:36 GMT  
		Size: 3.8 MB (3834161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92d9464a4245ff35eeb1b8b9106ddd763cb9d7df72855b4e7415f1c640689d6`  
		Last Modified: Thu, 27 Nov 2025 04:54:37 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:b4e655a79b849008755021b67ac54c329636ea105d14c4ea55492170059406b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135058572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b6b33cbe9bf115f334d33c2dec7fa63515e6ee9126f1dd022d41c1860656d5`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:24:54 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:24:54 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:24:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:24:54 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:12:10 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:12:10 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:12:10 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b3a61e63593f2bb78faf057afd24a1f7480ee78a2b074310e3dbb0ec5f8c03`  
		Last Modified: Thu, 27 Nov 2025 00:25:37 GMT  
		Size: 78.5 MB (78472692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a4fefb70b1f58e25e6317c56b36539e2aeafff8cfdc33d91b46d770d3a1776`  
		Last Modified: Thu, 27 Nov 2025 01:12:28 GMT  
		Size: 8.2 MB (8226742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:77716b0e59cb480bbb6d0e10416dfd1c9fda6593fb4230cc56f7a3e808791f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ba5bd0d9b802d395ac6ca53f277af8916b00539df6c5dff395f2c99e5d369a`

```dockerfile
```

-	Layers:
	-	`sha256:549340532a35c785c5c1c40208e5c0afa757a725c9afa3d85d935291bda14f20`  
		Last Modified: Thu, 27 Nov 2025 04:54:41 GMT  
		Size: 3.8 MB (3832197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a3bd79d10dfc4b6bcbb4ed7010d90c79d7c7ff56c9fa3ca5da23ed792a33020`  
		Last Modified: Thu, 27 Nov 2025 04:54:42 GMT  
		Size: 10.8 KB (10759 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:dd3d09f843e3c324bb383e3b4097e645c3e7b3898cd914fc5f309f6eb2fa6884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128592918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0d3c49a3829f73d66e1fe55b2cde646dc7584d5e55d97630c5b1b6c61b4ce4`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:27:04 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:04 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:27:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:27:04 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:14:11 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:14:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:14:11 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023f9d20b7b4318d23a4d152d11019f81abe8ced1a42c8b74fbec149b1c7ade5`  
		Last Modified: Thu, 27 Nov 2025 00:27:31 GMT  
		Size: 70.9 MB (70900602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea64079178e16a9581b6f799c604997bab5f609a4ad76ae3217fb82178b0556`  
		Last Modified: Thu, 27 Nov 2025 01:14:38 GMT  
		Size: 8.2 MB (8225450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:571f741f0b6f47dc8b6010e00b460f95d82276eb1f02d21aff5b58af1ba83a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a205a0ac88c2b36b34cf352d46306e292853a6191ff8a45aacfbf23c1f638`

```dockerfile
```

-	Layers:
	-	`sha256:e81e5218956c49b50d627bfa03a4b5d00764fbdbcebac60698adf98062c535b3`  
		Last Modified: Thu, 27 Nov 2025 04:54:46 GMT  
		Size: 3.8 MB (3829064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274392b2618d301f9e7400e21b1abc0b4ecee940df50de100400fa0c9dd8b76f`  
		Last Modified: Thu, 27 Nov 2025 04:54:47 GMT  
		Size: 10.6 KB (10591 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:182d4294ae80d6f3d63cf56eabba4f96671e36c91a18d0ab30f27c44b2863ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132471309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879dd0a53c25839e476b8043c7cda56e7efe17cdca6223259ed7b53f3f69e0c3`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:27:18 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:18 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:27:18 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:27:18 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:14:09 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:14:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:14:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e51a932852a19719e85c4c36cf51aa4382ccab272235259f3bac4268906bdc1`  
		Last Modified: Thu, 27 Nov 2025 00:28:20 GMT  
		Size: 71.9 MB (71917307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b46a98e74876a96e42e5134c31cec9906f37aa6aa9e2db420eedb8e180ea06`  
		Last Modified: Thu, 27 Nov 2025 01:14:36 GMT  
		Size: 8.2 MB (8227039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3269b9648ad727db92351c79c70ea876257b061fa9dacb99c50e05e71bba2928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26dffb51628e833c68db37d5722e04e5e0f7677dba4816e99d49936ae2dc8f2`

```dockerfile
```

-	Layers:
	-	`sha256:51c7a9a579bac75da2da682f8b7d23f1ead10878516eebffebcda88b882270ab`  
		Last Modified: Thu, 27 Nov 2025 04:54:51 GMT  
		Size: 3.8 MB (3836372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e872f30fba23c41d57fcbca80b6ce248884a3af81dfc8d9129d4c479c4ead2f`  
		Last Modified: Thu, 27 Nov 2025 04:54:51 GMT  
		Size: 10.7 KB (10690 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:a2ef9c7d5dbf6dde96958b138fc2fe5bf7b7eda523487efe4fff75d4e15725a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125896107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4b2423b5dcc1ccfbdf52993fc68a25b203bf1d394ef5cd48680d717c95de9c`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:27:56 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:56 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:27:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:27:56 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:13:31 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:31 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:13:31 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab6b96c5bfe14427985aff07bdff2124afde448cdeb834e26eb9e91733f4793`  
		Last Modified: Thu, 27 Nov 2025 00:28:42 GMT  
		Size: 70.5 MB (70531761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1f8ec93d108d1607680692c2474f23c910246930314aac9e3d22a67d3dc4b`  
		Last Modified: Thu, 27 Nov 2025 01:14:02 GMT  
		Size: 8.2 MB (8226705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:4b54d22d2b5c995e5825853345f89175b692b012fae7a7ccca83df5964142101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb91f09eb14167cb8b793578cc3f7f050b863988a41b56d0378dff550ef3946b`

```dockerfile
```

-	Layers:
	-	`sha256:0cacf25d7b54ea98fce88c487bf24598061b8d1b019981853b599e75cab793d5`  
		Last Modified: Thu, 27 Nov 2025 04:54:55 GMT  
		Size: 3.8 MB (3828740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222e5ade0f70c36d41273abeebc10b182d4d9f9f660da9b529e5fdbe3f9d1008`  
		Last Modified: Thu, 27 Nov 2025 04:54:56 GMT  
		Size: 10.6 KB (10634 bytes)  
		MIME: application/vnd.in-toto+json
