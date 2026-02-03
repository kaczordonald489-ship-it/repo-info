## `sapmachine:lts-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:f55d5ac016a27d497c55dc52c5fef19c99aad662c14675200089663ebaaa2c90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:5f67724709ced4d7ccf2240293777b04381744337f2176e4af93fc52ab13b527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250603265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243d0bbd7b6613cd1f14d4b5923d52679eb6e6a5a68f150c5826bb01adb7ccb4`
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
# Wed, 21 Jan 2026 20:02:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ef876d524c9b6f7f4b168f5439a79a0bc17fa544e46b59baa7509162af55c7`  
		Last Modified: Wed, 21 Jan 2026 20:03:03 GMT  
		Size: 221.1 MB (221066598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:541efdea8abf42b7b641bdba653831b089863060194e84f49ee1c2cff066d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1a45dcc12fbf8bba1afe124d493a11941165044db29db8bf37cf99b5d8a9bb`

```dockerfile
```

-	Layers:
	-	`sha256:c7c3f7ab91cba357bb1c7463626580624dbadbe4d6442fe33e10bc198d5545d8`  
		Last Modified: Wed, 21 Jan 2026 20:02:59 GMT  
		Size: 2.6 MB (2624160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05998976424a102e191aec6046d0dac96f63feb65b5c1eeb8ba5e702f43ab908`  
		Last Modified: Wed, 21 Jan 2026 20:02:59 GMT  
		Size: 12.7 KB (12690 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:40c60681ecba00dcbdd47b70cfc0db59e89227bf0dc6b4b76fd4c424a1d677d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246203186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d1344fbc4703290b3cf853057c510112b1d6c88066f473046aa7da8957d6d9`
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
# Wed, 21 Jan 2026 20:08:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:08:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab82b9c5121ab81d05cae3feb0cd7c03729c7051e0434b8c426416d5090674f8`  
		Last Modified: Wed, 21 Jan 2026 20:09:42 GMT  
		Size: 218.8 MB (218819689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6def80ee783516eedeac9cf99141e783ec735914c7bdf7168b9b660c5b0b5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128d7f3288b1c4ab08785d70162eeb6026aed71e03bdec24f50098faf5ce24a1`

```dockerfile
```

-	Layers:
	-	`sha256:d192f045ea57e70b889e587276fb78ef063976fde2728c298f96887923cb2b2a`  
		Last Modified: Wed, 21 Jan 2026 20:09:06 GMT  
		Size: 2.6 MB (2623983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d173bcabcd1b1d9f0b42d5f23b2663ccc332433bcb91caafdc76b0e6958e2ace`  
		Last Modified: Wed, 21 Jan 2026 20:09:06 GMT  
		Size: 12.9 KB (12937 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:be3b6954c9966c0c313bc75bb280809ca439ac71440e948e6f421de6b153d064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256324696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161630fb4c83847ce06f613848c046f9c70a5fab3896343de9fca012b129aed5`
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
# Wed, 21 Jan 2026 21:13:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:13:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:13:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413752d607cf55bfeb5e4fdbe2a480d167d7092f8388904392a2fb4751f344a7`  
		Last Modified: Wed, 21 Jan 2026 21:14:43 GMT  
		Size: 221.9 MB (221877734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:91cad7f1424b0c982820ed57b89bdc3e353185577320f20161df70ded80789e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32316157e92da94362e40f01b1df146fc164f5eb8e3ea4ce543dc2503e364ad1`

```dockerfile
```

-	Layers:
	-	`sha256:1dfae24baf29b461322222ff85b44b7c675203824a50788c5df4e6e8f535651d`  
		Last Modified: Wed, 21 Jan 2026 21:14:38 GMT  
		Size: 2.6 MB (2621200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8143fc3a77bf27957bb44ecd9a2563d695ad84de918bdda24dab4427e84b1b1e`  
		Last Modified: Wed, 21 Jan 2026 21:14:38 GMT  
		Size: 12.8 KB (12806 bytes)  
		MIME: application/vnd.in-toto+json
