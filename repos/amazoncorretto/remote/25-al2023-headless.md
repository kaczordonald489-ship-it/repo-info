## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:993daf9dc598d8249476724f809907ac521b753d7d8da1b4a082f6e4be149099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d505e6e3c319cade215cebde5cbdf8ea603f2e9598a8c1f199b531a99f600550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14d388229f4485c23cb3971f8489df79dc4b450c13831c1f2fdf0e43b1aed31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:10:07 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:10:07 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:10:07 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:10:07 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:10:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d528fa4c5008c551058ad69e335475215c92e27ad8894303bef0eb652f1cddc`  
		Last Modified: Wed, 28 Jan 2026 04:10:26 GMT  
		Size: 103.6 MB (103612558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e0a0331d0b0e6691d9b5a6f6f0ca15b531bbb707d06c2b134a34decd4c23a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e8e1017d77d11005bcb16d4f0a09a625253d4e734ec8b852a0365ffce6e3fd`

```dockerfile
```

-	Layers:
	-	`sha256:de6745e2b9e6e8d28936e790845c4ae4e46fd6a5b818d7ce1fb5d3bc1385f828`  
		Last Modified: Wed, 28 Jan 2026 04:10:24 GMT  
		Size: 5.2 MB (5194791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f247325981015e05e11a31e36e099d7b14b126ea2dd7a490a55fe8dfae2ace56`  
		Last Modified: Wed, 28 Jan 2026 04:10:23 GMT  
		Size: 9.0 KB (9031 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2bc7f6adb47c29324a92b82329d92c9baecd21f12b8270d0663c6d535aedb2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155452223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d1cb20bc666431f3d2e8668b16ff11f6df8805a263b445fb5d79f7d58f60b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:31:14 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:31:14 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:31:14 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:31:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:31:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7285388c31860e821e772912752e77147fe0cedb58508ac3063d3feee5dd3e67`  
		Last Modified: Wed, 28 Jan 2026 04:31:34 GMT  
		Size: 102.5 MB (102535585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc9b766fa5836fbb6250967031cc68419982258abbb610d48a3db465160a3627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eb964a2fe77611faa28c954183acc6aaa39da525f8f55d44570dc55484b6fc`

```dockerfile
```

-	Layers:
	-	`sha256:e6db43c78b4d7dc417957fb814d8533398e442f45986e0eaac67e9b9827549d5`  
		Last Modified: Wed, 28 Jan 2026 04:31:32 GMT  
		Size: 5.2 MB (5193602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b3edad6c19891889c98678cb72792b967e9970911637ee967be67a7ace4046a`  
		Last Modified: Wed, 28 Jan 2026 04:31:32 GMT  
		Size: 9.1 KB (9123 bytes)  
		MIME: application/vnd.in-toto+json
