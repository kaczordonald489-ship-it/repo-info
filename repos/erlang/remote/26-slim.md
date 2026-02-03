## `erlang:26-slim`

```console
$ docker pull erlang@sha256:7ed6ab50296c20e0da467c7df0be9d551eb7a7488bc825301e23f357661dc650
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

### `erlang:26-slim` - linux; amd64

```console
$ docker pull erlang@sha256:bc875df9f70960c483e054beecfe4f8ba4a61b99a8025b8bb836a3af2ccd8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118918708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f2404eedfaaa56bdfe4f9e1a8e7f875213f34e611135c4a124b80909e8995b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:39 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Tue, 03 Feb 2026 02:48:39 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 03 Feb 2026 02:48:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04023862b8796b1f12a56f8450a0bd7b0df4c09cda9e8c6c7c9bcb48a820978c`  
		Last Modified: Tue, 03 Feb 2026 02:48:54 GMT  
		Size: 70.4 MB (70437225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c8f96f6490106dc4ea078cd10d89d19d4042c7bdf07cea51119112713c16e9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8c333916b7d23b4ee8a6aab97939b80f575c6bc6d5d6b9f5e43b9948e02481`

```dockerfile
```

-	Layers:
	-	`sha256:8b5f8f2b78050f061f971f0e20998e1fb13688458339f1eb61f5b19714a7180a`  
		Last Modified: Tue, 03 Feb 2026 02:48:52 GMT  
		Size: 3.8 MB (3825994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d65462ca381692272963938e88bd6d8441a4acf123cfac8fc4073e1e56d978`  
		Last Modified: Tue, 03 Feb 2026 02:48:52 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:5203d3da5123d00bb038a8574e0aa2c080c11b60f782095aa7e4bac7c291747a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106559962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e4fc72c3570f5143ec26d5458a3032128d43f28d91ad7cb18d086ec5196163`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:31:52 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Tue, 03 Feb 2026 03:31:52 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 03 Feb 2026 03:31:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:31:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:48989bca0bd1f08c49cfd2a8eae58c5ffcacc0f005e701953d88f28a5e398ee1`  
		Last Modified: Tue, 03 Feb 2026 01:13:21 GMT  
		Size: 46.0 MB (46016664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2a901d637732ea28caf9637c3e8af41563f36bd0b8905497ead3001dd2915a`  
		Last Modified: Tue, 03 Feb 2026 03:32:06 GMT  
		Size: 60.5 MB (60543298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fc1e1fa1d15a66fb8cccca398c75d14157e597648aa0f84f5efef689f279ba8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05b4d104989f8e19175eda732d7964d413262d835c854d2c9c0be4093730157`

```dockerfile
```

-	Layers:
	-	`sha256:3a7af0f0220603b8eee1a6a1e5a1c5f02ef9a8d6dfad058c2472ee34c4188d8a`  
		Last Modified: Tue, 03 Feb 2026 03:32:04 GMT  
		Size: 3.8 MB (3829802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c57c10f523944353e1175d9c9de2e3a00f89f7fb76565b46c0819a9667d6b9b`  
		Last Modified: Tue, 03 Feb 2026 03:32:04 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:5af5fed66ecebd3c752e7acfc4baa049ba58ac3e9b4dcb8c28474526db8cf82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726580dfaab283dc8867a32026232bce4c55a6db1863ee7fc9ed15ab4bf0f512`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:42:30 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Tue, 03 Feb 2026 03:42:30 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 03 Feb 2026 03:42:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb23f847b7de668d2e913bb88e817f5145686190eb337f877b15616cf31f1f2`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 60.2 MB (60164967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:95038a59f804dd3e91e1b1407076253b8860527062a8610381281a25ba4d14ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1334b3682e98c5c274b4026457f2e38bcc91f45141bc3224246dc1e38ce558f`

```dockerfile
```

-	Layers:
	-	`sha256:802a3dd9617db5bd7a2eaa62296257449399710d9b5ecf1cecded26ce4e7071a`  
		Last Modified: Tue, 03 Feb 2026 03:42:42 GMT  
		Size: 3.8 MB (3828227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85840015f2794f975337708d45b2937c1d9a17b82b85860954bfde8f470d0e93`  
		Last Modified: Tue, 03 Feb 2026 03:42:42 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4560d6169d1b41a2bd12eb3fd4d8cedc71d865368031b7983c9f62cfd09cba81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116435717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8961350ec4601c01c4523885a5921713119ce8ec3f0052b047872b6018b90f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:51:22 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Tue, 03 Feb 2026 02:51:22 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 03 Feb 2026 02:51:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:22 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ad1318324febbdaf2659942f197cb3a165d1d0e671f70e8f90131057699b78`  
		Last Modified: Tue, 03 Feb 2026 02:51:37 GMT  
		Size: 68.1 MB (68069761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b46869a29906c7ce396d04a75c358cac7817bcfbe002c5ba013046a5ba079e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846ccba01de29a62d186ea5af2e6a05f21bc92ec41129444809e1ca6813c7124`

```dockerfile
```

-	Layers:
	-	`sha256:d3188b229d6c3fad9a8adddd8fa66dd8c73d90dade8115385d693b601e4ca301`  
		Last Modified: Tue, 03 Feb 2026 02:51:36 GMT  
		Size: 3.8 MB (3826255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f5a437c0657c8642c91733d07f4863d54b55a3fcc00b7d89fecad1ce0ef11e`  
		Last Modified: Tue, 03 Feb 2026 02:51:35 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:6d25916005f32ff24e4f4f6356ee4d5c7fbd7a3f8042f60cc1d9d3c7d2c35779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110634068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63f0e0a2b5b68a13b156474ec3ddff85cb71b2044edbaebb9426789584317cd`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:53:47 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Tue, 03 Feb 2026 02:53:47 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 03 Feb 2026 02:53:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04eaf4a1af0782517bfc4a1b77ca17aad65e9e7c46c4b4dde534ab50502004df`  
		Last Modified: Tue, 03 Feb 2026 02:54:00 GMT  
		Size: 61.2 MB (61165614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0930efd11038afc6819c922e9f0562d01e462fc43211c823dff108b4c304bb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f627c49822c37e2b7d5d893b1aefc209bde1b3fc37b00360cd42fef3837c97`

```dockerfile
```

-	Layers:
	-	`sha256:5ffc279116530004f0d7967b6b90b2386ad7d30f5fdc37431e3440ad2637d500`  
		Last Modified: Tue, 03 Feb 2026 02:53:58 GMT  
		Size: 3.8 MB (3823155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129ed00ff84123316a8a933df5ec450e660b3e0eae57033325e601e88f6a082f`  
		Last Modified: Tue, 03 Feb 2026 02:53:58 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:cd999908d4fafb3f70572349c1280886845b731cec8baf0c11a8d805af73f259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109906237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4970de2f126651baf15227e313b99dd467609942caaf40c9437af8ff63a433b1`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 20:04:59 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Fri, 16 Jan 2026 20:04:59 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Fri, 16 Jan 2026 20:04:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 20:04:59 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2897bcbed67bcc25e8da56b24dd23795fe133f0bf26f02bd53c947fd90a1f087`  
		Last Modified: Fri, 16 Jan 2026 20:06:01 GMT  
		Size: 61.1 MB (61142844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c1cbcb71c4196f648eadcc6edb126d3f994917d78b8160fcdbd5913506d8d731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05632f08ced80c965847b3ded647d36459cceb183e574f44c0393d3aa2b5545`

```dockerfile
```

-	Layers:
	-	`sha256:b6f98265fffa03ac077ac87b1496cdf36ea39ec166cde54252dd4da108fe43d5`  
		Last Modified: Fri, 16 Jan 2026 20:05:54 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:4e129fca89c36e5fa39e189e185e90ac785efe2575cfc219d85a61573b62d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114588516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79520ca3017b35cfcfc996d4d392e05345b5cde175409bc602b96e99ebf4065c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:35:28 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Tue, 03 Feb 2026 05:35:28 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 03 Feb 2026 05:35:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:35:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b9e2b5ee40fa9d8b43d6e717a860c8154c76e0ad54a465d1515e4dcdb4c400`  
		Last Modified: Tue, 03 Feb 2026 05:35:56 GMT  
		Size: 62.3 MB (62261227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:98446138cde19804cbab278e1a5dc8456b781b23920e28a76e06451b0da07da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6295848767121a113f0310a93ab0d69b0e79383178f4a75a0e127defca6fbc02`

```dockerfile
```

-	Layers:
	-	`sha256:23e3b2a4185ea0b48bca984d605663bc72b2a14c3cd8b843eef7275e8b43fb82`  
		Last Modified: Tue, 03 Feb 2026 05:35:54 GMT  
		Size: 3.8 MB (3830444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3478a1ee1c198ca9b9053bffbb688270495f9b41d9c0652553435fea338542b9`  
		Last Modified: Tue, 03 Feb 2026 05:35:54 GMT  
		Size: 13.6 KB (13606 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:a73fe18bca151d7987ccbd38a88833ff28cbfb3ba3c7e7d6b3003518b6425523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108106069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60b27744f127a63987cbfa632735240dface046cc1eee499656a9c3f503538f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:53:39 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.26.0
# Tue, 03 Feb 2026 03:53:39 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 03 Feb 2026 03:53:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:53:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77176d0f0f67f9ccd6bf699d3e4f31c70e2b1bdedc77ccdc1c1e563d3e16d736`  
		Last Modified: Tue, 03 Feb 2026 03:53:57 GMT  
		Size: 61.0 MB (60967726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ec04166a40a9f4802793751cc15be414132e453639c5d45f17fe403e46a9311b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b307c2be327b33b81e96725fa45c701fd6f25adee3f87397ea3efaa6e24bf4`

```dockerfile
```

-	Layers:
	-	`sha256:832eeee839075689620ff7ea5df362f98362292910595c6a7d2cc623dd86748b`  
		Last Modified: Tue, 03 Feb 2026 03:53:56 GMT  
		Size: 3.8 MB (3822822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f701ea43c87a225811e09d08a4e8a43f1d88eb44c9e77117265a84c18024b35b`  
		Last Modified: Tue, 03 Feb 2026 03:53:56 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json
