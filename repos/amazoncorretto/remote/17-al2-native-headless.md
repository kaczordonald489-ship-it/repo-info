## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:82654ebf999c71f13484abafa8f48bec1273ec22682b74defda8bb2610f37eec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b46c3e3fd23c8ed29b25863d2cdc7f5f6d672b3600e3be87f46f845447f1c771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150552868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3100e756f7c95b82c2a5028257401356107d4c9a6b2a9df8d2ad3f689ccf2b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:33:01 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:33:01 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 29 Jan 2026 21:33:01 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:33:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b734df9c0a11d47c3d6150771dfa6bd46d1deb0dd5fd6bddfb7f88dc319f98bb`  
		Last Modified: Thu, 29 Jan 2026 21:33:19 GMT  
		Size: 87.6 MB (87589159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:269db491ca5cddc4c1ccc235b7306714aadf0164388239c286064b07e330ede6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2657d1070ce97eca23f4c0a016bf7d88af98a4eab74862571e4a73f8b6dee5b4`

```dockerfile
```

-	Layers:
	-	`sha256:4e128a01ef911e13c9ce9ab3f0409c4831962ccf869d7e1aa6b9c1798dad712a`  
		Last Modified: Thu, 29 Jan 2026 21:33:17 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5375e16c29f26f2a9e7b12ced00333d3fb8569fbc198362f5c2ed2863b9877c`  
		Last Modified: Thu, 29 Jan 2026 21:33:16 GMT  
		Size: 9.3 KB (9293 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3eb800c104410ee943f0eef33a2d785c8c78b66df655c170b4ae272cf9dabfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144646566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1958c96300e22fa21e01662468c5052303504111630f31fb4f61d31c2a57234`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:50 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:50 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 29 Jan 2026 21:32:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c59f6dd0029ac468d65c60d03b648a3fd53f5287df121da891ca91ee740be0e`  
		Last Modified: Thu, 29 Jan 2026 21:33:08 GMT  
		Size: 79.8 MB (79847677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a33cf91f92e54f42cd0f38fde2646cd9c76407907fa0f2968563e4f3ebc84893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bfa88e866535c4387b42cb680b6ffbf775cd14c03665bd4c87aa5de03b4d9e`

```dockerfile
```

-	Layers:
	-	`sha256:739766d4e3a9f445c7e89ce1deb16bd9344d10a226e2e25d915447957aa2ce8d`  
		Last Modified: Thu, 29 Jan 2026 21:33:06 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787098a03bfa564c47d8e72595115c7a36b311e45f8bdb7ca1937e836d546620`  
		Last Modified: Thu, 29 Jan 2026 21:33:05 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json
