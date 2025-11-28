## `nginx:1-trixie`

```console
$ docker pull nginx@sha256:553f64aecdc31b5bf944521731cd70e35da4faed96b2b7548a3d8e2598c52a42
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:1-trixie` - linux; amd64

```console
$ docker pull nginx@sha256:5c733364e9a8f7e6d7289ceaad623c6600479fe95c3ab5534f07bfd7416d9541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59751534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60adc2e137e757418d4d771822fa3b3f5d3b4ad58ef2385d200c9ee78375b6d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:24:11 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 04:24:11 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 04:24:11 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 04:24:11 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 04:24:11 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 04:24:11 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 04:24:11 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 04:24:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 04:24:11 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 04:24:11 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 04:24:11 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 04:24:11 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 04:24:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:24:11 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 04:24:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 04:24:11 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5feb73171bf1bcf29fdd1ba642c3d30cdf4c6329b19d89be14d209d778c89ba`  
		Last Modified: Tue, 18 Nov 2025 04:24:28 GMT  
		Size: 30.0 MB (29970454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ab82928207dabd9abfddbc960dd842364037563fc560b8f6304e4a91454fe`  
		Last Modified: Tue, 18 Nov 2025 04:24:26 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d743880af45adf9f141eec1fe3a413087e528075a5d8884d6215ddfdd2b806`  
		Last Modified: Tue, 18 Nov 2025 04:24:26 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa2eb0631772679b0e48eca04f4906fba5fe94377e01618873a4a1171107ce`  
		Last Modified: Tue, 18 Nov 2025 04:24:26 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192e2451f8751fb74549c932e26a9bcfd7b669fe2f5bd8381ea5ac65f09b256b`  
		Last Modified: Tue, 18 Nov 2025 04:24:26 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de57a609c9d5148f10b38f5c920d276e9e38b2856fe16c0aae1450613dc12051`  
		Last Modified: Tue, 18 Nov 2025 04:24:26 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:af320b2df7e2bde33bd04165a7cad0b510f6ce6461d8f2e9c906fc77f99a8d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f8f863909e788aea1f4a99cdcd5c7d8bb6a4f2a926233d898aa75c112c82d9`

```dockerfile
```

-	Layers:
	-	`sha256:137b08466659d5ec7645a6ff389e0cdeade6563ec57787e4fe4ecbffc87859bd`  
		Last Modified: Tue, 18 Nov 2025 06:51:07 GMT  
		Size: 2.8 MB (2811745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43536266b8d99fcb59e2cfa3d1e43f772f66dd4fa4a9f7c1b8df0b06158ea76b`  
		Last Modified: Tue, 18 Nov 2025 06:51:07 GMT  
		Size: 34.5 KB (34544 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:62225d274171ff35162681fac1069e005db7bef4bb991d5dadb61d6fc87c9a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51360583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca992b375e221f13113ae45490cdea8ae21a9a2e02800e93ee66ed9f6a2e725`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 02:19:26 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 02:19:26 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 02:19:26 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:19:26 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:19:26 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:19:26 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:19:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 02:19:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:19:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:19:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:19:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:19:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:19:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:19:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:19:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b90ad3261e6e06eeb02c08e3127430aa0620338d67b4cd2f8e09d1294ce3931`  
		Last Modified: Tue, 18 Nov 2025 02:19:43 GMT  
		Size: 23.4 MB (23411837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abdc419c697e0628f8a09b00f81485d7860294210aa01b396b3ef28556ecfb`  
		Last Modified: Tue, 18 Nov 2025 02:19:42 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa006659f427c85ad04276fd51b6f8d3609195f125ca2e69d301734758a1201`  
		Last Modified: Tue, 18 Nov 2025 02:19:42 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1a5cc75b5fa9989389eb5e3f6c3d1297c4e63888b5bae3fb0a47dc8d3e593d`  
		Last Modified: Tue, 18 Nov 2025 02:19:42 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d222ba00958c72d5aa54b6606528c8e208c97e57342a3dffea83cb639a4825`  
		Last Modified: Tue, 18 Nov 2025 02:19:42 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628db4234427b2597227b22168b8796c524ede3e0325c783578ecb8e0e7c6c2e`  
		Last Modified: Tue, 18 Nov 2025 02:19:42 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:95f06ee8444e01fbfdf432b2b37bcc17efda81059415300bb70235ad4516aa55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a29e86a035578bc9c8f3a8c65bf73b0fc09692f93c56c6ed2e26df341ea48f`

```dockerfile
```

-	Layers:
	-	`sha256:54ae97910b27b24f2364eba7c86dfac2127088c4baa6412d5cd83a00c4d84e92`  
		Last Modified: Tue, 18 Nov 2025 03:52:06 GMT  
		Size: 2.8 MB (2837885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a2d93bcffba936a0b8f69afc917abe3557d9ed8e0036206005e9f807cb1b8a`  
		Last Modified: Tue, 18 Nov 2025 03:52:06 GMT  
		Size: 34.7 KB (34672 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:bead225e6794863c992c4c3214e7069f3dbde7e2e3fb03c462499e7c87b678a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49628150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f92e42001a4ad9e0d5630c8cf9b807937267a20ae76e9975551e98671645d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 02:21:33 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 02:21:33 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 02:21:33 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:33 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:33 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:33 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 02:21:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:21:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:21:33 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d7d51f66eca024f2c7045ff925e84209b5ba6caf1f2888653768687f40dc19`  
		Last Modified: Tue, 18 Nov 2025 02:21:52 GMT  
		Size: 23.4 MB (23413594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0e38dd611cdfeac832fe94edd68e7f9feb6a8538c3009e35c62c0e9f9a3853`  
		Last Modified: Tue, 18 Nov 2025 02:21:49 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b72bf0f284152f2aada1cac81dbf1d7c0c06b7b9003cc2a91782b8c723de0b7`  
		Last Modified: Tue, 18 Nov 2025 02:21:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926ea34f053da7815962ae3ce45d1cf461954a14fb4cc410143ae484e130af45`  
		Last Modified: Tue, 18 Nov 2025 02:21:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0225ec98df0f4126431e14cf3169047631135ff3bc2c3a6dedeb1e459d851`  
		Last Modified: Tue, 18 Nov 2025 02:21:49 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a513a6d72ba43405a515fbff9f79e1edf9b1b3670301e938dffa2ed3f59da6`  
		Last Modified: Tue, 18 Nov 2025 02:21:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:24cd250db1cde67fce0ce895700b076b719de887b107651fdbc1cb054dc4e967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8fa7375fd2298783b1c07b9f8eac2bf5451b824d93df4172467528a1acd505`

```dockerfile
```

-	Layers:
	-	`sha256:e6d647c129ac5f6384dad14811ab2d8d09818a73fa87ea54dabe6d10b7c00e11`  
		Last Modified: Tue, 18 Nov 2025 03:52:10 GMT  
		Size: 2.8 MB (2836630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aca3009ff6383692ab4042026c4aa224984a92b063d4e5178c515d87bcde184`  
		Last Modified: Tue, 18 Nov 2025 03:52:11 GMT  
		Size: 34.7 KB (34672 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:7de350c1fbb1f7b119a1d08f69fef5c92624cb01e03bc25c0ae11072b8969712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58242276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb747ca923a5e1139baddd6f4743e0c0c74df58f4ad8ddbc10ab183b92f5a5c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:42 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 02:21:42 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 02:21:42 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 02:21:42 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:42 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:42 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:42 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 02:21:42 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:42 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:42 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:42 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:21:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:21:42 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254fb813b1149e7c70ba8ea22cfe75899b15c372e21b3e3adabc35cec44f53d`  
		Last Modified: Tue, 18 Nov 2025 02:22:00 GMT  
		Size: 28.1 MB (28099072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b6fc5618c6392526541c86c3dc22f3b4547c84336f38580dc8dce6fc8e7e33`  
		Last Modified: Tue, 18 Nov 2025 02:21:57 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ecb62799cacecb49f89c037b18c33bf3ca0a5da1ab1a689bc4bdf5b34f1bb`  
		Last Modified: Tue, 18 Nov 2025 02:21:58 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc57e8335c98a9e86890d182f80ae294350592233a32839df6ec50cd23f24c0d`  
		Last Modified: Tue, 18 Nov 2025 02:21:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a807fe41d8ce16921c14999f94f18d32dbfb7e668c3e8565c1a3011454224`  
		Last Modified: Tue, 18 Nov 2025 02:21:58 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88770be1d44258c5e6a7fc143015a21b7d0de6d4af5bcfcdbcaed57626157fac`  
		Last Modified: Tue, 18 Nov 2025 02:21:58 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:82902e3d23a38265fe3ceb22da1f673a962d11acb40777a671d0a0e65ec7b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bceeabd717a0c87f95f1a93d882aee8fab56625832920dd4d41d3bd87f81a4`

```dockerfile
```

-	Layers:
	-	`sha256:d5fdc9d962cda2b641fac54ca63fd8000012ddda4fcdd25b8d07877dd5c112dd`  
		Last Modified: Tue, 18 Nov 2025 03:52:15 GMT  
		Size: 2.8 MB (2812229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1207165c1c8c237fd14edaa6b714b3ce1b76fd465eea02904cc5f3fa483318e`  
		Last Modified: Tue, 18 Nov 2025 03:52:16 GMT  
		Size: 34.7 KB (34720 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; 386

```console
$ docker pull nginx@sha256:1b8fdfa2a4116c8b19322133670b1feba5b8ffdbdd31f5437296a4a16dd94cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59989760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4642ce60dd28717421680e0a0f03ab3214a67146f75f296e69e70c12574495b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 02:21:30 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 02:21:30 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 02:21:30 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:30 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:30 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:21:30 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 02:21:30 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:30 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:30 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:30 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:21:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:21:30 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:21:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0945b7b95cfdc9e0e539be56208fce1e622bc198b179ff64fb5acf8cd67138`  
		Last Modified: Tue, 18 Nov 2025 02:21:50 GMT  
		Size: 28.7 MB (28692088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c73e661cd631ec45e2f79a2566953a50093d15b2d544dc9b93cffba10353ff`  
		Last Modified: Tue, 18 Nov 2025 02:21:46 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc6dfb70632192b3ee37147b662ed892ef3086f7eb00d7a6b070b817f60aa9d`  
		Last Modified: Tue, 18 Nov 2025 02:21:46 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24edb49c48663feeca0e63590eba636e582ba9c73274fcb24e58d3b2adb3e58`  
		Last Modified: Tue, 18 Nov 2025 02:21:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d3d37d97ea54ae72998fd964a5c57be30bdbfa3f2132de7e0e99922affa70`  
		Last Modified: Tue, 18 Nov 2025 02:21:46 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393cfe3d0bc6d127c26615088a34641e82e3f3630c0daa7b510271eab48e791c`  
		Last Modified: Tue, 18 Nov 2025 02:21:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:74dff7038a51bfb01eab538dbcec85c0f78e9cda415adf751417009111cf96d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1fa6675f7126f074a9492bcf1de1e7886d422e6c69aa909ec616f242b11082`

```dockerfile
```

-	Layers:
	-	`sha256:fa29e383b9f41e3f6b150ab19f6d97139637bedf900b2832ead3bebc39cbffbf`  
		Last Modified: Tue, 18 Nov 2025 03:52:20 GMT  
		Size: 2.8 MB (2831581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae56c6deb39a47eb6f2aae673b88d26d3483591383612a626ece8609563fbeec`  
		Last Modified: Tue, 18 Nov 2025 03:52:20 GMT  
		Size: 34.5 KB (34482 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:a4f9edd24727204b0313b7e6df93bea94b161d29310831df463a2294560064c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63817066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e5cf473ba099b0681c1d1b0f0fdc75f0183d9ee839e15025c3b187f0624811`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:18:11 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 15:18:11 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 15:18:11 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 15:18:11 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 15:18:11 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 15:18:11 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 15:18:11 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 15:18:12 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:12 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:13 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:18:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 15:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 15:18:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d912651b28a1f4550f9027605087cc0b23629661ff2b51880373e625d7ea8`  
		Last Modified: Tue, 18 Nov 2025 15:19:03 GMT  
		Size: 30.2 MB (30215610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbba70b7652397310f840e280558d4e3dc1cca4fb7f3f2d55ad0d3315177121`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee77fdcf2dfb637465abf0fd1d0919e741c1c17d5aeb4336cac727a01de857d8`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b84bf1fb0e81c24876666f7f8042ae7125ae059e487e5c6dcdb6f57e1570540`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c66213f80855923053c67ce2928b6d6944f278d50f258905642b0d31787455`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c1cb8f543bbb52d94639a15b6de03b238f7ce458d6f0d1695847ef82919a5`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:3c8658e7455c4b5fa268c6b7fc3073804b008a774245ea938708675b0ab99e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2e56352c08f5773c055578c4249e8ecabdc6fc2762e4344eabf0afdf57bd9`

```dockerfile
```

-	Layers:
	-	`sha256:541d987323ac4a6d147155db29e06037053dc559b50749e65d4931646c3b8e78`  
		Last Modified: Tue, 18 Nov 2025 18:50:52 GMT  
		Size: 2.8 MB (2839275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:542e041c49117c8c502451c174507632129f1ae75d642f593c1b5e6248ebe8fe`  
		Last Modified: Tue, 18 Nov 2025 18:50:53 GMT  
		Size: 34.6 KB (34624 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:2eca83f563c1b416ec37c092ec3f3903cf17aae8ce65305f1ad219a4e3024231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54686055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3046763668511eee4f4a7b1d9fb676e2c488842245e57076cd64c48dd3d522`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 12:58:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 12:58:08 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 12:58:08 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 12:58:08 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 12:58:08 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 12:58:08 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 12:58:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 12:58:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 12:58:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 12:58:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104bd6b25ed0570faf0ecc12fd9704f33039bbcfdbc9bc1d32371e739d12ceed`  
		Last Modified: Tue, 18 Nov 2025 12:59:51 GMT  
		Size: 26.4 MB (26408325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fa69b7788b2fb7e0c32101b1d39f3fb69d9bf22b60bb613b38fa709901458e`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10d384b97779774109c8339df3bd6d6f2ffad4242bf10bd7ff32806442654b3`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad94d4d1dc40669416aca412d7afde40639919f9d4814f225a46446b3e93f404`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c38407276eceb8594c03684c6358996b55947d883d32bff640bc435d0d0b439`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96363b0a094772c0ae15f9f3f4991c52f15ae87fc8dcfe1274ccc1f97645e0ba`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:3d7cc40ee7ce57cc7afc48ef305e0f3d897581d7e2f9ab9e3876635d727bd886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2863684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5237c858b06e8baba3bcc7235cb005847deea7f61ad850392dab0bb8261c0da`

```dockerfile
```

-	Layers:
	-	`sha256:0354bb9300ea32ab1706200fc61f1dbb8b24306851d68591ef7ae04ae3dddea5`  
		Last Modified: Tue, 18 Nov 2025 15:51:53 GMT  
		Size: 2.8 MB (2829062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b930ca1133f0600dc162ae497f32a81ed17457068768d5883a46d70bd00cf7`  
		Last Modified: Tue, 18 Nov 2025 15:51:54 GMT  
		Size: 34.6 KB (34622 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:0f5d5e7cf211bdc68fb55f67b51e2943533c12da7f4f042d1952b25c76798f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56970929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfe4a0cc8dd6660cf9484d6d539285c6f70fddbf376c9c42795876b04e4e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:03 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 02:22:03 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 02:22:03 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 02:22:03 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:22:03 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:22:03 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 02:22:03 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:22:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 02:22:03 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:22:03 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:22:03 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:22:03 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 02:22:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:22:03 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:22:03 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:22:03 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2df94d5e68e59c65ca957e2204df43cc81b2e06fbb2051e7f282feff713820`  
		Last Modified: Tue, 18 Nov 2025 02:22:25 GMT  
		Size: 27.1 MB (27131956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8782d19d780bb02b338c35936ae274a77ca56f962d60e91251c25d529379d655`  
		Last Modified: Tue, 18 Nov 2025 02:22:23 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cd8c01857a05a1b5f044acaa487c62457abe6c034ae53c1ff31742ddcf2674`  
		Last Modified: Tue, 18 Nov 2025 02:22:21 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186001a778777626b9a6cc1f37499f6999ba56727b1d1ff33b2edf19c709e68`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8617177bfd783cbfc258527d5d4e215e7352ed38622b315f56d73212be4310fe`  
		Last Modified: Tue, 18 Nov 2025 02:22:21 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7236d5a7918547e25547ad27fb4f73d2651193c3559e80a377269d90cc639c`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:7e5106e1757af2683cd6aba1b2346eb00f66ebac6cd23767870a51e8f152cdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2779575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb3adcc59fec7b6a92c1dc7e11d1b822f9142424dad97ec674d5e2a015a6819`

```dockerfile
```

-	Layers:
	-	`sha256:ddd0ccd96bff134250a51575fef41a6e7055a7b30a4915697280b3faba965bc1`  
		Last Modified: Tue, 18 Nov 2025 03:52:29 GMT  
		Size: 2.7 MB (2745031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65907c269e7dfa8d01379bf90b5f11bf0c0425f5e2197334673f43dfc98af83e`  
		Last Modified: Tue, 18 Nov 2025 03:52:30 GMT  
		Size: 34.5 KB (34544 bytes)  
		MIME: application/vnd.in-toto+json
