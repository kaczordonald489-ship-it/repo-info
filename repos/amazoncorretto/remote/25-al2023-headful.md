## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:7f0ea933dcd31e4c53f0906a3c5708970398a39c94d130788815d6731037e098
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ece47d5a827b130c2e12bcc9a4e9d885d60fc15ef9bad31b443d0c733e004f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158266706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33922e6c6e2ea7b6c56a7a02288fd07ff8ca38f2f2a5f22e34e8b19ba099a603`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:14:44 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:14:44 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:14:44 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:14:44 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:14:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab564d9b5faf6a9660576403836b08b7d368ae674fbbe2848020766e670df032`  
		Last Modified: Fri, 21 Nov 2025 05:41:14 GMT  
		Size: 104.3 MB (104297685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b933887f52ac23cdc0579d5db3500da86d69275cdbaa6a3e6beece3817b3da0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a82ded59df428d88acde80722126250c3d1a312674e218edbace3f39dd7ff3`

```dockerfile
```

-	Layers:
	-	`sha256:d4e4d032598145262b8275903ec93388a5079584d35f55c9f3f80bcde79009a2`  
		Last Modified: Thu, 20 Nov 2025 22:50:12 GMT  
		Size: 5.2 MB (5220208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621eb3d54c457055a2058a2b273ea78cb73317d54af3081ad674cc74e24e4825`  
		Last Modified: Thu, 20 Nov 2025 22:50:14 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cd94e008a9668c8b436eb4dd436ccc8e2ff3d6b3cf52e37a63521d6f72055c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156113188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cb942091885e793bfe3d1512e96efe028ab5e98e6e849c166a030d0f4df70`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:18:07 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:18:07 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:18:07 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:18:07 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:18:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7c94885efbb52b40147f435918ae4f69939810e6aeb3ab575d432757d46efc`  
		Last Modified: Thu, 20 Nov 2025 20:24:51 GMT  
		Size: 103.2 MB (103243767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8c198ef70586cbf47977ce1583782c9854089261ae4fb77356cd28f2b4b26a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add6029bbf45f3d4d7c5c3a940ad1f05ee33bc95359ffaecd63a9bb5c89bc1b6`

```dockerfile
```

-	Layers:
	-	`sha256:f2d828e81e9a7d538154553473573eb8162b6da63256776e2df13da50b48e1e5`  
		Last Modified: Thu, 20 Nov 2025 22:50:52 GMT  
		Size: 5.2 MB (5219022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2aecf1afea3ff0399b7bbd8c7022f1a7f0dd15287f76069737245df6d5e30e`  
		Last Modified: Thu, 20 Nov 2025 22:50:53 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
