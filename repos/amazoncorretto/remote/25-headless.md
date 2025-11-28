## `amazoncorretto:25-headless`

```console
$ docker pull amazoncorretto@sha256:43000572fe160772c12d7fcd67f25ad52cce0aac5ef15fdb891ea7a9488a96a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:48bd175498064c95750ca9ba0e94a1e4b5ea1c2012f6b0bd225f55c61993d8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157556354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae4b892da5f6678da092e92a8e13a587ae38d26a9371bfc902d3b2f0a1c4574`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:14:07 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:14:07 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:14:07 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:14:07 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:14:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab85d58621490fcb092ee57b5325c42fb9dadaa7fecbfbfd3762439b9453607`  
		Last Modified: Thu, 20 Nov 2025 20:30:39 GMT  
		Size: 103.6 MB (103587333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ecdf2664c6c5cc3270b201e8edcab90aaf61877744a0d9c39261f56e9f94905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5c5717debd66801a65565b5872ee863698ba5ad3eb2b771e9bfdc172163c34`

```dockerfile
```

-	Layers:
	-	`sha256:d59d15e77fac9a6c81c096d8abb7d5d9d8278cb926e9adc4f40490fb7b900aa6`  
		Last Modified: Thu, 20 Nov 2025 22:50:19 GMT  
		Size: 5.2 MB (5194783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ce36991343d586f1e3d62c5219e5efcefd3bf9e9d3a4d3fa5223e4b151ddde`  
		Last Modified: Thu, 20 Nov 2025 22:50:20 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4dd5f22303464b69e325c99726775ccace2f24a8ca90c3bfb97ac241ec10dae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155399376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0951c4a3915c780dbf6af6d58d1156e5777cd5399094dae1b080a70178a14630`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:17:25 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:17:25 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:17:25 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:17:25 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:17:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9a1239c951c5ed6b70b9ee467f273478e2113c49895e2fa3183ef5060989f`  
		Last Modified: Thu, 20 Nov 2025 20:25:30 GMT  
		Size: 102.5 MB (102529955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3becfbfa9362c7db225dfb488e0576c10b41b9dd2dcf48909d7101ca2f3bc15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d083eeada7223cbbf5a32f4868f9cb9ad1fd261025b625e3990edac04e6ed3`

```dockerfile
```

-	Layers:
	-	`sha256:5c33f5ecf75495b5d9609e08ce4554ca5b689775e21a9a6310e8cfb8bad2b700`  
		Last Modified: Thu, 20 Nov 2025 22:50:25 GMT  
		Size: 5.2 MB (5193594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f63d375a6bd08cec3ea6b0a5df5e85eb2579e178462fbaef3f612d045202888`  
		Last Modified: Thu, 20 Nov 2025 22:50:26 GMT  
		Size: 9.1 KB (9120 bytes)  
		MIME: application/vnd.in-toto+json
