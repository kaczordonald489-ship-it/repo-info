## `erlang:24-slim`

```console
$ docker pull erlang@sha256:93fb75bfe95386d0074a8f0b06485a79b53be1e7ce82b6631f4044bcea5aca06
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
$ docker pull erlang@sha256:675e1cc1aa96c3ac44fe7c3be28dab2577c477f4709000c53e7d4bc3bb67cb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118999072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99238c241bcf0a31e0b4e5dee8fcc74aee8dfc47f1daeda70aadbfbcf1a3d2dc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:36 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 03 Feb 2026 02:48:36 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 03 Feb 2026 02:48:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b9a4b26a5263d6fd2e8bf580dccad68e3740d759a9ce1e1526005598080af9`  
		Last Modified: Tue, 03 Feb 2026 02:48:51 GMT  
		Size: 65.2 MB (65242813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f089b4bac69055a48558e827a6ea31409296816e1f83f0e0b97d01394c8eaa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f546dc36138ea1382bb21c1312e00ec0696fb67024621347479c4e0fc7ba6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:62ad3e74a38220a5b785f94fcf4f5271939df7a17e2a708444cd17ed910214ac`  
		Last Modified: Tue, 03 Feb 2026 02:48:49 GMT  
		Size: 4.1 MB (4098871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e079cd1abbcedd04eb8240d745c0d1f99ae8748c1c4bbcaa2037646bc902356`  
		Last Modified: Tue, 03 Feb 2026 02:48:49 GMT  
		Size: 13.6 KB (13568 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:bbfb7de7e6d8e6481cd09aab590a9918a0369500bb9c50d25c5a048a5b29dc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106272794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf5c459f9c9cf9bfce42c0b87e8d6f1624d7b7239ccca0184c964fa54141d6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:44:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 03 Feb 2026 03:44:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 03 Feb 2026 03:44:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:44:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6ca5f53d580fbc72887807a74d2d1c2f8900fc3f535a8082d3df4fc3f9e84caa`  
		Last Modified: Tue, 03 Feb 2026 01:13:42 GMT  
		Size: 49.0 MB (49047418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7daae9f2fb9ad0379e21793421abd34542b2ab8119014293cd8b8fed388594c`  
		Last Modified: Tue, 03 Feb 2026 03:44:23 GMT  
		Size: 57.2 MB (57225376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:acd3c774cbae562b1b9e537d5203f135b3c67ae86744909766e21450ab562c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f862c873445c6612027faec21b992e3d4265fc219fc65b7800d2ba3c75172aa`

```dockerfile
```

-	Layers:
	-	`sha256:93416e2b94212977f42923ae2791c283b0105fcf4a546335382215e0efa2fc56`  
		Last Modified: Tue, 03 Feb 2026 03:44:21 GMT  
		Size: 4.1 MB (4100472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d505cc00df15c901956a37bf5b2f367793de10f1ad8025e4f8665b0915aeb44`  
		Last Modified: Tue, 03 Feb 2026 03:44:21 GMT  
		Size: 13.6 KB (13648 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:173f4cd662dcd18a8e1794ec62cf4d5693651f79eef5ec2f288beb42292084a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110334804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dad694b79e88ef4c284438e00270e79cf8121d43aea944a7c1bb9751413cf0d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 03 Feb 2026 02:51:33 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b3a9412663e782fb8852bd249e862903f223e78686326993be5b0c4f3f7b99`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 58.1 MB (58076484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:85240ea8fb2a89a5aafeef7d117bc3e7b33a98bf2b11211966fffbc0eacd72c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fae524387e1d3d57ecbacd7de3371d0fa2e96aae4e4d95277ec882d8663338`

```dockerfile
```

-	Layers:
	-	`sha256:ff46fff976c84717b904fd9eafc090a77857dab67f7b85ff7a300f11bf8e63b5`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 4.1 MB (4098492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df711e17f17da22124ae8910cf4f0e20fe3049ec71ab78c060f017b29fd9e82e`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:e89c82ca6278f2f429fcc05a9f92c32268052657f8481a6f66320dd30dffae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112404152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b7d9197da3e2ae1d9738edff19de9ff9fe1a1b867cf9dbaeb5558fa53d4625`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:53:01 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 03 Feb 2026 02:53:01 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 03 Feb 2026 02:53:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d867f1cb84f70eace1980e6a12e79215ae43c3022c3ce673b6568f18cefa5779`  
		Last Modified: Tue, 03 Feb 2026 02:53:13 GMT  
		Size: 57.7 MB (57704570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:52910c696ec9d0d962653c4a6b880cbe5faf6c1a453a97b3f688a90d29ed3f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2555e328d4c844931970ca5979f007db6dba464d826058532821faf0225e58dc`

```dockerfile
```

-	Layers:
	-	`sha256:c250838c03a9f32b08d4ec14a96cd7d5a2f4532a2542f0e60ffb727f9527ff18`  
		Last Modified: Tue, 03 Feb 2026 02:53:12 GMT  
		Size: 4.1 MB (4095399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a40d103b5156dd109978dc355aa66707c61e7adc7b18f7359774e309e302828`  
		Last Modified: Tue, 03 Feb 2026 02:53:12 GMT  
		Size: 13.5 KB (13536 bytes)  
		MIME: application/vnd.in-toto+json
