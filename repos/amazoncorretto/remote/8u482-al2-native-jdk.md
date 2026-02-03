## `amazoncorretto:8u482-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:78a252fdf52d166101c7d40fc7579e5a3f9f730bf07d816178668409d8a9953d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:77227645859475d4aa59196d959b99326bce96fefbef5767379a583abd5ef55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188260491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92189dadec4526975c7063b073149f0bfc574a757a61cce59d3828b0450a1c36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:53 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:06:53 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:06:53 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3983fefb9869aa859f0f2185017a081f9b33d2a89be393d5b4dba3c1a1fe0a`  
		Last Modified: Wed, 28 Jan 2026 04:07:15 GMT  
		Size: 125.3 MB (125296782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ac35964e94d202d1c7af4e59cbab2f1741efd39d8c3d0cfba9204669f09c29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8549c64c0ebc34f8bef2110eecf64e36081c97fa3e63b424a3fce5b7a5600c44`

```dockerfile
```

-	Layers:
	-	`sha256:a9cdfd9cd7d6f5324920026a1e0a624bd524cc3e140e0d35c7184367138366d8`  
		Last Modified: Wed, 28 Jan 2026 04:07:12 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381b52b060322f1fa126fe2332f365adaf76dcfe0f5d3310da29c57c5d210296`  
		Last Modified: Wed, 28 Jan 2026 04:07:12 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5d2537410b328659ad7e79ee38c92331b1c193ce55476b0c228a2590bccb3f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132408426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f5d8167dfb6bb2e6935ed3645724a305b3ee5174409c6e0483c43baf2c9eaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:26:58 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:26:58 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:26:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6203ccced79023d11351e5190b6bc40fd5f703c090d972be8b53cfb59a82db1`  
		Last Modified: Wed, 28 Jan 2026 04:27:14 GMT  
		Size: 67.6 MB (67609537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28a94105911bd1b22465140828e2c26c1ef9c3d4e8502e34cc0672b5558d3560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584c9cd30993a52197643e219f1ae7af70e761234af753325295656411230fa1`

```dockerfile
```

-	Layers:
	-	`sha256:2c5fbf45164ee95b0bbf8b8d72f42365f902771f53cd28ef0ec1cc3ee8310f2f`  
		Last Modified: Wed, 28 Jan 2026 04:27:13 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a98e2691f4b84a3278e02901972c69d27c96e50fd29912f7212d43eff2d5f1d5`  
		Last Modified: Wed, 28 Jan 2026 04:27:12 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
