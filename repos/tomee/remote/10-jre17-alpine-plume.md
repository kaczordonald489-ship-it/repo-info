## `tomee:10-jre17-alpine-plume`

```console
$ docker pull tomee@sha256:0552f2240d7b9ccc37679c70c3cf49f32e64c3ef3363d50546d68e025bcd4bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:10-jre17-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:e1665ae6377e48fa09cc552aee619ac6512f49b1a212be713e17d710a0cf5fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150957832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616d4eff677a58bd243d9629ae91819dddc2548df548da6ba7b4ba363a651e66`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:57:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:57:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:57:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:57:45 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 03:08:56 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6c3047e8edd3878e8d2a1cee95c04606042c6a55954ad365d20b58f88cc9ecd5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:08:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:08:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:08:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 04:24:43 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:24:43 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 28 Jan 2026 04:24:43 GMT
WORKDIR /usr/local/tomee
# Wed, 28 Jan 2026 04:24:44 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 04:24:54 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 28 Jan 2026 04:24:54 GMT
ENV TOMEE_VER=10.1.3
# Wed, 28 Jan 2026 04:24:54 GMT
ENV TOMEE_BUILD=plume
# Wed, 28 Jan 2026 04:24:59 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 28 Jan 2026 04:24:59 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:24:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712170bbbcf08e7e6d5fdc5e77492f5ee689ccc346dfd3323e70ed3cd4ce6391`  
		Last Modified: Wed, 28 Jan 2026 02:57:59 GMT  
		Size: 16.3 MB (16293985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec4236d96f40951be5c39840082eb0bf7c851bf489142edaf46c7902a13d804`  
		Last Modified: Wed, 28 Jan 2026 03:09:07 GMT  
		Size: 46.7 MB (46718954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9247b2da494fffed9d04179a8f1dab65aa3413f202ac970e4af2c4429403c50`  
		Last Modified: Wed, 28 Jan 2026 03:09:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8189bd200c048407210efb45fd23b31a6a50959b4337697e85a6200477c05b`  
		Last Modified: Wed, 28 Jan 2026 03:09:06 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eee1b477e039a97b2399746ea46ad7c82e53510329e2a93f91afbfef8f8a67f`  
		Last Modified: Wed, 28 Jan 2026 04:25:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a351f990a346eb133b5f046b762220b9181d1c55d31a2ba5614728bdd991a40b`  
		Last Modified: Wed, 28 Jan 2026 04:25:09 GMT  
		Size: 1.2 MB (1176198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60600a5be076d64f7ac6830ddf70a5d8b7246fdefff6fbaefccfc033c0ad7a86`  
		Last Modified: Wed, 28 Jan 2026 04:25:09 GMT  
		Size: 75.6 KB (75624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6772f864ba9b2b2a2b34fbe7c254ca1fe0f8bfb34c05f02c0203a37c244f5b`  
		Last Modified: Wed, 28 Jan 2026 04:25:11 GMT  
		Size: 82.9 MB (82885587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:5f8a2d01d5043636edd6537dc4518d6b351508758dbf62d2c3501535ce5f3d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1350968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a328bcae5332f341d4dee4a03c9e0896a9d567af60fd087f70d0ac16434ac4d`

```dockerfile
```

-	Layers:
	-	`sha256:ad4cfed37d12552410a8be39ca3673bcb73da091f6dfe078fe8c16cbdc459317`  
		Last Modified: Wed, 28 Jan 2026 04:25:09 GMT  
		Size: 1.3 MB (1323409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f41be1f67a377fbcd63fb902b2941a8d0a983807e8fc18ab7f210aec6f2d8d8`  
		Last Modified: Wed, 28 Jan 2026 04:25:09 GMT  
		Size: 27.6 KB (27559 bytes)  
		MIME: application/vnd.in-toto+json
