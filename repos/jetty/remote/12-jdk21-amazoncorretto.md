## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:5be47adab90e1acbf8761100921131fb1f5789a6377cbb4272037a98420ea96e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:e4c570a8cd6c9aac06bc692b71243165604a73d5056a89d3d5ef861fda7e44ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280603910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8dfdfb127e9d2168b6c868d0fcfa92a6b2288bf2f7ff6590df96a129c8781c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:08:32 GMT
ARG version=21.0.10.7-1
# Wed, 28 Jan 2026 04:08:32 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:08:32 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:08:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 02 Feb 2026 19:24:10 GMT
ENV JETTY_VERSION=12.1.6
# Mon, 02 Feb 2026 19:24:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 02 Feb 2026 19:24:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 02 Feb 2026 19:24:10 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 02 Feb 2026 19:24:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:24:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Mon, 02 Feb 2026 19:24:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 02 Feb 2026 19:24:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
WORKDIR /var/lib/jetty
# Mon, 02 Feb 2026 19:24:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 02 Feb 2026 19:24:10 GMT
USER jetty
# Mon, 02 Feb 2026 19:24:10 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 02 Feb 2026 19:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0798c1d1f022fade01bdc30b6baea9d516656141ed30e3c3d28131e29713d4`  
		Last Modified: Wed, 28 Jan 2026 04:08:53 GMT  
		Size: 165.6 MB (165556560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8a099d64466c1e7f43acf7f18c2ae58f1b38f57f4be0038a653f6464f82253`  
		Last Modified: Mon, 02 Feb 2026 19:24:24 GMT  
		Size: 52.1 MB (52081765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaecd7ee954c9e9bca3982dabab53e6054694034d000cd53cce140e7bb9eebb`  
		Last Modified: Mon, 02 Feb 2026 19:24:22 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:45f7fdc58f9561caaca1f4919d914023ae3984f31a1cae80590bfd055a137d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9887bc4c982b2d1eea491ac6a4bf2891f91e298b4b82a7eceb1174f20480b4d1`

```dockerfile
```

-	Layers:
	-	`sha256:2cd738fc068b63a81442b2ba1b062bb3d92e1f60a5b9f4e24676f3dd6ece0cf9`  
		Last Modified: Mon, 02 Feb 2026 19:24:23 GMT  
		Size: 6.2 MB (6151902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600bd5a20ef9f05983f9b853f035e7050b58c7bff32e29ff14ed52e42a1351cf`  
		Last Modified: Mon, 02 Feb 2026 19:24:23 GMT  
		Size: 17.4 KB (17352 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c3d91aad96f0f2a049a11ff39a71f736d67ae4f26e8d6d5c369628e6e9b9df36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280522457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fbb2894c786630755d776172d7e1b2cbc35a029c99acf7234f45363e0eec3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:30:00 GMT
ARG version=21.0.10.7-1
# Wed, 28 Jan 2026 04:30:00 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:30:00 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:30:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 02 Feb 2026 19:30:08 GMT
ENV JETTY_VERSION=12.1.6
# Mon, 02 Feb 2026 19:30:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 02 Feb 2026 19:30:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 02 Feb 2026 19:30:08 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 02 Feb 2026 19:30:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:30:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Mon, 02 Feb 2026 19:30:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 02 Feb 2026 19:30:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 02 Feb 2026 19:30:08 GMT
WORKDIR /var/lib/jetty
# Mon, 02 Feb 2026 19:30:08 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 02 Feb 2026 19:30:08 GMT
USER jetty
# Mon, 02 Feb 2026 19:30:08 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 02 Feb 2026 19:30:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:30:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef463fea7a93137770bb91fa14775d030ebc14a22312021b37329181cca2bdc`  
		Last Modified: Wed, 28 Jan 2026 04:30:23 GMT  
		Size: 163.6 MB (163610457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfadc2a720f3b349fbb3e5762f11035d4f30cf3b35b2158ee46e5957193c4c9d`  
		Last Modified: Mon, 02 Feb 2026 19:30:23 GMT  
		Size: 52.1 MB (52111237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80921f8226929a5b8d4cbdf4bf35e8eb83fd2f85290c6d6f8d9a1f764eedace`  
		Last Modified: Mon, 02 Feb 2026 19:30:21 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:79e3d0f937d97dcc2c5d826011ebc1998aefb500a145931e057d7c9b68b1dbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6167976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff80acddc5827b1f5d36e79659bb4ac1c7b29ce16523809a8f97c9b7dda10c1e`

```dockerfile
```

-	Layers:
	-	`sha256:0ee631af8b35c41e1e7b7c0aa67cba5f5f436d4f5145f10efb96510574c64c88`  
		Last Modified: Mon, 02 Feb 2026 19:30:21 GMT  
		Size: 6.2 MB (6150531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b3133c44f03c1b8da260a617a5a5949e8967a7c06eeda8ba0faaef7bd4c4af`  
		Last Modified: Mon, 02 Feb 2026 19:30:21 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
