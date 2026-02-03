## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:ef52b00c2911b0a6673b26a42e85f507b0c8beff889cdd08f7529271e43473bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5d33ab3203d5affd2814e0f68577299a06c8525a9a9bf52df3d6a3e015e22b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172097726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18d5fccede645da4acd0015fd8044fcd4d9881655eec72eecabef187b961c4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:50 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:06:50 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:06:50 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446b3f213cbb9a113358a6d960feb7f5e95977aefa65cba434768775d0ee0ed1`  
		Last Modified: Wed, 28 Jan 2026 04:07:12 GMT  
		Size: 109.1 MB (109134017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17b65e09c768304e324668665cfd2d33033a3b865590acb28964c9c10f85c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007e9c900b0d1171cccaabdfa034c87a60ca3a33b6b39a7047292999c2906332`

```dockerfile
```

-	Layers:
	-	`sha256:b38e62c1f19543d0b906ea951c83205bf03c5a3b3c19e503f3d9d05cf95df24b`  
		Last Modified: Wed, 28 Jan 2026 04:07:10 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eab617da81d32810dc835f4578dbad2ab650f1c76a02a01415264851625c9b6`  
		Last Modified: Wed, 28 Jan 2026 04:07:10 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:545309309ab93e2d994b64f356bf676978fcc08846f3a923ead1662deb2dfeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117774517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43263897911ec35e981ee5f81d68d6af45164da1a65aa5c83455984da1d1cebf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:26:39 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:26:39 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:26:39 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:26:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf6a393d387060c952e82d3cfb8823bd97e7e654b0be5cb7dd48dd8853006d4`  
		Last Modified: Wed, 28 Jan 2026 04:26:53 GMT  
		Size: 53.0 MB (52975628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e03079309b2b55767706e73b8da0249f4e0c80f37f89178a079f1d0a1eee36eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc22fcd80ba6351bcbfeaff71f005b7d011625d7bd5b5a9ab590c79ad896c8fb`

```dockerfile
```

-	Layers:
	-	`sha256:1ba644fe2eec85bce43b848b2efec0466c0100c000a60167ce6b0820bf0348f5`  
		Last Modified: Wed, 28 Jan 2026 04:26:52 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:547b30ddf210aea77b53166dbfe02e855ea191e54bbcf2c4863326d0ed00b7bf`  
		Last Modified: Wed, 28 Jan 2026 04:26:51 GMT  
		Size: 9.6 KB (9583 bytes)  
		MIME: application/vnd.in-toto+json
