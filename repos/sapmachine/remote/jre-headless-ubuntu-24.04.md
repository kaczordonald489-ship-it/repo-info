## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:36ad4f0fa4cb9ebc5af243f71199fe40067aeecbe71c02103d26b4aa990b1849
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:37e19573df52225e9323010dd80000d284dcb1851ce0cd07c78c2c36e7c10b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86275337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3442a7acb950f618d9083475f793c240e71686b2d12215b28b756b26722e306`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:02:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a161a153d9c802be8258a42e28d12d2580ad2370a62d1c87a837bf9a5cc4e`  
		Last Modified: Wed, 21 Jan 2026 20:02:49 GMT  
		Size: 56.5 MB (56549326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:33aac1e00e92109325f233c31f1593d68f28c3df33edb3275e57f9a5b9c8dac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6e8475dfab3331f4fcd04b907a79ee7cd89a8cc4b12550bf568d42bf8a0d1`

```dockerfile
```

-	Layers:
	-	`sha256:8ae2c81e70bd04cb3eab6a71e83ed614e7d411bafb3e02d55e279f9c40f7c55f`  
		Last Modified: Wed, 21 Jan 2026 20:02:47 GMT  
		Size: 2.3 MB (2282722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7ef95efec8d488e9bea31261fcc7dd3345d6093e3a81aad851d79768c2a876`  
		Last Modified: Wed, 21 Jan 2026 20:02:47 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b3446bb6f55516634aefc8fbfbb33ca742a4f9674a85aedf3cc16eca04d727cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84363877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e6c90979c5a410651848c1809f0997ca2f8d56f2064dc4f73b892d5fd995fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:08:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:08:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766408df45b14126337982449e93e178b846c7bdc5defd6a30ce6b29b6ee601`  
		Last Modified: Wed, 21 Jan 2026 20:09:21 GMT  
		Size: 55.5 MB (55500053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:73f5ff6f08f7f836978b0e747b62d74462250aa93f00baf39e6409e9a087efa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c90fb6ef94b6b88ea9a15efebb20d1c7054456243f9be457070bede3e71db4c`

```dockerfile
```

-	Layers:
	-	`sha256:a36d3471f7e00d49a7af96dd9bfcdbfe5529130bd8d013d052347d57d1b2af1c`  
		Last Modified: Wed, 21 Jan 2026 20:08:49 GMT  
		Size: 2.3 MB (2283310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f881ee22129bce59e0fb559fe83846d712884bab5542f55579f11240f962bf20`  
		Last Modified: Wed, 21 Jan 2026 20:08:48 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:65ca5ce3dabe11952a7a9286cb9296f85500be3873fffc9e9cd54dce5d173ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91654339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bd719f37efe8ad972b258294303bb374aa60b2d0228394190b5d35a08b3340`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 21:11:08 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:11:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:11:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2ed2d281017a1cd0ef43850ec9f794380b141ac8996d859848fe545f16e964`  
		Last Modified: Wed, 21 Jan 2026 21:11:38 GMT  
		Size: 57.3 MB (57348180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f57a7f0f6c3ac29db7fbefe8b9be811d0a5440407f518121d94bb77534c03093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca17cff4f98e2bd2f07bc6992488d8b0fcb0ed05190bb35e6adc401b3ababc19`

```dockerfile
```

-	Layers:
	-	`sha256:2fa893d2053e0dc388d8304befb3d606989eae81b5718ec62a1dc89d906a210c`  
		Last Modified: Wed, 21 Jan 2026 21:11:36 GMT  
		Size: 2.3 MB (2281551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91df361b8e6c7187ebc85c54589f6dffb7b1efa567256e8d7203a930df412b34`  
		Last Modified: Wed, 21 Jan 2026 21:11:36 GMT  
		Size: 12.7 KB (12712 bytes)  
		MIME: application/vnd.in-toto+json
