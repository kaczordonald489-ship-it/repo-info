## `varnish:alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json
