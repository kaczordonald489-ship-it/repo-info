## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:ea26998fcec2d649f82fec5d87aa5885991a3c9ed21e09f92bafb2fdbc4a0976
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9ccbaf44c506cce4579d9cfce2d8f00fd8773f06db9a56b0803155050e23f953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217299573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204d8733ae76b6e8a00577855b6e560d3430fad0183c3fa8db3d61d045a0554c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:07:05 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:07:05 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:07:05 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:07:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155f8b4e0ead6396c017e4dcf7953b0d4b2176b5fe022cd8a1bbe82a48f7f8e`  
		Last Modified: Wed, 28 Jan 2026 04:07:26 GMT  
		Size: 154.3 MB (154335864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5174477a8a927a68ca450726973ea2cbb91e95100341d84ceab2b561b0c5f714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d8c47525e7e5f2d5876a2ba09577fff368fed05b1663ca95694920c285ca19`

```dockerfile
```

-	Layers:
	-	`sha256:52b0a86c32240cf65f392323bee0b91734138b7bc45d7c6216bde013c0faa780`  
		Last Modified: Wed, 28 Jan 2026 04:07:23 GMT  
		Size: 5.7 MB (5683305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77deae01b59857990df9f61dd5fd35fe5328c26e1b10e79782f2e876f6556c4`  
		Last Modified: Wed, 28 Jan 2026 04:07:22 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2aeb79f757daaffac8402fbecc4687d25ca4cccd5de14ff2b33c6818b0930454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211421973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dad12bf1cb642cc9ebbfa2243990dcd488830ccca3924827058b51d6f71090`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:48 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:48 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:27:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa749dd48c468546f1ef5e01e620fee0d26b71d2e3fd97c8493265dc51e52866`  
		Last Modified: Wed, 28 Jan 2026 04:28:10 GMT  
		Size: 146.6 MB (146623084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e97b90a74e4528d40aecceb3b9e34a10102835d2755447e28a8689a41fd7e258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbcfbf88eef844a0997d6dbfc26e5bce1d1881e1b93de740114482c561cb466`

```dockerfile
```

-	Layers:
	-	`sha256:edd0a59ebd47364b202a123274c3d1108218d39c94323bd105560bdff7aaa662`  
		Last Modified: Wed, 28 Jan 2026 04:28:06 GMT  
		Size: 5.5 MB (5501773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b26ec5d9fd5f2524ccc6bab0b628354ff6ce274660b837324ec6ee9adae9b25`  
		Last Modified: Wed, 28 Jan 2026 04:28:05 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json
