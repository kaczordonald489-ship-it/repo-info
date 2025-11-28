## `golang:tip-trixie`

```console
$ docker pull golang@sha256:9025fefeac35e206b70b93401e3bb27cdbeffe88c16cc66c8ee2501e306d4007
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:45bfffd967e1dd6c72e9ef55a0c1a440efeeabe38f22250018fae13a31cc7773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337226540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20457d593233634f6ae1e3d852fa056690236196c963ed3447db681c38aeb3df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:35:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:13 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:13 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93140ce594be7615155bdad1fa0e5ff06321f5eecef3e2a5802efe294498a39e`  
		Last Modified: Mon, 24 Nov 2025 23:12:18 GMT  
		Size: 102.1 MB (102108693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5d9efbcfd700910b298e2e1f088186b48b23d603a67b46866474897785fcf4`  
		Last Modified: Mon, 24 Nov 2025 23:12:20 GMT  
		Size: 92.4 MB (92435230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37caf776b585e866247ed01e4f5e5cbcd2196c5c8463b8ddb75838ea629647c5`  
		Last Modified: Mon, 24 Nov 2025 22:37:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:0f8e442dca0488f3339adde78a9e073a770a19329218059db7167139b97df074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda24006edda0296963640ac9231133ad52884cfa21245756d23a0d78d2a9077`

```dockerfile
```

-	Layers:
	-	`sha256:1261280abdaadaaeb3b1155dcf778928fdfaa1d27a61d4b5dd0218b8f7ffb3c9`  
		Last Modified: Tue, 25 Nov 2025 00:23:29 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c028d023eeb2320bed77b5c9914305e55ea53ab50b30c2ace39b5028850922`  
		Last Modified: Tue, 25 Nov 2025 00:23:30 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:d06f5c233735b510ba4b316c5d2bf33ef6d5739c90138f8e8a430fc83db16202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293360058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bc9c33d735fc63d70b2521e741b4662eecb20f17cf860bee524d05bbb0245e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:35:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:21 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218357b2fe5eebbbbca9093d8622257ab1858f3db7823041be5a7f32e62a42d0`  
		Last Modified: Mon, 24 Nov 2025 22:38:09 GMT  
		Size: 72.8 MB (72754224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84acd51792b44af9faab6b3fd0d7f172d2f21a4324de65288c305f1fa5a5cb15`  
		Last Modified: Mon, 24 Nov 2025 22:38:11 GMT  
		Size: 88.6 MB (88553959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9304bbed295d8e9b85a0f68b5cdf927f6245eb499a62adc393cca7a0db32e1f`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:5c7fdd56bf7477bb6b0c50ee63b6106fe4531fc5e299c14e5587f0b27f112eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc42d1552880eed1fbf24ebf319984ecf41151fcff5f4f45a84c9084da03747`

```dockerfile
```

-	Layers:
	-	`sha256:668922fcfe12399dd69a85055873bfb6f4b3bb976fa3788946979dad35b8e015`  
		Last Modified: Tue, 25 Nov 2025 00:24:28 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c1789e909e5104ab4d84038afe9480713ec8cff3d05ced10a483df63b0d007`  
		Last Modified: Tue, 25 Nov 2025 00:24:10 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:0ee071ae200672bfb6452dcc87691818cbf1c38f8603a33eb4c98405bf04f626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328130529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4ddaf87ed20bcd735e37692bf2dfb3db514e17597a907e88cba6cc1727420d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:32 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:32 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:32 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0a93414a077e103a45f458108487fc81d464e46166c6b323c33303227d071`  
		Last Modified: Mon, 24 Nov 2025 22:53:27 GMT  
		Size: 98.3 MB (98254507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c063ea817571a2589abbf80a2044e326fd503e0a108dc319a7ad8231dbc1d73`  
		Last Modified: Mon, 24 Nov 2025 22:37:19 GMT  
		Size: 87.6 MB (87619860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f91ddb1d98f0e18c1c3d27d8091391227814692de509cb59e0069ac42c179b`  
		Last Modified: Mon, 24 Nov 2025 22:38:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8a7abd46a6523704da4d923af6b2fd92c89a55b4e2e6400e093117c44191f1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be74776ae78b77451deaaa23211d2bbaa99b238c37c5b9d17e0125e565878e18`

```dockerfile
```

-	Layers:
	-	`sha256:bbaf20196c88f08e789bd9fb4bc6511be352b66f0da8518f9e787f175dc35861`  
		Last Modified: Tue, 25 Nov 2025 00:24:35 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7a87e762621d0a24f95a47e12256b45ce1a0ac7dcab856703dd052eea692d4`  
		Last Modified: Tue, 25 Nov 2025 00:24:36 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:aa8b31cfd1e7bd4a706c6cfbbced254aec628bcee4d2875987ce163e28e0cb58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338300047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0a6a2a08e408e6c603a4f0f464feb5b206e7ce61621015106c6ede945492a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:15 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:15 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cfb736286179e6858e8b04a47a815f4071567b3b6f8b36ca52b15e872e6cea`  
		Last Modified: Tue, 18 Nov 2025 02:57:24 GMT  
		Size: 26.8 MB (26776415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c892592b339e9b2ca91d682c607a5e915b21a67ae25c1c71d1f3ef8ea35c2f`  
		Last Modified: Tue, 18 Nov 2025 04:11:31 GMT  
		Size: 69.8 MB (69803141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9e1b34b867d107be43dc0a8a201b6f21af35bd177893395e030bab8f98f56d`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 100.6 MB (100555299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba70aedae48e82029642c62322f6ff74fb35e5b6234375d05c3be6a27f83fa3f`  
		Last Modified: Tue, 25 Nov 2025 02:11:57 GMT  
		Size: 90.4 MB (90363290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b678d71cd0dc872062ce48733aa4ebe27c18379c8f2e0c6f0bfc1174ee3fee8`  
		Last Modified: Mon, 24 Nov 2025 22:37:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:feb699002f7cc30d757cd3319014277ce5b02576d6fe5f6e14608f92b66d61c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f142a8da1935afa994b9c2e3143a2930c0bdd10001f755502e76498b4b198f`

```dockerfile
```

-	Layers:
	-	`sha256:75416b9690d29f5d93713507c813befbc2f527420f4185b0778388c37c25f2b1`  
		Last Modified: Tue, 25 Nov 2025 00:24:44 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1160387dcbec3e95a23da61acd66388a2e6737fca82edeba63e8f3dfe860e6cf`  
		Last Modified: Tue, 25 Nov 2025 00:24:45 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:812e6c29f83c02e6bf97f6894e92639220060eed0c9048ae15fea8ae403e6635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.0 MB (335015416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1894421886e03893424152ffce92c01217bf4d8a223aab5bf70a33a7920f51`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:36 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f27d1d6766589192c9783cd48677f240bda846fcb9b1b3cc7956e55f813b1d`  
		Last Modified: Mon, 24 Nov 2025 22:47:08 GMT  
		Size: 92.8 MB (92815523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c192b4221bdae7479c6a0a0cefbefa83b4b143b2a4b40e323ae02e100ce6102`  
		Last Modified: Mon, 24 Nov 2025 22:46:59 GMT  
		Size: 89.1 MB (89072428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b525e17e7137fd229da32d2a7096f84f7388f0c19a95ebd4aa468127bbfb03ba`  
		Last Modified: Mon, 24 Nov 2025 22:39:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8a6f9d66418d0ff0d3a33c85138872dbef0d05f8b91490aa2fdb69ea20aa770c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e516c8c92327104e22f50c669be8d8f7bcae57abc9503961d603385dae2fad`

```dockerfile
```

-	Layers:
	-	`sha256:069c1c8c5f81f2b716a7b2158f03c85df8880cd0a900a2f2bc5171c228293cee`  
		Last Modified: Tue, 25 Nov 2025 00:24:54 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6a3fcfe6cf0d51603dae12114760d84e3d33f6cbf82dcecdd56f97132e4b52`  
		Last Modified: Tue, 25 Nov 2025 00:24:55 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:2bccd04dda994c93a1e8b8b57d5420f5d28978ee725a532b9acce42ac0b0a9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.7 MB (360659192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2169f3c9530cac6879360ebc4d6fca11ed770ba9491b59609b1435412e8973bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 22:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOPATH=/go
# Tue, 25 Nov 2025 06:38:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 06:38:29 GMT
COPY /target/ / # buildkit
# Tue, 25 Nov 2025 06:38:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Nov 2025 06:38:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d0f17fde453d9cf0b99bedd3dfac5dd06317d587dd69852c68ca1441ce0e8`  
		Last Modified: Sat, 22 Nov 2025 22:24:09 GMT  
		Size: 131.6 MB (131594403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737de4a2a89a200a514c4bb9d33946647ec30322b982a3272843e60840a135c`  
		Last Modified: Tue, 25 Nov 2025 06:45:54 GMT  
		Size: 89.7 MB (89678738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8b4a6dc3553e5332830083275a80d1003edc99a4ff6995f70b8030c856aa6`  
		Last Modified: Tue, 25 Nov 2025 06:45:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1360cd946ac4113d17d9e1f9a44b4b0b553ddd6af1657e70e9d78f5710237ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb354b97d10cdd79bb519299450684aa6b7456d73c52766a870d3be530830d1`

```dockerfile
```

-	Layers:
	-	`sha256:63197e752608866fb011fc9c05e3f1ed11eee0ffde60bcebe8ac1418665284ab`  
		Last Modified: Tue, 25 Nov 2025 09:23:41 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1b820d4899b7663101108f3a9a02261f463356efe68076c83be852ea6d3e18`  
		Last Modified: Tue, 25 Nov 2025 09:23:42 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:21913d62ff0f28b17a79145ab41dbe5d7797a5110727a14189ccdda3a2f27eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f135c375a7e3d75751728953b31790670434cc239fb783565956c7ca3573a89`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:37:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:19 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:19 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5391d091a5bc1ee814ac074a3bb08930ad54989e68737b6f3ab762b3833788`  
		Last Modified: Mon, 24 Nov 2025 22:38:37 GMT  
		Size: 75.9 MB (75919106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00d64c48f24f624221defe9715cae4847baad7ac3f98d927259b00270c75f2`  
		Last Modified: Tue, 25 Nov 2025 02:17:38 GMT  
		Size: 90.6 MB (90623953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d99ac0b0e47494d2aa39ee729c5bc0a7aa6524f62afcb7c26c08c6c25c1aca`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c36e4dccef71e613dc7c816c7ef66347523737d7078caed3e277a5982d64be6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b177af9fbca0868a1b5a0af5b0b96a6e808903935dd573663f7fb53bf0d2626`

```dockerfile
```

-	Layers:
	-	`sha256:3a35c157a4a759e214afa5a7be7b01ba2b2af706e4d2eee40013492360c3d3a6`  
		Last Modified: Tue, 25 Nov 2025 00:25:49 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d615f7daae6d48aeab9a79cc614756f7213c0479c1a0bfd52dd9c1bc58ae32`  
		Last Modified: Tue, 25 Nov 2025 00:25:29 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
