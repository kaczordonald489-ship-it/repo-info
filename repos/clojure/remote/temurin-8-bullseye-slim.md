## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:77e578aa094a7fbe6746bfe77fca3ab341b77779217f7347b0053cbbbec71f11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a2e0a9b4b428dc3d631ef6ba56739a26bb1d943c155ce33f14e81193a57ca7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144144373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2a8890e2270dc32f8caa3a42d1a342ce3051d46b06c141b78c24646db7980`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:05:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:11 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:05:12 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:06:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:06:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:06:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154ca13844bf3fc1369ab8f81d6b1c627106373131a35c8dda5b09b02f302e8`  
		Last Modified: Tue, 18 Nov 2025 06:05:51 GMT  
		Size: 54.7 MB (54733367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9d389df9bd6502f7321559f6701dfcb5723417049b40eec248e7f300fcb787`  
		Last Modified: Tue, 18 Nov 2025 06:06:37 GMT  
		Size: 59.2 MB (59151877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23972033fcddd0eff1bb259b9e60f4a1dfa2601daf5170fb821e785aedb55563`  
		Last Modified: Tue, 18 Nov 2025 06:06:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d494c3f877818ea3f5d5de3d412736d4125e56ecac93ae24fc2cf19382705d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c52910e8ac4906af26bd5908c88470a6e2134efcc61e2590690b005e2578af`

```dockerfile
```

-	Layers:
	-	`sha256:222c513afa24546e111a784908b30d2c0219c2d451e57491a671b4ecfe221dac`  
		Last Modified: Tue, 18 Nov 2025 07:49:42 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ef1a66a374039e3ee1de7f3d91a52ca3c1b4e7889384529e4471fc7db7222e`  
		Last Modified: Tue, 18 Nov 2025 07:49:43 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0ab3d595ed3ddc2e41319b9a6800d0bfcb520e7d3231f527be8542c12c973979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141851719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da6201329e20c71960bbf2c44ba37d492fdddd5a47a2a0546f0c6eef28feb77`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:54:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:54:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:54:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:54:30 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:54:30 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:54:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:54:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:54:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bdeeb631420b7b6c2c734f8e93f99e25897afd7bec3dec17506535cf1cd022`  
		Last Modified: Tue, 18 Nov 2025 04:55:12 GMT  
		Size: 53.8 MB (53814986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dca0e4a0bb00eee389d4dc7227e66919a2c7c6b925b99c8b50a6b8cdd2135b`  
		Last Modified: Tue, 18 Nov 2025 04:55:11 GMT  
		Size: 59.3 MB (59287622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c228c862c8753c2400e5166cc1c62accb44b6c5e6b5d8a43b15eb649c1bf21a5`  
		Last Modified: Tue, 18 Nov 2025 04:55:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0a46aabdf82c4ffc2390ad12d64bfbbe19af0bfed53a332b4ded33e4b4598cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c62d461e85dc4cc584170e330abd3a8c91da08a06ae9dbc8efe9bf69f8f9b8`

```dockerfile
```

-	Layers:
	-	`sha256:8e189412f6df923744826a5d5595c1643a814ada3da4abc90a25e2c90b0d7195`  
		Last Modified: Tue, 18 Nov 2025 07:49:49 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7204a21d86c3fb7794d049d9b1ff1e76f5bfbef03d53162d8a279cb8dd648f`  
		Last Modified: Tue, 18 Nov 2025 07:49:50 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
