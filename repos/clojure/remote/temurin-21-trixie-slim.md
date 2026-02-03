## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:e9bffd744f10c58bdf716c7deedcc96a6350f8f19b9139211088c999acf6b280
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f54a96cdf5bf239591cd1b4b44e9a3722bf05425a8d1952129c7c5ed98114b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259601474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2823a4b6e3d276655fcca788752a48618e1c306083fc2f216912817ecf7fe11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483296f9719872eaa4ef3d1826e98b176a7c8ff2f5ea87a1a8d3f294bb180027`  
		Last Modified: Tue, 03 Feb 2026 03:22:41 GMT  
		Size: 157.8 MB (157826034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1cf1bea7b2676e1e6a27354096ea807bcbde653f06d30af63bcf75e39df39d`  
		Last Modified: Tue, 03 Feb 2026 03:22:39 GMT  
		Size: 72.0 MB (71995800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3a8e35a1e3edd570a21990bb50e963e8007cbc47ab28a70b2865740bb9439`  
		Last Modified: Tue, 03 Feb 2026 03:22:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3ae4f2b7ffdae39a80f29a740a064767e46be59c211077a6e9b89d773000f`  
		Last Modified: Tue, 03 Feb 2026 03:22:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1945cc3a586c0fbc0e304b364bc40a3fd1b69ad824a652359b6beed93fce7cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04de16012246aada5b0c0ab174880fed2e1102873b14f917784a899ebff99550`

```dockerfile
```

-	Layers:
	-	`sha256:9b8c90b0907f0ced79d3f648a156a0e8c14b3c6a454c346979848f72bdd81cc6`  
		Last Modified: Tue, 03 Feb 2026 03:22:37 GMT  
		Size: 5.3 MB (5259401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1b6acc7848151bfde746c44b29e6c5ed40218afa42242786b4429cea8bb353`  
		Last Modified: Tue, 03 Feb 2026 03:22:36 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:240b53cb10053f966e2a55f7fd877cb15e8427a402f2cd7ae0ef23b12b366d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258055240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b898e119ba8af8faf4b3629fbcde00af86c94ef4f5f8506503498fc8ac87814`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:29 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:29 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833e80b106cac26e6497d2006087a64c627272be142bcc3768915f028d7a2d6e`  
		Last Modified: Tue, 03 Feb 2026 03:25:10 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c8c6b6b4529dcbf6af26be4b3a5286a4e20ccd85c00fdfdafded4b2190e6f1`  
		Last Modified: Tue, 03 Feb 2026 03:25:08 GMT  
		Size: 71.8 MB (71806553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da13a8e5d4159cd6a85550c2614130f915c19f9f8e883483d0a084ec7338b36e`  
		Last Modified: Tue, 03 Feb 2026 03:25:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e4b47f5e6cdfc33f6179dffe2b1250afe428d37c0657bc0ffad53d2121de9f`  
		Last Modified: Tue, 03 Feb 2026 03:25:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd7488f9aa75c718ad95dc16eecb7fca71cf21899fdd96b59687b9d39f2da39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e812a6bb1b4d8badd05f4969c9be3831d089b436e95dfed001d5f600243b6377`

```dockerfile
```

-	Layers:
	-	`sha256:a1a79de2928e4e779ca9024542263c9d9aa4362f2a17cc964775489415139f0f`  
		Last Modified: Tue, 03 Feb 2026 03:25:06 GMT  
		Size: 5.3 MB (5265170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4610aee64bfa210160320476f478749da85cb5cbaa660cbd7eef46302abcf19a`  
		Last Modified: Tue, 03 Feb 2026 03:25:05 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bb903e4b948330162e1642958d2673bc984d2cb7b9e75a3677f4d423ab1c28d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272129860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0831c19edda23ef7fe16407a20d03911d3e23f38cf74616a400f62cb2a2a491c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:31:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:31:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:31:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:31:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:31:19 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:32:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:32:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:32:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:32:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:32:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb8f4600d979d25ba9491f1c0b276d63f57f611e75453e2f2d5361bcc2ead2c`  
		Last Modified: Wed, 28 Jan 2026 18:32:52 GMT  
		Size: 157.9 MB (157942895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155710f318c7463bc829ce3a6500318ed369d6ae183edbbde317a77fcb92685`  
		Last Modified: Wed, 28 Jan 2026 18:32:50 GMT  
		Size: 80.6 MB (80590322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb0bff8ef1f4de78cb60eca34ac9bd54fba248a5825c61149797bd96c5d00c7`  
		Last Modified: Wed, 28 Jan 2026 18:32:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b81899dd88f9085870cab4864f28f841484b47e29a8ac14fabe13486c1eea`  
		Last Modified: Wed, 28 Jan 2026 18:32:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f47d3b34e4cb5a67a47ceb93ab95b0011326671236975e98f07bfcf1f16d1d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91dcbb4b605a6706ea888cb76142c05f54e618935b98e2bf2f21032a7f79ed2`

```dockerfile
```

-	Layers:
	-	`sha256:2bc0accc996e753049857bcec3b058811ece74712d3e140f799795dd8d3453cf`  
		Last Modified: Wed, 28 Jan 2026 18:32:45 GMT  
		Size: 5.3 MB (5263772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c9ed171cd5d4f928c2cdf48f8bf8c8871da89a91dd5ced9f209bb93ca51524`  
		Last Modified: Wed, 28 Jan 2026 18:32:44 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:d8d5d3e5e25138d04ea82d75022894c7946040d230cffb8dfe72bf96fe2f30e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256345830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803799bc0b3c19d19ee267c29eb4276fec30531754ed0c7824e6da6488a4df52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:58:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:58:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:58:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:58:05 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 22 Jan 2026 03:58:06 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:21:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 22 Jan 2026 04:21:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 22 Jan 2026 04:21:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:21:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:21:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ce3d8fe97e3f0f300cf6a379bdf8a6818893898d0842fdaef865eeba68c7ff`  
		Last Modified: Thu, 22 Jan 2026 04:04:03 GMT  
		Size: 157.2 MB (157194340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd76cb8af4dd3e38c7eae3325e8a0d72fd9a14b14d9196f7ed152291a2e92b7`  
		Last Modified: Thu, 22 Jan 2026 04:25:15 GMT  
		Size: 70.9 MB (70878764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6701652d5cad47430c5847ee2d32e960cbce9eeba80ae41575f27844dd3808`  
		Last Modified: Thu, 22 Jan 2026 04:25:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163d6293dcc1354641ef524165f4e596d16ea1efdac7a0239b30b8cdda7a6e90`  
		Last Modified: Thu, 22 Jan 2026 04:25:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44c725f99be72cc4a41677f685ed4bcad57bd6cf0e313ae48b9e61bbaa817640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb570a6660733c963afab1a9d5c884d5e894f5950c5ea57c48dc2dffc00ef8c`

```dockerfile
```

-	Layers:
	-	`sha256:9afaa7a08b4ec2ac3c028c1322907b57ebfdbce41d5c3edf445fbcbb1faeaabe`  
		Last Modified: Thu, 22 Jan 2026 04:25:05 GMT  
		Size: 5.2 MB (5248863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845059bf7a9f09dbecae5d277ad04857343d2075b936d47dbf30527de3ab71de`  
		Last Modified: Thu, 22 Jan 2026 04:25:04 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1671d07847d361f056d476ea067d8484e6200e2a8a1e07f80a0d227cbdcf8931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249861963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f57ea2e18f52b58fb2216119a238b54620f45f07509bbdfbb292340e67331`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:04:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:04:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:04:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:04:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:04:50 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:06:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:06:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:06:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:06:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:06:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ddacf145453dafd4beb96b06bd9815ba82a596f69a0b76695fe62e6eb186ba`  
		Last Modified: Tue, 03 Feb 2026 05:05:30 GMT  
		Size: 147.1 MB (147069811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44272bef96edab1725da6d1c0c6b5debcb613fcc8907b69d560017aa60578c99`  
		Last Modified: Tue, 03 Feb 2026 05:06:28 GMT  
		Size: 73.0 MB (72952962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3e7b7498b4be51f3fe20adadef4c5c87e045548366d772fbaed9837c0eb60`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceadabd8b75a3a6784823323246701ad2c70aacb54cd976bfcbdc6d6f8cba45`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13acbfb84559262bc4b3cc6d832592379d472acab1ad1c71197438b9494c446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ac3f7e33f8797567bcc9b76ce8c0b546bf3ca3e11e081d2e49b1c3cdd85a86`

```dockerfile
```

-	Layers:
	-	`sha256:97c66c5081218fe15fdd610c6dfecfacf7aa9966f18e6e1e150f91a8ecf1825f`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 5.3 MB (5255325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16b250399a90f1fbe5ba279ca90c115c6ee7d7049bad20d4503348b5fac7512`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
