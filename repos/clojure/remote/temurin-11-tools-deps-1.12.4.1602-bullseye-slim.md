## `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye-slim`

```console
$ docker pull clojure@sha256:d519a817bb632c7f53eb33c32b324b883e5681f7bca6c3fa856579e060563e3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ce32af678c802e8e3e76bcea052fd56924526625745209632bc6f4948ca72ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234362171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0c448cb79816ae8e0b11e44f6fd20ace7315d6f816905bf12516c068cf7909`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:19:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:19:51 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:20:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:20:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da603ae7b25182d33dc3fb9fa8505726979fc0d0ad3aa2204832656a4c6ea8ee`  
		Last Modified: Tue, 03 Feb 2026 03:20:26 GMT  
		Size: 145.0 MB (144966653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2c10cc2d18d8bc403c1b13e7f74a6b38aa8666a486c3a8fd509fee87f14ed5`  
		Last Modified: Tue, 03 Feb 2026 03:20:25 GMT  
		Size: 59.1 MB (59136587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47def7654e78c89348b8279eee9be272a394edbc582c7dc036fa2933a75eac9`  
		Last Modified: Tue, 03 Feb 2026 03:20:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7262134491b31d70e338e8a0eec6795e7fca585e7b88a2f8b080158baaf11a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee062762c02b3fd28038b52183ebbd337de8cfdd4bc1c28d2afb2a0ab02c73d`

```dockerfile
```

-	Layers:
	-	`sha256:06852e581ce7d1611c6ad4852dda0b03f85b872d29cd266d00ad7e0c656c0fc3`  
		Last Modified: Tue, 03 Feb 2026 03:20:22 GMT  
		Size: 5.3 MB (5329007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c6b74d94d13694bf49517d694bf121f8ccba03d06083f6f5cb4271e9f858c5`  
		Last Modified: Tue, 03 Feb 2026 03:20:22 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66fd3781a88dac490d237962a8cddbc8f2705a09d6fd52e93e065938f87413de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229763278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac8c59886b0007b86c0c0d0494cb9eaa3f1bc6e865d3e99b9253b432420f4aa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:28 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12def992b3009bf1d458a00442714021b56f9443ae8e86cc39309304bd36ca9b`  
		Last Modified: Tue, 03 Feb 2026 03:23:04 GMT  
		Size: 141.7 MB (141729962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0d2adc5466ff71755aae2719464655f33496a8f4e1eea5f8ad4729655fe0b7`  
		Last Modified: Tue, 03 Feb 2026 03:23:02 GMT  
		Size: 59.3 MB (59288229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4267a342f90edc37528eec6dbfc027ee91f5e9a653fbdad515e1a30a807069a`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:043c00cd986f481675b1a683daf4aba2a0ae9adec67db0e8b3c3ae949e457952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87771c9f07b9895d0ff91ad7c9cb6991fb9e47d3e71d25715f6a24e8434ab1c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2e7637d16d7d9ca8ed10521065a1a517d0eb1056988f71d9c9c41be5d8e589a`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 5.3 MB (5335357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb991e228b6c348b59cfc379fc923a365c174a72e5d1e2c0ff9346f9cc96d4c`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
