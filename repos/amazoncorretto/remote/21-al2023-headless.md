## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5f8f3b3c2275ddf856025f8d47bd89510b747c522137e284c28fc21834ce9455
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:49fb9a25af423f0a84a85bc92cc66a8af6d39df22b7af46e458cd3e381b432ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143215383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d41c20c9d490a2ab21ae1051c7747610a1cb4ea69f90b192b2188c0c6cc2fec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:12:16 GMT
ARG version=21.0.9.11-1
# Thu, 20 Nov 2025 20:12:16 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:12:16 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:12:16 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:12:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6510a4817c556b22292661b5f5c465e924b1082686a0f6fa8bb58135fd149f`  
		Last Modified: Thu, 20 Nov 2025 22:51:31 GMT  
		Size: 89.2 MB (89246362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0ff90123c1f9a58745a872733fd5e3aa779dbf215010ed57d7a1ea7e72e7cce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18537b64e309105e3eb98f30655e577c5889d298db4748ed8f72d08001a9fd`

```dockerfile
```

-	Layers:
	-	`sha256:7d96cde9af75b3e95fa590df2d25ebf8862ad6838cb254538c1cb78831dbd472`  
		Last Modified: Thu, 20 Nov 2025 22:49:39 GMT  
		Size: 5.2 MB (5184514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f69e086010a72007595d3df9cf13f276c3cfeffa245b16454da51fa4ca5caf01`  
		Last Modified: Thu, 20 Nov 2025 22:49:40 GMT  
		Size: 8.7 KB (8704 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2f191bbaab60857afc4fdf9b8a887b86e7250a638f202ed8b0b6040fdd4ac664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141232842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fa8cc8b5074fefad2571bf31799e2844d7783669ed4aca45f1a69faf51e038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:15:31 GMT
ARG version=21.0.9.11-1
# Thu, 20 Nov 2025 20:15:31 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:15:31 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:15:31 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:15:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3120489c2ccf7abb984db206629a70d67d8d4eb53dc840f60485ce24d870b4`  
		Last Modified: Thu, 20 Nov 2025 23:26:02 GMT  
		Size: 88.4 MB (88363421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c709e77054d62ee74747a7056d89cd3bd5b8222f528e9a76c513f99ff3f2d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96de95c1b89e7ef4a97665e1d8f3c342792d60f52da268a22f048d4c6f6b74ad`

```dockerfile
```

-	Layers:
	-	`sha256:247cb8f053692c2f95fa466bc2d0e33d7028d04169698932e3eae80c34bdd1cf`  
		Last Modified: Thu, 20 Nov 2025 22:49:45 GMT  
		Size: 5.2 MB (5183304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe21bcf48f1a18584f412bae30e70b7ebfd5554e48baa9fb442e14f2e249d4c`  
		Last Modified: Thu, 20 Nov 2025 22:49:46 GMT  
		Size: 8.8 KB (8785 bytes)  
		MIME: application/vnd.in-toto+json
