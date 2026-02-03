## `tomee:jre21-Temurin-alpine-plus`

```console
$ docker pull tomee@sha256:a85e9b3d18eb9fb781e84cd65fba18ddc5ee05ab6cfc794f46882e1e59f19c6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre21-Temurin-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:0382e5db91bf151d900f7fe34e3db08e5f185b3fd69cdb94263194fc618b809a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149314244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d58e08956e10cf98969791018eeef954a2a06da450033e7a0181054c223d76`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:03:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:03:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:03:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:03:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:03:00 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 03:12:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:12:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:12:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:12:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 04:58:48 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:58:48 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 28 Jan 2026 04:58:48 GMT
WORKDIR /usr/local/tomee
# Wed, 28 Jan 2026 04:58:49 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 04:58:58 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 28 Jan 2026 04:58:58 GMT
ENV TOMEE_VER=10.1.3
# Wed, 28 Jan 2026 04:58:58 GMT
ENV TOMEE_BUILD=plus
# Wed, 28 Jan 2026 04:58:59 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 28 Jan 2026 04:58:59 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:58:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a95a7405177abd55077356ffb7a848c87d9ca9c23db8124d028a03a08abbd43`  
		Last Modified: Wed, 28 Jan 2026 03:03:22 GMT  
		Size: 16.3 MB (16294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d692f84685999cf52a16deb2a62f05a72b23b165370268bb9f84bf2720cbf86f`  
		Last Modified: Wed, 28 Jan 2026 03:12:46 GMT  
		Size: 53.2 MB (53169010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea5914daf9376671fa3a740cdc4cf83f54bc69c4802edc5123a3224fb2878d`  
		Last Modified: Wed, 28 Jan 2026 03:12:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a0e1e7665e6e529029146a70d0814061dd236331e5b77b0c739c34fd466769`  
		Last Modified: Wed, 28 Jan 2026 03:12:44 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0246ec2acf4c3484a6cb951cc6bc80d2b031576f848139b10387623bc0853138`  
		Last Modified: Wed, 28 Jan 2026 04:59:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acbc206294f7dceee62f8ff2746c5242acce4f16fb1f8b3be320abfb059900b`  
		Last Modified: Wed, 28 Jan 2026 04:59:09 GMT  
		Size: 1.2 MB (1176199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721c35f408c3d68e44de608fb7f220061979b017cd9674359a9c6e60c01717e`  
		Last Modified: Wed, 28 Jan 2026 04:59:09 GMT  
		Size: 75.6 KB (75643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0764ee069cc92b64327c15c71e9f1b08db4f971b92cd395cf37a990226650d59`  
		Last Modified: Wed, 28 Jan 2026 04:59:11 GMT  
		Size: 74.8 MB (74791895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-Temurin-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:8c5574ad657baf3cb804af6ef7823eed497e1236c61af4c0d4eaddb3a229f4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1334613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b6dee344f494cd3db1b3e83ac5123ae932260925148b4cb89f14f68e0050a0`

```dockerfile
```

-	Layers:
	-	`sha256:78bdaf8fc953fbf7a2dad7f0bcee09572f6af9461c5680b69bfd341bc7e17be9`  
		Last Modified: Wed, 28 Jan 2026 04:59:09 GMT  
		Size: 1.3 MB (1307076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d994af6625c53e047212db06c197af7af237903a0c64c0c1cba9ebbc5d49534`  
		Last Modified: Wed, 28 Jan 2026 04:59:09 GMT  
		Size: 27.5 KB (27537 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre21-Temurin-alpine-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:a061c0b176bc33587fae749adfac4a483295300668666382fa7c1a6cfec44977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148665627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27fb7bcf17e64569c8475b3f8331510c05a5f91fae65d57c6633f90a1889069`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:58:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:58:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:58:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:58:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:58:37 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 02:58:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 02:58:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:58:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:58:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 04:45:19 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:45:19 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 28 Jan 2026 04:45:19 GMT
WORKDIR /usr/local/tomee
# Wed, 28 Jan 2026 04:46:11 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 04:46:20 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 28 Jan 2026 04:46:20 GMT
ENV TOMEE_VER=10.1.3
# Wed, 28 Jan 2026 04:46:20 GMT
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
	-	`sha256:6c24115e8411f4d7573c11f391a90280e4d56095cc395d3092b6a130688b6a8d`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 16.3 MB (16258234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67ace64d831b85fef838eaaa1fe4f670492e335b3c224aa1dc424897a2fab4`  
		Last Modified: Wed, 28 Jan 2026 02:58:53 GMT  
		Size: 52.2 MB (52226461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03eb363046abe0e3136c465d80392d4c599e6ab1b8c7986e57a303bb02e8a89`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f79a9f2e9a637bcd3b3896f8afa7f5cda80ce104d3d9eef9cb9475b6d9ba06`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d088a06b67c3c428ba235a7e434ff3c045de40a516a91edb07876c8e22a3b95c`  
		Last Modified: Wed, 28 Jan 2026 04:45:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6411444781a17355f51c732ceeb273f027a1126c1a2cadc16ac22f8f3879e9d6`  
		Last Modified: Wed, 28 Jan 2026 04:46:32 GMT  
		Size: 1.2 MB (1171256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db589e88d38a8b3b8ca80c6ef8aa0ace6cc4098fd1899d81f03f2a7abb0ee8f`  
		Last Modified: Wed, 28 Jan 2026 04:46:32 GMT  
		Size: 75.7 KB (75653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420dc776ffd1ac9805a1bb76f657393bacf3c14232e4305017d8398315a9daa1`  
		Last Modified: Wed, 28 Jan 2026 04:46:34 GMT  
		Size: 74.8 MB (74791893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-Temurin-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:c4d41c1c3b320b1175d1c29bcd4f492321ba38e67704849eab9ff4b091b9be79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1334296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32044b1c7f34b88ae927d633aae9ade348634c63fd30a1f2b452d12c51b37b2`

```dockerfile
```

-	Layers:
	-	`sha256:28969acd2c82dc86d66d08a902a1c325d713a76d3ee6725bd9d92f20f58d3400`  
		Last Modified: Wed, 28 Jan 2026 04:46:32 GMT  
		Size: 1.3 MB (1306562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b0f487ab7f053a3134eac9b6d9c7c838524fae576da763ce794742e445670c`  
		Last Modified: Wed, 28 Jan 2026 04:46:31 GMT  
		Size: 27.7 KB (27734 bytes)  
		MIME: application/vnd.in-toto+json
