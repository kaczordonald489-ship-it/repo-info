## `sapmachine:25-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:fb1f6a73f3898da67262e6665ee70813c8086bfad9d004aad81ad6941171d160
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:5ef104105617e8c5422635e8f7eb5c5d2401255b5154615806d4e57276494283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249393019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6969c228bb5b0379ae9a5d3858484f35fda91c0414151503cd850eeb1170dedc`
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
# Wed, 21 Jan 2026 20:02:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8bb97245d9658e6f8183566c22006824c47484db0b0d45705a6aedb27b4843`  
		Last Modified: Wed, 21 Jan 2026 20:03:08 GMT  
		Size: 219.9 MB (219856352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0ce41f60437dc9efe9abb6c79d77fee1c8a787d2e178474786e61250bde19a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b31ea86e18e16418c22bb6b96fe68daecea073a11769f53b4df715985d84fe`

```dockerfile
```

-	Layers:
	-	`sha256:dcb85e00a21171023c5ff94cbbbb20eb6c9a641cdf2e090ce8b9dfa339beb9e0`  
		Last Modified: Wed, 21 Jan 2026 20:03:04 GMT  
		Size: 2.4 MB (2370870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e25791d93852af377f2b75abd21b0c0fdab428e1e0c711edd88f44a753a9b297`  
		Last Modified: Wed, 21 Jan 2026 20:03:04 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d5227de5667b8ccb4f2fc83c643a0e65ade87b823f719aa24bbbde39540379b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (244990808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea4a348d20737bff538500ca509b2ecb7fbf8572634b361c499093e4e5b55c9`
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
# Wed, 21 Jan 2026 20:08:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:08:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccf7972ef6308f0440a5a669ca21bc16d5b12e97a16f9559ba3fe1ceb7d46d8`  
		Last Modified: Wed, 21 Jan 2026 20:09:41 GMT  
		Size: 217.6 MB (217607311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dc7894ef31efb9fedbf0278271a4b919bc37b52bb0e43f4dc0039772c4b797cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb349ac3376574b7412305a217a3d73779d08fd9f7d218ec2c2d59aac84d5a`

```dockerfile
```

-	Layers:
	-	`sha256:39c0aa4bde4747a30b614428011b13298b557dc755f6a09bacbd7213d095cd37`  
		Last Modified: Wed, 21 Jan 2026 20:09:04 GMT  
		Size: 2.4 MB (2370587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a7e70782e9933a2b94545e493044faf64eaa5adacef0f6835f9f463f259836`  
		Last Modified: Wed, 21 Jan 2026 20:09:03 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:01ca96f4830e4ea005452449c49a226b07ae70850e8bc23c09052067678f1686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254928299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba80b95998c6186d0a76c7aa3f32fc99aa89f24c31055fe4813a06fd721a2ad`
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
# Wed, 21 Jan 2026 21:13:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:13:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:13:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cff634d77290706c7402d650a29f6f6a636843e9b6d4cf6fc56aa395a719f1`  
		Last Modified: Wed, 21 Jan 2026 21:14:37 GMT  
		Size: 220.5 MB (220481337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f8534e9049e9e3f15d5594a7d73cb8317d000d72c81fc73e2bfcfe23b52515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed62cf130b8792b20d50187811d15b43ca9af713f71ab694487398b812785b4f`

```dockerfile
```

-	Layers:
	-	`sha256:173c6de60530c2eacdffcaf55ab80a4296b748a1a83953bd6ff2b53884eb34dd`  
		Last Modified: Wed, 21 Jan 2026 21:14:32 GMT  
		Size: 2.4 MB (2367772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12aba59fcde0c75bcd0d9ac7d1c4f91d3435e2a230327570e6f9a14e3dd1cf9`  
		Last Modified: Wed, 21 Jan 2026 21:14:32 GMT  
		Size: 10.3 KB (10340 bytes)  
		MIME: application/vnd.in-toto+json
