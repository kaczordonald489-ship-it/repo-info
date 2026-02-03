## `clojure:temurin-8-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:0f84a161a277d41cd8097755b44a5a05365dd535653eb59a66ed6eabaab27586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4ff0fad541b82e1dfc06bd747527533e622500db75b0cc5434e362fd86fc6e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189569044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d068cdb4e634876eb18a5a241be9b9c9914259f175cc343508ac20f8c2a7db7d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:17:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:17:51 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:18:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:18:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b4af6dff8f989c4aeed8efe6ef691cc42b8f3ba6179cf9941bed6ccfc3715`  
		Last Modified: Tue, 03 Feb 2026 03:18:24 GMT  
		Size: 54.7 MB (54733365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d95f448a0b5583a27370966519e49d66ce033dff7b59828238b2779900cd35`  
		Last Modified: Tue, 03 Feb 2026 03:19:29 GMT  
		Size: 85.5 MB (85542081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2853b0a1010fa40a4a2bfcf5acf9442c5ec703a707de69e63bba122cd740a2`  
		Last Modified: Tue, 03 Feb 2026 03:19:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:767a090d1e68c51230c79b0ae78baafacc80d199bd172edb22358711cb5b0907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adffeafef62866d05481fa694a777adb3fca0c7b9606957d06080c8d8c0a656b`

```dockerfile
```

-	Layers:
	-	`sha256:f064ebd6347d23a7fc4d7b1bcc207a143f370de7789810fec9b4404b12a10a3f`  
		Last Modified: Tue, 03 Feb 2026 03:19:22 GMT  
		Size: 7.6 MB (7589436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658ea17713852597f7cfb69f99b549914d4b1861ae374539ca3bf4e6ad4a22ce`  
		Last Modified: Tue, 03 Feb 2026 03:19:14 GMT  
		Size: 13.4 KB (13369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b2083c4d64cbe9ee088953d1e7f9fc30945676c6a29d10cfccd002469b60717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188828669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd49489e7d41dbe227fe223d0bc79ecbbee88f0aab4b8436571ef91c3d774653`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:21:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:21:17 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cdbcd3c6b15792edbf1aadd71c7250676d9109d4a8063e6ca414241155545b`  
		Last Modified: Tue, 03 Feb 2026 03:21:56 GMT  
		Size: 53.8 MB (53814986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393e05ac68df32c7d97de344c4e0e07201073027275ca0a31723c1d577f2248d`  
		Last Modified: Tue, 03 Feb 2026 03:21:57 GMT  
		Size: 85.4 MB (85361022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f975a007d832d491bfa80d7ba856813d0544abefa0a7eaa82f829c7f2c4f084`  
		Last Modified: Tue, 03 Feb 2026 03:21:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b999ee8a236c34f954e35af8cb16e802ae5ebe94123eecc672b7f8cebab685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688441c8f24005b0f2b0cc64a83ed01ae3b9bcff21a76c49acb1763ca97690c2`

```dockerfile
```

-	Layers:
	-	`sha256:10fe3397850ac914113b65e519add19615b7474146c4bf3cde3f3b7963fb3d28`  
		Last Modified: Tue, 03 Feb 2026 03:21:54 GMT  
		Size: 7.6 MB (7597164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd37d4eb4c7c5af1711ffc73dc1f35862f90dd30da85bc26dc1b368cc6c038c`  
		Last Modified: Tue, 03 Feb 2026 03:21:54 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7cadb86633446a447681e2edb13c6075812dd472f1721e1ded894973ecad5e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199435286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168ae73cdaa12b1d8e5ef983d277156c6f14d2046010c6dfd34ae2ead35734a4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:14:15 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:14:15 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:14:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:15:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:15:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b34b5b8592bb3be88a87ba608937e91bc4eafdf037851a2b30c77121302a62`  
		Last Modified: Wed, 28 Jan 2026 18:15:46 GMT  
		Size: 52.2 MB (52175137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2c40ff1aec727c0b125c7861b896e03f85d1edf46fbf0007d637227e3428e`  
		Last Modified: Wed, 28 Jan 2026 18:15:47 GMT  
		Size: 94.2 MB (94152541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6c48cf430a1e3f2fbd9c1eeb7275ec878b00294d0a92d41d611b173b0679c`  
		Last Modified: Wed, 28 Jan 2026 18:15:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:222f028b68003e40f62fe833ab44cf10382f871190ccbecdfe7280e0b5236e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83fba4c4d2415e5ed97311241d193e0b718876c4ef470cdacbcbc1babc989f5`

```dockerfile
```

-	Layers:
	-	`sha256:ad6204332a7c314dbec982ba7caefde24bd63fc2b1238e527c746c114c77d4b0`  
		Last Modified: Wed, 28 Jan 2026 18:15:43 GMT  
		Size: 7.6 MB (7594450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723c9dcae89fae6eb69743bdd3be9dd893baa1fa0ecb7d8b52d023ff73900cd3`  
		Last Modified: Wed, 28 Jan 2026 18:15:42 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
