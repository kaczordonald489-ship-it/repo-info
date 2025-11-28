## `sapmachine:21-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:cee00c2b6b4628b6eb828130ec20cb601836d9e440a1311a86265fc5740b734e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:21a616f6c5a255e8d05e359b5486757094667b213b00518cd90c6208c7523b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244514695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f786bfc5ff412ed731a107d4c3692e422aae5fba2b2a95bc75900284cbee5`
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
# Thu, 13 Nov 2025 23:38:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097bf9a9077d690d696f2d941fc2bc0fb5abb1d2ba36db1789167874d63b1dc8`  
		Last Modified: Fri, 14 Nov 2025 03:20:57 GMT  
		Size: 215.0 MB (214977897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:02594520787999857b7ef5f681eda6b80dc2576346d59af713305b159ae242d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2fb6e34d7034fde9275219eb0dc6a795d6383b3f06ec56f2973deb3e75b611`

```dockerfile
```

-	Layers:
	-	`sha256:132e0a1c4be8c742307e2f08ef208a71d7cead2ac6bbfb471cd2853add167cd0`  
		Last Modified: Fri, 14 Nov 2025 01:10:03 GMT  
		Size: 2.6 MB (2629722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4575e18d8f71d38ab6cb3cebbed99527670a6fab628d22efc33cd20fa8841c`  
		Last Modified: Fri, 14 Nov 2025 01:10:04 GMT  
		Size: 10.1 KB (10082 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d0a8856d0e432ff544c0f157be604ccf9b933cc995573674e44ed901899c37ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240560307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba03177256eb4d6f5ab7687b07deafab4347118c8cbd3955714404603a4f089c`
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
# Thu, 13 Nov 2025 23:38:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce8cea5ccd757827a236795590437033b1ff723bda0ce5959ccfea89dcbd96f`  
		Last Modified: Fri, 14 Nov 2025 20:09:51 GMT  
		Size: 213.2 MB (213176430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1135dd8f93b1c73becc4f06575580150a7a99ef7830207cc35b942663095afac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000ab268aee38116450efe8e863b0d1d318926286e9b02f11cc04a475b1c4c9`

```dockerfile
```

-	Layers:
	-	`sha256:56af009e2de16d7b0a11e53026c973e1843bf1ba555b60308d9eccd001e15967`  
		Last Modified: Fri, 14 Nov 2025 01:10:09 GMT  
		Size: 2.6 MB (2629452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9014e8c19c3bb865dd7e7903f60e90d8ca3911d39b758c4c76f5db9948af06c5`  
		Last Modified: Fri, 14 Nov 2025 01:10:10 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:743a6ad5ddec80066681a1573b4055db8fc2975a8cba3a887a08abc7f61b09ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250261071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b73f01f18767ba602c6be250b1fc6b5cd4b24f4b95123467d70e85f09bac6a`
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
# Fri, 14 Nov 2025 01:34:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 14 Nov 2025 01:34:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dd422078f159d8cdd7b6619cfeac90965f4bce58f9c0fc84149af1fe6c1d06`  
		Last Modified: Thu, 27 Nov 2025 21:55:18 GMT  
		Size: 215.8 MB (215814349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2ca8ff683a0265171930908d469be696557c7c51890268e3fbcba905bf767ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d38afe3e95e5c91484733fd0642711be147655ac590890d2e6ee19b9083bd7`

```dockerfile
```

-	Layers:
	-	`sha256:5fbf304865bb1b3ee620f5b0cca5f1c7c96537a5f37798d7e86977c3268ef5f8`  
		Last Modified: Fri, 14 Nov 2025 04:07:51 GMT  
		Size: 2.6 MB (2625915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfab1c3ea684be0905c9559a7dfca65183c86697cb7ab0e2ba572d8c9e531c8`  
		Last Modified: Fri, 14 Nov 2025 04:07:52 GMT  
		Size: 10.2 KB (10150 bytes)  
		MIME: application/vnd.in-toto+json
