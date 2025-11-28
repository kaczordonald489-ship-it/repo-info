## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:5e13c4518dafbc97cd8e7d86fac3e861f31dcd12449ddfb5d459419f3a9f76c4
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

### `elixir:otp-27-slim` - linux; amd64

```console
$ docker pull elixir@sha256:e0176341893dfdda02eece93c5bcc0a77343a65144d9edeaf63596d5fd05542b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132732415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2004d1708ae7a0a45c629011f73e169a97e37f5d6c0f0f85cd2ca4d4ed366620`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:26:05 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:05 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:26:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:26:05 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:13:20 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:20 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:13:20 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a608326287f68cb228977b71497e25fddd9e10183e5627f16f9d43c050b198`  
		Last Modified: Thu, 27 Nov 2025 00:26:56 GMT  
		Size: 76.0 MB (76016877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244c1c3992cea5de3ea7147f0143fdbfa361c140078d0d7ef18f9b3f06bde9a2`  
		Last Modified: Thu, 27 Nov 2025 01:13:37 GMT  
		Size: 8.2 MB (8234777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f7b7870ce8e201e0ba79294ee5315856868574e4b2e7eab9dd79a57491fc0e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c09c0765d781196b5836a53794b3de3d1f457626a754693c64468dbd22db4e1`

```dockerfile
```

-	Layers:
	-	`sha256:eeb801a40b4105d28b17814c8f736df85e482d4dae5564c1ad4ae548b97f3efb`  
		Last Modified: Thu, 27 Nov 2025 04:54:11 GMT  
		Size: 3.8 MB (3831140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed455f6fcaf31e398708d670502f872c7a86404f4119c55833e09b08fc180f8`  
		Last Modified: Thu, 27 Nov 2025 04:54:12 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:800abe28ae752cf26eb9aaaf595894592f6598405b2f68b51f47f4e59afd2ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117572452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb1b4af7bd55c89d330fa046e83b248cfeb36fc2493d0c3657140d1ab185049`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:24:37 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:24:37 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:24:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:24:37 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:13:43 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:43 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:13:43 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b4c76f8d04b084acf6dba2ed82cb74180587f530db0666e3a058ce11b14f12`  
		Last Modified: Thu, 27 Nov 2025 00:25:12 GMT  
		Size: 65.1 MB (65142259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c3106c35450ebbe1819536aed82eb92730d10cf48165f05316bae9a5020b5c`  
		Last Modified: Thu, 27 Nov 2025 01:14:05 GMT  
		Size: 8.2 MB (8234069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:1cc698117cd2359bd689541d98040ab7c99546bee1c18fd4b3e70173cb8fff85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46a8d5452fcc07e0e7d6c6378b0e6d079d3ef9b7bde0706b6ee130d3cbefa2`

```dockerfile
```

-	Layers:
	-	`sha256:3159b904426faf64e21a57ac81b9f8a30d5577073cb0303e799b99034c050983`  
		Last Modified: Thu, 27 Nov 2025 04:54:16 GMT  
		Size: 3.8 MB (3833365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f63db762379a521e61b3e000a380240db4df765a8443413a0ed21aca87e8dc5`  
		Last Modified: Thu, 27 Nov 2025 04:54:17 GMT  
		Size: 9.8 KB (9818 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:47b6747d877bc8345a8e58993b7d5f7af6a71d03baf22914173b3d6794f259af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130345055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eca0ca6403cceaf2b576132729a61a2557309ad355e15a2456244c5e0b6631d`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:26:21 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:26:21 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:26:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:26:21 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:13:28 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:13:28 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:13:28 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6539a0a51735fe965830e7a66c6bd4f6c39123e5b8281342bf88db83c8c3e831`  
		Last Modified: Thu, 27 Nov 2025 00:27:13 GMT  
		Size: 73.8 MB (73751245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4a5fa496c05e83f4ae9c9b75997ec2de13cf3d7a8849f08c2c2549da1bdea3`  
		Last Modified: Thu, 27 Nov 2025 01:13:45 GMT  
		Size: 8.2 MB (8234672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8920a27a304934f0762bd8646686582455cae1bce67c78339d78e3ac9a16e078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479785339537d5f6282efdb3c7a05d883e8763db14855de4adc3334e543c842c`

```dockerfile
```

-	Layers:
	-	`sha256:0bcb92f3f0d34178a7aa2ab60ff7b7d60173a27a539bfc4450a0e98cac0685a9`  
		Last Modified: Thu, 27 Nov 2025 04:54:21 GMT  
		Size: 3.8 MB (3831389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9e06015c788bd671dc36694d6d7a5f4adc92d519b133e35547ce4aced546ba`  
		Last Modified: Thu, 27 Nov 2025 04:54:22 GMT  
		Size: 9.8 KB (9838 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:0215940c13ffcae5aa558f6d06ea4288a39df3c190359414d27169b98284f740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123870906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddcb9ce5494926d5c94385db6f76f361a948603a9027ecd87a8cca666c7bbf5`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:27:02 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:27:02 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:27:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:27:02 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:16:57 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:16:57 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:16:57 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc7c2b4f80b87b88953a3765b55ba899ec3477be9cc497d5e3508acd0a2f575`  
		Last Modified: Thu, 27 Nov 2025 00:27:33 GMT  
		Size: 66.2 MB (66169718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab843cc300fdc9411705eb6d1d53db9bf8bcf6c21f50a3ce720a48b61b0a4db`  
		Last Modified: Thu, 27 Nov 2025 01:17:17 GMT  
		Size: 8.2 MB (8234322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ca034ce80859b53e597cf048fbdcfb11281cd2c5ff13a6f6df5e40e8babd5d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d3107e5ef88c0681bce13ad037114450d8efe6189f381bbf1225409cb2aac2`

```dockerfile
```

-	Layers:
	-	`sha256:4e1f116dd22d1e52ff2b0eceb338198c521abb239f1241e5cb7b44bb209d6924`  
		Last Modified: Thu, 27 Nov 2025 04:54:28 GMT  
		Size: 3.8 MB (3828307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:606def0c622856ebd615d90484d3632d59909cadbb850e160cd0b90307bdb026`  
		Last Modified: Thu, 27 Nov 2025 04:54:32 GMT  
		Size: 9.7 KB (9719 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:bfd4f7f6affa0eec07c525f4d5e8646c5649ba6200fa57231c2b42f3efcd6543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127817613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd5f6546366e86c8717e41c5fcfaef1ada89ea2eb852c94b125c6949308559b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:35:30 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:35:30 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:35:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:35:30 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:26:48 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:26:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:26:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be02e6946e68e185320c32718a92f772107e68af5d926b93b8d9ebeda6e7ca9c`  
		Last Modified: Thu, 27 Nov 2025 00:36:19 GMT  
		Size: 67.3 MB (67255779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c257e0849d6a697549830a6f2f2aa0eee0fd3fb0a3173967d9a9637d9320f796`  
		Last Modified: Thu, 27 Nov 2025 01:27:31 GMT  
		Size: 8.2 MB (8234871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:9990df58672b3c1752f08391b52c8dd85c436cc47dde3d0624472ce25d28e95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354681a65a8a167c922a2d3db0a8533afea76ab37246ec2fbdd499415cf2f98e`

```dockerfile
```

-	Layers:
	-	`sha256:26108cd4bcda0f89439a680fd33bf1b8cde9e8f1992bbbd941cff2a2140020cf`  
		Last Modified: Thu, 27 Nov 2025 04:54:36 GMT  
		Size: 3.8 MB (3835582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8396b2b85541df7b243463708a4a5b8d3c6325a8e6a8e5334b2bfabd4433e1d0`  
		Last Modified: Thu, 27 Nov 2025 04:54:37 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:ad566e23fa45c4169484eaa2aaff7058c8a11bb17ac4b1d6169622aad25220e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121281341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d2c99c92f5fad59c414aedd861104eaff76595afdf369acc9016ff19529f7e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Thu, 27 Nov 2025 00:31:59 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.25.0
# Thu, 27 Nov 2025 00:31:59 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Thu, 27 Nov 2025 00:31:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 00:31:59 GMT
CMD ["erl"]
# Thu, 27 Nov 2025 01:18:51 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Thu, 27 Nov 2025 01:18:51 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Nov 2025 01:18:51 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3fb474867870f70c90d89198517e79c456d9571d587cf4f3245c442885a782`  
		Last Modified: Thu, 27 Nov 2025 00:32:39 GMT  
		Size: 65.9 MB (65909266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aed1b45e8abfd15c91e142bfbc8e610de4c821c66447b900f1e3819fcb70fc`  
		Last Modified: Thu, 27 Nov 2025 01:19:14 GMT  
		Size: 8.2 MB (8234434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:09fc821a0850695c1248d4796263a46639625180c2f4a25f18357d654f8b9b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08d8ea057a3b68bf03e98427d87ad280fc8c683f7ea04bad2ceebec3adc5b51`

```dockerfile
```

-	Layers:
	-	`sha256:3b7137b81c66df26980de6bd5d467de6e03eb69f779c44668734f4ebbee1483e`  
		Last Modified: Thu, 27 Nov 2025 04:54:41 GMT  
		Size: 3.8 MB (3827968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4a47f8d08aeefa11c7640fd8984ea589facfbd914f452179b3bc750ed8e764`  
		Last Modified: Thu, 27 Nov 2025 04:54:42 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json
