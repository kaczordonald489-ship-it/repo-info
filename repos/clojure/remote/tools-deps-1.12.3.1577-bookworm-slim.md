## `clojure:tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:17dd90bca8eaaaba3110a1f333bb1834594524b10063862a0155322db430679d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e1a2850a833a6a16a8e203a3ae66a7616182cdcc7fb1222511b4ff628a9761c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189954867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fd32aaced88f3f360a0ca09fc7011b3333dfc9593be34f7ddd0a9d55fe77ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:17:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:17:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:17:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:17:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:17:04 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:17:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:17:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:17:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:17:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:17:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff1c0be36fcdf55678c1a36b8b988ca7381fda7d5c9967e90859cad6317fc4a`  
		Last Modified: Tue, 18 Nov 2025 06:17:52 GMT  
		Size: 92.0 MB (92045299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56982e0b1c7c139e2752a6f9498a0748e8147ab20e4d9a1be815ace2b1b09c03`  
		Last Modified: Tue, 18 Nov 2025 06:17:49 GMT  
		Size: 69.7 MB (69680083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050ace3baddab2c71556252d2580b6be2f18455007af2bd41922092476e4ae22`  
		Last Modified: Tue, 18 Nov 2025 06:17:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2211ec2c25b332f106f47ab0c2afb0650bc27b5f9a954e73403fd45ba39066`  
		Last Modified: Tue, 18 Nov 2025 06:17:46 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4d3413d948cac70e1a0ba57f50770d78eebbd3336659980771471278252c07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a724ef0d45f6563150a254b5c92acd6205c873977793480d6f618c51bb51a8f3`

```dockerfile
```

-	Layers:
	-	`sha256:fce5123db183e4fe9832c73e15071483446cba55c4a327e3942a70c15d077485`  
		Last Modified: Tue, 18 Nov 2025 07:47:13 GMT  
		Size: 5.1 MB (5064748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e0788f6558ed4e17cbd61325cb72567afbdf7fd679f127cd2275607d107b2bf`  
		Last Modified: Tue, 18 Nov 2025 07:47:14 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b9f3b5ab2b38824beabaa79bea81ef6ec63fc98e1d85ea75cde131bce03ba25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188715895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9f34e01c760d9d8a4c130fb6f6710d58df5f73fb271715f5084a27424b920b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:15:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:15:08 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:15:08 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:15:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:15:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:15:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:15:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:15:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb83e9201fd017e2fe023862f6c063f32e66685142d01466d6e62d5ee94ec6`  
		Last Modified: Tue, 18 Nov 2025 05:15:58 GMT  
		Size: 91.1 MB (91052529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573906ddb110a11a4300b5adfbfc3b08b5460b93d6b75fa59f7937c599d6cadc`  
		Last Modified: Tue, 18 Nov 2025 05:16:03 GMT  
		Size: 69.6 MB (69560121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd419da9932f4d4deff2f6d08def4544db988a6adbb62abff7222066fedc3786`  
		Last Modified: Tue, 18 Nov 2025 05:15:52 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca589c0d9d055ef6c4c4f29ffcb76849d24502f84b9eaf3dc28e1a1d3ac187`  
		Last Modified: Tue, 18 Nov 2025 05:15:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf6f6550594638595f781c1450b810c63b2387714d6f0dd6cd590fa6c3ca59ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa34b8a00c15de89891ba8d2bc74919bc963cc1685fa67ee2392a8d13a1584aa`

```dockerfile
```

-	Layers:
	-	`sha256:b2547221b2cfa48cf4174baba7d4ddd83aa97ca72f1d5b460989964278f88561`  
		Last Modified: Tue, 18 Nov 2025 07:47:18 GMT  
		Size: 5.1 MB (5070530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef56c7863a4419956e74cb25a0326933ec5255e23a41238161bd03493c99615`  
		Last Modified: Tue, 18 Nov 2025 07:47:21 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3fb8101cb9ff2ee530ac77e7fcb28da7afeca92bd8cd9d6fae0f4fdb8144fb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199193869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7e568e4daa2a9d2c1e28c88b4f0703a318ba8860de50e24c50d00b9f48ed08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:40:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:40:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:40:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:40:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:40:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:43:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:43:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:43:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:43:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:43:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a439639461396cfe319eb84b16332b2671db8af4803837382350f840521b8ddd`  
		Last Modified: Tue, 18 Nov 2025 06:41:34 GMT  
		Size: 91.6 MB (91610763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443affb70f9ad5de78806a9bbd7d65fc5464c435aa60f4d78c669a8f99cd80c`  
		Last Modified: Tue, 18 Nov 2025 06:44:47 GMT  
		Size: 75.5 MB (75513240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccbe88b9f8129cbfdf4ef5c2871a4e795b9ccf04147f87e8ab936b9e7ba7860`  
		Last Modified: Tue, 18 Nov 2025 06:44:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b3657fb80852294249e4af0f42d25fa2929d0caf2a303b49b3f09ba84f3a9f`  
		Last Modified: Tue, 18 Nov 2025 06:44:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:934fb99fd9e155648ef379a8b462d4a5c6dfc68dc510da9cd1411ec286a33c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743a47cd1ebbdd8fe4ec0001dc8ddb42bfc6211eaae6e48e6f34bda687d8ef8b`

```dockerfile
```

-	Layers:
	-	`sha256:d15c8603f35321d8a3757ffb9676648bfff966ba9889c1f1d5b0d38b21852536`  
		Last Modified: Tue, 18 Nov 2025 07:47:25 GMT  
		Size: 5.1 MB (5071216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211a5896f075d9b41ee9be2e4a5f34b162103ca2f45db2f5789ad48715ffdf14`  
		Last Modified: Tue, 18 Nov 2025 07:47:26 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:74f6f12be18747c526b04270fc764251233c1b8c78eeceb2d33e6cca6b566331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183586779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b195300959ccd4d5610884eeb65d66f63d003ab146a4bce9649d361faeacf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:33:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:33:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:33:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:33:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:33:25 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:33:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:33:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:33:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:33:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:33:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d02554740040e771c42d0cabc77b70e48ec4d15b1b2f09129177f138744d7`  
		Last Modified: Tue, 18 Nov 2025 05:34:38 GMT  
		Size: 88.2 MB (88210715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88424b8034a9157dfc3e86efe4806bd22cb4a4e128de1847d5a48559c96bf145`  
		Last Modified: Tue, 18 Nov 2025 05:34:32 GMT  
		Size: 68.5 MB (68490632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96844a5d0a0d803cdc1c00cc60edbbab6f1205ef7b814fb30db37c38b1c5bbfa`  
		Last Modified: Tue, 18 Nov 2025 05:34:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9474de7cd9319693acd81650243b1945cff6306f147316687fb6aa4c87a79e`  
		Last Modified: Tue, 18 Nov 2025 05:34:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e52f792bfcd20fe2c63c640ea941e58671b88ef2a33f88b2ea33eb76b719bfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3958e90d1becdc524a9167c6e2d8146271c4a537e25056319856bb640c7c6cd`

```dockerfile
```

-	Layers:
	-	`sha256:aef7ddc9fd6e355fab73e8df44e5c09e540307db87314260ad33a860bef2c680`  
		Last Modified: Tue, 18 Nov 2025 07:47:31 GMT  
		Size: 5.1 MB (5058617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1becd66e248ff0dd56a95654ab8367b977301c35b678c0259682b00d198b9ad`  
		Last Modified: Tue, 18 Nov 2025 07:47:31 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
