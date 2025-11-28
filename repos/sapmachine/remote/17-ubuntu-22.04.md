## `sapmachine:17-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:b8305e3fc4ebb0eae937824ecbe4f9554c79809be36055c18702ef756af6e5ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:3db78a0680c28e1975730ac797a028a1a63e2716634466a4d57d2e87777535af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229817037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0edd742053710d7c463bedd8565455ea623928cd7baad5ba824a6a5e9639c8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041fa410b0638c8f9834efdc5f0ced6ba0808626093438fdcf5ac9724b1aa73a`  
		Last Modified: Fri, 14 Nov 2025 01:30:39 GMT  
		Size: 200.3 MB (200280239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e440ba055cc860a280c98afe28ae3614d602d172ae7c834c93a39252add26a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c819e6321560428cf526ad790d2f074ce70eda91d572255fe833a090d34a5d`

```dockerfile
```

-	Layers:
	-	`sha256:fd03648c253fb6ff22a5468e8466fd93c4a392fc5f5273c37e3af68e5d7fd39d`  
		Last Modified: Fri, 14 Nov 2025 01:07:06 GMT  
		Size: 2.6 MB (2627863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e19d56ea27f51c1b2f9ee9b2f7bd769f533e849325ef1bda6a9b007f2dda585`  
		Last Modified: Fri, 14 Nov 2025 01:07:07 GMT  
		Size: 10.1 KB (10095 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b2a4685f03777ae98c6318cf437aaf359d1cd728364d928d7129d00fabbdcb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226335387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735df381886f56fa926655529fd8b3ff4013a00af12928d7edfe4d9c4898e4a9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:38:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b29d82a69e7d75c84e07a296736e1bed331709d60a768800f7be89c3c6daf5`  
		Last Modified: Sat, 15 Nov 2025 05:35:43 GMT  
		Size: 199.0 MB (198951510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b09de67268788f00df760d671ab209035b94b96e0bf1be3c6f02d0a8c803c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9945803b74d8ff2f94db26f7716db5bff1cd925b0924650535e7013a30d76ed4`

```dockerfile
```

-	Layers:
	-	`sha256:508ea2a849c0736230c685b30f1666e918240018ab700880ed04a62ef393b601`  
		Last Modified: Fri, 14 Nov 2025 01:07:12 GMT  
		Size: 2.6 MB (2627593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fd77454755ba7f27cf89c973ed90bcb76cdc0a25b6aed24c2bc7a7ea2ed03be`  
		Last Modified: Fri, 14 Nov 2025 01:07:13 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:87c6c2cf2bcc3bb10b9657a0d8e32a30510e85e9b3491fe95d630e16a66ff3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235413323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87714cbd1a7a67830f9302addbc5285af75f53231acd25cfc13ef77d034953c7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:50:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:50:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 14 Nov 2025 01:50:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8379e094ed7f7523cb1533f94f39cba71174c366f13ae705c044606f406ad620`  
		Last Modified: Fri, 14 Nov 2025 01:51:21 GMT  
		Size: 201.0 MB (200966601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:abef100136a612d51798664a564de098c115a28fbc44e5d4f4af73213647f5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e71abcfec326ddbb5872b8f7d1610062a71ed8a49b8d8947169d89df286455`

```dockerfile
```

-	Layers:
	-	`sha256:663a3d7d5a047b4960a2e1ba56c1b7ef6f7a5eaa97251b255655a0c302b8545c`  
		Last Modified: Fri, 14 Nov 2025 04:05:11 GMT  
		Size: 2.6 MB (2624056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d548bbd4d6144bb45e0a8f79cd93b35da74ffa7ec15bf46deb31c6623c26e50c`  
		Last Modified: Fri, 14 Nov 2025 04:05:12 GMT  
		Size: 10.2 KB (10163 bytes)  
		MIME: application/vnd.in-toto+json
