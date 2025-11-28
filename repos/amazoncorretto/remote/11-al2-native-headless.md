## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:db36652a4769a1d3d3c5b49c0633a0e4bb4facca60d4e7e17a2810718eaa199c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4ad4a53e9d39cf763e3e28c593dd307a8c1673bb197a0a8590c48ebc8fc1e5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217239502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc41700531c1934e1860960215a79213c84273db94e86cd8833a31bbe75bbe76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:20 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:20 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:16:20 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462780d947af50aa175dc4e932a375766c722329a0ce582a0ca97c3ff0c8079d`  
		Last Modified: Fri, 14 Nov 2025 07:52:00 GMT  
		Size: 154.3 MB (154308930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:840c349594386cbf73827f3d4b90f5e4cb2bbbd6a242df096a6c9b8aa2fe9ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b98ba42d27dec81756e6502df5b7f1fcbbd75b12d92953757724c829b8f114`

```dockerfile
```

-	Layers:
	-	`sha256:a62d73e2b0ae10dc04152e9847c88efbce82f9fbb91b8fdfe71905bbc56223b9`  
		Last Modified: Fri, 14 Nov 2025 04:48:14 GMT  
		Size: 5.7 MB (5683305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2efc62d7460fbc54ff6eeb0e16ad75d30b2c1f6efb39789f9ad8787cfb2a52a`  
		Last Modified: Fri, 14 Nov 2025 04:48:15 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2efc94a799f9af4ba712c86304fe0c2be1cf57cae354b58c52679b36b5301be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211380908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1d84ab543b81eac08a3d499266bb0cd2ca47881a1a49b8727f5ba7446d9902`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:44 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:44 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:16:44 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4140f9598d6ae1c780019982d75078b1da9345bb988bea6fa3aaaf3bd940435`  
		Last Modified: Sat, 15 Nov 2025 13:38:07 GMT  
		Size: 146.6 MB (146588107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ebecb247a959d0a18f961f907708a0f36fbef43cf27edfa5f5999317a42dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39be2a6a7335fd5a763187336934bbf665e6c1fc70f820509d6655d48250f07f`

```dockerfile
```

-	Layers:
	-	`sha256:08a1797b09b46feceade57680ba4598eea47358270c96de2ef9bfb5b997b97aa`  
		Last Modified: Fri, 14 Nov 2025 04:48:20 GMT  
		Size: 5.5 MB (5501773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b16aa0fa665b5bb167138c9e36610bc89782c0f1fa1056504b355fce5867cc`  
		Last Modified: Fri, 14 Nov 2025 04:48:20 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json
