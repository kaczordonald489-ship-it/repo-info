## `bash:devel-20251124-alpine3.22`

```console
$ docker pull bash@sha256:50532b3035b6034ed7535f4d2ecddf47ad4ae452b00ffa614002f4bf47602f28
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

### `bash:devel-20251124-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:a289aef6c9d28b3e9744ef09f71d65db81e6be9572978a88f948b198d8d4f22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6805883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55be7d352f9b2116e868c048438f1933974b7491dade3751074b893b49fc995f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 17:16:55 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 17:16:55 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 17:16:55 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 17:17:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 17:17:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 17:17:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 17:17:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f1ac083f6e0add6dca9de22e6a77512ee3e647e707c5c0ad4b51541021bbc`  
		Last Modified: Tue, 25 Nov 2025 17:17:41 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3669170cd5320773cc3a38fbbe79d4a5010d49222809064d6ffd65de6da356`  
		Last Modified: Tue, 25 Nov 2025 17:17:41 GMT  
		Size: 3.0 MB (3002641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f504413deadc75da40b8d9963de9d3a201d74bbd9b06f60766edcf273defb1a1`  
		Last Modified: Tue, 25 Nov 2025 17:17:41 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:28999243dd1702cb5c64406c8a4c5e5bc7a3ba9b492e8abbdbc53a3e56720ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cec35974e6c0332f26cdbb7f33b4711ddeb17aa473976a227f4c1d42e312bb`

```dockerfile
```

-	Layers:
	-	`sha256:9309952034e59a8471367c8c5691817dfd93b0856b70d0890dba5458ac93bab8`  
		Last Modified: Tue, 25 Nov 2025 19:02:40 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b712474930d2294dc73417594fc34981f8d18e741530103892fd82da2e7fef14`  
		Last Modified: Tue, 25 Nov 2025 19:02:41 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:26a245a85039b6c613da8ab63027843d623f41cd70d40bd9928978c5b2e2c326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6445892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3133cca9e652afbe70cb28e2f901e3b14636452efa211fa4c8d32ab7b198757`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 17:19:40 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 17:19:40 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 17:19:40 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 17:20:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 17:20:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 17:20:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 17:20:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2c491e661a082b893f817759053ca3f3d3b66a7ea5950fdb5890e594fdca3b`  
		Last Modified: Tue, 25 Nov 2025 17:20:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d38bb0699d10a7a516e5e9399ee011a14ca061700160984df17f60a6df1bdc`  
		Last Modified: Tue, 25 Nov 2025 17:20:33 GMT  
		Size: 2.9 MB (2941015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a1185ed01eb0e48f8ef66a5169b2bf1d0f850d30baead3b9cc6e3535c68344`  
		Last Modified: Tue, 25 Nov 2025 17:20:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:be5b90d9aa4f7363f18a520799f7aac8f386d934e8ca5f61dad309a71ba33ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea327053fd64de8c61f3b1aae04b3c23057cbc334bcba8ff104bf60e3627b031`

```dockerfile
```

-	Layers:
	-	`sha256:0c0b4a66ff4b0268b2e6ad68c81cc4680ed77f9ebcf3ba02419886f975a380a5`  
		Last Modified: Tue, 25 Nov 2025 19:02:44 GMT  
		Size: 17.9 KB (17909 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:4c571479ad43f3ae0ebdec7fb9ec1ae1f8ac877594f4d4b4a85d249b8f343fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e71b44200b23f7eb0fb795b62a12fdafae46cef649e69df3a97220ab90bad67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 17:19:47 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 17:19:47 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 17:19:47 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 17:20:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 17:20:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 17:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 17:20:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27196927407a6292b5b2ab59f13375f6b27cbecba69b6972eccb41fc4ba24af9`  
		Last Modified: Tue, 25 Nov 2025 17:20:40 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3eaccb313eef06ed710aa986310f3096b20cb5c80a921908d032931240e6b5`  
		Last Modified: Tue, 25 Nov 2025 17:20:40 GMT  
		Size: 2.9 MB (2892146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9af3e1b5fc42f4013eeb581cdb75a9f61e63ba23562fefc6f20522c74b6e4c`  
		Last Modified: Tue, 25 Nov 2025 17:20:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:887f095c78a91596df4598fc3ea1ad8a26f18bb16a43cff26b6adcab18a013b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a032bd78930aff57cb47aec9698dd16918f172eb5b360e1304ed13a461c07e6c`

```dockerfile
```

-	Layers:
	-	`sha256:713dee80b403159f68d64e2b6cbab57dfd18952ab968f55662ecd37c83c2eb81`  
		Last Modified: Tue, 25 Nov 2025 19:02:48 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301200f97a5a4979d133eb94a51887fd616f853ddd00fc76e5e5025784f66184`  
		Last Modified: Tue, 25 Nov 2025 19:02:49 GMT  
		Size: 18.1 KB (18124 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:745f22e88e24180e378db6e588af02c1078d5c6dfdb6da1f2efc0c8f521b24c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7231385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccefb77b9667f6be8b9b94f369e1e6e61bbce7ab22f0840de96733e740802ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 17:19:56 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 17:19:56 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 17:19:56 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 17:20:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 17:20:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 17:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 17:20:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3460ce729f7101cb0903d18f1b00879fe69d42cd52936f306a7f301f9c91a2eb`  
		Last Modified: Tue, 25 Nov 2025 17:20:47 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb3d494638b15facc9d4f6a179ba86fe8224c3444122663467986bc7659439`  
		Last Modified: Tue, 25 Nov 2025 17:20:47 GMT  
		Size: 3.1 MB (3092520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2222440572f84191b5f0b2f3f433f83f22cd97de64d8badcf016f1e04f87288`  
		Last Modified: Tue, 25 Nov 2025 17:20:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:c94cb8e0650717c0b27e387d70968423b1d0c9e216697cff19515093e1b9129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f97d556fb81305f137aa3f7a8422eae0135cc1ef4b9050daf3b5cbcf5a07289`

```dockerfile
```

-	Layers:
	-	`sha256:7461a05e7e8cc7beafd8126b94f889acb22ef125611b3d81b03c1e60b9e5972c`  
		Last Modified: Tue, 25 Nov 2025 19:02:52 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14c9e6d570c6330075060518c4de348b63e133c8c6a341a454028481aa80a135`  
		Last Modified: Tue, 25 Nov 2025 19:02:53 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:299158478b3ecbc45b9c8d2dddd9cd6bb094f44c2c7a498705ea31023811c175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6548479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea96f78f6f8b35f297c6368c10dc314c0f16a76af7f93dfa6c5d61c9572720ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 17:18:26 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 17:18:26 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 17:18:26 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 17:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 17:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 17:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 17:19:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df213022b8d3019f9817cbc23932d0247af9fa5c8523fb8c4219a908af47ad8`  
		Last Modified: Tue, 25 Nov 2025 17:19:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c380f861ae5f5a80e86073bff0cdc4332e8bd036539baa36a367cf0c7fc7078b`  
		Last Modified: Tue, 25 Nov 2025 17:19:27 GMT  
		Size: 2.9 MB (2928754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351a7f3407b71cb6ecb327830a748bc0ccd89688cf4e3f2ac9dfdc1019c17bc0`  
		Last Modified: Tue, 25 Nov 2025 17:19:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:8050db8523235753b270f4aec12605e63fea6c4b5f4ad6ba8e7a54ed6ef95fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 KB (136416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b9d5211e36115ecb6a2a14ee12d51a8880202fd2f18ca2aa284369528f2f09`

```dockerfile
```

-	Layers:
	-	`sha256:62a37dbdf56fdeff4cc81a740f0dc6556dc6a425c7dbb8d02a5c56a44057a56b`  
		Last Modified: Tue, 25 Nov 2025 19:02:57 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749abf0df4f959f6f4e6a2c59c1266ee3711d96c2a1e2203961fcd365e5adfb8`  
		Last Modified: Tue, 25 Nov 2025 19:02:58 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:9ea86bd1252f7ad23501a7205ac14e1487d45aed36b1fac9e05aceac3e043c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55de72fbc6f4a9431af163f89b9ba35c660ee82c7b0a001c325790b4a60635d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 17:52:59 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 17:52:59 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 17:52:59 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 17:53:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 17:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 17:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 17:53:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c24b7f3adc8d32ad502b1d7acb87f6ab791f9cce1766a5703396a1b7379b0d`  
		Last Modified: Tue, 25 Nov 2025 17:54:08 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad19f782e73441df7d45aab44d6f49e14837fe6a5ca3f10d4c46f95c5617c619`  
		Last Modified: Tue, 25 Nov 2025 17:54:08 GMT  
		Size: 3.3 MB (3276541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e20bbadcd6dfb3e6d095bb0b4d4fdc82e15bc25591820493b8822a390d1886`  
		Last Modified: Tue, 25 Nov 2025 17:54:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:306079821cfded04771111117f11f133852ec32353d899d198c82f993deba72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8405d5ff9985cbd200704d307d9973b0aeb7d6bbb334d0e8fd325b28f00ed467`

```dockerfile
```

-	Layers:
	-	`sha256:2106df7e5f804647ad6bc319cca371e8d8abbc3d730864243166e2d9792d3546`  
		Last Modified: Tue, 25 Nov 2025 19:03:05 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f3eae087d69ca71a6e96c1f36c53e06d9ec655fe1101b9eb2a4dce47f6fa85`  
		Last Modified: Tue, 25 Nov 2025 19:03:06 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:5a16531779dfe87506e6b1d374a55065243a9006f5a28eb8e87fdaced1eba773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d1094438bf8a2e4f861f358e992a328230890634936e7af10a2533fcbbcb38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 22:38:41 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 22:38:41 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 22:38:41 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 22:47:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 22:47:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 22:47:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 22:47:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b0f06ae856cc95996ee125f077b427f1f6974324aacbfdffc84afc6c2e50cc`  
		Last Modified: Tue, 25 Nov 2025 22:47:35 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2817ac6116b51d920dfd4505a1daf9540cc6012a87c1bec90db54588e3957464`  
		Last Modified: Tue, 25 Nov 2025 22:47:36 GMT  
		Size: 2.9 MB (2949497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb1b6ffbbcc47f5eeb585704e677b2c7e0651ce3b5cb2fec23a19a1934410da`  
		Last Modified: Tue, 25 Nov 2025 22:47:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:2967fc30bb2ce2c0991a8f3cbb9d434f6bf589b7b6e0d4dabb0c223597b30b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d31e97c696a5b46b3d933f589f3985d5f13d4c350ed92c63b13ce5fee3a6e4`

```dockerfile
```

-	Layers:
	-	`sha256:cb21d3e27eca44a3b8c8d3eede1dc703ad030cd7553953ec048f5fe9f5f5f78a`  
		Last Modified: Wed, 26 Nov 2025 01:02:36 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7eb04d719b62f9490fca3fa661eb38caf3d46ac425a6e49398d4dec5d6fb9f`  
		Last Modified: Wed, 26 Nov 2025 01:02:36 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:e0a730525d667beb076248e54b2a705aa1bd6c9082505f0fdce827a4458a390f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6742644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762eee12c025de8d3dc922116d8beea93071ad464afa558089b8358a9030eaf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 17:23:42 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Tue, 25 Nov 2025 17:23:42 GMT
ENV _BASH_VERSION=devel-20251124
# Tue, 25 Nov 2025 17:23:42 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Nov 2025 17:24:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Nov 2025 17:24:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 17:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 17:24:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4aecbcb5c66e435e72c137940940a0016f6e5543120d190f2abb9bf3f7918f`  
		Last Modified: Tue, 25 Nov 2025 17:24:34 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c8fd3b56fedd71e10bee02fa83833280379f6b53d32f096e380a78531ac1b8`  
		Last Modified: Tue, 25 Nov 2025 17:24:35 GMT  
		Size: 3.1 MB (3092611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3183cf82264c57ecd5981f9de1fc4d6d1da2bb979c2f0495bcc4c4e929df8b27`  
		Last Modified: Tue, 25 Nov 2025 17:24:35 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:e75df4b741f6aeb7b412fdac4fc3b9987ba40dca497752dad99ece123065a676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308658ab05e97bff60ec85d74a226858eb217151c71602f846b322f74d4fa29`

```dockerfile
```

-	Layers:
	-	`sha256:8bd17298330221fb0fe8c82fe4d662a763e37889984fbd71d2d6173c4a89fdf0`  
		Last Modified: Tue, 25 Nov 2025 19:03:09 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7f5dfb53fbb65103b203d03b0e823dce912de95f79a211ea98ba217734d48e`  
		Last Modified: Tue, 25 Nov 2025 19:03:14 GMT  
		Size: 18.0 KB (18042 bytes)  
		MIME: application/vnd.in-toto+json
