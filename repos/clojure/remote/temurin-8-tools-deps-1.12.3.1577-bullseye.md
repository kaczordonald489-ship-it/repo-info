## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:56ca4df26f573229fcf8f5c42f7493f6cf888c6b1b209638db975396a2739744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7296d519b02666a3072f73c3cd9a21f913782da83b4d6bfb12283489f0634034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178051661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649e96cfe5d269c5e31b2cf0e4d3d8a6bbb57176c1e1edad27964a65cda3ef59`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:47 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:05:47 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:06:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:06:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:06:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde800e590dae1c95831d8504245611960d5ae752fc2bb16e92a467600488c0`  
		Last Modified: Tue, 18 Nov 2025 06:06:29 GMT  
		Size: 54.7 MB (54733362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccce14c7420f9bbf227ae2b21aa8f84db1555ef7cb4c15eeffe1d2d735af82db`  
		Last Modified: Tue, 18 Nov 2025 06:06:32 GMT  
		Size: 69.6 MB (69561223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fc7dfbce25d4facdfac06531ed7198f512d0ac03774ab3be5dbc519a51527`  
		Last Modified: Tue, 18 Nov 2025 06:06:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3546ed76826147850bf00636334dfef79d5886a7f01080ca4ff111bd31eaf9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9475f9fea27fd580006927a398a31c1e45f8e76e24c6d5658122837dfa2ee505`

```dockerfile
```

-	Layers:
	-	`sha256:45dbe4420f3c0c725ac6e98d28a1d5ea8366513d4bf706338d0df6af365dbf17`  
		Last Modified: Tue, 18 Nov 2025 07:49:36 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381e9b961c0259788f24bd96dcaa03cd33d849facff5b59031e30f0269abf791`  
		Last Modified: Tue, 18 Nov 2025 07:49:37 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e87ad49c09816a706cf1cb46792fcd17a081c0f1c9880c2e55f76e56aa592de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175761661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04e58889e42c0d5a6735ed6701f94127a901d9994c49a8dcfeb563fcfe54bfa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:54:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:54:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:54:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:54:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:54:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:54:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:54:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aa8384e088f7986c555b083a4bd843a770dac58ca8ec6662fb9ca40971df22`  
		Last Modified: Tue, 18 Nov 2025 04:54:46 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41c2c738e3c2a6a0df6fcdfc10eb881e0b2a1b060de2fe43cb548d18db7f000`  
		Last Modified: Tue, 18 Nov 2025 04:54:49 GMT  
		Size: 69.7 MB (69688328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d16058f7a23aebd808cb30f86988fb46f0576c689349aa551bc1e973f249da`  
		Last Modified: Tue, 18 Nov 2025 04:54:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ee4b59438f7e3976a78bec0c63b5aae6edf13d9bfd501f7df53374117b5e325a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db08688a7c9e1bcdf8bfce1495625d0790e54c2aa11d1389260c17c36aa688cf`

```dockerfile
```

-	Layers:
	-	`sha256:633f08115685777ece4c0c67c54670a4aa336979f3c8e71fd85f851d46265a4d`  
		Last Modified: Tue, 18 Nov 2025 07:49:43 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a17b2e754c73b9a4c32d9138aec4ca75c5c3549a60c3556091ebcaba378a43`  
		Last Modified: Tue, 18 Nov 2025 07:49:43 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
