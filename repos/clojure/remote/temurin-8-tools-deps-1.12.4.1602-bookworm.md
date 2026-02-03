## `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:752e0cdbc4c8428424e81f9ba93211fac5f81e4db0627e202ebbc0352b435f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d3b9578b19ed0104ef9b08125ad24cf9705cf15973b1fe56f8e7f39c6cc9af8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184365886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05eaa320a391f6dd975053e5af0a6ac50a0fcd2a39bedd9f3cb0ff4a851cf906`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:18:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:18:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:18:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:18:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:18:11 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:18:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:18:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd554fb9b815178be5cb498507ed112a5811dfa16e24d01cb09fce8ae5b8b963`  
		Last Modified: Tue, 03 Feb 2026 03:18:47 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9314353d97002bbce17ffbf6303d574dd8fa606e775a940fe490348c1aac7ed`  
		Last Modified: Tue, 03 Feb 2026 03:18:48 GMT  
		Size: 81.2 MB (81150387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57814edaa7786fcaed4e565321a257e10e80230f98a8a4e9ce8a78d765a65c0`  
		Last Modified: Tue, 03 Feb 2026 03:18:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:38c9ff3b57e7ee701fcc99eb4956826b8879f67cc3174dd2df29752582f75493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1d04a9a6f2fda29a5f61cbc3756da67d6df48d014e033e592b95850f3ff9ad`

```dockerfile
```

-	Layers:
	-	`sha256:19646dc751914e5c97885b868b746403e2016ec6db1c2bd7c39d5b1c9f048f74`  
		Last Modified: Tue, 03 Feb 2026 03:18:45 GMT  
		Size: 7.5 MB (7497145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a362aeea4f535a516ca37e809e6ed7e3e994ca7d30de34792a0d99677acfee`  
		Last Modified: Tue, 03 Feb 2026 03:18:44 GMT  
		Size: 14.2 KB (14193 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f66c5c64448540d344cff237893499091834ee6d457b5719b8a338612eef1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183319869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc1624d051f03cb491be47aac482adb1700d4b96468196f8e10ff20f92965c7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:13 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:13 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfcd22bd6506af4c63a39832b537c2f551c0a9554b22111172b23ba39b18b5`  
		Last Modified: Tue, 03 Feb 2026 03:20:46 GMT  
		Size: 53.8 MB (53814986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9265ab7817b7d339b360386a8ca08d1e7bd83651940d67b854dec4f2105ac3`  
		Last Modified: Tue, 03 Feb 2026 03:21:25 GMT  
		Size: 81.1 MB (81138280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5385952b21b3e0cf1c00bfa78a6e3524b5466dddaeb396d611c422575a3bb74`  
		Last Modified: Tue, 03 Feb 2026 03:21:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:87962548066a5aafb3393ead74487c445b1df48e2dbe7b0f0b288980f2b0e02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7144a1cf7ea748e8cbbd438cb9bac0f3881a64ceb7a521731b1e7da598565924`

```dockerfile
```

-	Layers:
	-	`sha256:7a556514d17300041a3caf95fcb8c2680018acc6972e3dede7d1dc34770d7ec6`  
		Last Modified: Tue, 03 Feb 2026 03:21:24 GMT  
		Size: 7.5 MB (7503606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0613d0764b54f540c10b15532540d1fc84b2b408737a3f2ae50f36b64b19a3`  
		Last Modified: Tue, 03 Feb 2026 03:21:23 GMT  
		Size: 13.5 KB (13512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:02dc6f7eb84a76bd7771cc512285d8664614410b04baa2063175c747b6f18621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191490753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29544c7169c4c7cbee830baa852ae5498db641aa7bb140bb0c9cf472c0959748`
-	Default Command: `["clj"]`

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
# Wed, 28 Jan 2026 18:01:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:01:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:01:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bb83329a0c5fc6acd22d5872bbf056865238fc896237be5785fd14f1bcf9d`  
		Last Modified: Wed, 28 Jan 2026 18:02:08 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d112b5d2c3e3696ea1cb216c3fc6dd138abe09849fc424fe7f8e72cd1e82b518`  
		Last Modified: Wed, 28 Jan 2026 18:02:08 GMT  
		Size: 87.0 MB (86987596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7964e0031882735fca1d411effebd5ffc926d7b417c818f8c7bd85dc9a0c8dac`  
		Last Modified: Wed, 28 Jan 2026 18:02:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1694b7eaead272c90c68f3aeba606752c44c7426340ac6fdae3147abaa1e7050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d69f8901a5ea347acc6222217ee89f1439f7dff326c1835cd18a5f6e3d3eb49`

```dockerfile
```

-	Layers:
	-	`sha256:3c47527c5899c7dafad73012560b2c700af3ac6e59c573ba9c677bfbf13311fb`  
		Last Modified: Wed, 28 Jan 2026 18:02:05 GMT  
		Size: 7.5 MB (7502954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d090986c9af6b40791c1694177cf2e73d26e7f2f4522f1433a76603031e9d898`  
		Last Modified: Wed, 28 Jan 2026 18:02:04 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
