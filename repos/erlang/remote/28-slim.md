## `erlang:28-slim`

```console
$ docker pull erlang@sha256:4e5bbb14a5457780fe8ba9e2e5964af5489aad72580b47a8de868bc370d8aed2
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:28-slim` - linux; amd64

```console
$ docker pull erlang@sha256:99273d6e32d94a2180edf402c13bc715e5fdf344943ec069b40d0bc621810aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129167237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c513041800af051d3a4b8f3ff4c4d515e6bd5205c992048c72700951a54dda8c`
-	Default Command: `["erl"]`

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

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9bcb89b361586bc33655266443e43b184b21711d099802ac8cf5cdbf11c990e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fee4f1fc3743bb7e612ef0136f98a2c20f2ddf765366c3154d4252bd3e70dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9ad5d7ab0519db7e7a848ffbd4451e74010b4d1df109fe6e918a78577a06703d`  
		Last Modified: Thu, 27 Nov 2025 02:50:34 GMT  
		Size: 3.8 MB (3824270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44d6267dcba758b76111df7184cf5a82db34f55a84069eb99764ce1889de2883`  
		Last Modified: Thu, 27 Nov 2025 02:50:35 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:b7ecdeedeeb948a9de85d6d2a9871603c699f0ad49d3a304334d5d01f8c8469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116372000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36427ed4190a082c26e194d1806965132fb2e46c57b5c6b50abd49b573bc9e57`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:26:31 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:31 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:26:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:26:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564b9249c1a7a8a77a7d819e5065faa959bb5c75afb766e79908f7cfc7796464`  
		Last Modified: Thu, 27 Nov 2025 00:26:57 GMT  
		Size: 70.4 MB (70356169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:49c3a47616b3b3fea7730b98fbb415c51ddced727984b3a6e3a3e55571961ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fde3a854b7982139e9d8bb7ae6e9334737f1ab0921f53314d5f05d9745d883c`

```dockerfile
```

-	Layers:
	-	`sha256:7355d9aab5ac69ae1f9ae1877880955cb09decde5e0a2420caba4efe797542d8`  
		Last Modified: Thu, 27 Nov 2025 02:50:39 GMT  
		Size: 3.8 MB (3828086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e9921660905cef23aa9e562eba561ecfb638fd02bae7786d48d16bd6590044`  
		Last Modified: Thu, 27 Nov 2025 02:50:40 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:e644ea8116aeae934078bac96f09e6ce29fb0505675b7ddef0768fc230fcc476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113959388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccaa4c19b61c233f338ce5220c042909905152f66a379dbc81829ca9399ea3`
-	Default Command: `["erl"]`

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

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:26618ded75ca5a652e7d736631909b89c45833f78d8ec6027cdbdeb7472d4edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1624ac60fa5b1fe30262fc7fe668e6ec2dd37d1ac023d3749f54761b047a38c`

```dockerfile
```

-	Layers:
	-	`sha256:ba719d131611d004ad3a1bac6b86add0c6d86f8c6717bd4bc5959b87d2b32891`  
		Last Modified: Thu, 27 Nov 2025 02:50:45 GMT  
		Size: 3.8 MB (3826511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da2810282f0993d54fff42171df85d02227c61ae4087f1febf5370c09082c96`  
		Last Modified: Thu, 27 Nov 2025 02:50:46 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:aec430313d139d8cd36f71997b1f4c2b892ec2a1e1af9a7a6c30ce300d26d563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126831830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3618232825e1d2492a4e5e55f981522893657b5e8ff0a7c55ae105f894bb2`
-	Default Command: `["erl"]`

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

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e2ea7a5bba2446c602144f2c6d9dab1761f1435ec21c09f95a9d8f86e4ebcd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9696a857a3649f6b77c78a97f7a1c843326dadd9b8ba7b8477a8ba2591e72d`

```dockerfile
```

-	Layers:
	-	`sha256:1a25b7966cf5d5a5791ed5c63f576fcb70e722d99bc5d87776e8bcc00240e4b2`  
		Last Modified: Thu, 27 Nov 2025 02:50:50 GMT  
		Size: 3.8 MB (3824543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34603565becc65d47a1f024e19691f4acf5d9f3defa571140094d7e1482021de`  
		Last Modified: Thu, 27 Nov 2025 02:50:51 GMT  
		Size: 14.0 KB (14038 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:e15aa3360ba59cc1ff02fe9d00ad6ce2f5345a12160a95583aa3f3b1cc8c1c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120367468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd841ab0ebbbfbdc136a8a40ed963aaac813f54e39382dffa4d4827dd57e2cc`
-	Default Command: `["erl"]`

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

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1747657658a45d7901dbaf711944b133232d810fcfca29dcf38c5a937fb61567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cf152784e1be3763282e9b0ee27d88627fcc55ee2096258feaf96d976405ee`

```dockerfile
```

-	Layers:
	-	`sha256:3308aa6e376ead236f0139b2deed18277fa82e61b06ec0c5cc1ce5255d624944`  
		Last Modified: Thu, 27 Nov 2025 02:50:55 GMT  
		Size: 3.8 MB (3821427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24cdc646022d8cb9a2b4d7a7947daea9a4f562871abe43290aa5bdae00cd5ee9`  
		Last Modified: Thu, 27 Nov 2025 02:50:56 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:010bdbc0c907b27d85ac53ac21b6e6cf3c80f2ac5335a1e714198bde8f8e3e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119598624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb042471aec000f6dda3823227c46ca758f17aff5ea3f70dff1e95c2bd606021`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:55:19 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:55:19 GMT
LABEL org.opencontainers.image.version=28.2
# Thu, 27 Nov 2025 00:55:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:55:19 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2bb7ecb60d8523d7040d5a6181a410952d752544eae679f50087f1ad6dd3b2`  
		Last Modified: Thu, 27 Nov 2025 00:56:44 GMT  
		Size: 70.8 MB (70837668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e45b0c5a5bc481272195cc47630e1329f8e09c995db0546067a9e3fab89559df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e120b70466aeb3ebc753384b95850b26c54bee3679d9b3c454bd1c2c08271`

```dockerfile
```

-	Layers:
	-	`sha256:ebad50401502daa3fdb86846b9d5c7815ae7269304d856678826b3371cf81560`  
		Last Modified: Thu, 27 Nov 2025 02:51:00 GMT  
		Size: 13.8 KB (13782 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:0fd26ab51307f03cd5ac5e19a648b169fff8175658701ba38a8a6152f5de6294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124244270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd66d1790f9e1caee64bd5dc622da1433daf58542fd4878ddbd586df06217f9`
-	Default Command: `["erl"]`

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

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4a65e8026ce39862dde1f8857c3939aaff858c3d7181121b588f8e7776037118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51b3350df1222f1de5ae85e44cbe286fc6df29c946508b58b67f45111b14bcf`

```dockerfile
```

-	Layers:
	-	`sha256:409d4f8de6a1457f8931c1635c2054abbc9d2cc465f3bab8fee2f9ee4bd0da86`  
		Last Modified: Thu, 27 Nov 2025 02:51:03 GMT  
		Size: 3.8 MB (3828724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99425f10a5198d08a5565c66bc55e4270b17b7410c9059a31d2e4c4ae52c469`  
		Last Modified: Thu, 27 Nov 2025 02:51:04 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:613021f7fbc6e6551fd163568d63412aecfcc7ba83bce9a5f26d91ac1ccc79d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117669402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a61e847eef72143b6f7c0a5fe95dd47db2aab3febf6ff5a0f3266b97ed0322`
-	Default Command: `["erl"]`

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

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7ebe95c2afdb84d31fc95efa479ac316f75fb980f12dc119010be892629fac58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f11b9528088dd41fa257acaa5f4b8d210e12e43578010c22fb7fc11f450c7b3`

```dockerfile
```

-	Layers:
	-	`sha256:d85349782b8eeb9bda65464f5be252ea9c35835f46965845b6125c24cd2b51f3`  
		Last Modified: Thu, 27 Nov 2025 02:51:08 GMT  
		Size: 3.8 MB (3821098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95721c162158680aadfd394b91e733dc61acaf5c18de4ee8abecab15863e0609`  
		Last Modified: Thu, 27 Nov 2025 02:51:09 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json
