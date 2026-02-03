## `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:6862767844366f7b7674ad088905119aef30763472408e502b7316ec59b2ca3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:10e9d284607f76ff1146d2e3ba9330310df78e6f828dfcef3033e8bf9c33eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379a9855c7b5e8f9f8935a2d898c468a6b6c2e0681c54190483f17c045904895`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:21:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:21:52 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b6c7b693c716f623e0221c1c7f51db57203606e788c549a35888680cf7c323`  
		Last Modified: Tue, 03 Feb 2026 03:22:31 GMT  
		Size: 157.8 MB (157826005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e439905c886a8ff932c62550a80fab67cd78c4660ad786a52685976ce948e1b4`  
		Last Modified: Tue, 03 Feb 2026 03:22:30 GMT  
		Size: 69.5 MB (69541718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326faec0e44146007feb838db45ee31d7eaa2a4bd2fc8e7abf0ba032f21561e`  
		Last Modified: Tue, 03 Feb 2026 03:22:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c7e7cbe80b8fe4c8cdde33c239087d3f8ec351ecf013bc74b8302babbb59de`  
		Last Modified: Tue, 03 Feb 2026 03:22:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e9ca03ddaa38c01d4d4a7f24e800d87f890859242b94cf85b17953cf2d600249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10960182f5c064f4348895bd84a7f168c1544b0fdb72a6b6de0c648b43defe6d`

```dockerfile
```

-	Layers:
	-	`sha256:22aaf7c44e0facb77377dc2586ad702453820ccc9bac898923138e958f5372d8`  
		Last Modified: Tue, 03 Feb 2026 03:22:27 GMT  
		Size: 7.4 MB (7399570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:257c69abd5f15ac4136132c77126680efcd6ff794172153bcf893bcab754b6a3`  
		Last Modified: Tue, 03 Feb 2026 03:22:26 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aedb133f90e6b1cc27a85ac7489dcbd1e0183c35f43beee549e2aea546e9231d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278059819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff6e03da36407438ff0b0a8a5802004e025015bb05eedff9f7d304c8d0b482e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:24:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:16 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570ca0cb3a4e0ca09b8373c916c87023cb961c1c473aa0ab40579548ef54c85`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc168afa3b243f1ffec97569e4c9688bf17a3973f7271549d27c881612c5d18`  
		Last Modified: Tue, 03 Feb 2026 03:24:53 GMT  
		Size: 69.7 MB (69692878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841adc0d6b81349bb04e72c9fca692ad9777c34747e12cbd13c1d592b295b805`  
		Last Modified: Tue, 03 Feb 2026 03:24:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af18dd52e49ca73acd2086d93fb0e378f417b86e68b263bebd7b334d299591d`  
		Last Modified: Tue, 03 Feb 2026 03:24:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:80e0fad9a06abe2be84c156db49b67c91d7aa522553f6686182d8aea9a717975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7420565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b7b5725100c6a410d10a4d62c4573e6f3f2bd3c7b80611e01732b8794e70b1`

```dockerfile
```

-	Layers:
	-	`sha256:e81935ff434cd5eb6141ebfa280ebbbc2085d854eb1fa45f101b7cc2bb3930b6`  
		Last Modified: Tue, 03 Feb 2026 03:24:51 GMT  
		Size: 7.4 MB (7404669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818d0d1d207934add8a954df57600c9fe2068803ce3897df453d40e8863b0213`  
		Last Modified: Tue, 03 Feb 2026 03:24:50 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
