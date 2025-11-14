## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:5240f308cd276e7d0df6525a1752e89ef3d1bf5a2eab3f51e9ba045cd7ef4f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1f34992291b3339984fd532d4e2eabe7141766343d7c8ed22c0ce18f84856b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246622903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec958652aaf43fe9a7a00abf78ae7556151324055c539a4699b3937b902c575e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:52:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec673831a72559be1cd0fe46da8925268bbcf6231edde409c156b2e5bd92b8b`  
		Last Modified: Fri, 14 Nov 2025 03:33:46 GMT  
		Size: 144.8 MB (144847978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715ef59f15ae7d7ccb07b741cfb814cec11005ce9826b2ba2746f1ec5e97a11`  
		Last Modified: Fri, 14 Nov 2025 00:54:34 GMT  
		Size: 72.0 MB (71995777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0640800bf9c8795b1b42e72606d4806e685ef9943dcfc49b935264c1d269456`  
		Last Modified: Fri, 14 Nov 2025 00:54:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c27019fc8b00cf4322b57ce84ff6e62bc369bffc7cbed979d25a4f4c362ceb`  
		Last Modified: Fri, 14 Nov 2025 00:54:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:047855ac8f3758cd20edc4742c7178428e6ca6bbf2769bf610a6fc3e9be93ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2fa1ace9405e8f71f19566f4d1617ac345973876156489c09b2a2dda29a65f`

```dockerfile
```

-	Layers:
	-	`sha256:2d0156b5782c689b39ee4e855b30c537ebaa8bb47977b48fa6b3d20c3a522172`  
		Last Modified: Fri, 14 Nov 2025 04:38:15 GMT  
		Size: 5.3 MB (5256169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30f685c67017e9238857ba66f04469a43b215632626e32035ae6be5c4e9972c`  
		Last Modified: Fri, 14 Nov 2025 04:38:16 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:653964e6e73d37cb6011775716c5c4abeab6e67dfccc1aaba559355ad9811ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245631637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724beca3f971854769f7428109340c684b999b116d6331b6ae9261632529d691`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:44 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539b83a6c4f463ecae61a13323375dc31fb7a84e5c857f6bec1bcbbb826cbcfc`  
		Last Modified: Fri, 14 Nov 2025 00:56:27 GMT  
		Size: 143.7 MB (143679912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ffef44bd0452f321ac9c0409cb1e626960f54036118315014b2d13f5f0612f`  
		Last Modified: Fri, 14 Nov 2025 00:56:37 GMT  
		Size: 71.8 MB (71808386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9e2a0ef6f5adbea3be5b46952fb589baf9a3a70115c917777aef521d71bd1`  
		Last Modified: Fri, 14 Nov 2025 00:56:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d18c79fd8118976e21274fc6880f9ba0c3e84d05b89c304a56bf7abdbe26c62`  
		Last Modified: Fri, 14 Nov 2025 00:56:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc6e56b193439a0d9bc41d46647610e71887e94f2a9981ad9d8fe76ce2566d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826e0976d85aa8897593fb219fd600b03f2d9c75a3eb1af405d7810a9dba6b0`

```dockerfile
```

-	Layers:
	-	`sha256:4381896b3c1088c8629b289a452754074fcb9058d67b018415379feff31cb97c`  
		Last Modified: Fri, 14 Nov 2025 01:44:24 GMT  
		Size: 5.3 MB (5261938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9f10bac0fc97c069cd9ffe3841b9ff1d3ee12bc76733472b11e3fda51db9f`  
		Last Modified: Fri, 14 Nov 2025 01:44:24 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4b65cc9bb25bedfe4b6ce2e2db849e3c65255617163d969542f648d03ffd2a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255521345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4a8ec7d82a226bab77f6606bc1d1bb9e7df841321f723cf49c5102db833304`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:06:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:06:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:06:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:06:08 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:16:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:16:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:16:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:16:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:16:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c0b8920d1145986dc2b1ab28b2f1ed0575573627003c05e2df1cf5f419dcb`  
		Last Modified: Fri, 14 Nov 2025 13:33:40 GMT  
		Size: 144.5 MB (144525213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc226951be7d7889b49cd87b3c81215201257cee8274458cb1cb9f80e9e0ab`  
		Last Modified: Fri, 14 Nov 2025 07:17:10 GMT  
		Size: 77.4 MB (77396443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358826bc46df4a6e681e7a537239c8e1da685517a7b3ae39ac203e84c0e4953c`  
		Last Modified: Fri, 14 Nov 2025 07:16:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbb4884ef1f8aaf16db20615a91eae6517c1055c7d9d352f37e6e2d189df9b2`  
		Last Modified: Fri, 14 Nov 2025 07:16:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5aa5e8c2f4c3798632cbf4fffe35535e98a262751b84a4d31adedadc03362872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73eeec9983dcbb67fd0cfdd1e7e0c2880a8edf08b48d606f654f45bb3f2ec54b`

```dockerfile
```

-	Layers:
	-	`sha256:1f1adf8e2017daed23bf94e2cef1abb386ca8614c0a2000a7a51c7a999b3db80`  
		Last Modified: Fri, 14 Nov 2025 10:36:47 GMT  
		Size: 5.3 MB (5260540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8939f43141029b59a629ff8c7d0c245a6bd097ad12b23aff62210e042a081fa`  
		Last Modified: Fri, 14 Nov 2025 10:36:47 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6a8cd779fe8b63d843803787c175214edd927c4f6096388f8414dfb7b9524312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241047381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c63e1de4423d206f135a08a70fed651633bbc6cbcb006bb508939d85862b42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:21:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:21:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:21:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:21:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 03:21:44 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 03:44:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 03:44:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 03:44:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 03:44:20 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 03:44:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3bc662a464cc8c76c0909121505b0bd2314416266a8dac4aa9014c89143db2`  
		Last Modified: Mon, 10 Nov 2025 23:11:08 GMT  
		Size: 141.9 MB (141889561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004d6f80e0cb3558c9fe02916a5962d3a89727eca01bb4240204ebcba51aada`  
		Last Modified: Mon, 10 Nov 2025 03:48:15 GMT  
		Size: 70.9 MB (70880988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45abd6ed0e27918ccf886f07a186d50795c0091bc946e0e116682ff5ba1f2209`  
		Last Modified: Mon, 10 Nov 2025 03:48:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597010538ae1ce1d95a84c3a94c025ce22dae15b3684b61c80fbe22028193791`  
		Last Modified: Mon, 10 Nov 2025 03:48:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da876cb8710ad070389386920b3ed567bc92bdb89a6d644008c6bb6a029647d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99142899cef6789e3b14a431281056232dda95a9272e1ef738cdbc67e05d3e5f`

```dockerfile
```

-	Layers:
	-	`sha256:000d4b81eabf1af9665d95be0eec4d799a71aed2990eb150a3f00675d883766d`  
		Last Modified: Mon, 10 Nov 2025 04:36:18 GMT  
		Size: 5.2 MB (5243714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51542b49306001ac67a3bc4f29b8641dea8476993be64c0a9ea9e013cb5e62aa`  
		Last Modified: Mon, 10 Nov 2025 04:36:19 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:efdd0986d16ddc7ca3e772a6eda8f117bff8a6c6115df2b299849fd18a95501c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237651243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3d9098edc5372bd821db7f3cfb8afe2e994625b548f0be699db3eb48dadaa1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:25 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:58:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:58:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f13d1771014468c2762b50fac444775ee212cfc03b2579f1c62f791ba963ecc`  
		Last Modified: Fri, 14 Nov 2025 00:57:03 GMT  
		Size: 134.9 MB (134859068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cb8d02b5ed9fd549035c1498c79a680d1335501edfcceb47b9d9802a70e18c`  
		Last Modified: Fri, 14 Nov 2025 00:59:23 GMT  
		Size: 73.0 MB (72953742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f88e6cea5bb8efc2b154ab2d4c8d0f2bc6d8d10f0cf5e3aecab5112e44226e`  
		Last Modified: Fri, 14 Nov 2025 00:59:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad8d135317a4e011469dc902d98aec42c43a78d2dc85995295351458115273`  
		Last Modified: Fri, 14 Nov 2025 00:59:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6dbc774821706073caaf001035fd727714b1abf5f35005d393c2067c59cf46a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b587d0837402a8beb4712580c74e5172c91afa35fa1cada59c14de5dc200c1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a5e1226e5f5998a7b1a60261d9c0bedc7404362bd91be249009fba04d83ff9`  
		Last Modified: Fri, 14 Nov 2025 01:44:39 GMT  
		Size: 5.3 MB (5252093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35999569b2b4be780940e13fa346613d4281c624514a10bf2f55e7f78aa9a93c`  
		Last Modified: Fri, 14 Nov 2025 01:44:40 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
