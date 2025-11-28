## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:1ff88c88a03efa2c543082a093c400e493f02b7c2450cc87ea037bc9e310f76e
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:89d2e5b40eb73911dd1a4c9791fd5c38db102e335c8530f602008f15a7499e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242874921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b905b446112a5010209f1c1397d0724495011bfbd590db41d46ad72d3a72c10d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:07:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:07:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:07:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:07:58 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:07:58 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:08:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:08:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15cc912b4c5ad5f27fd2a5acec8b2ec8b67fd1f4e31990f7d5d609b5a1e1d36`  
		Last Modified: Thu, 20 Nov 2025 03:13:17 GMT  
		Size: 145.0 MB (144966651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ae6023738d7f753482c0815118bf05fd8a4767b294cc34c8301d967c877c11`  
		Last Modified: Tue, 18 Nov 2025 06:08:45 GMT  
		Size: 69.7 MB (69679178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc2e9c682d93800b13b1bdb0a2f2b7f3e03c4717dc4fb464a6eca216a25680`  
		Last Modified: Tue, 18 Nov 2025 06:08:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:def30893ce7f0eb07489d690fbd343f29f762f8bb7a69cae8d0d881f96dda02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448eb40f51ad3728b7011e8a7d7e19aef1246d71d844dcc4e7c2d228be11e151`

```dockerfile
```

-	Layers:
	-	`sha256:547066e04813000b528fd95b8ab3032f7cf8dbe7489fca1938af238d4ffb5a65`  
		Last Modified: Tue, 18 Nov 2025 07:37:25 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68d11cd0042dd0944806a70688790a9efbcdda19f66ad8df711609fcd2eb155`  
		Last Modified: Tue, 18 Nov 2025 07:37:26 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b2a349ed38e6e8cb8f389844a4ca7c89a27c1d8ffa470e30380509e6419d44cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239394308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef78269a87673480bf957f77b54225837df8d25c72f7bb4a31182621561568e6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:58:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:58:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:58:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:58:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:58:37 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:58:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:58:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:58:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d56c3cb1d93be601feb8f1434be25080e170048f685aa3ae368a11c673d21a`  
		Last Modified: Thu, 20 Nov 2025 21:24:23 GMT  
		Size: 141.7 MB (141731552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a647826ce30b8a0516b8dd11c76eaeaf4bccb4fa34a0d9f4e86a33a137f63b9c`  
		Last Modified: Tue, 18 Nov 2025 04:59:30 GMT  
		Size: 69.6 MB (69559904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ffe531858cc191944604a6088ee4e2e3298b698529a3f9241e3dbcbe881af6`  
		Last Modified: Tue, 18 Nov 2025 04:59:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:738aaa37115a3d1b5fff21cb358e9fc1354127d00428f4f465b3b0ebd584af11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714d9d98bb864f9339510576e4a7ac23778f7a2b16d442c5cfe84ae43e47e83f`

```dockerfile
```

-	Layers:
	-	`sha256:0205f2c785091c1849f9891cce1197e4ee36e33e3935634be5dd37b167c25d0d`  
		Last Modified: Tue, 18 Nov 2025 07:37:31 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed915d86b6c7e0601577b3f03648a65221151d904e4e7e419b2c6cd1a4014080`  
		Last Modified: Tue, 18 Nov 2025 07:37:32 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:12a8e8282f1e9be08ae155620f03a9463db4204b9f32e0bc73c27a7d405d83a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239664756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63e98802263602ed0c1896a0b044ab22939e814a008fe17b27b96b851e379ce`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:20:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:20:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:20:28 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:23:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:23:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:23:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb45d70f1a9cc9b98db4aadb38d046c09df2cfca82e5e26482a0ddb0592166f`  
		Last Modified: Tue, 18 Nov 2025 06:21:41 GMT  
		Size: 132.1 MB (132081977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494335bb400a682bb9daa56262b9913c360f4a875575bf24e6afcdbfbf01ff2a`  
		Last Modified: Tue, 18 Nov 2025 06:24:21 GMT  
		Size: 75.5 MB (75513308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56be6a345be39cbb2b4053d8eee33d45222944746e2a9e6f1fc557339c5a1d0`  
		Last Modified: Tue, 18 Nov 2025 06:24:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09aaf31a51cc9a3663c74096b8df4f38c137cb8b86a30e2840e2f5c4c3c2ce1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edd9d57a83c3ea26f6ff0756cc4abb568c4818d984530c957391c3c0f14ca15`

```dockerfile
```

-	Layers:
	-	`sha256:9d62a800d2318d721cc42540a07184cf67c517f8d6364b5afa483530f6d7d851`  
		Last Modified: Tue, 18 Nov 2025 07:37:36 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a89b66de2275553f8fa2844661540301b66e08cea1a2c0a7a48f201f85ff546`  
		Last Modified: Tue, 18 Nov 2025 07:37:37 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:339778835949a1151591ad1c81eda5f3de27f3cd11a690b7c3715fdab87b5df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221069939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5b3f253a04929a97b1a84dd86c60d6c2175535717643669d65eb938497f9d6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:24:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:24:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:24:24 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:24:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:24:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:24:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b6906427e688e4a5fd35349c75fc025a2356109f24048c2267857962f7a2c`  
		Last Modified: Tue, 18 Nov 2025 05:25:25 GMT  
		Size: 125.7 MB (125694398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1327fdfe91bb936e11f6ea02b55ed9a332bffb0e4c4a03e6d142bd92cd313b4e`  
		Last Modified: Tue, 18 Nov 2025 05:25:14 GMT  
		Size: 68.5 MB (68490508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4023e19f0bb7988fb989607655d1391bb3c5410f266aa7032976ba256a22ed58`  
		Last Modified: Tue, 18 Nov 2025 05:25:10 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6b6609b05d7aee635ec870d551ced368544aebaec3235a037eee46744cf4cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74fc2fc4c16804fcbd269ff2764f7b8e2d277fe6d8717d409554b7546422a9e`

```dockerfile
```

-	Layers:
	-	`sha256:d6a6623e3f254b38f1299fb9ec41992d2bb05c4894a77030f1758ee8308c665e`  
		Last Modified: Tue, 18 Nov 2025 07:37:42 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bbb186e90f11e3799c084ef4dea7c01634eb2e80eb28e7cc05cba66894ce788`  
		Last Modified: Tue, 18 Nov 2025 07:37:42 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
