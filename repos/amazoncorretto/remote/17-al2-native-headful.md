## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:ad908e531f9259318e574843a015fcd16fff0836f1e351dae854dba03be737f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6ccde7f3e972019f607e13a6dbe8ce2a5713543c117fe47d8a5c62434584ca36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154258631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5838d65b0f1912fa50da6adb35f6b2ece4040afe2711b0b282d624e3cdeb23c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:33:16 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:33:16 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 29 Jan 2026 21:33:16 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:33:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6689a34e9ad567b09a4f8caf0d72432bb0b084199a2edc67f2fd99c05bbccde`  
		Last Modified: Thu, 29 Jan 2026 21:33:36 GMT  
		Size: 91.3 MB (91294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:78b2e4c93ec9e3e8c52c2b15c0250442e1cc81bb825270f3eb8a6cc0f96276b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1901ad8a4a7b418779c73b13c70c621a5d10b919f06823f58d22200ad553063`

```dockerfile
```

-	Layers:
	-	`sha256:04664a3c604d63da7b7b213abba47b51bc5b867f44021bbcee7bb18ca0df74ef`  
		Last Modified: Thu, 29 Jan 2026 21:33:34 GMT  
		Size: 5.9 MB (5865818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7893214539ecb0e97173f521065af36c64b783374a13df4c32c2520be2c5f5`  
		Last Modified: Thu, 29 Jan 2026 21:33:34 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7d052fc7cb8db9f66fe980789443fcc58f122e068957b7d897e062455eb0f3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146795747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74e6238b5cfc051fc621bdf09f68a228ffd176a09b5572ad65af72e1ab22dc2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:51 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:51 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 29 Jan 2026 21:32:51 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7931823562362516cf66cd09d97b4e73832745c881c11cdbe3c10dec13c32b7d`  
		Last Modified: Thu, 29 Jan 2026 21:33:10 GMT  
		Size: 82.0 MB (81996858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b3de62242fab47e99f728787d610abed5a813aab9447ae83d9a4e9057f0ca15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1812f707039ecf52a4b5234b7533f06e8baa096eafac8db0e1be508ae9c253d3`

```dockerfile
```

-	Layers:
	-	`sha256:edfc6d2c87338924e461cbc085496e190d7dc4c8ee2567d79a32a512f34f0bab`  
		Last Modified: Thu, 29 Jan 2026 21:33:08 GMT  
		Size: 5.7 MB (5657561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b7c44ae0c980105b5f823142eb750a280aedfdd4b3412b53e6647c046d1cc9`  
		Last Modified: Thu, 29 Jan 2026 21:33:08 GMT  
		Size: 9.5 KB (9508 bytes)  
		MIME: application/vnd.in-toto+json
