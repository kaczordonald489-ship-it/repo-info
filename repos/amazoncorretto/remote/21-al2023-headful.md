## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:9e25a52dcbbdf43bdb7bf5da781621073a40568e72acdaf60fe64313321122e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ed91a46e1c4c528fe8e49f2ca4a111a9114936c081cb98b4f0060d01ab728ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143997800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603d2266d815be501d8ab4648d76f3b405180eba6e10087a1a9d22f10135f73a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:09:38 GMT
ARG version=21.0.10.7-1
# Wed, 28 Jan 2026 04:09:38 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:09:38 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:09:38 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:09:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fffbe0063f9c7f50ad0c24f9b2c94d1f8df1eac63a47737dec1532daebd6e`  
		Last Modified: Wed, 28 Jan 2026 04:09:57 GMT  
		Size: 90.0 MB (89973964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:33aabb2acbf73758bf5cbbc28896cbb327385ec20716eb3eb726732bf79fd435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80abec2a696540900add415cbfe96a242b4ca77643bc03565ee6e8984189f7f`

```dockerfile
```

-	Layers:
	-	`sha256:be360c8a1c95c91e6bd04e39fb23ec7fcdaaed8e71f1d6590927eea8797d3e86`  
		Last Modified: Wed, 28 Jan 2026 04:09:55 GMT  
		Size: 5.2 MB (5209951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f2edce9e2339659b99b66e1f5825d3b2180d7920ea5cdd02eac17995e5068b5`  
		Last Modified: Wed, 28 Jan 2026 04:09:54 GMT  
		Size: 8.9 KB (8891 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:858f8b506777c5c30912d00614f9563432d99d366904098a4efcabc1130fe112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142025643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4703cbe7d574073a8b9022ca7a029a15832839a8907f4972b543f275fb54ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:30:42 GMT
ARG version=21.0.10.7-1
# Wed, 28 Jan 2026 04:30:42 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:30:42 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:30:42 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:30:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404823810678926b839e383dd453caaa34f02e6990cdeb8a2e896c1069f2d2a`  
		Last Modified: Wed, 28 Jan 2026 04:31:02 GMT  
		Size: 89.1 MB (89109005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bb128649fc87b7448f7222d235bcd224b8211e8e7a3dbe854f67e9779ad14ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e143ae86498fe3dff61657a5f21b4458ecff482e4e9bf1036cadec74f99251`

```dockerfile
```

-	Layers:
	-	`sha256:4cb2d6153675a3bdafd31cae4eacc077960735c2c57aa42af4517b386c9b2208`  
		Last Modified: Wed, 28 Jan 2026 04:31:00 GMT  
		Size: 5.2 MB (5208744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9034f0571745c98126ec3b3ca8040749726e7eb3349bad8b88193b1f10f69007`  
		Last Modified: Wed, 28 Jan 2026 04:30:59 GMT  
		Size: 9.0 KB (8971 bytes)  
		MIME: application/vnd.in-toto+json
