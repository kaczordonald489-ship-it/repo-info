## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ffb18f929dbfa60ec511af816928cd6e7ca2101dd57b1977a65c02f552ec9f54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c690bce17e2894fd8e0c21b0d5164fd333e92b2d84b6f5dc98f2a5f86fabcf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130734653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b570931f55394c8bccd1df167aa40a34b549276f1e33e75c3dad076d409f6f57`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:07:02 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:07:02 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:07:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:07:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72458f6bbed08be21a94071252e95b3bcd55ed8edd78403f0c91e9f6574c034d`  
		Last Modified: Wed, 28 Jan 2026 04:07:19 GMT  
		Size: 76.7 MB (76710817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:39a9fd4d506979313205033ccdb1ad3b131d10b9281c107697dbf49a1e5cee1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67445e4d95385676f9467422c17a01be035cbe9a6c67c522ffa6c71b7c49805a`

```dockerfile
```

-	Layers:
	-	`sha256:3bc9242c0e0dcd383a337cd9e4ef9093856b9cfad53de7f643aabb0b636cff9a`  
		Last Modified: Wed, 28 Jan 2026 04:07:17 GMT  
		Size: 5.2 MB (5222248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58dbf8f91fb18339143597fdca167ba4cf87b51abaae317faf6b78eee7cbf430`  
		Last Modified: Wed, 28 Jan 2026 04:07:17 GMT  
		Size: 8.7 KB (8745 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0e06a573dfc4913b7d3a039ce949d9d52d8ee8c375b4637fcfe6ae038fb1bd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128872493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc912e45629ac7e9504b603616272996d7328ddc76e7f27838892e04a762681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:30 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:30 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:27:30 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4f05e9f7ac70a1ef9f8d6d939da1b5e5f45057edb1576425595a74e19342e0`  
		Last Modified: Wed, 28 Jan 2026 04:27:48 GMT  
		Size: 76.0 MB (75955855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6e3121a7791a4e99a6fc94f894a49bdf1bc553d20c78988c96224b73cbbf8924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54decf9d202f56163d74caeed3c3053045e91d261732f26f5be501ab97b36cac`

```dockerfile
```

-	Layers:
	-	`sha256:9ed27542b92ccc99708d2218ab18f2cbf15fe570cdb19ff46048446e2cc4b549`  
		Last Modified: Wed, 28 Jan 2026 04:27:46 GMT  
		Size: 5.2 MB (5221869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12580ac6a851b3d52623e4005bb2ee46de772ff23e5fd9cf3e27b40f19e2ba78`  
		Last Modified: Wed, 28 Jan 2026 04:27:46 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json
