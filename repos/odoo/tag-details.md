<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260119`](#odoo170-20260119)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260119`](#odoo180-20260119)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260119`](#odoo190-20260119)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:cfe26f3017df442161df8db55d0f1f67d5f4e486efb38297f3262f855c10c59e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:0e0ef85637b280be6d882856563cdb0831a0c5a7cdf75e8fd15bb662299c306c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.5 MB (608525289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df51d9355ac0e60dee0fa861dee0b86a858132095415023d3f803c84c8102ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:51:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:51:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:51:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:51:55 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:51:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:52:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:52:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:52:04 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 Jan 2026 17:52:04 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:52:04 GMT
ARG ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
# Tue, 20 Jan 2026 17:53:07 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:53:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:53:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:53:08 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
USER odoo
# Tue, 20 Jan 2026 17:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e741c97709b1945785bb53d1468bae62143260cfbf4ca227b59c1dabf30416`  
		Last Modified: Tue, 20 Jan 2026 17:54:43 GMT  
		Size: 233.8 MB (233821310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28390ae38c9dd94c36611b82d8e2d6d818f10ce955dca25afc72137f4423628a`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 2.6 MB (2597186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da17589aa8b3903d6bec34094d847b747ce96cfe0f25f84be54619dfaa32038`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 480.2 KB (480248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a843ca5ec6d229414e48d9bdfb8d48cab0bb8e8849c7c314ddc3ea591f838b`  
		Last Modified: Tue, 20 Jan 2026 17:54:46 GMT  
		Size: 342.1 MB (342087437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6d89ffc94252c614c733cf467cb09cc61184a5146966c64b45bbed4ec39ee`  
		Last Modified: Tue, 20 Jan 2026 17:54:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64da99e41198dc12b33a019f1207b64fc310de7fcc7392d67a31c05a06e00bc`  
		Last Modified: Tue, 20 Jan 2026 17:54:24 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f172676cdce88f98abc1108f734e7f36cbe17726aaa529d4754adbe741ca7bc`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eedb380b91e821460a816448670993169dbd16d979049c7b9ef6f07d5b8d49`  
		Last Modified: Tue, 20 Jan 2026 17:54:26 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:8f2fcb002161837bf8ce6611a91e15f4f1df8b548cf055b227644bcce4c338e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06776438d0ffde02be25f6246f48b95d62eb4d4ed0e1d8e67d59a73842a0ac48`

```dockerfile
```

-	Layers:
	-	`sha256:1bfe9fa79b0bc357c6e8da24e8f28e43cc7cd9d609ecebc35e2ac3c8b20e2234`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 41.9 MB (41869842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41625ece780f199de4e132eb53515e811fe9d22f54e2668371dd59c00e34f06e`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ece7235d839d8dc762ca6b9cbc5f80f1bd49ec352373fd158c0116584c14d078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.4 MB (603360603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0e2430e0c55cb24f8607fe43b0c5715f738f4a58cdec70c4c287a49ca68bc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:57:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:57:07 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:57:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:57:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:57:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 Jan 2026 17:57:15 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:57:15 GMT
ARG ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
# Tue, 20 Jan 2026 17:58:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:58:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:58:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:58:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
USER odoo
# Tue, 20 Jan 2026 17:58:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:58:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5392e9f9b8c753242dc56bde2aceb7d245e6bb193dc1eebb2e5a3c6ec657c55`  
		Last Modified: Tue, 20 Jan 2026 17:59:45 GMT  
		Size: 231.2 MB (231194081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7366455d1a3fff67f027823303fc7b0fd56d093ea8f5abfa3b6d51eca0ddd4`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 2.6 MB (2592358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbfdd80d68f54e67a87e1f84db2b3b3c2ceeaeb2b1306e6c2ae91bd2290ad26`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 480.3 KB (480266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b3a37e8bf6c1ece6b3c1a81d742ebd5c8c1ca80eb01e4c16aae614df64593`  
		Last Modified: Tue, 20 Jan 2026 17:59:47 GMT  
		Size: 341.7 MB (341707961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66167b6041274176f6cb491f67e5874173e01af02da49a266d5ca8ef17b21ad`  
		Last Modified: Tue, 20 Jan 2026 17:59:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a827cb477712c85fbb9b54ff0acc6177ce25cf8b121234047eecf2bf9381a00`  
		Last Modified: Tue, 20 Jan 2026 17:59:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ee1430abc8b8b5e4ee47d6126793c5529cae65b4f26492b65bb29dc5e5234d`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bced3890d693b31e366af7e1497f0b581599347d1e78bc5666a89068f89407`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f49295abac8fba19d879c3b82c12c24f73111f4ab5c135e35ce81f87343ceab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41903292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f7e56e20ac407f2b090ba02876a58fee91e5e76b672b1658c6371ae087dae1`

```dockerfile
```

-	Layers:
	-	`sha256:ec4733103790c18fdc83b53f4f7cbfab32dd775b7b1b124ea8017f703ed38465`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 41.9 MB (41876349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6af40fea65ea0951c7d9137222989eb7c2365a2b20357556c87a15c2229cc2f`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:cfe26f3017df442161df8db55d0f1f67d5f4e486efb38297f3262f855c10c59e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:0e0ef85637b280be6d882856563cdb0831a0c5a7cdf75e8fd15bb662299c306c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.5 MB (608525289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df51d9355ac0e60dee0fa861dee0b86a858132095415023d3f803c84c8102ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:51:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:51:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:51:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:51:55 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:51:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:52:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:52:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:52:04 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 Jan 2026 17:52:04 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:52:04 GMT
ARG ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
# Tue, 20 Jan 2026 17:53:07 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:53:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:53:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:53:08 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
USER odoo
# Tue, 20 Jan 2026 17:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e741c97709b1945785bb53d1468bae62143260cfbf4ca227b59c1dabf30416`  
		Last Modified: Tue, 20 Jan 2026 17:54:43 GMT  
		Size: 233.8 MB (233821310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28390ae38c9dd94c36611b82d8e2d6d818f10ce955dca25afc72137f4423628a`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 2.6 MB (2597186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da17589aa8b3903d6bec34094d847b747ce96cfe0f25f84be54619dfaa32038`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 480.2 KB (480248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a843ca5ec6d229414e48d9bdfb8d48cab0bb8e8849c7c314ddc3ea591f838b`  
		Last Modified: Tue, 20 Jan 2026 17:54:46 GMT  
		Size: 342.1 MB (342087437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6d89ffc94252c614c733cf467cb09cc61184a5146966c64b45bbed4ec39ee`  
		Last Modified: Tue, 20 Jan 2026 17:54:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64da99e41198dc12b33a019f1207b64fc310de7fcc7392d67a31c05a06e00bc`  
		Last Modified: Tue, 20 Jan 2026 17:54:24 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f172676cdce88f98abc1108f734e7f36cbe17726aaa529d4754adbe741ca7bc`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eedb380b91e821460a816448670993169dbd16d979049c7b9ef6f07d5b8d49`  
		Last Modified: Tue, 20 Jan 2026 17:54:26 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8f2fcb002161837bf8ce6611a91e15f4f1df8b548cf055b227644bcce4c338e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06776438d0ffde02be25f6246f48b95d62eb4d4ed0e1d8e67d59a73842a0ac48`

```dockerfile
```

-	Layers:
	-	`sha256:1bfe9fa79b0bc357c6e8da24e8f28e43cc7cd9d609ecebc35e2ac3c8b20e2234`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 41.9 MB (41869842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41625ece780f199de4e132eb53515e811fe9d22f54e2668371dd59c00e34f06e`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ece7235d839d8dc762ca6b9cbc5f80f1bd49ec352373fd158c0116584c14d078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.4 MB (603360603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0e2430e0c55cb24f8607fe43b0c5715f738f4a58cdec70c4c287a49ca68bc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:57:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:57:07 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:57:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:57:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:57:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 Jan 2026 17:57:15 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:57:15 GMT
ARG ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
# Tue, 20 Jan 2026 17:58:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:58:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:58:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:58:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
USER odoo
# Tue, 20 Jan 2026 17:58:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:58:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5392e9f9b8c753242dc56bde2aceb7d245e6bb193dc1eebb2e5a3c6ec657c55`  
		Last Modified: Tue, 20 Jan 2026 17:59:45 GMT  
		Size: 231.2 MB (231194081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7366455d1a3fff67f027823303fc7b0fd56d093ea8f5abfa3b6d51eca0ddd4`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 2.6 MB (2592358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbfdd80d68f54e67a87e1f84db2b3b3c2ceeaeb2b1306e6c2ae91bd2290ad26`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 480.3 KB (480266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b3a37e8bf6c1ece6b3c1a81d742ebd5c8c1ca80eb01e4c16aae614df64593`  
		Last Modified: Tue, 20 Jan 2026 17:59:47 GMT  
		Size: 341.7 MB (341707961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66167b6041274176f6cb491f67e5874173e01af02da49a266d5ca8ef17b21ad`  
		Last Modified: Tue, 20 Jan 2026 17:59:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a827cb477712c85fbb9b54ff0acc6177ce25cf8b121234047eecf2bf9381a00`  
		Last Modified: Tue, 20 Jan 2026 17:59:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ee1430abc8b8b5e4ee47d6126793c5529cae65b4f26492b65bb29dc5e5234d`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bced3890d693b31e366af7e1497f0b581599347d1e78bc5666a89068f89407`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f49295abac8fba19d879c3b82c12c24f73111f4ab5c135e35ce81f87343ceab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41903292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f7e56e20ac407f2b090ba02876a58fee91e5e76b672b1658c6371ae087dae1`

```dockerfile
```

-	Layers:
	-	`sha256:ec4733103790c18fdc83b53f4f7cbfab32dd775b7b1b124ea8017f703ed38465`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 41.9 MB (41876349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6af40fea65ea0951c7d9137222989eb7c2365a2b20357556c87a15c2229cc2f`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260119`

```console
$ docker pull odoo@sha256:cfe26f3017df442161df8db55d0f1f67d5f4e486efb38297f3262f855c10c59e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260119` - linux; amd64

```console
$ docker pull odoo@sha256:0e0ef85637b280be6d882856563cdb0831a0c5a7cdf75e8fd15bb662299c306c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.5 MB (608525289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df51d9355ac0e60dee0fa861dee0b86a858132095415023d3f803c84c8102ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:51:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:51:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:51:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:51:55 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:51:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:52:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:52:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:52:04 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 Jan 2026 17:52:04 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:52:04 GMT
ARG ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
# Tue, 20 Jan 2026 17:53:07 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:53:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:53:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:53:08 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:53:08 GMT
USER odoo
# Tue, 20 Jan 2026 17:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e741c97709b1945785bb53d1468bae62143260cfbf4ca227b59c1dabf30416`  
		Last Modified: Tue, 20 Jan 2026 17:54:43 GMT  
		Size: 233.8 MB (233821310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28390ae38c9dd94c36611b82d8e2d6d818f10ce955dca25afc72137f4423628a`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 2.6 MB (2597186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da17589aa8b3903d6bec34094d847b747ce96cfe0f25f84be54619dfaa32038`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 480.2 KB (480248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a843ca5ec6d229414e48d9bdfb8d48cab0bb8e8849c7c314ddc3ea591f838b`  
		Last Modified: Tue, 20 Jan 2026 17:54:46 GMT  
		Size: 342.1 MB (342087437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6d89ffc94252c614c733cf467cb09cc61184a5146966c64b45bbed4ec39ee`  
		Last Modified: Tue, 20 Jan 2026 17:54:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64da99e41198dc12b33a019f1207b64fc310de7fcc7392d67a31c05a06e00bc`  
		Last Modified: Tue, 20 Jan 2026 17:54:24 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f172676cdce88f98abc1108f734e7f36cbe17726aaa529d4754adbe741ca7bc`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eedb380b91e821460a816448670993169dbd16d979049c7b9ef6f07d5b8d49`  
		Last Modified: Tue, 20 Jan 2026 17:54:26 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:8f2fcb002161837bf8ce6611a91e15f4f1df8b548cf055b227644bcce4c338e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06776438d0ffde02be25f6246f48b95d62eb4d4ed0e1d8e67d59a73842a0ac48`

```dockerfile
```

-	Layers:
	-	`sha256:1bfe9fa79b0bc357c6e8da24e8f28e43cc7cd9d609ecebc35e2ac3c8b20e2234`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 41.9 MB (41869842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41625ece780f199de4e132eb53515e811fe9d22f54e2668371dd59c00e34f06e`  
		Last Modified: Tue, 20 Jan 2026 17:54:22 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260119` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ece7235d839d8dc762ca6b9cbc5f80f1bd49ec352373fd158c0116584c14d078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.4 MB (603360603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0e2430e0c55cb24f8607fe43b0c5715f738f4a58cdec70c4c287a49ca68bc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:57:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:57:07 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:57:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:57:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:57:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 Jan 2026 17:57:15 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:57:15 GMT
ARG ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
# Tue, 20 Jan 2026 17:58:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=d05da0fdc75fc57ccae2dd5b797183afb0be0ea8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:58:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:58:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:58:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:58:18 GMT
USER odoo
# Tue, 20 Jan 2026 17:58:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:58:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5392e9f9b8c753242dc56bde2aceb7d245e6bb193dc1eebb2e5a3c6ec657c55`  
		Last Modified: Tue, 20 Jan 2026 17:59:45 GMT  
		Size: 231.2 MB (231194081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7366455d1a3fff67f027823303fc7b0fd56d093ea8f5abfa3b6d51eca0ddd4`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 2.6 MB (2592358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbfdd80d68f54e67a87e1f84db2b3b3c2ceeaeb2b1306e6c2ae91bd2290ad26`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 480.3 KB (480266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b3a37e8bf6c1ece6b3c1a81d742ebd5c8c1ca80eb01e4c16aae614df64593`  
		Last Modified: Tue, 20 Jan 2026 17:59:47 GMT  
		Size: 341.7 MB (341707961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66167b6041274176f6cb491f67e5874173e01af02da49a266d5ca8ef17b21ad`  
		Last Modified: Tue, 20 Jan 2026 17:59:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a827cb477712c85fbb9b54ff0acc6177ce25cf8b121234047eecf2bf9381a00`  
		Last Modified: Tue, 20 Jan 2026 17:59:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ee1430abc8b8b5e4ee47d6126793c5529cae65b4f26492b65bb29dc5e5234d`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bced3890d693b31e366af7e1497f0b581599347d1e78bc5666a89068f89407`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:f49295abac8fba19d879c3b82c12c24f73111f4ab5c135e35ce81f87343ceab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41903292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f7e56e20ac407f2b090ba02876a58fee91e5e76b672b1658c6371ae087dae1`

```dockerfile
```

-	Layers:
	-	`sha256:ec4733103790c18fdc83b53f4f7cbfab32dd775b7b1b124ea8017f703ed38465`  
		Last Modified: Tue, 20 Jan 2026 17:59:39 GMT  
		Size: 41.9 MB (41876349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6af40fea65ea0951c7d9137222989eb7c2365a2b20357556c87a15c2229cc2f`  
		Last Modified: Tue, 20 Jan 2026 17:59:36 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:a419f4e386bbc4826b0850907e5831c94d2a963a0f067fe53205cea365678e01
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
$ docker pull odoo@sha256:76e9e8eaf613bb2b5637713672073ea410964f69cde25ef5fad883931f43a381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.6 MB (681595307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abef02c36e0ed230a09003ff4b8309c7ad7d76ac165ec18a6982c0f63bc2a68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:49:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:49:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:49:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:49:21 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:49:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:49:30 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:49:31 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:49:31 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 Jan 2026 17:49:31 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:49:31 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:50:23 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:50:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:50:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:50:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:50:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:50:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
USER odoo
# Tue, 20 Jan 2026 17:50:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:50:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7363844a9bc712673d51387979446fdce76368a200cbbab0c1d05ae9323dc2d`  
		Last Modified: Tue, 20 Jan 2026 17:52:21 GMT  
		Size: 254.6 MB (254560463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2636cfedf2cc50a6ba3fa7daa0edaa97f3c68d73d534b92d9137cf7e0b1ca30f`  
		Last Modified: Tue, 20 Jan 2026 17:52:11 GMT  
		Size: 14.4 MB (14356570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7e32146e066915a3cd972249a3d3679ac9951c0ab5e1e14df0aa2a1b33884c`  
		Last Modified: Tue, 20 Jan 2026 17:52:09 GMT  
		Size: 480.0 KB (480006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd1077dc2224aa904b91214a8eb092a0d6247f9026ad2f7df6464519d41a61b`  
		Last Modified: Tue, 20 Jan 2026 17:52:24 GMT  
		Size: 382.5 MB (382469811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb87d02673c980537bd2c1cc6742d8bb2c8731d1bb4a01a22e37417388f3056`  
		Last Modified: Tue, 20 Jan 2026 17:52:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8872d6b9f48ebb41841c693a4628a0af85850e4600f20dd431a60530af9e31d4`  
		Last Modified: Tue, 20 Jan 2026 17:52:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377734303d8c7cf0751e8a54a3dfd3998e85078935d354600b0a6b938873185`  
		Last Modified: Tue, 20 Jan 2026 17:52:12 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b9d1364c0e7b7089dadd9921e3c95308e6581176a4c89790205d9cb1fb0dce`  
		Last Modified: Tue, 20 Jan 2026 17:52:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:ef56218008dba19c636ab4e82fcb242ff4dccf0e51b01dec944a5e964d7257a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61535848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e77a3c65ebf4bebcca6a33b0349bd4097168450116afc93bb1b2e4ee718463`

```dockerfile
```

-	Layers:
	-	`sha256:34bb2887b84f8e243809158cf4e9aa25db9c14e2402f1bd5b3c39d011a8f7c08`  
		Last Modified: Tue, 20 Jan 2026 17:52:13 GMT  
		Size: 61.5 MB (61509049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f11503b5a84104cc758f0f55e85689eae2c94742ed5d422eafc2c7e22a81ec8`  
		Last Modified: Tue, 20 Jan 2026 17:52:09 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:079e5c9cfc52338568a989787d13c09a1b9f6ae38fb4a1564650ba2feb64e69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.9 MB (677947851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94afee94a68ebfe770653d251b9e3139efb6c2be5a713d5540a3d04b315eabc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:54:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:54:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:54:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:54:36 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:54:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:54:45 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:54:46 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:54:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 Jan 2026 17:54:46 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:54:46 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:55:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:55:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:55:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:55:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
USER odoo
# Tue, 20 Jan 2026 17:55:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:55:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ab2f5931c1623660fb8dc5db8ff82bb9884cc727525c9ac04f76d51001d57`  
		Last Modified: Tue, 20 Jan 2026 17:58:07 GMT  
		Size: 252.0 MB (251961272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58af47750d61fc39caa1c4d35bbc58c386bc34ca91782d75579236a4753a1f63`  
		Last Modified: Tue, 20 Jan 2026 17:57:59 GMT  
		Size: 14.3 MB (14334313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903dab9fea90d8828b7be83e5b62f1f16f5744b9d1b0d762e0e097cb3f844086`  
		Last Modified: Tue, 20 Jan 2026 17:57:58 GMT  
		Size: 480.0 KB (480003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efbebb20f3a7dd01870e80e74a0932f24526ec58124a5ef980126f15440f019`  
		Last Modified: Tue, 20 Jan 2026 17:58:09 GMT  
		Size: 382.3 MB (382306002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667551ff79de8eda7221cede516782f210f76be7c31930074e44bf63a1190c21`  
		Last Modified: Tue, 20 Jan 2026 17:57:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b9389214953a48b5ee96ab920ed2208a9ebd64967934d0a0e1946ccf2917b1`  
		Last Modified: Tue, 20 Jan 2026 17:58:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ecbeb1053a9b4fa1ff62b29cc89d992ebbd04d1e6f9d15fc595f83ec4d7e56`  
		Last Modified: Tue, 20 Jan 2026 17:58:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c7876fb9b357663b740b143e681cf807c2e3157516cd08f2bff488d922958`  
		Last Modified: Tue, 20 Jan 2026 17:58:02 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:9dcb38d774a449e95adc4e57c4ae4a5719671ad26226d09b1c3aa80b1e7d993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61543275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dac4d1306fd5237891c9882ff7d90155fda787d2ec7530f00eca5c623ed5fb0`

```dockerfile
```

-	Layers:
	-	`sha256:29247df502690c4cda4175004f4782feb32cbaef9ecfc2241444a2bcb530f47f`  
		Last Modified: Tue, 20 Jan 2026 17:58:01 GMT  
		Size: 61.5 MB (61516324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d578c25730bcc92567f5ef3d916d3dcc5a468501d9700d16fdcf0e5eb32b4cb`  
		Last Modified: Tue, 20 Jan 2026 17:57:58 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:6c65a9488771d2393814178a6ce8c9d566df3a8b7b99e19bc2ce9f4f9b85688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.8 MB (697772779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e91b4206a914ec7bb5ce34d6289bed577c94f3501d3d18c759a27ba841c274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20260119
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:56:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:56:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:56:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:56:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:56:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:56:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:56:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:56:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:56:11 GMT
USER odoo
# Tue, 20 Jan 2026 17:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:56:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e509c5c3b02efb80337015753b7d257c985e4f304db03c2943f1c45e512774`  
		Last Modified: Tue, 20 Jan 2026 18:04:28 GMT  
		Size: 383.0 MB (383012912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09e58a51b871e85dd6fdf0f7b31b3d40df6625754922822638fa31fd2c331c9`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35aeed090e81e665e0004cc8b08a79072b7c4fad395e7f8919d8651b3671187`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77847d86d593de0147b4a1d18d28018aeecff6e8ccbd2a24844ba38a06fb708b`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839fceb73b302378716ab1ff923eb98668576ddd7c022bc33ca4ab61b2e27b2`  
		Last Modified: Tue, 20 Jan 2026 18:04:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b5efadad7d1a76d57fc27ef9cbeaa6e7d003ad911ac8dcc654b2ed5f1a282f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61544287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ea98e1bb65829c5e2cdb5700f8f858f87af7eb23ab62c4a52ad4055172f7c8`

```dockerfile
```

-	Layers:
	-	`sha256:78617c40eea03bdee11a9c75a6f51bb103766b5e4ea43e167206734f12ca0d07`  
		Last Modified: Tue, 20 Jan 2026 18:04:21 GMT  
		Size: 61.5 MB (61517432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349f75b1329f69dd70d7d6f4b9c4215a9301667a7e525455d201b9d26955ddda`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:a419f4e386bbc4826b0850907e5831c94d2a963a0f067fe53205cea365678e01
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
$ docker pull odoo@sha256:76e9e8eaf613bb2b5637713672073ea410964f69cde25ef5fad883931f43a381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.6 MB (681595307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abef02c36e0ed230a09003ff4b8309c7ad7d76ac165ec18a6982c0f63bc2a68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:49:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:49:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:49:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:49:21 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:49:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:49:30 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:49:31 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:49:31 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 Jan 2026 17:49:31 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:49:31 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:50:23 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:50:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:50:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:50:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:50:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:50:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
USER odoo
# Tue, 20 Jan 2026 17:50:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:50:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7363844a9bc712673d51387979446fdce76368a200cbbab0c1d05ae9323dc2d`  
		Last Modified: Tue, 20 Jan 2026 17:52:21 GMT  
		Size: 254.6 MB (254560463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2636cfedf2cc50a6ba3fa7daa0edaa97f3c68d73d534b92d9137cf7e0b1ca30f`  
		Last Modified: Tue, 20 Jan 2026 17:52:11 GMT  
		Size: 14.4 MB (14356570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7e32146e066915a3cd972249a3d3679ac9951c0ab5e1e14df0aa2a1b33884c`  
		Last Modified: Tue, 20 Jan 2026 17:52:09 GMT  
		Size: 480.0 KB (480006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd1077dc2224aa904b91214a8eb092a0d6247f9026ad2f7df6464519d41a61b`  
		Last Modified: Tue, 20 Jan 2026 17:52:24 GMT  
		Size: 382.5 MB (382469811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb87d02673c980537bd2c1cc6742d8bb2c8731d1bb4a01a22e37417388f3056`  
		Last Modified: Tue, 20 Jan 2026 17:52:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8872d6b9f48ebb41841c693a4628a0af85850e4600f20dd431a60530af9e31d4`  
		Last Modified: Tue, 20 Jan 2026 17:52:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377734303d8c7cf0751e8a54a3dfd3998e85078935d354600b0a6b938873185`  
		Last Modified: Tue, 20 Jan 2026 17:52:12 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b9d1364c0e7b7089dadd9921e3c95308e6581176a4c89790205d9cb1fb0dce`  
		Last Modified: Tue, 20 Jan 2026 17:52:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ef56218008dba19c636ab4e82fcb242ff4dccf0e51b01dec944a5e964d7257a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61535848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e77a3c65ebf4bebcca6a33b0349bd4097168450116afc93bb1b2e4ee718463`

```dockerfile
```

-	Layers:
	-	`sha256:34bb2887b84f8e243809158cf4e9aa25db9c14e2402f1bd5b3c39d011a8f7c08`  
		Last Modified: Tue, 20 Jan 2026 17:52:13 GMT  
		Size: 61.5 MB (61509049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f11503b5a84104cc758f0f55e85689eae2c94742ed5d422eafc2c7e22a81ec8`  
		Last Modified: Tue, 20 Jan 2026 17:52:09 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:079e5c9cfc52338568a989787d13c09a1b9f6ae38fb4a1564650ba2feb64e69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.9 MB (677947851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94afee94a68ebfe770653d251b9e3139efb6c2be5a713d5540a3d04b315eabc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:54:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:54:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:54:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:54:36 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:54:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:54:45 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:54:46 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:54:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 Jan 2026 17:54:46 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:54:46 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:55:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:55:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:55:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:55:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
USER odoo
# Tue, 20 Jan 2026 17:55:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:55:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ab2f5931c1623660fb8dc5db8ff82bb9884cc727525c9ac04f76d51001d57`  
		Last Modified: Tue, 20 Jan 2026 17:58:07 GMT  
		Size: 252.0 MB (251961272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58af47750d61fc39caa1c4d35bbc58c386bc34ca91782d75579236a4753a1f63`  
		Last Modified: Tue, 20 Jan 2026 17:57:59 GMT  
		Size: 14.3 MB (14334313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903dab9fea90d8828b7be83e5b62f1f16f5744b9d1b0d762e0e097cb3f844086`  
		Last Modified: Tue, 20 Jan 2026 17:57:58 GMT  
		Size: 480.0 KB (480003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efbebb20f3a7dd01870e80e74a0932f24526ec58124a5ef980126f15440f019`  
		Last Modified: Tue, 20 Jan 2026 17:58:09 GMT  
		Size: 382.3 MB (382306002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667551ff79de8eda7221cede516782f210f76be7c31930074e44bf63a1190c21`  
		Last Modified: Tue, 20 Jan 2026 17:57:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b9389214953a48b5ee96ab920ed2208a9ebd64967934d0a0e1946ccf2917b1`  
		Last Modified: Tue, 20 Jan 2026 17:58:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ecbeb1053a9b4fa1ff62b29cc89d992ebbd04d1e6f9d15fc595f83ec4d7e56`  
		Last Modified: Tue, 20 Jan 2026 17:58:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c7876fb9b357663b740b143e681cf807c2e3157516cd08f2bff488d922958`  
		Last Modified: Tue, 20 Jan 2026 17:58:02 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9dcb38d774a449e95adc4e57c4ae4a5719671ad26226d09b1c3aa80b1e7d993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61543275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dac4d1306fd5237891c9882ff7d90155fda787d2ec7530f00eca5c623ed5fb0`

```dockerfile
```

-	Layers:
	-	`sha256:29247df502690c4cda4175004f4782feb32cbaef9ecfc2241444a2bcb530f47f`  
		Last Modified: Tue, 20 Jan 2026 17:58:01 GMT  
		Size: 61.5 MB (61516324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d578c25730bcc92567f5ef3d916d3dcc5a468501d9700d16fdcf0e5eb32b4cb`  
		Last Modified: Tue, 20 Jan 2026 17:57:58 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:6c65a9488771d2393814178a6ce8c9d566df3a8b7b99e19bc2ce9f4f9b85688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.8 MB (697772779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e91b4206a914ec7bb5ce34d6289bed577c94f3501d3d18c759a27ba841c274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20260119
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:56:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:56:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:56:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:56:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:56:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:56:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:56:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:56:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:56:11 GMT
USER odoo
# Tue, 20 Jan 2026 17:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:56:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e509c5c3b02efb80337015753b7d257c985e4f304db03c2943f1c45e512774`  
		Last Modified: Tue, 20 Jan 2026 18:04:28 GMT  
		Size: 383.0 MB (383012912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09e58a51b871e85dd6fdf0f7b31b3d40df6625754922822638fa31fd2c331c9`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35aeed090e81e665e0004cc8b08a79072b7c4fad395e7f8919d8651b3671187`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77847d86d593de0147b4a1d18d28018aeecff6e8ccbd2a24844ba38a06fb708b`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839fceb73b302378716ab1ff923eb98668576ddd7c022bc33ca4ab61b2e27b2`  
		Last Modified: Tue, 20 Jan 2026 18:04:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b5efadad7d1a76d57fc27ef9cbeaa6e7d003ad911ac8dcc654b2ed5f1a282f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61544287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ea98e1bb65829c5e2cdb5700f8f858f87af7eb23ab62c4a52ad4055172f7c8`

```dockerfile
```

-	Layers:
	-	`sha256:78617c40eea03bdee11a9c75a6f51bb103766b5e4ea43e167206734f12ca0d07`  
		Last Modified: Tue, 20 Jan 2026 18:04:21 GMT  
		Size: 61.5 MB (61517432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349f75b1329f69dd70d7d6f4b9c4215a9301667a7e525455d201b9d26955ddda`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260119`

```console
$ docker pull odoo@sha256:a419f4e386bbc4826b0850907e5831c94d2a963a0f067fe53205cea365678e01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260119` - linux; amd64

```console
$ docker pull odoo@sha256:76e9e8eaf613bb2b5637713672073ea410964f69cde25ef5fad883931f43a381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.6 MB (681595307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abef02c36e0ed230a09003ff4b8309c7ad7d76ac165ec18a6982c0f63bc2a68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:49:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:49:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:49:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:49:21 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:49:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:49:30 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:49:31 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:49:31 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 Jan 2026 17:49:31 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:49:31 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:50:23 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:50:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:50:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:50:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:50:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:50:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:50:24 GMT
USER odoo
# Tue, 20 Jan 2026 17:50:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:50:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7363844a9bc712673d51387979446fdce76368a200cbbab0c1d05ae9323dc2d`  
		Last Modified: Tue, 20 Jan 2026 17:52:21 GMT  
		Size: 254.6 MB (254560463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2636cfedf2cc50a6ba3fa7daa0edaa97f3c68d73d534b92d9137cf7e0b1ca30f`  
		Last Modified: Tue, 20 Jan 2026 17:52:11 GMT  
		Size: 14.4 MB (14356570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7e32146e066915a3cd972249a3d3679ac9951c0ab5e1e14df0aa2a1b33884c`  
		Last Modified: Tue, 20 Jan 2026 17:52:09 GMT  
		Size: 480.0 KB (480006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd1077dc2224aa904b91214a8eb092a0d6247f9026ad2f7df6464519d41a61b`  
		Last Modified: Tue, 20 Jan 2026 17:52:24 GMT  
		Size: 382.5 MB (382469811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb87d02673c980537bd2c1cc6742d8bb2c8731d1bb4a01a22e37417388f3056`  
		Last Modified: Tue, 20 Jan 2026 17:52:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8872d6b9f48ebb41841c693a4628a0af85850e4600f20dd431a60530af9e31d4`  
		Last Modified: Tue, 20 Jan 2026 17:52:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377734303d8c7cf0751e8a54a3dfd3998e85078935d354600b0a6b938873185`  
		Last Modified: Tue, 20 Jan 2026 17:52:12 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b9d1364c0e7b7089dadd9921e3c95308e6581176a4c89790205d9cb1fb0dce`  
		Last Modified: Tue, 20 Jan 2026 17:52:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:ef56218008dba19c636ab4e82fcb242ff4dccf0e51b01dec944a5e964d7257a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61535848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e77a3c65ebf4bebcca6a33b0349bd4097168450116afc93bb1b2e4ee718463`

```dockerfile
```

-	Layers:
	-	`sha256:34bb2887b84f8e243809158cf4e9aa25db9c14e2402f1bd5b3c39d011a8f7c08`  
		Last Modified: Tue, 20 Jan 2026 17:52:13 GMT  
		Size: 61.5 MB (61509049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f11503b5a84104cc758f0f55e85689eae2c94742ed5d422eafc2c7e22a81ec8`  
		Last Modified: Tue, 20 Jan 2026 17:52:09 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260119` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:079e5c9cfc52338568a989787d13c09a1b9f6ae38fb4a1564650ba2feb64e69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.9 MB (677947851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94afee94a68ebfe770653d251b9e3139efb6c2be5a713d5540a3d04b315eabc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:54:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:54:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:54:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:54:36 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:54:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:54:45 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:54:46 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:54:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 Jan 2026 17:54:46 GMT
ARG ODOO_RELEASE=20260119
# Tue, 20 Jan 2026 17:54:46 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:55:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:55:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:55:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:55:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:55:44 GMT
USER odoo
# Tue, 20 Jan 2026 17:55:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:55:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ab2f5931c1623660fb8dc5db8ff82bb9884cc727525c9ac04f76d51001d57`  
		Last Modified: Tue, 20 Jan 2026 17:58:07 GMT  
		Size: 252.0 MB (251961272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58af47750d61fc39caa1c4d35bbc58c386bc34ca91782d75579236a4753a1f63`  
		Last Modified: Tue, 20 Jan 2026 17:57:59 GMT  
		Size: 14.3 MB (14334313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903dab9fea90d8828b7be83e5b62f1f16f5744b9d1b0d762e0e097cb3f844086`  
		Last Modified: Tue, 20 Jan 2026 17:57:58 GMT  
		Size: 480.0 KB (480003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efbebb20f3a7dd01870e80e74a0932f24526ec58124a5ef980126f15440f019`  
		Last Modified: Tue, 20 Jan 2026 17:58:09 GMT  
		Size: 382.3 MB (382306002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667551ff79de8eda7221cede516782f210f76be7c31930074e44bf63a1190c21`  
		Last Modified: Tue, 20 Jan 2026 17:57:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b9389214953a48b5ee96ab920ed2208a9ebd64967934d0a0e1946ccf2917b1`  
		Last Modified: Tue, 20 Jan 2026 17:58:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ecbeb1053a9b4fa1ff62b29cc89d992ebbd04d1e6f9d15fc595f83ec4d7e56`  
		Last Modified: Tue, 20 Jan 2026 17:58:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c7876fb9b357663b740b143e681cf807c2e3157516cd08f2bff488d922958`  
		Last Modified: Tue, 20 Jan 2026 17:58:02 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:9dcb38d774a449e95adc4e57c4ae4a5719671ad26226d09b1c3aa80b1e7d993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61543275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dac4d1306fd5237891c9882ff7d90155fda787d2ec7530f00eca5c623ed5fb0`

```dockerfile
```

-	Layers:
	-	`sha256:29247df502690c4cda4175004f4782feb32cbaef9ecfc2241444a2bcb530f47f`  
		Last Modified: Tue, 20 Jan 2026 17:58:01 GMT  
		Size: 61.5 MB (61516324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d578c25730bcc92567f5ef3d916d3dcc5a468501d9700d16fdcf0e5eb32b4cb`  
		Last Modified: Tue, 20 Jan 2026 17:57:58 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260119` - linux; ppc64le

```console
$ docker pull odoo@sha256:6c65a9488771d2393814178a6ce8c9d566df3a8b7b99e19bc2ce9f4f9b85688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.8 MB (697772779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e91b4206a914ec7bb5ce34d6289bed577c94f3501d3d18c759a27ba841c274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20260119
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
# Tue, 20 Jan 2026 17:56:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:56:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:56:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:56:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260119 ODOO_SHA=798dfc952eed08e0d976364c26dc47a45535be70
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:56:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:56:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:56:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:56:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:56:11 GMT
USER odoo
# Tue, 20 Jan 2026 17:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:56:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e509c5c3b02efb80337015753b7d257c985e4f304db03c2943f1c45e512774`  
		Last Modified: Tue, 20 Jan 2026 18:04:28 GMT  
		Size: 383.0 MB (383012912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09e58a51b871e85dd6fdf0f7b31b3d40df6625754922822638fa31fd2c331c9`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35aeed090e81e665e0004cc8b08a79072b7c4fad395e7f8919d8651b3671187`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77847d86d593de0147b4a1d18d28018aeecff6e8ccbd2a24844ba38a06fb708b`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839fceb73b302378716ab1ff923eb98668576ddd7c022bc33ca4ab61b2e27b2`  
		Last Modified: Tue, 20 Jan 2026 18:04:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:b5efadad7d1a76d57fc27ef9cbeaa6e7d003ad911ac8dcc654b2ed5f1a282f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61544287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ea98e1bb65829c5e2cdb5700f8f858f87af7eb23ab62c4a52ad4055172f7c8`

```dockerfile
```

-	Layers:
	-	`sha256:78617c40eea03bdee11a9c75a6f51bb103766b5e4ea43e167206734f12ca0d07`  
		Last Modified: Tue, 20 Jan 2026 18:04:21 GMT  
		Size: 61.5 MB (61517432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349f75b1329f69dd70d7d6f4b9c4215a9301667a7e525455d201b9d26955ddda`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:6116ea0d16e143c780d065316bba04e8f68d93d8418eaf1672f417b368b0a5fe
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
$ docker pull odoo@sha256:9f84fca1a2a5669177e38e90a53200401adfe4f26b14b6834cee0a7879c2db4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.2 MB (696151267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375997b4a9ea1b4a5a073a19fc914ac63a0a1a1a3676c67ef3db8bd93cf1e0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:48:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:48:17 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:48:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:48:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:49:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:49:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:49:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:49:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
USER odoo
# Tue, 20 Jan 2026 17:49:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:49:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e32c44d64b22b09f9b27047dd9d078509daa81ea8cc7c59831f2ff6befd57`  
		Last Modified: Tue, 20 Jan 2026 17:51:42 GMT  
		Size: 254.6 MB (254560297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e21283126d6c3bbdb627e3db9f3fd50783640a49de04ba2796b7889fcdd4fcb`  
		Last Modified: Tue, 20 Jan 2026 17:51:34 GMT  
		Size: 14.4 MB (14356589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa583dfe843366b6ca2700914026e1a6867c21ea46ecc8444ca75c0d8cb423a`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 480.0 KB (479991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b3ebfd50b36d69135a863f2796eb6d703981b97f26b2a570274dbd0a024e88`  
		Last Modified: Tue, 20 Jan 2026 17:51:45 GMT  
		Size: 397.0 MB (397025938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f24605144f794459756dd6e6a45533cba89c4216ca6f4f919f139939951eac`  
		Last Modified: Tue, 20 Jan 2026 17:51:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2546c91a4bd0c90145324305aff6536e6ca5a74fb0cd1a1f706b904272daebe`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae10fefbbe87fc9f138f54688ea28d77514fb10f581e284976d80c21db02b54`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa435c5f17762fe361d40de34745d9aa8e31cb4d4e5cb7ecf9c3949be897c1d`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:ab577b18cce05ed8d8cf55df209a1aab88871fd8e8e8a838cd7cae184115f3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69262293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eed4058ffe6e3d2d0bb402d76545097fc61b9da69a197cad7e854bef8ff6e09`

```dockerfile
```

-	Layers:
	-	`sha256:03de055bb367e59e8e1210ccf50bbb3b35d8309cdca25458ab538a33eabc23f1`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 69.2 MB (69235200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a778bc765d0a3169bbc8c628f33dd0ffdab45add71fcfe8bc3b95aaaf504e75`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e035eb915c3a6e68734810d287d8ac28d9ceab8116389ce99e2b25b97a637120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.5 MB (692520977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27d1e3e4b23fc8a5da3581690f44a07df0f5d24c9ea706e4dbd692f7bfc8a37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:53:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:53:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:53:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:53:37 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:53:37 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:53:47 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:54:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:54:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:54:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:54:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
USER odoo
# Tue, 20 Jan 2026 17:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:54:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d3f7efb0b6437e6dad992249a9e9f212f4c429f91c18e1dd089be44e839eca`  
		Last Modified: Tue, 20 Jan 2026 17:57:50 GMT  
		Size: 252.0 MB (251960576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25358a67828d3d7ef6213e1eaeb9ad2660e4adaa4d1045483b465f96f6241b4c`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 14.3 MB (14334234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa0707f65e802f83913204602cbb05dc9fcc134626f7dc580d58a445b250fa9`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3919195b79dea6685eec4fb80e6282fd7f0c9ef1483d8d949a2dab30496fb9`  
		Last Modified: Tue, 20 Jan 2026 17:57:53 GMT  
		Size: 396.9 MB (396879902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f41f0f5bdbc86cb88249d87017d8984b91c56043b40d472af5ae0a894127be`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652adaa52722dd1cbcb106e97d293ede808015890010e4de5cec1de7b983f524`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a70e3e541f9b9f69ac58af6c7f14bc609065396f4d4b94dbca35e70c1118c1`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a9d8e8a22ca44f40837c40ee3fd9ef6c602f5d8580019f150efb926895b4a5`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:88c7505587a949ee392a0b1d9d547e0545403385261a6f847d1c77ba46c9b154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69269743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e16f0d2ac1ab59b61d795b2d232c0803dd6f657541b92c1b82abab1ea65d20`

```dockerfile
```

-	Layers:
	-	`sha256:aa63d456dfdc200fbfc53f2b4b3fa6d0c037a64a00a799d9b3e0b48efeec2938`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 69.2 MB (69242487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8ae7028b78d75057cae67cb5e00d79d3d23023bde2352f3377118078720d14`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:9833984eb447737f2fcda5c0ad5553e08c302136773fa19a378dd96968ad6e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.3 MB (712333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2838fcf1b6bc1ce44196fea1c9ee681af72f3a3b1578f1db8fdf4fce21957e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20260118
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:56:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:56:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:56:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:56:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:56:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:56:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:56:11 GMT
USER odoo
# Tue, 20 Jan 2026 17:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:56:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151ffb267c0a5be1759a65975327bab5213504b6c8bc3ea17de7b5a0b34a594`  
		Last Modified: Tue, 20 Jan 2026 18:04:29 GMT  
		Size: 397.6 MB (397573416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da15feec4aba697fcd38284d523426609089fc0119fe707762686d3398604c`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea6c0b655df738672b31a89ff5484495408fc1f6585df60070e67c5b77be5f`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab1b831bf4246d4385d80d093f81276ec85cfff2b85373698308100858b7d4`  
		Last Modified: Tue, 20 Jan 2026 18:04:18 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f868fad0c0bd07e104728719b1a389633405002728f82258eaa94072a4913`  
		Last Modified: Tue, 20 Jan 2026 18:04:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:d638e1a531945adf4046a18205acf241355cd86f5f379b57922e75c9884006f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69270744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43168bb406f693b975ad2749638d6e7f202905a70c08860fdf2725f50be00027`

```dockerfile
```

-	Layers:
	-	`sha256:bad7b514a7cfe62c5e6bb9f9973d52c5cfcdbf7c66f32c7b71603f3a42397b7e`  
		Last Modified: Tue, 20 Jan 2026 18:04:22 GMT  
		Size: 69.2 MB (69243589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb21a1984fa2c6049eed77bbcef06aaee981d00b8733f7a8772c877809cb98af`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:6116ea0d16e143c780d065316bba04e8f68d93d8418eaf1672f417b368b0a5fe
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
$ docker pull odoo@sha256:9f84fca1a2a5669177e38e90a53200401adfe4f26b14b6834cee0a7879c2db4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.2 MB (696151267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375997b4a9ea1b4a5a073a19fc914ac63a0a1a1a3676c67ef3db8bd93cf1e0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:48:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:48:17 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:48:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:48:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:49:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:49:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:49:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:49:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
USER odoo
# Tue, 20 Jan 2026 17:49:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:49:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e32c44d64b22b09f9b27047dd9d078509daa81ea8cc7c59831f2ff6befd57`  
		Last Modified: Tue, 20 Jan 2026 17:51:42 GMT  
		Size: 254.6 MB (254560297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e21283126d6c3bbdb627e3db9f3fd50783640a49de04ba2796b7889fcdd4fcb`  
		Last Modified: Tue, 20 Jan 2026 17:51:34 GMT  
		Size: 14.4 MB (14356589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa583dfe843366b6ca2700914026e1a6867c21ea46ecc8444ca75c0d8cb423a`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 480.0 KB (479991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b3ebfd50b36d69135a863f2796eb6d703981b97f26b2a570274dbd0a024e88`  
		Last Modified: Tue, 20 Jan 2026 17:51:45 GMT  
		Size: 397.0 MB (397025938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f24605144f794459756dd6e6a45533cba89c4216ca6f4f919f139939951eac`  
		Last Modified: Tue, 20 Jan 2026 17:51:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2546c91a4bd0c90145324305aff6536e6ca5a74fb0cd1a1f706b904272daebe`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae10fefbbe87fc9f138f54688ea28d77514fb10f581e284976d80c21db02b54`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa435c5f17762fe361d40de34745d9aa8e31cb4d4e5cb7ecf9c3949be897c1d`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ab577b18cce05ed8d8cf55df209a1aab88871fd8e8e8a838cd7cae184115f3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69262293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eed4058ffe6e3d2d0bb402d76545097fc61b9da69a197cad7e854bef8ff6e09`

```dockerfile
```

-	Layers:
	-	`sha256:03de055bb367e59e8e1210ccf50bbb3b35d8309cdca25458ab538a33eabc23f1`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 69.2 MB (69235200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a778bc765d0a3169bbc8c628f33dd0ffdab45add71fcfe8bc3b95aaaf504e75`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e035eb915c3a6e68734810d287d8ac28d9ceab8116389ce99e2b25b97a637120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.5 MB (692520977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27d1e3e4b23fc8a5da3581690f44a07df0f5d24c9ea706e4dbd692f7bfc8a37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:53:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:53:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:53:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:53:37 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:53:37 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:53:47 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:54:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:54:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:54:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:54:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
USER odoo
# Tue, 20 Jan 2026 17:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:54:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d3f7efb0b6437e6dad992249a9e9f212f4c429f91c18e1dd089be44e839eca`  
		Last Modified: Tue, 20 Jan 2026 17:57:50 GMT  
		Size: 252.0 MB (251960576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25358a67828d3d7ef6213e1eaeb9ad2660e4adaa4d1045483b465f96f6241b4c`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 14.3 MB (14334234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa0707f65e802f83913204602cbb05dc9fcc134626f7dc580d58a445b250fa9`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3919195b79dea6685eec4fb80e6282fd7f0c9ef1483d8d949a2dab30496fb9`  
		Last Modified: Tue, 20 Jan 2026 17:57:53 GMT  
		Size: 396.9 MB (396879902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f41f0f5bdbc86cb88249d87017d8984b91c56043b40d472af5ae0a894127be`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652adaa52722dd1cbcb106e97d293ede808015890010e4de5cec1de7b983f524`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a70e3e541f9b9f69ac58af6c7f14bc609065396f4d4b94dbca35e70c1118c1`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a9d8e8a22ca44f40837c40ee3fd9ef6c602f5d8580019f150efb926895b4a5`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:88c7505587a949ee392a0b1d9d547e0545403385261a6f847d1c77ba46c9b154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69269743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e16f0d2ac1ab59b61d795b2d232c0803dd6f657541b92c1b82abab1ea65d20`

```dockerfile
```

-	Layers:
	-	`sha256:aa63d456dfdc200fbfc53f2b4b3fa6d0c037a64a00a799d9b3e0b48efeec2938`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 69.2 MB (69242487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8ae7028b78d75057cae67cb5e00d79d3d23023bde2352f3377118078720d14`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:9833984eb447737f2fcda5c0ad5553e08c302136773fa19a378dd96968ad6e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.3 MB (712333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2838fcf1b6bc1ce44196fea1c9ee681af72f3a3b1578f1db8fdf4fce21957e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20260118
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:56:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:56:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:56:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:56:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:56:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:56:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:56:11 GMT
USER odoo
# Tue, 20 Jan 2026 17:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:56:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151ffb267c0a5be1759a65975327bab5213504b6c8bc3ea17de7b5a0b34a594`  
		Last Modified: Tue, 20 Jan 2026 18:04:29 GMT  
		Size: 397.6 MB (397573416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da15feec4aba697fcd38284d523426609089fc0119fe707762686d3398604c`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea6c0b655df738672b31a89ff5484495408fc1f6585df60070e67c5b77be5f`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab1b831bf4246d4385d80d093f81276ec85cfff2b85373698308100858b7d4`  
		Last Modified: Tue, 20 Jan 2026 18:04:18 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f868fad0c0bd07e104728719b1a389633405002728f82258eaa94072a4913`  
		Last Modified: Tue, 20 Jan 2026 18:04:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d638e1a531945adf4046a18205acf241355cd86f5f379b57922e75c9884006f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69270744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43168bb406f693b975ad2749638d6e7f202905a70c08860fdf2725f50be00027`

```dockerfile
```

-	Layers:
	-	`sha256:bad7b514a7cfe62c5e6bb9f9973d52c5cfcdbf7c66f32c7b71603f3a42397b7e`  
		Last Modified: Tue, 20 Jan 2026 18:04:22 GMT  
		Size: 69.2 MB (69243589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb21a1984fa2c6049eed77bbcef06aaee981d00b8733f7a8772c877809cb98af`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260119`

```console
$ docker pull odoo@sha256:6116ea0d16e143c780d065316bba04e8f68d93d8418eaf1672f417b368b0a5fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260119` - linux; amd64

```console
$ docker pull odoo@sha256:9f84fca1a2a5669177e38e90a53200401adfe4f26b14b6834cee0a7879c2db4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.2 MB (696151267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375997b4a9ea1b4a5a073a19fc914ac63a0a1a1a3676c67ef3db8bd93cf1e0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:48:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:48:17 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:48:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:48:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:49:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:49:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:49:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:49:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
USER odoo
# Tue, 20 Jan 2026 17:49:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:49:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e32c44d64b22b09f9b27047dd9d078509daa81ea8cc7c59831f2ff6befd57`  
		Last Modified: Tue, 20 Jan 2026 17:51:42 GMT  
		Size: 254.6 MB (254560297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e21283126d6c3bbdb627e3db9f3fd50783640a49de04ba2796b7889fcdd4fcb`  
		Last Modified: Tue, 20 Jan 2026 17:51:34 GMT  
		Size: 14.4 MB (14356589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa583dfe843366b6ca2700914026e1a6867c21ea46ecc8444ca75c0d8cb423a`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 480.0 KB (479991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b3ebfd50b36d69135a863f2796eb6d703981b97f26b2a570274dbd0a024e88`  
		Last Modified: Tue, 20 Jan 2026 17:51:45 GMT  
		Size: 397.0 MB (397025938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f24605144f794459756dd6e6a45533cba89c4216ca6f4f919f139939951eac`  
		Last Modified: Tue, 20 Jan 2026 17:51:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2546c91a4bd0c90145324305aff6536e6ca5a74fb0cd1a1f706b904272daebe`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae10fefbbe87fc9f138f54688ea28d77514fb10f581e284976d80c21db02b54`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa435c5f17762fe361d40de34745d9aa8e31cb4d4e5cb7ecf9c3949be897c1d`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:ab577b18cce05ed8d8cf55df209a1aab88871fd8e8e8a838cd7cae184115f3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69262293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eed4058ffe6e3d2d0bb402d76545097fc61b9da69a197cad7e854bef8ff6e09`

```dockerfile
```

-	Layers:
	-	`sha256:03de055bb367e59e8e1210ccf50bbb3b35d8309cdca25458ab538a33eabc23f1`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 69.2 MB (69235200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a778bc765d0a3169bbc8c628f33dd0ffdab45add71fcfe8bc3b95aaaf504e75`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260119` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e035eb915c3a6e68734810d287d8ac28d9ceab8116389ce99e2b25b97a637120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.5 MB (692520977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27d1e3e4b23fc8a5da3581690f44a07df0f5d24c9ea706e4dbd692f7bfc8a37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:53:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:53:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:53:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:53:37 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:53:37 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:53:47 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:54:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:54:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:54:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:54:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
USER odoo
# Tue, 20 Jan 2026 17:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:54:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d3f7efb0b6437e6dad992249a9e9f212f4c429f91c18e1dd089be44e839eca`  
		Last Modified: Tue, 20 Jan 2026 17:57:50 GMT  
		Size: 252.0 MB (251960576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25358a67828d3d7ef6213e1eaeb9ad2660e4adaa4d1045483b465f96f6241b4c`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 14.3 MB (14334234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa0707f65e802f83913204602cbb05dc9fcc134626f7dc580d58a445b250fa9`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3919195b79dea6685eec4fb80e6282fd7f0c9ef1483d8d949a2dab30496fb9`  
		Last Modified: Tue, 20 Jan 2026 17:57:53 GMT  
		Size: 396.9 MB (396879902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f41f0f5bdbc86cb88249d87017d8984b91c56043b40d472af5ae0a894127be`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652adaa52722dd1cbcb106e97d293ede808015890010e4de5cec1de7b983f524`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a70e3e541f9b9f69ac58af6c7f14bc609065396f4d4b94dbca35e70c1118c1`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a9d8e8a22ca44f40837c40ee3fd9ef6c602f5d8580019f150efb926895b4a5`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:88c7505587a949ee392a0b1d9d547e0545403385261a6f847d1c77ba46c9b154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69269743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e16f0d2ac1ab59b61d795b2d232c0803dd6f657541b92c1b82abab1ea65d20`

```dockerfile
```

-	Layers:
	-	`sha256:aa63d456dfdc200fbfc53f2b4b3fa6d0c037a64a00a799d9b3e0b48efeec2938`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 69.2 MB (69242487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8ae7028b78d75057cae67cb5e00d79d3d23023bde2352f3377118078720d14`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260119` - linux; ppc64le

```console
$ docker pull odoo@sha256:9833984eb447737f2fcda5c0ad5553e08c302136773fa19a378dd96968ad6e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.3 MB (712333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2838fcf1b6bc1ce44196fea1c9ee681af72f3a3b1578f1db8fdf4fce21957e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20260118
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:56:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:56:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:56:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:56:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:56:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:56:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:56:11 GMT
USER odoo
# Tue, 20 Jan 2026 17:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:56:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151ffb267c0a5be1759a65975327bab5213504b6c8bc3ea17de7b5a0b34a594`  
		Last Modified: Tue, 20 Jan 2026 18:04:29 GMT  
		Size: 397.6 MB (397573416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da15feec4aba697fcd38284d523426609089fc0119fe707762686d3398604c`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea6c0b655df738672b31a89ff5484495408fc1f6585df60070e67c5b77be5f`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab1b831bf4246d4385d80d093f81276ec85cfff2b85373698308100858b7d4`  
		Last Modified: Tue, 20 Jan 2026 18:04:18 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f868fad0c0bd07e104728719b1a389633405002728f82258eaa94072a4913`  
		Last Modified: Tue, 20 Jan 2026 18:04:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260119` - unknown; unknown

```console
$ docker pull odoo@sha256:d638e1a531945adf4046a18205acf241355cd86f5f379b57922e75c9884006f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69270744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43168bb406f693b975ad2749638d6e7f202905a70c08860fdf2725f50be00027`

```dockerfile
```

-	Layers:
	-	`sha256:bad7b514a7cfe62c5e6bb9f9973d52c5cfcdbf7c66f32c7b71603f3a42397b7e`  
		Last Modified: Tue, 20 Jan 2026 18:04:22 GMT  
		Size: 69.2 MB (69243589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb21a1984fa2c6049eed77bbcef06aaee981d00b8733f7a8772c877809cb98af`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:6116ea0d16e143c780d065316bba04e8f68d93d8418eaf1672f417b368b0a5fe
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
$ docker pull odoo@sha256:9f84fca1a2a5669177e38e90a53200401adfe4f26b14b6834cee0a7879c2db4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.2 MB (696151267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375997b4a9ea1b4a5a073a19fc914ac63a0a1a1a3676c67ef3db8bd93cf1e0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:48:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:48:17 GMT
ARG TARGETARCH=amd64
# Tue, 20 Jan 2026 17:48:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:48:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:48:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:48:28 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:49:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:49:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:49:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:49:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:49:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:49:29 GMT
USER odoo
# Tue, 20 Jan 2026 17:49:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:49:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e32c44d64b22b09f9b27047dd9d078509daa81ea8cc7c59831f2ff6befd57`  
		Last Modified: Tue, 20 Jan 2026 17:51:42 GMT  
		Size: 254.6 MB (254560297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e21283126d6c3bbdb627e3db9f3fd50783640a49de04ba2796b7889fcdd4fcb`  
		Last Modified: Tue, 20 Jan 2026 17:51:34 GMT  
		Size: 14.4 MB (14356589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa583dfe843366b6ca2700914026e1a6867c21ea46ecc8444ca75c0d8cb423a`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 480.0 KB (479991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b3ebfd50b36d69135a863f2796eb6d703981b97f26b2a570274dbd0a024e88`  
		Last Modified: Tue, 20 Jan 2026 17:51:45 GMT  
		Size: 397.0 MB (397025938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f24605144f794459756dd6e6a45533cba89c4216ca6f4f919f139939951eac`  
		Last Modified: Tue, 20 Jan 2026 17:51:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2546c91a4bd0c90145324305aff6536e6ca5a74fb0cd1a1f706b904272daebe`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae10fefbbe87fc9f138f54688ea28d77514fb10f581e284976d80c21db02b54`  
		Last Modified: Tue, 20 Jan 2026 17:51:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa435c5f17762fe361d40de34745d9aa8e31cb4d4e5cb7ecf9c3949be897c1d`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:ab577b18cce05ed8d8cf55df209a1aab88871fd8e8e8a838cd7cae184115f3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69262293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eed4058ffe6e3d2d0bb402d76545097fc61b9da69a197cad7e854bef8ff6e09`

```dockerfile
```

-	Layers:
	-	`sha256:03de055bb367e59e8e1210ccf50bbb3b35d8309cdca25458ab538a33eabc23f1`  
		Last Modified: Tue, 20 Jan 2026 17:51:37 GMT  
		Size: 69.2 MB (69235200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a778bc765d0a3169bbc8c628f33dd0ffdab45add71fcfe8bc3b95aaaf504e75`  
		Last Modified: Tue, 20 Jan 2026 17:51:33 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e035eb915c3a6e68734810d287d8ac28d9ceab8116389ce99e2b25b97a637120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.5 MB (692520977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27d1e3e4b23fc8a5da3581690f44a07df0f5d24c9ea706e4dbd692f7bfc8a37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 17:53:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 Jan 2026 17:53:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 Jan 2026 17:53:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 Jan 2026 17:53:37 GMT
ARG TARGETARCH=arm64
# Tue, 20 Jan 2026 17:53:37 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 Jan 2026 17:53:47 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 Jan 2026 17:53:48 GMT
ENV ODOO_VERSION=19.0
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_RELEASE=20260118
# Tue, 20 Jan 2026 17:53:48 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:54:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:54:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:54:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:54:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:54:55 GMT
USER odoo
# Tue, 20 Jan 2026 17:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:54:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d3f7efb0b6437e6dad992249a9e9f212f4c429f91c18e1dd089be44e839eca`  
		Last Modified: Tue, 20 Jan 2026 17:57:50 GMT  
		Size: 252.0 MB (251960576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25358a67828d3d7ef6213e1eaeb9ad2660e4adaa4d1045483b465f96f6241b4c`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 14.3 MB (14334234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa0707f65e802f83913204602cbb05dc9fcc134626f7dc580d58a445b250fa9`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3919195b79dea6685eec4fb80e6282fd7f0c9ef1483d8d949a2dab30496fb9`  
		Last Modified: Tue, 20 Jan 2026 17:57:53 GMT  
		Size: 396.9 MB (396879902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f41f0f5bdbc86cb88249d87017d8984b91c56043b40d472af5ae0a894127be`  
		Last Modified: Tue, 20 Jan 2026 17:57:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652adaa52722dd1cbcb106e97d293ede808015890010e4de5cec1de7b983f524`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a70e3e541f9b9f69ac58af6c7f14bc609065396f4d4b94dbca35e70c1118c1`  
		Last Modified: Tue, 20 Jan 2026 17:57:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a9d8e8a22ca44f40837c40ee3fd9ef6c602f5d8580019f150efb926895b4a5`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:88c7505587a949ee392a0b1d9d547e0545403385261a6f847d1c77ba46c9b154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69269743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e16f0d2ac1ab59b61d795b2d232c0803dd6f657541b92c1b82abab1ea65d20`

```dockerfile
```

-	Layers:
	-	`sha256:aa63d456dfdc200fbfc53f2b4b3fa6d0c037a64a00a799d9b3e0b48efeec2938`  
		Last Modified: Tue, 20 Jan 2026 17:57:45 GMT  
		Size: 69.2 MB (69242487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8ae7028b78d75057cae67cb5e00d79d3d23023bde2352f3377118078720d14`  
		Last Modified: Tue, 20 Jan 2026 17:57:41 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:9833984eb447737f2fcda5c0ad5553e08c302136773fa19a378dd96968ad6e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.3 MB (712333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2838fcf1b6bc1ce44196fea1c9ee681af72f3a3b1578f1db8fdf4fce21957e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20260118
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
# Tue, 20 Jan 2026 17:56:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 Jan 2026 17:56:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 Jan 2026 17:56:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260118 ODOO_SHA=9cb5691e31d2d8831887e85cc07268016f522f4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 Jan 2026 17:56:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jan 2026 17:56:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 Jan 2026 17:56:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jan 2026 17:56:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 Jan 2026 17:56:11 GMT
USER odoo
# Tue, 20 Jan 2026 17:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 17:56:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151ffb267c0a5be1759a65975327bab5213504b6c8bc3ea17de7b5a0b34a594`  
		Last Modified: Tue, 20 Jan 2026 18:04:29 GMT  
		Size: 397.6 MB (397573416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da15feec4aba697fcd38284d523426609089fc0119fe707762686d3398604c`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea6c0b655df738672b31a89ff5484495408fc1f6585df60070e67c5b77be5f`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab1b831bf4246d4385d80d093f81276ec85cfff2b85373698308100858b7d4`  
		Last Modified: Tue, 20 Jan 2026 18:04:18 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f868fad0c0bd07e104728719b1a389633405002728f82258eaa94072a4913`  
		Last Modified: Tue, 20 Jan 2026 18:04:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d638e1a531945adf4046a18205acf241355cd86f5f379b57922e75c9884006f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69270744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43168bb406f693b975ad2749638d6e7f202905a70c08860fdf2725f50be00027`

```dockerfile
```

-	Layers:
	-	`sha256:bad7b514a7cfe62c5e6bb9f9973d52c5cfcdbf7c66f32c7b71603f3a42397b7e`  
		Last Modified: Tue, 20 Jan 2026 18:04:22 GMT  
		Size: 69.2 MB (69243589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb21a1984fa2c6049eed77bbcef06aaee981d00b8733f7a8772c877809cb98af`  
		Last Modified: Tue, 20 Jan 2026 18:04:17 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
