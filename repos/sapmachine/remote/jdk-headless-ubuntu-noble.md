## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:f2a1e35c3ca20282d973b219a2683257d5b5d365e987726786ba68dc8fca9fc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:b986a302d2c8023b6d03fdd83bdbda148582068adda5d11341d3c2513d54dc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248960432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c443d46a79346b63ae73d51a5a5eb1e104c385aa9dcd3fe037ffea4fc79669a`
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
# Thu, 13 Nov 2025 23:37:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5308128090088117c90ba97cf8b9bc610a30e3592234be5e8836bd0e7c56b0`  
		Last Modified: Fri, 14 Nov 2025 02:05:43 GMT  
		Size: 219.2 MB (219235744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3cb78be989fcfd68e2088f4c0fe7ae38551fe1646ff780f17b3e0b557091575b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef668c0b3457ff8c1266177bd6003c7244a709854d927547162a791d9c1cff0`

```dockerfile
```

-	Layers:
	-	`sha256:8aaeb04662c78fb5c60e8a1a152eccb5e47d0d892665329a9338669c94d6de3b`  
		Last Modified: Fri, 14 Nov 2025 01:12:34 GMT  
		Size: 2.3 MB (2348185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16e0f80d72deee27f176a954c71dbdd5568102f2a508f1fb6bc326fda4c738a`  
		Last Modified: Fri, 14 Nov 2025 01:12:35 GMT  
		Size: 12.6 KB (12603 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:eef9f02acc9ecfec2e2f23cef5e6806c8672ebe900ea922946ad0d7e207fb806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245847749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2380a776d691012afe212d5518d19435aedfc9b80aece1053f87d7bd2f8334e`
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
# Thu, 13 Nov 2025 23:36:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3eedebe2c41605c97e5361a4e400dc7d9f8335ed319681dc745a7118a608d7`  
		Last Modified: Fri, 14 Nov 2025 23:31:44 GMT  
		Size: 217.0 MB (216985792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f1f707509733f5ce746caacad8f27374723bb72f6d82a08293e532f89c91e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385132fb08f5a2a091b53cc77c72127638f479b43ce9dddef92a1e255146c0f`

```dockerfile
```

-	Layers:
	-	`sha256:6af424109272ac8cd488d8fb8992d3965db0029bcc562f97209d2d22215409a3`  
		Last Modified: Fri, 14 Nov 2025 01:12:39 GMT  
		Size: 2.3 MB (2348773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46389ed3723d257dab02aad6490e00da5c5c8836a7ee44ec1ed5d519d26b7412`  
		Last Modified: Fri, 14 Nov 2025 01:12:40 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0f81282c167007ce2417f8b2b00f3cd5c6b5d5e1d8229b47e6505c443e96903b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254184340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc819582d289f2402e467c71613be3b168a367839eba2678c5a89be8c87ff79d`
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
# Fri, 14 Nov 2025 01:11:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:11:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2007a26407ba523fead171bad13e90eaa04fd25e208cb94b072b22e1a0eec3a`  
		Last Modified: Thu, 27 Nov 2025 22:06:43 GMT  
		Size: 219.9 MB (219879916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c7e9ea41a2eb9ad0f7f7b64d04b4f7dbddb0996a3a2dc1507731e324ca46bd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d57043de74ac0a63e43ce2e1dcfc71ea6f74670443803b0e86ffe419349f96`

```dockerfile
```

-	Layers:
	-	`sha256:b5aebe42065517c13f33451500ad0e3c25337d492593f6f24f1c5108694bfca0`  
		Last Modified: Fri, 14 Nov 2025 04:10:09 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8112c3c119e8842f02b7dd40c90744d29ff33d3c82d18ba143f26f807e7b14b7`  
		Last Modified: Fri, 14 Nov 2025 04:10:10 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json
