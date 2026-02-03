## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:55bc85842ce50ba1c6b506534caad3db46699091dc2ce402fe4057560f89b363
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:119de933a56784d69df9b53cc65009eb805226edd163c0a3e8ff540a96ca9d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229620810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d468b70640989b35e7419c08c419cb00ba9cd254b5d594b72b4f05798d87ea99`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:04:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf41b122fdd2b19ac2931e6e8ba82ff97ec865f90303716f07e737c63fb097a`  
		Last Modified: Wed, 21 Jan 2026 20:05:12 GMT  
		Size: 200.1 MB (200084143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d4a623001551aec069c711cffe5328a6abf38d60de33db4f9a046de5f98ca80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d66f8eba52923c4cc437835bb7776483d8a7daee9f865d55aa69370c89fdee5`

```dockerfile
```

-	Layers:
	-	`sha256:3f3cafa11b7dce96211d6c8cf7d88f0d4ca63dc2e5b19a28dfbb225a04685c0a`  
		Last Modified: Wed, 21 Jan 2026 20:05:08 GMT  
		Size: 2.4 MB (2378143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f5958640c1a03b3a7f60dedbe9cb847956b5875dbf1e6b637ad7b87bdbde7d`  
		Last Modified: Wed, 21 Jan 2026 20:05:08 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:35627ff44541c0b5744909b3f60d74089119d85ea30c044c7fba1e899e2abd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226146603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a358d04cec1310912a41e405816d593bd86e398847aec95924d3ee8ef2edd25e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:10:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36397f16ce3eff786408d31c05e461544ad94672ac08b25234383197e5ceddd5`  
		Last Modified: Wed, 21 Jan 2026 20:11:03 GMT  
		Size: 198.8 MB (198763106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c6ebfd3e2d15f62aea142a848ed631eff9ec7e80b038d99f9152702ec4810f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a301f2329215faee45f133a1cd3e868f246378e821859648bd750830484697`

```dockerfile
```

-	Layers:
	-	`sha256:929ff01340b98d65a987a8da29a2c4b0f69fe3b049cbef05123bc877be458532`  
		Last Modified: Wed, 21 Jan 2026 20:10:59 GMT  
		Size: 2.4 MB (2377815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977e1173e5929a7e7824acbfdc41c7b30d6a0d4c47a4603fe3cd53fe22e409d8`  
		Last Modified: Wed, 21 Jan 2026 20:10:59 GMT  
		Size: 9.0 KB (8994 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7becc224e9294d2774f52ab91d0e4102c5497567b7bc3a08edfe6bca5a96e475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235126639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbadea080629cd8de17d91713a28c971aa598d7bf1b46283b0209f59cde1e3f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 21:31:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:31:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:31:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c70a4f98efbd66083f4b7376dc7da7d91abdaf49a18799bd7887a216938debd`  
		Last Modified: Wed, 21 Jan 2026 21:32:40 GMT  
		Size: 200.7 MB (200679677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c3745e6d6406cd5cfe3eefdbb624d97ca41c4c3274d98ad1c8392c8d926a3390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3fa65f91ff6af8e3c07c292338bd61b455c1d9f308909df3f977a87bbc3266`

```dockerfile
```

-	Layers:
	-	`sha256:f35df0c953576e6ee507e55775c93cae3cd50262b0fd29b49598bc017356381c`  
		Last Modified: Wed, 21 Jan 2026 21:32:35 GMT  
		Size: 2.4 MB (2375639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a69f5f882121a40ec5605165ad1c28aef36ab9267f461a2f95b38a055e5c3f8`  
		Last Modified: Wed, 21 Jan 2026 21:32:34 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
