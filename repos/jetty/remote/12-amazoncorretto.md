## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:529fa14148e10776ae1a71d511fb1f078d3e012a40c42be59b057ddd11c93f40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:49e127f2ee2ae3af320b3ba42999d1cb073cfb74674175b3683d8ca4477d30ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322283497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2aaae5e5786007c24422bdb49d5b5ee2884e9d2476f04439cc41f2ab4f64d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:10:02 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:10:02 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:10:02 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:10:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:10:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 02 Feb 2026 19:24:06 GMT
ENV JETTY_VERSION=12.1.6
# Mon, 02 Feb 2026 19:24:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 02 Feb 2026 19:24:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 02 Feb 2026 19:24:06 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 02 Feb 2026 19:24:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:24:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Mon, 02 Feb 2026 19:24:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 02 Feb 2026 19:24:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 02 Feb 2026 19:24:06 GMT
WORKDIR /var/lib/jetty
# Mon, 02 Feb 2026 19:24:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 02 Feb 2026 19:24:06 GMT
USER jetty
# Mon, 02 Feb 2026 19:24:06 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 02 Feb 2026 19:24:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:24:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cb6fcb38396d39f54d43d1b722399b74f95aea87f5b449eac9d4eac383e396`  
		Last Modified: Wed, 28 Jan 2026 04:10:25 GMT  
		Size: 189.2 MB (189191028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9b4e9b2d9c61605a4cff05e982274b721933a618b2c569a4e83a164ade59b`  
		Last Modified: Mon, 02 Feb 2026 19:24:25 GMT  
		Size: 79.1 MB (79066757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f965f67c696fabc303c95a07f9b829a62eff6937b99923a2fd5c76054979670b`  
		Last Modified: Mon, 02 Feb 2026 19:24:22 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:d559e92046896b42ee09c7ebb1f2039d53377a59261f066a198ac48ea01de731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121b7b941818cb8e779357bb7d1bdb10fb968c48f76a93f459e0ebd8d2ca1bae`

```dockerfile
```

-	Layers:
	-	`sha256:c57009764e4fbb915e0c9b25a6c75542f2770f2f4e72e569d0918e782cca1e77`  
		Last Modified: Mon, 02 Feb 2026 19:24:23 GMT  
		Size: 7.5 MB (7474501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32057afbca78f6cf85e0fc150e36bed6154001d17326be345f9efccd09dc1ece`  
		Last Modified: Mon, 02 Feb 2026 19:24:23 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ddfbb553043e0e3cb65b0c5a241eb406e5d19dfd0f7351739027a1cee62cc420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319015962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e446dba0659403d6de64ed83e7ee77f3e9b8abcea6c3c6c953b3c4ff368f32f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:31:03 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:31:03 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:31:03 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:31:03 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:31:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
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
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a396e73c665f4fa119c9cd20fbfa42ece312688cd9297587073bc7d229c333b4`  
		Last Modified: Wed, 28 Jan 2026 04:31:30 GMT  
		Size: 187.1 MB (187090861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf9ca0d17f67bef304db092df4abe427b206d88d78aee82e5fab322706b84a`  
		Last Modified: Mon, 02 Feb 2026 19:30:29 GMT  
		Size: 79.0 MB (79006587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dfeeb72df6c334bd21bc12b7a23bcb9fa4f10cd8c7f8310ebbc69f2dac8198`  
		Last Modified: Mon, 02 Feb 2026 19:30:26 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f7d0467c45db6b7c91ecfc76cc3dfdde87772dc9e9da600202ac47841e246e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ebbfceca055a5c997ce6e4edd9a6b814965aa4510547bb49b9a5a3c740fa6c`

```dockerfile
```

-	Layers:
	-	`sha256:ccd065451c8b5a7ef245a71e99096ba5832ea6d8ea2099b5276fa1648bb1dfb8`  
		Last Modified: Mon, 02 Feb 2026 19:30:27 GMT  
		Size: 7.5 MB (7473481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2eb9fe2ab6e8e036bd1bb45d1e04f0d874a92b0321d51e49d6c9eea0ed9a48`  
		Last Modified: Mon, 02 Feb 2026 19:30:27 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
