## `tomee:10-alpine-plume`

```console
$ docker pull tomee@sha256:eecdb0cb1e77089c939f08c7d0e05238a6e72f4f01d20927f8e512f69df81f72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:56d4fed791dc4da0196bfb4f133e2ab9e70b6609563685e88872c626c6e92776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165155702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9325d8c12e18d8e81aedd566251ac387f20b41eca02c78c55b71aa838f9bc70d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:14:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:14:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:14:45 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:14:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0176d4b18047ce6669c451e7293998961340a6720e979adfbfefb7356d21d597';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='46a7eca285957dadb0adacd96fe385bc5512f31b7f90a3dd01f04679d614a420';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 04:58:07 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:58:07 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 28 Jan 2026 04:58:07 GMT
WORKDIR /usr/local/tomee
# Wed, 28 Jan 2026 04:58:08 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 04:58:17 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 28 Jan 2026 04:58:17 GMT
ENV TOMEE_VER=10.1.3
# Wed, 28 Jan 2026 04:58:17 GMT
ENV TOMEE_BUILD=plume
# Wed, 28 Jan 2026 04:58:22 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 28 Jan 2026 04:58:22 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:58:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba89a167f7fd2a7eda103eacbbc9129de402e6f5b21746f7574e3686573c742b`  
		Last Modified: Wed, 28 Jan 2026 03:15:03 GMT  
		Size: 9.4 MB (9421151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79cf6f12909fd91996c618448e3adf034b745c59a0cc6177eacf9badc03e7b3`  
		Last Modified: Wed, 28 Jan 2026 03:15:04 GMT  
		Size: 62.0 MB (61974320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504fac65c789e542c7c32e3d72b6f505138bdc68b36860d14740202a8316db14`  
		Last Modified: Wed, 28 Jan 2026 03:15:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babdbcd0b513a5a9ddad2421cb89e449ec361b0ebe84e773495b2415ffbd7ea3`  
		Last Modified: Wed, 28 Jan 2026 03:15:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad0d2552b1f92384944109e74e7e2538096a82decb7a58b403363753f03ef94`  
		Last Modified: Wed, 28 Jan 2026 04:58:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f83c0196a307a100058228d1345de872b7049a3c894f5e2369dc586c20be46b`  
		Last Modified: Wed, 28 Jan 2026 04:58:31 GMT  
		Size: 7.0 MB (6991574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31725b9238f36adf2aa348feaf8afd5284ffa9a8ae5455a31190f055c5836f9`  
		Last Modified: Wed, 28 Jan 2026 04:58:31 GMT  
		Size: 75.6 KB (75629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e77e013caa589386b9704c499f0bce94a3dc64de0b273490ee0da60ecef3df`  
		Last Modified: Wed, 28 Jan 2026 04:58:33 GMT  
		Size: 82.9 MB (82885539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:7076f24795d93a0c83168a819a05a320eddffd83c62bca472ade5302771771c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e205766fdc0264070789ed73901620251efbccb08247902615bdc755f59280`

```dockerfile
```

-	Layers:
	-	`sha256:e93e17e6633db4340dc284b07f03aa432592bd833f1b9f686f3b30f74a4dc28f`  
		Last Modified: Wed, 28 Jan 2026 04:58:31 GMT  
		Size: 1.3 MB (1316508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3e4a7609e59c8a9fb70fcdad73a7976c69baba4e5014612d1eae284d7a49a9`  
		Last Modified: Wed, 28 Jan 2026 04:58:31 GMT  
		Size: 30.1 KB (30133 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:bcd41984f7509572b157d165c99fb6ea5d4371c223c500142a18ce7cdfd89e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164332879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a489174dceb7ff4f6d5d358fa7bf678019f701fa4ba7ade5162272b95d63376c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:02:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:02:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:02:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:02:24 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:02:29 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0176d4b18047ce6669c451e7293998961340a6720e979adfbfefb7356d21d597';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='46a7eca285957dadb0adacd96fe385bc5512f31b7f90a3dd01f04679d614a420';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:02:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:02:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:02:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 04:45:18 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:45:18 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 28 Jan 2026 04:45:18 GMT
WORKDIR /usr/local/tomee
# Wed, 28 Jan 2026 04:45:19 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 04:45:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 28 Jan 2026 04:45:29 GMT
ENV TOMEE_VER=10.1.3
# Wed, 28 Jan 2026 04:45:29 GMT
ENV TOMEE_BUILD=plume
# Wed, 28 Jan 2026 04:45:33 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 28 Jan 2026 04:45:33 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:45:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b1333bd1e2829978df661cb50b4db2ddfbcf66ac1c016d92fe24f4a3418ba1`  
		Last Modified: Wed, 28 Jan 2026 03:02:41 GMT  
		Size: 9.4 MB (9435012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9104344c3ac249e99cab1a9ac52adb82512332471a4fb47eedb5aeb163b85ec`  
		Last Modified: Wed, 28 Jan 2026 03:02:43 GMT  
		Size: 60.9 MB (60874468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a7ec361f0060dc31b17ca5fa375d22b72fec28f8b5f8a2256e051aa6d5779`  
		Last Modified: Wed, 28 Jan 2026 03:02:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3747b9409be7e1245934ccd39c4a14288d93b982319330164cce2143f64d01a7`  
		Last Modified: Wed, 28 Jan 2026 03:02:41 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa396fa59440c0f138f4ac30465b43f06ff6b6d32b0badd96ffa5e54cba87d68`  
		Last Modified: Wed, 28 Jan 2026 04:45:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf21895767f63d155872318e69ca6c1ba7ccc444cb6647776443e71493b245d`  
		Last Modified: Wed, 28 Jan 2026 04:45:44 GMT  
		Size: 6.9 MB (6920046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bce2bbcf9fa2c5c7a3f0e9bba987ba6880e9600198dd96b0dcc071fea27b5b`  
		Last Modified: Wed, 28 Jan 2026 04:45:43 GMT  
		Size: 75.6 KB (75641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed718cb74e0e43b88889e0b233d1d9d001b02780b1f2180f13eabbf1957c6d69`  
		Last Modified: Wed, 28 Jan 2026 04:45:46 GMT  
		Size: 82.9 MB (82885582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:4c91eed003e57c7da938738fc5adb0d3bc3819277c9693b5b930453f0734cfc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862dde3b6b7565e2ade756f7cf1980d7aeb53b94680b99a1775c39ad48a7e3ff`

```dockerfile
```

-	Layers:
	-	`sha256:acbffa0380f9b2fcfcbac99ceb05008c3640b7c81de2f5e64c7ef75a56e6c294`  
		Last Modified: Wed, 28 Jan 2026 04:45:43 GMT  
		Size: 1.3 MB (1316087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19d6f4ce2162c92457e05b11a7a2b5c0cb4205b13f675be32a9df742c4ffdc`  
		Last Modified: Wed, 28 Jan 2026 04:45:43 GMT  
		Size: 30.4 KB (30426 bytes)  
		MIME: application/vnd.in-toto+json
