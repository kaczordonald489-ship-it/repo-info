## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f0484601a5a5e20752fb439d290a3dca10986134ed4d8e43752cbd3b888935b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a21b76b555a460a76d475d79c6d26c9095fd9532660611d29785a4178d04d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229201730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c9bd21bc18b2d53e4899815903ad16ae4732e2eea53b2490e7ab6cf71cebe`
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
# Thu, 13 Nov 2025 23:39:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3add33b8f33226600d8e92c707b7d3c96e02f031e87a59891603c93dd58cef`  
		Last Modified: Fri, 14 Nov 2025 01:39:11 GMT  
		Size: 199.5 MB (199477042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:709d3e768c8d701ca231a86e6136a5204d444b8091f53341f3fb1abc04a12233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212e163b6de8155bddee995f64abf4b23df54e3b39779a69c6a68f713d872f40`

```dockerfile
```

-	Layers:
	-	`sha256:3fbc33a44541661ee33df129ecf768307097ddc72bc4533568466336c2df03ba`  
		Last Modified: Fri, 14 Nov 2025 01:06:40 GMT  
		Size: 2.4 MB (2354472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3187d1655780b3f2cd51924f3b6c32efb3ee2e3acb062fe61989ccddfb4913`  
		Last Modified: Fri, 14 Nov 2025 01:06:41 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:12efbb6b0b1b1a85ef95de85379187a848a83d99ae62d2a2812e11ce0218623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227062386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2d6865090fdc0e2895ee825e0e161bc4eb6fcdcb13d12f6c399491f0a556a8`
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
# Thu, 13 Nov 2025 23:38:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:38:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64162347897755be74e2ad8ea944f498fcc6a008758b33745c544f9529ae21a0`  
		Last Modified: Wed, 19 Nov 2025 21:49:23 GMT  
		Size: 198.2 MB (198200429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3468e0f338681053979b6a02c0e25c0300821f05fa913ced0633aa6dc069f223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818c39389d8011f93f28d08413d79663da2478f715fef0fee3aaa7ffc9b7aa09`

```dockerfile
```

-	Layers:
	-	`sha256:1865286a2ea46a09003f3bb3bb09175e36ab650f24b5e4f3eb4876456e08bdd8`  
		Last Modified: Fri, 14 Nov 2025 01:06:45 GMT  
		Size: 2.4 MB (2354979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b3c629a7d41396529918aff1d8927ce2f88d43a8e8d9f7c7faee8839ab0908`  
		Last Modified: Fri, 14 Nov 2025 01:06:46 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d4e4d61865d69414cba4fe6e54654368209a2766480b519636fd8ce35e5cb033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234389775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b9bec5e084adceeccb8ebbfd91ac463161b8c76664aeae4c7cbfb8294cc6c4`
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
# Fri, 14 Nov 2025 01:44:58 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:44:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 14 Nov 2025 01:44:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f155498ac0d730c7480d4da3c2d5b49f1db349eb60c6e423955dcbf74823f4`  
		Last Modified: Wed, 19 Nov 2025 21:51:03 GMT  
		Size: 200.1 MB (200085351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e857aa25ec3eaece2acab58e85bb83b761e0500588cbb60d774be07b1b52b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fe7f358c2ec89c799c0cc2902a0d71c934dcdb903b8ac0fd0f4987eb4514dc`

```dockerfile
```

-	Layers:
	-	`sha256:aa9c37b459fb78b5f6494b43172bcb31fc7c1f8f591ab6e887ed351bd96f990e`  
		Last Modified: Fri, 14 Nov 2025 04:04:53 GMT  
		Size: 2.4 MB (2350526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b12b3df7addd35c277c6e6491d47c319d156de2924a2943eb901facde668f8`  
		Last Modified: Fri, 14 Nov 2025 04:04:53 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
