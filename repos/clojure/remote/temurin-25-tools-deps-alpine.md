## `clojure:temurin-25-tools-deps-alpine`

```console
$ docker pull clojure@sha256:a5e473efbe877b07ecf6eed72337ba105fd4911aa65cb6e9b33c9a28f942a146
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d80585f5ce73b2d4aca27068d4fc369abfa551a9c2b59c7b530bf5524ccf49d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135483736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c28c0c525971acdbd91fa9866fb77eb1bff97d77d638bfb8a9faabd1e84c2fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:13:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:13:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:13:48 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:13:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:13:56 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 18:06:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:02 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:05 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 28 Jan 2026 18:06:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c82c37cc1e371eead2dc58300215ff956e7c66f7a9be860363938c03e5c76da`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 14.2 MB (14246382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31aa63af3fdb098e136e53cb2a136db5e58d0d583a45a29aa0f688e2b0c3b3`  
		Last Modified: Wed, 28 Jan 2026 03:14:13 GMT  
		Size: 91.3 MB (91279981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e456b61d1dd1581cd1136ee74763eedb7bf7af1158ecad882564104548359d1`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331024c35ae2ab78ba266cd395ff3155e7a3135687cde5017449ef802da8d926`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec74b6d19b5e846f88d4c852f8d98d9111a9b39dbab748f9cc1f9902729356cc`  
		Last Modified: Wed, 28 Jan 2026 18:06:14 GMT  
		Size: 26.1 MB (26149037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3512ca357065a28644758d1e52c1840ba1d27d3cc88844d208c75e49e368b`  
		Last Modified: Wed, 28 Jan 2026 18:06:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28433381913aa2f2c0d03c90e409c006ae84ad189d546c24e59b6d0430199b10`  
		Last Modified: Wed, 28 Jan 2026 18:06:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:b6d8683f43ffa19614b9e860c461f58ee6fb71f6a2c33b81be4c6a2a5a22ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b6b0df73ae053a1329c5c936535d8a27305280fcd2c971ec2fdab71a805c89`

```dockerfile
```

-	Layers:
	-	`sha256:146aca0799f6fe294be0bfe03ac80c0feefe4baeb245933dd9ba69f40109fd7a`  
		Last Modified: Wed, 28 Jan 2026 18:06:14 GMT  
		Size: 1.2 MB (1181154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc25402284fbf737dab0db0f6a348b8993a00c6143c5e0e855ed40f07899e54c`  
		Last Modified: Wed, 28 Jan 2026 18:06:14 GMT  
		Size: 15.4 KB (15425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f91f210e6d64e5b0b77089b4fbf298723eee19d6c546018a4ff37e84c3bc708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134971893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52424583789f5de43753693f25a320a14c883a8c83bd0402a04c1a221db6340c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:00:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:00:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:00:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:00:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:00:45 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:00:53 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:00:54 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 18:06:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:18 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:21 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 28 Jan 2026 18:06:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5288573acdcd1544c20a13292ab18c2f63bfc25bd67e4ff7fda45bcd6ff95602`  
		Last Modified: Wed, 28 Jan 2026 03:01:09 GMT  
		Size: 14.4 MB (14352508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59a6d58393b4efd9f9346f830fb5d4b12d5abe806a5efe2b15f408c79a26081`  
		Last Modified: Wed, 28 Jan 2026 03:01:11 GMT  
		Size: 90.2 MB (90190699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452efb31da7be8de7a686fffee1b06489e32b6b26a07b4b1108bee8041a3e12`  
		Last Modified: Wed, 28 Jan 2026 03:01:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a8435556e3b5786f56d544bb393ce6a392d6617de1793d08481767d196bd9d`  
		Last Modified: Wed, 28 Jan 2026 03:01:12 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe83dac59493c8ab6db9c4154d3b70c8e7fb40a8c05c66d55fcb1237caf94bf`  
		Last Modified: Wed, 28 Jan 2026 18:06:31 GMT  
		Size: 26.3 MB (26285711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc6b0f24f15aa34fcc62447223cb158a012309fb90dd270a854ce657645bc62`  
		Last Modified: Wed, 28 Jan 2026 18:06:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbdad0437efda8d0b533b4fb47749e42a491a3876587b2582717454e06dc3c8`  
		Last Modified: Wed, 28 Jan 2026 18:06:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a6131c0a802698270f0b1e9874f74cd8e363ffb3bc6c50fb821047d89006e2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1127d32ff9deba8eceb838f7978e14fa0e3ec85d697d9651cd166aa11e71d376`

```dockerfile
```

-	Layers:
	-	`sha256:c91910e60cb6cbcfd8fcd0246791731a51cb79858aaf7147b27575797f74fff1`  
		Last Modified: Wed, 28 Jan 2026 18:06:30 GMT  
		Size: 1.3 MB (1331153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf84fa2734d9469ae195f857f4a448be808185c135e5f7875e06b0cd8055d7c`  
		Last Modified: Wed, 28 Jan 2026 18:06:30 GMT  
		Size: 15.5 KB (15517 bytes)  
		MIME: application/vnd.in-toto+json
