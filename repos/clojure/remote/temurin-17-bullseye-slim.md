## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:f9011375282235101183b2dd105b546f589aa983d4ef54772e7ef01a2c56ad5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:489681333b97c31c685395a8e7ed5852aaf1317f35156771884bfd5b8a23dd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234259601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819256261b7456871ef76c914dc54b37899fc857f157c14a2dbae31caf606784`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:20:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:20:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:20:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:20:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:10:33 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:10:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:10:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:10:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:10:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:10:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c457558a99fadafdb901c6ccd5cc70bae08a6d6db54204a2fbff26105d90115b`  
		Last Modified: Tue, 18 Nov 2025 06:47:19 GMT  
		Size: 144.8 MB (144848023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800ac986b7fa1f9325bceb8ad793334f3282af04f0789d5af57fd2450e76924`  
		Last Modified: Tue, 18 Nov 2025 06:11:12 GMT  
		Size: 59.2 MB (59152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b336cb970e889afd75837f9048ffcca5ee4cc85b270a9354a324282d2076c803`  
		Last Modified: Tue, 18 Nov 2025 06:11:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7d5d544049e88606e1de10fcfdeaf9386bce771ee85b89f87a1b5917f62723`  
		Last Modified: Tue, 18 Nov 2025 06:11:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3322617cb74cd63c221e5cae4301bcd5e1e9c8c03d19bbb742a10dcfc577ec35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f1ab206107cb8e969ead666eb116b54ce59721cd6c13105860107fb2ea4e52`

```dockerfile
```

-	Layers:
	-	`sha256:6ee93e4d3c8ab418e3a74d51326937b1f6e1e35dace9477662a5cf0e6616de92`  
		Last Modified: Tue, 18 Nov 2025 07:42:39 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f614d598a302ad85b4095d2ac9a803798f073cc757d5964ff1e7e02d2719100`  
		Last Modified: Tue, 18 Nov 2025 07:42:40 GMT  
		Size: 15.0 KB (15032 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54a383ac137af20ebc9432527e07b6d2b0897c495cb7597e5f477a2a57aad114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231716987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8251e7e9511cb714b882004dff80a839a16d534897c308dd600d00829fb55b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:47:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 03:47:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 03:47:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:47:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:02:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:05:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:05:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:05:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:05:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:05:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1bf7cf8499be72efd862c35e030809d2d6c3b13d9de1bdd76c4bb60eba81f9`  
		Last Modified: Tue, 18 Nov 2025 07:06:52 GMT  
		Size: 143.7 MB (143679884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6064266997895c0f9079c9e853fd1676698404a0ba035d514a8b779e9884f88`  
		Last Modified: Tue, 18 Nov 2025 05:05:34 GMT  
		Size: 59.3 MB (59287599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dbee5ce32e60e58da1d710b7a9156621ef7f9704f52803b3600bad795ea28b`  
		Last Modified: Tue, 18 Nov 2025 05:05:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34027930ef4393bb361dd16e84a69417409268df14c4521a241e97bf0b128ac6`  
		Last Modified: Tue, 18 Nov 2025 05:05:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:00642cbf2bf61ef4e4c3b2a8685e1d5b60a935a71e676987dc03f2a321f6c272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce5c02152da5596965fcf222e018f5597107312d372c5d9b4652270ed8172b8`

```dockerfile
```

-	Layers:
	-	`sha256:6ee2bb55f3581f8d64c8775fa8db8bc27d706408d25a7acd58098c5bdfa1c2a2`  
		Last Modified: Tue, 18 Nov 2025 07:43:19 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a4ba8d398c2fb0f49a9c69910869d3bdc2f64254109076218bfb28059b8f41`  
		Last Modified: Tue, 18 Nov 2025 07:43:19 GMT  
		Size: 15.2 KB (15152 bytes)  
		MIME: application/vnd.in-toto+json
