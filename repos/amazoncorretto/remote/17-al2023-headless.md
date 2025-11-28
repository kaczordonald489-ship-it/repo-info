## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:d8dd4e761b0917db739714d03078a476777c58f7d649dda9f1afedcf72bfe6e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:87fa3516aa6acadfa3eea8a000f93e617bbd2bbbb4920664d90e45139086d368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136321243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ba04c82dfcd521401aa442667226e04441bd79a2769f7255bcb96798ce38a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:10:20 GMT
ARG version=17.0.17.10-1
# Thu, 20 Nov 2025 20:10:20 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:10:20 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:10:20 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0c219f489ffb713ba7209e0e18b3bcaba1bb91d14c1d188b567d98b355ac4`  
		Last Modified: Thu, 20 Nov 2025 20:17:29 GMT  
		Size: 82.4 MB (82352222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1b032a64722bad38d08f0352ca155853c139f2aa391c594b77ae20fff9814d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf08b0f47ca52ae56a227a99685624c5b0c3a2e56f5cef6554a44a5601aea2b`

```dockerfile
```

-	Layers:
	-	`sha256:7eb5872633406c4c15399f158e027f00c3a2c31843656d947d27d6098f209d08`  
		Last Modified: Thu, 20 Nov 2025 22:49:00 GMT  
		Size: 5.2 MB (5182896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ca3ff1114ddb2e99e708d93aa32e297d9858b23634b7a2f9dcd212ed08040b`  
		Last Modified: Thu, 20 Nov 2025 22:49:01 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ae9741f9c8243af8288c09508b1d926c60cd997c502d163405bb477a6365a29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134639237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a31e0a3898aa711778b1af84e24c29aedec0893665bd401e47175084e7a7ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:13:20 GMT
ARG version=17.0.17.10-1
# Thu, 20 Nov 2025 20:13:20 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:13:20 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:13:20 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:13:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0051b4faf47309d14e2afe003ff1ffd17a47a94f0bcaba2f9aa4ae3c88c5e934`  
		Last Modified: Thu, 20 Nov 2025 20:29:21 GMT  
		Size: 81.8 MB (81769816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7e1c8e1b746c161dc6a92996fe9dcf593881e153db71f61cb48fbeb8df868dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3457f2f8fe2ed47d3e9bc8a3a887987b15dfd8699d745bfd548b189f5f3b0092`

```dockerfile
```

-	Layers:
	-	`sha256:4367968cbb664b31d8e2ac0c56dca63354ae7323368d8a8087908f04abe2f3b7`  
		Last Modified: Thu, 20 Nov 2025 22:49:06 GMT  
		Size: 5.2 MB (5181684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0662332fa98e37bb183f40254718182353d3b3508e83fd0e6a2f96b281021def`  
		Last Modified: Thu, 20 Nov 2025 22:49:07 GMT  
		Size: 8.8 KB (8793 bytes)  
		MIME: application/vnd.in-toto+json
