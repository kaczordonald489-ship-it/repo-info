## `haxe:latest`

```console
$ docker pull haxe@sha256:0684cdc16693028aaa8e63cc6aac0a3786a76a867aa292831161ca67f90aa41a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:84a1335e9bae6807b6bfb1c3c5a564c53f93507e802e14d361bf0ea53989be86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398485394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62197949725bee8533b613d3aff04aa26d384314f4f4d79cb736a4b61d92e8da`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:25:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 10:25:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:25:35 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 18 Nov 2025 10:26:57 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 18 Nov 2025 10:26:57 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 18 Nov 2025 10:26:57 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 18 Nov 2025 10:30:24 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 18 Nov 2025 10:30:24 GMT
CMD ["haxe"]
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
	-	`sha256:12da942ee66e3c46150d614120f43faf4bda1ba903b76a7362ee22e7177d9d16`  
		Last Modified: Tue, 18 Nov 2025 10:31:07 GMT  
		Size: 1.3 MB (1261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3178fd86240aae7502a5c2d34c0bbb9454d7816ab96fd8ab0d4a3a52187935a1`  
		Last Modified: Tue, 18 Nov 2025 10:31:07 GMT  
		Size: 1.4 MB (1385124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84b9262bc3cf7034aec4091a02917774e6916b18213f56d97b10a0f2220c34c`  
		Last Modified: Tue, 18 Nov 2025 13:24:53 GMT  
		Size: 258.9 MB (258932411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:36a802f6a278c0a3f51718fb1d3e22be26db7a5f8aad08ef1cc04f48b3774ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d533b4d275c159af34263d57ad4068dc882db24f1f82c1406149541846f6b0`

```dockerfile
```

-	Layers:
	-	`sha256:f24cf07bd4c434f7a165b997c5af4941b1af522962ae4a54711a55d4693798d5`  
		Last Modified: Tue, 18 Nov 2025 13:24:16 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:81a4f73d6075716053d3a0a20e4d0f9d894eb31c60f1e9d713837d5241d1d552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361506029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06eebca99d204b9b8d018ff7f6884ac1be54c5d6c5925d8469bc52206cb3a60c`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:29:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:29:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:29:57 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 18 Nov 2025 06:31:19 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 18 Nov 2025 06:31:19 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 18 Nov 2025 06:31:19 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 18 Nov 2025 06:35:22 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 18 Nov 2025 06:35:22 GMT
CMD ["haxe"]
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
	-	`sha256:f9c7a20fd1b35d52c3ef234db241b7b9a7f9409b4658de2bd10b31389b902e08`  
		Last Modified: Tue, 18 Nov 2025 06:36:02 GMT  
		Size: 1.2 MB (1159476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6568b70ab52e86ce570899f486b58d53644e16cd36505d2d8d7a13e7804e4d`  
		Last Modified: Tue, 18 Nov 2025 06:36:02 GMT  
		Size: 1.3 MB (1326691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f769b25f073e084d00eb7f67ae39e3a1ccc54ed5bc9cc648bf857009eb5378df`  
		Last Modified: Tue, 18 Nov 2025 07:26:33 GMT  
		Size: 233.2 MB (233236914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:dcb272d686e91f5a9c6dfe5c7833e7b527f265f3d92a47b1833398ecd4f49412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6805c769f8b1e20293461133380ed156e13fab7597a3f30c02ee95e031f14e69`

```dockerfile
```

-	Layers:
	-	`sha256:cbfb6256bbe16c2df54ab084c0f8199289b33fa3bb71ee5d3d94a36e0f16af0d`  
		Last Modified: Tue, 18 Nov 2025 07:26:10 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:eae8a60b446498f1ddc7ccab5400e4acd7cbfb5aa97a61a761a7ece79b483c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401368326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a49365692561f4c4f3e4a4416c67226ede87637955fc920e9139db5b5ce304c`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:39:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:39:37 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 18 Nov 2025 06:40:53 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 18 Nov 2025 06:40:53 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 18 Nov 2025 06:40:53 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 18 Nov 2025 06:44:29 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 18 Nov 2025 06:44:29 GMT
CMD ["haxe"]
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
	-	`sha256:5da011ae018a3a5def9dfe44ce16be4a82ddb8e454129420b08b546993abcd88`  
		Last Modified: Tue, 18 Nov 2025 06:45:16 GMT  
		Size: 1.3 MB (1257972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697f653268f476749a2c79682200d61277aec08de333a6258099df761ff77af`  
		Last Modified: Tue, 18 Nov 2025 06:45:16 GMT  
		Size: 1.4 MB (1419899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970003b0385caaecfc92f15b1652f5a4756fb6b1bf5064a35caaa07cb50e44b1`  
		Last Modified: Tue, 18 Nov 2025 07:26:35 GMT  
		Size: 262.4 MB (262361583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:1274777522d3d14472f2f09771b45ad0eea50143e8dcdabc3e387c7317a7e9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d804320b3fcfb463cfc249a8d6a1b0dcd6a5edb4a8cb0c57899ed57642fffa1b`

```dockerfile
```

-	Layers:
	-	`sha256:e3164a893f9d5ed4ba7c767a127892f0d92c6bd28b59f192f0e2294170fac0c2`  
		Last Modified: Tue, 18 Nov 2025 07:26:13 GMT  
		Size: 19.3 KB (19297 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.26100.7171; amd64

```console
$ docker pull haxe@sha256:6a14fb1f26486c36942958ad698bf0feaa40f7303c8f013db22b890c71adbc5b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3265418278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184017e4e91caddc958b3a94c734b955e2117beb45ff3dc68d8787a3708c51e8`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:24:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Nov 2025 19:24:40 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 11 Nov 2025 19:24:41 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 11 Nov 2025 19:24:41 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 11 Nov 2025 19:24:42 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 11 Nov 2025 19:24:43 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 11 Nov 2025 19:24:49 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:25:08 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:25:14 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 11 Nov 2025 19:25:15 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 11 Nov 2025 19:25:27 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:25:27 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 11 Nov 2025 19:26:30 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:26:36 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 11 Nov 2025 19:26:37 GMT
ENV HOMEDRIVE=C:
# Tue, 11 Nov 2025 19:26:42 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:26:49 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 11 Nov 2025 19:26:49 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3ac4338ff2d7cd4467062333d5da9606afdfa7168155dfb3ba3031e994bbd4`  
		Last Modified: Tue, 11 Nov 2025 19:27:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ab8b0246d2fc6e0faea84f188da6146bb464b34ec715448129cec27acaac71`  
		Last Modified: Tue, 11 Nov 2025 19:27:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84118473cfaaf22a89c3dc562403e9b2e3578f07406c7c401b2b3f57f6a82fc5`  
		Last Modified: Tue, 11 Nov 2025 19:27:10 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d161c51cc38d67687e0645127e85fba8c97edb9774df72b47c14656c9822267`  
		Last Modified: Tue, 11 Nov 2025 19:27:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d5bf84bef7667f9646909fe7b4cee2d5b9874c5886b3581ac30e904422dc2`  
		Last Modified: Tue, 11 Nov 2025 19:27:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915b4c035ce536e74251385cf067fcb97f47ef4da0d2105aa43b3b3ee40f72`  
		Last Modified: Tue, 11 Nov 2025 19:27:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a580e878dd4b42b55a4edb3bee287f8f6829b8a4083b93a4911c37d170195ab`  
		Last Modified: Tue, 11 Nov 2025 19:27:11 GMT  
		Size: 357.1 KB (357061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec6a48bb8841f456fbac762d08031e35655fcd6986aeabef412b90f87f407e`  
		Last Modified: Tue, 11 Nov 2025 19:27:11 GMT  
		Size: 12.9 MB (12921054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbb4ef4b4c672880eeea6a1f92e8265426a50443a9bd7f366325ec4f55532ba`  
		Last Modified: Tue, 11 Nov 2025 19:27:11 GMT  
		Size: 363.1 KB (363122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfff3f89c5e8690c52460e3567a370c38f26ecc9087bdbb99c0a3a3cf29b142`  
		Last Modified: Tue, 11 Nov 2025 19:27:11 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f361d9fb2bbf393e84b40e559682e42424bb494400b2183719145913029cd0ab`  
		Last Modified: Tue, 11 Nov 2025 19:27:08 GMT  
		Size: 4.4 MB (4382133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbacdef6b750fdd8fee9e58cf9d4f6eca458f23a92be4b2752de35bd949419c1`  
		Last Modified: Tue, 11 Nov 2025 19:27:07 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0106d7eccb037e9afa051517aab5c9a3009b590594bb1fe05b0971445c710bfc`  
		Last Modified: Tue, 11 Nov 2025 19:27:09 GMT  
		Size: 10.8 MB (10832298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ca41be62150634cf37b92b8fe0b3bd523cf2d70582bf7546293c7575bd9eba`  
		Last Modified: Tue, 11 Nov 2025 19:27:08 GMT  
		Size: 353.4 KB (353356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686c07b5512da4869a9bed007abfa997ddc8ec1173453a7ef4dfd98abf49a474`  
		Last Modified: Tue, 11 Nov 2025 19:27:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f203bd59e9cb3abd87cb330343e243ecfc90a2c50478c50907ed07ab29ec47a`  
		Last Modified: Tue, 11 Nov 2025 19:27:07 GMT  
		Size: 362.3 KB (362340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7284ed6bad89ef6653d6102dba2bd4a858a40b42666063e157af0aaaf402b6c`  
		Last Modified: Tue, 11 Nov 2025 19:27:08 GMT  
		Size: 378.1 KB (378054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a107386ff6636cd5f6616206d2c1134ee0bafe674d439f5206b7f6c1d6c9db87`  
		Last Modified: Tue, 11 Nov 2025 19:27:08 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.4405; amd64

```console
$ docker pull haxe@sha256:32735e7a6abcdb4187287cb7ab902fd3793cd8bd0da1bdb8fa78301350ff2afd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1800177521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eae60d743bf71bb5a9add6ff53775a25441d85a2d8cc31990d32980d8679211`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:21:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Nov 2025 19:21:59 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 11 Nov 2025 19:21:59 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 11 Nov 2025 19:22:00 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 11 Nov 2025 19:22:00 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 11 Nov 2025 19:22:01 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 11 Nov 2025 19:22:07 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:22:26 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:22:32 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 11 Nov 2025 19:22:33 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 11 Nov 2025 19:22:46 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:22:46 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 11 Nov 2025 19:23:56 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:24:02 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 11 Nov 2025 19:24:02 GMT
ENV HOMEDRIVE=C:
# Tue, 11 Nov 2025 19:24:08 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:24:17 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 11 Nov 2025 19:24:17 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291d602329acab85d3ee064a4257428aa4eb5ce7707134d2630f8b68bba8577`  
		Last Modified: Tue, 11 Nov 2025 19:24:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8408fbd6231871a771b867717a83bda3a90319014c9a579b8e2eb04b1b757ccb`  
		Last Modified: Tue, 11 Nov 2025 19:24:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757b08c301a27a91a3297a632fc9211dac9b1acb4791f45ba181579d3d675568`  
		Last Modified: Tue, 11 Nov 2025 19:24:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35548427dd655b02ef317610dcb7882b0c30cc9a9387dde0d584f45cacde109a`  
		Last Modified: Tue, 11 Nov 2025 19:24:36 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293c28a8b1d2283bd6f01078bfee463bd76c6f1d1b35b307f14205af6d332161`  
		Last Modified: Tue, 11 Nov 2025 19:24:36 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c199c6225860532c8e258cb1f47f844da4796b1a73706ced6c79b2f2b39a835a`  
		Last Modified: Tue, 11 Nov 2025 19:24:36 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca233a77a7333fef0fff97537caaf27653ddafaba57efe8510d639d360c7a9d`  
		Last Modified: Tue, 11 Nov 2025 19:24:37 GMT  
		Size: 498.3 KB (498322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45cdb9357bf8fdd1b7799b5aad22400163cf3a0e78738c13171eee51c73a3ef`  
		Last Modified: Tue, 11 Nov 2025 19:24:38 GMT  
		Size: 12.9 MB (12932658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde068806f79e4b9d3fa085e1875d22821e59d96520bf1e57ad2869749cdb196`  
		Last Modified: Tue, 11 Nov 2025 19:24:37 GMT  
		Size: 377.6 KB (377619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943850ada35864632491dafe27d42a18e08f7f9b6fa220f372d249b1770fee3b`  
		Last Modified: Tue, 11 Nov 2025 19:24:37 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc77849d3a2c05228aa21112bfff2fde1cb71bda6a8ccc191de090c338d3fff5`  
		Last Modified: Tue, 11 Nov 2025 19:24:36 GMT  
		Size: 4.4 MB (4394721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94dea02eef70f7646a5cc9d77d7b0315a6dd09ec0040f34d6f00436062d19f3`  
		Last Modified: Tue, 11 Nov 2025 19:24:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b10969f3d39a696e5b2350a62f7613fb8c2fe764ba24381479c97b7d3d4325d`  
		Last Modified: Tue, 11 Nov 2025 19:24:37 GMT  
		Size: 10.9 MB (10851510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc890e14142870c0b7dcc2cd8044f286df05866180b5c7808c772fb38fca4f97`  
		Last Modified: Tue, 11 Nov 2025 19:24:34 GMT  
		Size: 372.3 KB (372343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537dd80e41ad5485db5920e579105b974e32cf3d189e331fe78f47e088c0bdd1`  
		Last Modified: Tue, 11 Nov 2025 19:24:34 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc061f1ab6161b53d5a4a3b372572868a87e78f1035ae54a0816b934df01ecf`  
		Last Modified: Tue, 11 Nov 2025 19:24:34 GMT  
		Size: 381.3 KB (381310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5966bbfa0d02e54f0717e26f7ace71d1a83b4546d2f9046bf54b6af8f0c19db`  
		Last Modified: Tue, 11 Nov 2025 19:24:34 GMT  
		Size: 394.4 KB (394392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02943c1eb6918bfc637850373f407f8fd8f5bc215412e245665dee32f7837d11`  
		Last Modified: Tue, 11 Nov 2025 19:24:34 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
