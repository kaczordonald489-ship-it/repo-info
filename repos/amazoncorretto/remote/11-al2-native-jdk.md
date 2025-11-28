## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:b839561d9f7cef5efd0e39393ef80520a802d2ff9a57f0612eb8581e0f4c0dfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b6e604b6468ce7e40d49b63458068a7c20706053d8ae2238ac3ee619a82cbead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224508815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad14f4141f52ab1cefb09b0d77eab753c9fe16c0791e385e91f4857ed58d9e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:24 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:24 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83f4429f2e28b32a80293992313f96d8e1d27224fb07487a5d7c5f8217283c9`  
		Last Modified: Fri, 14 Nov 2025 09:04:31 GMT  
		Size: 161.6 MB (161578243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:459d9b728bcc35b2d62967da12898c290c207c81fd7b56b009cd97290883eeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118e280b57c1b8f0449b682b04cce3ec9ba50300f7d0d427f9ecf1f5b9403434`

```dockerfile
```

-	Layers:
	-	`sha256:e3958194a8efabe8350d5ce82e29b5f7dd897195436af053e647c4b3b6d78bc7`  
		Last Modified: Fri, 14 Nov 2025 04:47:40 GMT  
		Size: 6.0 MB (5995082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44677c580001cc777debbd7670439e1bae7cbbaefd68df1e3edd4c31585efe9`  
		Last Modified: Fri, 14 Nov 2025 04:47:40 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bce2e2e6ff96b0c98e895e9c69264d1c15b0cc39c661af816eb42bc78d9c1886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216445626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f14582d81dc26d93ecc85e7a895523f0af6e4ac014cf66a5de8704eb049cca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:55 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:55 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:16:55 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd53a6739385a3bd8d26321bff1c35df1772e4166013890cf75d2ea00d1707e2`  
		Last Modified: Sat, 15 Nov 2025 13:39:24 GMT  
		Size: 151.7 MB (151652825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b025e8e9b1770748ed5bada52adac7102111cb466af12b8606f52d15d6b9c8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a0077cdd5d4e9a7897f694fbaea3700c81eea38f4547c7195984d1adbeb731`

```dockerfile
```

-	Layers:
	-	`sha256:fa5d77cab2e839cbf6b9419ff04dd3a77fdd736bc9bbd39e9f02e6e1b3b19245`  
		Last Modified: Fri, 14 Nov 2025 04:48:20 GMT  
		Size: 5.8 MB (5787796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d7c06d81846f07fa5a54445376afd95e602c2c97c70c778c925e11ff3d137a`  
		Last Modified: Fri, 14 Nov 2025 04:48:21 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
