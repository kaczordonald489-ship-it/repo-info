## `erlang:24-slim`

```console
$ docker pull erlang@sha256:9b953cad80687f583a21b00170b076bee2a1f11e73540221ea4a25006026530b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:1f12966422b8f99b114bd999bb476c37e5b9907be4587b69dcd256e0e76ac6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118997862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253863311a5a25502ace8c058f4c76a28702511aa01919e78e2023e89dd9ba96`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:20:15 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 18 Nov 2025 05:20:15 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 18 Nov 2025 05:20:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:20:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e24e9681b98d034f4d1ec7d34ac4a2c69860b14fed0ddf0fa9a73b328c61d9`  
		Last Modified: Tue, 18 Nov 2025 05:20:42 GMT  
		Size: 65.2 MB (65241431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ce4cc16df81cf9d2460a3e48ed3db281c3642a774fdd07c3363695975113e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fc63ac30191742fce45d6d53cd52612e604f970c4e179bdea107dc648e1986`

```dockerfile
```

-	Layers:
	-	`sha256:3b9f9aa1ccdeb13b4f5f6d3cd58d31aad80b72b0eab18eaa0d15b6a421b76d64`  
		Last Modified: Tue, 18 Nov 2025 08:46:29 GMT  
		Size: 4.1 MB (4098871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479028200c170a49bc58fb31599d4d61c11d9f9f13c605b582e9193df5fd6971`  
		Last Modified: Tue, 18 Nov 2025 08:46:30 GMT  
		Size: 13.6 KB (13568 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:ca0788109ca3fcc529b0bcfb97d32bf0f2fdbdda603ec99aac2d3ed3a49212a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106271798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6208fc58fb9ea064dfe265785981ad478d0d92cafc47d2bb3eebf3f9b92c40`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:26:30 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 18 Nov 2025 04:26:30 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 18 Nov 2025 04:26:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:26:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:516616c63b11e5af36116ed0b70c230c2287eab3b74b11a00eb299cc4575af64`  
		Last Modified: Tue, 18 Nov 2025 01:14:16 GMT  
		Size: 49.0 MB (49046365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a1ec34f167927619a48fc73c4079662eef9828da926c62266aa91e0cf3113`  
		Last Modified: Tue, 18 Nov 2025 04:26:54 GMT  
		Size: 57.2 MB (57225433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:94245891294f79d4e7628dbef74daccdac476fb4acb3761cda1d5231b465a681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4de98e7571bb70ff2b2eefc3e341e5a4a9bb3120204d9a6835430dc3b3642e`

```dockerfile
```

-	Layers:
	-	`sha256:74b70dad7feb75911e2c8bdd27ddd6039945b40d3f9600dc95cfad4637519796`  
		Last Modified: Tue, 18 Nov 2025 05:47:18 GMT  
		Size: 4.1 MB (4100472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb41a98bc908dfd77a92226aa855740b35b37486b66f2a4e290a4483ecbeeed8`  
		Last Modified: Tue, 18 Nov 2025 05:47:18 GMT  
		Size: 13.6 KB (13648 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:449bcdf3e22ffc3bb2e3a49e7928343cb5fba71e1afe2ec9d22aca2496709c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110334443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c276c2df0b5fcc871f908b566e3434af2022ad9c67f272e0d06923fd61b8e4d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:47:42 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 18 Nov 2025 03:47:42 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 18 Nov 2025 03:47:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:47:42 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89112eec52821d212d9f13e0f8165934ffb93f12b95ebe10d05d9d402935c2e7`  
		Last Modified: Tue, 18 Nov 2025 03:48:10 GMT  
		Size: 58.1 MB (58076748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f6f731b67141c36ae1bde61f081736ddf30dc32c627459550a4755c8b32df5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bbf23a352d71cb834f7320c612158f5f507565043b0ee09b48517137bcc771`

```dockerfile
```

-	Layers:
	-	`sha256:e4ced682bbbb4d2ef71412020bafa38f7f60e89435257f3a66909c8c2ae2449c`  
		Last Modified: Tue, 18 Nov 2025 05:47:22 GMT  
		Size: 4.1 MB (4098492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f226f664b169420545dcd3ad9bfb0ee7391c5564bbe7f96a33e7fa9aa3951a`  
		Last Modified: Tue, 18 Nov 2025 05:47:23 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:ec62a6d26005d1211bb77b6c46e267e1e6861d62ee7ee0dea6fe62eda03302d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112404332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b64f83acf5b7755b985afc0e3849bc918e78f98b91d0151b802071103662af`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:01:31 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 18 Nov 2025 03:01:31 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 18 Nov 2025 03:01:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe4e014f211f526c0988b1713c1a62af190408b42adf2c38f0b2a4ba3bab7a5`  
		Last Modified: Tue, 18 Nov 2025 03:01:57 GMT  
		Size: 57.7 MB (57704733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:52811c948a5b6d58081c236e2d3f530f06be07786a7aa0d47649a0b2c39895ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506b253f1dde5d550cc447581d583ab63035ce6295c5e427ede999e3e02e48b5`

```dockerfile
```

-	Layers:
	-	`sha256:d59911d0554ae8f0b25a684df138d50ba118b52d098c10dd8eb1e6aa26e60fbd`  
		Last Modified: Tue, 18 Nov 2025 05:47:27 GMT  
		Size: 4.1 MB (4095399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce91305fe073a00da07bed5943534a23a7359b17fabd8578f2b6607e0f212bc3`  
		Last Modified: Tue, 18 Nov 2025 05:47:27 GMT  
		Size: 13.5 KB (13536 bytes)  
		MIME: application/vnd.in-toto+json
