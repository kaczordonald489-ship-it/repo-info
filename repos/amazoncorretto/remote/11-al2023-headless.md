## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:24b3a986036105dabf6ff501d9c019dba6d173143c478917ae8601fa0ed911f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ec56c163bed9ef2452afa860c24a691a12deb0bf369bc140b2211dbc0ea4b454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130032937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d2b35664e99e7c8213d81cdc38b087c2e8448ae26c91d175805a7731cda22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:52 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:06:52 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:06:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801a45ddc962bc8f8c1a1da19a7d98c2a3f9d1e902737bca80318c5d661490ea`  
		Last Modified: Wed, 28 Jan 2026 04:07:08 GMT  
		Size: 76.0 MB (76009101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e7777a93be7c89774d03109b705a1a2dd8ccd5ad2abe520dbfdc1e31aebdc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a033bf8c2fd09da4214d39b0e8720bb97251ef30b7d13e15cfb4511fd11b60`

```dockerfile
```

-	Layers:
	-	`sha256:b214dd950775df132397695084ef26c48197ed8ae2be5b30dfc24ec788ce4c44`  
		Last Modified: Wed, 28 Jan 2026 04:07:07 GMT  
		Size: 5.2 MB (5196823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf4cd30ce3c9309b8028c635541d362a6f44e007ea726596454839733f309f9`  
		Last Modified: Wed, 28 Jan 2026 04:07:06 GMT  
		Size: 8.6 KB (8608 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8913e169e809ffdd057cce24f10d98911ecc543bc7c30b69708e9a9188522b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8763fe083d786653b4872c56249c6e4b9ebeb3b5bed0e7bdf6d03df9f98e1bf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:19 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:19 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:27:19 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cc4d7162d985519f14c3c93cf08e7eee44f8262a0e0a4473a39e20e8d660b6`  
		Last Modified: Wed, 28 Jan 2026 04:27:36 GMT  
		Size: 75.2 MB (75239414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6416f352ab629d5b73c76e5bbfcaa8911ccebbfc16ecdf17826a383f9a3782f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262dcba55f6779a6a997feac4051254bbc21752161823688272e31c55e0a7a50`

```dockerfile
```

-	Layers:
	-	`sha256:5f6cec9a6651c5d7968a78923d848cdab6a50e8e6c3367b3dc9507c5ad704041`  
		Last Modified: Wed, 28 Jan 2026 04:27:35 GMT  
		Size: 5.2 MB (5196441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353819bcc416ff96943b05eb6143034049b19f16bd35a5c1de599411fc4ea809`  
		Last Modified: Wed, 28 Jan 2026 04:27:34 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
