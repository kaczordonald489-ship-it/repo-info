## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:0e0e4810cadf5995bbbe92333f2d8be032becf62c7fb2a3b0f89ddaef8000673
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b416a18775e6d9e18aba7dbe8eb26f98772ac983a231c8aa5ee7d6a6f3645d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267507751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96595ea52c83d072becb6b7d2806df66da158eb1e68d243d6710c35892f66f07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:31:57 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:31:57 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 29 Jan 2026 21:31:57 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:31:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 02 Feb 2026 19:24:46 GMT
ENV JETTY_VERSION=12.1.6
# Mon, 02 Feb 2026 19:24:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 02 Feb 2026 19:24:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 02 Feb 2026 19:24:46 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 02 Feb 2026 19:24:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:24:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Mon, 02 Feb 2026 19:24:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 02 Feb 2026 19:24:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 02 Feb 2026 19:24:46 GMT
WORKDIR /var/lib/jetty
# Mon, 02 Feb 2026 19:24:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 02 Feb 2026 19:24:46 GMT
USER jetty
# Mon, 02 Feb 2026 19:24:46 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 02 Feb 2026 19:24:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8326e4bb78b88f1d188237c6144a0f1f66da758b1b6fc8d8639c42d704a4202`  
		Last Modified: Thu, 29 Jan 2026 21:32:18 GMT  
		Size: 152.5 MB (152461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e028dd168ecbec6547e0fabf9b2d8432490d2ed07e5b22b7010579cdc76774`  
		Last Modified: Mon, 02 Feb 2026 19:24:59 GMT  
		Size: 52.1 MB (52080941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1370c7d0d5b846a1969cfbbd3d115bb8130c07d77bb693f1ff10f8518ce5958`  
		Last Modified: Mon, 02 Feb 2026 19:24:58 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ed78cea07f52acf36718c84940c2fd4dc31a8af0a22bfed15049771a2146b760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e862ca7e89e1e3f763c704fc0ebf0169c3084cfc0dc661452e29b4ce6d5641d`

```dockerfile
```

-	Layers:
	-	`sha256:c7e297d71489e6253dabf7027d9569e8944b00dab107f7594b0ae4eb5c52a62b`  
		Last Modified: Mon, 02 Feb 2026 19:24:58 GMT  
		Size: 6.2 MB (6151999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27cbaee563ff96d23c116e04abfc95c938dd702251540408428612d561bbbcb1`  
		Last Modified: Mon, 02 Feb 2026 19:24:57 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:9bc9342fbd3eaa07b70d5124f848e127186351cbd1bf31b3f00aa92120f25da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267891241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1cc21f558d7eae1212e089a0f9ae073ca7b34b880de84772a010a0e02d81b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:33:05 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:33:05 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 29 Jan 2026 21:33:05 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:33:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 02 Feb 2026 19:30:43 GMT
ENV JETTY_VERSION=12.1.6
# Mon, 02 Feb 2026 19:30:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 02 Feb 2026 19:30:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 02 Feb 2026 19:30:43 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 02 Feb 2026 19:30:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:30:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Mon, 02 Feb 2026 19:30:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 02 Feb 2026 19:30:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 02 Feb 2026 19:30:43 GMT
WORKDIR /var/lib/jetty
# Mon, 02 Feb 2026 19:30:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 02 Feb 2026 19:30:43 GMT
USER jetty
# Mon, 02 Feb 2026 19:30:43 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 02 Feb 2026 19:30:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:30:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ee4d8a45ac6dbdf61b0ee55fe6f15b35ac70940c33ec3b405fba90deb89a65`  
		Last Modified: Thu, 29 Jan 2026 21:33:27 GMT  
		Size: 151.0 MB (150980367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534f4767e24ec03d4658b2475cbd4dcc3aeea801b13a514935d2680a606d0764`  
		Last Modified: Mon, 02 Feb 2026 19:30:58 GMT  
		Size: 52.1 MB (52110109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b772764b9246be629a3b09adf7430a6cfd8a319dd837a4b1e9cffdc35823564`  
		Last Modified: Mon, 02 Feb 2026 19:30:47 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3ea666ac7b64200fed794d35afa433d32a802722341cd8d0e167df534bbe937e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94318551cf4a47ec25e089e122fa67f3a18a6dc41ed0a063119f3c0cdca036e8`

```dockerfile
```

-	Layers:
	-	`sha256:89cff760c2c488ef9035421fafd0577dae0214419f532636b9d04d1f3245b855`  
		Last Modified: Mon, 02 Feb 2026 19:30:57 GMT  
		Size: 6.2 MB (6150628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4fdef8bbaaa81eb82c86b00a8162c5d6b4313a7c0f904f80c9838950240841a`  
		Last Modified: Mon, 02 Feb 2026 19:30:56 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
