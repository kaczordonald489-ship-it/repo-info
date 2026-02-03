## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:d30c2d5198a909b0c7e7582b4f551bc70810a7440a5d4468987528b5918b6dbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3e2278072fb96a945012e018b944c46911270258a9eab80d4de0e9086e0cc7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181441100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374c6ca79e950cd309a19461f767f9a78f0bff94784657b7374bbe3ad69aaf54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:03 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b987242f9011d1bb55586248e372f067755e13078d0638640d600818fdc9f`  
		Last Modified: Tue, 03 Feb 2026 03:23:38 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b78ceb72bf13762a9cd31ae30b6078afb131fc0061f433ad8a3223fdbbb546`  
		Last Modified: Tue, 03 Feb 2026 03:23:37 GMT  
		Size: 59.1 MB (59136470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4698cbf1351e6bbfa26be70c9be17384fdd860750ce5d57cb5b6e1d9cf9d0fd`  
		Last Modified: Tue, 03 Feb 2026 03:23:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16568603aeea38cc10d408f751ea1833d5247e1d49a7ac2a6a56e242f9b13f`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81f8f4df3acb35466f4dac2d433b6d18f50a9565ddc21a692341dec22c990b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84065bd47ebd8614616469ecfe93041870403d922656ac8ebf4c21491b0d97f`

```dockerfile
```

-	Layers:
	-	`sha256:338da976e4ead7615b1fa609bbb6fac451b1032122a762646659924b8e20be73`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 5.3 MB (5260226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732c3b2f606f3c7be01de763edede47927885e8ceb9cab54f81f90e441db9459`  
		Last Modified: Tue, 03 Feb 2026 03:23:34 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb48a5e8ba75f9912c8d616ad4eea3b76ca3d92626d0a950914f826f3b911503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179085971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410fd31f087254638c4e60e66a6d5dbfe3f94aa94b6c5761d414659bfbd622c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:25:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:38 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:25:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:25:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1a7ec6228a54257632ec69e84adf522cf5429dc8724eb18b7c3cfa08a30d6b`  
		Last Modified: Tue, 03 Feb 2026 03:26:13 GMT  
		Size: 91.1 MB (91052511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f49f512e97e18b00879c5732ebeef6be27b1aae5d37858b6dd4841c3e2da343`  
		Last Modified: Tue, 03 Feb 2026 03:26:13 GMT  
		Size: 59.3 MB (59287978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d32ed4c4be0e53263617879991697dde4561578f0e1514612139e1af18f39`  
		Last Modified: Tue, 03 Feb 2026 03:26:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30d180e79d86e6a8308cd2a14c5ba72646b4e30758a84ebda3b44e8e40d7360`  
		Last Modified: Tue, 03 Feb 2026 03:26:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:717875a6fdb4b376c08e6c45e408f1fba1f8a1061f2abad3b745448d850915db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac516b298b60cd8afe36acd7256e1fac22b133a148ab71de6dba4801ce788e7`

```dockerfile
```

-	Layers:
	-	`sha256:65728d8c5932f3ae8565bdf3c9cb92a89214f5188171a3fe367bcf3077c2915f`  
		Last Modified: Tue, 03 Feb 2026 03:26:10 GMT  
		Size: 5.3 MB (5265979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38262d96ae08ce7b1f467bf809519d979d692a867a8ac9dfd6bee185a9629580`  
		Last Modified: Tue, 03 Feb 2026 03:26:10 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json
