## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:06a32c1de904deb5d518a9a056be696120e4f8986dec86afece2799c9f34f5c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d0ca8590145b8b74c42e58189418da169d1f9c5612ecbe19776ea588d745bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144129030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299bf7edfaccc4dfa11642a2953dfe268934fb750c7309d9ac08a3e4c7571113`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:17:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:17:43 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:18:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:18:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc3a6966eeb6b68ab998c5df3275389d80b7147dbe2df0216a9cb2a9fa5219`  
		Last Modified: Tue, 03 Feb 2026 03:18:13 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3174cf8ba43d5f61a454fc5151aacab99b0aaf49aa1c3ceefdd172fcf80e61`  
		Last Modified: Tue, 03 Feb 2026 03:18:58 GMT  
		Size: 59.1 MB (59136709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce4696b30b14e3df60d5d3443c1d20c4e64781103a6f83a909127118c8483b9`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:729753679899333e8739ecf7f0fcdfdda66e71fdc660a9266bb879faef8d9833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6230803b33327cd52686d7e7582304f15be87707066e884586012476b92b2682`

```dockerfile
```

-	Layers:
	-	`sha256:72aabb57dd4f73886bb2a26db39870189310033eef10a70e1f25e5eb35dd7f6c`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 5.4 MB (5430476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2574badbea58b35611c952239320ec15bdeadd731552503871771732eb9062`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7ba1d5854999b78072f80a5a272b13f77a3f3b9af4d4abccb2e4fc096b78d2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141848165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88eb3eb6f0d517aece835b4389a804a6268b21f4ae44c8ac64d651de033b427`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:21:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:21:16 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dc335902a69e63f16d943f94dc6c81fbd226a3e5469fdfc2c3266b80e91901`  
		Last Modified: Tue, 03 Feb 2026 03:21:47 GMT  
		Size: 53.8 MB (53814986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8052af2f1e2471a670038863dbbd0cb380619b3de98075ba96c024417f9f5ffc`  
		Last Modified: Tue, 03 Feb 2026 03:21:47 GMT  
		Size: 59.3 MB (59288094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bc0a774cd8637d30dc70e23f4429234a830f493c56d7ab877623e4d8b595e2`  
		Last Modified: Tue, 03 Feb 2026 03:21:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27b7e9440ff5ae6ba349fbe3a0d58f0722aefc1be2f47425dac573199d5a45f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba3c9d20dca613d26a6710fd4a7b2a1f864b81585293a78ffb0d22b43b15f0b`

```dockerfile
```

-	Layers:
	-	`sha256:81987e6a80b832d09681245dc3b00b03ee0577389b6437b529d9c9db9a71c228`  
		Last Modified: Tue, 03 Feb 2026 03:21:45 GMT  
		Size: 5.4 MB (5436906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da370ac00ffa73dcb8dd0a3f8b39c6dcfff72652685ab36151708766d2f8397c`  
		Last Modified: Tue, 03 Feb 2026 03:21:45 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
