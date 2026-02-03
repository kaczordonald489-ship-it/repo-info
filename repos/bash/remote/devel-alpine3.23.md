## `bash:devel-alpine3.23`

```console
$ docker pull bash@sha256:6617eab7044692fa977942f9a3edd9dcb12fc0ddc5019e3fe209f53e13fd761a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:8fbe4a527f10b3505182981c30fe8d79a1e5a20a242bfc413633f26e323f222d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6886509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc58289e81dc03bc1c714107ad3100d48e3c47de1e6a9268c4f975e90d5d516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:33:39 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 18:33:39 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 18:33:39 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:34:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:34:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:34:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acb769f612a28a61fb41fb75019e75dfd173c722d5805d2de8b8009ae12b23b`  
		Last Modified: Wed, 28 Jan 2026 18:34:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e61d114edc01266ded8873c32f6573a652852f2b6e804c82c932be8c32d28d`  
		Last Modified: Wed, 28 Jan 2026 18:34:20 GMT  
		Size: 3.0 MB (3023900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b148c4afbed8e3968c720fed8fe34cab57dde6c398d7b99fe9732cd71620627`  
		Last Modified: Wed, 28 Jan 2026 18:34:19 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:25a22de72028eb3184db959ffd4a47e287f5bd2b40b99e7121afbdaaa0f7915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5cfbf522eb3a5eeaa2189b5d42f80ca7167459e694dd84eb447b7fe5cb6ebb`

```dockerfile
```

-	Layers:
	-	`sha256:e89e72b03d2f3ed54f4d0b1ecbcb8dca6ca26d9759cf6a171e4f5ea4939461d5`  
		Last Modified: Wed, 28 Jan 2026 18:34:19 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a3cb98aff2fbfd8ad097c9fe317ec040271bf7f75ef94d63c17ae2c00a27c8`  
		Last Modified: Wed, 28 Jan 2026 18:34:19 GMT  
		Size: 18.2 KB (18164 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:52395ef74a42844e8e0575b7c400f52ee701d5c0a78a242ea4f21fe0299bc86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6552627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1672bf3434e01e53ae87f7f6202795babf157f147682dce8145071ad59d64af6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:33:53 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 18:33:53 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 18:33:53 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:34:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a0cba14f742f1555419529617df4c8546063bd2180238f147979878a9d417f`  
		Last Modified: Wed, 28 Jan 2026 18:34:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea62a5d0a426f700bc7660acb816abc43e28cf909047862e1c6be608d4ea579`  
		Last Modified: Wed, 28 Jan 2026 18:34:41 GMT  
		Size: 3.0 MB (2982018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c51eab315454e7233641b0b270d46c67cb49cd261e6d4789f7dd40edb568c9`  
		Last Modified: Wed, 28 Jan 2026 18:34:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:40277a426f65a57e56e23d85735d3d0a15daa50fb2eedb76f4e792b0cc91bd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca25e481b1b6669b16e0e97bffb9bfe12fe99526406553cc4c30d9417d59cd2`

```dockerfile
```

-	Layers:
	-	`sha256:26b3542f34d03cbc10421f95b5113ff114cadfc40ca3703ca11b10a25419a39e`  
		Last Modified: Wed, 28 Jan 2026 18:34:41 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:f8492bab4d22d120519024bb40643bf4c03a8bbc1121232693d71d5745ee0c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4151c0ae9886b6ee3a54af9aa1870d15d3217399935867f07e058c0d77437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:33:55 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 18:33:55 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 18:33:55 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:34:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:34:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5511225e8fc731f5d297aff91da283288c514880e4e6c2f4d93006042344aa`  
		Last Modified: Wed, 28 Jan 2026 18:34:43 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56cf563e3c954c098763a02f70b64969bf0ae2d61f9cb13895fc662f9096a4d`  
		Last Modified: Wed, 28 Jan 2026 18:34:43 GMT  
		Size: 2.9 MB (2931995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab02ea4be7e6247c1bebd21e767f37a162e3eb73f68e2265673298326a64dd`  
		Last Modified: Wed, 28 Jan 2026 18:34:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:3031ce0d1a313b8c1392abf02fcbe79199d0f69b5032e314fc342a76ea520a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08672dded70a136d8d3dcc10a425eff23e267ac080df5eed317a09228e04f98`

```dockerfile
```

-	Layers:
	-	`sha256:9daf538bdd9c8cad6e64227c48e226ced17ce2b85f22eabcdce83048d6fd7874`  
		Last Modified: Wed, 28 Jan 2026 18:34:43 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be1c9573bafed9899f9c4619bcea95e11e175e6814553b290834c8f7bfbf54d`  
		Last Modified: Wed, 28 Jan 2026 18:34:43 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:03b93af87cdbd26ea5e6633c1e1290e2d02f27a77bc9723218dd61fa5954743c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7292392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca2c0df2f806ea5af3d7ad944c8bcce732c997e592d92b8d31a2703bcd286c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:43:10 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 18:43:10 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 18:43:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:43:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:43:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:43:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f97699e79612171d01f1ee1218568390c639a3ce63cf2855ecc0d5136ebed6f`  
		Last Modified: Wed, 28 Jan 2026 18:43:55 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab285021fc246de035351e39fcb987f14a18c9498d953b29881aa9712074960`  
		Last Modified: Wed, 28 Jan 2026 18:43:55 GMT  
		Size: 3.1 MB (3094507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a31581d937d095b9bc123bea217e0a46874fd526ff33443be387aa03725a8f`  
		Last Modified: Wed, 28 Jan 2026 18:43:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:b4184f9973324e091a8fa16f88ddde0cbf2b9412eb8de68f55c9f4f00053345b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f219ded9a08950bb52a0ad5a0fd70949f9104ba5dc248bfad2d28d9c439c4f`

```dockerfile
```

-	Layers:
	-	`sha256:ef53b61b9124c54e4163ec6fe990eebc51308a02ef127ae81b7429509c51b55b`  
		Last Modified: Wed, 28 Jan 2026 18:43:55 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b94d0716154e2ecd8be61c9b89adbd78fee89b39147e61e98d43842d4083584c`  
		Last Modified: Wed, 28 Jan 2026 18:43:55 GMT  
		Size: 18.3 KB (18268 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:a716a0750e92e5387e7f9f79a1792da0fcec8a80280f015cc21e88626b192f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6638036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf963c942a761702cc2452e4955420e21d9b21ef778e32a610a32c039b0d5a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:34:08 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 18:34:08 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 18:34:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:34:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:34:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:34:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b5548f689ab0afcd53a64470d89f503736b1b9a8125e35dbb40f99fa87fdbb`  
		Last Modified: Wed, 28 Jan 2026 18:34:51 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ec8ce1c23c3ba2a43bc13b3c012182cb49e2087815607227a5e0ee24d60623`  
		Last Modified: Wed, 28 Jan 2026 18:34:51 GMT  
		Size: 3.0 MB (2950252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16fddbf1e4bdbb032b888401c56d42863666455e6deabacbf9f7a22c7f9e3a8`  
		Last Modified: Wed, 28 Jan 2026 18:34:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:e329e01eea5b63b108e8ca887b4c061f162daccd2bdcfd4a5b771f9ce29e6957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048ea6b70e7c53a70e1d3dbfa76b4c9142abf3f8a0b4ad45e3e83371cba717ad`

```dockerfile
```

-	Layers:
	-	`sha256:60ea99b233df0b0adc4f990ef1cd58529b8f1a5227905c3eb330f3e1718375b8`  
		Last Modified: Wed, 28 Jan 2026 18:34:51 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70f9fa3fcfe3685d7c453d19c994ba2fddfaef2d0ad5cc0b77e9d711ce4f93b`  
		Last Modified: Wed, 28 Jan 2026 18:34:51 GMT  
		Size: 18.1 KB (18132 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:2855f3e1bb994864329f58e72628cbb5fbef07fdfca063bb35ca0ad13c2785c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d8e65f6f7ffebdb5879f27efce776c9f7502a4c880e8a5c02913acc44a340c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:12:14 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 02:12:14 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 02:12:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:38:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:38:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df562137f442ce368a20fd090a2aee8c61c51133b0500c9b70a1c208a23adb`  
		Last Modified: Wed, 28 Jan 2026 02:13:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edecbd651eb0ff5f4c88718645fb99e80120615f2124090244de172f50da2452`  
		Last Modified: Wed, 28 Jan 2026 18:38:58 GMT  
		Size: 3.3 MB (3332677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fa1373bab11ecf768c1e91c2a7f85e868e6a480bd96210b0e53fd9c8171a5b`  
		Last Modified: Wed, 28 Jan 2026 18:38:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:118b010f75b303899e7ca56d06f805bf5d3b2fe180a182f038cebdc8bf71f6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da14b64972818e9f61f78496d5740817b15ee3b4809d0c8cfd344d7ae5a23fd2`

```dockerfile
```

-	Layers:
	-	`sha256:c1a4104628f8d3e1bfdddaeb127fcc319ef0d8fb28ee4ff6adfdf1b0a96dfaf0`  
		Last Modified: Wed, 28 Jan 2026 18:38:57 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5d9a95469e10874d0702c7a8252071d4647d462aa309d35fe48c9bb6d4de8d`  
		Last Modified: Wed, 28 Jan 2026 18:38:57 GMT  
		Size: 18.2 KB (18207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.23` - linux; riscv64

```console
$ docker pull bash@sha256:d7dacb5d2cdfee4b0d75afea0bdc387a9d1c04153d39baee9ec853cbbe16704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6799309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13491eeecf751f9a55be83350934a298f331001dc2b649eccd431f5e8cab44ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:17:11 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 04:17:11 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 04:17:11 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Fri, 30 Jan 2026 18:17:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 Jan 2026 18:17:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 18:17:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jan 2026 18:17:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0540f5e7cbbd06be9591105e336b004c6e351dc53f24f7df485f56578662b1b4`  
		Last Modified: Wed, 28 Jan 2026 04:26:38 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ffaae1805215a6b3be4f6119f35888f3344b419b7f3af56e69625446a86949`  
		Last Modified: Fri, 30 Jan 2026 18:18:12 GMT  
		Size: 3.2 MB (3213221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb27a8c065c4964a468af5094d7107bb2569d2c2c9f867432ca01ad1f59ba2`  
		Last Modified: Fri, 30 Jan 2026 18:18:11 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:3002e373749aad7fd6bc59977e729bf9ebdd3e2b00aa501467ccdcdaccbcb18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba41d4db8eb24404bfd8677be3f41efeb6d411881cad65bb4bfd2035a7d578c`

```dockerfile
```

-	Layers:
	-	`sha256:8195a4e4c17ad0bce5c770eb3fa87599546367c9fd5ef7add1a8f1de658e4e0f`  
		Last Modified: Fri, 30 Jan 2026 18:18:11 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563154a110355103f295bdfdf1349f86bbb12483e658dce469eeef2f99cfb201`  
		Last Modified: Fri, 30 Jan 2026 18:18:11 GMT  
		Size: 18.2 KB (18207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:94e3303614cfd301cafc7e849859f339cca5c04a1bd79bb8802eebbfb4d82818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cceba4864c41db901520bc50ede7a911694eb517dc70c49c92380cca3d21702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:12:15 GMT
ENV _BASH_COMMIT=b805bbec801b3ac9adf1e67707b2d5bd3da9e60b
# Wed, 28 Jan 2026 02:12:15 GMT
ENV _BASH_VERSION=devel-20260123
# Wed, 28 Jan 2026 02:12:15 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 18:33:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 18:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:33:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f34932483ae323b9c0468361629e1e26fb7403cef6d4353f0f81140eed823`  
		Last Modified: Wed, 28 Jan 2026 02:13:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919f1e1acb6ce659a26e5d66c83b27ae8b4c33f24d9c32ec7bc36c5326ad2794`  
		Last Modified: Wed, 28 Jan 2026 18:34:03 GMT  
		Size: 3.1 MB (3116744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a266c04e10a913cdc81c8c743d383d490b8f5f6718a9238ca2ca74c6699965`  
		Last Modified: Wed, 28 Jan 2026 18:34:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:4cc3069cd25d78d2b2ca8e9068f2ba9511881ff9f5b0f205364e500ae4e7a1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fabd6c424018d9d0a0e2b02473244b89ec1f263785a0e0fd5a4dd9ee44e2434`

```dockerfile
```

-	Layers:
	-	`sha256:abf0cc94fef505910a14a3a98669c98d459725448474d97827bd4338a25c6c37`  
		Last Modified: Wed, 28 Jan 2026 18:34:03 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60518f957402f355d43aa72ee4a92b5572e8cb72bd9b4cc7a3789ebd18984c5c`  
		Last Modified: Wed, 28 Jan 2026 18:34:03 GMT  
		Size: 18.2 KB (18164 bytes)  
		MIME: application/vnd.in-toto+json
