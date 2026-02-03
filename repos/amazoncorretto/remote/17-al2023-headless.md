## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:d1774c004d9b20de53c1a6b62ae0af0de67fbc4d6f45e6ab853f62c02b532db3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:293df05a4143a8c711965a9b1b57fee2146ba813851faac2e4c67b8dc0b461f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136385023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba7a9530f99984e8242d50f92271a419dd8d678fc48fda6889f290cf7e554f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:48 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:48 GMT
ARG package_version=1
# Thu, 29 Jan 2026 21:32:48 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 29 Jan 2026 21:32:48 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec422d2c7a4723afd3f35d45142f19300761ac131a12d07a5e5a0a863fd8e3d`  
		Last Modified: Thu, 29 Jan 2026 21:33:05 GMT  
		Size: 82.4 MB (82361187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:306c745ae7ec14264540f473163f5281871a3bfe012e8fe2fa122574c4e415bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd71e34b4c4b5af3e5be46f7ea2c8246434cf3e758e61879dd59622c83c26e7`

```dockerfile
```

-	Layers:
	-	`sha256:cd92b4e7dac09698bb041888832487570b97c34ebc78a991420f06cdc62e7512`  
		Last Modified: Thu, 29 Jan 2026 21:33:04 GMT  
		Size: 5.2 MB (5182896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdaf44cf8df4688936f893dcd7c9807d46471827e779c1076850bdf1151db99e`  
		Last Modified: Thu, 29 Jan 2026 21:33:03 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7ef6c1312e333673213d334b7134f03a66e41dee52f8e6de0b03df432b3eae54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134680076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe1ebc6e4b38b08fc97cbfcc10091b455106abd689bcac3bd96162e6fea179d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:21 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:21 GMT
ARG package_version=1
# Thu, 29 Jan 2026 21:32:21 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 29 Jan 2026 21:32:21 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25121e5ca76e7fc9f91a80ca92470f805fe1faeabadb68b43dfdee23eedb7c1f`  
		Last Modified: Thu, 29 Jan 2026 21:32:40 GMT  
		Size: 81.8 MB (81763438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72e245f1d50bf02ff74b25206b4533ae47fe0c84b013f7e2decc47cf378eebcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9366fc85cc294edb0e1c7aef6a4787d9b7d20aa5c84fc1a45b0284b49d5c0edf`

```dockerfile
```

-	Layers:
	-	`sha256:776ddee740d92a4412fe1ebab71bf58daf7c30d06abfa02a3f33bad178676e83`  
		Last Modified: Thu, 29 Jan 2026 21:32:38 GMT  
		Size: 5.2 MB (5181684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176d584d323a9916396396d67916a3056c24bcf138541403f330d782a84e665d`  
		Last Modified: Thu, 29 Jan 2026 21:32:38 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json
