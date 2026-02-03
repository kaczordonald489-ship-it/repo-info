## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:2756b5dd833b85430b9f91e81a1dea0459e8ff2f93bf12c34df6107455d1b78b
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ae38a3e8b12f97437326d0acb3dcf06ca9083b9d2b503666c72a969694247db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246741571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73486db28f3f9089c40d0523c505bc85f48b82f1dd2f9b61c97c61e722bcd706`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:11 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:20:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:20:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed928638cb803e837e3f7d66c80812c5f3e23ed747873f6911d930f8cded677f`  
		Last Modified: Tue, 03 Feb 2026 03:20:51 GMT  
		Size: 145.0 MB (144966615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2391b5e55f7a308120d6e388979a5d1713d423a8830cea4919e896993f785`  
		Last Modified: Tue, 03 Feb 2026 03:20:50 GMT  
		Size: 72.0 MB (71995715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ead732e14869239048de5a7d071a4851b000310c300e58692b039ce5c70a485`  
		Last Modified: Tue, 03 Feb 2026 03:20:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:679285e1f32de6cd838b6941bcba590307a540334131935fecdc628d3f3f2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7ae9e9863ee62d01a2e5958f2ff64e5cccffdee2d1156fe548390295c2f574`

```dockerfile
```

-	Layers:
	-	`sha256:a6239b37d32503bb53a08020302ff9a2ad1ecb957858b99144fd48986b61fbd9`  
		Last Modified: Tue, 03 Feb 2026 03:20:47 GMT  
		Size: 5.3 MB (5276438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992312d2bcd0fc74ef43af8af7aa72f0271c71b97d85c9fcb868c29a94d142a0`  
		Last Modified: Tue, 03 Feb 2026 03:20:47 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:efc35aa2ac325c3fba0c660b3c929f0f32371684cdfe2c6dd6614fe71c90048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243677248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2668346dc4c4363a7267000a5e6d475d68f5c32479dbc74af678651853b0f5ba`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:27 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee6b6c03e81c3d3fb9f6df4c4b3ba24a456aa66d3cce3b045520f30de3e674a`  
		Last Modified: Tue, 03 Feb 2026 03:23:08 GMT  
		Size: 141.7 MB (141729962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d23a1626c4cc4ed5da7fb02aff4e8043411c88d6e9ddb3d8b291168c755a34`  
		Last Modified: Tue, 03 Feb 2026 03:23:06 GMT  
		Size: 71.8 MB (71806574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751618e5de1f31f23e7a0d9958672739816dbc48f10227d2d63810a6325f9726`  
		Last Modified: Tue, 03 Feb 2026 03:23:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45ed154e3849186a22a2b7aa58aa2a0b243307fa14f0782ea210c27c06ef6395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9510ee277936dd41d23be5610fed88e441a4763ecdbf284f5150e2486a0908b`

```dockerfile
```

-	Layers:
	-	`sha256:4768be1edcbbd5ee4a4496442886e866e80e6007904c4f67b7595836579372aa`  
		Last Modified: Tue, 03 Feb 2026 03:23:03 GMT  
		Size: 5.3 MB (5282825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a58df9053c3fe52ade6d03b3f1ec7b81328a4ee4020ea7ada64ce7215e700e`  
		Last Modified: Tue, 03 Feb 2026 03:23:02 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:61f80da6714605c726a331f7f91cd3d9ca0ec869ab0021af54c8585a9a20b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246266945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8ba21b6e8f5738f33d56c06a6b441d5a31edea711669a79ac21a29e0a1b99`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:21:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:21:26 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:22:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:22:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:22:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad69adfcc4d51808f6f22619ad46da87bc82e1dd7a4c8618619435d6ed0b7a1`  
		Last Modified: Wed, 28 Jan 2026 18:22:50 GMT  
		Size: 132.1 MB (132079784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62f3e30f747c9deca0e68467873cbf71e6f7bf6760948e3c8b35917ec25672`  
		Last Modified: Wed, 28 Jan 2026 18:22:49 GMT  
		Size: 80.6 MB (80590916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1023d64163d453483621baee1e0865fc486aa1c5cc553b9ffb260976f1f64eca`  
		Last Modified: Wed, 28 Jan 2026 18:22:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a167b5fce33f48dab35bc5f434b22340a21493dc2ad3e201be36a5698c5027fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2baae8c0a396bb9d89594470cf9af03874bb3ee922299eb58e2c11294b3c35`

```dockerfile
```

-	Layers:
	-	`sha256:1408b2dd0acd58f3cfb51ee16bada4dadabb0c01394f1338d923509d6c8804bb`  
		Last Modified: Wed, 28 Jan 2026 18:22:46 GMT  
		Size: 5.3 MB (5280194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5326df07dad645d3350e9083ca38ba0745ce2f00ba915ef955f129482155c8cb`  
		Last Modified: Wed, 28 Jan 2026 18:22:46 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f9b01a8b819d8dfcf4d7868aa26a3b726e74e413e8fe3d0caa2f967417a09941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228486727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f669ab9f6faaf82d7bdc3afd1546b8ba8904b03bd73a5de28ea1f0f7a7a24ab9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:00:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:00:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:00:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:00:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:00:42 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:02:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:02:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:02:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e2d81bbd15ea30a3436c15b21bba5e4613dfa7471a0f7f15d836cbe0aecbc`  
		Last Modified: Tue, 03 Feb 2026 05:01:21 GMT  
		Size: 125.7 MB (125694848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a854882f47066d0b8e3e2d16ae8cb4fddabbd56862122cea1ec28e94009ec3`  
		Last Modified: Tue, 03 Feb 2026 05:02:26 GMT  
		Size: 73.0 MB (72953082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d094a4c49350b1e49e4783d45323c2f0e4ac49f3310cca58ea9fac741cf12346`  
		Last Modified: Tue, 03 Feb 2026 05:02:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8467eba618a6d080b9c689716e497cbb79b97d02f4924fc65b2166dcc50c8a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d796da3ceb75e4620784e8457182ea87ae6d398c7d37b4c648d4c60a916d73`

```dockerfile
```

-	Layers:
	-	`sha256:2e58d619931668ba790d3392a0377d22c2a71d7e93a70862bf70ef6a526cb9ee`  
		Last Modified: Tue, 03 Feb 2026 05:02:24 GMT  
		Size: 5.3 MB (5272366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e11f7dea9469e6b77b045424527156cfb6b5ee85ed9371dd823765ba857b121`  
		Last Modified: Tue, 03 Feb 2026 05:02:23 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
