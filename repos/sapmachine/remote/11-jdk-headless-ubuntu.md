## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:bd0093ff95a66b0da512ced62e632fcda57dd70f4f5a23ed1f98389af49ba316
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:5113ec70fb2734823c7e094404e06022707f837e76683b8c4eb5dccb4b4c3388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229176564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b2f1a06edee68c0f185ad88db6e99b2df1f4a64e0d812f5bf2af49799a182`
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
# Thu, 13 Nov 2025 23:39:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 13 Nov 2025 23:39:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce841edffe95374e66c9363b872d422182877de0d5b0a62755ed4129079d78`  
		Last Modified: Fri, 14 Nov 2025 21:29:35 GMT  
		Size: 199.5 MB (199451876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d5f11baa3702ed10e8f169f85d83c1a710406660f88a979faf6cabd90fb1d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4ffdabcd8dc54da53ae4775d69e0d8a1b2fd3bb42ebf031269a3819aafbca9`

```dockerfile
```

-	Layers:
	-	`sha256:f3998730be88c7189e1865a31db530dab0d9b419da468b6dbdc08373a0c06fa0`  
		Last Modified: Fri, 14 Nov 2025 01:04:25 GMT  
		Size: 2.4 MB (2367212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36fc176685d49e30f89678c71a28542e199336c435da52d098160efd9d134971`  
		Last Modified: Fri, 14 Nov 2025 01:04:26 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json
