<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20251121`](#odoo170-20251121)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20251121`](#odoo180-20251121)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20251121`](#odoo190-20251121)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:070bf7985f2c65c4ae6726a5d93b0a74cb6c67d69a81ee2b72c094dbebb94f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:e76f7c4eb34684eaf59802f79f9d9f5e5bf0def4d0a86f9f66b342c5d1722768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.8 MB (605761669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa4591fb4a2a9189962bdaf75f6c76fd371e59dbb0b8dd33bbf20783ed9b1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:34 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:42 GMT
ENV ODOO_VERSION=17.0
# Fri, 21 Nov 2025 18:38:42 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:42 GMT
ARG ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
# Fri, 21 Nov 2025 18:39:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7151d498913f6b3d7ca99ce51ab09689260178253dd1332b79dcee2e0943899`  
		Last Modified: Fri, 21 Nov 2025 21:08:35 GMT  
		Size: 233.8 MB (233821083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a32091b4a718ea3c6d1a8f0db9f540d804a82c951d321d8d8e4a780819449`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 2.6 MB (2597239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e31d53077cc2529de3c6bbdcfae22a804c13f7c744624e65fb1b96dec52f81`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 480.3 KB (480252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71a9b697105cae6688c7285d22e65460e813676f419c6137693082d993bb31`  
		Last Modified: Fri, 21 Nov 2025 20:17:44 GMT  
		Size: 339.3 MB (339323862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05532665d5c0469836381b1119a846244937fca3c76da5648d8f587e8dcd9fad`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d699a436ca3c50867ab0c03a3a2962c3242d124df85a500901d922cb4604b1`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cea95f7b0d857f13670b4871fc877fd8dd1aeccd92d0e9d4ccb1e00347c48`  
		Last Modified: Fri, 21 Nov 2025 18:41:22 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7a86f1cb048608d6f7553a588091611a7a788d3bcb023747923c58e5b46003`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:18b969fb25c6d63183ab4a02cb7af4f7273b91826a99b8be292304334491521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41851696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b8a6044472f9ea0dc9f5ecde780491878f7c46599918dc364c7f4d8efa7cfe`

```dockerfile
```

-	Layers:
	-	`sha256:2fc7ce3c99b95c37acaa78a4d2376c7f4242aa1026d838f44f52b60ad496d9ad`  
		Last Modified: Fri, 21 Nov 2025 20:12:28 GMT  
		Size: 41.8 MB (41824904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:346acfe690a93c20aeb6e5192cca3c7d3417697a2a17257bb425b60d7caf16fe`  
		Last Modified: Fri, 21 Nov 2025 20:12:29 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:752d063f76655f64edb7d10141d96f42c8c63bec774937b01c9e96145703bf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600602289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0772cb992e9c9265ebe14ad9c2d62c72f11b704b0b061920a9da0f1f4b4706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:08 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:18 GMT
ENV ODOO_VERSION=17.0
# Fri, 21 Nov 2025 18:38:18 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:18 GMT
ARG ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
# Fri, 21 Nov 2025 18:39:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3904153b2a772a623782fcd5e781c96610ca8d138c14a407d7974ac4fa47cf`  
		Last Modified: Fri, 21 Nov 2025 18:45:11 GMT  
		Size: 231.2 MB (231194118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bae6dee8c3a6084a9f017b3c4ce589a3a8d31d5116bf05bf4506f1b36f53d64`  
		Last Modified: Fri, 21 Nov 2025 18:40:59 GMT  
		Size: 2.6 MB (2592488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed43d4bef8a1dff0c83c594c50c1d5af551abbd61bf092523f66a00bb7a54732`  
		Last Modified: Fri, 21 Nov 2025 18:40:59 GMT  
		Size: 480.3 KB (480263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0cbaa9ad3a93dd0b6285b169e20ef19d15e4b8f604e656c55298dd6fa2902c`  
		Last Modified: Fri, 21 Nov 2025 18:45:12 GMT  
		Size: 338.9 MB (338949109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c861f0bda832dc70ca71cbb8da9ed0f924f6ca0d84288def34bea49e48170fc`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9464eca9dbeb72845ca7c1d622349c469822929f7ddd0d63495938b96a22cf`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba68d28cf828d85ad50e47330825b9f8bca484489929b7e377d3955eab5b43`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b681231a257babec875748a230cb2c81ddc6e7bf96f43024f09d84dea6477dd`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e8eaaae1eaab1e00247f26b1038876023ca3605ed42b96ac56df3a593ccb97a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41858355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a008b0a041922d810b6f5c30bf17424c38848c9b27356c5d37b2cb15aaf0e91`

```dockerfile
```

-	Layers:
	-	`sha256:1d2b46a636d01bf1431bc5b39dcb72fb290de26ec720feb654e89cac141f4854`  
		Last Modified: Fri, 21 Nov 2025 20:13:26 GMT  
		Size: 41.8 MB (41831411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcffc38d3735020a9a5ca1055e47164d6063e74091dc8168639e2e64b583c432`  
		Last Modified: Fri, 21 Nov 2025 20:13:27 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:070bf7985f2c65c4ae6726a5d93b0a74cb6c67d69a81ee2b72c094dbebb94f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:e76f7c4eb34684eaf59802f79f9d9f5e5bf0def4d0a86f9f66b342c5d1722768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.8 MB (605761669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa4591fb4a2a9189962bdaf75f6c76fd371e59dbb0b8dd33bbf20783ed9b1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:34 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:42 GMT
ENV ODOO_VERSION=17.0
# Fri, 21 Nov 2025 18:38:42 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:42 GMT
ARG ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
# Fri, 21 Nov 2025 18:39:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7151d498913f6b3d7ca99ce51ab09689260178253dd1332b79dcee2e0943899`  
		Last Modified: Fri, 21 Nov 2025 21:08:35 GMT  
		Size: 233.8 MB (233821083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a32091b4a718ea3c6d1a8f0db9f540d804a82c951d321d8d8e4a780819449`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 2.6 MB (2597239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e31d53077cc2529de3c6bbdcfae22a804c13f7c744624e65fb1b96dec52f81`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 480.3 KB (480252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71a9b697105cae6688c7285d22e65460e813676f419c6137693082d993bb31`  
		Last Modified: Fri, 21 Nov 2025 20:17:44 GMT  
		Size: 339.3 MB (339323862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05532665d5c0469836381b1119a846244937fca3c76da5648d8f587e8dcd9fad`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d699a436ca3c50867ab0c03a3a2962c3242d124df85a500901d922cb4604b1`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cea95f7b0d857f13670b4871fc877fd8dd1aeccd92d0e9d4ccb1e00347c48`  
		Last Modified: Fri, 21 Nov 2025 18:41:22 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7a86f1cb048608d6f7553a588091611a7a788d3bcb023747923c58e5b46003`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:18b969fb25c6d63183ab4a02cb7af4f7273b91826a99b8be292304334491521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41851696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b8a6044472f9ea0dc9f5ecde780491878f7c46599918dc364c7f4d8efa7cfe`

```dockerfile
```

-	Layers:
	-	`sha256:2fc7ce3c99b95c37acaa78a4d2376c7f4242aa1026d838f44f52b60ad496d9ad`  
		Last Modified: Fri, 21 Nov 2025 20:12:28 GMT  
		Size: 41.8 MB (41824904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:346acfe690a93c20aeb6e5192cca3c7d3417697a2a17257bb425b60d7caf16fe`  
		Last Modified: Fri, 21 Nov 2025 20:12:29 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:752d063f76655f64edb7d10141d96f42c8c63bec774937b01c9e96145703bf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600602289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0772cb992e9c9265ebe14ad9c2d62c72f11b704b0b061920a9da0f1f4b4706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:08 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:18 GMT
ENV ODOO_VERSION=17.0
# Fri, 21 Nov 2025 18:38:18 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:18 GMT
ARG ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
# Fri, 21 Nov 2025 18:39:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3904153b2a772a623782fcd5e781c96610ca8d138c14a407d7974ac4fa47cf`  
		Last Modified: Fri, 21 Nov 2025 18:45:11 GMT  
		Size: 231.2 MB (231194118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bae6dee8c3a6084a9f017b3c4ce589a3a8d31d5116bf05bf4506f1b36f53d64`  
		Last Modified: Fri, 21 Nov 2025 18:40:59 GMT  
		Size: 2.6 MB (2592488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed43d4bef8a1dff0c83c594c50c1d5af551abbd61bf092523f66a00bb7a54732`  
		Last Modified: Fri, 21 Nov 2025 18:40:59 GMT  
		Size: 480.3 KB (480263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0cbaa9ad3a93dd0b6285b169e20ef19d15e4b8f604e656c55298dd6fa2902c`  
		Last Modified: Fri, 21 Nov 2025 18:45:12 GMT  
		Size: 338.9 MB (338949109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c861f0bda832dc70ca71cbb8da9ed0f924f6ca0d84288def34bea49e48170fc`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9464eca9dbeb72845ca7c1d622349c469822929f7ddd0d63495938b96a22cf`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba68d28cf828d85ad50e47330825b9f8bca484489929b7e377d3955eab5b43`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b681231a257babec875748a230cb2c81ddc6e7bf96f43024f09d84dea6477dd`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e8eaaae1eaab1e00247f26b1038876023ca3605ed42b96ac56df3a593ccb97a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41858355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a008b0a041922d810b6f5c30bf17424c38848c9b27356c5d37b2cb15aaf0e91`

```dockerfile
```

-	Layers:
	-	`sha256:1d2b46a636d01bf1431bc5b39dcb72fb290de26ec720feb654e89cac141f4854`  
		Last Modified: Fri, 21 Nov 2025 20:13:26 GMT  
		Size: 41.8 MB (41831411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcffc38d3735020a9a5ca1055e47164d6063e74091dc8168639e2e64b583c432`  
		Last Modified: Fri, 21 Nov 2025 20:13:27 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20251121`

```console
$ docker pull odoo@sha256:070bf7985f2c65c4ae6726a5d93b0a74cb6c67d69a81ee2b72c094dbebb94f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20251121` - linux; amd64

```console
$ docker pull odoo@sha256:e76f7c4eb34684eaf59802f79f9d9f5e5bf0def4d0a86f9f66b342c5d1722768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.8 MB (605761669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa4591fb4a2a9189962bdaf75f6c76fd371e59dbb0b8dd33bbf20783ed9b1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:34 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:42 GMT
ENV ODOO_VERSION=17.0
# Fri, 21 Nov 2025 18:38:42 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:42 GMT
ARG ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
# Fri, 21 Nov 2025 18:39:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:50 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7151d498913f6b3d7ca99ce51ab09689260178253dd1332b79dcee2e0943899`  
		Last Modified: Fri, 21 Nov 2025 21:08:35 GMT  
		Size: 233.8 MB (233821083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a32091b4a718ea3c6d1a8f0db9f540d804a82c951d321d8d8e4a780819449`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 2.6 MB (2597239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e31d53077cc2529de3c6bbdcfae22a804c13f7c744624e65fb1b96dec52f81`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 480.3 KB (480252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71a9b697105cae6688c7285d22e65460e813676f419c6137693082d993bb31`  
		Last Modified: Fri, 21 Nov 2025 20:17:44 GMT  
		Size: 339.3 MB (339323862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05532665d5c0469836381b1119a846244937fca3c76da5648d8f587e8dcd9fad`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d699a436ca3c50867ab0c03a3a2962c3242d124df85a500901d922cb4604b1`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cea95f7b0d857f13670b4871fc877fd8dd1aeccd92d0e9d4ccb1e00347c48`  
		Last Modified: Fri, 21 Nov 2025 18:41:22 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7a86f1cb048608d6f7553a588091611a7a788d3bcb023747923c58e5b46003`  
		Last Modified: Fri, 21 Nov 2025 18:41:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:18b969fb25c6d63183ab4a02cb7af4f7273b91826a99b8be292304334491521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41851696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b8a6044472f9ea0dc9f5ecde780491878f7c46599918dc364c7f4d8efa7cfe`

```dockerfile
```

-	Layers:
	-	`sha256:2fc7ce3c99b95c37acaa78a4d2376c7f4242aa1026d838f44f52b60ad496d9ad`  
		Last Modified: Fri, 21 Nov 2025 20:12:28 GMT  
		Size: 41.8 MB (41824904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:346acfe690a93c20aeb6e5192cca3c7d3417697a2a17257bb425b60d7caf16fe`  
		Last Modified: Fri, 21 Nov 2025 20:12:29 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20251121` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:752d063f76655f64edb7d10141d96f42c8c63bec774937b01c9e96145703bf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600602289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0772cb992e9c9265ebe14ad9c2d62c72f11b704b0b061920a9da0f1f4b4706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:08 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:18 GMT
ENV ODOO_VERSION=17.0
# Fri, 21 Nov 2025 18:38:18 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:18 GMT
ARG ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
# Fri, 21 Nov 2025 18:39:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=1acee67205be41870d2de781aa787aa5bbd68f3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:24 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3904153b2a772a623782fcd5e781c96610ca8d138c14a407d7974ac4fa47cf`  
		Last Modified: Fri, 21 Nov 2025 18:45:11 GMT  
		Size: 231.2 MB (231194118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bae6dee8c3a6084a9f017b3c4ce589a3a8d31d5116bf05bf4506f1b36f53d64`  
		Last Modified: Fri, 21 Nov 2025 18:40:59 GMT  
		Size: 2.6 MB (2592488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed43d4bef8a1dff0c83c594c50c1d5af551abbd61bf092523f66a00bb7a54732`  
		Last Modified: Fri, 21 Nov 2025 18:40:59 GMT  
		Size: 480.3 KB (480263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0cbaa9ad3a93dd0b6285b169e20ef19d15e4b8f604e656c55298dd6fa2902c`  
		Last Modified: Fri, 21 Nov 2025 18:45:12 GMT  
		Size: 338.9 MB (338949109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c861f0bda832dc70ca71cbb8da9ed0f924f6ca0d84288def34bea49e48170fc`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9464eca9dbeb72845ca7c1d622349c469822929f7ddd0d63495938b96a22cf`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba68d28cf828d85ad50e47330825b9f8bca484489929b7e377d3955eab5b43`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b681231a257babec875748a230cb2c81ddc6e7bf96f43024f09d84dea6477dd`  
		Last Modified: Fri, 21 Nov 2025 18:40:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:e8eaaae1eaab1e00247f26b1038876023ca3605ed42b96ac56df3a593ccb97a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41858355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a008b0a041922d810b6f5c30bf17424c38848c9b27356c5d37b2cb15aaf0e91`

```dockerfile
```

-	Layers:
	-	`sha256:1d2b46a636d01bf1431bc5b39dcb72fb290de26ec720feb654e89cac141f4854`  
		Last Modified: Fri, 21 Nov 2025 20:13:26 GMT  
		Size: 41.8 MB (41831411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcffc38d3735020a9a5ca1055e47164d6063e74091dc8168639e2e64b583c432`  
		Last Modified: Fri, 21 Nov 2025 20:13:27 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:d4cb3f0913d956b6f2dd6a0cd7b74b5df77f01b3d9e3291b36cafeddfaac6e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18` - linux; amd64

```console
$ docker pull odoo@sha256:1ce3e21922713d79637ebf40e2e354daf9879117ff27db7414714b1faece239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678307066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa593b2c910f32db3a2809655aded359e0ad99107396921e9e01c021921203e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:50 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:59 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:59 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:38:59 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:59 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:39:47 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871dc00805dc2b893ccf13de646d9d4394ab0b5dc53269b3c4df0f39f4b554dd`  
		Last Modified: Fri, 21 Nov 2025 20:46:27 GMT  
		Size: 254.6 MB (254557515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64c2bad5f39c1ff921c714a6ee1b117aab2aebfe4d7c2bc0dad87a7ed7b06c`  
		Last Modified: Fri, 21 Nov 2025 18:41:49 GMT  
		Size: 14.4 MB (14356367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb05fcc6f0bfef08147cc9ab6a2af38072610e9f7532943e8a7090ef1b0821c8`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9c5d428972cca0abf135695aa4908475e302f6daab10fa897dfe1696870fd9`  
		Last Modified: Fri, 21 Nov 2025 20:59:47 GMT  
		Size: 379.2 MB (379185971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c177810503a753837c6b98d6d33e38fb893fcfe93d63347c1c2d432adac3b565`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db1dcdf03ee8033721a87cf974b4f1c7b0a5d0aa08cd704e2bf22fe949b4036`  
		Last Modified: Fri, 21 Nov 2025 18:41:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd95484fd8fb44ff9db672dd774b973c45c47b26311aa34ce8db6ba6813a09a8`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bbb749dcb27742a6c3238ac71f43217fb768f88ced0f0d3b0d77e2de20c6e3`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d4b0ef7ccd47bc5edfeed4333bc432cf939a70cd5af22795dc3225f48dacef77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61419538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e0b52259451092964956c4a687c00d65a36791655cb73442ed7234c13fb5ad`

```dockerfile
```

-	Layers:
	-	`sha256:68a98c0b53a4038181b6ef28caf8e6fbe41b140286f2b03b787b3601b9d8f113`  
		Last Modified: Fri, 21 Nov 2025 20:12:45 GMT  
		Size: 61.4 MB (61392739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a28d80ad43f58121a13bbdd08dd6680a44233bc750cc5e2f5e80e07e6d9d16`  
		Last Modified: Fri, 21 Nov 2025 20:12:49 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8bb56ece0a29a013050d03388d1e031347f0c59765e0e45913bcfc08f0cea88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 MB (674680252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1020b7857042b83cf21b5cb394ef76e07b375b8b187542b78c42a51e96096fb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:29 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:37 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:38 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:38:38 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:38 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:39:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde9207442d8b73a6300f40350cecd72e59f1bfc61021ec0e437deca2ca6e540`  
		Last Modified: Fri, 21 Nov 2025 21:05:23 GMT  
		Size: 252.0 MB (251959836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa11ea96132459caa16fae62125c53fc24cac9ffe5daa8c1e4068385d5668d`  
		Last Modified: Fri, 21 Nov 2025 18:42:20 GMT  
		Size: 14.3 MB (14334163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842bbd8a7e11ac80904a551bdc18f152034d5e5f31668ec39c8604fd0833f363`  
		Last Modified: Fri, 21 Nov 2025 18:42:19 GMT  
		Size: 480.0 KB (480006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45d489ef81781e2c07946e72601f6f5d468af8472e94d45741008482f057aa1`  
		Last Modified: Fri, 21 Nov 2025 20:15:01 GMT  
		Size: 379.0 MB (379041855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65780f5bd59dbb74e31ca3e5dfaf0deec37d814be62a20635484417f05bfdd8`  
		Last Modified: Fri, 21 Nov 2025 18:42:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b39e02a474fbd001967b27fe3c160b4c5ae3d72daad4e1cc0210d6864565e5`  
		Last Modified: Fri, 21 Nov 2025 18:42:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10823dfe243d9b38e8659a1b121fc267f473b66c0cd54b67c4848e3d312dc3bd`  
		Last Modified: Fri, 21 Nov 2025 18:42:18 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510224cca6971905fa4fef89f30a60701f0f7e02eb81d6ab208f8b17c8a3a866`  
		Last Modified: Fri, 21 Nov 2025 18:42:18 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:4bdd46a4f9b3c7b3a091e4d883ecff359bb248d120d675ba714606b874f3b830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61426965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81218cd254686a8313c653085586930a5b4643dc19a7604414272432770cd9dd`

```dockerfile
```

-	Layers:
	-	`sha256:c7eeb71cabd49a2fff8b5e3c5448f607ae487418dd0e86e8a9e1a18a85eba3a0`  
		Last Modified: Fri, 21 Nov 2025 20:14:21 GMT  
		Size: 61.4 MB (61400014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d49d5dc16398206fc2056aecfc7ce74fb558db3ec22518eb88e4150d1b7c511`  
		Last Modified: Fri, 21 Nov 2025 20:14:23 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:8bc21e91f059da8ab458c79c0b0584feff441b5fbd8684e41ff8af7a4870d618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.5 MB (694470065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06332a37c1ee7ff4ea983754494ca27b1aa24b30a0f587aac37001ebe445197b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:40:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:42:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:42:59 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:43:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:43:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:43:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
USER odoo
# Fri, 21 Nov 2025 18:43:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:43:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b47702e52f3a5f2e8a1b2408e6843452eaec51d55389899bc0f54f156af25f`  
		Last Modified: Fri, 21 Nov 2025 18:50:44 GMT  
		Size: 14.9 MB (14885218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bed9ce04570ec2a8b46f795c12e54099f7f6bd485dea581c978739dfb9f1f4`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e99e836c44d49e5831e294ff88e03757ac8dcc428035682ecacd0b396e2601`  
		Last Modified: Sat, 22 Nov 2025 00:19:01 GMT  
		Size: 379.7 MB (379720057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f16089013bb07e6d9fe5897c11fc622fb35b5663b2f703d3a531917cb98cc`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3762675b572de533360901d0e594f525904cb0f9fe5482420c681d844fbd182`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1479f33e54f8a8f150f4de2975908b511b89b1e6ac808820c0f38d8703fccede`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0393d5bde68f5e1edb8dd012a2ca2258bb7a60646ee4e98881f447d72659b8`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:6bb3c4fa046b5ed41379d39880c7cc1344ebfc4c69f68ab5e89f817b3db2cfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61427976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbba84d67edf49fda3d51964e1c4683e88613dd8fd3f13474ad72db6a4d861a9`

```dockerfile
```

-	Layers:
	-	`sha256:6049a846e3999dc52b45b9b7179cf29c9c1ee54d98b63e496faba89ab3b795c2`  
		Last Modified: Fri, 21 Nov 2025 20:16:38 GMT  
		Size: 61.4 MB (61401122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1161e5327791af69a8c830a2711c8898a83cf913473ea12d617efd540b5cc2d4`  
		Last Modified: Fri, 21 Nov 2025 20:16:20 GMT  
		Size: 26.9 KB (26854 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:d4cb3f0913d956b6f2dd6a0cd7b74b5df77f01b3d9e3291b36cafeddfaac6e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0` - linux; amd64

```console
$ docker pull odoo@sha256:1ce3e21922713d79637ebf40e2e354daf9879117ff27db7414714b1faece239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678307066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa593b2c910f32db3a2809655aded359e0ad99107396921e9e01c021921203e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:50 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:59 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:59 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:38:59 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:59 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:39:47 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871dc00805dc2b893ccf13de646d9d4394ab0b5dc53269b3c4df0f39f4b554dd`  
		Last Modified: Fri, 21 Nov 2025 20:46:27 GMT  
		Size: 254.6 MB (254557515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64c2bad5f39c1ff921c714a6ee1b117aab2aebfe4d7c2bc0dad87a7ed7b06c`  
		Last Modified: Fri, 21 Nov 2025 18:41:49 GMT  
		Size: 14.4 MB (14356367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb05fcc6f0bfef08147cc9ab6a2af38072610e9f7532943e8a7090ef1b0821c8`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9c5d428972cca0abf135695aa4908475e302f6daab10fa897dfe1696870fd9`  
		Last Modified: Fri, 21 Nov 2025 20:59:47 GMT  
		Size: 379.2 MB (379185971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c177810503a753837c6b98d6d33e38fb893fcfe93d63347c1c2d432adac3b565`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db1dcdf03ee8033721a87cf974b4f1c7b0a5d0aa08cd704e2bf22fe949b4036`  
		Last Modified: Fri, 21 Nov 2025 18:41:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd95484fd8fb44ff9db672dd774b973c45c47b26311aa34ce8db6ba6813a09a8`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bbb749dcb27742a6c3238ac71f43217fb768f88ced0f0d3b0d77e2de20c6e3`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d4b0ef7ccd47bc5edfeed4333bc432cf939a70cd5af22795dc3225f48dacef77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61419538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e0b52259451092964956c4a687c00d65a36791655cb73442ed7234c13fb5ad`

```dockerfile
```

-	Layers:
	-	`sha256:68a98c0b53a4038181b6ef28caf8e6fbe41b140286f2b03b787b3601b9d8f113`  
		Last Modified: Fri, 21 Nov 2025 20:12:45 GMT  
		Size: 61.4 MB (61392739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a28d80ad43f58121a13bbdd08dd6680a44233bc750cc5e2f5e80e07e6d9d16`  
		Last Modified: Fri, 21 Nov 2025 20:12:49 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8bb56ece0a29a013050d03388d1e031347f0c59765e0e45913bcfc08f0cea88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 MB (674680252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1020b7857042b83cf21b5cb394ef76e07b375b8b187542b78c42a51e96096fb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:29 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:37 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:38 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:38:38 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:38 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:39:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde9207442d8b73a6300f40350cecd72e59f1bfc61021ec0e437deca2ca6e540`  
		Last Modified: Fri, 21 Nov 2025 21:05:23 GMT  
		Size: 252.0 MB (251959836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa11ea96132459caa16fae62125c53fc24cac9ffe5daa8c1e4068385d5668d`  
		Last Modified: Fri, 21 Nov 2025 18:42:20 GMT  
		Size: 14.3 MB (14334163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842bbd8a7e11ac80904a551bdc18f152034d5e5f31668ec39c8604fd0833f363`  
		Last Modified: Fri, 21 Nov 2025 18:42:19 GMT  
		Size: 480.0 KB (480006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45d489ef81781e2c07946e72601f6f5d468af8472e94d45741008482f057aa1`  
		Last Modified: Fri, 21 Nov 2025 20:15:01 GMT  
		Size: 379.0 MB (379041855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65780f5bd59dbb74e31ca3e5dfaf0deec37d814be62a20635484417f05bfdd8`  
		Last Modified: Fri, 21 Nov 2025 18:42:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b39e02a474fbd001967b27fe3c160b4c5ae3d72daad4e1cc0210d6864565e5`  
		Last Modified: Fri, 21 Nov 2025 18:42:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10823dfe243d9b38e8659a1b121fc267f473b66c0cd54b67c4848e3d312dc3bd`  
		Last Modified: Fri, 21 Nov 2025 18:42:18 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510224cca6971905fa4fef89f30a60701f0f7e02eb81d6ab208f8b17c8a3a866`  
		Last Modified: Fri, 21 Nov 2025 18:42:18 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4bdd46a4f9b3c7b3a091e4d883ecff359bb248d120d675ba714606b874f3b830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61426965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81218cd254686a8313c653085586930a5b4643dc19a7604414272432770cd9dd`

```dockerfile
```

-	Layers:
	-	`sha256:c7eeb71cabd49a2fff8b5e3c5448f607ae487418dd0e86e8a9e1a18a85eba3a0`  
		Last Modified: Fri, 21 Nov 2025 20:14:21 GMT  
		Size: 61.4 MB (61400014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d49d5dc16398206fc2056aecfc7ce74fb558db3ec22518eb88e4150d1b7c511`  
		Last Modified: Fri, 21 Nov 2025 20:14:23 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:8bc21e91f059da8ab458c79c0b0584feff441b5fbd8684e41ff8af7a4870d618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.5 MB (694470065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06332a37c1ee7ff4ea983754494ca27b1aa24b30a0f587aac37001ebe445197b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:40:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:42:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:42:59 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:43:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:43:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:43:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
USER odoo
# Fri, 21 Nov 2025 18:43:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:43:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b47702e52f3a5f2e8a1b2408e6843452eaec51d55389899bc0f54f156af25f`  
		Last Modified: Fri, 21 Nov 2025 18:50:44 GMT  
		Size: 14.9 MB (14885218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bed9ce04570ec2a8b46f795c12e54099f7f6bd485dea581c978739dfb9f1f4`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e99e836c44d49e5831e294ff88e03757ac8dcc428035682ecacd0b396e2601`  
		Last Modified: Sat, 22 Nov 2025 00:19:01 GMT  
		Size: 379.7 MB (379720057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f16089013bb07e6d9fe5897c11fc622fb35b5663b2f703d3a531917cb98cc`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3762675b572de533360901d0e594f525904cb0f9fe5482420c681d844fbd182`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1479f33e54f8a8f150f4de2975908b511b89b1e6ac808820c0f38d8703fccede`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0393d5bde68f5e1edb8dd012a2ca2258bb7a60646ee4e98881f447d72659b8`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6bb3c4fa046b5ed41379d39880c7cc1344ebfc4c69f68ab5e89f817b3db2cfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61427976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbba84d67edf49fda3d51964e1c4683e88613dd8fd3f13474ad72db6a4d861a9`

```dockerfile
```

-	Layers:
	-	`sha256:6049a846e3999dc52b45b9b7179cf29c9c1ee54d98b63e496faba89ab3b795c2`  
		Last Modified: Fri, 21 Nov 2025 20:16:38 GMT  
		Size: 61.4 MB (61401122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1161e5327791af69a8c830a2711c8898a83cf913473ea12d617efd540b5cc2d4`  
		Last Modified: Fri, 21 Nov 2025 20:16:20 GMT  
		Size: 26.9 KB (26854 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251121`

```console
$ docker pull odoo@sha256:d4cb3f0913d956b6f2dd6a0cd7b74b5df77f01b3d9e3291b36cafeddfaac6e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20251121` - linux; amd64

```console
$ docker pull odoo@sha256:1ce3e21922713d79637ebf40e2e354daf9879117ff27db7414714b1faece239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678307066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa593b2c910f32db3a2809655aded359e0ad99107396921e9e01c021921203e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:50 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:59 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:59 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:38:59 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:59 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:39:47 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:47 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871dc00805dc2b893ccf13de646d9d4394ab0b5dc53269b3c4df0f39f4b554dd`  
		Last Modified: Fri, 21 Nov 2025 20:46:27 GMT  
		Size: 254.6 MB (254557515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64c2bad5f39c1ff921c714a6ee1b117aab2aebfe4d7c2bc0dad87a7ed7b06c`  
		Last Modified: Fri, 21 Nov 2025 18:41:49 GMT  
		Size: 14.4 MB (14356367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb05fcc6f0bfef08147cc9ab6a2af38072610e9f7532943e8a7090ef1b0821c8`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9c5d428972cca0abf135695aa4908475e302f6daab10fa897dfe1696870fd9`  
		Last Modified: Fri, 21 Nov 2025 20:59:47 GMT  
		Size: 379.2 MB (379185971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c177810503a753837c6b98d6d33e38fb893fcfe93d63347c1c2d432adac3b565`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db1dcdf03ee8033721a87cf974b4f1c7b0a5d0aa08cd704e2bf22fe949b4036`  
		Last Modified: Fri, 21 Nov 2025 18:41:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd95484fd8fb44ff9db672dd774b973c45c47b26311aa34ce8db6ba6813a09a8`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bbb749dcb27742a6c3238ac71f43217fb768f88ced0f0d3b0d77e2de20c6e3`  
		Last Modified: Fri, 21 Nov 2025 18:41:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:d4b0ef7ccd47bc5edfeed4333bc432cf939a70cd5af22795dc3225f48dacef77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61419538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e0b52259451092964956c4a687c00d65a36791655cb73442ed7234c13fb5ad`

```dockerfile
```

-	Layers:
	-	`sha256:68a98c0b53a4038181b6ef28caf8e6fbe41b140286f2b03b787b3601b9d8f113`  
		Last Modified: Fri, 21 Nov 2025 20:12:45 GMT  
		Size: 61.4 MB (61392739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a28d80ad43f58121a13bbdd08dd6680a44233bc750cc5e2f5e80e07e6d9d16`  
		Last Modified: Fri, 21 Nov 2025 20:12:49 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251121` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8bb56ece0a29a013050d03388d1e031347f0c59765e0e45913bcfc08f0cea88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 MB (674680252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1020b7857042b83cf21b5cb394ef76e07b375b8b187542b78c42a51e96096fb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:29 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:37 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:38 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:38:38 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:38 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:39:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:58 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde9207442d8b73a6300f40350cecd72e59f1bfc61021ec0e437deca2ca6e540`  
		Last Modified: Fri, 21 Nov 2025 21:05:23 GMT  
		Size: 252.0 MB (251959836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa11ea96132459caa16fae62125c53fc24cac9ffe5daa8c1e4068385d5668d`  
		Last Modified: Fri, 21 Nov 2025 18:42:20 GMT  
		Size: 14.3 MB (14334163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842bbd8a7e11ac80904a551bdc18f152034d5e5f31668ec39c8604fd0833f363`  
		Last Modified: Fri, 21 Nov 2025 18:42:19 GMT  
		Size: 480.0 KB (480006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45d489ef81781e2c07946e72601f6f5d468af8472e94d45741008482f057aa1`  
		Last Modified: Fri, 21 Nov 2025 20:15:01 GMT  
		Size: 379.0 MB (379041855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65780f5bd59dbb74e31ca3e5dfaf0deec37d814be62a20635484417f05bfdd8`  
		Last Modified: Fri, 21 Nov 2025 18:42:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b39e02a474fbd001967b27fe3c160b4c5ae3d72daad4e1cc0210d6864565e5`  
		Last Modified: Fri, 21 Nov 2025 18:42:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10823dfe243d9b38e8659a1b121fc267f473b66c0cd54b67c4848e3d312dc3bd`  
		Last Modified: Fri, 21 Nov 2025 18:42:18 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510224cca6971905fa4fef89f30a60701f0f7e02eb81d6ab208f8b17c8a3a866`  
		Last Modified: Fri, 21 Nov 2025 18:42:18 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:4bdd46a4f9b3c7b3a091e4d883ecff359bb248d120d675ba714606b874f3b830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61426965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81218cd254686a8313c653085586930a5b4643dc19a7604414272432770cd9dd`

```dockerfile
```

-	Layers:
	-	`sha256:c7eeb71cabd49a2fff8b5e3c5448f607ae487418dd0e86e8a9e1a18a85eba3a0`  
		Last Modified: Fri, 21 Nov 2025 20:14:21 GMT  
		Size: 61.4 MB (61400014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d49d5dc16398206fc2056aecfc7ce74fb558db3ec22518eb88e4150d1b7c511`  
		Last Modified: Fri, 21 Nov 2025 20:14:23 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251121` - linux; ppc64le

```console
$ docker pull odoo@sha256:8bc21e91f059da8ab458c79c0b0584feff441b5fbd8684e41ff8af7a4870d618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.5 MB (694470065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06332a37c1ee7ff4ea983754494ca27b1aa24b30a0f587aac37001ebe445197b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:40:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
ENV ODOO_VERSION=18.0
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
# Fri, 21 Nov 2025 18:42:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:42:59 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=a13f7fb056248eb3941cc45f33ddf63917484bb3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:43:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:43:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:43:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:43:00 GMT
USER odoo
# Fri, 21 Nov 2025 18:43:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:43:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b47702e52f3a5f2e8a1b2408e6843452eaec51d55389899bc0f54f156af25f`  
		Last Modified: Fri, 21 Nov 2025 18:50:44 GMT  
		Size: 14.9 MB (14885218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bed9ce04570ec2a8b46f795c12e54099f7f6bd485dea581c978739dfb9f1f4`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e99e836c44d49e5831e294ff88e03757ac8dcc428035682ecacd0b396e2601`  
		Last Modified: Sat, 22 Nov 2025 00:19:01 GMT  
		Size: 379.7 MB (379720057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f16089013bb07e6d9fe5897c11fc622fb35b5663b2f703d3a531917cb98cc`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3762675b572de533360901d0e594f525904cb0f9fe5482420c681d844fbd182`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1479f33e54f8a8f150f4de2975908b511b89b1e6ac808820c0f38d8703fccede`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0393d5bde68f5e1edb8dd012a2ca2258bb7a60646ee4e98881f447d72659b8`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:6bb3c4fa046b5ed41379d39880c7cc1344ebfc4c69f68ab5e89f817b3db2cfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61427976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbba84d67edf49fda3d51964e1c4683e88613dd8fd3f13474ad72db6a4d861a9`

```dockerfile
```

-	Layers:
	-	`sha256:6049a846e3999dc52b45b9b7179cf29c9c1ee54d98b63e496faba89ab3b795c2`  
		Last Modified: Fri, 21 Nov 2025 20:16:38 GMT  
		Size: 61.4 MB (61401122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1161e5327791af69a8c830a2711c8898a83cf913473ea12d617efd540b5cc2d4`  
		Last Modified: Fri, 21 Nov 2025 20:16:20 GMT  
		Size: 26.9 KB (26854 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:18f4ead7d36dbe259ceca67dda6aafec4456509b2dccf39f86a85b1d44e4691b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19` - linux; amd64

```console
$ docker pull odoo@sha256:2964f9c4666ef6a5ef34ef6324ec54a94e1993b3941d3666db83ab7db13281da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687897817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88060bbc10987662bfe69a893ae28b95efb384216dd62b25e9b99ac8fac9a7f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:53 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:39:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:40:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:40:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:40:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:40:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
USER odoo
# Fri, 21 Nov 2025 18:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:40:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d34ac84d0f90bd397e100f55b8ae2b279b5186d94e87064a92cfa051410403`  
		Last Modified: Fri, 21 Nov 2025 19:18:37 GMT  
		Size: 254.6 MB (254557777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3de4ea1dcb394ad7102b0bc5698faf6ff3f79b75e10d8612b06c2dc0187ca2`  
		Last Modified: Fri, 21 Nov 2025 18:42:28 GMT  
		Size: 14.4 MB (14356466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2622d6b8ae2a84a8f36bf6c039b3fc4c96dfe80515d2c5ea77ba63fef67da2`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 480.0 KB (479994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88800fe7970c65fa15e083f824c4519478dbc1b8c486e962c5ba8bd41cf66f`  
		Last Modified: Fri, 21 Nov 2025 19:18:48 GMT  
		Size: 388.8 MB (388776451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca115ed5ea01074878beed6b8008578acfbc5de66e6906ca70698cb07817e3e`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3238a841c6f0e2462aeef9909f95aef97d790682d4f5ca19a264279a34bf6c`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfc90d8ce43d6e581ead6d7cfdf736619f53847ffc51109d4c5de8f07238625`  
		Last Modified: Fri, 21 Nov 2025 18:42:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11a273c8998d41e0f1d5f4e34a74c764c9f187267b2889246a7a0f604c2ead9`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:c272e5692065cadff7e15207d4d2b4e86ebda6357481c87dffaa3fb52b3940bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68412665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc864b9f01a5b888002e6fd65e607c82a20231fd93e134a715134974148a405`

```dockerfile
```

-	Layers:
	-	`sha256:36b67e958ab15f92464205b1c2ffe65e8f28cfc55184e9182d1d181f2abc3782`  
		Last Modified: Fri, 21 Nov 2025 20:13:06 GMT  
		Size: 68.4 MB (68385572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5185bab1b6e412966059c4ec3435b2e0196b51a89275e0579b50fc1b371dd130`  
		Last Modified: Fri, 21 Nov 2025 20:13:07 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f41de1d80ac362620acd527a3c296d1a4edd87d9fc86be86c1c1fbec37e6690f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.3 MB (684275571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c0b4e1d7fbc061ff4272c1f54bec13d56d3fa442bb80d2577028c6dac16d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:29 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:39 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:39:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003fb6b0f8c2e157dad0b6b5f83834c810f7ae15d29665dfd75aeaa3d7d649f5`  
		Last Modified: Fri, 21 Nov 2025 18:48:26 GMT  
		Size: 252.0 MB (251960396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1266c4bf294b49c12008a7b8ca557a9c88209d6584266f1c7ddee68ff214b2`  
		Last Modified: Fri, 21 Nov 2025 18:42:47 GMT  
		Size: 14.3 MB (14334140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cc54ffc2287a77b24213bc10d4715a8598901370f9fed3aed86467fd88c41a`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 480.0 KB (480020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad798e7d34186abfa68256a0081ab78aa965b57dcc68b2c63d8c6531c6c14044`  
		Last Modified: Fri, 21 Nov 2025 18:48:32 GMT  
		Size: 388.6 MB (388636623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5db9fb7d5ee7e84e08884e4e6ef1e68213d3ffca6c05f03c2c59269e1f807cf`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9c46582f5a458fc9a5941da8ebf2b7dcb5242ad46c78b18f06ea20145a638`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f62cbf03e9f73f889f1df93457978b96cee136bd89934a2a74cd6f3a3353bb`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b7e8d98e3e469de687b190b2631cc9f723339b2a70134350b700d36c716cf2`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:7f804b9288ae72a6853b43e2c712e2e20ce4c33767c101583daca09c41f5d624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68420116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c07896c788320e91476932a0e130d70599e2784b2f62e5ddfdcd6e9188c71c4`

```dockerfile
```

-	Layers:
	-	`sha256:c72aa394b3094b14274a6780356f7da95a580bdde3fcdc4c2a62576a664f8acb`  
		Last Modified: Fri, 21 Nov 2025 20:14:57 GMT  
		Size: 68.4 MB (68392859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51842942d84cc0d6a28282f18085e44be411fc75ccfc066a977af6765bf8bcab`  
		Last Modified: Fri, 21 Nov 2025 20:14:58 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:4f6059a377661abd889550d22dcdde02396a25f044bace5d47abac5492d59b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.1 MB (704063362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5c0778b0e87ff5b1e282e70d40208cde19e9b085cc3039b6ab783c2aa89140`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:40:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:43:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:43:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:43:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:43:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
USER odoo
# Fri, 21 Nov 2025 18:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:43:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b47702e52f3a5f2e8a1b2408e6843452eaec51d55389899bc0f54f156af25f`  
		Last Modified: Fri, 21 Nov 2025 18:50:44 GMT  
		Size: 14.9 MB (14885218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bed9ce04570ec2a8b46f795c12e54099f7f6bd485dea581c978739dfb9f1f4`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d694a4a80abbd45c8a3c78146036aacdb5762b0d6d9f58c13dd968f4bb0b7980`  
		Last Modified: Fri, 21 Nov 2025 19:12:55 GMT  
		Size: 389.3 MB (389313356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f16089013bb07e6d9fe5897c11fc622fb35b5663b2f703d3a531917cb98cc`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe896974271cc2a60996dc5e2036fadeb14d0e50be9eb6668a843b30abb1b237`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233572647d2aaedc04c327753f9af9cf83b7fa0aaed31b5fa26200fbfe477030`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4adc3e7bb184764c09cda0a24bcf9b6ee23e83d0b4b2be7af6d99cab663058`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:3dfeca69507dc0194023d37e435726d799310b8a3da27c2fab172b37685f41d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68421115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e763f1c535f7fca4c3d5bac0efaa3e3ec09f4c251f5304e7a6e356ddd5388c88`

```dockerfile
```

-	Layers:
	-	`sha256:6604bbc0538ca467ff3fb0c3a0d0a5b3cc123cec54779b80dc36ab7a31e0cf36`  
		Last Modified: Fri, 21 Nov 2025 20:16:48 GMT  
		Size: 68.4 MB (68393961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321e0d0580b8e6cf05d0f0228ef05c6e756b13130d592ebc4e1bfd7f9db29f95`  
		Last Modified: Fri, 21 Nov 2025 20:16:50 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:18f4ead7d36dbe259ceca67dda6aafec4456509b2dccf39f86a85b1d44e4691b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0` - linux; amd64

```console
$ docker pull odoo@sha256:2964f9c4666ef6a5ef34ef6324ec54a94e1993b3941d3666db83ab7db13281da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687897817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88060bbc10987662bfe69a893ae28b95efb384216dd62b25e9b99ac8fac9a7f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:53 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:39:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:40:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:40:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:40:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:40:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
USER odoo
# Fri, 21 Nov 2025 18:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:40:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d34ac84d0f90bd397e100f55b8ae2b279b5186d94e87064a92cfa051410403`  
		Last Modified: Fri, 21 Nov 2025 19:18:37 GMT  
		Size: 254.6 MB (254557777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3de4ea1dcb394ad7102b0bc5698faf6ff3f79b75e10d8612b06c2dc0187ca2`  
		Last Modified: Fri, 21 Nov 2025 18:42:28 GMT  
		Size: 14.4 MB (14356466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2622d6b8ae2a84a8f36bf6c039b3fc4c96dfe80515d2c5ea77ba63fef67da2`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 480.0 KB (479994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88800fe7970c65fa15e083f824c4519478dbc1b8c486e962c5ba8bd41cf66f`  
		Last Modified: Fri, 21 Nov 2025 19:18:48 GMT  
		Size: 388.8 MB (388776451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca115ed5ea01074878beed6b8008578acfbc5de66e6906ca70698cb07817e3e`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3238a841c6f0e2462aeef9909f95aef97d790682d4f5ca19a264279a34bf6c`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfc90d8ce43d6e581ead6d7cfdf736619f53847ffc51109d4c5de8f07238625`  
		Last Modified: Fri, 21 Nov 2025 18:42:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11a273c8998d41e0f1d5f4e34a74c764c9f187267b2889246a7a0f604c2ead9`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c272e5692065cadff7e15207d4d2b4e86ebda6357481c87dffaa3fb52b3940bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68412665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc864b9f01a5b888002e6fd65e607c82a20231fd93e134a715134974148a405`

```dockerfile
```

-	Layers:
	-	`sha256:36b67e958ab15f92464205b1c2ffe65e8f28cfc55184e9182d1d181f2abc3782`  
		Last Modified: Fri, 21 Nov 2025 20:13:06 GMT  
		Size: 68.4 MB (68385572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5185bab1b6e412966059c4ec3435b2e0196b51a89275e0579b50fc1b371dd130`  
		Last Modified: Fri, 21 Nov 2025 20:13:07 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f41de1d80ac362620acd527a3c296d1a4edd87d9fc86be86c1c1fbec37e6690f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.3 MB (684275571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c0b4e1d7fbc061ff4272c1f54bec13d56d3fa442bb80d2577028c6dac16d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:29 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:39 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:39:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003fb6b0f8c2e157dad0b6b5f83834c810f7ae15d29665dfd75aeaa3d7d649f5`  
		Last Modified: Fri, 21 Nov 2025 18:48:26 GMT  
		Size: 252.0 MB (251960396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1266c4bf294b49c12008a7b8ca557a9c88209d6584266f1c7ddee68ff214b2`  
		Last Modified: Fri, 21 Nov 2025 18:42:47 GMT  
		Size: 14.3 MB (14334140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cc54ffc2287a77b24213bc10d4715a8598901370f9fed3aed86467fd88c41a`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 480.0 KB (480020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad798e7d34186abfa68256a0081ab78aa965b57dcc68b2c63d8c6531c6c14044`  
		Last Modified: Fri, 21 Nov 2025 18:48:32 GMT  
		Size: 388.6 MB (388636623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5db9fb7d5ee7e84e08884e4e6ef1e68213d3ffca6c05f03c2c59269e1f807cf`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9c46582f5a458fc9a5941da8ebf2b7dcb5242ad46c78b18f06ea20145a638`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f62cbf03e9f73f889f1df93457978b96cee136bd89934a2a74cd6f3a3353bb`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b7e8d98e3e469de687b190b2631cc9f723339b2a70134350b700d36c716cf2`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7f804b9288ae72a6853b43e2c712e2e20ce4c33767c101583daca09c41f5d624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68420116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c07896c788320e91476932a0e130d70599e2784b2f62e5ddfdcd6e9188c71c4`

```dockerfile
```

-	Layers:
	-	`sha256:c72aa394b3094b14274a6780356f7da95a580bdde3fcdc4c2a62576a664f8acb`  
		Last Modified: Fri, 21 Nov 2025 20:14:57 GMT  
		Size: 68.4 MB (68392859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51842942d84cc0d6a28282f18085e44be411fc75ccfc066a977af6765bf8bcab`  
		Last Modified: Fri, 21 Nov 2025 20:14:58 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:4f6059a377661abd889550d22dcdde02396a25f044bace5d47abac5492d59b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.1 MB (704063362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5c0778b0e87ff5b1e282e70d40208cde19e9b085cc3039b6ab783c2aa89140`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:40:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:43:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:43:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:43:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:43:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
USER odoo
# Fri, 21 Nov 2025 18:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:43:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b47702e52f3a5f2e8a1b2408e6843452eaec51d55389899bc0f54f156af25f`  
		Last Modified: Fri, 21 Nov 2025 18:50:44 GMT  
		Size: 14.9 MB (14885218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bed9ce04570ec2a8b46f795c12e54099f7f6bd485dea581c978739dfb9f1f4`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d694a4a80abbd45c8a3c78146036aacdb5762b0d6d9f58c13dd968f4bb0b7980`  
		Last Modified: Fri, 21 Nov 2025 19:12:55 GMT  
		Size: 389.3 MB (389313356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f16089013bb07e6d9fe5897c11fc622fb35b5663b2f703d3a531917cb98cc`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe896974271cc2a60996dc5e2036fadeb14d0e50be9eb6668a843b30abb1b237`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233572647d2aaedc04c327753f9af9cf83b7fa0aaed31b5fa26200fbfe477030`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4adc3e7bb184764c09cda0a24bcf9b6ee23e83d0b4b2be7af6d99cab663058`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3dfeca69507dc0194023d37e435726d799310b8a3da27c2fab172b37685f41d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68421115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e763f1c535f7fca4c3d5bac0efaa3e3ec09f4c251f5304e7a6e356ddd5388c88`

```dockerfile
```

-	Layers:
	-	`sha256:6604bbc0538ca467ff3fb0c3a0d0a5b3cc123cec54779b80dc36ab7a31e0cf36`  
		Last Modified: Fri, 21 Nov 2025 20:16:48 GMT  
		Size: 68.4 MB (68393961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321e0d0580b8e6cf05d0f0228ef05c6e756b13130d592ebc4e1bfd7f9db29f95`  
		Last Modified: Fri, 21 Nov 2025 20:16:50 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251121`

```console
$ docker pull odoo@sha256:18f4ead7d36dbe259ceca67dda6aafec4456509b2dccf39f86a85b1d44e4691b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20251121` - linux; amd64

```console
$ docker pull odoo@sha256:2964f9c4666ef6a5ef34ef6324ec54a94e1993b3941d3666db83ab7db13281da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687897817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88060bbc10987662bfe69a893ae28b95efb384216dd62b25e9b99ac8fac9a7f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:53 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:39:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:40:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:40:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:40:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:40:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
USER odoo
# Fri, 21 Nov 2025 18:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:40:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d34ac84d0f90bd397e100f55b8ae2b279b5186d94e87064a92cfa051410403`  
		Last Modified: Fri, 21 Nov 2025 19:18:37 GMT  
		Size: 254.6 MB (254557777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3de4ea1dcb394ad7102b0bc5698faf6ff3f79b75e10d8612b06c2dc0187ca2`  
		Last Modified: Fri, 21 Nov 2025 18:42:28 GMT  
		Size: 14.4 MB (14356466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2622d6b8ae2a84a8f36bf6c039b3fc4c96dfe80515d2c5ea77ba63fef67da2`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 480.0 KB (479994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88800fe7970c65fa15e083f824c4519478dbc1b8c486e962c5ba8bd41cf66f`  
		Last Modified: Fri, 21 Nov 2025 19:18:48 GMT  
		Size: 388.8 MB (388776451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca115ed5ea01074878beed6b8008578acfbc5de66e6906ca70698cb07817e3e`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3238a841c6f0e2462aeef9909f95aef97d790682d4f5ca19a264279a34bf6c`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfc90d8ce43d6e581ead6d7cfdf736619f53847ffc51109d4c5de8f07238625`  
		Last Modified: Fri, 21 Nov 2025 18:42:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11a273c8998d41e0f1d5f4e34a74c764c9f187267b2889246a7a0f604c2ead9`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:c272e5692065cadff7e15207d4d2b4e86ebda6357481c87dffaa3fb52b3940bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68412665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc864b9f01a5b888002e6fd65e607c82a20231fd93e134a715134974148a405`

```dockerfile
```

-	Layers:
	-	`sha256:36b67e958ab15f92464205b1c2ffe65e8f28cfc55184e9182d1d181f2abc3782`  
		Last Modified: Fri, 21 Nov 2025 20:13:06 GMT  
		Size: 68.4 MB (68385572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5185bab1b6e412966059c4ec3435b2e0196b51a89275e0579b50fc1b371dd130`  
		Last Modified: Fri, 21 Nov 2025 20:13:07 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251121` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f41de1d80ac362620acd527a3c296d1a4edd87d9fc86be86c1c1fbec37e6690f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.3 MB (684275571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c0b4e1d7fbc061ff4272c1f54bec13d56d3fa442bb80d2577028c6dac16d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:29 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:39 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:39:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003fb6b0f8c2e157dad0b6b5f83834c810f7ae15d29665dfd75aeaa3d7d649f5`  
		Last Modified: Fri, 21 Nov 2025 18:48:26 GMT  
		Size: 252.0 MB (251960396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1266c4bf294b49c12008a7b8ca557a9c88209d6584266f1c7ddee68ff214b2`  
		Last Modified: Fri, 21 Nov 2025 18:42:47 GMT  
		Size: 14.3 MB (14334140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cc54ffc2287a77b24213bc10d4715a8598901370f9fed3aed86467fd88c41a`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 480.0 KB (480020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad798e7d34186abfa68256a0081ab78aa965b57dcc68b2c63d8c6531c6c14044`  
		Last Modified: Fri, 21 Nov 2025 18:48:32 GMT  
		Size: 388.6 MB (388636623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5db9fb7d5ee7e84e08884e4e6ef1e68213d3ffca6c05f03c2c59269e1f807cf`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9c46582f5a458fc9a5941da8ebf2b7dcb5242ad46c78b18f06ea20145a638`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f62cbf03e9f73f889f1df93457978b96cee136bd89934a2a74cd6f3a3353bb`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b7e8d98e3e469de687b190b2631cc9f723339b2a70134350b700d36c716cf2`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:7f804b9288ae72a6853b43e2c712e2e20ce4c33767c101583daca09c41f5d624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68420116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c07896c788320e91476932a0e130d70599e2784b2f62e5ddfdcd6e9188c71c4`

```dockerfile
```

-	Layers:
	-	`sha256:c72aa394b3094b14274a6780356f7da95a580bdde3fcdc4c2a62576a664f8acb`  
		Last Modified: Fri, 21 Nov 2025 20:14:57 GMT  
		Size: 68.4 MB (68392859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51842942d84cc0d6a28282f18085e44be411fc75ccfc066a977af6765bf8bcab`  
		Last Modified: Fri, 21 Nov 2025 20:14:58 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251121` - linux; ppc64le

```console
$ docker pull odoo@sha256:4f6059a377661abd889550d22dcdde02396a25f044bace5d47abac5492d59b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.1 MB (704063362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5c0778b0e87ff5b1e282e70d40208cde19e9b085cc3039b6ab783c2aa89140`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:40:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:43:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:43:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:43:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:43:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
USER odoo
# Fri, 21 Nov 2025 18:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:43:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b47702e52f3a5f2e8a1b2408e6843452eaec51d55389899bc0f54f156af25f`  
		Last Modified: Fri, 21 Nov 2025 18:50:44 GMT  
		Size: 14.9 MB (14885218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bed9ce04570ec2a8b46f795c12e54099f7f6bd485dea581c978739dfb9f1f4`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d694a4a80abbd45c8a3c78146036aacdb5762b0d6d9f58c13dd968f4bb0b7980`  
		Last Modified: Fri, 21 Nov 2025 19:12:55 GMT  
		Size: 389.3 MB (389313356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f16089013bb07e6d9fe5897c11fc622fb35b5663b2f703d3a531917cb98cc`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe896974271cc2a60996dc5e2036fadeb14d0e50be9eb6668a843b30abb1b237`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233572647d2aaedc04c327753f9af9cf83b7fa0aaed31b5fa26200fbfe477030`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4adc3e7bb184764c09cda0a24bcf9b6ee23e83d0b4b2be7af6d99cab663058`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251121` - unknown; unknown

```console
$ docker pull odoo@sha256:3dfeca69507dc0194023d37e435726d799310b8a3da27c2fab172b37685f41d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68421115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e763f1c535f7fca4c3d5bac0efaa3e3ec09f4c251f5304e7a6e356ddd5388c88`

```dockerfile
```

-	Layers:
	-	`sha256:6604bbc0538ca467ff3fb0c3a0d0a5b3cc123cec54779b80dc36ab7a31e0cf36`  
		Last Modified: Fri, 21 Nov 2025 20:16:48 GMT  
		Size: 68.4 MB (68393961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321e0d0580b8e6cf05d0f0228ef05c6e756b13130d592ebc4e1bfd7f9db29f95`  
		Last Modified: Fri, 21 Nov 2025 20:16:50 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:18f4ead7d36dbe259ceca67dda6aafec4456509b2dccf39f86a85b1d44e4691b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:2964f9c4666ef6a5ef34ef6324ec54a94e1993b3941d3666db83ab7db13281da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687897817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88060bbc10987662bfe69a893ae28b95efb384216dd62b25e9b99ac8fac9a7f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:53 GMT
ARG TARGETARCH=amd64
# Fri, 21 Nov 2025 18:38:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:39:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:39:03 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:39:03 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:40:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:40:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:40:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:40:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:40:06 GMT
USER odoo
# Fri, 21 Nov 2025 18:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:40:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d34ac84d0f90bd397e100f55b8ae2b279b5186d94e87064a92cfa051410403`  
		Last Modified: Fri, 21 Nov 2025 19:18:37 GMT  
		Size: 254.6 MB (254557777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3de4ea1dcb394ad7102b0bc5698faf6ff3f79b75e10d8612b06c2dc0187ca2`  
		Last Modified: Fri, 21 Nov 2025 18:42:28 GMT  
		Size: 14.4 MB (14356466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2622d6b8ae2a84a8f36bf6c039b3fc4c96dfe80515d2c5ea77ba63fef67da2`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 480.0 KB (479994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88800fe7970c65fa15e083f824c4519478dbc1b8c486e962c5ba8bd41cf66f`  
		Last Modified: Fri, 21 Nov 2025 19:18:48 GMT  
		Size: 388.8 MB (388776451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca115ed5ea01074878beed6b8008578acfbc5de66e6906ca70698cb07817e3e`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3238a841c6f0e2462aeef9909f95aef97d790682d4f5ca19a264279a34bf6c`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfc90d8ce43d6e581ead6d7cfdf736619f53847ffc51109d4c5de8f07238625`  
		Last Modified: Fri, 21 Nov 2025 18:42:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11a273c8998d41e0f1d5f4e34a74c764c9f187267b2889246a7a0f604c2ead9`  
		Last Modified: Fri, 21 Nov 2025 18:42:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c272e5692065cadff7e15207d4d2b4e86ebda6357481c87dffaa3fb52b3940bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68412665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc864b9f01a5b888002e6fd65e607c82a20231fd93e134a715134974148a405`

```dockerfile
```

-	Layers:
	-	`sha256:36b67e958ab15f92464205b1c2ffe65e8f28cfc55184e9182d1d181f2abc3782`  
		Last Modified: Fri, 21 Nov 2025 20:13:06 GMT  
		Size: 68.4 MB (68385572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5185bab1b6e412966059c4ec3435b2e0196b51a89275e0579b50fc1b371dd130`  
		Last Modified: Fri, 21 Nov 2025 20:13:07 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f41de1d80ac362620acd527a3c296d1a4edd87d9fc86be86c1c1fbec37e6690f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.3 MB (684275571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c0b4e1d7fbc061ff4272c1f54bec13d56d3fa442bb80d2577028c6dac16d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:38:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:38:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:38:29 GMT
ARG TARGETARCH=arm64
# Fri, 21 Nov 2025 18:38:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:38:39 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:38:40 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:38:40 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:39:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:39:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:39:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:39:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:39:57 GMT
USER odoo
# Fri, 21 Nov 2025 18:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:39:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003fb6b0f8c2e157dad0b6b5f83834c810f7ae15d29665dfd75aeaa3d7d649f5`  
		Last Modified: Fri, 21 Nov 2025 18:48:26 GMT  
		Size: 252.0 MB (251960396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1266c4bf294b49c12008a7b8ca557a9c88209d6584266f1c7ddee68ff214b2`  
		Last Modified: Fri, 21 Nov 2025 18:42:47 GMT  
		Size: 14.3 MB (14334140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cc54ffc2287a77b24213bc10d4715a8598901370f9fed3aed86467fd88c41a`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 480.0 KB (480020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad798e7d34186abfa68256a0081ab78aa965b57dcc68b2c63d8c6531c6c14044`  
		Last Modified: Fri, 21 Nov 2025 18:48:32 GMT  
		Size: 388.6 MB (388636623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5db9fb7d5ee7e84e08884e4e6ef1e68213d3ffca6c05f03c2c59269e1f807cf`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9c46582f5a458fc9a5941da8ebf2b7dcb5242ad46c78b18f06ea20145a638`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f62cbf03e9f73f889f1df93457978b96cee136bd89934a2a74cd6f3a3353bb`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b7e8d98e3e469de687b190b2631cc9f723339b2a70134350b700d36c716cf2`  
		Last Modified: Fri, 21 Nov 2025 18:42:46 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7f804b9288ae72a6853b43e2c712e2e20ce4c33767c101583daca09c41f5d624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68420116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c07896c788320e91476932a0e130d70599e2784b2f62e5ddfdcd6e9188c71c4`

```dockerfile
```

-	Layers:
	-	`sha256:c72aa394b3094b14274a6780356f7da95a580bdde3fcdc4c2a62576a664f8acb`  
		Last Modified: Fri, 21 Nov 2025 20:14:57 GMT  
		Size: 68.4 MB (68392859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51842942d84cc0d6a28282f18085e44be411fc75ccfc066a977af6765bf8bcab`  
		Last Modified: Fri, 21 Nov 2025 20:14:58 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:4f6059a377661abd889550d22dcdde02396a25f044bace5d47abac5492d59b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.1 MB (704063362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5c0778b0e87ff5b1e282e70d40208cde19e9b085cc3039b6ab783c2aa89140`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 21 Nov 2025 18:40:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 21 Nov 2025 18:40:35 GMT
ENV ODOO_VERSION=19.0
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_RELEASE=20251121
# Fri, 21 Nov 2025 18:40:35 GMT
ARG ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
# Fri, 21 Nov 2025 18:43:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251121 ODOO_SHA=6357a789f287485b002acf6888fe8cdd45e2d5d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 21 Nov 2025 18:43:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 21 Nov 2025 18:43:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 21 Nov 2025 18:43:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 21 Nov 2025 18:43:19 GMT
USER odoo
# Fri, 21 Nov 2025 18:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Nov 2025 18:43:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b47702e52f3a5f2e8a1b2408e6843452eaec51d55389899bc0f54f156af25f`  
		Last Modified: Fri, 21 Nov 2025 18:50:44 GMT  
		Size: 14.9 MB (14885218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bed9ce04570ec2a8b46f795c12e54099f7f6bd485dea581c978739dfb9f1f4`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d694a4a80abbd45c8a3c78146036aacdb5762b0d6d9f58c13dd968f4bb0b7980`  
		Last Modified: Fri, 21 Nov 2025 19:12:55 GMT  
		Size: 389.3 MB (389313356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f16089013bb07e6d9fe5897c11fc622fb35b5663b2f703d3a531917cb98cc`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe896974271cc2a60996dc5e2036fadeb14d0e50be9eb6668a843b30abb1b237`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233572647d2aaedc04c327753f9af9cf83b7fa0aaed31b5fa26200fbfe477030`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4adc3e7bb184764c09cda0a24bcf9b6ee23e83d0b4b2be7af6d99cab663058`  
		Last Modified: Fri, 21 Nov 2025 18:50:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:3dfeca69507dc0194023d37e435726d799310b8a3da27c2fab172b37685f41d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68421115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e763f1c535f7fca4c3d5bac0efaa3e3ec09f4c251f5304e7a6e356ddd5388c88`

```dockerfile
```

-	Layers:
	-	`sha256:6604bbc0538ca467ff3fb0c3a0d0a5b3cc123cec54779b80dc36ab7a31e0cf36`  
		Last Modified: Fri, 21 Nov 2025 20:16:48 GMT  
		Size: 68.4 MB (68393961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321e0d0580b8e6cf05d0f0228ef05c6e756b13130d592ebc4e1bfd7f9db29f95`  
		Last Modified: Fri, 21 Nov 2025 20:16:50 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json
