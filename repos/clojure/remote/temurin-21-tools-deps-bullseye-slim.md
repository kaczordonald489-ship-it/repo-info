## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:85262d4447dc7e9bba4c7f44ab63b3731dee8c047e6d2e512a4843b72ce0886f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:695fba27fb5f9e82bceb2e81592f53b96880be77f4e080bb3b9d9ecd17592ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247237491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9a45eacc437d9f614e1edd8d9698838629faf05f57f79a7e990da12e83402a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:14:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:14:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:14:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:14:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:14:43 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:14:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:14:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:14:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:14:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:14:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de4a092d2770628b4ae8e0e792583d4e40f05db145235f2bc2e4846e224952`  
		Last Modified: Tue, 18 Nov 2025 07:49:49 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e2d99a9f325a4f38ee04a925d715b665890880865a542e02ad1ca9a35acce8`  
		Last Modified: Tue, 18 Nov 2025 06:15:30 GMT  
		Size: 59.2 MB (59151935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42afdcc092fccea89352be149dbc8d9ceefd4ce1136e01b0602f4f35a299c83`  
		Last Modified: Tue, 18 Nov 2025 06:15:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678b7c9c63775a747858568c4eba304f968252f9fffaa8e7964eb9334556953`  
		Last Modified: Tue, 18 Nov 2025 06:15:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3af75cd07b3e79f450f0bc6a356adfe0b041efcfe7cd48404a91a9b0b87a0cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12c28d8878bdf77eb8054f2fe741182b4d369cf467eaa9fb019b56c64143157`

```dockerfile
```

-	Layers:
	-	`sha256:591d09c2e2f2eca9dfa3b20688ed078e4f852c1560dc3bc8d7712ea0257f5124`  
		Last Modified: Tue, 18 Nov 2025 07:44:12 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6848d0fcf03be1a8f7cd043869f8a7fb59e8724559f313fe06e99301294a3601`  
		Last Modified: Tue, 18 Nov 2025 07:44:13 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ba2c7c863ecaf76aadda8d7ae83591b4631692904182e1c883599373c3a7d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244144772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fee238c8b96e57c6ccc3586fa50c62643931804539b2fde467e727d0d9638c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:10:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:10:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:10:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:10:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:10:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:10:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:10:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:10:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e93b112927cb86936bd6d0875d40ff5241a0263fb1d66fddf39e0263ad38ae`  
		Last Modified: Thu, 20 Nov 2025 17:08:53 GMT  
		Size: 156.1 MB (156107654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f943a28f15cdff230f1f64552cdf0679ae8f849c1a1a67c4e2f9d8f6e63f1ab`  
		Last Modified: Tue, 18 Nov 2025 05:11:09 GMT  
		Size: 59.3 MB (59287611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc07b37e9bcadbbd1618175f0b5b11a52912e60d8ef1865115a9b56ff68becb`  
		Last Modified: Tue, 18 Nov 2025 05:11:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcfd7e5b1b7f38cae2b6b2acf8ff0377a48ed2276d64c4282adbbf8fa6b2c0`  
		Last Modified: Tue, 18 Nov 2025 05:11:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64780853dbb10157aa781f634848efbc9151fc22367ac25e71a85b070d88c3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c463ecfb4c528dc6735a1ab3a98f8122091a638f6448eeed1b6dcd79942e67`

```dockerfile
```

-	Layers:
	-	`sha256:21122bb6822122c22b006e4b9709a232338762831862a1ff4ffc17d3c04e8683`  
		Last Modified: Tue, 18 Nov 2025 07:44:17 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4211b5e389583e8e315371e9476669b06abb6d480497de5f7719d21f61d6c05`  
		Last Modified: Tue, 18 Nov 2025 07:44:18 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
