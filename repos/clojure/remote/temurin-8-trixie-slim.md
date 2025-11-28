## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:cbc2aee3aba72c855920ae66ea59ecd8fe0683258ab9c6b4c50117d21908aebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:db0978fade25c66821ce045b4e1b684026c08ed2639067519c65b025b941a96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156506889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136d6fcaa9b9c9d9a1ff22b5c994bf51e815d5f137361a92f6ae7ff529c8bf45`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:05:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:05:21 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:06:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:06:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:06:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4630edd71fe56932bc2ebb15f6034cbf5774be33a4a56f4cb2481150a7762851`  
		Last Modified: Tue, 18 Nov 2025 06:06:02 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5936df85cc67f8032859cb8530c56daf72f83eb9020a6de1f4457dca42594a`  
		Last Modified: Tue, 18 Nov 2025 06:06:59 GMT  
		Size: 72.0 MB (71996370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3743d5f2e6f0b233093dea00c06a0bdd6e91c404f791f97ce1f0a7a73765377`  
		Last Modified: Tue, 18 Nov 2025 06:06:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:941296734d2cc883d1efdde74baa01126dad1de91e1af8dc6a3a479e495d6477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c405bfd4e23aeb0e83adcfc82f1b9ea7767aa74dfcd009b836092bfb4bde64`

```dockerfile
```

-	Layers:
	-	`sha256:4b3a48e48086d3489432533230dc515a041938690d670756826144ef56a011a6`  
		Last Modified: Tue, 18 Nov 2025 07:51:28 GMT  
		Size: 5.4 MB (5377807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e28468c572544b42a23247374f2a04a942f77f9061e36e5e587607f43f159b`  
		Last Modified: Tue, 18 Nov 2025 07:51:29 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1419acf49f88fef8b90a252f25d4aba37db5cd81889a58448da92b6da8c4cf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155762896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44574174aaf80a6ba9ab3083694b58848b042377d05e6407d130758b54ea8d8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:55:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:55:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:55:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:55:27 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:55:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:55:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:55:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685f2f37afb3c2936cdc1565d32765b4b8828d20f10b573bd3f215ca865f5066`  
		Last Modified: Tue, 18 Nov 2025 04:56:13 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c68d43e2df0b86663903fefd2ee14fda5c2985b95bc727e29c5c109c1b2dba`  
		Last Modified: Tue, 18 Nov 2025 04:56:15 GMT  
		Size: 71.8 MB (71808645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825badba8ade1d0bd06adae3bd76d19ae89d772f1390eacfb6b8c9e5226a5b4`  
		Last Modified: Tue, 18 Nov 2025 04:56:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:333bf566461e7e39f304ad8fcc2d78a0af7b2b603b61edab23a3f230f1b816a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aa302b9039ddea733ff3c7439962a87b2afc01e13fded09d9d534ffd123f57`

```dockerfile
```

-	Layers:
	-	`sha256:62787df245cdb846564f8571f38c588e2659b04a9fd3495a08a0927e441aa275`  
		Last Modified: Tue, 18 Nov 2025 07:51:34 GMT  
		Size: 5.4 MB (5384274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fa12d26b609d41f8ec0675151c97e91dd5cba1ea2834ea9d63f95082e0ded4`  
		Last Modified: Tue, 18 Nov 2025 07:51:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7a0f3fa674983d90de53c18b6f4e6ba477ddb14f9e123449781cdbacbdf022e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163164637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4d3079620fc2738639974bca34f97bd85c51924f461a3ce63ae2b1948fe997`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:00:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:00:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:00:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:00:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Wed, 19 Nov 2025 01:00:01 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:02:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Nov 2025 01:02:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Nov 2025 01:02:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71419e9ee2bd73ee8f94b7448e68f7185a7bb5e2552828526f349e1c2af2ff7d`  
		Last Modified: Wed, 19 Nov 2025 01:01:37 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d44086d962e56286d0085aa24829efb13db49701535d02cecaaab37ddfdc937`  
		Last Modified: Wed, 19 Nov 2025 01:03:23 GMT  
		Size: 77.4 MB (77391991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e8d8a20d6fe9716cb10997366952386e9b27e6f9ed52c0c0dc88d784a0aa64`  
		Last Modified: Wed, 19 Nov 2025 01:03:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddf69138d81b36f66f3aaf2fc0b08901409ebacff23d12d4909491fee43e5e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ee30f5f1712ea970471a2824ec6b30f2675cc216cba7f86e9cf00e95718436`

```dockerfile
```

-	Layers:
	-	`sha256:44bd62b7e98aaa452a3dc7c77afaa8281468597aa12cfcdb108487da49f1870a`  
		Last Modified: Wed, 19 Nov 2025 01:37:33 GMT  
		Size: 5.4 MB (5382771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9c35de22d75fc934248c94b6970480cab993f6e5185fd58502574b895edc6d`  
		Last Modified: Wed, 19 Nov 2025 01:37:34 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
