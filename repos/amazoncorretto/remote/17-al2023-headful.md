## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:985c44823f001bf02e56a04c27005ad41b6755550b404ec3bf70644e85158870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b74583de71e09d61134440216e0877793cda9ed6c6b035b497f4ed2c13cae84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137055005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90a74153e1c8a9ced32ea96aa871d8fd25376a873bdc92003e0adec37c7a65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:11:12 GMT
ARG version=17.0.17.10-1
# Thu, 20 Nov 2025 20:11:12 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:11:12 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:11:12 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:11:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77ffe407cf6fa52c5d92eef813a58eee2ad256c40b0ff6371a374e356de58f`  
		Last Modified: Thu, 20 Nov 2025 23:30:54 GMT  
		Size: 83.1 MB (83085984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61c772b042b0b7cd65758cf2e38462d39d48239f3db3e6b40271f2220204e3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e7fee72bca7a13acbf14c4357fb0c35705d73887b2f889ba89569adde704c9`

```dockerfile
```

-	Layers:
	-	`sha256:31b0bb2f077e6afdbbfb5495131bef2e94990dce507ebd7f88565dabbce3f736`  
		Last Modified: Thu, 20 Nov 2025 22:48:52 GMT  
		Size: 5.2 MB (5208327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e0a1478d4b6f9fa658cd901b0660fdc65fd22984d84378d546a1ecaf94e8d5`  
		Last Modified: Thu, 20 Nov 2025 22:48:53 GMT  
		Size: 8.9 KB (8892 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:48d7b1a8c9e5fa0e8c59d12a27e4f0ffc6b42c5c60ade9923cac4891964a3a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135371901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a93767df7b5cbf419c9a7b5435d4041bd350dc2d555d225cd10af0b59eafff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:14:24 GMT
ARG version=17.0.17.10-1
# Thu, 20 Nov 2025 20:14:24 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:14:24 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:14:24 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:14:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9854ccc3bc890d38d41a29a78e44cd61b2e8a4b7a1048320431aa215475030a7`  
		Last Modified: Fri, 21 Nov 2025 00:02:20 GMT  
		Size: 82.5 MB (82502480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:664d47404b13326cec75cc2378d822033cbf21b90040fcd234986e3fb8309457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb1ceffc5645e06c4d34853397aafc13e00ac5350ecb3bea41ca07571ab83bb`

```dockerfile
```

-	Layers:
	-	`sha256:7167585ca12f0c6200b0487e19b9ecc422c949d21094fa727f88c11e08dcc7a0`  
		Last Modified: Thu, 20 Nov 2025 22:48:58 GMT  
		Size: 5.2 MB (5207118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93ad1d3d14b883b863e040c5904614a02a512522ee7d27e21118336bf2b799`  
		Last Modified: Thu, 20 Nov 2025 22:48:59 GMT  
		Size: 9.0 KB (8971 bytes)  
		MIME: application/vnd.in-toto+json
