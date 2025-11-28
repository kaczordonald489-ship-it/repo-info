## `sapmachine:21-jdk-headless`

```console
$ docker pull sapmachine@sha256:e0557df9826b452c8dca17631496c826033c2cb325f4028573cff303604d7f5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:dec5804efbae1b0c11baf5a4eced9357bf3a16e52e88cb96c959aefcfcaa2d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243900318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80ea4b916ba868e07e1ef105747353624c45922fc4f8bf6ec88fc2e1d754785`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e408dc3501f6786fc4c2366373e8d12877abd7b19e922636957d8c40d74c68f8`  
		Last Modified: Fri, 14 Nov 2025 06:17:13 GMT  
		Size: 214.2 MB (214175630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8ba2f25d379be393b8bf0c6f24f9e67c7e7c7c5f52f3df77771a40a3c954e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b79a6998fb6747c7e3ad67086ea0f68a4abe9b9241d89a8f4023ba88186cbf5`

```dockerfile
```

-	Layers:
	-	`sha256:cfc2563e58ae8e248df041dee0965c7e7ecc7620a737566f890ec5789838ff80`  
		Last Modified: Fri, 14 Nov 2025 01:09:38 GMT  
		Size: 2.4 MB (2356331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad98753c308facbc2398a1cfe67500e85a90fd34a46187ecb8fcb100d289788e`  
		Last Modified: Fri, 14 Nov 2025 01:09:39 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed912ddbc064e90826166b446429b61826daa9f48a26cf30f058e3540beb57f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241277545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb309ad283e8fdca5b607f159f9c7057cc939aa67ec5402fc6820a620be8751a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:37:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b516cc66d6dbae7fbd3c247b33af46be9521800c3987aa4cec77494b7f367`  
		Last Modified: Sun, 16 Nov 2025 06:13:07 GMT  
		Size: 212.4 MB (212415588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36bac5ed87b86a630c9a8525e81f009c6c45961f54a09f7badbda027e33c4452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3efd69d7c3cb8a2b30c52693355273e562764b6b2794e8c34b4f77716267d7`

```dockerfile
```

-	Layers:
	-	`sha256:99bcaf5b8b549f4440d1887a5fe272cdc1f15d2eb9e068e86728ce52b007c0e4`  
		Last Modified: Fri, 14 Nov 2025 01:09:43 GMT  
		Size: 2.4 MB (2356838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a90bd2ef617e6299d6d700636b66c0e649a8397c4dc6ec7d4f384e3d5eb120`  
		Last Modified: Fri, 14 Nov 2025 01:09:43 GMT  
		Size: 10.4 KB (10373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4e4597b4a79eb179cc94a12ccf04d9cb877b510d3acf9e6cd74bfc1029353be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249225428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a5082993fa3320666e1750981c98a2a4f041aedd7d583450a6c9ea521fa4ce`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:27:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:27:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 14 Nov 2025 01:27:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b13cdd1af30402323c6a78fb4ea33eaa55a0a156069f1247aa04e14876b4a`  
		Last Modified: Thu, 27 Nov 2025 21:51:38 GMT  
		Size: 214.9 MB (214921004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8548d218d266cc34937f91340725126eb530fcb0175bae14a9e2c31a7c919b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b9234e9bd009a933c17168521a84120069f5fab513454bb5b2fa75b852f3c7`

```dockerfile
```

-	Layers:
	-	`sha256:68b49b42b846ce4474a075e73a44e28ec88d6f24f836229c871116696eb1d92d`  
		Last Modified: Fri, 14 Nov 2025 04:07:27 GMT  
		Size: 2.4 MB (2352385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d767cfd9a7897bb557a00c73058f9a2bd9a519ff13edeb9bddf2f1859eec96b`  
		Last Modified: Fri, 14 Nov 2025 04:07:28 GMT  
		Size: 10.3 KB (10289 bytes)  
		MIME: application/vnd.in-toto+json
