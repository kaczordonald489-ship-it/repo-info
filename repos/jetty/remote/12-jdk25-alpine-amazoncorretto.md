## `jetty:12-jdk25-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:b302eb26d1fd471a8854f31443499175c909c45d36fd0a63fe3629a98dcf32d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:070812f700a786d4aa18642d5b3d67ab845610163f1f888cb0764d1c4a9f5332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239898323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebe96c4cd678a0100b9eaa451739332158111579c9b599f1a80359fce2c09b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:59 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:59 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 02 Feb 2026 19:23:34 GMT
ENV JETTY_VERSION=12.1.6
# Mon, 02 Feb 2026 19:23:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 02 Feb 2026 19:23:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 02 Feb 2026 19:23:34 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 02 Feb 2026 19:23:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 02 Feb 2026 19:23:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Mon, 02 Feb 2026 19:23:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 02 Feb 2026 19:23:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 02 Feb 2026 19:23:34 GMT
WORKDIR /var/lib/jetty
# Mon, 02 Feb 2026 19:23:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 02 Feb 2026 19:23:34 GMT
USER jetty
# Mon, 02 Feb 2026 19:23:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 02 Feb 2026 19:23:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:23:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce024e0c1fc281f3f61f3cf3a1e72dcd0c8f1a01d7b36ccd799f9d0d0de6c041`  
		Last Modified: Wed, 28 Jan 2026 02:53:20 GMT  
		Size: 180.8 MB (180759289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9999fb7b7305b3a678e9dd7b6ea065ed782cfda1183816977d5a04a862833`  
		Last Modified: Mon, 02 Feb 2026 19:23:46 GMT  
		Size: 55.3 MB (55275337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b0fd66673bdbdc354cdd3e93419cb905b498cbb3e35f87c52b22ce237255a`  
		Last Modified: Mon, 02 Feb 2026 19:23:45 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9dcf2560e89cc9a703f276f9668e66dffa90ce349a718c49536e1e1632193f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1072861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05595d88b2d2a278968f1eab4ddb3f60a443e04ca4e991439e0e6ab6ad06016a`

```dockerfile
```

-	Layers:
	-	`sha256:a2a7a1829296098dd9d01faf7a903a63dd7d62f289766e35b7f4e424ff12d26b`  
		Last Modified: Mon, 02 Feb 2026 19:23:44 GMT  
		Size: 1.1 MB (1055790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9bbedadea1c1f7d1bbe1467236dbf97cc787b382b9386394393e4a3c3e38bed`  
		Last Modified: Mon, 02 Feb 2026 19:23:44 GMT  
		Size: 17.1 KB (17071 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f743ecc72693dc6147d754e734196c4cd8547d36a0ceb3bbdd05b0de5c870c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237787000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1817891309ab88109462ae0e4d4550feabbb67ec94cec70c735edd58e9b119d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:31 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:54:31 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:54:31 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:54:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:54:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 02 Feb 2026 19:29:34 GMT
ENV JETTY_VERSION=12.1.6
# Mon, 02 Feb 2026 19:29:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 02 Feb 2026 19:29:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 02 Feb 2026 19:29:34 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 02 Feb 2026 19:29:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 02 Feb 2026 19:29:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Mon, 02 Feb 2026 19:29:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 02 Feb 2026 19:29:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 02 Feb 2026 19:29:34 GMT
WORKDIR /var/lib/jetty
# Mon, 02 Feb 2026 19:29:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 02 Feb 2026 19:29:34 GMT
USER jetty
# Mon, 02 Feb 2026 19:29:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 02 Feb 2026 19:29:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:29:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00285b52f6f6c9e088cd08bc54a41499c353ac64712efcaf2aff682f021f1a`  
		Last Modified: Wed, 28 Jan 2026 02:54:52 GMT  
		Size: 178.4 MB (178412260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334e1bb0edd41edc76a88fc79a4c27107c9d1de8f4a9a6030d54a8e189a3dd76`  
		Last Modified: Mon, 02 Feb 2026 19:29:46 GMT  
		Size: 55.2 MB (55175773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f056391ef5a61418c587a0d12af0005d4d3cb592ef6572c064024eeabda18c0f`  
		Last Modified: Mon, 02 Feb 2026 19:29:45 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c1b49c1d870eb1992f61566ba5a6f191643136554e7009c6116350c7c71a26e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f43771f2cf3a8a8486263fad3df8f4acc0d7a55dffa70074aefbfad5c5738e`

```dockerfile
```

-	Layers:
	-	`sha256:8561889ed9f7c2d2e4030ae24305c38a9f29e1daa7caa477db81bf3d9a916062`  
		Last Modified: Mon, 02 Feb 2026 19:29:45 GMT  
		Size: 1.1 MB (1054544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d325cfca7835a899f7a5555e31a386c5b22f38e427c1a8c056e17c4c4989e6b8`  
		Last Modified: Mon, 02 Feb 2026 19:29:44 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json
