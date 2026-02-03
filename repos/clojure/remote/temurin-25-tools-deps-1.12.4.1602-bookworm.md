## `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:6bbf970952cb7e2bb80000714b87e44cf8ee3f78ab1bfbd95e5e217506a4e202
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8866a4a0f5fe35e74f096381be5c64cc41fa37b176cf00b39682813f4958c57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221678251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc6f24a99e03b09474c5906af05865ff393f3edddf4cd290b24d725cb5fa1bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e604d36698b49d6ffdfc4ebf6b472e4b72903838c45ed8b8ce2125ac77b078db`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fc623b6cc4d614193b1a9e64c80e91feee6259f5cc3172a3d166a953ef38ab`  
		Last Modified: Tue, 03 Feb 2026 03:23:23 GMT  
		Size: 81.2 MB (81150408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc1a809877e6c17b26aaee1d4b75f5f69e4e22a682170ceae5cf43e8661f69d`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae7ec0c9a5b6b5724d904ad3b9f7a4127ef8eee0d308870bb297230fecfdc98`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fb2c444b7fc9f3a762657d20d376dc18c9573d177448f669478fa92e5a03dffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e20b83e83abaa85e86a93292992e35dc7d43e4183aa66da613a5c46cfd429d`

```dockerfile
```

-	Layers:
	-	`sha256:cf02cb98734aa2757facaf91b7e7c051fbb4b5d5df3e2ac71d55b0da6270a47c`  
		Last Modified: Tue, 03 Feb 2026 03:23:21 GMT  
		Size: 7.3 MB (7328199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48e1e2293f60cb76036a4f5e10087b348c41d6db20b24cc3b2e659d6212a2d3`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab91764d20f9a9e20a9e0e52da13abad65efd9387171a41acf5bee3f6cd099c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220557454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b19f2ef3b087bb21a14335ae9df066cab4789271181ae073e71b696e0b210`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:13 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:13 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5209cd1180975ed9b4cb5256a0e719f2eb5ba5c3c32b857be32712b7db7ae4d6`  
		Last Modified: Tue, 03 Feb 2026 03:25:51 GMT  
		Size: 91.1 MB (91052509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a113c2d259f8b5f6af8c385bac4e620d4a3905e37ab9256da74ea8c6d3f690b`  
		Last Modified: Tue, 03 Feb 2026 03:25:51 GMT  
		Size: 81.1 MB (81137946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba81b27bab3c910a62dbb04821f0d4f092816cb2dd1bdb36e91747f9d4fda93b`  
		Last Modified: Tue, 03 Feb 2026 03:25:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d21f1b2a893eb352fe98c94e06378a60109ddf8fc29b1033b9b2a343e774fb`  
		Last Modified: Tue, 03 Feb 2026 03:25:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4acb15b512c762ee648893e1bbc62ac17755d72ea95d69efb0776ce391cfeaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644d6d7008e46f4ca53ee108ece4b6428f7c9f74b3c212d202d190ab5c93c5ed`

```dockerfile
```

-	Layers:
	-	`sha256:2d15ed16cffbb447bddbc0cfc2045117cadd37366515df1f2049bb9638756c3e`  
		Last Modified: Tue, 03 Feb 2026 03:25:48 GMT  
		Size: 7.3 MB (7334031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e11aa9ef22e00c3967b6382ad334fd24ee783052413fc4f6ebd4512a1dd0a32`  
		Last Modified: Tue, 03 Feb 2026 03:25:47 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0ad403141c9e67d3bda30e7de5ea56340c2d78f585fd7fcb9c09fcae607f8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230926028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f33f7e318b15379e69240bb6a02132738546de1b941b49de0e52ee26fbdca3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:00:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:00:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:00:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:00:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:00:33 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:32:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:32:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:32:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:32:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:32:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fa589af2d7cc446e03d21ea40f1e5c774818b048bcf7c10ea2c7201d72d8d`  
		Last Modified: Wed, 28 Jan 2026 18:02:31 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b5d66deab728a4f82924ba403275ebdc53d6c24ed94b8cfbf95f5cdec73b3`  
		Last Modified: Wed, 28 Jan 2026 18:33:34 GMT  
		Size: 87.0 MB (86986822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963dd44626248d2bb78f98d53c874214ddb17e630572ad03ef2a9ddcf9401ff`  
		Last Modified: Wed, 28 Jan 2026 18:33:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc150ea611541ce340cc11f540826379cb234b11346be0819d6b6a062a6dd498`  
		Last Modified: Wed, 28 Jan 2026 18:33:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89578aad67bb1eba44ff941b8d7b18fcd61480fdf32418751a8aea1584d40680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0716c75a4e9291f5fa1df35fc5ed50874168f2c9336ebaa3e5bd46e929f3ae2`

```dockerfile
```

-	Layers:
	-	`sha256:b160c47f52896ca0a163980bc9a4ec99fb4646ed322607821c81a8cdac28223e`  
		Last Modified: Wed, 28 Jan 2026 18:33:32 GMT  
		Size: 7.3 MB (7334749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48eaf337a9e2bca96b37cbd192ffafb92ba8349491be732a2f68f0107f223d8`  
		Last Modified: Wed, 28 Jan 2026 18:33:31 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:07b670e58da8af1d9bf768bf32a1eca8de51af12bbee8ceca62de6edfd3895e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215312955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a07d3731df96f542823161490fa078e6b2c5d94f07f4eef614d0db8e6819e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:06:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:06:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:06:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:06:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:06:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:06:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:06:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:06:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:06:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fbcf9e62fed9a27010c243172583199c320889fe240163fa48c65ec281731e`  
		Last Modified: Tue, 03 Feb 2026 05:07:28 GMT  
		Size: 88.2 MB (88210680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c82570398ddbbb4d1d4689642187c8f3425c64185e830d7b5b407cd79c9f9cb`  
		Last Modified: Tue, 03 Feb 2026 05:07:28 GMT  
		Size: 80.0 MB (79962889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17055933c93fe4a12bf47e4896516bc9f9cf2ae99b28d422a7d6fd9034c5e9`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e4d369dc1f6ad8e7e1c64682e54c8c141eda912fe416eefcc1d5b8228a8493`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7ef54313aefc9bd7627a0dcd66d77612bf29374737cd0094d71853145d0652b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6eb5c8bab34444ccb0098228ed708476747c8b767ccf8896adf9c5d58ca4b`

```dockerfile
```

-	Layers:
	-	`sha256:3ba368cbe7fe1f686fa2aeff03d3fa12913cccb6c9d4318b5a6e253a94a1779d`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 7.3 MB (7322066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac05d94e64deef910cf0657913ade33d2ec7e515224e68e9b40020021c840fb2`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
