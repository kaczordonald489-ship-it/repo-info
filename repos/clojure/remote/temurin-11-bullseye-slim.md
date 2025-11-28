## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:129b7896af049da0e57e816d8ae362c343fd01eb0bc124d5ff82a6b0d9ad02f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5b9643aea8b52d8d3a1654662b3b98f04c7a5133051e695498922e6d8f2bd8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234377716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6be0af4af060028f82082bc500ec2faaf537fed418d737ebc0e535f0689c2e2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:21:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:21:49 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:08:11 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:08:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:08:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2a6467ad4d5626da8abf33b8793e286aa9c7c90778260608598df063b1b38`  
		Last Modified: Tue, 18 Nov 2025 06:45:04 GMT  
		Size: 145.0 MB (144966584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8495f8de9a73b6eb93161b79ba9072915e34045d65bcf3de06f5b1c0aadef08d`  
		Last Modified: Tue, 18 Nov 2025 06:08:56 GMT  
		Size: 59.2 MB (59152003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b0fdf74eb3d6a34b4165c937ea812c9febf33fec93f09009515da7e12630ff`  
		Last Modified: Tue, 18 Nov 2025 06:08:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b0c13452cd5a90ad9b71c8531452babe945ba4bfab0ae2d1c95509a58d1fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b083412666daebd6fde57b24a25d4d33ab73227cc898fcc1209c1aba9b86a7a`

```dockerfile
```

-	Layers:
	-	`sha256:bdc2c9f4b5bb842f166d1157fc4162e1b14da8c3f8fa3d3e72e7e851ab6f03b7`  
		Last Modified: Tue, 18 Nov 2025 07:37:40 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ceccf8cf015bd3b9300dcefc8de522c51b308e3db851218f763a54ae97717b`  
		Last Modified: Tue, 18 Nov 2025 07:37:41 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8433d5dbeda61b9eb1e73299f4496cd80c7419ea93bdaca5ff23d73ef0e86f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229768259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850d77dfd8050c52aa2a7427acbac83ae123051d8434077c624e766b0ec681f0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:48:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 03:48:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 03:48:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:48:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:57:02 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:59:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:59:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:59:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e409d8923097838e94d274f9d85ef99ab4c5e30630806588f7ded4d05058f870`  
		Last Modified: Tue, 18 Nov 2025 06:51:02 GMT  
		Size: 141.7 MB (141731502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9850baf5a328c34e2a9cca2e2a9e4020882be71aa6b2710c9563ff6019918939`  
		Last Modified: Tue, 18 Nov 2025 04:59:55 GMT  
		Size: 59.3 MB (59287649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee095aa41ee33f5caac6658805d5a2bc29a4061ac79b4ff122635376202c8d8`  
		Last Modified: Tue, 18 Nov 2025 04:59:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49dd548e38dc4aff0285c6143df6db44fefff9a779f66381a922f930af611037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39ff9cf15cf4fa7ef3e879213018a694beec367ad9003b41fe3698d24d67d85`

```dockerfile
```

-	Layers:
	-	`sha256:fbbf7be953ade07806e9d4c6c90553107b9ea6ce3676ea3398a7d63d1d01741c`  
		Last Modified: Tue, 18 Nov 2025 07:37:45 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc25a4b8b6cc8a1c2c4ac25e5f47544db3ae977d962d36d2ef4056765288d3c`  
		Last Modified: Tue, 18 Nov 2025 07:37:46 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json
