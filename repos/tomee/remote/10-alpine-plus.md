## `tomee:10-alpine-plus`

```console
$ docker pull tomee@sha256:103ccd872bbab0e702475c9f3fc6d67bcc18f93a154760b2574a1ca6948c7e71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:39c356e30746c28c3778a10057c840127df2a56a25fd86c91df5e29dfdaf1e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157062033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62aea4f613be259be8ad2b16d698b8b095ecc38c744f6efa06255dd9b45455b9`
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 04:58:18 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 28 Jan 2026 04:58:18 GMT
ENV TOMEE_VER=10.1.3
# Wed, 28 Jan 2026 04:58:18 GMT
ENV TOMEE_BUILD=plus
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
	-	`sha256:ceeea4e281eb55e9fe0c881593e59ee83df27ba31330e179214ca84b0829383c`  
		Last Modified: Wed, 28 Jan 2026 04:58:30 GMT  
		Size: 7.0 MB (6991578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fb3ebf4676a42071b12a489f08dad77b2630e67e1ee30028653b5a067fad10`  
		Last Modified: Wed, 28 Jan 2026 04:58:32 GMT  
		Size: 75.6 KB (75630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b657a5e9e0d1ae0b24275f268bd4adba7cc5e7e7187ae2e63db219d9a84cec`  
		Last Modified: Wed, 28 Jan 2026 04:58:34 GMT  
		Size: 74.8 MB (74791865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:cdfa87a6be13911a1d8402c44c2d3f18100608cc516ba88585031a5cb96c6770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1327760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a766fe9fee3dac0abfbfb05d5ffd43b052fb6c1a42278af16c3a113c23d3eac`

```dockerfile
```

-	Layers:
	-	`sha256:fa2332599a2240c9b0144a6c7957ceb3d19d5bf5704040936f285913473cd6fb`  
		Last Modified: Wed, 28 Jan 2026 04:58:32 GMT  
		Size: 1.3 MB (1297661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d1c81ecd544fdbf64b4baf2dd54220aaeeaca8a352be675297baab8aed1f59`  
		Last Modified: Wed, 28 Jan 2026 04:58:32 GMT  
		Size: 30.1 KB (30099 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-alpine-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:200ad186eebdaaeb9ff8e1900b3f5154560adc65decd4941788e4d1fd40176da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156239113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6083481f11bc7fcc1eae11d80bf1703ea23c2e41152eb406061aa0db2f4c664`
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
# Wed, 28 Jan 2026 04:46:08 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:46:08 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 28 Jan 2026 04:46:08 GMT
WORKDIR /usr/local/tomee
# Wed, 28 Jan 2026 04:46:09 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 04:46:19 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 28 Jan 2026 04:46:19 GMT
ENV TOMEE_VER=10.1.3
# Wed, 28 Jan 2026 04:46:19 GMT
ENV TOMEE_BUILD=plus
# Wed, 28 Jan 2026 04:46:23 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 28 Jan 2026 04:46:23 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:46:23 GMT
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
	-	`sha256:5e45bb3fbbe06fe6671bcb4cfb8a0fe1861fb5fbf1b8a72c96f4443e31b065c4`  
		Last Modified: Wed, 28 Jan 2026 04:46:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e927285d78cba522b0c69082b77f1c5b53c8b92bdb8e272a7ba558c5c137aea7`  
		Last Modified: Wed, 28 Jan 2026 04:46:33 GMT  
		Size: 6.9 MB (6920029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced8c02f94e1341ea2ee733dcdef8489952e4e5f3d8e97574be8a242130d36e`  
		Last Modified: Wed, 28 Jan 2026 04:46:32 GMT  
		Size: 75.6 KB (75645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f957716c7308badc48a0970988db26a37a73fe3829b3d4c6e49e5b7247abed`  
		Last Modified: Wed, 28 Jan 2026 04:46:35 GMT  
		Size: 74.8 MB (74791829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:1809c0d2f4743207dc804cc38492017610e0614fc995ee54588453b3b02ac977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1327632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1430ad0454b3a42a6b72165ea16cf781f6f4bb95176c07a414071071613cc`

```dockerfile
```

-	Layers:
	-	`sha256:ddf7b0b0590dccae73671f40fd19ceab1a088bc006d45275a23011c8ee28055b`  
		Last Modified: Wed, 28 Jan 2026 04:46:32 GMT  
		Size: 1.3 MB (1297240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30363dc3ad732d4684dd74503ac9e28715e6c6f889dcabffcef24c9308fe57d`  
		Last Modified: Wed, 28 Jan 2026 04:46:32 GMT  
		Size: 30.4 KB (30392 bytes)  
		MIME: application/vnd.in-toto+json
